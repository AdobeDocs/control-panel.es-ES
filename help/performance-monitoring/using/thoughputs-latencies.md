---
product: campaign
solution: Campaign
title: Monitorización de los impactos y la latencia
description: Obtenga información sobre cómo monitorizar las pulsaciones y la latencia de las instancias de Campaign en el Panel de control de Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: cbc068c921d0d16b49c881693e44e1ba2a90d015
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Monitorización de los impactos y la latencia {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Acerca de las entradas y la monitorización de la latencia "
>abstract="En esta pestaña, puede monitorizar cómo las entradas y la latencia del envío son las tendencias a lo largo del tiempo en las instancias."

Monitorizar cómo las pulsaciones de la entrega y la latencia son tendencias a lo largo de un periodo de tiempo es esencial para comprender el uso de las instancias y garantizar que tengan un buen rendimiento.

Esta información está disponible en Panel de control de Campaign para cada una de las instancias de Campaign en la variable **[!UICONTROL Performance Monitoring]** tarjeta, **[!UICONTROL Throughputs & Latencies]** pestaña .

>[!NOTE]
>
>Todas las cifras presentadas en esta esfera son aproximadas y sólo con fines informativos.

![](assets/throughput-latencies-overview.png)

De forma predeterminada, los datos se muestran para el día actual. Puede cambiar el periodo de tiempo mostrado utilizando la variable **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** y **[!UICONTROL 7 days]** botones.

La variable **[!UICONTROL Throughput]** proporciona información sobre el número de mensajes enviados por hora desde la instancia de Campaign seleccionada para todos los canales de comunicación a los que está autorizado.

También puede visualizar esta información en formato tabular con columnas que se pueden ordenar en lugar de un gráfico. Para ello, haga clic en el botón **[!UICONTROL Visualization settings]** a continuación, seleccione **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)

La variable **[!UICONTROL Latency]** proporciona información sobre la latencia encontrada en la instancia seleccionada al enviar comunicaciones transaccionales en tiempo real. Las latencias se capturan y visualizan con un percentil 95 y 99, lo que significa que el 95 % y el 99 % de las solicitudes deben ser más rápidas que la latencia dada.

![](assets/throughput-latencies-latency.png)
