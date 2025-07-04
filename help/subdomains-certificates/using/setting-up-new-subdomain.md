---
product: campaign
solution: Campaign
title: Configuración de un nuevo subdominio
description: Obtenga información sobre cómo configurar un nuevo subdominio para las instancias de Campaign
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: d92781c3-14cc-4716-a131-580ccff46d6e
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '1526'
ht-degree: 100%

---


# Configuración de un nuevo subdominio {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Configuración de nuevos subdominios y administración de certificados"
>abstract="Debe configurar un nuevo subdominio y administrar los certificados SSL de los subdominios para empezar a enviar correos electrónicos o publicar páginas de aterrizaje con Adobe Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=es" text="Monitorización de certificados SSL"

## Lectura obligatoria {#must-read}

Esta página proporciona información sobre cómo configurar nuevos subdominios mediante delegación de subdominios completos o CNAME. Los conceptos globales sobre estos dos métodos se presentan en esta sección: [Promoción de subdominios](../../subdomains-certificates/using/subdomains-branding.md).

**Temas relacionados:**

* [Supervisión de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)

### Selección de instancias

La delegación de subdominios solo está disponible para instancias de **producción**.

Si la instancia que selecciona en el asistente no tiene subdominios configurados previamente, el primer subdominio configurado se convertirá en el **subdominio principal** para esa instancia y no podrá cambiarlo en el futuro. Como resultado, se crearán **registros DNS inversos** para otros subdominios que usen este subdominio principal. **Las direcciones de respuesta y devolución** de otros subdominios se generarán desde el subdominio principal.

### Delegar certificados SSL de los subdominios en Adobe

Al configurar un nuevo subdominio, puede hacer que Adobe se encargue de administrar el certificado SSL. Esto es muy recomendable, ya que Adobe creará automáticamente el certificado y lo renovará cada año antes de que caduque.

Si utiliza CNAME para configurar una delegación de subdominios, Adobe proporcionará registros de certificado para usarlos en la solución de alojamiento de dominios con el fin de generar su certificado.

>[!NOTE]
>
>SSL administrado por Adobe es una funcionalidad gratuita a disposición de los usuarios sin cargo alguno. [Obtenga más información sobre la administración de certificados SSL](monitoring-ssl-certificates.md#management)

### Configuración de servidores de nombres

Al configurar servidores de nombres, asegúrese de **no delegar nunca su subdominio raíz a Adobe**. De lo contrario, el dominio solo podrá trabajar con Adobe. Cualquier otro uso será imposible, como, por ejemplo, enviar correos electrónicos internos a los empleados de la organización.

Además, **no cree ningún archivo de zona independiente** para este nuevo subdominio.

## Delegación completa de subdominios {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="cp_add_new_subdomain"
>title="Adición de un nuevo subdominio"
>abstract="Adobe recomienda la delegación completa del subdominio. Sin embargo, puede utilizar CNAME o un método personalizado para configurar sus subdominios."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=es" text="Configuración de un nuevo subdominio"
>additional-url="https://helpx.adobe.com/es/enterprise/using/support-for-experience-cloud.html" text="Póngase en contacto con el Servicio de atención al cliente"

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_create_delegate"
>title="Cree y delegue su subdominio"
>abstract="Cree el subdominio que quiere utilizar con Adobe Campaign en su solución de alojamiento y deléguelo en Adobe."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=es" text="Configuración de un nuevo subdominio"

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_submit"
>title="Envío del subdominio"
>abstract="Confirme y envíe el subdominio que se ha configurado en los pasos anteriores."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=es" text="Configuración de un nuevo subdominio"

Para delegar completamente un subdominio a Adobe Campaign, siga los pasos a continuación.

![](assets/do-not-localize/how-to-video.png) Descubra esta funcionalidad en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=es#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=es#subdomains-and-certificates)

1. En la tarjeta **[!UICONTROL Subdominios y certificados]**, seleccione la instancia de producción deseada y, a continuación, haga clic en **[!UICONTROL Configurar nuevo subdominio]**.

   ![](assets/subdomain1.png)

1. Haga clic en **[!UICONTROL Siguiente]** para confirmar el método de delegación completo.

   ![](assets/subdomain3.png)

1. Cree los subdominios y servidores de nombres deseados en la solución de hospedaje que use su organización. Para ello, copie y pegue la información del servidor de nombres de Adobe que se muestra en el asistente. Para obtener más información sobre cómo crear un subdominio en una solución de alojamiento, consulte el [tutorial en vídeo](https://video.tv.adobe.com/v/34038?captions=spa).

   >[!NOTE]
   >
   > Para Adobe Campaign Standard, los subdominios delegados le permiten enviar comunicaciones de **marketing** y **transaccionales**.

   ![](assets/subdomain4.png)

1. Una vez creado el subdominio con la información correspondiente del servidor de nombres de Adobe, haga clic en **[!UICONTROL Siguiente]**.

1. Si ha seleccionado una instancia de Campaign v7/v8, seleccione el caso de uso que desee para el subdominio: **Comunicaciones de marketing** o **Comunicaciones transaccionales y operativas**. Los conceptos globales sobre los casos de uso de los subdominios se presentan en [esta sección](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/subdomain5.png)

1. Escriba el subdominio que ha creado en la solución de alojamiento y, a continuación, haga clic en **[!UICONTROL Enviar]**.

   Asegúrese de añadir el **nombre completo** del subdominio que desea delegar. Por ejemplo, para delegar el subdominio &quot;usoffer.email.weretail.com&quot;, escriba &quot;usoffer.email.weretail.com&quot;.

1. Para delegar la generación del certificado SSL del subdominio a Adobe, habilite la opción **[!UICONTROL Optar por SSL administrado por Adobe para subdominios]**. [Más información acerca de la delegación de certificados SSL](delegate-ssl.md)

   ![](assets/subdomain6.png)

Una vez enviado el subdominio, el Panel de control realizará varias comprobaciones y pasos de configuración. Para obtener más información, consulte [Comprobación y configuración de subdominios](#subdomain-checks-and-configuration).

## Configuración del subdominio mediante CNAME {#use-cnames}

>[!CONTEXTUALHELP]
>id="cp_add_cname_subdomain_create_delegate"
>title="Configuración del subdominio"
>abstract="En esta pantalla, especifique el subdominio que desea configurar con CNAME."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=es" text="Configuración de un nuevo subdominio"

>[!CONTEXTUALHELP]
>id="cp_add_cname_records"
>title="Generación de registros"
>abstract="Vaya a la solución de alojamiento para generar la lista de registros DNS que se muestran en esta pantalla."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=es" text="Configuración de un nuevo subdominio"

>[!CONTEXTUALHELP]
>id="cp_add_cname_subdomain_submit"
>title="Envío del subdominio"
>abstract="Confirme y envíe el subdominio que se ha configurado en los pasos anteriores."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=es" text="Configuración de un nuevo subdominio"

Para configurar un subdominio mediante CNAME, siga los pasos a continuación.

![](assets/do-not-localize/how-to-video.png) Descubra esta función en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=es#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=es)

1. En la tarjeta **[!UICONTROL Subdominios y certificados]**, seleccione la instancia de producción deseada y, a continuación, haga clic en **[!UICONTROL Configurar nuevo subdominio]**.

   ![](assets/subdomain1.png)

1. Seleccione el método **[!UICONTROL CNAME]** y, a continuación, haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/cname-method-selection.png)

1. Si ha seleccionado una instancia de Campaign v7/v8, seleccione el caso de uso que desee para el subdominio: **Comunicaciones de marketing** o **Comunicaciones transaccionales y operativas**. Los conceptos globales sobre los casos de uso de los subdominios se presentan en [esta sección](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/cname-use-case.png)

1. Escriba el subdominio que ha creado en la solución de alojamiento.

   Para delegar la generación del certificado SSL del subdominio a Adobe, habilite la opción **[!UICONTROL Optar por SSL administrado por Adobe para subdominios]**. [Más información sobre la delegación de certificados SSL](delegate-ssl.md)

   ![](assets/cname-adobe-managed.png)

   >[!NOTE]
   >
   >Asegúrese de añadir el **nombre completo** del subdominio que desea configurar. Por ejemplo, para configurar el subdominio “usoffers.email.weretail.com”, escriba “usoffers.email.weretail.com”.

1. Se muestra la lista de registros que se van a colocar en los servidores DNS. Copie estos registros, uno por uno o descargando un archivo CSV, y luego vaya a la solución de alojamiento de dominios para generar los registros DNS coincidentes.

   ![](assets/cname-generate-record.png)

1. Asegúrese de que todos los registros DNS de pasos anteriores se hayan generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, seleccione la primera instrucción y haga clic en **[!UICONTROL Siguiente]** para confirmar.

   Si desea crear los registros y enviar la configuración del subdominio más adelante, seleccione la segunda instrucción. A continuación, podrá reanudar la configuración del subdominio directamente desde el área **[!UICONTROL Procesando]** de la pantalla de administración de subdominios. Tenga en cuenta que el Panel de control mantendrá los registros DNS que se van a colocar en el servidor durante 30 días. Más allá de ese periodo, tendrá que configurar el subdominio desde cero.

   >[!NOTE]
   >
   >Si decide no delegar el certificado SSL a Adobe, este es el último paso de la configuración del subdominio. Haga clic en el botón **[!UICONTROL Enviar]**.

   ![](assets/cname-confirmation.png)

1. Si decide delegar el certificado de los subdominios a Adobe, los registros de certificados se generan automáticamente. Copie estos registros, uno por uno o descargando un archivo CSV, y luego vaya a la solución de alojamiento de dominios para generar los certificados coincidentes.

   ![](assets/cname-csr-generation.png)

1. Asegúrese de que todos los registros de certificados se hayan generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, seleccione la primera instrucción y haga clic en **[!UICONTROL Enviar]** para confirmar.

   ![](assets/cnames-submit.png)

Una vez enviado el subdominio, el Panel de control realizará varias comprobaciones y pasos de configuración. Para obtener más información, consulte [Comprobación y configuración de subdominios](#subdomain-checks-and-configuration).

## Comprobación y configuración de subdominios {#subdomain-checks-and-configuration}

1. Una vez enviado el subdominio, el Panel de control comprobará que señala correctamente a los registros NS de Adobe y que el registro de Inicio de autoridad (SOA) no existe para este subdominio.

   >[!NOTE]
   >
   >Tenga en cuenta que mientras se ejecuta la configuración del subdominio, otras solicitudes del Panel de control se pondrán en cola y solo se ejecutarán una vez que finalice la configuración del subdominio, para evitar problemas de rendimiento.

1. Si las comprobaciones son correctas, el Panel de control establecerá el inicio del subdominio con registros DNS, direcciones URL adicionales, bandejas de entrada, etc.

   ![](assets/subdomain7.png)

   Puede obtener más detalles acerca del progreso de la configuración haciendo clic en el botón de configuración de subdominios **[!UICONTROL Detalles]**.

   ![](assets/subdomain_audit.png)

1. Al final, se notificará al **Equipo de entrega** acerca del nuevo subdominio para auditarlo. El proceso de auditoría puede demorarse hasta 10 días hábiles después de configurarse el subdominio.

   >[!IMPORTANT]
   >
   >Las comprobaciones de entrega que se realizan incluyen bucles de comentarios y pruebas de bucles por quejas de spam. Por lo tanto, no recomendamos el uso del subdominio antes de que se haya completado la auditoría, ya que podría causar una mala reputación de subdominio.
   >
   >Sin embargo, tenga en cuenta que puede realizar operaciones relacionadas con los certificados SSL en el subdominio, incluso si la auditoría de entregabilidad todavía se está procesando.

1. Al final del proceso, los subdominios se configurarán para que funcionen con la instancia de Adobe Campaign y se crearán los elementos siguientes:

   * **El subdominio con los siguientes registros DNS**: SOA, MX, CNAME, DKIM, SPF, TXT,
   * **Subdominios adicionales** para réplica de host, recurso, páginas de seguimiento y clave de dominio,
   * **Bandeja de entrada**: Remitente, Error, Responder.

   De forma predeterminada, la bandeja de entrada Responder del Panel de control está configurada para borrar correos electrónicos y no se puede revisar. Si desea supervisar la bandeja de entrada Responder para sus campañas de marketing, no utilice esta dirección.

Puede obtener más detalles acerca del subdominio haciendo clic en los botones **[!UICONTROL Detalles del subdominio]** e **[!UICONTROL Información del remitente]**.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Resolución de problemas {#troubleshooting}

* En algunos casos, la configuración se completa, pero es posible que el subdominio no se haya verificado correctamente. El subdominio permanecerá en la lista **[!UICONTROL Configurado]** con un registro de trabajo que proporciona información sobre el error. Póngase en contacto con el Servicio de atención al cliente si tiene problemas.
* En caso de que el subdominio se muestre como “No verificado” después de configurarlo, inicie una nueva verificación del subdominio (**...** / **[!UICONTROL Verificar subdominio]**). Si aún muestra el mismo estado, la razón podría ser que hay alguna personalización en el esquema de destinatarios, que no se puede comprobar mediante procesos estándar. Intente enviar una campaña con ese subdominio.
* Si la configuración del subdominio está tardando demasiado (más de 10 días hábiles) en el paso de auditoría de la entrega, póngase en contacto con el Servicio de atención al cliente.
