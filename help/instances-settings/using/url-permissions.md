---
title: Permisos de URL
description: Obtenga información sobre cómo administrar los permisos de URL en el Panel de control
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# Permisos de URL {#url-permissions}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_urlpermissions&quot;
>title=&quot;Acerca de los permisos de URL&quot;
>abstract=&quot;Administre las direcciones URL con las que se pueden conectar las instancias de Adobe Campaign&quot;.
>extra-url=&quot;https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4&quot; text=&quot;Ver vídeo de demostración&quot;

>[!CAUTION]
>
>Esta función solo está disponible para instancias de Campaign Classic.

## Acerca de los permisos de URL {#about-url-permissions}

Lista predeterminada de direcciones URL a las que pueden llamar los códigos JavaScript (flujos de trabajo, etc.) las instancias de Campaign Classic están limitadas. Son direcciones URL que permiten que las instancias funcionen correctamente.

De forma predeterminada, las instancias no pueden conectarse a direcciones URL externas. El Panel de control le permite agregar algunas direcciones URL externas a la lista de direcciones URL autorizadas, para que la instancia pueda conectarse a ellas. Esto le permite conectar las instancias de Campaign a sistemas externos como, por ejemplo, servidores SFTP o sitios web para habilitar la transferencia de datos o archivos.

Una vez que se agrega una URL, se hace referencia a ella en el archivo de configuración de la instancia (serverConf.xml).

**Temas relacionados:**

* [Configuración del servidor de campañas](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html)
* [Protección de conexión saliente](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Outgoing_connection_protection)
* [Adición de permisos de URL (vídeo de tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/adding-url-permissions.html)

## Prácticas recomendadas {#best-practices}

* No conecte la instancia de Campaign a sitios web o servidores a los que no tenga intención de conectarse.
* Elimine las direcciones URL con las que ya no esté trabajando. Sin embargo, tenga en cuenta que, si otra sección de su empresa sigue conectándose a la dirección URL que eliminó, nadie podrá volver a utilizarla.
* El Panel de control admite los protocolos **http**, **https** y **sftp** . La introducción de direcciones URL o protocolos no válidos producirá errores.

## Administración de permisos de URL {#managing-url-permissions}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_url_add&quot;
>title=&quot;Agregar nueva dirección URL&quot;
>abstract=&quot;Agregue direcciones URL para permitir conexiones con la instancia de Campaign&quot;.

Para agregar una dirección URL a la que se pueda conectar su instancia, siga estos pasos:

1. Abra la **[!UICONTROL Instances Settings]** tarjeta para acceder a la **[!UICONTROL URL Permissions]** ficha.

   >[!NOTE]
   >
   >Si la tarjeta Configuración de instancia no está visible en la página de inicio del Panel de control, significa que el identificador de organización de IMS no está asociado a ninguna instancia de Adobe Campaign Classic
   >
   >La ficha Permisos <b><span class="uicontrol">de</span></b> URL muestra todas las direcciones URL externas a las que se puede conectar su instancia. Esta lista no incluye las direcciones URL necesarias para que Campaign funcione (por ejemplo, conexiones entre elementos de infraestructura).

1. Seleccione en el panel izquierdo la instancia que desee y haga clic en el **[!UICONTROL Add new URL]** botón.

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >Todas las instancias de campaña se muestran en la lista del panel izquierdo.
   >
   >Como la administración de permisos de URL está dedicada únicamente a instancias de Campaign Classic, se muestra el mensaje &quot;Instancia no aplicable&quot; si selecciona una instancia de Campaign Standard.

1. Escriba la dirección URL para autorizar, con su protocolo asociado (http, https o sftp).

   >[!NOTE]
   >
   >Es posible autorizar varias instancias para conectarse a la dirección URL. Para ello, agréguelas directamente desde el campo Instancia(s) escribiendo su primera letra.

   ![](assets/add_url2.png)

1. La dirección URL se agrega a la lista y ahora puede conectarse a ella.

   >[!NOTE]
   >
   >La variable &quot;/.*&quot; caracteres se agregan automáticamente al final de la dirección URL que introduzca después de validarla, para cubrir todas las subpáginas de la página introducida.

   ![](assets/add_url_listnew.png)

Puede eliminar una dirección URL en cualquier momento seleccionándola y haciendo clic en el **[!UICONTROL Delete URL]** botón.

Tenga en cuenta que, si elimina una dirección URL, su instancia no podrá volver a llamarla.

## Preguntas frecuentes {#common-questions}

**He agregado una nueva dirección URL, pero mi instancia sigue sin poder conectarse a esa dirección URL. ¿Por qué?**

En algunos casos, las direcciones URL que intenta conectar requieren una lista blanca, una entrada de contraseña u otra forma de autenticación. El Panel de control no administra autenticación adicional.
