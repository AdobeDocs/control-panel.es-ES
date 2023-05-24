---
product: campaign
solution: Campaign
title: Acerca de la monitorización de bases de datos
description: Obtenga información sobre cómo supervisar su base de datos de Campaign en el Panel de control
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2bd7d2dd-97be-49bb-9f8e-7161d0742bc1
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 79%

---

# Acerca de la monitorización de bases de datos {#database-monitoring}

## Acerca de las bases de datos de instancias {#about-instances-databases}

Según el contrato, cada una de las instancias de Campaign se aprovisiona con una cantidad específica de espacio en la base de datos. Las bases de datos incluyen todos los **activos**, **flujos de trabajo** y **datos** que se almacenan en Adobe Campaign.

Con el tiempo, las bases de datos pueden alcanzar su capacidad máxima, especialmente si los recursos almacenados nunca se eliminan de la instancia o si hay muchos flujos de trabajo en estado pausado.

El desbordamiento de una base de datos de instancias puede dar lugar a varios problemas (incapacidad para iniciar sesión, enviar correos electrónicos, etc.). Por lo tanto, la supervisión de las bases de datos de las instancias es esencial para garantizar un rendimiento óptimo.

Si se ha suscrito a [alertas por correo electrónico](../../performance-monitoring/using/email-alerting.md), recibirá notificaciones por correo electrónico cuando una de las bases de datos de las instancias haya alcanzado el 80 % o más de su capacidad.

## Monitorización del uso de la base de datos{#monitoring-database-usage}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="Acerca de la monitorización de bases de datos"
>abstract="En esta pestaña, puede obtener información en tiempo real sobre el uso y la evolución más recientes e históricos de la base de datos para cada una de las instancias de Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=es" text="Acerca de la monitorización del rendimiento"

El Panel de control le permite monitorizar el uso de la base de datos para cada una de las instancias de Campaign. Para ello, abra la tarjeta **[!UICONTROL Performance Monitoring]** y seleccione la pestaña **[!UICONTROL Databases]**.

Seleccione la instancia que desee en **[!UICONTROL Instance List]** para mostrar información acerca de la capacidad de la base de datos de la instancia y el espacio utilizado.

>[!NOTE]
>
>Si la cantidad de espacio disponible en la base de datos, como se muestra en el Panel de control, no refleja la cantidad especificada en el contrato, póngase en contacto con el Servicio de atención al cliente.

![](assets/databases_dashboard.png)

Los datos de este tablero se actualizan en función de la variable **[!UICONTROL Database cleanup technical workflow]** que se ejecuta en la instancia de Campaign (consulte [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=es#list-of-technical-workflows) y [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=es) documentación). Puede comprobar la última vez que el flujo de trabajo se ejecutó por debajo de **[!UICONTROL Used Space]** y **[!UICONTROL Provided Space]** métricas. Tenga en cuenta que, si el flujo de trabajo no se ha ejecutado desde hace más de 3 días, le recomendamos que se ponga en contacto con el Servicio de atención al cliente de Adobe para que investigue por qué no se está ejecutando.

En este tablero hay disponibles métricas adicionales para ayudarle a analizar el uso de la base de datos de la instancia. Se detallan en estas secciones:

* [Utilización de la base de datos](../../performance-monitoring/using/database-utilization.md)
* [Resumen de almacenamiento](../../performance-monitoring/using/database-storage-overview.md)
* [Los 10 recursos temporales principales](../../performance-monitoring/using/database-top-ten-resources.md)
* [Consultas activas](../../performance-monitoring/using/database-active-queries.md)

![](assets/do-not-localize/how-to-video.png) Descubra esta función en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=es#performance-monitoring) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=es#performance-monitoring)
