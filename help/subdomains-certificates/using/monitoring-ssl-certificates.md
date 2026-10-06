---
product: campaign
solution: Campaign
title: Supervisión de los certificados SSL de los subdominios
description: Obtenga información sobre cómo supervisar los certificados SSL de los subdominios
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 100%
---
# Supervisión de los certificados SSL de los subdominios {#monitoring-ssl-certificates}

## Acerca de los certificados SSL {#about-ssl-certificates}

Adobe Campaign recomienda proteger los subdominios que albergan sus páginas de destino, especialmente aquellos que recopilan información confidencial de sus clientes.

**El cifrado SSL (Secure Socket Layer)** garantiza que los subdominios que haya configurado para que funcionen con Adobe sean seguros. Cuando el cliente rellena un formulario web o visita una página de destino alojada en Adobe Campaign, la información se envía de forma predeterminada a través de un protocolo no seguro (HTTP). Para garantizar una seguridad adicional, proteja la información enviada con un protocolo HTTPS. Por ejemplo, su dirección de subdominio &quot;http://info.mywebsite.com/&quot; será ahora &quot;https://info.mywebsite.com/&quot;.

**Los certificados SSL no están instalados en los propios subdominios configurados**. Se instalan en subdominios asociados, principalmente los que hospedan páginas de destino, páginas de recursos y otros.

**Los certificados SSL se proporcionan para un período de tiempo** específico (1 año, 60 días, etc.). Una vez que caduca un certificado, puede experimentar problemas al acceder a las páginas de destino o al usar recursos del subdominio. Para evitarlo, el Panel de control le permite supervisar los certificados SSL de los subdominios, así como iniciar el proceso de renovación.

![](assets/no_certificate.png)

## Administración de certificados SSL {#management}

La monitorización de los certificados SSL es clave para garantizar que los subdominios sean seguros. Con el Panel de control, puede instalar y renovar los certificados SSL de los subdominios directamente usted mismo, o delegarlos en Adobe para que este proceso se realice automáticamente sin que tenga que hacer nada.

Se recomienda delegar la administración de los certificados SSL de los subdominios a Adobe, ya que Adobe creará automáticamente el certificado y lo renovará cada año antes de que caduque. Esto reduce el riesgo de errores que se pueden producir al administrar los certificados manualmente. [Descubra cómo delegar certificados SSL de subdominios en Adobe](delegate-ssl.md)

A continuación, encontrará una lista completa de los impactos asociados a la administración manual de certificados frente a delegar esta operación en Adobe:

|       | Certificado administrado por el cliente | Certificado administrado por Adobe |
|  ---  |  ---  |  ---  |
| Proveedor de certificados | Autoridades de certificación de terceros | Adobe mediante AWS Certificate Manager |
| Pasos manuales | Generación de CSR, compra e instalación de certificados | Ninguno |
| Proceso de renovación | Responsabilidad del cliente | Administrado automáticamente por Adobe |
| Seguridad del subdominio | El dominio puede tener subdominios no seguros (seguimiento, duplicación y res) a menos que esté instalando/renovando certificados. | Todos los dominios nuevos (si se opta por la administración de Adobe) tendrán todos los subdominios protegidos de forma predeterminada. |
| Coste del certificado | El cliente asume el coste de los certificados | Gratuito |

## Monitorización de certificados SSL {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Detalles del subdominio"
>abstract="Recupere información sobre los certificados SSL de los subdominios."

El estado de los certificados SSL de los subdominios está disponible directamente desde la lista de subdominios al seleccionar la tarjeta **[!UICONTROL Subdominios y certificados]**.

Los subdominios se organizan según la fecha de caducidad más próxima del certificado SSL, con información visual sobre la caducidad, en días:

* **Verde**: el subdominio no tiene un certificado que caduque en los próximos 60 días.
* **Naranja**: uno o varios subdominios tienen un certificado que caducará en los próximos 60 días.
* **Rojo**: uno o varios subdominios tienen un certificado que caducará en los próximos 30 días.
* **Gris**: no se ha instalado ningún certificado para el subdominio.

![](assets/subdomains_list.png)

Para obtener más detalles acerca de un subdominio, haga clic en el botón **[!UICONTROL Detalles del subdominio]**.
Se muestra la lista de todos los subdominios relacionados. Por lo general, incluye subdominios de páginas de destino, páginas de recursos, etc.

La pestaña **[!UICONTROL Información del remitente]** proporciona información sobre las bandejas de entrada configuradas (Remitente, Responder a, Correo electrónico de error).

![](assets/subdomain_details.png)

Si uno de los certificados SSL de su subdominio está a punto de caducar, puede renovarlo directamente desde el Panel de control. Para obtener más información sobre esto, consulte esta sección: [Renovación del certificado SSL de un subdominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

**Temas relacionados:**

* [Renovación del certificado SSL de un subdominio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Promoción de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
