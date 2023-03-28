---
product: campaign
solution: Campaign
title: Eliminación de la delegación de subdominios
description: Obtenga información sobre cómo quitar la delegación de subdominios en Adobe.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: dbd1b2dd31cf732609f8a515e9adc1c43cbf39c6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Eliminación de la delegación de subdominios en Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Quitar delegación del subdominio"
>abstract="Esta pantalla le permite eliminar la delegación de un subdominio en Adobe. Tenga en cuenta que este proceso no se puede deshacer y es irreversible hasta que se complete su ejecución.<br><br>Si intenta quitar la delegación de un dominio principal para la instancia seleccionada, se le pedirá que elija el dominio que lo reemplazará."

El Panel de control de Campaign le permite eliminar la delegación de un subdominio que se ha delegado completamente en el Adobe o en el que se ha delegado mediante CNAME.

## Notas importantes {#important}

Antes de continuar, considere detenidamente los impactos que se producirán una vez que se activa el proceso de eliminación:

* Una vez activado el proceso, la eliminación de la delegación de subdominios no se puede deshacer y es irreversible hasta que se completa la ejecución del proceso.
* No se puede eliminar ninguna otra delegación de subdominios cuando hay un proceso similar en progreso en otro subdominio.
* Una delegación eliminada en un subdominio no se puede volver a delegar hasta tres días después de su eliminación.

## Eliminación de una delegación de subdominio {#steps}

Para eliminar la delegación de un subdominio en Adobe, siga estos pasos:

1. Haga clic en el botón de los tres puntos situado junto a la delegación de dominio que desee quitar y seleccione **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. Revise el aviso y confirme que se ha eliminado la delegación del dominio en Adobe.

1. Revise la información relativa a la instancia a la que está asociado el subdominio, incluidas las afinidades de IP y configuraciones de marca relacionadas.

   Si va a eliminar la delegación del dominio principal para la instancia seleccionada, debe elegir el dominio que lo reemplazará mediante la lista **[!UICONTROL Replacement Domain]**.

   Haga clic en **[!UICONTROL Next]** para continuar con la eliminación.

   ![](assets/undelegate-subdomain-details.png)

1. Si quita una delegación de tipo CNAME o si va a reemplazar un dominio principal por un dominio delegado mediante CNAME, se agregará un **[!UICONTROL Action]** para administrar los registros DNS. [Obtenga más información en esta sección](#dns)

1. Revise el resumen que se muestra. Para confirmar la eliminación, escriba la URL del dominio cuya delegación desea quitar y haga clic en **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

Una vez iniciada la eliminación de la delegación, el trabajo pendiente se muestra en los registros de trabajos hasta que se completa.

![](assets/undelegate-job.png)

## Administración de registros DNS {#dns}

Para configurar una delegación de dominios con CNAME, Panel de control de Campaign requiere que agregue registros específicos en el servidor DNS. [Obtenga información sobre cómo configurar subdominios mediante CNAME](setting-up-new-subdomain.md#use-cnames)

Al quitar una delegación de tipo CNAME, debe **quitar estos registros DNS** del servidor para evitar problemas. Además, si desea eliminar la delegación de un subdominio principal y sustituirlo por un dominio que se haya delegado mediante CNAME, es posible que tenga que **agregar registros DNS** en el servidor, según las afinidades IP establecidas para el subdominio.

La tabla siguiente enumera las acciones que se deben realizar según el tipo de delegación que elimine y el tipo de delegación que se utilice para configurar el dominio de reemplazo.

| Delegación eliminada | Dominio de reemplazo | Acción requerida |
|  ---  |  ---  |  ---  |
| Completo | Sin dominio de reemplazo | No se requiere ninguna acción |
| Completo | CNAME | Añadir registros DNS (opcional en función de las afinidades IP) |
| Completo | Completo | No se requiere ninguna acción |
| CNAME | Sin dominio de reemplazo | Eliminar registros DNS |
| CNAME | CNAME | Eliminar y agregar registros DNS (opcional en función de las afinidades IP) |
| CNAME | Completo | Eliminar registros DNS |

Para ello, agregue un **[!DNL Action]** antes de confirmar la eliminación de la delegación. Esta pantalla muestra los registros DNS que se van a quitar o agregar, según el contexto.

![](assets/action-step.png)

### Eliminar registros DNS

1. Vaya al servidor DNS y elimine los registros enumerados en el Panel de control de Campaign.
1. Vuelva al Panel de control de Campaign y haga clic en **[!UICONTROL Next]** para continuar con la eliminación de la delegación.

### Agregar registros DNS

1. Vaya al servidor DNS y agregue los registros enumerados en Panel de control de Campaign.
1. Espere a que la adición de DNS sea efectiva.
1. Vuelva al Panel de control de Campaign y haga clic en **[!UICONTROL Verify]**.
1. Una vez verificada correctamente la adición de registros, haga clic en **[!UICONTROL Next]** para continuar con la eliminación de la delegación.

## Códigos de error {#FAQ}

En esta sección se enumeran los mensajes de error que pueden surgir al intentar quitar la delegación de un subdominio:

| Código de error | Mensaje | Descripción |
|  ---  |  ---  |  ---  |
| 8002 | La eliminación del dominio delegado solicitada no se puede atender porque hay una solicitud similar en progreso que se solapa. Inténtelo pasados 3 días | Ya hay un trabajo de eliminación de delegación de subdominios en proceso para la instancia seleccionada. Espere hasta tres días para iniciar un nuevo trabajo de eliminación. |
| 8003 | La eliminación del dominio delegado solicitada no se admite para esta instancia. | No se admite la eliminación de delegaciones para el subdominio seleccionado debido a un problema técnico. Póngase en contacto con el Servicio de atención al cliente. |
| 8004 | No se permite la eliminación del dominio delegado solicitada, ya que solo hay un dominio en esta instancia. | Solo se ha delegado un subdominio para la instancia seleccionada. No se permite eliminar la delegación. |
| 8005 | Esta configuración no admite la eliminación del dominio delegado solicitada. | No se admite la eliminación de delegaciones para el subdominio seleccionado debido a un problema técnico. Póngase en contacto con el Servicio de atención al cliente. |
| 8006 | No se permite la eliminación del dominio delegado solicitada por razones desconocidas. Póngase en contacto con el Servicio de atención al cliente. | No se admite la eliminación de delegaciones para la instancia seleccionada debido a problemas desconocidos. Póngase en contacto con el Servicio de atención al cliente. |
