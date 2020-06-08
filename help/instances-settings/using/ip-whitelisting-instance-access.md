---
title: Listas blancas de IP
description: Obtenga más información sobre las listas blancas de direcciones IP en el Panel de control de Campaign para acceso a instancias
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5
workflow-type: ht
source-wordcount: '705'
ht-degree: 100%

---


# Listas blancas de IP {#ip-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="Acerca de las listas blancas de IP"
>abstract="Administre las listas blancas de direcciones permitidas IP para acceder a sus instancias."
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="Ver vídeo de demostración"

>[!IMPORTANT]
>
>Esta función solo está disponible para instancias de Campaign Classic.

## Acerca de las listas blancas de IP {#about-ip-whitelisting}

De forma predeterminada, la instancia de Adobe Campaign Classic no es accesible desde varias direcciones IP.

Si su dirección IP no se ha incluido en la lista blanca de direcciones, no podrá iniciar sesión en la instancia desde esta dirección. Del mismo modo, es posible que no pueda conectar una API a su instancia de centro de mensajes o de marketing si la dirección IP no se ha incluido explícitamente en la lista blanca con la instancia.

El Panel de control de Campaign permite configurar nuevas conexiones a las instancias mediante la lista blanca de rangos de direcciones IP. Para realizar esto, siga los pasos descritos a continuación.

Una vez que las direcciones IP estén en la lista blanca de direcciones, puede crear y vincular operadores de Campaign a ellos para que los usuarios puedan acceder a la instancia.

## Prácticas recomendadas {#best-practices}

Asegúrese de seguir las recomendaciones y limitaciones que se indican a continuación al incluir direcciones IP en la lista blanca en el Panel de control.

* **No habilite el acceso IP a todos los tipos de acceso** si no desea que la dirección IP se conecte a los servidores RT o a la zona de seguridad de AEM.
* **Si ha habilitado temporalmente el acceso a su instancia para una dirección IP**, asegúrese de eliminar las direcciones IP de las direcciones IP en la lista blanca una vez que ya no necesite conectarse a su instancia.
* **No recomendamos que se incluyan en la lista blanca las direcciones IP de lugares públicos** (aeropuertos, hoteles, etc.). Utilice su dirección VPN de la compañía para mantener la seguridad de su instancia en todo momento.

## Lista blanca de direcciones IP para el acceso a instancias {#whistelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="Adición de un nuevo rango de IP"
>abstract="Defina el rango IP que desea incluir en la lista blanca para conectarse a su instancia."

Para incluir direcciones IP en la lista blanca, siga estos pasos:

1. Abra la pestaña **[!UICONTROL Instances Settings card]** para acceder a la lista blanca de direcciones IP y haga clic en **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Si la tarjeta Configuración de instancia no está visible en la página de inicio del Panel de control, el ID de organización de IMS no está asociado a ninguna instancia de Adobe Campaign Classic

   ![](assets/ip_whitelist_list1.png)

1. Complete la información del rango IP que desee incluir en la lista blanca como se describe a continuación.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**: instancias en las que las direcciones IP podrán conectarse. Se pueden manipular varias instancias al mismo tiempo. Por ejemplo, la lista blanca de IP se puede realizar en las instancias Producción y Fase a través del mismo paso.
   * **[!UICONTROL IP Range]**: rango IP que desea incluir en la lista blanca en formato CIDR. Tenga en cuenta que un rango IP no puede superponerse a un intervalo de la lista blanca existente. En ese caso, primero elimine el rango que contiene la IP superpuesta.
   >[!NOTE]
   >
   >CIDR (enrutamiento entre dominios sin clase) es el formato admitido al agregar intervalos de IP con la interfaz del Panel de control. La sintaxis consiste en una dirección IP, seguida de / y un número decimal. El formato y su sintaxis se detallan en [este artículo](https://whatismyipaddress.com/cidr).
   >
   >Puede buscar en Internet herramientas gratuitas en línea que le ayudarán a convertir la gama de IP al formato CIDR.

   * **[!UICONTROL Label]**: etiqueta que se mostrará en la lista blanca de direcciones IP.
   * **[!UICONTROL Name]**: el nombre debe ser único para el tipo de acceso, la instancia (en caso de conexión API externa) y la dirección IP.


1. Especifique el tipo de acceso que desea conceder a las direcciones IP:

   * **[!UICONTROL Campaign Console Access]**: se permitirá que las direcciones IP se conecten a la Consola de Campaign Classic. Tenga en cuenta que el acceso a la consola solo está habilitado para instancias de Marketing. No se permite el acceso a las instancias de MID y RT y, por tanto, no se habilita.
   * **[!UICONTROL AEM connection]**: se permitirá que las direcciones IP de AEM especificadas se conecten a la instancia de Marketing.
   * **[!UICONTROL External API connection]**: se permitirá que las API externas con las direcciones IP especificadas se conecten a la instancia de Marketing y/o Centro de mensajes (RT). Tenga en cuenta que la conexión a la consola de instancias de RT no está habilitada.
   ![](assets/ip_whitelist_acesstype.png)

1. Haga clic en el botón **[!UICONTROL Save]**. El intervalo de IP se agrega a la lista de direcciones IP en la lista blanca de direcciones.

   ![](assets/ip_whitelist_added.png)

Para eliminar los rangos de IP en la lista blanca, selecciónelos y haga clic en el botón **[!UICONTROL Delete IP range]** .

**Temas relacionados:**
* [Listas blancas de IP (tutorial en vídeo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-whitelisting.html)
* [Vinculación de una zona de seguridad a un operador](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
