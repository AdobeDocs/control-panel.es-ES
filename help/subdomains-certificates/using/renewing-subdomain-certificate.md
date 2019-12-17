---
title: Renovación del certificado SSL de un subdominio
description: Obtenga información sobre cómo renovar los certificados SSL de los subdominios
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Renovación del certificado SSL de un subdominio {#renewing-subdomains-ssl-certificates}

## Acerca de la renovación de certificados {#about-certificate-renewal-process}

El proceso de renovación de certificados SSL incluye 3 pasos, que se realizan directamente desde el Panel de control:

1. **Generación de la solicitud de firma certificada (CSR) El Servicio de atención al cliente de** Adobe genera un CSR para usted. Deberá proporcionar la información necesaria para generar el CSR (como Nombre común, Nombre de organización y dirección, etc.).
1. **Compra del certificado** SSL Una vez generado el CSR, puede descargarlo y utilizarlo para adquirir el certificado SSL de la entidad emisora de certificados que apruebe su empresa.
1. **Instalación del certificado** SSL Una vez adquirido el certificado SSL, puede instalarlo en el subdominio deseado.

## Generación de una solicitud de firma de certificado (CSR) {#generating-csr}

Para generar una solicitud de firma de certificado (CSR), siga estos pasos:

1. En la **[!UICONTROL Subdomains & Certificates]**tarjeta, seleccione la instancia que desee y haga clic en el**[!UICONTROL Manage Certificate]** botón.

   ![](assets/renewal1.png)

1. Seleccione **[!UICONTROL Generate a CSR]**, luego haga clic**[!UICONTROL Next]** para iniciar el asistente que lo guiará a través del proceso de generación de CSR.

   ![](assets/renewal2.png)

1. Se muestra un formulario con todos los detalles necesarios para generar su CSR.

   Asegúrese de completar la información solicitada de manera completa y precisa (póngase en contacto con su equipo interno, con los equipos de seguridad y TI si es necesario) y, a continuación, haga clic en **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**:
   * **[!UICONTROL Organization Unit]**:
   * **[!UICONTROL Instance]**:: Dirección URL de la instancia de Campaign asociada al subdominio.
   ![](assets/renewal3.png)

1. Seleccione los subdominios que desea incluir en el CSR y, a continuación, haga clic en **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Los subdominios seleccionados se muestran en la lista. Para cada uno de ellos, seleccione los subdominios que desee incluir y haga clic en **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. Se muestra un resumen de los subdominios que se incluirán en el CSR. Haga clic en **[!UICONTROL Submit]**para confirmar la solicitud.

   ![](assets/renewal6.png)

1. El archivo .csr correspondiente a su selección se genera y descarga automáticamente. Ahora puede utilizarla para adquirir el certificado SSL de la entidad emisora de certificados que apruebe su empresa.

## Compra de un certificado con el CSR {#purchasing-certificate}

Después de obtener un CSR de solicitud de firma de certificado del Panel de control, compre un certificado SSL de una autoridad de certificación aprobada por su organización.

## Instalación del certificado SSL {#installing-ssl-certificate}

Una vez adquirido un certificado SSL, siga estos pasos para instalarlo en su instancia.

1. En la **[!UICONTROL Subdomains & Certificates]**tarjeta, seleccione la instancia que desee y haga clic en el**[!UICONTROL Manage Certificate]** botón.

   ![](assets/renewal1.png)

1. Haga clic en **[!UICONTROL Install SSL Certificate]**, luego**[!UICONTROL Next]** para iniciar el asistente que lo guiará a través del proceso de instalación del certificado.

   ![](assets/install1.png)

1. Seleccione el archivo .zip que contiene el certificado que desea instalar y haga clic en **[!UICONTROL Submit]**.

   ![](assets/install2.png)
