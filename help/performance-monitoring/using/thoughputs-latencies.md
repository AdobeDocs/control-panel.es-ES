---
product: campaign
solution: Campaign
title: Monitorización del rendimiento y la latencia
description: Aprenda a monitorizar el rendimiento y la latencia de las instancias de Campaign en el Panel de control de Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 73%

---

# Monitorización del rendimiento y la latencia {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Acerca de la monitorización del rendimiento y la latencia "
>abstract="En esta pestaña, puede monitorizar cómo el rendimiento y la latencia de la entrega son las tendencias a lo largo del tiempo en las instancias."

El Panel de control de Campaign permite monitorizar las entradas de envío y la latencia de cada una de las instancias.

>[!IMPORTANT]
>
>Esta función está disponible para todos los clientes Campaign Standards y de la versión 8, así como para los clientes de Campaign V7 con los números de compilación 9032, 9330, 9346 o 9349 que tengan [independiente](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html) implementaciones (sin ninguna instancia media).

Monitorizar cómo el rendimiento y la latencia de la entrega son tendencias a lo largo de un período es esencial para comprender el uso de las instancias y garantizar que tengan un buen rendimiento.

Esta información está disponible en Panel de control de Campaign para cada una de las instancias de Campaign de la tarjeta **[!UICONTROL Performance Monitoring]**, pestaña **[!UICONTROL Throughputs & Latency]** (tenga en cuenta que el Panel de control de Campaign puede tardar hasta una hora en mostrar las cifras).

* El área **[!UICONTROL Throughput]** proporciona información sobre el número de mensajes enviados por hora desde la instancia de Campaign seleccionada para todos los canales de comunicación a los que está autorizado.

   >[!NOTE]
   >
   >Para Campaign v7/v8, el número de rendimiento mostrado es el rendimiento logrado desde instancias de MID (fuentes intermedias). Para implementaciones de marketing independientes (MKT) (sin ninguna instancia de MID), se muestra el rendimiento de la instancia de MKT en su lugar.

* El área **[!UICONTROL Latency]** proporciona información sobre la latencia encontrada en la instancia seleccionada al enviar comunicaciones transaccionales en tiempo real. Las latencias se capturan y visualizan con un percentil 95 y 99, lo que significa que el 95 % y el 99 % de las solicitudes deben ser más rápidas que la latencia dada.

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>Todas las cifras presentadas en esta área son aproximadas y solo con fines informativos.

De forma predeterminada, los datos se muestran para el día actual. Puede cambiar el período mostrado utilizando los botones **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** y **[!UICONTROL 7 days]**.

También puede visualizar la información en formato tabular con columnas que se pueden ordenar en lugar de un gráfico. Para ello, haga clic en el botón **[!UICONTROL Visualization settings]** y seleccione **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)
