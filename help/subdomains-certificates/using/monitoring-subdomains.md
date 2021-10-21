---
product: campaign
solution: Campaign
title: Supervisión de los certificados SSL de los subdominios
description: Obtenga información sobre cómo supervisar los certificados SSL de los subdominios
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 8dce5b9d1eb59b7ebc8ef1f73f7552dcf61077a1
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 21%

---

# Supervisión de subdominios {#monitoring-subdomains}

>[!AVAILABILITY]
>
>Esta capacidad no está disponible para Campaign v8.

Es esencial monitorizar los subdominios para garantizar que todos estén correctamente configurados para funcionar con Adobe Campaign.

Se puede acceder directamente a la lista de subdominios de cada una de las instancias de producción al seleccionar la variable **[!UICONTROL Subdomains & Certificates]** tarjeta.

La variable **[!UICONTROL Last verification]** indica cuándo se verificó un subdominio por última vez. Puede iniciar una verificación en cualquier momento haciendo clic en el botón **...** / **[!UICONTROL Verify subdomain]** botón.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe no recomienda el uso de subdominios sin fecha de certificado, ya que podría significar que estos subdominios pueden estar teniendo algunos problemas de envío.

Al iniciar una verificación, se realizan varias operaciones para comprobar que el subdominio está configurado correctamente (comprobación de inquilino de instancia, prueba de envío de correo electrónico, etc.)

Si falla la verificación del subdominio, póngase en contacto con el servicio de atención al cliente de Adobe para obtener más información.

**Temas relacionados:**

* [Renovación del certificado SSL de un subdominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Promoción de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
