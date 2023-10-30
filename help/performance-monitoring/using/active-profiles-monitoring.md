---
product: campaign
solution: Campaign
title: Supervisión de perfiles activos
description: Obtenga información en tiempo real sobre el uso y la evolución más recientes e históricos de los Perfiles activos para cada una de las instancias de Campaign.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '433'
ht-degree: 100%

---

# Monitorización de perfiles activos {#active-profiles-monitoring}

## Acerca de los perfiles activos {#about-active-profiles}

>[!IMPORTANT]
>
>La monitorización de perfiles activos desde el Panel de control está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso. Está disponible en la versión 10368 de Campaign Standard.

Según el contrato, cada una de las instancias de Campaign se aprovisiona con una cantidad específica de perfiles activos que se contabilizan a efectos de facturación. Consulte su contrato más reciente para obtener una referencia sobre la cantidad de perfiles activos adquiridos.

Un “perfil” es un registro de información (por ejemplo, un registro de la tabla nmsRecipient o una tabla externa que contiene una ID de cookie, ID de cliente, ID móvil u otra información relacionada con un canal determinado) que representa a un cliente final, a un cliente potencial o a un contacto.

Los perfiles se consideran activos si se han segmentado o si se ha comunicado con ellos en los últimos 12 meses.

>[!NOTE]
>
>Los canales de Facebook y Twitter no se tienen en cuenta.

Para obtener más información sobre los perfiles activos, consulte las documentaciones de [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=es) y [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=es#active-profiles).

## Monitorización del uso de perfiles activos {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Acerca de la monitorización de perfiles activos"
>abstract="En esta pestaña, puede obtener información en tiempo real sobre el uso y la evolución más recientes e históricos de los perfiles activos para cada una de las instancias de Campaign."

La información relacionada con el uso de perfiles activos se actualiza en el Panel de control en función de los Flujos de trabajo técnicos de [!DNL Campaign] dedicados que se ejecutan todos los días en las instancias:
* Flujo de trabajo [&quot;Facturación&quot;](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=es) para Campaign Standard.
* Flujo de trabajo [&quot;Número de perfiles de facturación activos&quot;](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=es) para Campaign v7/v8.


Para supervisar el uso de perfiles activos en el Panel de control de Campaign, vaya a la pestaña tarjeta de **[!UICONTROL Performance Monitoring]** > **[!UICONTROL Active Profiles]** y seleccione la instancia que desee en **[!UICONTROL Instance List]**.

Se muestra información sobre el uso de perfiles activos.

![](assets/active-profiles-graph.png)

La sección superior muestra la siguiente información:

* El recuento de perfiles activos que se utilizan actualmente en la instancia seleccionada, junto con la marca de tiempo de la ejecución del flujo de trabajo de facturación más reciente para su instancia.

* Recuento total de perfiles activos utilizados en su organización en todas las instancias.

  >[!NOTE]
  >
  >Esta sección solo está visible si tiene varias instancias asociadas a su organización.

* Recuento total de perfiles activos asignados a su organización.

La sección inferior proporciona una representación visual del uso del perfil activo durante los últimos 30 días. Puede cambiar este lapso de tiempo a 1 año utilizando el filtro situado en la esquina superior derecha. Al pasar el ratón por encima de una de las barras de gráficos, podrá obtener la cantidad exacta de perfiles activos utilizados en el período seleccionado.
