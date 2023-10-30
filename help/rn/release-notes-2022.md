---
title: Notas de la versión de 2022
description: Esta página enumera todas las versiones de Panel de control de 2022.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9fb18bb6-c4e4-48aa-849c-d9129add5266
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 100%

---

# Notas de la versión de 2022 {#rn-2022}

## Octubre de 2022 {#october-2022}

Las alertas por correo electrónico ahora le avisan cuando uno de sus certificados SSL caducará en 30 días o menos. [Más información](../performance-monitoring/using/email-alerting.md)

## Septiembre de 2022 {#september-2022}

Los clientes con un modelo de alojamiento híbrido ya pueden configurar nuevos subdominios. [Más información](../subdomains-certificates/using/setting-up-new-subdomain.md)

## Agosto de 2022 {#august-2022}

* Los clientes con un modelo de alojamiento híbrido ya pueden verificar sus subdominios. [Más información](../subdomains-certificates/using/monitoring-subdomains.md)
* El campo Unidad organizativa (OU) ya es opcional en Solicitud de generación de certificados (CSR). [Más información](../subdomains-certificates/using/renewing-subdomain-certificate.md)

## Julio de 2022 {#july-2022}

<table>
<thead>
<tr>
<th><strong>Instalación de certificados de subdominios para el modelo de alojamiento híbrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>Los clientes con modelo de alojamiento híbrido ahora pueden renovar los certificados SSL de sus subdominios desde el Panel de control.</p><p>Para obtener más información, consulte la <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentación detallada.</a></p>
</td>
</tr>
</tbody>
</table>

## Junio de 2022 {#june-2022}

### Novedades

<table>
<thead>
<tr>
<th><strong>Los 10 archivos que más espacio consumen en los servidores SFTP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede identificar los 10 archivos que más espacio consumen en un servidor SFTP. <a href="../sftp/using/sftp-storage-management.md">Más información</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Recordatorios del calendario de servicios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El calendario de servicios ahora le permite configurar recordatorios para recibir notificaciones por correo electrónico antes de que se produzca un evento en las instancias. <a href="../service-events/service-events.md">Más información</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mejoras en la generación de CSR de los subdominios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se han llevado a cabo varias mejoras en el proceso de generación de CSR. <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">Más información</a></p><ul><li>Al generar una CSR, ahora puede seleccionar uno de los subdominios incluidos como Nombre común.</li><li>Ahora puede copiar el resumen de la CSR antes de generarla.</li><li>Una vez que se ha generado una CSR, puede descargarla de nuevo desde los registros de trabajos. Esta función no se aplica a los certificados generados antes de esta versión.</li></ul><p>

</td>
</tr>
</tbody>
</table>

### Mejoras

**Configuración de instancias**

* El número máximo de claves GPG en el Panel de control se ha aumentado a 60 claves. [Más información](../instances-settings/using/gpg-keys-management.md)

## Mayo de 2022 {#may-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilidad del Panel de control para modelos de alojamiento híbridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control ya está disponible para los clientes con un modelo de alojamiento híbrido. Estos clientes pueden aprovechar las funciones del Panel de control al proporcionar su URL de instancia MID/RT configurada en su instancia de marketing en el Panel de control.</p><p>Para obtener más información, consulte la <a href="../instances-settings/using/external-accounts.md">documentación detallada.</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actualizaciones de supervisión de las latencias y los procesos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se han mejorado las funciones de supervisión de los resultados y las latencias:<ul><li>Ahora puede identificar los ID de los cinco envíos principales que contribuyen al rendimiento de su instancia.</li><li>Los clientes de las versiones 7 y 8 de Campaign Classic ahora pueden visualizar la latencia de un canal específico.</p></li><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/throughputs-latencies.md">documentación detallada.</a></p>
</td>
</tr>
</tbody>
</table>


## Abril de 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Monitorización de contactos y eventos clave en las instancias</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede monitorizar las versiones anteriores y futuras, así como las revisiones de servicio que se producen en las instancias, y acceder a una lista de contactos clave en Adobe para cualquier solicitud o problema.</p><p>Para obtener más información, consulte la <a href="../service-events/service-events.md">documentación detallada.</a></p>
</td>
</tr>
</tbody>
</table>

## Marzo de 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilidad de monitorización de rendimiento y latencia</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La monitorización de rendimiento y latencia ahora está disponible para todos los clientes de Campaign Standard y v8, así como para los clientes de Campaign v7 con los números de versión 9032, 9330, 9346 o 9349 que tengan implementaciones independientes (sin ninguna instancia intermediaria).</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/throughputs-latencies.md">documentación detallada.</a></p>
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
<p>Ahora puede monitorizar los parámetros de flujo de trabajo que puedan requerir una atención específica para evitar problemas en las instancias. </p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/workflow-monitoring.md">documentación detallada</a>.</p>
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
<p>Ahora, el Panel de control le permite supervisar las consultas que se han estado ejecutando durante más tiempo en las instancias.</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/database-active-queries.md">documentación detallada</a>.</p>
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
<p>Ahora puede monitorizar cómo el rendimiento y la latencia de la entrega son tendencias a lo largo del tiempo en las instancias.</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/throughputs-latencies.md">documentación detallada</a>.</p>
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
<p>Ahora, las operaciones de certificados SSL se pueden ejecutar en un subdominio recién configurado, incluso si la auditoría de capacidad de entrega sigue en curso.</p><p>Para obtener más información, consulte la <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>
