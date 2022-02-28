---
product: campaign
solution: Campaign
title: Monitorización de consultas activas
description: Aprenda a monitorizar las consultas activas en las instancias de Campaign en el Panel de control de Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: a1ea14f9-ec1d-4e10-89ef-846065512e8c
source-git-commit: 7078ff03bf2e4d156a71de4d900cbfcbd2ded312
workflow-type: ht
source-wordcount: '103'
ht-degree: 100%

---

# Monitorización de consultas activas {#long-running-queries}

El área **[!UICONTROL Active queries]** de la pestaña **[!UICONTROL Databases]** lista las cinco consultas que se han estado ejecutando durante el mayor tiempo en la instancia seleccionada.

![](assets/active-queries.png)

Las columnas **[!UICONTROL Duration]** especifican cuánto tiempo se ha estado ejecutando una consulta en la instancia. La duración se muestra en este formato: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Si una de las consultas ha estado activa durante más de 24 horas, póngase en contacto con el Servicio de atención al cliente para que identifique y resuelva el problema. Deberá proporcionarles el valor de columna **[!UICONTROL PID]**, que es un identificador único para la consulta.
