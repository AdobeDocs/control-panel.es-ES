---
product: campaign
solution: Campaign
title: Resumen de almacenamiento
description: Obtenga información sobre cómo monitorizar en la Panel de control de Campaign los diferentes recursos de Campaign que consumen espacio en la base de datos en las instancias.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---

# Resumen de almacenamiento {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Información general acerca del almacenamiento"
>abstract="En esta pestaña, puede obtener información detallada sobre los distintos recursos de Campaign que consumen espacio en la base de datos."

El área **[!UICONTROL Storage overview]** proporciona una representación gráfica del espacio ocupado por:

* **[!UICONTROL System resources]**

  Tenga en cuenta que, si los recursos del sistema consumen una gran parte del espacio de la base de datos, le recomendamos que se ponga en contacto con el Servicio de atención al cliente.

* **[!UICONTROL Out-of-the-box tables]** proporcionadas de forma predeterminada con las instancias de Campaign,
* **[!UICONTROL Temporary tables]** creadas por flujos de trabajo y envíos,
* **[!UICONTROL Non-out of the box tables]** generadas después de crear recursos personalizados.

![](assets/database-storage-overview.png)

Haga clic en el botón **[!UICONTROL View details]** para obtener más información sobre los distintos recursos que consumen espacio en la base de datos.

Puede utilizar la lista desplegable para restringir la búsqueda y mostrar solo las tablas de un tipo de recurso específico (flujos de trabajo, envíos, destinatarios).

![](assets/database-storage-details.png)

Tenga en cuenta que esta pantalla también le permite monitorizar los parámetros de flujo de trabajo que pueden requerir una atención específica para evitar problemas en las instancias. Obtenga más información en [esta página](workflow-monitoring.md).
