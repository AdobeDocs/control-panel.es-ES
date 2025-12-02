---
product: campaign
solution: Campaign
title: Delegar certificados SSL de los subdominios en Adobe
description: Obtener información sobre cómo delegar sus certificados SSL de los subdominios a Adobe
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a2b3d409-704b-4e81-ae40-b734f755b598
source-git-commit: 31d181770474428a7b42e96f2e603cc820db48d4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 61%

---

# Delegar certificados SSL de los subdominios en Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="Delegar certificados SSL de los subdominios en Adobe"
>abstract="El Panel de control le permite que Adobe administre los certificados SSL de sus subdominios. Si utiliza CNAME para configurar el subdominio, los registros de certificados se generarán y se proporcionarán automáticamente para generar un certificado en la solución de alojamiento de dominios."

Se recomienda delegar la administración de los certificados SSL de los subdominios a Adobe, ya que Adobe creará automáticamente el certificado y lo renovará cada año antes de que caduque.

Si utiliza CNAME para configurar una delegación de subdominios, Adobe proporcionará registros de certificado para usarlos en la solución de alojamiento de dominios con el fin de generar tu certificado.

La delegación de certificados SSL a Adobe se puede realizar al configurar un nuevo subdominio o para subdominios ya delegados.

>[!NOTE]
>
>SSL administrado por Adobe es una funcionalidad gratuita a disposición de los usuarios sin cargo alguno. La delegación del certificado de un subdominio a Adobe es transparente y no afecta a las campañas ni a la entregabilidad. [Obtenga más información sobre la administración de certificados SSL](monitoring-ssl-certificates.md#management)


## Delegación de nuevos certificados SSL de subdominios {#new}

Para delegar certificados SSL al configurar un subdominio nuevo, habilite la opción **[!UICONTROL Optar por SSL administrado por Adobe para subdominios]** del asistente de configuración de subdominios. El proceso de generación de certificados difiere según el método de delegación de subdominios:

* **Delegación de subdominios completa**: Adobe solicita e instala automáticamente el certificado SSL sin que usted tenga que realizar ninguna acción. Una vez enviada la configuración del subdominio, la solicitud de instalación del certificado se procesa inmediatamente como parte del flujo de trabajo de configuración del subdominio. [Más información sobre la delegación de subdominios completa](setting-up-new-subdomain.md#full-subdomain-delegation)

* **Delegación CNAME**: los registros de certificado que se van a copiar en su solución de alojamiento se proporcionarán más adelante en el asistente de configuración. Debe generar estos registros de certificado en la solución de alojamiento de dominios antes de enviar la configuración del subdominio. [Más información sobre la delegación CNAME](setting-up-new-subdomain.md#use-cnames)

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## Delegación de certificados SSL para subdominios ya delegados {#delegated}

Para delegar certificados SSL para un subdominio ya delegado, pulse el botón de los tres puntos situado junto al subdominio deseado y haga clic en **[!UICONTROL Cambiar a SSL administrado]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

El proceso de generación de certificados depende de cómo se configuró originalmente el subdominio:

### Subdominios totalmente delegados

Para los subdominios configurados mediante delegación de subdominios completa (con servidores de nombres Adobe), Adobe solicita e instala automáticamente el certificado SSL. Una vez que haga clic en **[!UICONTROL Cambiar a SSL administrado]** y confirme, la solicitud de instalación del certificado se enviará inmediatamente sin que usted requiera ninguna acción adicional.

### Subdominios delegados CNAME

Para los subdominios configurados con la delegación CNAME, se muestra un cuadro de diálogo con los registros de certificado generados automáticamente por Adobe. Copie estos registros, uno por uno o descargando un archivo CSV, y luego vaya a la solución de alojamiento de dominios para generar los certificados coincidentes.

Asegúrese de que todos los registros de certificados se hayan generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, confirme la creación de los registros y haga clic en **[!UICONTROL Enviar]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
