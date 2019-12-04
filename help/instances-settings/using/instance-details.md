---
title: Detalles de instancia
description: Obtenga información sobre cómo supervisar los detalles de su instancia en el Panel de control
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Detalles de instancia {#instance-details}

>[!CAUTION]
>
>Esta función solo está disponible para instancias de Campaign Classic.

## Acerca de los detalles de instancia {#about-instance-details}

La arquitectura de instancia de Adobe Campaign Classic puede contener varios servidores para permitir la flexibilidad de las actividades de marketing. Por ejemplo, puede tener servidores de fuentes de marketing, tiempo real (o centro de mensajes) y medios que admitan su instancia.

La funcionalidad Detalles de instancia permite ver la arquitectura plana de la instancia. Además de la información del servidor, también le permite saber si la compilación de la instancia está actualizada o no, así como recomendar actualizaciones cuando sea necesario.

>[!NOTE]
>
>Recomendamos que las instancias se actualicen al menos una vez al año para evitar la degradación del rendimiento y poder aprovechar las funciones y correcciones más recientes que ofrece Adobe Campaign Classic.

**Temas relacionados:**

* [Realización de una actualización de compilación](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Actualización de Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Recuperación de información sobre las instancias {#retrieving-information-about-instances}

Para obtener información sobre los servidores conectados a las instancias, siga estos pasos:

1. Abra la **[!UICONTROL Instances Settings]** tarjeta para acceder a la **[!UICONTROL Instance Details]** ficha.

   >[!NOTE]
   >
   >Si la tarjeta Configuración de instancia no está visible en la página de inicio del Panel de control, significa que el identificador de organización de IMS no está asociado a ninguna instancia de Adobe Campaign Classic

1. Seleccione en el panel izquierdo la instancia de Campaign Classic que desee.

   >[!NOTE]
   >
   >Todas las instancias de campaña se muestran en la lista del panel izquierdo. Como la función Detalles de instancia está dedicada únicamente a instancias de Campaign Classic, se muestra el mensaje "Instancia no aplicable" si selecciona una instancia de Campaign Standard.

1. Se muestran los servidores conectados a la instancia.

   ![](assets/instance_details.png)

La información disponible es:

* **[!UICONTROL Type]**:: tipo del servidor. Los valores posibles son MKT (Marketing), MID (fuentes intermedias) y RT (mensajes del centro de mensajes / mensajes en tiempo real).
* **[!UICONTROL Name]**:: el nombre del servidor.
* **[!UICONTROL Build:]** la versión de compilación instalada en el servidor.
* **[!UICONTROL Upgrade info]**:: esta columna le informa si se requiere alguna actualización para el servidor.
   * Verde: su servidor está actualizado, no se requiere ninguna actualización.
   * Amarillo: debe considerar la posibilidad de actualizar. Le faltan las funciones y correcciones más recientes.
   * Rojo: actualice lo antes posible. Faltan nuevas funciones y es posible que el rendimiento del servidor no sea óptimo.

Si es necesario actualizar uno de los servidores, consulte [esta documentación](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) para obtener más información sobre cómo proceder.

## Preguntas frecuentes {#common-questions}

**No veo el servidor MID en la arquitectura de mi instancia, ¿significa que mis instancias no funcionan correctamente? ¿Necesito la instancia de RT para algo que no puedo hacer hoy?**

Su propia instancia puede tener un aspecto muy diferente y es posible que no tenga todos los tipos de servidores, o que tenga varios del mismo servidor. No tener un tipo de servidor u otro no significa que no pueda enviar un mensaje en tiempo real ni realizar otros tipos de actividades. Puede solicitar capacidad adicional del servidor, se aplicarán tarifas adicionales.

Póngase en contacto con el Servicio de atención al cliente si cree que algunos servidores no se muestran en la página "Detalles de la instancia". Asegúrese de anotar la URL de instancia específica en el mensaje.
