---
product: campaign
solution: Campaign
title: Supervisión de perfiles activos
description: Obtenga información en tiempo real sobre el uso y la evolución más recientes e históricos de los Perfiles activos para cada una de las instancias de Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: ebebff05669160b97de7e0d58d898ba0e3a30df1
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 41%

---

# Monitorización de perfiles activos {#active-profiles-monitoring}

## Acerca de los perfiles activos {#about-active-profiles}

>[!IMPORTANT]
>
>La monitorización de perfiles activos desde el Panel de control está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso. Está disponible en la versión del 10368 de Campaign Standard.

Según el contrato, cada una de las instancias de Campaign se aprovisiona con una cantidad específica de perfiles activos que se contabilizan a efectos de facturación. Consulte su contrato más reciente para obtener una referencia sobre la cantidad de perfiles activos adquiridos.

Un “perfil” es un registro de información (por ejemplo, un registro de la tabla nmsRecipient o una tabla externa que contiene una ID de cookie, ID de cliente, ID móvil u otra información relacionada con un canal determinado) que representa a un cliente final, a un cliente potencial o a un contacto.

Los perfiles se consideran activos si se han segmentado o si se ha comunicado con ellos en los últimos 12 meses.

>[!NOTE]
>
>Los canales de Facebook y Twitter no se tienen en cuenta.

Para obtener más información sobre perfiles activos, consulte [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) y [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) documentaciones.

## Monitorización del uso de perfiles activos {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Acerca de la monitorización de perfiles activos"
>abstract="En esta pestaña, puede obtener información en tiempo real sobre el uso y la evolución más recientes e históricos de los perfiles activos para cada una de las instancias de Campaign y de su organización."

La información relacionada con el uso de perfiles activos se actualiza en Panel de control de Campaign en función de las [!DNL Campaign] Flujos de trabajo técnicos que se ejecutan todos los días en las instancias:
* Flujo de trabajo [&quot;Facturación&quot;](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=es) para Campaign Standard.
* El [&quot;Número de perfiles de facturación activos&quot;](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=es) flujo de trabajo para Campaign v7/v8.


Para supervisar el uso de perfiles activos en el Panel de control de Campaign, vaya a **[!UICONTROL Performance Monitoring]** tarjeta > **[!UICONTROL Active Profiles]** y seleccione la instancia que desee en la pestaña **[!UICONTROL Instance List]**.

Se muestra información sobre el uso de perfiles activos.

![](assets/active-profiles-graph.png)

La sección superior muestra la siguiente información:

* El recuento de perfiles activos que se utilizan actualmente en la instancia seleccionada, junto con la marca de tiempo de la ejecución del flujo de trabajo de facturación más reciente para su instancia.

* Recuento total de perfiles activos utilizados en su organización en todas las instancias. Esta sección solo está visible si tiene varias instancias asociadas a su organización.

* Recuento total de perfiles activos asignados a su organización.

La sección inferior proporciona una representación visual del uso del perfil activo durante los últimos 30 días. Puede cambiar este lapso de tiempo a 1 año utilizando el filtro situado en la esquina superior derecha. Al pasar el ratón por encima del gráfico, podrá obtener la cantidad exacta de perfiles activos utilizados en el periodo seleccionado.
