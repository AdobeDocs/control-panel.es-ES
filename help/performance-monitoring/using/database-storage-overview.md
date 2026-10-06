---
product: campaign
solution: Campaign
title: Resumen de almacenamiento
description: Descubra cómo monitorizar en el Panel de control los diferentes recursos de Campaign que están consumiendo espacio de base de datos en sus instancias.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
TQID: 'https://experienceleague.adobe.com/3zcScy61C5LHsWM86WWWuy0uic-pdNQGKc0qY7ewwOQ'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e519a22f-a06a-42fc-9d09-d78a3ab2c434
    internal-label: Monitoring guidelines
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 100%
---
# Resumen de almacenamiento {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Información general acerca del almacenamiento"
>abstract="En esta pestaña, puede obtener información detallada sobre los distintos recursos de Campaign que consumen espacio en la base de datos."

El área **[!UICONTROL Información general de almacenamiento]** proporciona una representación gráfica del espacio ocupado por:

* **[!UICONTROL Recursos del sistema]**

  Tenga en cuenta que, si los recursos del sistema consumen una gran parte del espacio de la base de datos, le recomendamos que se ponga en contacto con el Servicio de atención al cliente.

* **[!UICONTROL Tablas listas para usarse]** proporcionadas de forma predeterminada con las instancias de Campaign,
* **[!UICONTROL Tablas temporales]** creadas por flujos de trabajo y envíos,
* **[!UICONTROL Tablas no listas para usarse]** generadas después de crear recursos personalizados.

![](assets/database-storage-overview.png)

Haga clic en el botón **[!UICONTROL Ver detalles]** para obtener más detalles sobre los diferentes recursos que están consumiendo espacio de la base de datos.

Puede utilizar la lista desplegable para refinar la búsqueda y mostrar tablas de un tipo de recurso específico solamente (flujos de trabajo, envíos, destinatarios).

![](assets/database-storage-details.png)

Tenga en cuenta que esta pantalla también le permite monitorizar los parámetros del flujo de trabajo que pueden requerir una atención específica para evitar cualquier problema en las instancias. Obtenga más información en [esta página](workflow-monitoring.md).
