---
product: campaign
solution: Campaign
title: Administración de registros TXT
description: Obtenga información sobre cómo administrar registros TXT para la verificación de la propiedad del dominio.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 118fa4d722980e507d15647453e96a8b6189f837
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 25%

---


# Introducción a los registros TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Administración de registros TXT"
>abstract="Los registros TXT son un tipo de registros DNS que se utilizan para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas. El Panel de control de Campaign le permite agregar tres tipos de registros a sus subdominios: verificación del sitio de Google, registros DMARC y registros BIMI."

## Acerca de los registros TXT {#about}

Los registros TXT son un tipo de registros DNS que se utilizan para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas. El Panel de control de Campaign permite agregar tres tipos de registros a los subdominios:

* **Registros TXT de Google** le permiten certificar que es el propietario de su dominio, lo que garantiza altas tasas de mensajes en bandeja de entrada y bajas tasas de spam para sus correos electrónicos. [Aprenda a añadir registros TXT de Google](managing-txt-records.md)
* **Registros DMARC** proporciona una forma de autenticar el dominio del remitente y evitar el uso no autorizado del dominio con fines malintencionados. [Aprenda a añadir registros DMARC](dmarc.md)
* **Registros BIMI** le permite mostrar un logotipo aprobado junto a los correos electrónicos en las bandejas de entrada de los proveedores de buzones de correo para mejorar el reconocimiento y la confianza de la marca. [Aprenda a añadir registros BIMI](bimi.md)

## Supervisión de los registros de los subdominios {#monitor}

Puede monitorizar todos los registros TXT que se han agregado para cada subdominio accediendo a los detalles de los subdominios.

En esta pantalla, se muestran todos los registros de tipo TXT del subdominio seleccionado, con información en la columna &quot;Valor&quot; de su configuración. Para eliminar un registro TXT, DMARC o BIMI de Google, haga clic en el botón de los tres puntos y seleccione Eliminar. También puede editar registros DMARC y BIMI si es necesario.

![](assets/txt-records.png)
