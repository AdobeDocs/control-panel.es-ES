---
title: Acerca de los subdominios
description: Más información sobre los subdominios
translation-type: tm+mt
source-git-commit: c2ef995d49118943bdd77e6d3c14ef7ec643e672

---


# Acerca del subdominio {#about-subdomains}

## ¿Por qué configurar subdominios? {#why-setting-up-subdomains}

Un subdominio es una división de su dominio que puede utilizarse para aislar varios tipos de tráfico (corporativo, información de marketing, etc.).

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones informativas y de marketing:

* info.mybrand.com para sus comunicaciones internas
* marketing.mybrand.com para sus correos electrónicos de prospección.

En este caso, puede decidir delegar el subdominio &quot;marketing.mybrand.com&quot; en Adobe Campaign. Al hacer esto, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan bloqueados por los proveedores de servicios de Internet debido a la mala capacidad de entrega, esto impediría que se bloquearan todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot;.

## Métodos de delegación de subdominios {#subdomain-delegation-methods}

La delegación de subdominios permite delegar una subsección de su dominio (técnicamente, una &quot;zona DNS&quot;) para su uso con Adobe Campaign. Los métodos de configuración disponibles son:

* **Delegación de subdominios completa en Adobe Campaign** (recomendado)

   El subdominio se delega completamente en Adobe. Adobe puede ofrecer la campaña como un servicio administrado controlando y manteniendo todos los aspectos de DNS necesarios para la entrega, el procesamiento y el seguimiento de las campañas de correo electrónico.

* **Uso de CNAME** (no recomendado y no admitido a través del Panel de control):

   Cree un subdominio y utilice CNAME para señalar registros específicos de Adobe. Con esta configuración, tanto Adobe como el cliente comparten la responsabilidad de mantener DNS.

Para obtener más información sobre cada uno de estos métodos (responsabilidad implícita, requisitos, etc.), consulte [esta documentación](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
