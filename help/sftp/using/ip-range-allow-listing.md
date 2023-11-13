---
product: campaign
solution: Campaign
title: Adición de rangos de IP a la lista de permitidos
description: Obtenga información sobre cómo agregar rangos de IP a la lista de permitidos para acceder a servidores SFTP.
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 45a3bfcd-500c-4139-b610-d39989260ab7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '1080'
ht-degree: 100%

---

# Adición de rangos de IP a la lista de permitidos {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Acerca de las listas de IP permitidas"
>abstract="En esta pestaña, puede agregar rangos de IP a la lista de permitidos para establecer una conexión con los servidores SFTP. Aquí solo se muestran los servidores SFTP a los que tiene acceso. Póngase en contacto con el administrador para solicitar acceso a otros servidores SFTP."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Ver vídeo de demostración"

Los servidores SFTP están protegidos. Para poder acceder a ellos con el fin de ver archivos o escribir otros nuevos, es necesario añadir la dirección IP pública del sistema o cliente que accede a los servidores a la lista de permitidos.

![](assets/do-not-localize/how-to-video.png) Descubra esta función en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=es#sftp-management) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=es#sftp-management)

## Acerca del formato CIDR {#about-cidr-format}

CIDR (enrutamiento entre dominios sin clase) es el formato admitido al agregar intervalos de IP con la interfaz del Panel de control.

La sintaxis consiste en una dirección IP, seguida de / y un número decimal. El formato y su sintaxis se detallan en [este artículo](https://whatismyipaddress.com/cidr){target="_blank"}.

Puede buscar en Internet herramientas gratuitas en línea que le ayudarán a convertir el rango IP del que dispone al formato CIDR.

## Prácticas recomendadas {#best-practices}

Asegúrese de seguir las recomendaciones y limitaciones que se indican a continuación al incluir direcciones IP en la lista de permitidos en el Panel de control-

* **Añada rangos de IP a la lista de permitidos** en lugar de a direcciones IP únicas. Para incluir una sola dirección IP en la lista de permitidos, añada /32 para indicar que el rango solo incluye una sola dirección IP.
* **No agregue rangos muy anchos a la lista de permitidos**, por ejemplo, incluyendo >265 direcciones IP. El Panel de control rechazará cualquier rango de formato CIDR que esté entre /0 y /23.
* Solo se pueden agregar **direcciones IP públicas** a la lista de permitidos.
* Asegúrese de **eliminar con regularidad las direcciones IP** que ya no necesite de la lista de permitidos.

## Adición de direcciones IP a la lista de permitidos {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Configuración de rango de IP"
>abstract="Defina los rangos de IP que desea agregar a la lista de permitidos para conectarse a los servidores SFTP."

Para agregar un rango de IP a la lista de permitidos, siga estos pasos:

1. Abra la tarjeta **[!UICONTROL SFTP]** y seleccione la pestaña **[!UICONTROL Lista de IP permitidas]**.
1. La lista de las direcciones IP en la lista de permitidos se muestra para cada instancia. Seleccione la instancia deseada de la lista de la izquierda y, a continuación, haga clic en el botón **[!UICONTROL Agregar nuevo rango de IP]**.

   ![](assets/control_panel_add_range.png)

1. Defina el rango de direcciones IP que quiere añadir a la lista de permitidos. Este campo solo acepta rangos de direcciones IP en formato CIDR, como por ejemplo *192.150.5.0/24*.

   ![](assets/control_panel_add_range4.png)

   >[!IMPORTANT]
   >
   >Un rango de IP no puede superponerse a un intervalo existente en la lista de permitidos. En ese caso, primero elimine el rango que contiene la IP superpuesta.

1. Es posible añadir un rango a la lista de permitidos para múltiples instancias. Para ello, pulse la tecla de la flecha hacia abajo o escriba las primeras letras de la instancia deseada y selecciónela en la lista de sugerencias.

   ![](assets/control_panel_add_range3.png)

1. Defina la etiqueta que se mostrará para este rango IP en la lista.

   ![](assets/control_panel_add_range2.png)

   >[!NOTE]
   >
   >Los siguientes caracteres especiales están permitidos en el campo **[!UICONTROL Etiqueta]**:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

1. Para administrar mejor la lista de direcciones IP permitidas, puede establecer una duración para la disponibilidad de cada rango de IP. Para ello, seleccione una unidad en la lista desplegable **[!UICONTROL Tipo]** y defina una duración en el campo correspondiente. Para obtener más información acerca de la caducidad del rango IP, consulte [esta sección](#expiry).

   ![](assets/control_panel_add_range5.png)

   >[!NOTE]
   >
   >De forma predeterminada, el campo **[!UICONTROL Tipo]** está configurado como **[!UICONTROL Ilimitado]**, lo que significa que el rango IP nunca caduca.

1. En el campo **[!UICONTROL Comentario]** puede indicar una razón para permitir este rango de IP (por qué, para quién, etc.).

1. Haga clic en el botón **[!UICONTROL Save.]** El rango IP añadido a la lista de permitidos se mostrará como **[!UICONTROL Pendiente]** hasta que la solicitud se procese por completo, lo que solo debería tardar unos segundos.

   ![](assets/control_panel_add_range6.png)

>[!IMPORTANT]
>
>Si está intentando conectar los servidores SFTP a un nuevo sistema, y, por tanto, añadiendo nuevos rangos de IP a la lista de permitidos, es posible que tenga que introducir nuevas claves públicas para completar la conexión. Para obtener más información, consulte [esta sección](key-management.md).

## Administración de rangos de IP {#managing-ip-ranges}

Los rangos de IP creados se muestran en la pestaña **[!UICONTROL Lista de IP permitidas]**.

Puede ordenar los elementos en función de la fecha de creación o edición, del usuario que los creó o editó y de la caducidad del rango IP.

También puede buscar un rango de IP empezando a escribir una etiqueta, un rango, un nombre o un comentario.

![](assets/control_panel_allow_list_sort.png)

Para editar uno o más rangos de IP, consulte [esta sección](#editing-ip-ranges).

Para eliminar uno o varios rangos de IP de la lista de permitidos, selecciónelos y, a continuación, haga clic en el botón **[!UICONTROL Eliminar rango de IP]**.

![](assets/control_panel_delete_range.png)

### Caducidad {#expiry}

La columna **[!UICONTROL Caduca]** muestra cuántos días quedan para que caduque el rango de IP.

Si se ha suscrito a [alertas por correo electrónico](../../performance-monitoring/using/email-alerting.md), recibirá notificaciones por correo electrónico 10 días y 5 días antes de que caduque un intervalo de IP, y el día en que está previsto que caduque. Al recibir la alerta, puede [editar el rango de IP](#editing-ip-ranges) para ampliar su periodo de validez si es necesario.

Un rango de IP caducado se eliminará automáticamente después de 7 días. Aparece como **[!UICONTROL Caducado]** en la columna **[!UICONTROL Caduca]**. En este periodo de 7 días:

* Un rango de IP caducado ya no se puede utilizar para acceder a los servidores SFTP.

* No puede crear otro rango de IP que coincida con un rango caducado. Antes de crear un nuevo rango de IP, es necesario eliminar el rango de IP caducado.

* Puede [editar](#editing-ip-ranges) un rango de IP caducado y actualizar su duración para que vuelva a estar disponible.

* Puede eliminarlo de la lista de permitidos.

## Editar de rangos de IP {#editing-ip-ranges}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_update"
>title="Actualización de rangos de IP"
>abstract="Actualice los rangos de IP seleccionados que pueden conectarse al servidor SFTP."

Para editar rangos de IP, siga los pasos que se indican a continuación.

>[!NOTE]
>
>Solo puede editar rangos de IP que hayan sido creados desde la versión de octubre de 2021 del Panel de control.

<!--Edition is not available for IP ranges that have been created before the Control Panel October 2021 release.-->

1. Seleccione uno o más rangos de IP de la lista **[!UICONTROL Lista de IP permitidas]**.

1. Haga clic en el botón **[!UICONTROL Actualizar rango de IP]**.

   ![](assets/control_panel_edit_range.png)

1. Solo puede editar la caducidad del rango IP y/o añadir un nuevo comentario.

   >[!NOTE]
   >
   >Para modificar el formato CIDR, su etiqueta o editar las instancias relacionadas, primero debe eliminar el rango IP y crear uno nuevo que corresponda a sus necesidades.

   ![](assets/control_panel_edit_range2.png)

1. Guarde los cambios.

## Monitorización de cambios {#monitoring-changes}

Los **[!UICONTROL Registros de trabajos]** de la página de inicio del Panel de control le permiten hacer un seguimiento y monitorizar todos los cambios que se han realizado en las direcciones IP de la lista de permitidos.

Para obtener más información sobre la interfaz del Panel de control, consulte [esta sección](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_log.png)
