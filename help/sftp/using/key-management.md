---
title: Administración de claves
description: Obtenga información sobre cómo administrar las claves para conectarse a los servidores SFTP
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Administración de claves {#key-management}

Adobe recomienda que todos los clientes establezcan una conexión con sus servidores SFTP **con un par de claves públicas y privadas**.

A continuación se describen los pasos para generar una clave SSH pública y agregarla para acceder al servidor SFTP, así como las recomendaciones relativas a la autenticación.

Una vez configurado el acceso al servidor, recuerde **incluir en la lista blanca las direcciones** IP que requerirán acceso al servidor para poder conectarse a él. Para obtener más información, consulte [esta sección](../../instances-settings/using/ip-whitelisting-instance-access.md).

>[!NOTE]
>
>Actualmente no es posible eliminar una clave pública SSH.

## Prácticas recomendadas {#best-practices}

**Acerca de la clave SSH pública**

Asegúrese de utilizar siempre la misma autenticación para conectarse al servidor y de utilizar un formato admitido para la clave.

**Integración de API con nombre de usuario y contraseña**

En casos muy excepcionales, la autenticación basada en contraseña está habilitada en algunos servidores SFTP. Adobe recomienda utilizar la autenticación basada en claves, ya que este método es más eficaz y seguro. Puede solicitar cambiar a la autenticación basada en claves poniéndose en contacto con el Servicio de atención al cliente.

>[!CAUTION]
>
>Si la contraseña caduca, incluso si hay claves instaladas en el sistema, no podrá iniciar sesión en sus cuentas de SFTP.

![](assets/control_panel_passwordexpires.png)

## Instalación de la clave SSH {#installing-ssh-key}

>[!CAUTION]
>
>Los pasos a continuación son un ejemplo de la creación de claves SSH solamente. Siga las directrices de su organización con respecto a las claves SSH. El ejemplo siguiente es sólo un ejemplo de cómo se puede hacer esto y sirve como punto de referencia útil para comunicar los requisitos a su equipo o grupo de red interno.

1. Vaya a la **[!UICONTROL Key Management]**ficha y, a continuación, haga clic en el**[!UICONTROL Add public key]** botón.

   ![](assets/key0.png)

1. En el cuadro de diálogo que se abre, seleccione el nombre de usuario para el que desea crear la clave pública y el servidor para el que desea activar la clave.

   >[!NOTE]
   >
   >La interfaz comprobará si un determinado nombre de usuario está activo en una instancia determinada y le proporcionará una opción para activar la clave en una o varias instancias.
   >
   >Se pueden agregar una o más claves SSH públicas para cada usuario.

   ![](assets/key1.png)

1. Copie y pegue la clave SSH pública. Para generar una clave pública, siga los pasos a continuación correspondientes a su sistema operativo:

   >[!NOTE]
   >
   >El tamaño de la clave SSH pública debe ser de **2048 bits**.

   **Linux y Mac:**

   Utilice Terminal para generar un par de claves pública y privada:
   1. Introduzca este comando: `ssh-keygen -t rsa -C <your_email@example.com>`.
   1. Proporcione un nombre a la clave cuando se le solicite. Si el directorio .ssh no existe, el sistema creará uno para usted.
   1. Introduzca y vuelva a introducir una frase de contraseña cuando se le solicite. También se puede dejar en blanco.
   1. El sistema crea un par de claves &quot;name&quot; y &quot;name.pub&quot;. Busque el archivo &quot;name.pub&quot; y ábralo. Debe tener una cadena alfanumérica que termine con la dirección de correo electrónico especificada.
   **Windows:**

   Es posible que deba instalar una herramienta de terceros que le ayude a generar pares de clave pública/privada con el mismo formato &quot;name.pub&quot;.

1. Abra el archivo .pub y, a continuación, copie y pegue toda la cadena empezando por &quot;ssh...&quot;. en el Panel de control.

   ![](assets/publickey.png)

1. Haga clic en el **[!UICONTROL Save]**botón para crear la clave. El Panel de control guarda la clave pública y su huella digital asociada, cifrada con el formato SHA256.

Puede utilizar las huellas digitales para que coincidan con las claves privadas guardadas en el equipo con las claves públicas correspondientes guardadas en el Panel de control.

![](assets/fingerprintNEW2.png)

El &quot;**...**&quot; permite eliminar una clave existente o copiar su huella digital asociada en el portapapeles.

![](assets/key_options.png)
