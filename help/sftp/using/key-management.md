---
product: campaign
solution: Campaign
title: Administración de claves
description: Obtenga información sobre cómo administrar claves para conectarse a servidores SFTP
feature: Control Panel
role: Architect
level: Experienced
exl-id: 03815e01-6371-4e1c-b4b8-7abe25957cee
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 36%

---

# Administración de claves {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="Acerca de la administración de claves públicas"
>abstract="En esta pestaña, cree, administre y edite las claves públicas."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="Ver vídeo de demostración"

Adobe recomienda que todos los clientes establezcan una conexión con sus servidores SFTP **con un par de claves públicas y privadas**.

A continuación, se describen los pasos para generar una clave SSH pública y añadirla para acceder al servidor SFTP, así como las recomendaciones relativas a la autenticación.

Una vez configurado el acceso al servidor, recuerde **añadir las direcciones IP que requerirán acceso al servidor a la lista de permitidos** para poder conectarse a él. Para obtener más información, consulte [esta sección](../../instances-settings/using/ip-allow-listing-instance-access.md).

![](assets/do-not-localize/how-to-video.png) Descubra esta función en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/generate-ssh-key.html#sftp-management) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html#sftp-management)

## Prácticas recomendadas {#best-practices}

**Acerca de la clave SSH pública**

Asegúrese de utilizar siempre la misma autenticación para conectarse al servidor y de utilizar un formato admitido para la clave.

**Integración de API con nombre de usuario y contraseña**

En casos muy excepcionales, la autenticación basada en contraseña está habilitada en algunos servidores SFTP. Adobe recomienda utilizar la autenticación basada en claves, ya que este método es más eficaz y seguro. Puede solicitar cambiar a la autenticación basada en claves poniéndose en contacto con el Servicio de atención al cliente.

>[!IMPORTANT]
>
>Si la contraseña caduca, incluso si hay claves instaladas en el sistema, no podrá iniciar sesión en sus cuentas de SFTP.

## Instalación de la clave SSH {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="Adición de clave pública"
>abstract="Genere una clave SSH pública para una instancia y agréguela a Panel de control de Campaign para acceder al servidor SFTP."

>[!IMPORTANT]
>
>Siempre debe seguir las directrices de su organización con respecto a las claves SSH. Los pasos siguientes son solo un ejemplo de cómo se puede crear la clave SSH y pueden servir como punto de referencia útil para comunicar los requisitos a su equipo o grupo de red interna.

1. Vaya a la pestaña **[!UICONTROL Key Management]** y, a continuación, haga clic en el botón **[!UICONTROL Add new public key]**.

   ![](assets/key0.png)

1. En el cuadro de diálogo que aparece, seleccione el nombre de usuario para el que desea crear la clave pública y el servidor para el que desea activar la clave.

   ![](assets/key1.png)

   >[!NOTE]
   >
   >Panel de control de Campaign comprobará si un nombre de usuario determinado está activo en una instancia determinada y le permitirá activar la clave en una o varias instancias.
   >
   >Se pueden añadir una o más claves SSH públicas por cada usuario.

1. Para administrar mejor las claves públicas, puede establecer una duración para la disponibilidad de cada clave. Para ello, seleccione una unidad en la **[!UICONTROL Type]** lista desplegable y defina una duración en el campo correspondiente. Para obtener más información sobre la caducidad de la clave pública, consulte [esta sección](#expiry).

   ![](assets/key_expiry.png)

   >[!NOTE]
   >
   >De forma predeterminada, la variable **[!UICONTROL Type]** el campo está definido como **[!UICONTROL Unlimited]**, lo que significa que la clave pública nunca caduca.

1. En el **[!UICONTROL Comment]** , puede indicar un motivo para añadir esta clave pública (por qué, para quién, etc.).

1. Para poder rellenar el **[!UICONTROL Public Key]** , debe generar una clave SSH pública. Siga los pasos que se indican a continuación según su sistema operativo.

   **Linux y Mac:**

   Utilice el terminal para generar un par de claves pública y privada:
   1. Introduzca este comando: `ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`.
   1. Proporcione un nombre a la clave cuando se le solicite. Si el directorio .ssh no existe, el sistema creará uno.
   1. Introduzca y vuelva a introducir una contraseña cuando se le solicite. No obstante, lo puede dejar en blanco.
   1. El sistema crea un par de claves &quot;name&quot; y &quot;name.pub&quot;. Busque el archivo &quot;name.pub&quot; y ábralo. Debe tener una cadena alfanumérica que termina con la dirección de correo electrónico especificada.

   **Windows:**

   Es posible que tenga que instalar una herramienta de terceros que le ayude a generar pares de clave pública/privada con el mismo formato &quot;name.pub&quot;.

1. Abra el archivo .pub y, a continuación, copie y pegue toda la cadena empezando por &quot;ssh...&quot; en el Panel de control.

   ![](assets/publickey.png)

   >[!NOTE]
   >
   >La variable **[!UICONTROL Public Key]** solo acepta el formato OpenSSH. El tamaño de la clave SSH pública debe ser de **2048 bits**.

1. Haga clic en el botón **[!UICONTROL Save]** para crear la clave. Panel de control de Campaign guarda la clave pública y la huella digital asociada, cifrada con el formato SHA256.

>[!IMPORTANT]
>
>Si la clave que ha creado se utiliza para establecer una conexión con un sistema que nunca se ha conectado al servidor SFTP seleccionado anteriormente, deberá añadir una IP pública de dicho sistema a la lista de permitidos antes de poder utilizar este sistema con el servidor SFTP. Consulte [esta sección](ip-range-allow-listing.md).

Puede utilizar las huellas digitales para que coincidan con las claves privadas guardadas en el equipo con las claves públicas correspondientes guardadas en el Panel de control de Campaign.

![](assets/fingerprint_compare.png)

El botón **...** permite eliminar una clave existente o copiar su huella digital asociada en el portapapeles.

![](assets/key_options.png)

## Administración de claves públicas {#managing-public-keys}

Las claves públicas que crea se muestran en la **[!UICONTROL Key Management]** pestaña .

Puede ordenar los elementos en función de la fecha de creación o edición, del usuario que la creó o editó y de la caducidad del intervalo IP.

También puede buscar una clave pública empezando a escribir un nombre o un comentario.

![](assets/control_panel_key_management_sort.png)

Para editar uno o varios rangos de IP, consulte [esta sección](#editing-public-keys).

Para eliminar una o varias claves públicas de la lista, selecciónelas y haga clic en el botón **[!UICONTROL Delete public key]** botón.

![](assets/control_panel_delete_key.png)

### Caducidad {#expiry}

La variable **[!UICONTROL Expires]** muestra cuántos días quedan hasta que caduque la clave pública.

Si se ha suscrito a [alertas por correo electrónico](../../performance-monitoring/using/email-alerting.md), recibirá notificaciones por correo electrónico 10 días y 5 días antes de que caduque una clave pública y, el día en que caduque. Al recibir la alerta, puede [editar la clave pública](#editing-public-keys) para ampliar su periodo de validez si es necesario.

Una clave pública caducada se eliminará automáticamente pasados 7 días. Se muestra como **[!UICONTROL Expired]** en el **[!UICONTROL Expires]** para abrir el Navegador. Dentro de este periodo de 7 días:

* Ya no se puede utilizar una clave pública caducada para conectarse al servidor SFTP.

* Puede [editar](#editing-public-keys) una clave pública caducada y actualice su duración para que vuelva a estar disponible.

* Puede eliminarlo de la lista.

## Edición de claves públicas {#editing-public-keys}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_update"
>title="Editar claves públicas"
>abstract="Actualice las claves públicas seleccionadas para acceder al servidor SFTP."

Para editar claves públicas, siga los pasos a continuación.

>[!NOTE]
>
>Solo puede editar las claves públicas que se han creado desde la versión de Panel de control de Campaign de octubre de 2021.

1. Seleccione uno o varios elementos de la lista **[!UICONTROL Key Management]** lista.
1. Haga clic en el botón **[!UICONTROL Update public key]**.

   ![](assets/control_panel_edit_key.png)

1. Solo puede editar la caducidad de la clave pública o agregar un comentario nuevo.

   >[!NOTE]
   >
   >Para modificar el nombre de usuario, la instancia y la clave pública en formato OpenSSH, elimine la clave pública y cree una nueva que se ajuste a sus necesidades.

1. Guarde los cambios.
