---
product: campaign
solution: Campaign
title: Alertas por correo electrónico
description: Descubra cómo recibir notificaciones por correo electrónico en caso de problemas con las instancias de Campaign
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '285'
ht-degree: 100%

---

# Alertas por correo electrónico {#email-alerting}

Para proporcionar una mayor flexibilidad al trabajo, el Panel de control está equipado con una funcionalidad de alerta por correo electrónico en tiempo real.

## Lista de alertas {#list}

La lista de alertas es la siguiente:

* **Uso de almacenamiento SFTP**: uno de los servidores SFTP ha alcanzado el 80 % o más de su capacidad. Consulte la[Administración del almacenamiento SFTP](../../sftp/using/sftp-storage-management.md).

* **Uso de bases de datos**: una de las bases de datos de las instancias ha alcanzado el 80 % o más de su capacidad. Consulte [Monitorización de bases de datos](../../performance-monitoring/using/database-monitoring.md).

* **Caducidad de listas de IP permitidas de SFTP**: uno de los rangos de IP que ha definido ha caducado o va a caducar en 10 días o menos. Consulte [Lista de rangos de IP permitidos](../../sftp/using/ip-range-allow-listing.md).

* **Caducidad de la clave pública de SFTP**: una de las claves públicas que ha definido ha caducado o va a caducar en 10 días o menos. Consulte [Administración de claves](../../sftp/using/key-management.md).

* **Caducidad del certificado SSL**: uno de los certificados SSL de los subdominios ha caducado o va a caducar en 30 días o menos. Consulte [Monitorización de los certificados SSL de los subdominios](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>Además, el Panel de control le permite **definir recordatorios** para recibir notificaciones por correo electrónico antes de que se produzca un evento en las instancias (versiones y revisiones de servicio).
>
>Para ello, tiene que haberse suscrito a las alertas por correo electrónico y definir un recordatorio para los próximos eventos que desee. [Descubra cómo definir recordatorios para los próximos eventos](../../service-events/service-events.md#reminders)

## Suscribirse a alertas {#subscribe}

Para suscribirse a estas alertas, siga estos pasos:

1. Haga clic en el botón **[!UICONTROL Notificaciones de alerta]** disponible desde cualquier ubicación del Panel de control y, a continuación, haga clic en **[!UICONTROL Suscribirse]**.

   ![](assets/subscribing.png)

1. Se enviará un correo electrónico para confirmar la suscripción.

   ![](assets/email_subscription.png)

1. Después de suscribirse, el Panel de control le notificará los problemas del sistema y le recomendará las acciones a tomar. Las alertas por correo electrónico se envían a todas las personas que se hayan suscrito a **todas las instancias** de las que sean Administradores.

   ![](assets/alert_sample.png)
