---
title: Notas de la versión de 2023
description: Esta página enumera todas las versiones de Panel de control de Campaign de 2023.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 100%

---

# Notas de la versión de 2023 {#rn-2023}

## Septiembre de 2023 {#september-2023}

<table>
<thead>
<tr>
<th><strong>Gestión de registros DMARC y BIMI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>Ahora puede añadir registros DMARC y BIMI directamente desde el Panel de control:

<ul><li>Los <strong>registros DMARC</strong> proporcionan una forma de autenticar el dominio del remitente y evitar el uso no autorizado del dominio con fines malintencionados. <a href="../subdomains-certificates/using/dmarc.md">Obtenga información sobre cómo añadir registros DMARC</a></li>
<li>Los <strong>registros BIMI</strong> le permiten mostrar un logotipo aprobado junto a los correos electrónicos en las bandejas de entrada de los proveedores de buzones de correo para mejorar el reconocimiento y la confianza de la marca. <a href="../subdomains-certificates/using/bimi.md">Obtenga información sobre cómo añadir registros BIMI</a></li></ul>
</td>
</tr>
</tbody>
</table>

## Junio de 2023 {#june-2023}

* Ahora puede delegar los certificados SSL de subdominios ya delegados a Adobe directamente desde la lista de subdominios. [Más información](../subdomains-certificates/using/delegate-ssl.md)

* El remitente de los correos electrónicos de alerta ha cambiado a `"alert@notifications.campaign.adobe.com"`.

## Mejoras de mayo de 2023 {#may-2023}

**Delegación de certificados SSL de los subdominios a Adobe**

Ahora puede administrar por Adobe los certificados SSL de los subdominios. Si utiliza CNAME para configurar el subdominio, los registros de certificados se generarán y se proporcionarán automáticamente para generar un certificado en la solución de alojamiento de dominios.

Tenga en cuenta que esta capacidad solo está disponible al configurar un nuevo subdominio. No puede delegar certificados para los subdominios delegados existentes. [Más información](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>SSL administrado por Adobe es una funcionalidad gratuita a disposición de los usuarios sin cargo alguno.

## Marzo de 2023 {#march-2023}

**Eliminación de la delegación de subdominios para CNAME**

Ahora puede quitar la delegación de subdominios que se han configurado mediante CNAME. [Más información](../subdomains-certificates/using/remove-delegated-subdomains.md)

## Febrero de 2023 {#february-2023}

**Eliminación de la delegación para subdominios delegados en Adobe**

Ahora puede quitar la delegación de un subdominio delegado de forma completa en Adobe. [Más información](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>La eliminación de la delegación no está disponible actualmente para los subdominios que se han configurado con CNAME.

**Calendario de servicios**

El calendario de servicios ahora proporciona una vista de calendario para seguir los eventos importantes que se producen en las instancias. Además, se ha añadido información sobre las notificaciones enviadas a los usuarios suscritos a las alertas del Panel de control de Campaign. [Más información](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## Enero de 2023 {#january-2023}

**Nueva capacidad del modelo de alojamiento híbrido**

Los clientes con modelo de alojamiento híbrido pueden ahora añadir direcciones IP a la lista de permitidos para acceder a las instancias de MID. [Más información](../instances-settings/using/ip-allow-listing-instance-access.md)

**Mejora de la solicitud de firma de certificado (CSR)**

El campo Ciudad/Localidad es ahora opcional durante la generación de la solicitud de firma de certificado.
