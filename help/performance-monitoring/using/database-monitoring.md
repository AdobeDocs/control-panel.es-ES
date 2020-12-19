---
product: campaign
solution: Campaign
title: Supervisión de bases de datos
description: Obtenga información sobre cómo supervisar la base de datos de Campañas en el Panel de control de Campaign
translation-type: tm+mt
source-git-commit: 2d84a5ebe8dbf42264c94f882a51180aae2a58a6
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 1%

---


# Supervisión de bases de datos {#database-monitoring}

## Acerca de las bases de datos de instancias {#about-instances-databases}

Según el contrato, cada una de las instancias de Campaña se aprovisiona con una cantidad específica de espacio en la base de datos.

Las bases de datos incluyen todos los **recursos**, **flujos de trabajo** y **datos** que se almacenan en Adobe Campaign.

Con el tiempo, las bases de datos pueden alcanzar su capacidad máxima, especialmente si los recursos almacenados nunca se eliminan de la instancia o si hay muchos flujos de trabajo en pausa.

El desbordamiento de una base de datos de instancia puede provocar varios problemas (incapacidad de iniciar sesión, enviar correos electrónicos, etc.). Por lo tanto, la supervisión de las bases de datos de las instancias es esencial para garantizar un rendimiento óptimo.

>[!NOTE]
>
>Si la cantidad de espacio proporcionado en la base de datos, según muestra el Panel de control de Campaign, no refleja la cantidad especificada en el contrato, póngase en contacto con el Servicio de atención al cliente.

## Monitoreo del uso de la base de datos {#monitoring-instances-database}

![](assets/do-not-localize/how-to-video.png) Descubra esta función en vídeo con  [Campaña ](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring) Classic o  [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring)

Panel de control de Campaign permite supervisar el uso de la base de datos para cada una de las instancias de Campaña. Para ello, abra la tarjeta **[!UICONTROL Performance Monitoring]** y luego seleccione la ficha **[!UICONTROL Databases]**.

Seleccione la instancia que desee en **[!UICONTROL Instance List]** para mostrar información sobre la capacidad de la base de datos de la instancia y el espacio utilizado.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>Tenga en cuenta que los datos de este panel se actualizan en función de la **[!UICONTROL Database cleanup technical workflow]** que se ejecuta en la instancia de Campaña (consulte [Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) y [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html) documentación).
>
>Puede comprobar la última vez que el flujo de trabajo se ejecutó por debajo de las métricas **[!UICONTROL Used Space]** y **[!UICONTROL Provided Space]**. Tenga en cuenta que, si el flujo de trabajo no se ha estado ejecutando desde hace más de 3 días, le recomendamos que se ponga en contacto con el servicio de atención al cliente de Adobe para que investigue por qué el flujo de trabajo no se está ejecutando.

En este panel encontrará métricas adicionales que le ayudarán a analizar el uso de la base de datos de la instancia:

* [Uso de la base de datos](../../performance-monitoring/using/database-monitoring.md#database-utilization)
* [Almacenamiento general](../../performance-monitoring/using/database-monitoring.md#storage-overview)
* [Los 10 recursos temporales principales](../../performance-monitoring/using/database-monitoring.md#top-10)

### Utilización de la base de datos {#database-utilization}

El área **[!UICONTROL Database utilization]** proporciona una representación gráfica del uso mínimo, promedio y máximo de la base de datos durante los últimos 7 días, así como el umbral de utilización de la base de datos del 90% representado por una curva de puntos roja.

Para cambiar el período de tiempo, utilice los filtros disponibles en la esquina superior derecha del gráfico.

Para mejorar la legibilidad, también puede resaltar una o varias curvas en el gráfico. Para ello, selecciónelos en la leyenda **[!UICONTROL Aggregation Type]**.

Para obtener más información sobre un período de tiempo específico, pase el ratón sobre el gráfico para mostrar información sobre el uso de la base de datos que se realizó en este momento.

![](assets/databases_dashboard_detail.png)

### Información general de almacenamiento {#storage-overview}

El área **[!UICONTROL Storage overview]** proporciona una representación gráfica del espacio ocupado por:

* **[!UICONTROL System resources]**

   Tenga en cuenta que, si los recursos del sistema consumen una gran parte del espacio de la base de datos, recomendamos ponerse en contacto con el Servicio de atención al cliente.

* **[!UICONTROL Out-of-the-box tables]** proporcionado de forma predeterminada con las instancias de Campaña,
* **[!UICONTROL Temporary tables]** creado por flujos de trabajo y envíos,
* **[!UICONTROL Non-out of the box tables]** generado después de crear recursos personalizados.

![](assets/database-storage-overview.png)

Haga clic en el botón **[!UICONTROL View details]** para obtener más detalles sobre los diferentes recursos que consumen espacio en la base de datos.

![](assets/database-storage-details.png)

Utilice el filtro para refinar las tablas de búsqueda y visualización de un tipo de recurso específico solamente.

![](assets/database-storage-overview-filter.png)

### Los 10 recursos temporales principales {#top-10}

El área **[!UICONTROL Top 10 temporary resources]** lista los 10 mayores recursos temporales generados por flujos de trabajo y envíos.

La supervisión de flujos de trabajo y envíos que están creando grandes recursos temporales es un paso clave para supervisar la base de datos. Si algún recurso temporal consume demasiado espacio en la base de datos, asegúrese de que es necesario disponer de este flujo de trabajo o envío y, finalmente, navegue hasta la instancia para detenerlo.

>[!IMPORTANT]
>
>La recomendación general es evitar tener **más de 40 columnas** en los recursos no predeterminados.

![](assets/database-top10.png)

>[!NOTE]
>
>Si se detecta que un flujo de trabajo tiene un gran número de recuentos de tablas o tamaño de base de datos, se recomienda revisar el flujo de trabajo para investigar por qué está generando tantos datos.
>
>Al final de esta página también hay disponibles recursos de Campaign Standard y de Classic para ayudarle a evitar la sobrecarga de la base de datos.

El botón **[!UICONTROL View all]** le permite acceder a información detallada sobre estos recursos temporales.

![](assets/database-top10-view.png)

>[!NOTE]
>
>El valor de la columna **[!UICONTROL Keep interim results]** indica si la opción está habilitada (&quot;1&quot;) o deshabilitada (&quot;0&quot;) en la Campaña. Se puede acceder a la opción **[!UICONTROL Keep interim results]** en las propiedades de los flujos de trabajo. Le permite guardar los resultados de las transiciones entre las distintas actividades de un flujo de trabajo (consulte [documentación de Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html) y [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/workflow-best-practices.html#logs)).
>
>Si la opción está habilitada para uno de sus flujos de trabajo, el flujo de trabajo de limpieza de la base de datos no podrá recuperar el espacio consumido por los resultados intermedios. Por lo tanto, recomendamos revisar el flujo de trabajo para comprobar si la opción se puede desactivar.

## Prevención de la sobrecarga de base de datos {#preventing-database-overload}

oferta Campaign Standard y Clásica de varias formas de evitar el consumo excesivo de espacio en disco de la base de datos.

La sección siguiente proporciona recursos útiles de documentación de Campañas para ayudarle a optimizar el uso de las bases de datos:

**Supervisión de flujos de trabajo**

* [Prácticas recomendadas](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html)  de flujos de trabajo (Campaign Standard)
* [Supervisión de la ejecución](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html)  del flujo de trabajo (Campaign Classic)

**Mantenimiento de la base de datos**

* Flujo de trabajo técnico de limpieza de bases de datos ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Guía](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html)  de mantenimiento de la base de datos (Campaign Classic)
* [Solución de problemas](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html)  del rendimiento de la base de datos (Campaign Classic)
* [Opciones](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database)  relacionadas con la base de datos (Campaign Classic)
* Retención de datos ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/data-retention.html) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html#data-retention))

>[!NOTE]
>
>Además, puede recibir notificaciones cuando una de sus bases de datos alcance su capacidad. Para ello, suscríbase a [alertas de correo electrónico](../../performance-monitoring/using/email-alerting.md).
