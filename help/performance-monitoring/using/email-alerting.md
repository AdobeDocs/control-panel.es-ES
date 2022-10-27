---
product: campaign
solution: Campaign
title: Alertas por correo electrónico
description: Obtenga información sobre cómo recibir notificaciones por correo electrónico en caso de problemas con las instancias de Campaign
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 2%

---

# Alertas por correo electrónico {#email-alerting}

Con el fin de proporcionar buena flexibilidad a su trabajo, Panel de control de Campaign está equipado con funciones de alerta por correo electrónico en tiempo real.

## Lista de alertas {#list}

La lista de alertas es la siguiente:

* **Uso del almacenamiento SFTP**: Uno de los servidores SFTP ha alcanzado el 80 % o más de su capacidad. Consulte [Administración de almacenamiento SFTP](../../sftp/using/sftp-storage-management.md).

* **Uso de la base de datos**: Una de las bases de datos de instancias ha alcanzado el 80% o más de su capacidad. Consulte [Supervisión de bases de datos](../../performance-monitoring/using/database-monitoring.md).

* **Caducidad de la lista de permitidos de SFTP**: Uno de los intervalos de IP definidos ha caducado o va a caducar en 10 días o menos. Consulte [Adición de rangos de IP a la lista de permitidos](../../sftp/using/ip-range-allow-listing.md).

* **Caducidad de clave pública SFTP**: Una de las claves públicas que definió caducó o caducará en 10 días o menos. Consulte [Administración de claves](../../sftp/using/key-management.md).

* **Caducidad del certificado SSL**: Uno de los certificados SSL de los subdominios ha caducado o va a caducar en 30 días o menos. Consulte [Supervisión de los certificados SSL de los subdominios](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>Además, el Panel de control de Campaign le permite **establecer recordatorios** para recibir notificaciones por correo electrónico antes de que se produzca un evento en las instancias (versiones y revisiones de servicios).
>
>Para ello, debe haberse suscrito a las alertas de correo electrónico y establecer un recordatorio para los próximos eventos que desee. [Obtenga información sobre cómo configurar recordatorios para eventos próximos](../../service-events/service-events.md#reminders)

## Suscribirse a alertas {#subscribe}

Para suscribirse a estas alertas, siga estos pasos:

1. Haga clic en el **[!UICONTROL Alerting notifications]** disponible desde cualquier ubicación del Panel de control de Campaign y haga clic en **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Se envía un correo electrónico para confirmar la suscripción.

   ![](assets/email_subscription.png)

1. Tras la suscripción, el Panel de control de Campaign notificará los problemas del sistema y recomendará las acciones que deben realizarse. Las alertas por correo electrónico se envían a todos los que se han registrado para **todas las instancias** que son administradores de.

   ![](assets/alert_sample.png)
