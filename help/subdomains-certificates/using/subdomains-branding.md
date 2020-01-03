---
title: Marca de subdominios
description: Más información sobre la marca de subdominios
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# Marca de subdominios {#subdomains-branding}

>[!NOTE]
>
>La delegación de subdominios del Panel de control se encuentra actualmente en fase beta y sujeta a frecuentes actualizaciones y modificaciones sin previo aviso.

## ¿Por qué configurar subdominios? {#why-setting-up-subdomains}

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico (mensajes transaccionales, información de marketing, etc.).

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para sus comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para sus correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan bloqueados por los proveedores de servicios de Internet debido a una mala entrega, esto impediría que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; queden bloqueados.

## Métodos de delegación de subdominios {#subdomain-delegation-methods}

La delegación de subdominios permite delegar una subsección de su dominio (técnicamente, una &quot;zona DNS&quot;) para su uso con Adobe Campaign. Los métodos de configuración disponibles son:

* **Delegación de subdominios completa en Adobe Campaign** (recomendado): El subdominio se delega completamente en Adobe. Adobe puede ofrecer la campaña como un servicio administrado controlando y manteniendo todos los aspectos de DNS necesarios para la entrega, el procesamiento y el seguimiento de las campañas de correo electrónico.

* **Uso de CNAME** (no recomendado y no admitido por el Panel de control): Cree un subdominio y utilice CNAME para señalar registros específicos de Adobe. Con esta configuración, tanto Adobe como el cliente comparten la responsabilidad de mantener DNS.

En el cuadro que figura a continuación se ofrece un resumen del funcionamiento de estos métodos, así como el nivel de esfuerzo que supone:

| Método de delegación | Cómo funciona | Nivel de esfuerzo |
|---|---|---|
| **Delegación completa** | Cree el registro de subdominio y espacio de nombres. A continuación, Adobe configurará todos los registros DNS necesarios para Adobe Campaign.<br/><br/>En esta configuración, Adobe es totalmente responsable de administrar el subdominio y todos los registros DNS. | Bajo |
| **CNAME, método personalizado** | Cree el registro de subdominio y espacio de nombres. A continuación, Adobe proporcionará los registros que se van a colocar en los servidores DNS y configurará los valores correspondientes en los servidores DNS de Adobe Campaign.<br/><br/>En esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS. | Alto |

En [esta documentación](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)encontrará información adicional sobre la delegación de dominios.
