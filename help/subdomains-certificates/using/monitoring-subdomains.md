---
product: campaign
solution: Campaign
title: Monitorización de subdominios
description: Supervise los subdominios para asegurarse de que todos están correctamente configurados para funcionar con Adobe Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: a6a77cf6e564f4607c0c12facb2061cfb102a5a5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 7%

---

# Monitorización de subdominios {#monitoring-subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Eliminar subdominios delegados "
>abstract="Esta pantalla le permite eliminar cualquier subdominio que se haya delegado en Panel de control de Campaign. Tenga en cuenta que la eliminación del subdominio no se puede deshacer y será irreversible una vez enviado.<br>Si está intentando quitar el dominio principal de la instancia seleccionada, se le pedirá que elija el dominio que la sustituirá."

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
* [Promoción de la marca de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
