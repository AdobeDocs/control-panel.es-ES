---
product: campaign
solution: Campaign
title: Lista de IP permitidas
description: Obtenga información sobre cómo agregar direcciones IP a la lista de permitidos en el Panel de control para obtener acceso a instancias.
feature: Control Panel, Access Management
role: Admin
level: Intermediate
exl-id: 1d1eeff8-969e-4529-b947-2a68defb8d13
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '794'
ht-degree: 100%

---

# Lista de IP permitidas {#ip-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="Acerca de las listas de IP permitidas"
>abstract="Añada direcciones IP a la lista de permitidos para acceder a sus instancias."
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="Ver vídeo de demostración"

## Acerca de las listas de IP permitidas {#about-ip-allow-listing}

>[!IMPORTANT]
>
>Esta funcionalidad solo está disponible para las instancias de las versiones 7 y 8 de Campaign.

De forma predeterminada, la instancia de Adobe Campaign no es accesible desde varias direcciones IP.

Si su dirección IP no se ha incluido en la lista de permitidos, no podrá iniciar sesión en la instancia desde esa dirección. Del mismo modo, es posible que no pueda conectar una API a su instancia de centro de mensajes o de marketing si la dirección IP no se ha incluido explícitamente en la lista de permitidos con la instancia.

El Panel de control le permite configurar nuevas conexiones a las instancias añadiendo rangos de direcciones IP a la lista de permitidos. Para realizar esto, siga los pasos descritos a continuación.

Una vez que las direcciones IP estén en la lista de permitidos, puede crear y vincular operadores de Campaign a ellas para que los usuarios puedan acceder a la instancia.

![](assets/do-not-localize/how-to-video.png) [Descubra esta funcionalidad en vídeo](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/ip-allow-listing.html?lang=es#instance-settings)

## Prácticas recomendadas {#best-practices}

Asegúrese de seguir las recomendaciones y limitaciones que se indican a continuación al incluir direcciones IP en la lista de permitidos en el Panel de control-

* **No habilite el acceso IP a todos los tipos de acceso** si no desea que la dirección IP se conecte a los servidores RT o a la zona de seguridad de AEM.
* **Si ha habilitado temporalmente el acceso a su instancia para una dirección IP**, asegúrese de eliminar las direcciones IP de la lista de permitidos una vez que ya no necesite conectarse a su instancia.
* **No recomendamos añadir direcciones IP de lugares públicos a la lista de permitidos** (aeropuertos, hoteles, etc.). Utilice su dirección VPN de la compañía para mantener la seguridad de su instancia en todo momento.

## Añadir direcciones IP a la lista de permitidos para el acceso a instancias {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="Configuración de rango de IP"
>abstract="Defina el rango de IP que desea agregar a la lista de permitidos para conectarse a la instancia."

>[!NOTE]
>
>Si la tarjeta **[!UICONTROL Configuración de instancias]** no está visible en la página de inicio del Panel de control, significa que su [ID de la organización](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=es) no está asociada a ninguna instancia de Adobe Campaign v7/v8.

Para añadir direcciones IP a la lista de permitidos, siga estos pasos:

1. Abra la **[!UICONTROL tarjeta de configuración de instancias]** para acceder a la pestaña con el listado de IP permitidas y, a continuación, haga clic en **[!UICONTROL Añadir nuevo rango de IP]**.



   ![](assets/ip_whitelist_list1.png)

1. Complete la información del rango de IP que desee incluir en la lista de permitidos como se describe a continuación.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instancia(s)]**: instancias a las que podrán conectarse las direcciones IP. Se pueden manipular varias instancias al mismo tiempo. Por ejemplo, la adición de IP a lista de permitidos se puede realizar en las instancias Production y Stage siguiendo el mismo paso.
   * **[!UICONTROL Rango de IP]**: el rango de IP que desea agregar a la lista de permitidos, en formato CIDR. Tenga en cuenta que un rango de IP no puede superponerse a un intervalo existente en la lista de permitidos. En ese caso, primero elimine el rango que contiene la IP superpuesta.

   >[!NOTE]
   >
   >CIDR (enrutamiento entre dominios sin clase) es el formato admitido al agregar intervalos de IP con la interfaz del Panel de control. La sintaxis consiste en una dirección IP, seguida de / y un número decimal. El formato y su sintaxis se detallan en [este artículo](https://whatismyipaddress.com/cidr).
   >
   >Puede buscar en Internet herramientas gratuitas en línea que le ayudarán a convertir el rango IP del que dispone al formato CIDR.

   * **[!UICONTROL Etiqueta]**: etiqueta que se mostrará en la lista de permitidos.
   * **[!UICONTROL Nombre]**: el nombre debe ser único para el tipo de acceso, la instancia (en caso de conexión API externa) y la dirección IP.

1. Especifique el tipo de acceso que desea conceder a las direcciones IP:

   * **[!UICONTROL Acceso a Campaign Console]**: las direcciones IP que se podrán conectar a la consola de cliente de Campaign. Tenga en cuenta que el acceso a la consola solo está habilitado para instancias de Marketing. No se permite el acceso a las instancias de MID y RT y, por tanto, no se habilita.
   * **[!UICONTROL Conexión de AEM]**: se permitirá que las direcciones IP de AEM especificadas se conecten a la instancia de Marketing.
   * **[!UICONTROL Conexión de API externa]**: se permitirá que las API externas con las direcciones IP especificadas se conecten a la instancia de Marketing y/o Centro de mensajes (RT). Tenga en cuenta que la conexión a la consola de instancias de RT no está habilitada.

   >[!NOTE]
   >
   >Si está utilizando una instancia con un modelo de alojamiento híbrido, solo podrá añadir direcciones IP en “Conexión de API externa” para las instancias de MID y RT. 

   ![](assets/ip_whitelist_acesstype.png)

1. Haga clic en el botón **[!UICONTROL Save.]** El rango de IP se agrega a la lista de permitidos.

   <!--![](assets/ip_whitelist_added.png)-->

De forma predeterminada, la instancia de Adobe Campaign no es accesible desde varias direcciones IP.

Para eliminar uno o varios rangos de IP de la lista de permitidos, selecciónelos y, a continuación, haga clic en el botón **[!UICONTROL Eliminar rango de IP]**.

![](assets/ip_whitelist_delete.png)

**Temas relacionados:**

* [Vinculación de una zona de seguridad a un operador](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/additional-configurations/security-zones.html?lang=es#linking-a-security-zone-to-an-operator)
