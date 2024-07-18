---
product: campaign
solution: Campaign
title: Administración de claves
description: Obtenga información sobre cómo administrar claves para conectarse a servidores SFTP
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 03815e01-6371-4e1c-b4b8-7abe25957cee
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 100%

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

![](assets/do-not-localize/how-to-video.png) Descubra esta funcionalidad en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/generate-ssh-key.html?lang=es#sftp-management) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html?lang=es#sftp-management)

## Prácticas recomendadas {#best-practices}

**Acerca de la clave SSH pública**

Asegúrese de utilizar siempre la misma autenticación para conectarse al servidor y de utilizar un formato admitido para la clave.

**Integración de API con nombre de usuario y contraseña**

En casos muy excepcionales, la autenticación basada en contraseña está habilitada en algunos servidores SFTP. Adobe recomienda utilizar la autenticación basada en claves, ya que este método es más eficaz y seguro. Puede solicitar el cambio a la autenticación basada en claves poniéndose en contacto con el Servicio de atención al cliente.

>[!IMPORTANT]
>
>Si la contraseña caduca, incluso si hay claves instaladas en el sistema, no podrá iniciar sesión en sus cuentas de SFTP.

## Instalación de la clave SSH {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="Adición de clave pública"
>abstract="Genere una clave SSH pública para una instancia y añádala al panel de control de Campaign para acceder al servidor SFTP."

>[!IMPORTANT]
>
>Debe seguir siempre las directrices de su organización con respecto a las claves SSH. Los pasos que se indican a continuación son solo un ejemplo de cómo se puede realizar la creación de claves SSH y pueden servir como punto de referencia para comunicar los requisitos al equipo o al grupo interno de la red.

1. Vaya a la pestaña **[!UICONTROL Administración de claves]** y, a continuación, haga clic en el botón **[!UICONTROL Añadir nueva clave pública]**.

   ![](assets/key0.png)

1. En el cuadro de diálogo que aparece, seleccione el nombre de usuario para el que desea crear la clave pública y el servidor para el que desea activar la clave.

   ![](assets/key1.png)

   >[!NOTE]
   >
   >El Panel de control comprobará si un determinado nombre de usuario está activo en una instancia determinada y le permitirá habilitar la clave en una o varias instancias.
   >
   >Se pueden añadir una o más claves SSH públicas por cada usuario.

1. Para administrar mejor las claves públicas, puede establecer una duración para la disponibilidad de cada clave. Para ello, seleccione una unidad en la lista desplegable **[!UICONTROL Tipo]** y defina una duración en el campo correspondiente. Para obtener más información acerca de la caducidad de la clave pública, consulte [esta sección](#expiry).

   ![](assets/key_expiry.png)

   >[!NOTE]
   >
   >De forma predeterminada, el campo **[!UICONTROL Tipo]** está definido como **[!UICONTROL Ilimitado]**, lo que significa que la clave pública nunca caduca.

1. En el campo **[!UICONTROL Comentario]**, puede indicar una razón para añadir esta clave pública (por qué, para quién, etc.).

1. Para poder rellenar el campo **[!UICONTROL Clave pública]**, es necesario generar una clave pública SSH. Siga los pasos que se indican a continuación según su sistema operativo.

   **Linux y Mac:**

   Utilice el terminal para generar un par de claves pública y privada:
   1. Introduzca este comando: `ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`.
   1. Proporcione un nombre a la clave cuando se le solicite. Si el directorio .ssh no existe, el sistema creará uno.
   1. Introduzca y vuelva a introducir una contraseña cuando se le solicite. No obstante, lo puede dejar en blanco.
   1. El sistema crea un par de claves &quot;name&quot; y &quot;name.pub&quot;. Busque el archivo &quot;name.pub&quot; y ábralo. Debe tener una cadena alfanumérica que termina con la dirección de correo electrónico especificada.

   **Windows:**

   Es posible que necesite instalar una herramienta de terceros que le ayude a generar pares de claves privadas/públicas con el mismo formato “nombre.pub”.

1. Abra el archivo .pub y, a continuación, copie y pegue toda la cadena empezando por &quot;ssh...&quot; en el Panel de control.

   ![](assets/publickey.png)

   >[!NOTE]
   >
   >El campo **[!UICONTROL Clave pública]** solo admite el formato OpenSSH. El tamaño de la clave SSH pública debe ser de **2048 bits**.

1. Haga clic en el botón **[!UICONTROL Guardar]** para crear la clave. El Panel de control guarda la clave pública y su huella digital asociada, cifrada con el formato SHA256.

>[!IMPORTANT]
>
>Si la clave que ha creado se utiliza para establecer una conexión con un sistema que nunca antes se ha conectado al servidor SFTP seleccionado, tendrá que añadir una IP pública de ese sistema a la lista de permitidas antes de poder utilizar este sistema con el servidor SFTP. Consulte [esta sección](ip-range-allow-listing.md).

Puede utilizar las huellas digitales para hacer coincidir las claves privadas guardadas en el equipo con las correspondientes claves públicas guardadas en el Panel de control.

![](assets/fingerprint_compare.png)

El botón **...** permite eliminar una clave existente o copiar su huella digital asociada en el portapapeles.

![](assets/key_options.png)

## Administración de claves públicas {#managing-public-keys}

Las claves públicas creadas se muestran en la pestaña **[!UICONTROL Administración de claves]**.

Puede ordenar los elementos en función de la fecha de creación o edición, del usuario que los creó o editó y de la caducidad del rango IP.

También puede buscar una clave pública empezando a escribir un nombre o un comentario.

![](assets/control_panel_key_management_sort.png)

Para editar uno o más rangos de IP, consulte [esta sección](#editing-public-keys).

Para eliminar una o varias claves públicas de la lista, selecciónelas y haga clic en el botón **[!UICONTROL Eliminar clave pública]**.

![](assets/control_panel_delete_key.png)

### Caducidad {#expiry}

La columna **[!UICONTROL Caduca]** muestra cuántos días quedan para que caduque la clave pública.

Si se ha suscrito a [alertas por correo electrónico](../../performance-monitoring/using/email-alerting.md), recibirá notificaciones por correo electrónico 10 días y 5 días antes de que caduque una clave pública, y el día en que está previsto que caduque. Al recibir la alerta, puede [editar la clave pública](#editing-public-keys) para ampliar su periodo de validez si es necesario.

Una clave pública caducada se eliminará automáticamente después de 7 días. Aparece como **[!UICONTROL Caducado]** en la columna **[!UICONTROL Caduca]**. En este periodo de 7 días:

* Una clave pública caducada ya no se puede utilizar para conectarse al servidor SFTP.

* Puede [editar](#editing-public-keys) una clave pública caducada y actualizar su duración para que vuelva a estar disponible.

* Puede eliminarla de la lista.

## Editar claves públicas {#editing-public-keys}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_update"
>title="Edición de claves públicas"
>abstract="Actualice las claves públicas seleccionadas para acceder al servidor SFTP."

Para editar claves públicas, siga los pasos que se indican a continuación.

>[!NOTE]
>
>Solo puede editar claves públicas que hayan sido creadas desde la versión de octubre de 2021 del Panel de control.

1. Seleccione uno o varios elementos de la lista **[!UICONTROL Administración de claves]**.
1. Haga clic en el botón **[!UICONTROL Actualizar clave pública]**.

   ![](assets/control_panel_edit_key.png)

1. Solo puede editar la caducidad de la clave pública y añadir un nuevo comentario.

   >[!NOTE]
   >
   >Para modificar el nombre de usuario, la instancia y la clave pública en formato OpenSSH, elimine la clave pública y cree una nueva que se ajuste a sus necesidades.

1. Guarde los cambios.
