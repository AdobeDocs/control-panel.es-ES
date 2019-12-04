---
title: Inicio de sesión en el servidor SFTP
description: Obtenga información sobre cómo iniciar sesión en el servidor SFTP
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Inicio de sesión en el servidor SFTP {#logging-into-sft-server}

Los pasos a continuación detallan cómo conectar el servidor SFTP a través de la aplicación cliente SFTP.

Antes de iniciar sesión en el servidor, asegúrese de que:

* El servidor SFTP está **alojado por Adobe**.
* Se ha configurado el **nombre de usuario** para el servidor. You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* Tiene un par **de claves pública y** privada para iniciar sesión en el servidor SFTP. Consulte [esta sección](../../sftp/using/key-management.md) para obtener más información sobre cómo agregar la clave SSH.
* La dirección IP **pública se ha incluido** en la lista de direcciones permitidas en el servidor SFTP. Si no es así, consulte [esta sección](../../sftp/using/ip-range-whitelisting.md) para obtener más información sobre cómo incluir en la lista de direcciones permitidas el intervalo de direcciones IP.
* Tiene acceso a un software **cliente** SFTP. Puede consultar al departamento de TI de la aplicación cliente SFTP que recomiende utilizar o buscar una en Internet si así lo permiten las políticas de su empresa.

Para conectarse al servidor SFTP, siga estos pasos:

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]** tab from the **[!UICONTROL SFTP]** card.

   ![](assets/fingerprintNEW2.png)

1. Inicie la aplicación cliente SFTP y, a continuación, copie y pegue la dirección del servidor desde el Panel de control, seguido de "campaign.adobe.com" y rellene el nombre de usuario.

   ![](assets/connect1.png)

1. En el **[!UICONTROL SSH Private Key]** campo, seleccione el archivo de clave privada almacenado en el equipo. Corresponde a un archivo de texto con el mismo nombre que la clave pública, sin la extensión ".pub" (por ejemplo, "habilitar").

   ![](assets/connect2.png)

   El **[!UICONTROL Password]** campo se rellena automáticamente con la clave privada del archivo.

   ![](assets/connect3.png)

   Puede comprobar que la clave que intenta utilizar se guarda en el Panel de control comparando la huella digital de la clave pública o privada con la huella digital de las claves que aparecen en la ficha Administración de claves de la tarjeta SFTP.

   ![](assets/fingerprint3.png)

   >[!NOTE]
   >
   >Si utiliza un ordenador Mac, puede ver la huella digital de la clave privada almacenada en el equipo ejecutando este comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Una vez rellenada toda la información, haga clic en **[!UICONTROL Connect]** para iniciar sesión en el servidor SFTP.

   ![](assets/sftpconnected.png)
