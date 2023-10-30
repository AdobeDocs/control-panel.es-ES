---
title: Notas de la versión 2020
description: Esta página enumera todas las versiones de Panel de control de 2020.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 70357a40-3dc1-486d-bba2-f500b3175d62
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '429'
ht-degree: 100%

---

# Notas de la versión 2020 {#rn-2020}

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
<p>El Panel de control ahora le permite configurar un subdominio para trabajar con Adobe mediante CNAME directamente desde la interfaz.</p><p>Para obtener más información, consulte la <a href="../subdomains-certificates/using/setting-up-new-subdomain.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mejoras en la monitorización de bases de datos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La monitorización de bases de datos se ha mejorado con métricas adicionales, lo que le permite obtener información detallada sobre los recursos que consumen espacio en la base de datos.</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/database-monitoring.md">documentación detallada</a>.</p>
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
<p>Después de delegar un nuevo subdominio, el Panel de control le permite realizar un seguimiento de la auditoría realizada por el equipo de entrega.</p><p>Para obtener más información, consulte la <a href="../subdomains-certificates/using/setting-up-new-subdomain.md">documentación detallada</a>.</p>
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
<p>El Panel de control ya le permite generar un par de claves GPG para que pueda descifrar fácilmente los datos que llegan a Campaign desde el exterior. Además, hemos agregado una función para que pueda instalar una clave GPG pública con el fin de cifrar los datos que salen de Campaign.</p><p>Para obtener más información, consulte la <a href="../instances-settings/using/gpg-keys-management.md">documentación detallada</a>.</p>
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
<p>El Panel de control ahora le permite monitorizar el número de perfiles activos que utilizan las instancias y que se contabilizan con fines de facturación.</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/active-profiles-monitoring.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>La monitorización de perfiles activos desde el Panel de control está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

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
<p>El Panel de control ahora le permite renovar los certificados SSL de sus subdominios configurados con el método CNAME.</p><p>Para obtener más información, consulte la <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentación detallada</a>.</p>
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
<p>Añada el registro de verificación del sitio TXT de Google a todos los subdominios utilizados para enviar correos electrónicos a las direcciones de Gmail a través del Panel de control de Campaign.</p><p>Para obtener más información, consulte la <a href="../subdomains-certificates/using/managing-txt-records.md">documentación detallada</a>.</p>
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
<p>El Panel de control de Campaign está equipado con funcionalidades de supervisión de bases de datos, lo que le permite ver el uso del espacio de las bases de datos según demanda e historial.</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/database-monitoring.md">documentación detallada</a>.</p>
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
<p>El Panel de control de Campaign está equipado con funciones de alerta por correo electrónico en tiempo real que le permiten iniciar sesión en el Panel de control y registrarse para recibir alertas cuando el sistema está en riesgo de deterioro del rendimiento o se requiere una acción para garantizar un alto rendimiento en el futuro.</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/email-alerting.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Enero de 2020 {#january-2020}

Hemos añadido nuevas funciones para que los usuarios administradores configuren subdominios y renueven los certificados SSL desde el Panel de control.

Para obtener más información, consulte estas páginas:
* [ Configuración de un nuevo subdominio](../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renovación del certificado SSL de un subdominio](../subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Estas funciones estarán disponibles en la versión beta y sujetas a frecuentes actualizaciones y modificaciones sin previo aviso.
