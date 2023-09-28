---
product: campaign
solution: Campaign
title: Añadir registros DMARC
description: Obtenga información sobre cómo agregar un registro DMARC para un subdominio.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: fc026f157346253fc79bde4ce624e7efa3373af2
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---


# Añadir registros DMARC {#dmarc}

## Acerca de los registros DMARC {#about}

Autenticación de mensajes, creación de informes y conformidad basados en dominio (DMARC) es un estándar de protocolo de autenticación de correo electrónico que ayuda a las organizaciones a proteger sus dominios de correo electrónico de ataques de suplantación de identidad y suplantación de identidad. Permite decidir cómo debe gestionar un proveedor de buzones los correos electrónicos que no superan las comprobaciones SPF y DKIM, lo que proporciona una forma de autenticar el dominio del remitente y evitar el uso no autorizado del dominio con fines malintencionados.

## Limitaciones y requisitos previos {#limitations}

* Los registros SPF y DKIM son requisitos previos para crear un registro DMARC.
* Los registros DMARC solo se pueden agregar para subdominios que utilizan delegación de subdominios completa. [Más información sobre los métodos de configuración de subdominios](subdomains-branding.md#subdomain-delegation-methods)

## Añadir un registro DMARC para un subdominio {#add}

Para añadir un registro DMARC para un subdominio, siga estos pasos:

1. En la lista de subdominios, haga clic en el botón de puntos suspensivos situado junto al subdominio deseado y seleccione **[!UICONTROL Subdomain details]**.

1. Haga clic en **[!UICONTROL Add TXT record]** y luego elija **[!UICONTROL DMARC]** desde el **[!UICONTROL Record Type]** lista desplegable.

   ![](assets/dmarc-add.png)

1. Elija la **[!UICONTROL Policy Type]** que el servidor de destinatario debe seguir cuando falla uno de los correos electrónicos. Los tipos de directivas disponibles son:

   * Ninguno,
   * Cuarentena (ubicación de carpeta de correo no deseado),
   * Rechazar (bloquear el correo electrónico).

   Si el subdominio acaba de configurarse, se recomienda configurar este valor en &quot;Ninguno&quot; hasta que el subdominio esté completamente configurado y los correos electrónicos se envíen correctamente. Una vez que todo esté configurado correctamente, puede cambiar el Tipo de directiva a &quot;Cuarentena&quot; o &quot;Rechazar&quot;.

   >[!NOTE]
   >
   > La creación de registros BIMI no está disponible con un tipo de directiva de registro DMARC establecido en &quot;Ninguno&quot;.

1. Rellene las direcciones de correo electrónico que deben recibir los informes DMARC. Cuando uno de los correos electrónicos falla, los informes DMARC se envían automáticamente a la dirección de correo electrónico que elija:

   * Los informes DMARC agregados proporcionan información de alto nivel como, por ejemplo, el número de correos electrónicos con errores durante un periodo determinado.
   * Los informes de errores de DMARC forenses proporcionan información detallada como, por ejemplo, la dirección IP desde la que se originan los mensajes de correo electrónico erróneos.

1. De forma predeterminada, la política DMARC seleccionada se aplica a todos los correos electrónicos. Puede cambiar este parámetro para que se aplique únicamente a un porcentaje específico de correos electrónicos.

   Cuando implemente gradualmente DMARC, es posible que comience con un pequeño porcentaje de los mensajes. A medida que más mensajes de su dominio pasen la autenticación con servidores de recepción, actualice el registro con un porcentaje mayor, hasta que alcance el 100 por ciento.

   >[!NOTE]
   >
   >Si su dominio utiliza BIMI, su política DMARC debe tener un valor porcentual del 100%. BIMI no admite directivas DMARC con este valor establecido en menos del 100%.

   ![](assets/dmarc-add2.png)

1. Los informes DMARC se envían cada 24 horas. Puede cambiar la frecuencia de envío de los informes en la **[!UICONTROL Reporting Interval]** field. El intervalo mínimo autorizado es de 1 hora, mientras que el valor máximo autorizado es de 2190 horas (es decir, 3 meses).

1. En el **SPF** y **[!UICONTROL DKIM Identifier Alignment]** , especifique lo estrictos que deben ser los servidores de destinatarios al comprobar las autenticaciones SPF y DKIM de un correo electrónico.

   * **[!UICONTROL Relaxed]** mode: el servidor acepta la autenticación incluso si el correo electrónico se envía desde un subdominio,
   * **[!UICONTROL Strict]** El modo de solo acepta autenticación cuando el dominio del remitente coincide exactamente con un dominio SPF y DKIM.

   Digamos que estamos trabajando con el `http://www.luma.com` dominio. En el modo &quot;Relajado&quot;, los correos electrónicos procedentes del `marketing.luma.com` El servidor autorizará el subdominio, mientras que se rechazarán en el modo &quot;Estricto&quot;.

1. Clic **[!UICONTROL Add]** para confirmar la creación del registro DMARC.

Una vez procesada la creación del registro DMARC (aproximadamente 5 minutos), este se muestra en la pantalla de detalles de los subdominios. [Obtenga información sobre cómo supervisar registros TXT para los subdominios](gs-txt-records.md#monitor)