---
product: campaign
solution: Campaign
title: Promoción de subdominios
description: Más información sobre la promoción de subdominios
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 79%

---


# Promoción de subdominios {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Acerca de los subdominios y los certificados SSL"
>abstract="Supervise los subdominios y los certificados SSL asociados."
>additional-url="https://docs.adobe.com/content/help/es-ES/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Supervisión de los certificados SSL de los subdominios"

>[!IMPORTANT]
>
>La configuración de subdominios del Panel de control de Campaign está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

## ¿Por qué configurar subdominios? {#why-setting-up-subdomains}

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico (mensajes transaccionales, información de marketing, etc.).

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan en la lista de bloqueados de los proveedores de servicios de Internet debido a la mala capacidad de entrega, esto impedirá que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; terminen en la lista de bloqueados.

## Métodos de configuración de subdominios {#subdomain-delegation-methods}

La configuración de subdominio permite configurar una subsección de su dominio (técnicamente, una &quot;zona DNS&quot;) para su uso con Adobe Campaign. Los métodos de configuración disponibles son estos:

* **Delegación de subdominios completa en Adobe Campaign** (recomendado): el subdominio se delega completamente a Adobe. Adobe puede ofrecer Campaign como servicio administrado controlando y manteniendo todos los aspectos de DNS necesarios para la entrega, el procesamiento y el seguimiento de campañas de correo electrónico.

* **Uso de CNAME**: Cree un subdominio y utilice CNAME para apuntar a registros específicos del Adobe. Con esta configuración, tanto Adobe como el cliente comparten la responsabilidad de mantener DNS.

En el cuadro que figura a continuación se ofrece un resumen del funcionamiento de estos métodos, así como el nivel de esfuerzo que suponen:

| Método de configuración | Funcionamiento | Nivel de esfuerzo |
|---|---|---|
| **Delegación completa** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe configurará todos los registros DNS necesarios para Adobe Campaign.<br/><br/>En esta configuración, Adobe es totalmente responsable de administrar el subdominio y todos los registros DNS. | Bajo |
| **CNAME, método personalizado** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe proporcionará los registros que se van a colocar en los servidores DNS y configurará los valores correspondientes en los servidores DNS de Adobe Campaign.<br/><br/>En esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS. | Alto |

Additional information on domain configuration is available in [this documentation](https://helpx.adobe.com/es/campaign/kb/domain-name-delegation.html).

Si tiene alguna pregunta acerca de los métodos de configuración de subdominio, póngase en contacto con el equipo de entrega de Adobe o póngase en contacto con el Servicio de atención al cliente para solicitar consultoría sobre la entrega.

## Casos de uso de subdominios (Campaign Classic){#subdomains-use-cases}

Al configurar subdominios para instancias de Campaign Classic, debe seleccionar el caso de uso para el que se usará el subdominio (consulte [Configuración de un nuevo subdominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

Los casos de uso posibles son:

* **Comunicaciones de marketing**: comunicaciones con fines comerciales. Ejemplo: campañas de correo electrónico de ventas.

* **Comunicaciones transaccionales y operativas**: las comunicaciones transaccionales contienen información destinada a completar un proceso que el destinatario ha iniciado con usted. Ejemplo: confirmación de compra, correo electrónico de restablecimiento de contraseña. Las comunicaciones de organización se refieren al intercambio de información, ideas y vistas dentro y fuera de la organización, sin fines comerciales.

**Desglose de los subdominios según los casos de uso es una práctica recomendada para la entrega**. Al hacerlo, la reputación de cada subdominio está aislada y protegida. Por ejemplo: si el subdominio para comunicaciones de marketing termina en la lista de bloqueados de los proveedores de servicios de Internet, el subdominio de comunicaciones transaccionales no se verá afectado y podrá enviar comunicaciones.

**Puede configurar subdominios para casos** de uso de mercadotecnia y transaccional:

* En los casos de uso de Marketing, los subdominios se configurarán en instancias de **MID** (fuentes medias).
* En los casos de uso transaccional, los subdominios se configurarán en TODAS las instancias de **RT** (centro de mensajes/mensajería en tiempo real) para garantizar la conectividad. Por lo tanto, los subdominios funcionarán con todas las instancias de RT.

>[!NOTE]
>
>Si utiliza Campaign Classic, el Panel de control de Campaign le permite ver qué instancias de RT/MID están conectadas a la instancia de Marketing con la que está trabajando. Para obtener más información, consulte la sección [Detalles de instancias](../../instances-settings/using/instance-details.md).

**Temas relacionados:**

* [Configuración de un nuevo subdominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Tutorial video](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Supervisión de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)
