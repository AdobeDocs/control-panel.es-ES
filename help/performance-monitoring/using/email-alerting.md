---
product: campaign
solution: Campaign
title: Alertas por correo electrónico
description: Obtenga información sobre cómo recibir notificaciones por correo electrónico en caso de problemas con las instancias de Campaign
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 3%

---

# Alertas por correo electrónico {#email-alerting}

Para proporcionar una mayor flexibilidad a su trabajo, el Panel de control de Campaign está equipado con la funcionalidad de alertas por correo electrónico en tiempo real.

## Lista de alertas {#list}

La lista de alertas es la siguiente:

* **Uso de almacenamiento SFTP**: uno de los servidores SFTP ha alcanzado el 80 % o más de su capacidad. Consulte la[Administración del almacenamiento SFTP](../../sftp/using/sftp-storage-management.md).

* **Uso de base de datos**: una de las bases de datos de instancias ha alcanzado el 80 % o más de su capacidad. Consulte [Monitorización de bases de datos](../../performance-monitoring/using/database-monitoring.md).

* **Caducidad de lista de IP permitidas para SFTP**: uno de los intervalos de IP definidos ha caducado o caducará en 10 días o menos. Consulte [Lista de rangos de IP permitidos](../../sftp/using/ip-range-allow-listing.md).

* **Caducidad de clave pública SFTP**: una de las claves públicas que ha definido ha caducado o caducará en 10 días o menos. Consulte [Administración de claves](../../sftp/using/key-management.md).

* **Caducidad del certificado SSL**: Uno de los certificados SSL de los subdominios ha caducado o caducará en 30 días o menos. Consulte [Supervisión de los certificados SSL de los subdominios](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>Además, el Panel de control de Campaign le permite **definir recordatorios** para recibir notificaciones por correo electrónico antes de que se produzca un evento en las instancias (versiones y revisiones de servicio).
>
>Para ello, debe haberse suscrito a las alertas de correo electrónico y establecer un recordatorio para los próximos eventos deseados. [Aprenda a configurar recordatorios para próximos eventos](../../service-events/service-events.md#reminders)

## Suscribirse a alertas {#subscribe}

Para suscribirse a estas alertas, siga estos pasos:

1. Haga clic en **[!UICONTROL Notificaciones de alerta]** disponible desde cualquier ubicación del Panel de control de Campaign y, a continuación, haga clic en **[!UICONTROL Suscribirse]**.

   ![](assets/subscribing.png)

1. Se envía un correo electrónico para confirmar la suscripción.

   ![](assets/email_subscription.png)

1. Después de la suscripción, el Panel de control de Campaign le notificará los problemas del sistema y recomendará las acciones que debe realizar. Las alertas por correo electrónico se envían a todas las personas que se hayan registrado en **todas las instancias** que son administradores de.

   ![](assets/alert_sample.png)
