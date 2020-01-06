---
title: Supervisión de los certificados SSL de los subdominios
description: Obtenga información sobre cómo supervisar los certificados SSL de los subdominios
translation-type: tm+mt
source-git-commit: c51a43fb310bbb8bd7570bc4ea668d708159535c

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
