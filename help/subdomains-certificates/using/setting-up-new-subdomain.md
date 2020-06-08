---
title: Configuración de un nuevo subdominio
description: Obtenga información sobre cómo configurar un nuevo subdominio para las instancias de Campaign
translation-type: ht
source-git-commit: 47b4c6abd7b41a63d881b658849ac985c72656f8
workflow-type: ht
source-wordcount: '932'
ht-degree: 100%

---


# Configuración de un nuevo subdominio {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Configuración de nuevos subdominios y administración de certificados"
>abstract="Debe configurar un nuevo subdominio y administrar los certificados SSL de los subdominios para que el inicio envíe correos electrónicos o publique páginas de aterrizaje con Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/es-ES/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Supervisión de los certificados SSL de los subdominios"

>[!IMPORTANT]
>
>La delegación de subdominios del Panel de control está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

## Delegación completa de subdominios {#full-subdomain-delegation}

El Panel de control de Campaign permite delegar completamente un subdominio a Adobe Campaign. Para realizar esto, siga los pasos a continuación.

>[!NOTE]
>
>Si la instancia seleccionada no tiene subdominios configurados previamente, el primer subdominio delegado a Adobe se convertirá en el **subdominio principal** para esa instancia y no podrá cambiarlo en el futuro.
>
>Se crearán registros DNS inversos para otros subdominios que utilicen el subdominio principal. Las direcciones de respuesta y devolución de otros subdominios se generarán desde el subdominio principal.

1. En la tarjeta **[!UICONTROL Subdomains & Certificates]**, seleccione la instancia de producción que desee y haga clic en **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >La delegación de subdominios solo está disponible para instancias de **producción** .

1. Haga clic en **[!UICONTROL Next]** para confirmar el método de delegación completo.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >El Panel de control de Campaign no admite actualmente [CNAME](#use-cnames) ni métodos personalizados.

1. Cree los subdominios y servidores de nombres deseados en la solución de hospedaje que use su organización. Para ello, copie y pegue la información del servidor de nombres de Adobe que se muestra en el asistente. Para obtener más información sobre cómo crear un subdominio en una solución de alojamiento, consulte el [tutorial en vídeo](https://video.tv.adobe.com/v/30175?captions=spa).

   >[!IMPORTANT]
   >
   >Al configurar servidores de nombres, asegúrese de **no delegar nunca su subdominio raíz a Adobe**. De lo contrario, el dominio solo podrá trabajar con Adobe. Cualquier otro uso será imposible, como, por ejemplo, enviar correos electrónicos internos a los empleados de la organización.
   >
   >Además, **no cree ningún archivo de zona independiente** para este nuevo subdominio.

   ![](assets/subdomain4.png)

   Una vez creado el subdominio con la información correspondiente del servidor de nombres de Adobe, haga clic en **[!UICONTROL Next]**.

1. Seleccione el caso de uso que desee para el subdominio:

   * **Comunicaciones de marketing**: comunicaciones con fines comerciales. Ejemplo: campañas de correo electrónico de ventas.
   * **Comunicaciones transaccionales y operativas**: las comunicaciones transaccionales contienen información destinada a completar un proceso que el destinatario ha iniciado con usted. Ejemplo: confirmación de compra, correo electrónico de restablecimiento de contraseña. Las comunicaciones de organización se refieren al intercambio de información, ideas y vistas dentro y fuera de la organización, sin fines comerciales.
   ![](assets/subdomain5.png)

   **Desglose de los subdominios según los casos de uso es una práctica recomendada para la entrega**. Al hacerlo, la reputación de cada subdominio está aislada y protegida. Por ejemplo: si el subdominio para comunicaciones de marketing termina en la lista negra de proveedores de servicio de Internet, el subdominio de comunicaciones transaccionales no se verá afectado y podrá enviar comunicaciones.

   **Puede delegar un subdominio para los casos de uso de marketing y transaccional**:

   * En los casos de uso de Marketing, los subdominios se configurarán en instancias de **MID** (fuentes medias).
   * En los casos de uso transaccional, los subdominios se configurarán en TODAS las instancias de **RT** (centro de mensajes/mensajería en tiempo real) para garantizar la conectividad. Por lo tanto, los subdominios funcionarán con todas las instancias de RT.
   >[!NOTE]
   >
   >Si utiliza Campaign Classic, el Panel de control de Campaign le permite ver qué instancias de RT/MID están conectadas a la instancia de Marketing con la que está trabajando. Para obtener más información, consulte [esta sección](../../instances-settings/using/instance-details.md).

1. Escriba el subdominio que creó en la solución de alojamiento y haga clic en **[!UICONTROL Submit]**.

   Asegúrese de añadir el **nombre completo** del subdominio que desea delegar. Por ejemplo, para delegar el subdominio &quot;usoffer.email.weretail.com&quot;, escriba &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Una vez enviado el subdominio, el Panel de control de Campaign comprobará que señala correctamente a los registros NS de Adobe y que el registro de Inicio de autoridad (SOA) no existe para este subdominio.

1. Si las comprobaciones son correctas, el Panel de control de Campaign establecerá el inicio del subdominio con registros DNS, direcciones URL adicionales, bandejas de entrada, etc. Para obtener más detalles sobre el progreso de la configuración, haga clic en el botón **[!UICONTROL Process details]**.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >En algunos casos, la delegación pasa por ahí, pero es posible que el subdominio no se haya verificado correctamente. El subdominio irá directamente a la lista **[!UICONTROL Verified subdomains]** con el estado **[!UICONTROL Unverified]** y un registro de trabajo que proporciona información sobre el error. Póngase en contacto con el Servicio de atención al cliente si tiene problemas..
   >
   >Tenga en cuenta que mientras se ejecuta la delegación de subdominios, otras solicitudes a través del Panel de control de Campaign se pondrán en cola y se gestionarán solo después de que finalice la delegación de subdominios para evitar cualquier problema de rendimiento.

Al final del proceso, los subdominios se configurarán para que funcionen con la instancia de Adobe Campaign y se crearán los elementos siguientes:

* **El subdominio** con los siguientes **registros DNS**: SOA, MX, CNAME, DKIM, SPF, TXT,
* **Subdominios adicionales** para réplica de host, recurso, páginas de seguimiento y clave de dominio,
* **Bandeja de entrada**: Remitente, Error, Responder.

>[!NOTE]
>
>De forma predeterminada, la bandeja de entrada Responder del Panel de control de Campaign está configurada para borrar correos electrónicos y no se puede revisar. Si desea supervisar la bandeja de entrada Responder para sus campañas de marketing, no utilice esta dirección.

Puede obtener más información sobre el subdominio haciendo clic en los botones **[!UICONTROL Subdomain details]** y **[!UICONTROL Sender info]**.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

>[!IMPORTANT]
>
>Después de la fase de procesamiento, debe verificar con el Servicio de atención al cliente de Adobe que se ha archivado una solicitud de auditoría para que el equipo de entrega controle el nuevo subdominio que se ha creado. El proceso de auditoría puede tardar hasta entre 3 y 10 días hábiles después de delegarse el subdominio.
>
>Las comprobaciones que se realizan incluyen bucles de comentarios y pruebas de bucles por quejas de spam. Por lo tanto, no recomendamos el uso del subdominio antes de que se haya completado la auditoría, ya que podría causar una mala reputación de subdominio.

## Uso de CNAME {#use-cnames}

El uso de CNAME para delegación de subdominios no lo ofrece el Panel de control de Campaign. Para utilizar este método, póngase en contacto con el Servicio de atención al cliente de Adobe.

**Temas relacionados:**

* [Delegación de subdominios (tutorial en vídeo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Promoción de subdominios](../../subdomains-certificates/using/subdomains-branding.md)
* [Supervisión de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)