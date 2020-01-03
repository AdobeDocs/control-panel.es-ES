---
title: Supervisión de los certificados SSL de los subdominios
description: Obtenga información sobre cómo supervisar los certificados SSL de los subdominios
translation-type: tm+mt
source-git-commit: 001064877594a10733c054f925f254545f93145d

---


# Supervisión de los certificados SSL de los subdominios {#monitoring-ssl-certificates}

## Acerca de los certificados SSL {#about-ssl-certificates}

Adobe Campaign recomienda proteger los subdominios que alojan las páginas de aterrizaje, especialmente aquellos que recopilan información confidencial de sus clientes.

**El cifrado** SSL (Capa de zócalo seguro) garantiza que los subdominios delegados en Adobe sean seguros. Cuando el cliente rellena un formulario web o visita una página de aterrizaje alojada por Adobe Campaign, la información se envía de forma predeterminada a través de un protocolo no seguro (HTTP). Para garantizar una seguridad adicional, proteja la información enviada con un protocolo HTTPS. Por ejemplo, su dirección de subdominio &quot;http://info.mywebsite.com/&quot; será ahora &quot;https://info.mywebsite.com/&quot;.

**Los certificados SSL no están instalados en los propios** subdominios delegados. Se instalan en subdominios asociados, principalmente los que hospedan páginas de aterrizaje, páginas de recursos y otros.

**Los certificados SSL se proporcionan para un período de tiempo** específico (1 año, 60 días, etc.). Una vez que caduca un certificado, puede experimentar problemas al acceder a las páginas de aterrizaje o al usar recursos del subdominio. Para evitarlo, el Panel de control le permite supervisar los certificados SSL de los subdominios, así como iniciar el proceso de renovación.

![](assets/no_certificate.png)

## Supervisión de certificados SSL {#monitoring-certificates}

El estado de los certificados SSL de los subdominios está disponible directamente en la lista de subdominios al seleccionar la **[!UICONTROL Subdomains & Certificates]**tarjeta.

Los subdominios se organizan según la fecha de caducidad más próxima del certificado SSL, con información visual sobre la caducidad, en días:

* **Verde**: el subdominio no tiene un certificado que caduque en los próximos 60 días.
* **Naranja**: uno o varios subdominios tienen un certificado que caducará en los próximos 60 días.
* **Rojo**: uno o varios subdominios tienen un certificado que caducará en los próximos 30 días.
* **Gris**: no se ha instalado ningún certificado para el subdominio.

![](assets/subdomains_list.png)

Para obtener más información sobre un subdominio, haga clic en el **[!UICONTROL Subdomain Details]**botón .
Se muestra la lista de todos los subdominios relacionados. Generalmente incluye subdominios de páginas de aterrizaje, páginas de recursos, etc.

La **[!UICONTROL Sender info]**ficha proporciona información sobre las bandejas de entrada configuradas (Remitente, Responder a, Correo electrónico de error).

![](assets/subdomain_details.png)

Si uno de los certificados SSL de su subdominio está a punto de caducar, puede renovarlo directamente desde el Panel de control. Para obtener más información sobre esto, consulte esta sección: [Renovación del certificado](../../subdomains-certificates/using/renewing-subdomain-certificate.md)SSL de un subdominio.

>[!NOTE]
>
>La renovación de certificados del Panel de control pronto estará disponible en versión beta. Mientras tanto, consulte [esta página](https://helpx.adobe.com/campaign/kb/control-panel-subdomains-certificates.html) para obtener más información sobre cómo supervisar los certificados dentro del Panel de control.
