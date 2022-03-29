---
product: campaign
solution: Campaign
title: Versiones del Panel de control
description: Esta página enumera todas las nuevas funciones y mejoras de Panel de control de Campaign
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 35b849725711bfee9852cf8f503bc599f6d8eaff
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 63%

---

# Versiones del Panel de control {#control-panel-releases}

Esta página enumera todas las nuevas funciones y mejoras de Panel de control de Campaign.

>[!NOTE]
>
>Solo los usuarios administradores pueden acceder al Panel de control de Campaign. Obtenga más información sobre los permisos en [esta sección](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=es#discover-control-panel).
>
>Para Campaign v7, la instancia debe estar alojada en Amazon Web Service (AWS) y actualizarse a la versión más reciente [Compilación estable de Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=es#rn-statuses) (o para construir 9032 o superior). Aprenda a comprobar su versión en [esta sección](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=es#getting-your-campaign-version). Para comprobar si la instancia está alojada en AWS, siga los pasos detallados en [esta página](faq.md#hosted-aws).

## Marzo de 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilidad de monitorización de latencia y de rendimiento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La monitorización de latencia y de rendimiento ya está disponible para todos los clientes Campaign Standards y v8, y para los clientes de Campaign V7 con los números de compilación 9032, 9330, 9346 o 9349 que tienen implementaciones independientes (sin ninguna instancia media).</p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/thoughputs-latencies.md">documentación detallada.</a></p>
</td>
</tr>
</tbody>
</table>

## Febrero de 2022 {#february-2022}

<table>
<thead>
<tr>
<th><strong>Monitorización de parámetros de flujo de trabajo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede monitorizar los parámetros de flujo de trabajo que puedan requerir una atención específica para evitar problemas en las instancias. </p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/workflow-monitoring.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Enero de 2022 {#january-2022}

<table>
<thead>
<tr>
<th><strong>Monitorización de consultas activas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, el Panel de control de Campaign le permite supervisar las consultas que se han estado ejecutando durante más tiempo en las instancias.</p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/database-active-queries.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitorización de rendimiento y latencia </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede monitorizar cómo el rendimiento y la latencia de la entrega son tendencias a lo largo del tiempo en las instancias.</p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/thoughputs-latencies.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Operaciones de certificados SSL en nuevos subdominios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, las operaciones de certificados SSL se pueden realizar en un subdominio recién configurado, incluso si la auditoría de la entrega sigue en curso.</p><p>Para obtener más información, consulte la <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Octubre de 2021 {#october-2021}

<table>
<thead>
<tr>
<th><strong>Intervalo de IP y periodo de validez de clave pública</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora es posible establecer una duración para la disponibilidad de intervalos de IP y claves públicas. </p><p>Para obtener más información, consulte <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">Adición de rangos de IP a la lista de permitidos</a> y <a href="sftp/using/key-management.md#installing-ssh-key">Administración de claves</a> secciones.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rango de IP y edición de clave pública</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede editar el <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">Intervalos de IP</a> y <a href="sftp/using/key-management.md#editing-public-keys">claves públicas</a> que cree. Tenga en cuenta que esta función no está disponible para los elementos creados antes de la versión de Panel de control de Campaign actual.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alerta sobre el intervalo IP SFTP y la caducidad de la clave pública</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funcionalidad de alertas por correo electrónico ahora incluye alertas sobre la IP SFTP que permiten enumerar la caducidad y la caducidad de la clave pública SFTP.</p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/email-alerting.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad total con Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La variable <strong>Subdominio</strong> y <strong>Certificado</strong> las funciones de administración ahora son compatibles con Panel de control de Campaign en Adobe Campaign v8.</a>.</p>
</td>
</tr>
</tbody>
</table>

## Agosto de 2021 {#august-2021}

<table>
<thead>
<tr>
<th><strong>Compatibilidad con Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control de Campaign ya está disponible para Adobe Campaign v8, excepto el <strong>Subdominio</strong> y <strong>Certificado</strong> funciones de administración, que aún no son compatibles.</p><p>Para obtener más información, consulte <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html" target="blank">Documentación de Campaign v8</a>.</p>
</td>
</tr>
</tbody>
</table>

## Octubre de 2020 {#october-2020}

<table>
<thead>
<tr>
<th><strong>Configuración del subdominio mediante CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control de Campaign ahora le permite configurar un subdominio para trabajar con Adobe mediante CNAME directamente desde la interfaz.</p><p>Para obtener más información, consulte la <a href="subdomains-certificates/using/setting-up-new-subdomain.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mejoras en la supervisión de bases de datos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La supervisión de la base de datos se ha mejorado con métricas adicionales que le permiten obtener información detallada sobre los recursos que consumen espacio en la base de datos.</p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/database-monitoring.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Junio de 2020 {#june-2020}

<table>
<thead>
<tr>
<th><strong>Auditoría de entrega de subdominios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Después de delegar un nuevo subdominio, el Panel de control le permite realizar un seguimiento de la auditoría realizada por el equipo de entrega.</p><p>Para obtener más información, consulte la <a href="subdomains-certificates/using/setting-up-new-subdomain.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Administración de claves GPG</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control ya le permite generar un par de claves GPG para que pueda descifrar fácilmente los datos que llegan a Campaign desde el exterior. Además, hemos agregado una función para que pueda instalar una clave GPG pública con el fin de cifrar los datos que salen de Campaign.</p><p>Para obtener más información, consulte la <a href="instances-settings/using/gpg-keys-management.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitorización de perfiles activos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control de Campaign ahora le permite monitorizar el número de perfiles activos que utilizan las instancias y que se contabilizan con fines de facturación.</p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/active-profiles-monitoring.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>La monitorización de perfiles activos desde el Panel de control de Campaign está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

## Mayo de 2020 {#may-2020}

<table>
<thead>
<tr>
<th><strong>Administración de certificados para subdominios CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control de Campaign ahora le permite renovar los certificados SSL de sus subdominios configurados con el método CNAME.</p><p>Para obtener más información, consulte la <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Abril de 2020 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Administración de registros TXT de Google</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Añada el registro de verificación del sitio TXT de Google a todos los subdominios utilizados para enviar correos electrónicos a las direcciones de Gmail a través del Panel de control de Campaign.</p><p>Para obtener más información, consulte la <a href="subdomains-certificates/using/managing-txt-records.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supervisión del espacio de la base de datos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control de Campaign está equipado con funcionalidades de supervisión de bases de datos, lo que le permite ver el uso del espacio de las bases de datos según demanda e historial.</p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/database-monitoring.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alertas por correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control de Campaign está equipado con funciones de alerta por correo electrónico en tiempo real que le permiten iniciar sesión en el Panel de control y registrarse para recibir alertas cuando el sistema está en riesgo de deterioro del rendimiento o se requiere una acción para garantizar un alto rendimiento en el futuro.</p><p>Para obtener más información, consulte la <a href="performance-monitoring/using/email-alerting.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Enero de 2020 {#january-2020}

Hemos añadido nuevas funciones para que los usuarios administradores configuren subdominios y renueven los certificados SSL desde el Panel de control de Campaign.

Para obtener más información, consulte estas páginas:
* [ Configuración de un nuevo subdominio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renovación del certificado SSL de un subdominio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Estas funciones estarán disponibles en la versión beta y sujetas a frecuentes actualizaciones y modificaciones sin previo aviso.

## Septiembre de 2019 {#september-2019}

Hemos añadido nuevas funciones para que los usuarios administradores agreguen direcciones IP a la lista de permitidos para conectarse a instancias de Campaign v7/v8.
Además, los usuarios administradores ahora pueden ver la lista de instancias de Campaign v7/v8 y los requisitos para las actualizaciones de la compilación.

Para obtener más información, consulte la [documentación especializada](instances-settings/using/ip-allow-listing-instance-access.md).

## Agosto de 2019 {#august-2019}

Hemos añadido nuevas funcionalidades para que los administradores reciban notificaciones antes de que expiren los certificados SSL para sus dominios. Para obtener más información, consulte la [documentación detallada](subdomains-certificates/using/monitoring-ssl-certificates.md).

Además, los administradores ahora pueden borrar las claves SSH que se añadieron para acceder a los servidores SFTP.

## Julio de 2019 {#july-2019}

Se han añadido nuevas funciones para que los administradores puedan tener bueno control de la configuración de las instancias de Campaign v7/v8. Las nuevas funcionalidades del Panel de control incluyen la posibilidad de añadir las URL a las que se conecta Adobe Campaign para las transferencias de datos o archivos.

Para obtener más información, consulte la [documentación detallada](instances-settings/using/url-permissions.md).
