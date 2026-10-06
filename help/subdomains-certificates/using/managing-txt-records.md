---
product: campaign
solution: Campaign
title: Añadir registros de verificación de sitios de Google para un subdominio
description: Descubra cómo añadir un registro de verificación de sitios de Google para un subdominio a fin de verificar la propiedad del dominio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
TQID: 'https://experienceleague.adobe.com/TtF1W0tOklUuEpihvsYlxdszEujRrDXv-Ar0y3c7QX8'
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
source-wordcount: '323'
ht-degree: 100%
---
# Adición de registros de verificación del sitio Google {#adding-a-google-txt-record}

Para garantizar altas tasas de mensajes en bandeja de entrada y bajas tasas de spam, algunos servicios como Google requieren que agregue un registro TXT a la configuración de su dominio para verificar que es el propietario del dominio.

Actualmente, Gmail es uno de los proveedores de direcciones de correo electrónico más populares. Para garantizar la buena entrega y el envío correcto de correos electrónicos a las direcciones de Gmail, Adobe Campaign le permite agregar registros TXT de verificación de sitios de Google especiales a sus subdominios para asegurar que se verifican.

Para agregar un registro TXT de Google al subdominio utilizado para enviar direcciones de Gmail por correo electrónico, siga estos pasos:

1. En la lista de subdominios, haga clic en el botón de los tres puntos situado junto al subdominio deseado y seleccione **[!UICONTROL Detalles del subdominio]**.

1. Haga clic en el botón **[!UICONTROL Añadir registro TXT]**, y, a continuación, seleccione **[!UICONTROL Verificación de sitios de Google]** en la lista desplegable **[!UICONTROL Tipo de registro]**.

1. Introduzca el valor generado en las herramientas de administración de G Suite. Para obtener más información al respecto, consulte la [Ayuda de administración de G Suite](https://support.google.com/a/answer/183895).

   ![](assets/txt_addtxt.png)

1. Haga clic en el botón **[!UICONTROL Añadir]** para confirmar.

   ![](assets/txt_txtadded.png)

Una vez agregado el registro TXT, Google debe verificarlo. Para ello, vaya a las herramientas de administración de G Suite y, a continuación, inicie el paso de verificación (consulte la [Ayuda de administración de G Suite](https://support.google.com/a/answer/183895)).

Para eliminar un registro, selecciónelo en la lista de registros y haga clic en el botón Eliminar.

>[!NOTE]
>
>El único registro que puede eliminar de la lista de registros DNS es el que agregó anteriormente (en nuestro caso, el registro TXT de Google).

![](assets/do-not-localize/how-to-video.png) Descubra esta funcionalidad en vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=es#subdomains-and-certificates) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=es#subdomains-and-certificates)
