---
product: campaign
solution: Campaign
title: Alertas por correo electrónico
description: Obtenga información sobre cómo recibir notificaciones por correo electrónico en caso de problemas con las instancias de Campaign
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: 6249776ef4981cd3d706bf1946be0e054b471fb6
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# Alertas por correo electrónico {#email-alerting}

Con el fin de proporcionar buena flexibilidad a su trabajo, Panel de control de Campaign está equipado con funciones de alerta por correo electrónico en tiempo real.

Para suscribirse a estas alertas, siga estos pasos:

1. Haga clic en el **[!UICONTROL Alerting notifications]** disponible desde cualquier ubicación del Panel de control de Campaign y haga clic en **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Se envía un correo electrónico para confirmar la suscripción.

   ![](assets/email_subscription.png)

1. Tras la suscripción, el Panel de control de Campaign notificará los problemas del sistema y recomendará las acciones que deben realizarse. Las alertas por correo electrónico se envían a todos los que se han registrado para **todas las instancias** que son administradores de.

   ![](assets/alert_sample.png)

La lista de alertas es la siguiente:

* **Uso del almacenamiento SFTP**: Uno de los servidores SFTP ha alcanzado el 80 % o más de su capacidad. Consulte [Administración de almacenamiento SFTP](../../sftp/using/sftp-storage-management.md).

* **Uso de la base de datos**: Una de las bases de datos de instancias ha alcanzado el 80% o más de su capacidad. Consulte [Supervisión de bases de datos](../../performance-monitoring/using/database-monitoring.md).

* **Caducidad del certificado SSL**: Uno de los certificados SSL de los subdominios ha caducado o va a caducar en 60 días o menos. Consulte [Supervisión de los certificados SSL de los subdominios](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

* **Caducidad de la lista de permitidos de SFTP**: Uno de los intervalos de IP definidos ha caducado o va a caducar en 10 días o menos. Consulte [Adición de rangos de IP a la lista de permitidos](../../sftp/using/ip-range-allow-listing.md).

* **Caducidad de clave pública SFTP**: Una de las claves públicas que definió caducó o caducará en 10 días o menos. Consulte [Administración de claves](../../sftp/using/key-management.md).