---
product: campaign
solution: Campaign
title: Preguntas frecuentes sobre el Panel de control de Campaign
description: Preguntas frecuentes relacionadas con el Panel de control de Campaign
feature: Panel de control de Campaign
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
translation-type: ht
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: ht
source-wordcount: '631'
ht-degree: 100%

---

# Preguntas frecuentes {#faq}

## ID de la organización IMS {#ims-org-id}

**¿Qué es un ID de organización de IMS?**

Se trata de un ID exclusivo que se le proporciona a su instancia cuando inicia sesión por primera vez en Adobe Experience Cloud. Debe tener el formato siguiente: xxx@AdobeOrg.

Para obtener más información, consulte la [documentación de Adobe Experience Cloud](https://marketing.adobe.com/resources/help/es_ES/mcloud/organizations.html).

**¿Dónde puedo encontrar mi ID de organización de IMS?**

Una forma es ir a la [Página de inicio de Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Encontrará su ID de organización de IMS en la parte inferior de la sección **[!UICONTROL Quick Access]** de Administración. Puede encontrar información más detallada en la [documentación de Adobe Experience Cloud](https://marketing.adobe.com/resources/help/es_ES/mcloud/organizations.html).

La otra forma es iniciar **Admin Console**. El ID de organización de IMS será visible en la dirección URL y debe tener un aspecto similar al siguiente: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**¿Por qué necesito saber mi ID de organización de IMS?**

Para administrar la configuración de su instancia, queremos asegurarnos de que obtiene la información adecuada de la instancia correcta en caso de que utilice varias instancias para su compañía.

**¿Qué sucede si tengo varios ID de organización de IMS?**

Puede tener más de un ID de organización de IMS si tiene acceso a varias soluciones de Adobe. En este caso, el ID de organización de IMS correcto que debe utilizar es el que ve debajo de la instancia de Adobe Campaign.

>[!NOTE]
>
>Si tiene el mismo ID de organización de IMS para Adobe Campaign y Adobe Analytics, no hay problema. Tener un ID de organización de IMS para Analytics y Campaign es un requisito si tiene pensado integrar las soluciones con el fin de aprovechar los casos de uso complejos, como el abandono del carro de compras (AA + AC).
>
>Si tiene diferentes ID de organización de IMS para Adobe Campaign y Adobe Analytics, póngase en contacto con el Servicio de atención al cliente para alinearlos.

**¿Cómo puedo saber si mi instancia de Adobe Campaign está alojada en AWS o no?**

Para comprobar si la instancia está alojada en AWS, siga estos pasos:

1. Recupere la dirección URL de inicio de sesión. Es la dirección URL que utiliza para iniciar sesión en la instancia de Campaign y termina principalmente con “.campaign.adobe.com” o “.neolane.net”.
1. Abra el terminal y, a continuación, ejecute una operación **[!DNL nslookup]** en la dirección URL de inicio de sesión.

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

1. Compruebe el valor “name” en el resultado devuelto. Si contiene “amazonaws.com”, significa que su instancia está alojada en AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Si desea realizar la migración a AWS, póngase en inicio con el administrador de éxito del cliente.

## Panel de control de Campaign{#control-panel}

**¿Qué es el Panel de control de Campaign?**

El Panel de control de Campaign permite a los administradores de productos administrar directamente diversas configuraciones y supervisar la capacidad de los servidores SFTP conectados a Adobe Campaign.

**¿Cuáles son algunas de las capacidades actuales del Panel de control de Campaign?**

El Panel de control de Campaign le permite hacer el seguimiento del almacenamiento y las direcciones IP de lista de permitidos, y administrar las claves SSH de sus servidores SFTP por su cuenta en función de sus necesidades y otras acciones.

Para obtener más información, consulte la documentación de acciones admitidas por el Panel de control de Campaign.

**¿El Panel de control de Campaign solo sirve para Adobe Campaign?**

Sí, solo podrá administrar la configuración de Adobe Campaign en el Panel de control de Campaign.

**¿Puedo utilizar el Panel de control de Campaign?**

El Panel de control de Campaign solo está abierto a los administradores de productos de nuestros clientes actuales que tienen Adobe Campaign alojado en AWS. Tenga en cuenta que aún no se admiten entornos híbridos.

Si no es administrador, pero desea acceder a él, póngase en contacto con el administrador del producto para que le ayude a agregarlo como administrador.

**¿Cómo puedo acceder al Panel de control de Campaign?**

Siga las instrucciones detalladas que se encuentran en la documentación de Acceso al Panel de control de Campaign.

**¿Se cobra una tarifa adicional para utilizar el Panel de control de Campaign?**

No, no hay costo adicional si usted es cliente actual de Adobe Campaign.
