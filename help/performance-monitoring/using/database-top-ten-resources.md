---
product: campaign
solution: Campaign
title: Los 10 recursos temporales principales
description: Obtenga información sobre cómo monitorizar en el Panel de control de Campaign los 10 recursos temporales más grandes generados por flujos de trabajo y envíos en la base de datos de Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: b17abddf6bad7e58cb7bd825cd97322427a0b21f
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 69%

---

# Los 10 recursos temporales principales {#top-10}

El área **[!UICONTROL Top 10 temporary resources]** enumera los 10 recursos temporales más grandes generados por flujos de trabajo y envíos.

La monitorización de flujos de trabajo y envíos que crean grandes recursos temporales es un paso clave para monitorizar la base de datos. Si algún recurso temporal consume demasiado espacio en la base de datos, asegúrese de que es necesario tener este flujo de trabajo o envío y, finalmente, vaya a la instancia para pararlo.

>[!IMPORTANT]
>
>La recomendación general es evitar tener **más de 40 columnas** en recursos que no sean predeterminados. Si se ve que un flujo de trabajo tiene un gran número de recuentos de tablas o tamaño de base de datos, se recomienda revisar el flujo de trabajo para investigar por qué está generando tantos datos.
>
>Las directrices para Campaign Standards y Clásicos también están disponibles en [esta página](database-preventing-overload.md) para ayudarle a evitar la sobrecarga de la base de datos.

![](assets/database-top10.png)

El **[!UICONTROL View all]** permite acceder a la **[!UICONTROL Storage overview]** detalles para obtener información detallada sobre estos recursos temporales. Para obtener más información, consulte [esta página](database-storage-overview.md).
