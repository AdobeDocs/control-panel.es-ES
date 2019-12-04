---
title: Lista blanca de IP
description: Obtenga más información sobre la lista de direcciones permitidas IP en el Panel de control, por ejemplo, el acceso
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Lista blanca de IP {#ip-whitelisting}

>[!CAUTION]
>
>Esta función solo está disponible para instancias de Campaign Classic.

## Acerca de la lista blanca de IP {#about-ip-whitelisting}

De forma predeterminada, la instancia de Adobe Campaign Classic no es accesible desde varias direcciones IP.

Si su dirección IP no se ha admitido en la lista de direcciones permitidas, no podrá iniciar sesión en la instancia desde esta dirección. Del mismo modo, es posible que no pueda conectar una API a su instancia de centro de mensajes o de marketing si la dirección IP no se ha incluido explícitamente en la lista blanca con la instancia.

El Panel de control permite configurar nuevas conexiones a las instancias mediante la lista blanca de intervalos de direcciones IP. Para ello, siga los pasos que se describen a continuación.

Una vez que las direcciones IP estén en la lista de direcciones permitidas, puede crear y vincular operadores de campaña a ellos para que los usuarios puedan acceder a la instancia.

## Prácticas recomendadas {#best-practices}

Asegúrese de seguir las recomendaciones y limitaciones que se indican a continuación al incluir direcciones IP en la lista blanca en el Panel de control.

* **No habilite el acceso IP a todos los tipos** de acceso si no desea que la dirección IP se conecte a los servidores RT o a la zona de seguridad de AEM.
* **Si habilitó temporalmente el acceso a su instancia para una dirección** IP, asegúrese de eliminar las direcciones IP de las direcciones IP permitidas una vez que ya no necesite conectarse a su instancia.
* **No recomendamos que se incluyan en la lista blanca las direcciones IP de los lugares** públicos (aeropuertos, hoteles, etc.). Utilice la dirección VPN de su empresa para mantener su instancia segura en todo momento.

## Lista blanca de direcciones IP para el acceso a instancias {#whistelisting-ip-addresses}

Para incluir direcciones IP en la lista blanca, siga estos pasos:

1. Abra la ficha **[!UICONTROL Instances Settings card]** para acceder a la lista de direcciones permitidas IP y haga clic en **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Si la tarjeta Configuración de instancia no está visible en la página de inicio del Panel de control, significa que el identificador de organización de IMS no está asociado a ninguna instancia de Adobe Campaign Classic

   ![](assets/ip_whitelist_list1.png)

1. Complete la información del intervalo IP que desee incluir en la lista blanca como se describe a continuación.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**:: Instancias en las que las direcciones IP podrán conectarse. Se pueden manipular varias instancias al mismo tiempo. Por ejemplo, la lista blanca de IP se puede realizar en las instancias Producción y Fase a través del mismo paso.
   * **[!UICONTROL IP Range]**:: Intervalo IP que desea incluir en la lista blanca, en formato CIDR. Tenga en cuenta que un intervalo IP no puede superponerse a un intervalo de la lista blanca existente. En ese caso, primero elimine el rango que contiene la IP superpuesta.
   >[!NOTE]
   >
   >CIDR (Enrutamiento entre dominios sin clase) es el formato admitido al agregar intervalos de IP con la interfaz del Panel de control. La sintaxis consiste en una dirección IP, seguida de un carácter '/' y un número decimal. El formato y su sintaxis se detallan en [este artículo](https://whatismyipaddress.com/cidr).
   >
   >Puede buscar en Internet herramientas gratuitas en línea que le ayudarán a convertir la gama de IP que tiene en mano al formato CIDR.

   * **!UICONTROL Label]**:: Etiqueta que se mostrará en la lista de direcciones IP permitidas.
   * **[!UICONTROL Name]**:: El nombre debe ser único para el tipo de acceso, la instancia (en caso de conexión API externa) y la dirección IP.


1. Especifique el tipo de acceso que desea conceder a las direcciones IP:

   * **[!UICONTROL Campaign Console Access]**:: Se permitirá que las direcciones IP se conecten a la consola de Campaign Classic. Tenga en cuenta que el acceso a la consola solo está habilitado para instancias de Marketing. No se permite el acceso a las instancias de MID y RT y, por tanto, no se habilita.
   * **[!UICONTROL AEM connection]**:: Se permitirá que las direcciones IP de AEM especificadas se conecten a la instancia de Marketing.
   * **[!UICONTROL External API connection]**:: Se permitirá que las API externas con las direcciones IP especificadas se conecten a la instancia de Marketing y/o Centro de mensajes (RT). Tenga en cuenta que la conexión a la consola de instancias de RT no está habilitada.
   ![](assets/ip_whitelist_acesstype.png)

1. Haga clic en el botón **.[!UICONTROL Save]** El intervalo de IP se agrega a la lista de direcciones IP permitidas.

   ![](assets/ip_whitelist_added.png)

Para eliminar los rangos de IP permitidos, selecciónelos y haga clic en el **[!UICONTROL Delete IP range]** botón .

**Temas relacionados:**
* [Lista blanca de IP (vídeo de tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-whitelisting.html)
* [Vinculación de una zona de seguridad a un operador](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
