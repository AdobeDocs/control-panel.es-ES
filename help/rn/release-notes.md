---
title: Última versión
description: Esta página enumera todas las nuevas funciones y mejoras de Panel de control
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a8e2fb9789e9755aa6b9c55019816d7e748606ec
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 26%

---

# Última versión {#control-panel-releases}

Esta página enumera las nuevas funciones y mejoras de Panel de control.

## Octubre de 2023 {#october-2023}

**Interfaz de usuario**

* El Panel de control de Campaign ya está disponible en otros idiomas. [Más información](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Supervisión de perfiles activos**

* Ahora puede monitorizar el número de perfiles activos a los que tiene derecho para su organización y el recuento total de perfiles utilizados en su organización en todas las instancias, si utiliza varias instancias. [Más información](../performance-monitoring/using/active-profiles-monitoring.md)

**Registros DMARC**

* Ahora, varias direcciones de correo electrónico pueden recibir correos electrónicos de informes acumulados e informes de errores. [Más información](../subdomains-certificates/using/dmarc.md)
* Se han realizado cambios si existen registros DMARC y BIMI para un subdominio:

   * Los registros DMARC no se pueden eliminar. Si desea eliminar uno, primero debe eliminar el registro BIMI.
   * Los registros DMARC se pueden editar, pero no se permite reducir la categoría de la directiva a &quot;Ninguno&quot; y su valor porcentual debe ser 100.

