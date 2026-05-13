---
product: campaign
solution: Campaign
title: Resumen de almacenamiento
description: Descubra cómo monitorizar en el Panel de control los diferentes recursos de Campaign que están consumiendo espacio de base de datos en sus instancias.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
TQID: https://experienceleague.adobe.com/3zcScy61C5LHsWM86WWWuy0uic-pdNQGKc0qY7ewwOQ
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: tm+mt
source-wordcount: 180
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
