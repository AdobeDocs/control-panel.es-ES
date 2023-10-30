---
product: campaign
solution: Campaign
title: Inicio de sesión en el servidor SFTP
description: Obtenga información sobre cómo iniciar sesión en el servidor SFTP
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# Inicio de sesión en el servidor SFTP {#logging-into-sft-server}

Los pasos siguientes detallan cómo conectar el servidor SFTP a través de la aplicación cliente SFTP.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](https://video.tv.adobe.com/v/27263?quality=12)

Antes de iniciar sesión en el servidor, asegúrese de que:

* El servidor SFTP está **alojado por el Adobe**.
* Se ha configurado el **nombre de usuario** para el servidor. Puede comprobar esta información directamente en el Panel de control de Campaign, en la **Administración de claves** de la tarjeta SFTP.
* Tiene un **par de claves pública y privada** para iniciar sesión en el servidor SFTP. Consulte [esta sección](../../sftp/using/key-management.md) para más información sobre cómo añadir la clave SSH.
* Su **se ha añadido una dirección IP pública a la lista de permitidos** en el servidor SFTP. Si no es así, consulte [esta sección](../../sftp/using/ip-range-allow-listing.md) para obtener más información sobre cómo añadir el intervalo de IP a la lista de permitidos.
* Tiene acceso a un **Software de cliente SFTP**. Puede consultar con su departamento de TI la aplicación cliente SFTP que recomienden utilizar, o buscar una en Internet si las políticas de su empresa lo permiten.

Para conectarse al servidor SFTP, siga estos pasos:

1. Inicie el Panel de control de Campaign y seleccione la opción **[!UICONTROL Key Management]** de la pestaña **[!UICONTROL SFTP]** Tarjeta de.

   ![](assets/sftp_card.png)

1. Inicie la aplicación cliente SFTP, copie y pegue la dirección del servidor desde la Panel de control de Campaign, seguida de &quot;campaign.adobe.com&quot; y escriba el nombre de usuario.

   ![](assets/do-not-localize/connect1.png)

1. En el **[!UICONTROL SSH Private Key]** , seleccione el archivo de clave privada almacenado en el equipo. Corresponde a un archivo de texto que tiene el mismo nombre que la clave pública, sin la extensión &quot;.pub&quot; (por ejemplo, &quot;enable&quot;).

   ![](assets/do-not-localize/connect2.png)

   El **[!UICONTROL Password]** El campo se rellena automáticamente con la clave privada del archivo.

   ![](assets/do-not-localize/connect3.png)

   Puede comprobar que la clave que intenta utilizar esté guardada en la Panel de control de Campaign comparando la huella de la clave privada o pública con la huella de las claves que aparecen en la pestaña Administración de claves de la tarjeta SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Si utiliza un equipo Mac, puede ver la huella digital de la clave privada almacenada en el equipo ejecutando este comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Una vez completada toda la información, haga clic en **[!UICONTROL Connect]** para iniciar sesión en el servidor SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
