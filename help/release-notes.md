---
product: campaign
solution: Campaign
title: Versiones del Panel de control
description: Últimas notas de la versión de Panel de control de Campaign.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 8c604e9b1f657be938b04d096ac22efed99e1cbe
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 73%

---

# Versiones del Panel de control {#control-panel-releases}

Aquí encontrará información sobre las últimas versiones del Panel de control de Campaign.

>[!NOTE]
>
>Todos los usuarios administradores pueden acceder al Panel de control de Campaign. Los pasos para otorgar acceso de administrador a un usuario se detallan en [esta sección](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=es#discover-control-panel).
>
>Para Campaign Classic v7, tenga en cuenta que la instancia debe estar alojada en AWS y actualizarse con la última [versión estable](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/gs-release/rn-overview.html). Aprenda a comprobar su versión en [esta sección](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=es#getting-your-campaign-version). Para comprobar si la instancia está alojada en AWS, siga los pasos detallados en [esta página](faq.md).

## Octubre de 2021 {#october-2021}

**Intervalo de IP y periodo de validez de clave pública**

Ahora es posible establecer una duración para la disponibilidad de intervalos de IP y claves públicas. Obtenga más información en la [Adición de rangos de IP a la lista de permitidos](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) y [Administración de claves](sftp/using/key-management.md#installing-ssh-key) secciones.

**Rango de IP y edición de clave pública**

Ahora puede editar el [Intervalos de IP](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) y [claves públicas](sftp/using/key-management.md#editing-public-keys) que cree. Tenga en cuenta que esta función no está disponible para los elementos creados antes de la versión de Panel de control de Campaign actual.

**Alerta sobre el intervalo IP SFTP y la caducidad de la clave pública**

La funcionalidad de alertas por correo electrónico ahora incluye alertas sobre la IP SFTP que permiten enumerar la caducidad y la caducidad de la clave pública SFTP. [Más información](performance-monitoring/using/email-alerting.md)

**Compatibilidad total con Campaign v8**

La variable **Subdominio** y **Certificado** las funciones de administración ahora son compatibles con Panel de control de Campaign en Adobe Campaign v8.

## Agosto de 2021 {#august-2021}

**Compatibilidad con Campaign v8**

El Panel de control de Campaign ya está disponible para Adobe Campaign v8, excepto el **Subdominio** y **Certificado** funciones de administración, que aún no son compatibles. Obtenga más información en la [documentación de Campaign v8](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html){target=&quot;_blank&quot;}

## Octubre de 2020 {#october-2020}

**Configuración del subdominio mediante CNAME**

El Panel de control de Campaign ahora le permite configurar un subdominio para trabajar con Adobe mediante CNAME directamente desde la interfaz. [Más información](subdomains-certificates/using/setting-up-new-subdomain.md)

**Mejoras en la supervisión de bases de datos**

La supervisión de la base de datos se ha mejorado con métricas adicionales que le permiten obtener información detallada sobre los recursos que consumen espacio en la base de datos. [Más información](performance-monitoring/using/database-monitoring.md)

## Junio de 2020 {#june-2020}

**Auditoría de entrega de subdominios**

Después de delegar un nuevo subdominio, el Panel de control le permite realizar un seguimiento de la auditoría realizada por el equipo de entrega. [Más información](subdomains-certificates/using/setting-up-new-subdomain.md)

**Administración de claves GPG**

El Panel de control ya le permite generar un par de claves GPG para que pueda descifrar fácilmente los datos que llegan a Campaign desde el exterior. Además, hemos agregado una función para que pueda instalar una clave GPG pública con el fin de cifrar los datos que salen de Campaign. [Más información](instances-settings/using/gpg-keys-management.md)

**Supervisión de perfiles activos**

El Panel de control de Campaign ahora le permite monitorizar el número de perfiles activos que utilizan las instancias y que se contabilizan con fines de facturación. [Más información](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>La monitorización de perfiles activos desde el Panel de control de Campaign está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

## Mayo de 2020 {#may-2020}

**Administración de certificados para subdominios CNAME**

El Panel de control de Campaign ahora le permite renovar los certificados SSL de sus subdominios configurados con el método CNAME. [Más información](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Abril de 2020 {#april-2020}

**Administración de registros TXT de Google**

Añada el registro de verificación del sitio TXT de Google a todos los subdominios utilizados para enviar correos electrónicos a las direcciones de Gmail a través del Panel de control de Campaign. [Más información](subdomains-certificates/using/managing-txt-records.md)

**Supervisión del espacio de la base de datos**

El Panel de control de Campaign está equipado con funcionalidades de supervisión de bases de datos, lo que le permite ver el uso del espacio de las bases de datos según demanda e historial. [Más información](performance-monitoring/using/database-monitoring.md)

**Alertas por correo electrónico**

El Panel de control de Campaign está equipado con funciones de alerta por correo electrónico en tiempo real que le permiten iniciar sesión en el Panel de control y registrarse para recibir alertas cuando el sistema está en riesgo de deterioro del rendimiento o se requiere una acción para garantizar un alto rendimiento en el futuro. [Más información](performance-monitoring/using/email-alerting.md)

## Enero de 2020 {#january-2020}

*22 de enero de 2020*

Hemos añadido nuevas funciones para que los usuarios administradores configuren subdominios y renueven los certificados SSL desde el Panel de control de Campaign.

Para obtener más información, consulte estas páginas:
* [Configuración de un nuevo subdominio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renovación del certificado SSL de un subdominio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Estas funciones estarán disponibles en la versión beta y sujetas a frecuentes actualizaciones y modificaciones sin previo aviso.

## Septiembre de 2019 {#september-2019}

*16 de septiembre de 2019*

Hemos agregado nuevas funcionalidades para que los usuarios administradores agreguen direcciones IP a la lista de permitidos para conectarse a instancias de Campaign Classic.
Además, los usuarios administradores ahora pueden ver la lista de instancias de Campaign Classic y los requisitos para las actualizaciones de versiones.

Para obtener más información, consulte la [documentación especializada](instances-settings/using/ip-allow-listing-instance-access.md).

## Agosto de 2019 {#august-2019}

Hemos añadido nuevas funcionalidades para que los administradores reciban notificaciones antes de que expiren los certificados SSL para sus dominios. Para obtener más información, consulte la [documentación detallada](subdomains-certificates/using/monitoring-ssl-certificates.md).

Además, los administradores ahora pueden borrar las claves SSH que se añadieron para acceder a los servidores SFTP.

## Julio de 2019 {#july-2019}

Se han añadido nuevas funciones para que los administradores puedan tener un mayor control de la configuración de las instancias de Campaign Classic. Las nuevas funcionalidades del Panel de control incluyen la posibilidad de añadir las URL a las que se conecta Adobe Campaign para las transferencias de datos o archivos.

Para obtener más información, consulte la [documentación detallada](instances-settings/using/url-permissions.md).
