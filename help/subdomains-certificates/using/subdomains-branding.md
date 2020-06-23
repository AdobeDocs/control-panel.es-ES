---
title: Promoción de subdominios
description: Más información sobre la promoción de subdominios
translation-type: tm+mt
source-git-commit: 80b35e82116b064a7b141d957ab79ecfc9a99026
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 88%

---


# Promoción de subdominios {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Acerca de los subdominios y los certificados SSL"
>abstract="Supervise los subdominios y los certificados SSL asociados."
>additional-url="https://docs.adobe.com/content/help/es-ES/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Supervisión de los certificados SSL de los subdominios"

>[!IMPORTANT]
>
>La delegación de subdominios del Panel de control de Campaign está disponible en versión beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

## ¿Por qué configurar subdominios? {#why-setting-up-subdomains}

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico (mensajes transaccionales, información de marketing, etc.).

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo, si los subdominios &quot;marketing.mybrand.com&quot; terminan siendo agregados a la lista de bloques por Proveedores de servicio de Internet debido a una mala entrega, esto impediría que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; se agreguen a la lista de bloques.

## Métodos de delegación de subdominios {#subdomain-delegation-methods}

La delegación de subdominios le permite delegar una subsección de su dominio (técnicamente, una &quot;zona DNS&quot;) para utilizarla con Adobe Campaign. Los métodos de configuración disponibles son estos:

* **Delegación de subdominios completa en Adobe Campaign** (recomendado): el subdominio se delega completamente a Adobe. Adobe puede ofrecer Campaign como servicio administrado controlando y manteniendo todos los aspectos de DNS necesarios para la entrega, el procesamiento y el seguimiento de campañas de correo electrónico.

* **Uso de CNAME** (no recomendado y no admitido por el Panel de control de Campaign): cree un subdominio y utilice CNAME para señalar registros específicos de Adobe. Con esta configuración, tanto Adobe como el cliente comparten la responsabilidad de mantener DNS.

En el cuadro que figura a continuación se ofrece un resumen del funcionamiento de estos métodos, así como el nivel de esfuerzo que suponen:

| Método de delegación | Funcionamiento | Nivel de esfuerzo |
|---|---|---|
| **Delegación completa** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe configurará todos los registros DNS necesarios para Adobe Campaign.<br/><br/>En esta configuración, Adobe es totalmente responsable de administrar el subdominio y todos los registros DNS. | Bajo |
| **CNAME, método personalizado** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe proporcionará los registros que se van a colocar en los servidores DNS y configurará los valores correspondientes en los servidores DNS de Adobe Campaign.<br/><br/>En esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS. | Alto |

En [esta documentación](https://helpx.adobe.com/es/campaign/kb/domain-name-delegation.html) encontrará información adicional sobre la delegación de dominios.

Si tiene alguna pregunta acerca de los métodos de delegación de subdominios, póngase en contacto con el equipo de entrega de Adobe o póngase en contacto con el Servicio de atención al cliente para solicitar consultoría de entrega.

**Temas relacionados:**

* [Configuración de un nuevo subdominio](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Delegación de subdominios (tutorial en vídeo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Supervisión de subdominios](../../subdomains-certificates/using/monitoring-subdomains.md)
