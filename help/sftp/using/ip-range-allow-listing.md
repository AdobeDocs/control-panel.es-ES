---
title: El rango IP permite el listado
description: Obtenga información sobre cómo agregar intervalos de IP a la lista de permitidos para el acceso a los servidores SFTP
translation-type: tm+mt
source-git-commit: f6d75de9c3d92e4f5d0b3d254f103db0901ab20a
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 40%

---


# El rango IP permite el listado {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Acerca del listado de permitidas por IP"
>abstract="En esta ficha, puede agregar rangos de IP a la lista de permitidos para establecer una conexión con los servidores SFTP. Aquí solo se muestran los servidores SFTP a los que tiene acceso. Póngase en contacto con el administrador para solicitar acceso a otros servidores SFTP."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Ver vídeo de demostración"

Los servidores SFTP están protegidos. Para poder acceder a ellos con el fin de vista de archivos o de escribir nuevos archivos, debe agregar la dirección IP pública del sistema o cliente que accede a los servidores a la lista de permitidos.

## Acerca del formato CIDR {#about-cidr-format}

CIDR (enrutamiento entre dominios sin clase) es el formato admitido al agregar intervalos de IP con la interfaz del Panel de control de Campaign.

La sintaxis consiste en una dirección IP, seguida de / y un número decimal. El formato y su sintaxis se detallan en [este artículo](https://whatismyipaddress.com/cidr).

Puede buscar en Internet herramientas gratuitas en línea que le ayudarán a convertir la gama de IP al formato CIDR.

## Prácticas recomendadas {#best-practices}

Asegúrese de seguir las recomendaciones y limitaciones siguientes al agregar direcciones IP a la lista de permitidos en el Panel de control.

* **Añada intervalos de IP a la lista de permitidos** en lugar de a direcciones IP únicas. Para agregar una sola dirección IP a la lista de permitidos, anexe un &#39;/32&#39; a la misma para indicar que el rango solo incluye una sola dirección IP.
* **No agregue rangos muy anchos a la lista de permitidos**, por ejemplo, incluyendo > 265 direcciones IP. El Panel de control de Campaign rechazará cualquier rango de formato CIDR que esté entre /0 y /23.
* Solo se pueden agregar direcciones **IP** públicas a la lista de permitidos.
* Asegúrese de eliminar **regularmente las direcciones** IP que ya no necesite de la lista de permitidos.

## Añadir direcciones IP a la lista de permitidos {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Adición de un nuevo rango de IP"
>abstract="Defina los intervalos de IP que desea agregar a la lista de permitidos para conectarse a los servidores SFTP."

Para agregar un intervalo de IP a la lista de permitidos, siga estos pasos:

1. Abra la tarjeta **[!UICONTROL SFTP]** y seleccione la pestaña **[!UICONTROL IP Whistelisting]**.
1. La lista de las direcciones IP en la lista de permitidos se muestra para cada instancia. Seleccione la instancia que desee en la lista del lado izquierdo y haga clic en el botón **[!UICONTROL Add new IP range]**.

   ![](assets/control_panel_add_range.png)

1. Defina el rango IP que desea agregar a la lista de permitidos, en formato CIDR, y luego defina la etiqueta que se mostrará en la lista.

   >[!NOTE]
   >
   >Estos caracteres especiales se permiten en el campo Etiqueta:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >Un intervalo IP no puede superponerse a un intervalo existente en la lista de permitidos. En ese caso, primero elimine el rango que contiene la IP superpuesta.
   >
   >Es posible agregar un rango en la lista de permitidos para varias instancias. Para ello, pulse la tecla de la flecha hacia abajo o escriba las primeras letras de la instancia deseada y selecciónela en la lista de sugerencias.

   ![](assets/control_panel_add_range3.png)

1. Haga clic en el botón **[!UICONTROL Save]**. La adición de IP a la lista de permitidos se mostrará como PENDIENTE hasta que la solicitud se procese por completo. Esto solo debería tardar unos segundos.

Para eliminar intervalos IP de la lista de permitidos, selecciónelos y haga clic en el **[!UICONTROL Delete IP range]** botón .

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Actualmente no es posible editar un rango en la lista de permitidos. Para modificar un rango de IP, elimínelo y luego cree uno que se ajuste a sus necesidades.

## Control de cambios {#monitoring-changes}

The **[!UICONTROL Job Logs]** in the Control Panel home page let you monitor all changes that have been made to IP addresses on the allow list.

Para obtener más información sobre la interfaz del Panel de control de Campaign, consulte [esta sección](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_log.png)
