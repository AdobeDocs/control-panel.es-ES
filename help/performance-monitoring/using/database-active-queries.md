---
product: campaign
solution: Campaign
title: Monitorización de consultas activas
description: Aprenda a monitorizar las consultas activas en las instancias de Campaign en el Panel de control.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a1ea14f9-ec1d-4e10-89ef-846065512e8c
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 100%

---

# Monitorización de consultas activas {#long-running-queries}

El área **[!UICONTROL Consultas activas]** de la pestaña **[!UICONTROL Bases de datos]** enumera las cinco consultas que se han estado ejecutando durante el mayor tiempo en la instancia seleccionada.

![](assets/active-queries.png)

Las columnas **[!UICONTROL Duración]** especifican cuánto tiempo se ha estado ejecutando una consulta en la instancia. La duración se muestra en este formato: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Si una de las consultas ha estado activa durante más de 24 horas, póngase en contacto con el Servicio de atención al cliente para que identifique y resuelva el problema. Tendrá que proporcionarles el valor de la columna **[!UICONTROL PID]**, que es un identificador único para la consulta.
