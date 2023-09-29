---
product: campaign
solution: Campaign
title: Añadir registros BIMI
description: Aprenda a añadir un registro BIMI para un subdominio.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: dfb6f548c4d53df7eb807d9aa21065449927f945
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Añadir registros BIMI {#dmarc}

## Acerca de los registros BIMI {#about}

Indicadores de marca para la identificación de mensajes (BIMI) es un estándar del sector que permite que aparezca un logotipo aprobado junto al correo electrónico de un remitente en las bandejas de entrada de los proveedores de buzones de correo para mejorar el reconocimiento y la confianza de la marca. Ayuda a evitar la suplantación de identidad (phishing) y la suplantación de identidad (phishing) de correo electrónico mediante la verificación de la identidad del remitente con autenticación DMARC, lo que dificulta a los actores malintencionados la suplantación de marcas legítimas en los correos electrónicos. Encontrará información detallada sobre la implementación de BIMI en [Guía de prácticas recomendadas de entrega de Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)

![](assets/bimi-example.png){width="70%" align="center"}

## Limitaciones y requisitos previos {#limitations}

* Los registros SPF, DKIM y DMARC son requisitos previos para crear un registro BIMI.
* Los registros BIMI solo se pueden añadir para subdominios que utilicen delegación de subdominios completa. [Más información sobre los métodos de configuración de subdominios](subdomains-branding.md#subdomain-delegation-methods)
* Requisitos previos del registro DMARC:

   * El tipo de directiva de registro del subdominio debe establecerse en &quot;Cuarentena&quot; o &quot;Rechazar&quot;. La creación de registros BIMI no está disponible con un tipo de directiva DMARC establecido en &quot;Ninguno&quot;.
   * El porcentaje de correos electrónicos a los que se aplica la política DMARC debe ser del 100 %. BIMI no es compatible con las políticas DMARC con este porcentaje establecido en menos del 100%.

[Obtenga información sobre cómo configurar registros DMARC](dmarc.md)

## Añadir un registro BIMI para un subdominio {#add}

Para añadir un registro BIMI para un subdominio, siga estos pasos:

1. En la lista de subdominios, haga clic en el botón de puntos suspensivos situado junto al subdominio deseado y seleccione **[!UICONTROL Subdomain details]**.

1. Haga clic en **[!UICONTROL Add TXT record]** y luego elija **[!UICONTROL BIMI]** desde el **[!UICONTROL Record type]** lista desplegable.

   ![](assets/bimi-add.png)

1. En el **[!UICONTROL Company Logo URL]**, especifique la URL del archivo de SVG que contiene su logotipo.

1. Aunque **[!UICONTROL Certificate URL]** es opcional, es necesaria para algunos proveedores de buzones de correo como Gmail y Apple, que cubren el 80 % del mercado de buzones de correo. Por lo tanto, recomendamos obtener un Certificado de Marca Verificada (VMC) para aprovechar realmente BIMI.

   +++¿Cómo obtengo una VMC?

   Los pasos principales para obtener una MVC son los siguientes:

   1. Registre su logotipo de marca como una marca comercial con una oficina de propiedad intelectual reconocida por los emisores de VMC. Si tiene un equipo legal, le recomendamos que trabaje con ellos para obtener su logotipo de marca comercial o para verificar que ya esté registrado.

   1. Después de verificar que su logotipo es de marca comercial, póngase en contacto con DigiCert o con la autoridad de certificación (CA) de Entrust para solicitar un VMC.

   1. Cuando su VMC esté aprobada, recibirá un archivo de correo mejorado de privacidad (PEM) de certificado de entidad. Anexe cualquier otro certificado intermedio que obtenga de la CA a este archivo PEM. Cargue el archivo PEM (junto con los archivos adjuntos) en su servidor web público y tome nota de la URL del archivo PEM. Utilizará la dirección URL en su registro BIMI TXT.

   1. Una vez que el registro BIMI esté visible en la página de detalles del subdominio para un subdominio en particular, puede utilizar el Inspector BIMI disponible [aquí](https://bimigroup.org/bimi-generator/) para comprobar si el registro BIMI funciona correctamente.

   Encontrará información detallada sobre la implementación de BIMI en la [Documentación estándar BIMI](https://bimigroup.org/implementation-guide/)
+++

1. Clic **[!UICONTROL Add]** para confirmar la creación del registro BIMI.

Una vez procesada la creación del registro BIMI (aproximadamente 5 minutos), aparece en la pantalla de detalles de los subdominios. [Obtenga información sobre cómo supervisar registros TXT para los subdominios](gs-txt-records.md#monitor)
