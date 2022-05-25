---
product: campaign
solution: Campaign
title: Añadir instancias MID/RT (modelo híbrido)
description: Aprenda a añadir instancias de MID/RT para el Panel de control de Campaign con el modelo de alojamiento híbrido.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 2458263ef5981a16d983912b498e320501df7889
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 3%

---


# Añadir instancias MID/RT (modelo híbrido)

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="Cuentas externas"
>abstract="En esta pantalla, los clientes con modelo de alojamiento híbrido pueden proporcionar su URL de instancia de MID/RT configurada en la instancia de marketing en Panel de control de Campaign, para aprovechar las capacidades de Panel de control de Campaign."

El Panel de control de Campaign permite a los clientes con un modelo de alojamiento híbrido aprovechar las funcionalidades específicas del Panel de control de Campaign. Para ello, deben proporcionar la URL de instancia de MID/RT configurada en su instancia de marketing en Panel de control de Campaign.

Para obtener más información sobre los modelos de alojamiento, consulte [documentación del Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Añadir una instancia de MID/RT {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="La dirección URL de la instancia, que se puede encontrar en la consola de cliente de Campaign en el menú Administration > Platform > External Accounts ."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Operador"
>abstract="ID del operador proporcionado después del aprovisionamiento inicial por el administrador de Adobe."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Contraseña"
>abstract="Contraseña del operador proporcionada después del aprovisionamiento inicial por el administrador de Adobe."

Los clientes híbridos deben conectarse al Panel de control de Campaign a través del Experience Cloud. Al acceder al Panel de control de Campaign por primera vez, solo se muestran dos tarjetas en la página principal.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>En caso de que encuentre algún problema para acceder al Panel de control de Campaign, lo más probable es que la instancia de marketing aún no esté asignada a su ID de organización. Póngase en contacto con el Servicio de atención al cliente para completar esta configuración y continuar. Si la conexión se realiza correctamente, verá la página de inicio del Panel de control de Campaign.

Para poder acceder a las funcionalidades del Panel de control de Campaign, debe proporcionar la información de la instancia de MID/RT en la **[!UICONTROL Instances Settings]** tarjeta. Para realizar esto, siga los pasos a continuación.

1. En el **[!UICONTROL Instances Settings]** seleccione la **[!UICONTROL External Accounts]** pestaña .

1. Seleccione la instancia de marketing que desee en la lista desplegable y haga clic en **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Proporcione información sobre la instancia de MID/RT que desea añadir.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: URL de la instancia, que se puede encontrar en la consola del cliente de Campaign en la **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]** para abrir el Navegador.

      ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Credenciales del operador proporcionadas después del aprovisionamiento inicial por el administrador de Adobe.

      >[!NOTE]
      >
      >Si estos detalles no están disponibles, póngase en contacto con el Servicio de atención al cliente.

1. Haga clic en **[!UICONTROL Save]** para confirmar.

Al añadir la URL de MID/RT, se activa un proceso asincrónico para validar la corrección de las URL. Este proceso puede tardar unos minutos. Hasta que se valide la URL de instancia de MID/RT, el trabajo estará pendiente. Solo una vez completada la validación, puede acceder a las funciones principales del Panel de control de Campaign.

![](assets/external-account-pending.png)

Puede quitar o desactivar una URL de instancia de MID/RT en cualquier momento seleccionándola en la lista.

![](assets/external-account-edit.png)

Tenga en cuenta que puede supervisar cualquier acción realizada en la variable **[!UICONTROL External Accounts]** en una URL de instancia de MID/RT desde **[!UICONTROL Job Logs]**:

![](assets/external-account-logs.png)

## Capacidades disponibles para clientes híbridos {#capabilities}

Una vez que se añade una instancia de MID/RT al Panel de control de Campaign, puede aprovechar las funciones que se enumeran a continuación:

* [Supervisión de los contactos y eventos clave](../../service-events/service-events.md)
* [Ver los detalles de la instancia](../../instances-settings/using/instance-details.md),
* [Añadir direcciones IP a la lista de permitidos](../../instances-settings/using/ip-allow-listing-instance-access.md) (para instancias de RT),
* [Ver información sobre subdominios delegados](../../subdomains-certificates/using/monitoring-subdomains.md),
* [Ver información sobre certificados SSL](../../subdomains-certificates/using/monitoring-ssl-certificates.md).