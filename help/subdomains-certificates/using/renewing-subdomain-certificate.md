---
product: campaign
solution: Campaign
title: Renovación del certificado SSL de un subdominio
description: Obtenga información sobre cómo renovar los certificados SSL de los subdominios
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 1f422833e1495525612e760714e50a9aaf744db5
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 88%

---

# Renovación del certificado SSL de un subdominio {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="renovación de certificado SSL"
>abstract="Para renovar un certificado SSL, debe generar un CSR, adquirir el certificado SSL para los subdominios e instalar el paquete de certificados."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="Generación de una solicitud de firma de certificado (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="Instalación de un certificado SSL"

## Acerca de la renovación de certificados {#about-certificate-renewal-process}

>[!IMPORTANT]
>
>La configuración de subdominios del Panel de control de Campaign está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.
>
>Esta capacidad no está disponible para Campaign v8.

El proceso de renovación de certificados SSL incluye 3 pasos:

1. **Generación de la solicitud de firma de certificado (CSR)**
El Servicio de atención al cliente de Adobe genera un CSR para usted. Debe proporcionar la información necesaria para generar la CSR (como Nombre común, Nombre de organización y dirección, etc.).
1. **Compra del certificado SSL**
Una vez generada la CSR, puede descargarla y utilizarla para adquirir el certificado SSL de la entidad emisora de certificados que apruebe su compañía.
1. **Instalación del certificado SSL**
Una vez adquirido el certificado SSL, puede instalarlo en el subdominio deseado.

![](assets/do-not-localize/how-to-video.png) Descubra esta función en vídeo usando [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#adding-ssl-certificates)

## Generación de una solicitud de firma de certificado (CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="Generación de CSR"
>abstract="La solicitud de firma de certificado debe generarse para la instancia y los subdominios que tiene previsto proteger antes de comprar un certificado."

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="Selección de los subdominios para la CSR"
>abstract="Puede optar por incluir todos los subdominios o solo los específicos en la solicitud de firma de certificado. Solo los subdominios seleccionados se certificarán mediante el certificado SSL adquirido."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="Acerca de la marca de subdominios"

Para generar una solicitud de firma de certificado (CSR), siga estos pasos:

1. En la tarjeta **[!UICONTROL Subdomains & Certificates]**, seleccione la instancia que desee y haga clic en el botón **[!UICONTROL Manage Certificate]**.

   ![](assets/renewal1.png)

1. Seleccione **[!UICONTROL 1 - Generate a CSR]**, luego haga clic en **[!UICONTROL Next]** para iniciar el asistente que lo guiará a través del proceso de generación de CSR.

   ![](assets/renewal2.png)

1. Verá un formulario con todos los detalles necesarios para generar su CSR.

   Asegúrese de completar la información solicitada de forma completa y precisa; de lo contrario, es posible que el certificado no se renueve (póngase en contacto con el equipo interno, los equipos de seguridad y TI si es necesario) y haga clic en **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**: nombre oficial de la organización.
   * **[!UICONTROL Organization Unit]**: unidad vinculada al subdominio (ejemplo: Marketing, TI).
   * **[!UICONTROL Instance]** (precargada): dirección URL de la instancia de Campaign asociada al subdominio.

   ![](assets/renewal3.png)

1. Seleccione los subdominios que desea incluir en la CSR y, a continuación, haga clic en **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Los subdominios seleccionados se muestran en la lista. Para cada uno de ellos, seleccione los subdominios que desee incluir y haga clic en **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. Se muestra un resumen de los subdominios que se incluirán en la CSR. Haga clic en **[!UICONTROL Submit]** para confirmar la solicitud.

   ![](assets/renewal6.png)

1. El archivo .csr correspondiente a su selección se genera y descarga automáticamente. Ahora puede utilizarlo para adquirir el certificado SSL de la entidad emisora de certificados que apruebe su compañía.

   >[!NOTE]
   >
   >Si el archivo no se guarda o descarga, se perderá y tendrá que volver a generarlo.

## Compra de un certificado con la CSR {#purchasing-certificate}

Después de obtener una CSR (solicitud de firma de certificado) de Panel de control de Campaign, compre un certificado SSL de una autoridad de certificación aprobada por su organización.

## Instalación del certificado SSL {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Instalación del certificado SSL"
>abstract="Instale el certificado SSL adquirido de la entidad emisora de certificados aprobada por su organización."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="Acerca de la marca de subdominios"

Una vez adquirido un certificado SSL, puede instalarlo en su instancia. Antes de continuar, asegúrese de conocer los requisitos previos siguientes:

* La solicitud de firma de certificado (CSR) debe haberse generado desde el Panel de control de Campaign. De lo contrario, no podrá instalar el certificado desde el Panel de control de Campaign.
* La solicitud de firma de certificado (CSR) debe coincidir con el subdominio configurado para funcionar con Adobe. Por ejemplo, no puede contener más subdominios que el que se ha configurado.
* El certificado debe tener una fecha actual. No es posible instalar certificados con fechas en el futuro y no deben caducar (es decir, fechas de inicio y finalización válidas).
* El certificado debe ser emitido por una autoridad de certificación (CA) de confianza como Comodo, DigiCert, GoDaddy, etc.
* El tamaño del certificado debe ser de 2048 bits y el algoritmo debe ser RSA.
* El certificado debe tener el formato X.509 PEM.
* Se admiten certificados SAN.
* No se admiten certificados comodín.
* El archivo ZIP o el certificado no deben estar protegidos con contraseña.
* El archivo ZIP solo debe contener lo siguiente en los archivos preferiblemente individuales:
   * Certificado de entidad final.
   * Cadena de certificados intermedia (organizada en orden correcto).
   * Certificado raíz (opcional).

Para instalar el certificado, siga estos pasos:

1. En la tarjeta **[!UICONTROL Subdomains & Certificates]**, seleccione la instancia que desee y haga clic en el botón **[!UICONTROL Manage Certificate]**.

   ![](assets/renewal1.png)

1. Seleccione **[!UICONTROL 3 - Install Certificate Bundle]**, luego haga clic en **[!UICONTROL Next]** para iniciar el asistente que lo guiará a través del proceso de instalación del certificado.

   ![](assets/install1.png)

1. Seleccione el archivo .zip que contiene el certificado que desea instalar y haga clic en **[!UICONTROL Submit]**.

   ![](assets/install2.png)

>[!NOTE]
>
>El certificado se instalará en todos los dominios o subdominios incluidos en la CSR. No se tendrá en cuenta ningún dominio o subdominio adicional presente en el certificado.

Una vez instalado el certificado SSL, la fecha de caducidad y el icono de estado del certificado se actualizan en consecuencia.

**Temas relacionados:**

* [Promoción de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
* [Supervisión de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)
