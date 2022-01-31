---
product: campaign
solution: Campaign
title: Supervisión de consultas activas
description: Obtenga información sobre cómo monitorizar las consultas activas en las instancias de Campaign en el Panel de control de Campaign .
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: 6922e132321f67e1e8122e33ead3c5e54c639763
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# Supervisión de consultas activas {#long-running-queries}

La variable **[!UICONTROL Active queries]** del **[!UICONTROL Databases]** lista las cinco consultas que se han estado ejecutando durante el mayor tiempo en la instancia seleccionada.

![](assets/active-queries.png)

La variable **[!UICONTROL Duration]** columnas especifica cuánto tiempo se ha estado ejecutando una consulta en la instancia. La duración se muestra en este formato: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Si una de las consultas ha estado activa durante más de 24 horas, póngase en contacto con el Servicio de atención al cliente para que identifique y resuelva el problema. En ese caso, deberá proporcionarles la variable **[!UICONTROL PID]** valor de columna, que es un identificador único para la consulta.
