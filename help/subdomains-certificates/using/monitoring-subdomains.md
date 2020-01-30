---
title: Supervisión de los certificados SSL de los subdominios
description: Obtenga información sobre cómo supervisar los certificados SSL de los subdominios
translation-type: tm+mt
source-git-commit: ce15da4aabb0350cb9a60cc16556ffcf691fc3df

---


# Supervisión de subdominios {#monitoring-subdomains}

Es esencial supervisar los subdominios para asegurarse de que todos están configurados correctamente para funcionar con Adobe Campaign.

Se puede acceder directamente a la lista de subdominios de cada una de las instancias de producción al seleccionar la **[!UICONTROL Subdomains & Certificates]**tarjeta.

La **[!UICONTROL Last verification]**columna indica cuándo se verificó un subdominio por última vez.** Puede iniciar una verificación en cualquier momento haciendo clic en el botón **... /**[!UICONTROL Verify subdomain]** .

![](assets/subdomain_verification.png)

>[!CAUTION]
>
>Adobe no recomienda el uso de subdominios sin fecha de certificado, ya que esto podría significar que estos subdominios pueden tener algunos problemas de entrega.

Al iniciar una verificación, se realizan varias operaciones para comprobar que el subdominio está configurado correctamente (comprobación de inquilino de instancia, prueba de envío de correo electrónico, etc.)

Si falla la verificación del subdominio, póngase en contacto con el servicio de atención al cliente de Adobe para obtener más información.

**Temas relacionados:**

* [Adición de certificados SSL (vídeo de tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Renovación del certificado SSL de un subdominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
