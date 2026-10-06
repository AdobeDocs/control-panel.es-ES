---
title: Último lanzamiento
description: Esta página enumera todas las nuevas funciones y mejoras de Panel de control
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
TQID: 'https://experienceleague.adobe.com/Q1kU0q1e-a-H0LvAyK-5yYhfrUpGco1hVHWUsz-syhY'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e5e477db-ebc7-4368-ab0f-4d8fc2aed405
    internal-label: Release notes
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 100%
---
# Último lanzamiento {#control-panel-releases}

Esta página enumera las nuevas funciones y mejoras de Panel de control.

## Octubre de 2023 {#october-2023}

**Interfaz de usuario**

* El Panel de control ya está disponible en otros idiomas. [Más información](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Monitorización de perfiles activos**

* Ahora puede monitorizar el número de perfiles activos a los que tiene derecho para su organización y el recuento total de perfiles utilizados en su organización en todas las instancias, si utiliza varias instancias. [Más información](../performance-monitoring/using/active-profiles-monitoring.md)

**Registros DMARC**

* Ahora, varias direcciones de correo electrónico pueden recibir correos electrónicos de informes acumulados e informes de errores. [Más información](../subdomains-certificates/using/dmarc.md)
* Se han realizado cambios si existen registros DMARC y BIMI para un subdominio:

  * Los registros DMARC no se pueden eliminar. Si desea eliminar uno, primero debe eliminar el registro BIMI.
  * Los registros DMARC se pueden editar, pero no se permite bajar la categoría de la directiva a &quot;Ninguno&quot; y su valor porcentual debe ser 100.

