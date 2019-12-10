---
title: Administración de almacenamiento SFTP
description: Obtenga información sobre cómo supervisar y administrar el almacenamiento del servidor SFTP
translation-type: tm+mt
source-git-commit: 111c8fd461f6f1c567288acd7a83aee5ef7fce97

---


# Administración de almacenamiento SFTP {#sftp-storage-management}

Es posible que tenga una capacidad de almacenamiento diferente aprovisionada en el servidor SFTP, según las condiciones contractuales.

Es esencial que supervise regularmente el espacio disponible para cada uno de los servidores SFTP. De lo contrario, es posible que ya no pueda guardar ningún archivo adicional en el servidor ni ejecutar correctamente flujos de trabajo que dependan de las actualizaciones de este servidor.

**Temas relacionados:**

* [Vídeo del tutorial de Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-sftp-servers.html)
* [Vídeo del tutorial de Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Acceso a la información de capacidad de almacenamiento {#accessing-storage-capacity-information}

La **[!UICONTROL Top utilized SFTP disk capacity]**sección del encabezado incluye los tres servidores más utilizados y conectados a las instancias a las que tiene acceso de administrador. Esta información está disponible en todas las fichas de la tarjeta SFTP.

![](assets/control_panel_topspaceNEW.png)

La información sobre el espacio utilizado por todas las instancias a las que tiene acceso está disponible en la **[!UICONTROL Storage]**ficha de la tarjeta SFTP. Se actualiza en cada actualización de página.

![](assets/control_panel_spaceNEW.png)

Para cada caso, una alerta visual le permite saber cuándo su almacenamiento supera su capacidad:

* **Naranja**: la instancia superó el 80 % de su capacidad,
* **Rojo**: la instancia supera el 90% de su capacidad.

También hay disponibles sugerencias adicionales para ayudarle a saber cómo proceder con el servidor a medida que se acerca su capacidad.

## Prácticas recomendadas cuando se agota la capacidad de almacenamiento {#best-practices-when-capacity-runs-out}

1. **Limpie el servidor SFTP de archivos** antiguos o innecesarios. Para obtener más información sobre cómo acceder a la carpeta del servidor SFTP, consulte [esta sección](../../sftp/using/logging-into-sftp-server.md).
1. Asegúrese de que los **flujos de trabajo** que limpian los servidores SFTP se ejecutan correctamente. Para obtener más información sobre los flujos de trabajo técnicos en Adobe Campaign, consulte las documentaciones dedicadas de [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) y [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) .
1. Póngase en contacto con el equipo de su cuenta para **solicitar más almacenamiento** (se pueden aplicar cargos adicionales).
1. Póngase en contacto con el **Servicio de atención al cliente** si cree que hay algún problema.
