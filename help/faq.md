---
product: campaign
solution: Campaign
title: Preguntas frecuentes sobre el Panel de control
description: Preguntas frecuentes relacionadas con el Panel de control
feature: Control Panel
role: Admin
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: 98cf425548884c3a5e503c35ce5ea5b7ceaee67f
workflow-type: ht
source-wordcount: '719'
ht-degree: 100%

---

# Preguntas frecuentes {#faq}

## Panel de control {#control-panel}

### ¿Qué es el Panel de control?

El Panel de control permite a los administradores de productos administrar directamente diversas configuraciones y supervisar la capacidad de los servidores SFTP conectados a Adobe Campaign.

### ¿Cuáles son algunas de las capacidades actuales del Panel de control?

El Panel de control le permite hacer el seguimiento del almacenamiento y las direcciones IP de lista de permitidos, y administrar las claves SSH de sus servidores SFTP por su cuenta en función de sus necesidades y otras acciones.

Para obtener más información, consulte la documentación de acciones admitidas por el Panel de control.

### ¿Hay algunas funciones que aún no son compatibles con Campaign v8, pero que están disponibles en Campaign Classic v7?{#v8-restrictions}

No. Todas las funciones disponibles en la versión 7 de Campaign ahora también están disponibles mediante el Panel de control en la versión 8 de Campaign, incluidas las funciones relacionadas con la administración de subdominios y certificados.

### ¿El Panel de control solo sirve para Adobe Campaign?

Sí, solo podrá administrar la configuración de Adobe Campaign en el Panel de control.

### ¿Puedo utilizar el Panel de control?

El Panel de control solo está disponible para los administradores de productos de nuestros clientes actuales que tengan Adobe Campaign instalado en AWS.

El Panel de control permite a los clientes con un modelo de alojamiento híbrido aprovechar las funcionalidades específicas del Panel de control. Para ello, deben proporcionar la dirección URL de instancia MID/RT configurada en su instancia de marketing en el Panel de control. [Más información](instances-settings/using/external-accounts.md)

Si no es administrador, pero desea acceder a él, póngase en contacto con el administrador del producto para que le ayude a agregarlo como administrador.

### Como usuario Campaign Classic v7, ¿cuáles son las condiciones para acceder al Panel de control? {#v7-restrictions}

El acceso al Panel de control está restringido a los usuarios administradores. [Más información](discover/using/managing-permissions.md).

Para la versión 7 de Campaign, tenga en cuenta que la instancia debe estar alojada en Amazon Web Services (AWS) y actualizarse a la última [versión estable de Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=es#rn-statuses) o la versión 9032 o superior. Aprenda a comprobar la versión 7 de Campaign Classic en [esta sección](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=es#getting-your-campaign-version). Para comprobar si la instancia de Campaign Classic está alojada en AWS, siga los pasos que se detallan en [esta sección](#hosted-aws).

### ¿Cómo puedo acceder al Panel de control?

Siga las instrucciones detalladas que se encuentran en la documentación de Acceso al Panel de control.

### ¿Se cobra una tarifa adicional para utilizar el Panel de control?

No, no hay costo adicional si usted es cliente actual de Adobe Campaign.

## ID de la organización {#ims-org-id}

### ¿Qué es un ID de organización?

Se trata de un ID exclusivo que se le proporciona a su instancia cuando inicia sesión por primera vez en Adobe Experience Cloud. Debe tener el formato siguiente: xxx@AdobeOrg.

Para obtener más información, consulte la [documentación de Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=es).

### ¿Dónde puedo encontrar mi ID de organización?

Una forma es ir a la [Página de inicio de Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administración]**. Encontrará el ID de la organización en la parte inferior de la sección **[!UICONTROL Acceso rápido]** de la página de administración. Puede encontrar información más detallada en la [documentación de Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=es).

La otra forma es iniciar **Admin Console**. El ID de organización será visible en la dirección URL y debe tener un aspecto similar a: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

### ¿Por qué necesito saber mi ID de organización?

Para administrar la configuración de su instancia, queremos asegurarnos de que obtenga la información adecuada de la instancia correcta en caso de que utilice varias instancias para su compañía.

### ¿Qué sucede si tengo varios ID de organización?

Tener un ID de organización para Analytics y Campaign es un requisito si tiene pensado integrar las soluciones con el fin de aprovechar los casos de uso complejos, como el abandono del carro de compras (para Adobe Analytics y Adobe Campaign). Puede disponer de más de un ID de organización si tiene acceso a varias soluciones de Adobe. En este caso, el ID de organización correcto que debe usar es el que ve debajo de la instancia de Adobe Campaign.

<!--
>[!NOTE]
>
>If you have different organization IDs for Adobe Campaign and Adobe Analytics, please reach out to Customer Care to get them aligned.
-->

### ¿Cómo puedo saber si mi instancia de Adobe Campaign está alojada en AWS o no?{#hosted-aws}

Para comprobar si la instancia está alojada en AWS, siga estos pasos:

1. Recupere la dirección URL de inicio de sesión. Es la dirección URL que utiliza para iniciar sesión en la instancia de Campaign y termina mayoritariamente con “.campaign.adobe.com” o “.neolane.net”.
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
