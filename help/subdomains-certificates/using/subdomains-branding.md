---
product: campaign
solution: Campaign
title: Promoción de subdominios
description: Más información sobre la promoción de subdominios
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 100%

---

# Promoción de subdominios {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Acerca de los subdominios y los certificados SSL"
>abstract="Supervise los subdominios y los certificados SSL asociados."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=es" text="Monitorización de certificados SSL"

## ¿Por qué configurar subdominios?  {#why-setting-up-subdomains}

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico (mensajes transaccionales, información de marketing, etc.).

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan en la lista de bloqueados de los proveedores de servicios de Internet debido a la mala capacidad de entrega, esto impedirá que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; terminen en la lista de bloqueados.

## Métodos de configuración de subdominios {#subdomain-delegation-methods}

La configuración de subdominios le permite configurar una subsección del dominio (técnicamente una “zona DNS”) para utilizarla con Adobe Campaign. Los métodos de configuración disponibles son estos:

* **Delegación de subdominios completa en Adobe Campaign** (recomendado): el subdominio se delega completamente a Adobe. Adobe puede ofrecer Campaign como servicio administrado controlando y manteniendo todos los aspectos de DNS necesarios para la entrega, el procesamiento y el seguimiento de campañas de correo electrónico.

* **Uso de CNAME**: cree un subdominio y utilice CNAME para señalar registros específicos de Adobe. Con esta configuración, tanto Adobe como el cliente comparten la responsabilidad de mantener DNS.

En el cuadro que figura a continuación se ofrece un resumen del funcionamiento de estos métodos, así como el nivel de esfuerzo que suponen:

| Método de configuración | Funcionamiento | Nivel de esfuerzo |
|---|---|---|
| **Delegación completa** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe configurará todos los registros DNS necesarios para Adobe Campaign.<br/><br/>En esta configuración, Adobe es totalmente responsable de administrar el subdominio y todos los registros DNS. | Bajo |
| **CNAME, método personalizado** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe proporcionará los registros que se van a colocar en los servidores DNS y configurará los valores correspondientes en los servidores DNS de Adobe Campaign.<br/><br/>En esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS. | Alto |

Encontrará más información sobre la configuración de dominios en [esta documentación](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=es).

Si tiene alguna pregunta acerca de los métodos de configuración de subdominios, póngase en contacto con el equipo de entregabilidad de Adobe o, si lo prefiere, póngase en contacto con el servicio de atención al cliente para solicitar consultoría de entregabilidad.

## Casos de uso de subdominios (Campaign v7/v8){#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="Seleccione el caso de uso del subdominio"
>abstract="El desglose de los subdominios según los casos de uso es una práctica recomendada para la entregabilidad. Al hacerlo, la reputación de cada subdominio está aislada y protegida."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=es" text="Configuración de un nuevo subdominio"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=es" text="Promoción de subdominios"

Al configurar subdominios para instancias de Campaign v7/v8, es necesario seleccionar el caso de uso para el que se utilizará el subdominio (consulte [ Configuración de un nuevo subdominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

Los posibles casos de uso son:

* **Comunicaciones de marketing**: comunicaciones con fines comerciales. Ejemplo: campañas de correo electrónico de ventas.

* **Comunicaciones transaccionales y operativas**: las comunicaciones transaccionales contienen información destinada a completar un proceso que el destinatario ha iniciado con usted. Ejemplo: confirmación de compra, correo electrónico de restablecimiento de contraseña. Las comunicaciones de organización se refieren al intercambio de información, ideas y vistas dentro y fuera de la organización, sin fines comerciales.

**Desglose de los subdominios según los casos de uso es una práctica recomendada para la entrega**. Al hacerlo, la reputación de cada subdominio está aislada y protegida. Por ejemplo: si el subdominio para comunicaciones de marketing termina en la lista de bloqueados de los proveedores de servicios de Internet, el subdominio de comunicaciones transaccionales no se verá afectado y podrá enviar comunicaciones.

**Puede configurar subdominios para los casos de uso de marketing y transaccional**:

* En los casos de uso de Marketing, los subdominios se configurarán en instancias de **MID** (fuentes medias).
* En los casos de uso transaccional, los subdominios se configurarán en TODAS las instancias de **RT** (centro de mensajes/mensajería en tiempo real) para garantizar la conectividad. Por lo tanto, los subdominios funcionarán con todas las instancias de RT.

>[!NOTE]
>
>Si está utilizando Campaign v7/v8, el Panel de control le permite ver qué instancias de RT/MID están conectadas a la instancia de Marketing con la que está trabajando. Para obtener más información, consulte la sección [Detalles de instancias](../../instances-settings/using/instance-details.md).

**Temas relacionados:**

* [Configuración de un nuevo subdominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Supervisión de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)
