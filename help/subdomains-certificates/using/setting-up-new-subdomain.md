---
title: Configuración de un nuevo subdominio
description: Obtenga información sobre cómo configurar un nuevo subdominio para las instancias de campaña
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# Configuración de un subdominio {#setting-up-subdomain}

El Panel de control permite delegar completamente un subdominio a Adobe Campaign. Para ello, siga los pasos detallados a continuación.

>[!NOTE]
>
>El uso de CNAME para delegación de subdominios no es compatible con el Panel de control. For more on this method, refer to [this page](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

1. En la **[!UICONTROL Subdomains & Certificates]**tarjeta, seleccione la instancia que desee y haga clic en el**[!UICONTROL Setup new subdomain]** botón.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >El **[!UICONTROL Setup new subdomain]**botón solo está disponible para instancias de producción.

1. Seleccione el **[!UICONTROL Delegation to Adobe]**método y haga clic en**[!UICONTROL Next]**.

   ![](assets/subdomain3.png)

1. Cree el subdominio que desee en la solución de hospedaje utilizada por su organización. Para ello, copie la información del servidor de nombres de Adobe que se muestra en el asistente y péguela en la solución de alojamiento.

   Para obtener más información sobre cómo crear un subdominio en una solución de alojamiento, consulte el vídeo del tutorial accesible desde el asistente.

   ![](assets/subdomain4.png)

   Una vez creado el subdominio con la información correspondiente del servidor de nombres de Adobe, haga clic en **[!UICONTROL Next]**.

1. Seleccione el caso de uso que desee para el subdominio:

   * **Comunicaciones** de marketing: comunicaciones destinadas a fines comerciales. Ejemplo: campaña de correo electrónico de ventas.
   * **Comunicaciones** transaccionales y operativas: las comunicaciones transaccionales contienen información destinada a completar un proceso que el destinatario ha iniciado con usted. Ejemplo: confirmación de compra, correo electrónico de restablecimiento de contraseña. Las comunicaciones de organización se refieren al intercambio de información, ideas y opiniones dentro y fuera de la organización, sin fines comerciales.
   Desglosar los subdominios de este modo es una práctica recomendada para la entrega. Al hacerlo, la reputación de cada subdominio está aislada y protegida. Por ejemplo, si los proveedores de servicios de Internet acaban bloqueando el subdominio de comunicaciones de marketing, el subdominio de comunicaciones de transacción no se verá afectado y podrá seguir enviando comunicaciones.

   ![](assets/subdomain5.png)

   >[!NOTE]
   >
   >Sólo puede seleccionar un caso de uso que se haya configurado para su instancia. Si la instancia solo se ha configurado para &quot;Comunicaciones de marketing&quot;, no podrá seleccionar el caso de uso &quot;Comunicaciones de transacción y operación&quot;.

1. Introduzca el subdominio que ha creado en la solución de alojamiento con la información del servidor de nombres de Adobe y, a continuación, haga clic en **[Enviar]**.

   >[!NOTE]
   >
   > Asegúrese de completar el subdominio **completo** que desea delegar. Por ejemplo, para delegar el subdominio &quot;usoffer.email.weretail.com&quot;, escriba &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Una vez que se envía el subdominio, el Panel de control realizará varias operaciones para configurar el subdominio y comprobar que señala correctamente a la instancia de Campaign (creación de registros de espacio de nombres, configuración de instancia de Campaign, verificación de registros de Start of Authority, etc.).

   Puede obtener más detalles sobre el progreso de la configuración en cualquier momento haciendo clic en el **[!UICONTROL Process details]**botón.

   ![](assets/subdomain7.png)

¿Qué obtienes al final del proceso?
* Subdominio con los siguientes registros DNS: SOA, MX, CNAME, DKIM, SPF, TXT.
* Subdominios adicionales a réplica de host, recurso, páginas de seguimiento y dominio
* Bandeja de entrada: remitente, error, respuesta
* En última instancia, los subdominios se configurarán para que funcionen con la instancia de Adobe Campaign
