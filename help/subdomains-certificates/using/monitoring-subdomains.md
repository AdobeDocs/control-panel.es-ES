---
product: campaign
solution: Campaign
title: Supervisión de los certificados SSL de los subdominios
description: Obtenga información sobre cómo supervisar los certificados SSL de los subdominios
feature: Control Panel
role: Architect
level: Experienced
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 17%

---


# Supervisión de subdominios {#monitoring-subdomains}

Es esencial monitorizar los subdominios para garantizar que todos estén correctamente configurados para funcionar con Adobe Campaign.

Se puede acceder directamente a la lista de subdominios para cada una de las instancias de producción al seleccionar la tarjeta **[!UICONTROL Subdomains & Certificates]** .

La columna **[!UICONTROL Last verification]** indica cuándo se verificó un subdominio por última vez. Puede iniciar una verificación en cualquier momento haciendo clic en **...Botón** / **[!UICONTROL Verify subdomain]**.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe no recomienda el uso de subdominios sin fecha de certificado, ya que podría significar que estos subdominios pueden estar teniendo algunos problemas de envío.

Al iniciar una verificación, se realizan varias operaciones para comprobar que el subdominio está configurado correctamente (comprobación de inquilino de instancia, prueba de envío de correo electrónico, etc.)

Si falla la verificación del subdominio, póngase en contacto con el servicio de atención al cliente de Adobe para obtener más información.

**Temas relacionados:**

* [Renovación del certificado SSL de un subdominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Promoción de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
