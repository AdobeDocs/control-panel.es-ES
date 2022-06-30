---
title: Última versión
description: Esta página enumera todas las nuevas funciones y mejoras de Panel de control de Campaign
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: daa52035ea5db89552b56afc4ab5690610b6e846
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 55%

---

# Última versión {#control-panel-releases}

Esta página enumera todas las nuevas funciones y mejoras de Panel de control de Campaign.

## Junio de 2022 {#june-2022}

### Novedades?

<table>
<thead>
<tr>
<th><strong>Los 10 archivos principales que consumen espacio en los servidores SFTP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede identificar los 10 archivos principales que consumen más espacio en un servidor SFTP. <a href="../sftp/using/sftp-storage-management.md">Más información</a></p>
<img src="../assets/do-not-localize/sftp.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avisos del calendario de servicios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El calendario de servicios ahora le permite configurar recordatorios para recibir notificaciones por correo electrónico antes de que se produzca un evento en las instancias. <a href="../service-events/service-events.md">Más información</a></p>
<img src="../assets/do-not-localize/reminders.gif"/>
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
<p>Se han realizado varias mejoras en el proceso de generación de CSR. <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">Más información</a></p><ul><li>Al generar una CSR, ahora puede seleccionar uno de los subdominios incluidos como Nombre común.</li><li>Ahora puede copiar el resumen de la CSR antes de generar la CSR.</li><li>Una vez que se ha generado una CSR, puede descargarla de nuevo desde los registros de trabajos. Esta capacidad no se aplica a los certificados generados antes de esta versión.</li></ul><p>
<img src="../assets/do-not-localize/CSR.gif"/>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Configuración de instancias**

* El número máximo de claves GPG en Panel de control de Campaign se ha aumentado a 60 claves. [Más información](../instances-settings/using/gpg-keys-management.md)

## Mayo de 2022 {#may-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilidad del Panel de control de Campaign para el modelo de alojamiento híbrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Panel de control de Campaign ya está disponible para los clientes con un modelo de alojamiento híbrido. Estos clientes pueden aprovechar las funciones del Panel de control de Campaign al proporcionar su URL de instancia MID/RT configurada en su instancia de marketing en Panel de control de Campaign.</p><p>Para obtener más información, consulte la <a href="../instances-settings/using/external-accounts.md">documentación detallada.</a></p>
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
<p>Se han mejorado las capacidades de supervisión de los resultados y las latencias:<ul><li>Ahora puede identificar los ID de los cinco envíos principales que contribuyen al rendimiento de su instancia.</li><li>Los clientes de las versiones 7 y 8 de Campaign Classic ahora pueden visualizar la latencia de un canal específico.</p></li><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/thoughputs-latencies.md">documentación detallada.</a></p>
</td>
</tr>
</tbody>
</table>


## Abril de 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Supervisión de contactos y eventos clave en las instancias</strong><br/></th>
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
<th><strong>Disponibilidad de monitorización de latencia y de rendimiento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La monitorización de latencia y de rendimiento ya está disponible para todos los clientes Campaign Standards y v8, y para los clientes de Campaign V7 con los números de compilación 9032, 9330, 9346 o 9349 que tienen implementaciones independientes (sin ninguna instancia media).</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/thoughputs-latencies.md">documentación detallada.</a></p>
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
<p>Ahora, el Panel de control de Campaign le permite supervisar las consultas que se han estado ejecutando durante más tiempo en las instancias.</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/database-active-queries.md">documentación detallada</a>.</p>
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
<p>Ahora puede monitorizar cómo el rendimiento y la latencia de la entrega son tendencias a lo largo del tiempo en las instancias.</p><p>Para obtener más información, consulte la <a href="../performance-monitoring/using/thoughputs-latencies.md">documentación detallada</a>.</p>
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
<p>Ahora, las operaciones de certificados SSL se pueden realizar en un subdominio recién configurado, incluso si la auditoría de la entrega sigue en curso.</p><p>Para obtener más información, consulte la <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>
