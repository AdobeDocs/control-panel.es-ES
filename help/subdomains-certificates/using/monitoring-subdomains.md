---
product: campaign
solution: Campaign
title: Monitorización de subdominios
description: Supervise los subdominios para asegurarse de que están correctamente configurados para trabajar con Adobe Campaign.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 9%

---


# Supervisión de los subdominios {#monitoring-subdomains}

Es esencial monitorizar los subdominios para asegurarse de que están correctamente configurados para trabajar con Adobe Campaign.

Se puede acceder directamente a la lista de subdominios para cada una de las instancias de producción al seleccionar el **[!UICONTROL Subdominios y certificados]** Tarjeta de.

El **[!UICONTROL Última verificación]** indica cuándo se verificó un subdominio por última vez. Puede iniciar una verificación en cualquier momento haciendo clic en el icono **...** / **[!UICONTROL Verificar subdominio]** botón.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>El Adobe no recomienda el uso de subdominios sin fecha de certificado, ya que podría significar que estos subdominios pueden tener algunos problemas de envío.

Al iniciar una verificación, se realizan varias operaciones para comprobar que el subdominio está configurado correctamente (comprobación del inquilino de la instancia, prueba de envío de correo electrónico, etc.) Si la verificación del subdominio falla, póngase en contacto con el Servicio de atención al cliente de Adobe para obtener más información.

**Temas relacionados:**

* [Renovación del certificado SSL de un subdominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Promoción de la marca de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
