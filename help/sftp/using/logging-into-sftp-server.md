---
product: campaign
solution: Campaign
title: Inicio de sesión en el servidor SFTP
description: Obtenga información sobre cómo iniciar sesión en el servidor SFTP
feature: Control Panel
role: Architect
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# Inicio de sesión en el servidor SFTP {#logging-into-sft-server}

Los pasos siguientes detallan cómo conectar el servidor SFTP a través de la aplicación de cliente SFTP.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](https://video.tv.adobe.com/v/27263?quality=12)

Antes de iniciar sesión en el servidor, asegúrese de que:

* El servidor SFTP es **alojado por Adobe**.
* Se ha configurado el **nombre de usuario** para el servidor. Puede comprobar esta información directamente en el Panel de control de Campaign, en la **Administración de claves** en la tarjeta SFTP.
* Tiene un **par de clave pública y privada** para iniciar sesión en el servidor SFTP. Consulte [esta sección](../../sftp/using/key-management.md) para obtener más información sobre cómo añadir la clave SSH.
* Su **se ha añadido la dirección IP pública a la lista de permitidos** en el servidor SFTP. Si no es así, consulte [esta sección](../../sftp/using/ip-range-allow-listing.md) para obtener más información sobre cómo agregar su rango de IP a la lista de permitidos.
* Tiene acceso a un **Software de cliente SFTP**. Puede consultar al departamento de TI de la aplicación cliente SFTP que recomienden usar o buscar una en Internet si las directivas de su empresa permiten esto.

Para conectarse al servidor SFTP, siga estos pasos:

1. Inicie el Panel de control de Campaign y, a continuación, seleccione la **[!UICONTROL Key Management]** en la ficha **[!UICONTROL SFTP]** tarjeta.

   ![](assets/sftp_card.png)

1. Inicie la aplicación de cliente SFTP, copie y pegue la dirección del servidor desde el Panel de control de Campaign, seguido de &quot;campaign.adobe.com&quot; y, a continuación, rellene el nombre de usuario.

   ![](assets/do-not-localize/connect1.png)

1. En el **[!UICONTROL SSH Private Key]** seleccione el archivo de clave privada almacenado en el equipo. Corresponde a un archivo de texto que tiene el mismo nombre que su clave pública, sin la extensión &quot;.pub&quot; (por ejemplo, &quot;habilitar&quot;).

   ![](assets/do-not-localize/connect2.png)

   La variable **[!UICONTROL Password]** se rellena automáticamente con la clave privada del archivo.

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
