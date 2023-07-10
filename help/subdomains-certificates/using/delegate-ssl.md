---
product: campaign
solution: Campaign
title: Delegar certificados SSL de los subdominios en Adobe
description: Obtener información sobre cómo delegar sus certificados SSL de los subdominios a Adobe
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 0eefdbde25c955c84ee7534976256ca4df9a686c
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 100%

---

# Delegar certificados SSL de los subdominios en Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="Delegar certificados SSL de los subdominios en Adobe"
>abstract="El Panel de control le permite administrar por Adobe los certificados SSL de los subdominios. Si utiliza CNAME para configurar el subdominio, los registros de certificados se generarán y proporcionarán automáticamente para generar un certificado en la solución de alojamiento de dominios."

Se recomienda delegar los certificados SSL de los subdominios al Adobe, ya que Adobe creará automáticamente el certificado y lo renovará cada año antes de que caduque el certificado.

Si utiliza CNAME para configurar una delegación de subdominios, Adobe proporcionará registros de certificado para usarlos en la solución de alojamiento de dominios con el fin de generar tu certificado.

La delegación de certificados SSL a Adobe se puede realizar al configurar un nuevo subdominio o para subdominios ya delegados.

>[!NOTE]
>
>SSL administrado por Adobe es una funcionalidad gratuita a disposición de los usuarios sin cargo alguno.

## Delegación de nuevos certificados SSL de subdominios {#new}

Para delegar certificados SSL al configurar un nuevo subdominio, habilite la opción **[!UICONTROL Opt for Adobe managed SSL for sub-domains]** del asistente de configuración de subdominios. Los registros de certificados que se copiarán en la solución de alojamiento se proporcionarán más adelante en el asistente de configuración. Los pasos detallados se documentan en [esta sección](setting-up-new-subdomain.md).

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## Delegación de certificados SSL para subdominios ya delegados {#delegated}

Para delegar certificados SSL para un subdominio ya delegado, haga clic en el botón de puntos suspensivos situado junto al subdominio deseado y seleccione **[!UICONTROL Switch to Managed SSL]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

Aparece un cuadro de diálogo con los registros de certificado que Adobe ha generado automáticamente. Copie estos registros, uno por uno o descargando un archivo CSV, y luego vaya a la solución de alojamiento de dominios para generar los certificados coincidentes.

Asegúrese de que todos los registros de certificados se hayan generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, confirme la creación de los registros y haga clic en **[!UICONTROL Submit]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
