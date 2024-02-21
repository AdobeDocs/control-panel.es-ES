---
product: campaign
solution: Campaign
title: Supervisión de perfiles activos
description: Obtenga información en tiempo real sobre el uso y la evolución más recientes e históricos de los Perfiles activos para cada una de las instancias de Campaign.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: 73cf3102c0926728595e975ee4c85bf110f2a23d
workflow-type: tm+mt
source-wordcount: '418'
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
>No se tienen en cuenta los canales de Facebook y X (anteriormente conocido como Twitter).

Para obtener más información sobre los perfiles activos, consulte las documentaciones de [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=es) y [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=es#active-profiles).

## Monitorización del uso de perfiles activos {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Acerca de la monitorización de perfiles activos"
>abstract="En esta pestaña, puede obtener información en tiempo real sobre el uso y la evolución más recientes e históricos de los perfiles activos para cada una de las instancias de Campaign."

Para monitorizar el uso del perfil activo en el Panel de control, vaya a la tarjeta **[!UICONTROL Monitorización del rendimiento]** > pestaña **[!UICONTROL Perfiles activos]** y seleccione la instancia que desee de la **[!UICONTROL Lista de instancias]**.

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

La información relacionada con el uso de perfiles activos se actualiza en el Panel de control en función de los flujos de trabajo técnicos &quot;Facturación&quot; de [!DNL Campaign] dedicados que se ejecutan todos los días en las instancias:

| Versión de la campaña | Flujo de trabajo técnico | Ejecuciones |
|  ---  |  ---  |  ---  |
| Campaign Standard | [Facturación](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=es) | Diaria |
| Campaign v7/v8 | [Facturación](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=es) | Mensual |

