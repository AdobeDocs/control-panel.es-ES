---
title: Administración de almacenamientos SFTP
description: Obtenga información sobre cómo supervisar y administrar el almacenamiento del servidor SFTP
translation-type: tm+mt
source-git-commit: 834adb7c937a9927901f91e257a8df44e72ca45b

---


# Administración de almacenamientos SFTP {#sftp-storage-management}

>[!CONTEXTUALHELP]
>id=&quot;cp_almacenamiento&quot;
>title=&quot;Acerca de la capacidad de almacenamiento&quot;
>abstract=&quot;En esta ficha, puede realizar la vista de la capacidad de almacenamiento y de la información de utilización de sus servidores SFTP. Aquí solo se muestran los servidores SFTP a los que tiene acceso. Póngase en contacto con el administrador para solicitar acceso a otros servidores SFTP.&quot;
>extra-url=&quot;https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4&quot; text=&quot;Ver vídeo de demostración&quot;

Es posible que tenga una capacidad de almacenamiento diferente aprovisionada en el servidor SFTP, según las condiciones contractuales.

Es esencial que supervise regularmente el espacio disponible para cada uno de los servidores SFTP. De lo contrario, es posible que ya no pueda guardar ningún archivo adicional en el servidor o ejecutar correctamente flujos de trabajo que dependan de las actualizaciones de este servidor.

**Temas relacionados:**

* [Vídeo de tutorial de Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/monitoring-server-capacity-whitelisting-adding-ssh-key.html)
* [Vídeo de tutorial de Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Acceso a la información de capacidad de almacenamiento {#accessing-storage-capacity-information}

La información sobre el espacio utilizado por todas las instancias a las que tiene acceso está disponible en la **[!UICONTROL Storage]** ficha de la tarjeta SFTP. Se actualiza en cada actualización de página.

![](assets/control_panel_space.png)

En cada caso, una alerta visual le permite saber cuándo su almacenamiento supera su capacidad:

* **Naranja**: la instancia superó el 80 % de su capacidad,
* **Rojo**: la instancia supera el 90% de su capacidad.

También hay disponibles sugerencias adicionales para ayudarle a saber cómo proceder con el servidor a medida que se acerca su capacidad.

## Prácticas recomendadas cuando se agota la capacidad de almacenamiento {#best-practices-when-capacity-runs-out}

1. **Limpie el servidor SFTP de archivos** antiguos o innecesarios. Para obtener más información sobre cómo acceder a la carpeta del servidor SFTP, consulte [esta sección](../../sftp/using/logging-into-sftp-server.md).
1. Asegúrese de que los **flujos de trabajo** que limpian los servidores SFTP se ejecutan correctamente. Para obtener más información sobre flujos de trabajo técnicos en Adobe Campaign, consulte los documentos dedicados al [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) y al [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) .
1. Póngase en contacto con el equipo de su cuenta para **solicitar más almacenamientos** (pueden aplicarse cargos adicionales).
1. Póngase en contacto con el **Servicio de atención al cliente** si cree que hay algún problema.
