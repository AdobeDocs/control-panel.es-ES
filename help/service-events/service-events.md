---
product: campaign
solution: Campaign
title: Supervisar los contactos y eventos clave
description: 'Obtenga información sobre cómo identificar eventos que se producen en las instancias y contactos clave en el Adobe. '
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: da68420340ea8605f6e1347e86797c9e6a790ea6
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 1%

---

# Supervisar los contactos y eventos clave {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Calendario de servicios"
>abstract="La sección Contactos clave enumera las personas en Adobe con las que ponerse en contacto para cualquier solicitud o problema de las instancias. En la sección Calendario de eventos de servicio , puede identificar todas las versiones y revisiones de servicio pasadas y próximas para la instancia seleccionada."

>[!IMPORTANT]
>
>El calendario de servicios está disponible en versión beta y sujeto a frecuentes actualizaciones y modificaciones sin previo aviso.

La identificación de eventos planificados en las instancias es esencial para monitorizar las instancias de Campaign.

Con el Panel de control de Campaign, puede supervisar las versiones y revisiones de servicio que se producen en las instancias y acceder a una lista de contactos clave en el Adobe para cualquier solicitud o problema.

Se puede acceder a esta información desde la **[!UICONTROL Service Calendar]** en la página de inicio del Panel de control de Campaign.

## Contactos clave {#key-contacts}

La variable **[!UICONTROL Key contacts]** lista las personas en el Adobe con las que puede ponerse en contacto para cualquier solicitud o problema de las instancias.

>[!NOTE]
>
>Esta sección muestra información solamente para cuentas de servicio administradas.

![](assets/service-events-contacts.png)

Los contactos clave incluyen las siguientes funciones:

* **[!UICONTROL TAM]**: Administrador técnico de cuentas,
* **[!UICONTROL CSM]**: Administrador de éxito de clientes,
* **[!UICONTROL Deliverability]**: punto de contacto para operaciones de envío,
* **[!UICONTROL Transition Manager]**: Managed Services Transition Manager (solo cuenta de Managed Services),
* **[!UICONTROL On-boarding Specialist]**: Especialista asignado a la cuenta para ayudarle en la incorporación al Campaign Classic (solo cuenta de Managed Services).

## Eventos {#events}

La variable **[!UICONTROL Service Event Calendar]** muestra todas las versiones anteriores y futuras, así como las revisiones de servicio de la instancia seleccionada.

![](assets/service-events-calendar.png)

La variable **[!UICONTROL Note]** proporciona información sobre el estado de cada versión:

* **[!UICONTROL General availability]**: Última compilación estable disponible.
* **[!UICONTROL Limited availability]**: Solo implementación bajo demanda.
* **[!UICONTROL Release candidate]**: Ingeniería validada. Esperando pruebas de producción.
* **[!UICONTROL Pre release]**: Disponibilidad anticipada para necesidades específicas del cliente.
* **[!UICONTROL No longer available]**: La versión no presenta ningún problema importante, pero hay una nueva disponible con correcciones de errores adicionales. Se requiere una actualización.
* **[!UICONTROL Deprecated]**: Genere la incrustación de regresiones conocidas.
La compilación ya no es compatible. Una actualización es obligatoria.

Puede asignar un indicador a uno o varios eventos próximos para realizar un seguimiento de ellos. Para ello, haga clic en el botón elipse situado junto al nombre del evento.

![](assets/service-events-flag.png)
