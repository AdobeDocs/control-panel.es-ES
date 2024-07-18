---
product: campaign
solution: Campaign
title: Identificación de los contactos y eventos clave
description: Obtenga información sobre cómo identificar eventos que se producen en las instancias y contactos clave en Adobe.
feature: Control Panel, Monitoring
role: Admin
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 100%

---

# Identificación de los contactos y eventos clave {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Calendario de servicios"
>abstract="La sección Contactos clave enumera las personas en Adobe con las que ponerse en contacto para cualquier solicitud o problema de las instancias. En la sección Calendario de eventos de servicios, puede identificar las versiones y alertas pasadas o futuras de la instancia seleccionada, así como configurar recordatorios para un evento determinado."

>[!IMPORTANT]
>
>El Calendario de servicios estará disponible en la versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

Para monitorizar de forma eficaz las instancias de Campaign, es crucial seguir los eventos importantes que pueden afectar potencialmente a su(s) instancia(s). El Panel de control de Campaign le permite identificar eventos como nuevas versiones, actualizaciones, parches, correcciones rápidas, etc. y proporciona una lista de contactos de Adobe clave para cualquier solicitud o problema.

Se puede acceder a esta información desde la tarjeta **[!UICONTROL Calendario de servicios]** de la página de inicio del Panel de control.

## Contactos clave {#key-contacts}

La sección **[!UICONTROL Contactos clave]** lista las personas en Adobe con las que puede ponerse en contacto para cualquier solicitud o problema sobre las instancias.

>[!NOTE]
>
>Esta sección solo muestra información para cuentas de servicio administradas.

![](assets/service-events-contacts.png)

Los contactos clave incluyen las siguientes funciones:

* **[!UICONTROL TAM]**: administrador de cuentas técnico,
* **[!UICONTROL CSM]**: Customer Success Manager,
* **[!UICONTROL Entregabilidad]**: punto de contacto para las operaciones de entregabilidad,
* **[!UICONTROL Gestor de transición]**: gestor de transición de Managed Services (solo para la cuenta de Managed Services),
* **[!UICONTROL Especialista en incorporación]**: especialista asignado a la cuenta para ayudarle en la incorporación a Campaign Classic (solo para la cuenta de Managed Services).

## Seguimiento de los eventos importantes {#events}

La sección **[!UICONTROL Calendario de eventos de servicio]** muestra todas las versiones anteriores y futuras, así como las alertas a las que se suscribieron los usuarios en las alertas de correo electrónico del Panel de control. Además, el Panel de control de Campaign permite a los usuarios establecer recordatorios y marcar eventos relevantes para la instancia seleccionada a fin de que estén mejor organizados y sean más eficientes.

Los eventos se muestran en un calendario o en una lista. Puede alternar entre las dos vistas mediante los botones **[!UICONTROL Calendario]** y **[!UICONTROL Lista]** situados en la esquina superior derecha de la sección.

![](assets/service-events-calendar.png)

<table><tr style="border: 0;">
<td><img src="assets/do-not-localize/nav-buttons.png">
</td><td>En la vista de calendario, los botones de navegación están disponibles en la esquina superior derecha para ayudarle a examinar los eventos. Utilice las <b>flechas dobles</b> para ir al primer evento presente después o antes del mes seleccionado y las <b>flechas únicas</b> para pasar de un mes a otro. Haga clic en <b>botón de círculo</b> para volver a la vista de hoy.</td>
</tr></table>

Se muestran tres tipos de eventos:

* **Recordatorios** establecidos por los usuarios para recibir notificaciones antes de que se produzca un evento. Se muestran en verde en la vista de calendario. [Aprenda a configurar el recordatorio](#reminders)
* **Alertas** enviadas por correo electrónico por el Panel de control de Campaign para notificar a los usuarios de problemas en sus instancias, como una sobrecarga del almacenamiento o la caducidad del certificado SSL. Se muestran en naranja en la vista de calendario. La descripción del evento especifica si la alerta se envía al usuario que ha iniciado sesión, según su suscripción a alertas de correo electrónico. [Obtenga más información sobre la funcionalidad de alertas por correo electrónico del Panel de control de Campaign](../performance-monitoring/using/email-alerting.md)

* Las **Versiones** indican las implementaciones pasadas y próximas a la instancia, que se muestran respectivamente en gris y azul en la vista calendario. Los detalles del evento especifican el tipo de versión asociada a cada implementación:

   * **[!UICONTROL Disponibilidad general]**: última versión estable disponible.
   * **[!UICONTROL Disponibilidad limitada]**: solo implementación a petición.
   * **[!UICONTROL Liberar candidato]**: validado por ingeniería. Esperando pruebas de producción.
   * **[!UICONTROL Versión preliminar]**: disponibilidad anticipada para necesidades específicas del cliente.
   * **[!UICONTROL Ya no está disponible]**: la versión no presenta ningún problema importante, pero hay una nueva disponible con correcciones de errores adicionales. Se requiere una actualización.
   * **[!UICONTROL Obsoleto]**: regresiones conocidas de la incrustación de la versión. La versión ya no es compatible. Es obligatorio actualizar.

Puede asignar un indicador a uno o varios eventos próximos para realizar un seguimiento de ellos. Para ello, haga clic en el botón de los tres puntos situado junto al nombre del evento.

![](assets/service-events-flag.png)

## Definición de recordatorios {#reminders}

Con el Calendario de servicios, puede configurar recordatorios para recibir notificaciones por correo electrónico antes de que se produzca un evento.

>[!NOTE]
>
>Para recibir notificaciones acerca de próximos eventos, asegúrese de haberse suscrito a las alertas de correo electrónico en el Panel de control. [Más información](../performance-monitoring/using/email-alerting.md)

Para establecer una alerta para un evento, siga estos pasos:

1. Pase el ratón por encima del evento que desea que se le recuerde o haga clic en el botón de los tres puntos en la vista de lista y seleccione **[!UICONTROL Definición de recordatorio]**.

1. Asigne un título al recordatorio y seleccione la fecha en la que desea que se le notifique antes de que se produzca el evento.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Si no se ha suscrito a las alertas del Panel de control, se mostrará un mensaje que le permitirá suscribirse a las notificaciones por correo electrónico.

1. El recordatorio ahora se establece para el evento seleccionado. Puede pasar el ratón sobre él en cualquier momento para mostrar su título.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >Se pueden configurar hasta dos recordatorios para el mismo evento.

1. En la fecha especificada en el recordatorio, se enviará un correo electrónico para notificarle el próximo evento, y el recordatorio se eliminará automáticamente del recuento de **[!UICONTROL Recordatorios]** en el menú Calendario de servicios.
