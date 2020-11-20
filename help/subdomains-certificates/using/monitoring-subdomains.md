---
product: campaign
solution: Campaign
title: Supervisión de los certificados SSL de los subdominios
description: Obtenga información sobre cómo supervisar los certificados SSL de los subdominios
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 24%

---


# Supervisión de subdominios {#monitoring-subdomains}

Es esencial supervisar los subdominios para asegurarse de que todos están configurados correctamente para funcionar con Adobe Campaign.

Se puede acceder directamente a la lista de subdominios para cada una de las instancias de producción al seleccionar la **[!UICONTROL Subdomains & Certificates]** tarjeta.

La **[!UICONTROL Last verification]** columna indica cuándo se verificó un subdominio por última vez. Puede iniciar una verificación en cualquier momento haciendo clic en el botón **...** / **[!UICONTROL Verify subdomain]** .

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe no recomienda el uso de subdominios sin fecha de certificado, ya que esto podría significar que estos subdominios podrían tener algunos problemas de entrega.

Al iniciar una verificación, se realizan varias operaciones para comprobar que el subdominio está configurado correctamente (comprobación de inquilino de instancia, prueba de envío de correo electrónico, etc.)

Si falla la verificación del subdominio, póngase en contacto con el Servicio de atención al cliente de Adobe para obtener más información.

**Temas relacionados:**

* [Adición de certificados SSL (tutorial en vídeo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Renovación del certificado SSL de un subdominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Promoción de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
