---
title: Preguntas más frecuentes sobre el Panel de control
description: Cuestiones comunes relacionadas con el Panel de control
translation-type: tm+mt
source-git-commit: ddf4ca24c1583e388c07aae110522627220d5e66

---


# Preguntas más frecuentes {#faq}

## ID de organización IMS {#ims-org-id}

**¿Qué es un ID de organización de IMS?**

Se trata de un ID exclusivo que se le proporciona a su instancia cuando inicia sesión por primera vez en Adobe Experience Cloud. Debe tener el formato siguiente: xxx@AdobeOrg.

Para obtener más información, consulte la documentación [de](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)Adobe Experience Cloud.

**¿Dónde puedo encontrar mi ID de organización de IMS?**

One way is to navigate to [Adobe Experience Cloud Home](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. You will find your IMS Org ID at the bottom of Administration**[!UICONTROL Quick Access]** section. Puede encontrar información más detallada en la [documentación de Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

La otra manera es iniciar **Admin Console**. El ID de organización de IMS estará visible en la dirección URL, debería tener un aspecto similar al siguiente: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**¿Por qué necesito saber mi identificador de organización de IMS?**

Para que pueda administrar la configuración de su instancia, queremos asegurarnos de que obtiene la información adecuada para la instancia correcta en caso de que utilice varias instancias para su empresa.

**¿Qué sucede si tengo varios ID de organización de IMS?**

Puede tener más de un ID de organización de IMS si tiene acceso a varias soluciones de Adobe. En este caso, el ID de organización de IMS correcto que debe utilizar es el que ve en la instancia de Adobe Campaign.

>[!NOTE]
>
>Si tiene el mismo ID de organización de IMS para Adobe Campaign y Adobe Analytics, esto es genial. Tener un ID de organización de IMS entre Analytics y Campaign es un requisito si planea integrar las soluciones para aprovechar los casos de uso complejos como el abandono del carro de compras (para AA + AC).
>
>Si tiene diferentes ID de organización de IMS para Adobe Campaign y Adobe Analytics, póngase en contacto con el Servicio de atención al cliente para alinearlos.

**¿Cómo puedo saber si mi instancia de Adobe Campaign está alojada en AWS o no?**

Para comprobar si la instancia está alojada en AWS, siga estos pasos:

1. Recupere la dirección URL de inicio de sesión. Es la dirección URL que utiliza para iniciar sesión en la instancia de Campaign. La mayoría de las veces termina con &quot;.campaign.adobe.com&quot; o&quot;.neolane.net&quot;.
1. Abra el terminal y, a continuación, ejecute una **[!DNL nslookup]**operación en la dirección URL de inicio de sesión.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. La respuesta devuelve información sobre la instancia.

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. Ejecute una operación **nslookup** en la dirección IP devuelta.

   `doe-macOS% nslookup 12.34.567.89`

1. Compruebe el valor &quot;name&quot; en el resultado devuelto. Si contiene &quot;amazonaws.com&quot;, significa que su instancia está alojada en AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Si desea migrar a AWS, póngase en contacto con el administrador de éxito del cliente para iniciar el proceso.

## Panel de control {#control-panel}

**¿Qué es el Panel de control?**

El Panel de control permite a los administradores de productos administrar directamente varios ajustes y supervisar la capacidad de los servidores SFTP conectados a Adobe Campaign.

**¿Cuáles son algunas de las capacidades actuales del Panel de control?**

El Panel de control le permite rastrear el almacenamiento de información, las direcciones IP de la lista blanca y administrar las claves SSH para sus servidores SFTP por su cuenta en función de sus necesidades y otras acciones.

Para obtener más información, consulte la documentación de acciones admitidas por el Panel de control.

**¿El Panel de control solo está disponible para Adobe Campaign?**

Sí, solo podrá administrar la configuración de Adobe Campaign en el Panel de control.

**¿Puedo utilizar el Panel de control?**

El Panel de control solo está abierto a los administradores de productos de nuestros clientes actuales que tienen Adobe Campaign alojado en AWS.

Si no es administrador, pero desea acceder a él, póngase en contacto con el administrador del producto para que le ayude a agregarlo como administrador.

**¿Cómo puedo acceder al Panel de control?**

Siga las instrucciones detalladas que se encuentran en la documentación de Acceso al Panel de control.

**¿Existe una tarifa adicional para utilizar el Panel de control?**

No, no hay ningún costo adicional si es cliente actual de Adobe Campaign.
