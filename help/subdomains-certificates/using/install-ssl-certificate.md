---
product: campaign
solution: Campaign
title: Renovación del certificado SSL de un subdominio
description: Obtenga información sobre cómo renovar los certificados SSL de los subdominios
feature: Control Panel
role: Architect
level: Experienced
exl-id: af440b5d-1d21-44fb-831f-f2bdd6011b82
source-git-commit: 9be5a3ae48dccf74f509aa95fee29bbfdafddcdf
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 89%

---

# Instalación del certificado SSL {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Instalación del certificado SSL"
>abstract="Instale el certificado SSL adquirido de la entidad emisora de certificados aprobada por su organización."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=es" text="Acerca de la marca de subdominios"

Una vez adquirido un certificado SSL, puede instalarlo en su instancia. Antes de continuar, asegúrese de conocer los requisitos previos siguientes:

* La solicitud de firma de certificado (CSR) debe haberse generado desde el Panel de control. De lo contrario, no podrá instalar el certificado desde el Panel de control.
* La solicitud de firma de certificado (CSR) debe coincidir con el subdominio que se configuró para funcionar con el Adobe. Por ejemplo, no puede contener más subdominios que el que se ha configurado.
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
