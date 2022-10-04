---
product: campaign
solution: Campaign
title: Renovación del certificado SSL de un subdominio
description: Obtenga información sobre cómo renovar los certificados SSL de los subdominios
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 963c2af5cdca80ebc2cd79e0708dc4dfe8c6ec1e
workflow-type: ht
source-wordcount: '228'
ht-degree: 100%

---

# Renovación de un certificado SSL {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Renovación de certificado SSL"
>abstract="Para renovar un certificado SSL, debe generar una CSR, adquirir el certificado SSL de los subdominios e instalar el paquete de certificados."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=es#generating-csr" text="Generación de una solicitud de firma de certificado (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=es#installing-ssl-certificate" text="Instalación de un certificado SSL"

El proceso de renovación de certificados SSL incluye 3 pasos:

1. **Generación de la solicitud de firma de certificado (CSR)**

   La solicitud de firma de certificado debe generarse para la instancia y los subdominios que tiene previsto proteger antes de comprar un certificado.  Debe proporcionar la información necesaria para generar la CSR (como Nombre común, Nombre de organización y dirección, etc.). [Más información](generate-csr.md)

1. **Compra del certificado SSL**

   Una vez generada la CSR, puede utilizarla para adquirir el certificado SSL de la autoridad de certificación que apruebe su compañía.

1. **Instalación del certificado SSL**

   Instale el certificado SSL adquirido en el subdominio deseado para protegerlo. [Más información](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Descubra esta función en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=es#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=es#adding-ssl-certificates)

**Temas relacionados:**

* [Guía de prácticas recomendadas de capacidad de entrega: Proceso de solicitud de certificado SSL para Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=es)
* [Promoción de la marca de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitorización de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)
