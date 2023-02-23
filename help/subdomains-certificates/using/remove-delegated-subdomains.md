---
product: campaign
solution: Campaign
title: Eliminar delegación de subdominios
description: Obtenga información sobre cómo eliminar la delegación de subdominios a Adobe.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 5a8c4c4d1c5c527135901cd41f2b0936af8737b4
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 2%

---

# Eliminar delegación de subdominios al Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Quitar delegación de subdominios"
>abstract="Esta pantalla le permite eliminar la delegación de un subdominio al Adobe. Tenga en cuenta que este proceso no se puede deshacer ni detener una vez enviado.<br><br>Si está intentando eliminar la delegación de un dominio principal para la instancia seleccionada, se le pedirá que elija el dominio que lo sustituirá."

Panel de control de Campaign le permite eliminar la delegación de un subdominio que se ha delegado en el Adobe, incluida la configuración de CNAME.

## Notas importantes {#important}

Antes de continuar, tenga en cuenta los impactos que se producen una vez activado el proceso de eliminación:

* La eliminación de la delegación de subdominios no se puede deshacer y será irreversible una vez iniciada hasta que se ejecute el proceso.
* No se puede quitar ninguna otra delegación de subdominios si hay un proceso similar en otro subdominio en curso.
* Una delegación eliminada de un subdominio no se puede volver a delegar hasta 3 días después de su eliminación.

## Eliminación de una delegación de subdominios {#steps}

Para eliminar la delegación de un subdominio al Adobe, siga estos pasos:

1. Haga clic en el botón de puntos suspensivos situado junto a la delegación de dominio que desee eliminar y seleccione **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. Revise la renuncia de responsabilidad y reconozca la eliminación de la delegación de dominios al Adobe.

1. Revise la información sobre la instancia a la que está asociado el subdominio, incluidas las afinidades de IP relacionadas y las configuraciones de marca.

   Si quita la delegación del dominio principal de la instancia seleccionada, debe elegir el dominio que la sustituirá con la variable **[!UICONTROL Replacement Domain]** lista.

   Haga clic en **[!UICONTROL Next]** para continuar con la eliminación.

   ![](assets/undelegate-subdomain-details.png)

1. Revise el resumen que aparece. Para confirmar la eliminación, escriba la dirección URL del dominio para el que desea eliminar la delegación y haga clic en **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

Una vez iniciada la eliminación de la delegación, el trabajo pendiente se muestra en los registros de trabajos hasta que se completa.

![](assets/undelegate-job.png)

## Códigos de error {#FAQ}

Esta sección enumera los mensajes de error que puede encontrar al intentar eliminar la delegación de un subdominio:

| Código de error | Mensaje | Descripción |
|  ---  |  ---  |  ---  |
| 8002 | No se puede abordar la eliminación del dominio delegado solicitado porque hay una solicitud de superposición similar en curso. Inténtelo después de 3 días | Ya se está procesando un trabajo de eliminación de delegación de subdominios para la instancia seleccionada. Espere hasta 3 días para iniciar un nuevo trabajo de eliminación. |
| 8003 | La eliminación del dominio delegado solicitado no es compatible con esta instancia. | La eliminación de delegación no es compatible con el subdominio seleccionado debido a un problema técnico, póngase en contacto con el Servicio de atención al cliente. |
| 8004 | No se permite la eliminación del dominio delegado solicitado, ya que solo hay un dominio en esta instancia. | Solo se ha delegado un subdominio para la instancia seleccionada. No se permite la eliminación de la delegación. |
| 8005 | La eliminación del dominio delegado solicitado no es compatible con esta configuración. | La eliminación de delegación no es compatible con el subdominio seleccionado debido a un problema técnico, póngase en contacto con el Servicio de atención al cliente. |
| 8006 | No se permite la eliminación del dominio delegado solicitado debido a motivos desconocidos. Póngase en contacto con el servicio de atención al cliente. | La eliminación de delegación no es compatible con la instancia seleccionada debido a problemas desconocidos, póngase en contacto con el Servicio de atención al cliente. |
