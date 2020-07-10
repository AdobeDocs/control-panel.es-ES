---
title: Lista de IP permitidas
description: Obtenga información sobre cómo agregar direcciones IP a la lista de permitidos en el Panel de control para obtener acceso a instancias
translation-type: tm+mt
source-git-commit: abe22509e3389874e0b3586a99a1ad2d49681ed8
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 49%

---


# Lista de IP permitidas {#ip-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="Acerca del listado de permitidas por IP"
>abstract="Añada las direcciones IP a la lista de permitidos para acceder a las instancias."
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="Ver vídeo de demostración"

>[!IMPORTANT]
>
>Esta función solo está disponible para instancias de Campaign Classic.

## Acerca del listado de permitidas por IP {#about-ip-allow-listing}

De forma predeterminada, la instancia de Adobe Campaign Classic no es accesible desde varias direcciones IP.

Si su dirección IP no se ha agregado a la lista de permitidos, no podrá iniciar sesión en la instancia desde esta dirección. Del mismo modo, es posible que no pueda conectar una API a la instancia de centro de mensajes o de marketing si la dirección IP no se ha agregado a la lista de permitidos con la instancia de forma explícita.

El Panel de control permite configurar nuevas conexiones a las instancias mediante la adición de intervalos de direcciones IP a la lista de permitidos. Para realizar esto, siga los pasos descritos a continuación.

Una vez que las direcciones IP están en la lista de permitidos, puede crear y vincular los operadores de Campaña a ellos para que los usuarios puedan acceder a la instancia.

## Prácticas recomendadas {#best-practices}

Asegúrese de seguir las recomendaciones y limitaciones siguientes al agregar direcciones IP a la lista de permitidos en el Panel de control.

* **No habilite el acceso IP a todos los tipos de acceso** si no desea que la dirección IP se conecte a los servidores RT o a la zona de seguridad de AEM.
* **Si habilitó temporalmente el acceso a la instancia para una dirección** IP, asegúrese de eliminar las direcciones IP de la lista de permitidos una vez que ya no necesite conectarse a la instancia.
* **No recomendamos añadir direcciones IP de lugares públicos a la lista de permitidos** (aeropuertos, hoteles, etc.). Utilice su dirección VPN de la compañía para mantener la seguridad de su instancia en todo momento.

## Añadir direcciones IP a la lista de permitidos de acceso de instancia {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="Adición de un nuevo rango de IP"
>abstract="Defina el rango IP que desea agregar a la lista de permitidos para conectarse a la instancia."

Para agregar direcciones IP a la lista de permitidos, siga estos pasos:

1. Open the **[!UICONTROL Instances Settings card]** to access the IP allow listing tab, then click **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Si la tarjeta Configuración de instancia no está visible en la página de inicio del Panel de control de Campaign, el ID de organización de IMS no está asociado a ninguna instancia de Adobe Campaign Classic

   ![](assets/ip_whitelist_list1.png)

1. Complete la información del intervalo IP que desee agregar a la lista de permitidos como se describe a continuación.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**: instancias en las que las direcciones IP podrán conectarse. Se pueden manipular varias instancias al mismo tiempo. Por ejemplo, la lista de permitidas por IP se puede realizar tanto en las instancias de Producción como de Etapa a través del mismo paso.
   * **[!UICONTROL IP Range]**:: Intervalo de IP que desea agregar a la lista de permitidos, en formato CIDR. Tenga en cuenta que un intervalo IP no puede superponerse a un intervalo existente en la lista de permitidos. En ese caso, primero elimine el rango que contiene la IP superpuesta.
   >[!NOTE]
   >
   >CIDR (enrutamiento entre dominios sin clase) es el formato admitido al agregar intervalos de IP con la interfaz del Panel de control. La sintaxis consiste en una dirección IP, seguida de / y un número decimal. El formato y su sintaxis se detallan en [este artículo](https://whatismyipaddress.com/cidr).
   >
   >Puede buscar en Internet herramientas gratuitas en línea que le ayudarán a convertir la gama de IP al formato CIDR.

   * **[!UICONTROL Label]**:: Etiqueta que se mostrará en la lista de permitidos.
   * **[!UICONTROL Name]**: el nombre debe ser único para el tipo de acceso, la instancia (en caso de conexión API externa) y la dirección IP.


1. Especifique el tipo de acceso que desea conceder a las direcciones IP:

   * **[!UICONTROL Campaign Console Access]**: se permitirá que las direcciones IP se conecten a la Consola de Campaign Classic. Tenga en cuenta que el acceso a la consola solo está habilitado para instancias de Marketing. No se permite el acceso a las instancias de MID y RT y, por tanto, no se habilita.
   * **[!UICONTROL AEM connection]**: se permitirá que las direcciones IP de AEM especificadas se conecten a la instancia de Marketing.
   * **[!UICONTROL External API connection]**: se permitirá que las API externas con las direcciones IP especificadas se conecten a la instancia de Marketing y/o Centro de mensajes (RT). Tenga en cuenta que la conexión a la consola de instancias de RT no está habilitada.
   ![](assets/ip_whitelist_acesstype.png)

1. Haga clic en el botón **[!UICONTROL Save]**. El intervalo IP se agrega a la lista de permitidos.

   ![](assets/ip_whitelist_added.png)

Para eliminar intervalos IP de la lista de permitidos, selecciónelos y haga clic en el **[!UICONTROL Delete IP range]** botón .

**Temas relacionados:**
* [Lista de IP permitidas (vídeo de tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-allow-listing.html)
* [Vinculación de una zona de seguridad a un operador](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)