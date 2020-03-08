---
title: Renovación del certificado SSL de un subdominio
description: Obtenga información sobre cómo renovar los certificados SSL de los subdominios
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# Renovación del certificado SSL de un subdominio {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id=&quot;cp_add_ssl_certificate&quot;
>title=&quot;Agregar certificado SSL&quot;
>abstract=&quot;Para agregar un certificado SSL, debe generar un CSR, adquirir el certificado SSL para los subdominios e instalar el paquete de certificados&quot;.
>adicional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generación de una solicitud de firma de certificado (CSR)&quot;
>adicional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate&quot; text=&quot;How to install a SSL certificate&quot;&quot;

>[!IMPORTANT]
>
>La delegación de subdominios del Panel de control está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

## Acerca de la renovación de certificados {#about-certificate-renewal-process}

El proceso de renovación de certificados SSL incluye 3 pasos:

1. **Generación de la solicitud de firma certificada (CSR) El Servicio de atención al cliente de** Adobe genera un CSR para usted. Deberá proporcionar la información necesaria para generar el CSR (como Nombre común, Nombre de organización y dirección, etc.).
1. **Compra del certificado** SSL Una vez generado el CSR, puede descargarlo y utilizarlo para adquirir el certificado SSL de la entidad emisora de certificados que apruebe su empresa.
1. **Instalación del certificado** SSL Una vez adquirido el certificado SSL, puede instalarlo en el subdominio deseado.

>[!NOTE]
>
>La renovación de certificados SSL a través del Panel de control está disponible sólo para subdominios **delegados** completamente.

## Generación de una solicitud de firma de certificado (CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id=&quot;cp_generate_csr&quot;
>title=&quot;Generate CSR&quot;
>abstract=&quot;La solicitud de firma de certificado debe generarse para la instancia y los subdominios que planea proteger antes de comprar un certificado.&quot;

>[!CONTEXTUALHELP]
>id=&quot;cp_select_subdomain&quot;
>title=&quot;Seleccione los subdominios para su CSR&quot;
>abstract=&quot;Puede optar por incluir todos o solo los subdominios específicos en la solicitud de firma de certificados. Solo los subdominios seleccionados se certificarán mediante el certificado SSL adquirido&quot;.
>adicional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generación de una solicitud de firma de certificado (CSR)&quot;
>extra-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;Acerca de la marca de subdominios&quot;

Para generar una solicitud de firma de certificado (CSR), siga estos pasos:

1. En la **[!UICONTROL Subdomains & Certificates]** tarjeta, seleccione la instancia que desee y haga clic en el **[!UICONTROL Manage Certificate]** botón.

   ![](assets/renewal1.png)

1. Seleccione **[!UICONTROL Generate a CSR]**, luego haga clic **[!UICONTROL Next]** para iniciar el asistente que lo guiará a través del proceso de generación de CSR.

   ![](assets/renewal2.png)

1. Se muestra un formulario con todos los detalles necesarios para generar su CSR.

   Asegúrese de completar la información solicitada de forma completa y precisa; de lo contrario, es posible que el certificado no se renueve (póngase en contacto con el equipo interno, los equipos de seguridad y TI si es necesario) y haga clic en **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**:: nombre oficial de la organización.
   * **[!UICONTROL Organization Unit]**:: unidad vinculada al subdominio (ejemplo: Marketing, TI).
   * **[!UICONTROL Instance]** (precargada): Dirección URL de la instancia de Campaign asociada al subdominio.
   ![](assets/renewal3.png)

1. Seleccione los subdominios que desea incluir en el CSR y, a continuación, haga clic en **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Los subdominios seleccionados se muestran en la lista. Para cada uno de ellos, seleccione los subdominios que desee incluir y haga clic en **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. Se muestra un resumen de los subdominios que se incluirán en el CSR. Haga clic en **[!UICONTROL Submit]** para confirmar la solicitud.

   ![](assets/renewal6.png)

1. El archivo .csr correspondiente a su selección se genera y descarga automáticamente. Ahora puede utilizarla para adquirir el certificado SSL de la entidad emisora de certificados que apruebe su empresa.

   >[!NOTE]
   >
   >Si el CSR no se guarda o descarga, se perderá y tendrá que volver a generarlo.

## Compra de un certificado con el CSR {#purchasing-certificate}

Después de obtener un CSR de solicitud de firma de certificado del Panel de control, compre un certificado SSL de una autoridad de certificación aprobada por su organización.

## Instalación del certificado SSL {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id=&quot;cp_install_ssl_certificate&quot;
>title=&quot;Install SSL Certificate&quot;
>abstract=&quot;Instale el certificado SSL que adquirió de la entidad emisora de certificados aprobada por su organización&quot;.
>extra-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;Acerca de la marca de subdominios&quot;

Una vez adquirido un certificado SSL, puede instalarlo en su instancia. Antes de continuar, asegúrese de conocer los requisitos previos siguientes:

* La solicitud de firma de certificado (CSR) debe haberse generado desde el Panel de control. De lo contrario, no podrá instalar el certificado desde el Panel de control.
* La solicitud de firma de certificado (CSR) debe coincidir con el subdominio delegado a Adobe. Por ejemplo, no puede contener más subdominios que el que se ha delegado.
* El certificado debe tener una fecha actual. No es posible instalar certificados con fechas en el futuro y no deben caducar (es decir, fechas de inicio y finalización válidas).
* El certificado debe ser emitido por una autoridad de certificación (CA) de confianza como Comodo, DigiCert, GoDaddy, etc.
* El tamaño del certificado debe ser de 2048 bits y el algoritmo debe ser RSA.
* El certificado debe tener el formato X.509 PEM.
* Se admiten certificados SAN.
* No se admiten los certificados comodín.
* El archivo ZIP o el certificado no deben estar protegidos con contraseña.
* El archivo ZIP solo debe contener lo siguiente en los archivos preferiblemente individuales:
   * Certificado de entidad final.
   * Cadena de certificados intermedia (organizada en orden correcto).
   * Certificado raíz (opcional).

Para instalar el certificado, siga estos pasos:

1. En la **[!UICONTROL Subdomains & Certificates]** tarjeta, seleccione la instancia que desee y haga clic en el **[!UICONTROL Manage Certificate]** botón.

   ![](assets/renewal1.png)

1. Haga clic en **[!UICONTROL Install SSL Certificate]**, luego **[!UICONTROL Next]** para iniciar el asistente que lo guiará a través del proceso de instalación del certificado.

   ![](assets/install1.png)

1. Seleccione el archivo .zip que contiene el certificado que desea instalar y haga clic en **[!UICONTROL Submit]**.

   ![](assets/install2.png)

Una vez instalado el certificado SSL, la fecha de caducidad y el icono de estado del certificado se actualizan en consecuencia.

**Temas relacionados:**

* [Adición de certificados SSL (vídeo de tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Marca de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
* [Supervisión de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)