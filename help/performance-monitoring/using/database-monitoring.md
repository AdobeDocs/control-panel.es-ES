---
title: Supervisión de bases de datos
description: Obtenga información sobre cómo supervisar la base de datos de Campañas en el Panel de control
translation-type: tm+mt
source-git-commit: 296cbcfa8588b05c03452afdb5bdbad8da1595d0

---


# Supervisión de bases de datos {#database-monitoring}

## Acerca de las bases de datos de instancias {#about-instances-databases}

Según el contrato, cada una de las instancias de Campaña se aprovisiona con una cantidad específica de espacio en la base de datos.

Las bases de datos incluyen todos **los recursos**, **flujos de trabajo** y **datos** almacenados en Adobe Campaign.

Con el tiempo, las bases de datos pueden alcanzar su capacidad máxima, especialmente si los recursos almacenados nunca se eliminan de la instancia o si hay muchos flujos de trabajo en pausa.

El desbordamiento de una base de datos de instancia puede provocar varios problemas (incapacidad de iniciar sesión, enviar correos electrónicos, etc.). Por lo tanto, la supervisión de las bases de datos de las instancias es esencial para garantizar un rendimiento óptimo.

>[!NOTE]
>
>Es posible que la cantidad de espacio en la base de datos proporcionada en el Panel de control no refleje la cantidad de espacio en la base de datos especificada en el contrato. La mayoría de las veces, se le proporciona temporalmente espacio de base de datos mayor para garantizar el rendimiento del sistema.

## Monitoreo del uso de la base de datos {#monitoring-instances-database}

El Panel de control permite supervisar el uso de la base de datos para cada una de las instancias de Campaña. Para realizar esto, siga los pasos a continuación.

1. Abra la **[!UICONTROL Performance Monitoring]** tarjeta y seleccione la **[!UICONTROL Databases]** ficha.

1. Seleccione la instancia que desee en el **[!UICONTROL Instance List]**.

   El área superior proporciona información sobre la capacidad de la base de datos de la instancia y el espacio utilizado.

   ![](assets/databases_dashboard.png)

   El área inferior proporciona una representación gráfica de la utilización de la base de datos en los últimos 7 días. Puede cambiar el período de tiempo mostrado mediante los filtros disponibles en la esquina superior derecha.

   Al pasar el ratón sobre el gráfico, podrá obtener información detallada sobre el período de tiempo seleccionado.

   ![](assets/databases_dashboard_detail.png)

>[!NOTE]
>
>También puede recibir notificaciones cuando una de sus bases de datos alcance su capacidad. Para ello, suscríbase a las alertas de [correo electrónico](../../performance-monitoring/using/email-alerting.md)

## Prevención de la sobrecarga de la base de datos {#preventing-database-overload}

oferta Campaign Standard y Clásica de varias formas de evitar el consumo excesivo de espacio en disco de la base de datos.

La sección siguiente proporciona recursos útiles de documentación de Campañas para ayudarle a optimizar el uso de las bases de datos:

**Supervisión de Flujos de trabajo**

* [Prácticas recomendadas](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) de Flujos de trabajo (Campaign Standard)
* [Supervisión de la ejecución](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) del flujo de trabajo (Campaign Classic)

**Mantenimiento de la base de datos**

* Flujo de trabajo técnico de limpieza de bases de datos ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Guía](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) de mantenimiento de la base de datos (Campaign Classic)
* [Solución de problemas](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) del rendimiento de la base de datos (Campaign Classic)
* [Opciones](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) relacionadas con la base de datos (Campaign Classic)
