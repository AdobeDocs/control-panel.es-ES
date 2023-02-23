---
product: campaign
solution: Campaign
title: Monitorización de subdominios
description: Supervise los subdominios para asegurarse de que todos están correctamente configurados para funcionar con Adobe Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: acf0334e894649d6b5edf0b96877c3f643894763
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---


# Supervisión de los subdominios {#monitoring-subdomains}

Es esencial monitorizar los subdominios para garantizar que todos estén correctamente configurados para funcionar con Adobe Campaign.

Se puede acceder directamente a la lista de subdominios de cada una de las instancias de producción al seleccionar la variable **[!UICONTROL Subdomains & Certificates]** tarjeta.

La variable **[!UICONTROL Last verification]** indica cuándo se verificó un subdominio por última vez. Puede iniciar una verificación en cualquier momento haciendo clic en el botón **...** / **[!UICONTROL Verify subdomain]** botón.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe no recomienda el uso de subdominios sin fecha de certificado, ya que podría significar que estos subdominios pueden estar teniendo algunos problemas de envío.

Al iniciar una verificación, se realizan varias operaciones para comprobar que el subdominio está configurado correctamente (comprobación de inquilino de instancia, prueba de envío de correo electrónico, etc.) Si falla la verificación del subdominio, póngase en contacto con el servicio de atención al cliente de Adobe para obtener más información.

**Temas relacionados:**

* [Renovación del certificado SSL de un subdominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Promoción de la marca de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
