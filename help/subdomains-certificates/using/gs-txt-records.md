---
product: campaign
solution: Campaign
title: Administración de registros TXT
description: Obtenga información sobre cómo administrar registros TXT para la verificación de la propiedad del dominio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 013d6674-0988-4553-a23e-b3ec23da5323
TQID: 'https://experienceleague.adobe.com/G8eirPm9hY0XRZTtMOBpmdwxuo3-Uvdo9LQjiSiElPU'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 100%
---
# Introducción a los registros TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Administración de registros TXT"
>abstract="Los registros TXT son un tipo de registros DNS que se utilizan para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas. El Panel de control permite añadir tres tipos de registros a sus subdominios: verificación del sitio de Google, registros DMARC y registros BIMI."

## Acerca de los registros TXT {#about}

Los registros TXT son un tipo de registros DNS que se utilizan para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas. El Panel de control le permite añadir tres tipos de registros a los subdominios:

* Los **registros TXT de Google** le permiten certificar que es el propietario de su dominio, lo que garantiza altas tasas de mensajes en la bandeja de entrada y bajas tasas de correo electrónico no deseado para sus correos electrónicos. [Obtenga información sobre cómo añadir registros TXT de Google](managing-txt-records.md)
* Los **registros DMARC** proporcionan una forma de autenticar el dominio del remitente y evitar el uso no autorizado del dominio con fines malintencionados. [Obtenga información sobre cómo añadir registros DMARC](dmarc.md)
* Los **registros BIMI** le permiten mostrar un logotipo aprobado junto a los correos electrónicos en las bandejas de entrada de los proveedores de buzones de correo para mejorar el reconocimiento y la confianza de la marca. [Obtenga información sobre cómo añadir registros BIMI](bimi.md)

## Monitorización de los registros de los subdominios {#monitor}

Puede monitorizar todos los registros TXT que se han añadido para cada subdominio accediendo a los detalles de los subdominios.

En esta pantalla, se muestran todos los registros de tipo TXT del subdominio seleccionado, con información en la columna &quot;Valor&quot; de su configuración. Para eliminar un registro TXT, DMARC o BIMI de Google, haga clic en el botón de los tres puntos y seleccione Eliminar. También puede editar registros DMARC y BIMI si es necesario.

![](assets/txt-records.png)
