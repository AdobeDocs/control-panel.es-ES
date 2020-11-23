---
product: campaign
solution: Campaign
title: Configuración de un nuevo subdominio
description: Obtenga información sobre cómo configurar un nuevo subdominio para las instancias de Campaign
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 47%

---


# Configuración de un nuevo subdominio {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Configuración de nuevos subdominios y administración de certificados"
>abstract="Debe configurar un nuevo subdominio y administrar los certificados SSL de los subdominios para que el inicio envíe correos electrónicos o publique páginas de aterrizaje con Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/es-ES/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Supervisión de los certificados SSL de los subdominios"

>[!IMPORTANT]
>
>La configuración de subdominios del Panel de control de Campaign está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

Esta página proporciona información sobre cómo configurar nuevos subdominios mediante delegación de subdominios completa o CNAME. En esta sección se presentan los conceptos globales sobre estos dos métodos: [Marca de subdominios](../../subdomains-certificates/using/subdomains-branding.md).

**Temas relacionados:**

* [Supervisión de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)

## Lectura obligatoria {#must-read}

### Selección de instancias

Subdomain configuration is available for **production** instances only.

Si la instancia seleccionada en el asistente no tiene subdominios de configuración anteriores, el primer subdominio configurado se convertirá en el subdominio **** principal de esa instancia y no podrá cambiarlo en el futuro.

Como resultado, se crearán registros **DNS** inversos para otros subdominios que usen este subdominio principal. **Las direcciones de respuesta y devolución de otros subdominios se generarán desde el subdominio principal.**

### Configuración de servidores de nombres

Al configurar servidores de nombres, asegúrese de **no delegar nunca su subdominio raíz a Adobe**. De lo contrario, el dominio solo podrá trabajar con Adobe. Cualquier otro uso será imposible, como, por ejemplo, enviar correos electrónicos internos a los empleados de la organización.

Además, **no cree ningún archivo de zona independiente** para este nuevo subdominio.

## Delegación completa de subdominios {#full-subdomain-delegation}

Para delegar completamente un subdominio a Adobe Campaign, siga los pasos a continuación.

![](assets/do-not-localize/how-to-video.png) Descubrir esta función en vídeo mediante [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=en#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=en#subdomains-and-certificates)

1. En la tarjeta **[!UICONTROL Subdomains & Certificates]**, seleccione la instancia de producción que desee y haga clic en **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

1. Haga clic en **[!UICONTROL Next]** para confirmar el método de delegación completo.

   ![](assets/subdomain3.png)

1. Cree los subdominios y servidores de nombres deseados en la solución de hospedaje que use su organización. Para ello, copie y pegue la información del servidor de nombres de Adobe que se muestra en el asistente. Para obtener más información sobre cómo crear un subdominio en una solución de alojamiento, consulte el [tutorial en vídeo](https://video.tv.adobe.com/v/30175?captions=spa).

   ![](assets/subdomain4.png)

1. Una vez creado el subdominio con la información correspondiente del servidor de nombres de Adobe, haga clic en **[!UICONTROL Next]**.

1. Si seleccionó una instancia de Campaign Classic, seleccione el caso de uso que desee para el subdominio: **Comunicaciones** de marketing o comunicaciones **** transaccionales y operativas. Los conceptos globales sobre los casos de uso de los subdominios se presentan en [esta sección](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/subdomain5.png)

1. Escriba el subdominio que creó en la solución de alojamiento y haga clic en **[!UICONTROL Submit]**.

   Asegúrese de añadir el **nombre completo** del subdominio que desea delegar. Por ejemplo, para delegar el subdominio &quot;usoffer.email.weretail.com&quot;, escriba &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

Una vez enviado el subdominio, el Panel de control de Campaign realizará varias comprobaciones y pasos de configuración. Para obtener más información sobre esto, consulte Comprobaciones y configuración [de subdominios](#subdomain-checks-and-configuration).

## Configuración del subdominio mediante CNAME {#use-cnames}

Para configurar un subdominio mediante CNAME, siga los pasos a continuación.

![](assets/do-not-localize/how-to-video.png) Descubrir esta función en vídeo mediante [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=en#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=en)

1. En la tarjeta **[!UICONTROL Subdomains & Certificates]**, seleccione la instancia de producción que desee y haga clic en **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

1. Select the **[!UICONTROL CNAME]** method, then click **[!UICONTROL Next]**.

   ![](assets/cname-method-selection.png)

1. Si seleccionó una instancia de Campaign Classic, seleccione el caso de uso que desee para el subdominio: **Comunicaciones** de marketing o comunicaciones **** transaccionales y operativas. Los conceptos globales sobre los casos de uso de los subdominios se presentan en [esta sección](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/cname-use-case.png)

1. Escriba el subdominio que creó en la solución de alojamiento y haga clic en **[!UICONTROL Next]**.

   Make sure you fill in the **full name** of the subdomain to setup. Por ejemplo, para configurar el subdominio &quot;usoffer.email.weretail.com&quot;, escriba &quot;usoffer.email.weretail.com&quot;.

   ![](assets/cname-submit.png)

1. Se muestra la lista de los registros que se van a colocar en los servidores DNS. Copie estos registros, uno por uno o descargando un archivo CSV, luego navegue a la solución de alojamiento de dominios para generar los registros DNS coincidentes.

   ![](assets/cname-generate-record.png)

1. Asegúrese de que todos los registros DNS de pasos anteriores se hayan generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, seleccione la primera instrucción y haga clic en **[!UICONTROL Submit]** para confirmar.

   ![](assets/cname-confirmation.png)

   >[!NOTE]
   >
   >Si desea crear los registros y enviar la configuración del subdominio más adelante, seleccione la segunda instrucción y haga clic en **[!UICONTROL Submit later]**. A continuación, podrá reanudar la configuración de subdominio directamente desde el **[!UICONTROL Processing]** área de la pantalla de administración de subdominios.
   >
   >Tenga en cuenta que los registros DNS que se van a colocar en el servidor se conservarán por Panel de control de Campaign 30 días. Más allá de ese período, tendrá que configurar el subdominio desde cero.

Una vez enviado el subdominio, el Panel de control de Campaign realizará varias comprobaciones y pasos de configuración. Para obtener más información sobre esto, consulte Comprobaciones y configuración [de subdominios](#subdomain-checks-and-configuration).

## Comprobación y configuración de subdominios {#subdomain-checks-and-configuration}

1. Una vez enviado un subdominio, el Panel de control de Campaign comprobará que señala correctamente a los registros NS de Adobe y que el registro de Inicio de autoridad (SOA) no existe para este subdominio.

   >[!NOTE]
   >
   >Tenga en cuenta que mientras se ejecuta la configuración de subdominio, otras solicitudes a través del Panel de control de Campaign se introducirán en una cola y se realizarán solamente después de que se complete la configuración del subdominio, para evitar problemas de rendimiento.

1. Si las comprobaciones son correctas, el Panel de control de Campaign establecerá el inicio del subdominio con registros DNS, direcciones URL adicionales, bandejas de entrada, etc.

   ![](assets/subdomain7.png)

   You can get more details on the configuration progress by clicking the subdomain configuration **[!UICONTROL Details]** button.

   ![](assets/subdomain_audit.png)

1. Al final, se notificará al **equipo de entrega** del nuevo subdominio para auditarlo. El proceso de auditoría puede tardar hasta 10 días laborables después de configurar el subdominio.

   >[!IMPORTANT]
   >
   >Las comprobaciones de la capacidad de entrega que se realizan incluyen los bucles de comentarios y las pruebas de los bucles de denuncia de spam. Por lo tanto, no recomendamos el uso del subdominio antes de que se haya completado la auditoría, ya que podría causar una mala reputación de subdominio.

1. Al final del proceso, los subdominios se configurarán para que funcionen con la instancia de Adobe Campaign y se crearán los elementos siguientes:

   * **El subdominio con los siguientes registros DNS**: SOA, MX, CNAME, DKIM, SPF, TXT,
   * **Subdominios adicionales** para réplica de host, recurso, páginas de seguimiento y clave de dominio,
   * **Bandeja de entrada**: Remitente, Error, Responder.

   De forma predeterminada, la bandeja de entrada Responder del Panel de control de Campaign está configurada para borrar correos electrónicos y no se puede revisar. Si desea supervisar la bandeja de entrada Responder para sus campañas de marketing, no utilice esta dirección.

Puede obtener más información sobre el subdominio haciendo clic en los botones **[!UICONTROL Subdomain details]** y **[!UICONTROL Sender info]**.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Resolución de problemas {#troubleshooting}

* En algunos casos, la configuración de subdominios pasa, pero es posible que el subdominio no se verifique correctamente. El subdominio permanecerá en la lista **[!UICONTROL Configured]** con un registro de trabajos que proporciona información sobre el error. Póngase en contacto con el Servicio de atención al cliente si tiene problemas.
* Si el subdominio se muestra como &quot;Unverified&quot; después de configurarse, inicie una nueva verificación de subdominio (**...**/**[!UICONTROL Verify subdomain]**). Si aún muestra el mismo estado, la razón podría ser que hay alguna personalización en el esquema de destinatarios, que no se puede comprobar mediante procesos estándar. Intente enviar una campaña con ese subdominio.
* Si la configuración del subdominio está tardando demasiado (más de 10 días hábiles) en el paso de auditoría de la entrega, póngase en contacto con Atención al cliente.
