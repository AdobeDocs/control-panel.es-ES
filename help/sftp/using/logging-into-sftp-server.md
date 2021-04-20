---
product: campaign
solution: Campaign
title: Inicio de sesión en el servidor SFTP
description: Obtenga información sobre cómo iniciar sesión en el servidor SFTP
feature: Control Panel
role: Architect
level: Experienced
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 7%

---


# Inicio de sesión en el servidor SFTP {#logging-into-sft-server}

Los pasos siguientes detallan cómo conectar el servidor SFTP a través de la aplicación de cliente SFTP.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](https://video.tv.adobe.com/v/27263?quality=12)

Antes de iniciar sesión en el servidor, asegúrese de que:

* El servidor SFTP está **alojado por Adobe**.
* Se ha configurado el **nombre de usuario** para el servidor. Puede comprobar esta información directamente en el Panel de control de Campaign, en la pestaña **Administración de claves** de la tarjeta SFTP.
* Tiene un **par de claves públicas y privadas** para iniciar sesión en el servidor SFTP. Consulte [esta sección](../../sftp/using/key-management.md) para obtener más información sobre cómo agregar la clave SSH.
* Su **dirección IP pública se ha agregado a la lista de permitidos** en el servidor SFTP. Si no es así, consulte [esta sección](../../sftp/using/ip-range-allow-listing.md) para obtener más información sobre cómo agregar su rango de IP a la lista de permitidos.
* Tiene acceso a un **software cliente SFTP**. Puede consultar al departamento de TI de la aplicación cliente SFTP que recomienden usar o buscar una en Internet si las directivas de su empresa permiten esto.

Para conectarse al servidor SFTP, siga estos pasos:

1. Inicie el Panel de control de Campaign y, a continuación, seleccione la pestaña **[!UICONTROL Key Management]** en la tarjeta **[!UICONTROL SFTP]** .

   ![](assets/sftp_card.png)

1. Inicie la aplicación de cliente SFTP, copie y pegue la dirección del servidor desde el Panel de control de Campaign, seguido de &quot;campaign.adobe.com&quot; y, a continuación, rellene el nombre de usuario.

   ![](assets/do-not-localize/connect1.png)

1. En el campo **[!UICONTROL SSH Private Key]**, seleccione el archivo de clave privada almacenado en el equipo. Corresponde a un archivo de texto que tiene el mismo nombre que su clave pública, sin la extensión &quot;.pub&quot; (por ejemplo, &quot;habilitar&quot;).

   ![](assets/do-not-localize/connect2.png)

   El campo **[!UICONTROL Password]** se rellena automáticamente con la clave privada del archivo.

   ![](assets/do-not-localize/connect3.png)

   Puede comprobar que la clave que intenta utilizar se guarde en el Panel de control de Campaign comparando la huella digital de la clave privada o pública con la huella digital de las claves que aparecen en la pestaña Administración de claves de la tarjeta SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Si utiliza un equipo Mac, puede ver la huella digital de la clave privada almacenada en el equipo ejecutando este comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Una vez que se haya rellenado toda la información, haga clic en **[!UICONTROL Connect]** para iniciar sesión en el servidor SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
