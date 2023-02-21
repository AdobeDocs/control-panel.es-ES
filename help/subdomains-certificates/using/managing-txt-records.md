---
product: campaign
solution: Campaign
title: Administración de registros TXT
description: Obtenga información sobre cómo administrar registros TXT para la verificación de la propiedad del dominio.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 95%

---

# Administración de registros TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Administración de registros TXT"
>abstract="Algunos servicios como Google requieren que añada un registro TXT a la configuración de su dominio para comprobar que es el propietario de este."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=es" text="Configuración de un nuevo subdominio"

## Acerca de los registros TXT {#about-txt-records}

Los registros TXT son un tipo de registros DNS que se utilizan para proporcionar información de texto sobre un dominio y que pueden leer fuentes externas.

Para garantizar altas tasas de mensajes en bandeja de entrada y bajas tasas de spam, algunos servicios como Google requieren que agregue un registro TXT a la configuración de su dominio para verificar que es el propietario del dominio.

Actualmente, Gmail es uno de los proveedores de direcciones de correo electrónico más populares. Para garantizar la buena entrega y el envío correcto de correos electrónicos a las direcciones de Gmail, Adobe Campaign le permite agregar registros TXT de verificación de sitios de Google especiales a sus subdominios para asegurar que se verifican.

![](assets/do-not-localize/how-to-video.png) Descubra esta función en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates)

## Adición de un registro TXT de Google para un subdominio {#adding-a-google-txt-record}

Para agregar un registro TXT de Google al subdominio utilizado para enviar direcciones de Gmail por correo electrónico, siga estos pasos:

1. Vaya a la tarjeta **[!UICONTROL Subdomain and Certificates]**.

1. Seleccione la instancia y, a continuación, abra los detalles del subdominio al que desea agregar un registro DNS.

   ![](assets/txt_subdomaindetails.png)

1. Haga clic en el botón **[!UICONTROL Add TXT record]** y, a continuación, introduzca el valor generado en las herramientas de administración de G Suite. Para obtener más información al respecto, consulte la [Ayuda de administración de G Suite](https://support.google.com/a/answer/183895).

   ![](assets/txt_addtxt.png)

1. Haga clic en el botón **[!UICONTROL Add]** para confirmar.

   ![](assets/txt_txtadded.png)

Una vez agregado el registro TXT, Google debe verificarlo. Para ello, vaya a las herramientas de administración de G Suite y, a continuación, inicie el paso de verificación (consulte la [Ayuda de administración de G Suite](https://support.google.com/a/answer/183895)).

Para eliminar un registro, selecciónelo en la lista de registros y haga clic en el botón Eliminar.

>[!NOTE]
>
>El único registro que puede eliminar de la lista de registros DNS es el que agregó anteriormente (en nuestro caso, el registro TXT de Google).
