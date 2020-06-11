---
title: Monitoreo de perfiles activos
description: Obtenga información en tiempo real sobre el uso y la evolución más recientes e históricos de los Perfiles activos para cada una de las instancias de Campaña.
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 14%

---


# Monitoreo de perfiles activos {#active-profiles-monitoring}

>[!IMPORTANT]
>
>La supervisión de perfiles activos por parte del Panel de control está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.
>
>La función está disponible para los clientes alojados en AWS desde la compilación Campaign Standard 10368 y la compilación Campaign Classic 8931. Si está utilizando una compilación anterior, debe actualizar para utilizar esta función.

## Acerca de los perfiles activos {#about-active-profiles}

Según el contrato, cada una de las instancias de Campaña se aprovisiona con una cantidad específica de perfiles activos que se contabilizan a efectos de facturación. Consulte su contrato más reciente para obtener referencia sobre el número de perfiles activos adquiridos.

Un “perfil” es un registro de información (por ejemplo, un registro de la tabla nmsRecipient o una tabla externa que contiene una ID de cookie, ID de cliente, ID móvil u otra información relacionada con un canal determinado) que representa a un cliente final, a un cliente potencial o a un contacto.

Los Perfiles se consideran activos si han sido objeto de un canal o se han comunicado con ellos en los últimos 12 meses.

>[!NOTE]
>
>Los canales de Facebook y Twitter no se tienen en cuenta.

Para obtener más información sobre perfiles activos, consulte las documentaciones de [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) y [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) .

## Monitoreo de perfiles activos {#monitoring-active-profiles}

El Panel de control permite supervisar el uso de perfiles activos para cada una de las instancias de Campaña.

Para ello, siga estos pasos:

1. Abra la tarjeta **[!UICONTROL Performance Monitoring]** y seleccione la pestaña **[!UICONTROL Active Profiles]**.

1. Seleccione la instancia que desee en el **[!UICONTROL Instance List]**.

1. Se muestra el número de perfiles activos utilizados por la instancia, así como la última vez que se ejecutó el flujo de trabajo de facturación en la instancia.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>Los perfiles activos se cuentan en función de los flujos de trabajo técnicos dedicados que se ejecutan todos los días en las instancias:
>
>* Flujo de trabajo de [&quot;Facturación&quot;](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html) para Campaign Standard,
>* Flujo de trabajo [&quot;Número de perfiles de facturación activos&quot;](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) para Campaign Classic.


El área inferior proporciona una representación gráfica del uso de perfiles activos durante los últimos 30 días. Puede cambiar el período de tiempo mostrado a 1 año utilizando los filtros disponibles en la esquina superior derecha.

Al pasar el ratón por encima de una de las barras de gráficos, podrá obtener el número exacto de perfiles activos utilizados en el período seleccionado.
