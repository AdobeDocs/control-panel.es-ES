---
title: Lista blanca del rango de IP
description: Obtenga información sobre cómo incluir en la lista blanca los rangos IP para el acceso a los servidores SFTP
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Lista blanca del rango de IP {#ip-range-whitelisting}

Los servidores SFTP están protegidos. Para poder acceder a ellos con el fin de ver archivos o escribir nuevos, debe incluir en la lista blanca la dirección IP pública del sistema o cliente que accede a los servidores.

## Acerca del formato CIDR {#about-cidr-format}

CIDR (Enrutamiento entre dominios sin clase) es el formato admitido al agregar intervalos de IP con la interfaz del Panel de control.

La sintaxis consiste en una dirección IP, seguida de un carácter &#39;/&#39; y un número decimal. El formato y su sintaxis se detallan en [este artículo](https://whatismyipaddress.com/cidr).

Puede buscar en Internet herramientas gratuitas en línea que le ayudarán a convertir la gama de IP que tiene en mano al formato CIDR.

## Prácticas recomendadas {#best-practices}

Asegúrese de seguir las recomendaciones y limitaciones que se indican a continuación al incluir direcciones IP en la lista blanca en el Panel de control.

* **Lista blanca de intervalos** IP en lugar de direcciones IP únicas. Para incluir una sola dirección IP en la lista blanca, añada un &#39;/32&#39; para indicar que el rango solo incluye una sola dirección IP.
* **No incluya rangos** muy anchos en la lista de direcciones permitidas, por ejemplo, > 265 direcciones IP. El Panel de control rechazará cualquier rango de formato CIDR que esté entre /0 y /23.
* Solo se pueden incluir en la lista blanca las direcciones **IP** públicas.
* Asegúrese de eliminar **regularmente las direcciones** IP en la lista blanca que ya no necesite.

## Lista blanca de direcciones IP {#whitelisting-ip-addresses}

Para incluir un intervalo IP en la lista blanca, siga estos pasos:

1. Abra la **[!UICONTROL SFTP]**tarjeta y seleccione la**[!UICONTROL IP Whistelisting]** ficha.
1. Se muestra la lista de direcciones IP permitidas para cada instancia. Seleccione la instancia que desee en la lista de la izquierda y haga clic en el **[!UICONTROL Add new IP range]**botón.

   ![](assets/control_panel_add_range.png)

1. Defina el rango IP que desea incluir en la lista blanca, en formato CIDR, y luego defina la etiqueta que se mostrará en la lista.

   >[!NOTE]
   >
   >Estos caracteres especiales se permiten en el campo Etiqueta:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!CAUTION]
   >
   >Un intervalo IP no puede superponerse a un intervalo de la lista blanca existente. En ese caso, primero elimine el rango que contiene la IP superpuesta.
   >
   >Es posible incluir un rango en la lista blanca para varias instancias. Para ello, presione la tecla de flecha hacia abajo o escriba las primeras letras de la instancia deseada y selecciónela en la lista de sugerencias.

   ![](assets/control_panel_add_range3.png)

1. Haga clic en el botón **[!UICONTROL Save]**. La adición a la lista blanca de IP se mostrará como PENDIENTE hasta que la solicitud se procese por completo. Esto sólo debería tardar unos segundos.

Para eliminar los rangos de IP permitidos, selecciónelos y haga clic en el **[!UICONTROL Delete IP range]**botón .

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Actualmente no es posible editar un rango de la lista blanca. Para modificar un rango de IP, elimínelo y luego cree uno que se ajuste a sus necesidades.

## Control de cambios {#monitoring-changes}

La **[!UICONTROL Job Logs]**página principal del Panel de control permite supervisar todos los cambios realizados en las direcciones IP permitidas.

Para obtener más información sobre la interfaz del Panel de control, consulte [esta sección](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_log.png)
