---
title: Supervisión de los certificados SSL de los subdominios
description: Obtenga información sobre cómo supervisar los certificados SSL de los subdominios
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Supervisión de subdominios {#monitoring-subdomains}

Es esencial supervisar los subdominios para asegurarse de que todos están configurados correctamente para funcionar con Adobe Campaign.

Se puede acceder directamente a la lista de subdominios de cada una de las instancias de producción al seleccionar la **[!UICONTROL Subdomains & Certificates]**tarjeta.

![](assets/subdomains_list.png)

Para obtener más información sobre un subdominio, haga clic en el **[!UICONTROL Subdomain Details]**botón .
Se muestra la lista de todos los subdominios relacionados. Generalmente incluye subdominios de páginas de aterrizaje, páginas de recursos, etc.

La **[!UICONTROL Sender info]**ficha proporciona información sobre las bandejas de entrada configuradas (Remitente, Responder a, Correo electrónico de error).

![](assets/subdomain_details.png)


En la lista de subdominios, la columna indica cuándo se verificó un subdominio por última vez. **[!UICONTROL Last verification]**** Puede iniciar una verificación en cualquier momento haciendo clic en el botón **... /**[!UICONTROL Verify subdomain]** .

>[!CAUTION]
>
>Adobe no recomienda el uso de subdominios sin fecha de verificación, ya que esto podría significar que estos subdominios podrían tener algunos problemas de entrega.

![](assets/subdomain_verification.png)

Al iniciar una verificación, se realizan varias operaciones para comprobar que el subdominio está configurado correctamente:

1. El Panel de control comprueba que el subdominio pertenece al inquilino de instancia.
1. Se envía un correo electrónico desde la instancia que utiliza ese subdominio a un conjunto de destinatarios de prueba de &quot;250ok&quot; (una plataforma de análisis de correo electrónico y entrega de terceros).
1. Después de recibir el correo electrónico, 250ok lee los encabezados de correo electrónico y comprueba si el SPF y DKIM están configurados y son válidos.
1. El Panel de control sondea continuamente el estado de la entrega desde 250ok durante unos 20 minutos. Si SPF y DKIM pasan, significa que el subdominio solicitado se verifica y está completamente configurado y listo para usarse para enviar correos electrónicos.
