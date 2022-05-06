---
product: campaign
solution: Campaign
title: Conectar instancias de MID/RT
description: Obtenga información sobre cómo conectar instancias de MID/RT al Panel de control de Campaign.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 1b712300bd7a1ef8dc784fa977f938bacc4c5e5b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 7%

---


# Conectar instancias de MID/RT

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="Detalles del subdominio"
>abstract="En esta pantalla, los clientes con un modelo de alojamiento híbrido pueden proporcionar sus instancias de MID/RT presentes en su instancia de marketing para realizar acciones específicas en Panel de control de Campaign."

El Panel de control de Campaign permite a los clientes con un modelo de alojamiento híbrido realizar acciones específicas en Panel de control de Campaign al proporcionar sus instancias de MID/RT presentes en su instancia de marketing. Para obtener más información sobre los modelos de alojamiento, consulte [documentación del Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Conectar una instancia de MID/RT {#connect}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Detalles del subdominio"
>abstract="ID del operador utilizado en la consola de cliente para añadir la instancia MID/RT en la instancia de marketing."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Detalles del subdominio"
>abstract="Contraseña del operador utilizado en la consola de cliente para añadir la instancia MID/RT en la instancia de marketing."

Para proporcionar una instancia de MID/RT en el Panel de control de Campaign, siga estos pasos:

1. En el **[!UICONTROL Instances Settings]** seleccione la **[!UICONTROL External Accounts]** pestaña .

1. Seleccione la instancia de marketing en la lista desplegable y haga clic en **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Proporcione información sobre la instancia MID/RT para conectarse:
   * **[!UICONTROL URL]**: URL de la instancia,
   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Credenciales del operador utilizado en la consola de cliente para agregar la instancia MID/RT en la instancia de marketing.

   ![](assets/external-account-add.png)

1. Haga clic en **[!UICONTROL Save]** para confirmar.

La instancia ahora está conectada al Panel de control de Campaign. Puede quitar o desactivar una conexión en cualquier momento seleccionándola en la lista.

![](assets/external-account-edit.png)

## Funcionalidades disponibles para instancias de MID/RT {#capabilities}

Una vez que una instancia de MID/RT está conectada al Panel de control de Campaign, puede aprovechar las funciones que se enumeran a continuación para monitorearla:

* [Ver los detalles de la instancia](../../instances-settings/using/instance-details.md),
* [Añada direcciones IP a la lista de permitidos para acceder a sus instancias](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [Ver información sobre subdominios delegados](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [Ver información sobre certificados SSL](../../subdomains-certificates/using/monitoring-ssl-certificates.md).
