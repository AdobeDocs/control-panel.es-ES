---
title: Acerca de los certificados SSL
description: Más información sobre los certificados SSL
translation-type: tm+mt
source-git-commit: ce93b595f4fbc2b3d72aadd034f93392565cb0e2

---


# Acerca de los certificados SSL {#about-ssl-certificates}

Adobe Campaign recomienda proteger los subdominios que alojan las páginas de aterrizaje, especialmente aquellos que recopilan información confidencial de sus clientes.

**El cifrado** SSL (Capa de zócalo seguro) garantiza que los subdominios delegados en Adobe sean seguros. Cuando el cliente rellena un formulario web o visita una página de aterrizaje alojada por Adobe Campaign, la información se envía de forma predeterminada a través de un protocolo no seguro (HTTP). Para garantizar una seguridad adicional, proteja la información enviada con un protocolo HTTPS. Por ejemplo, su dirección de subdominio "http://info.mywebsite.com/" será ahora "https://info.mywebsite.com/".

**Los certificados SSL no están instalados en los propios** subdominios delegados. Se instalan en subdominios asociados, principalmente los que hospedan páginas de aterrizaje, páginas de recursos y otros.

**Los certificados SSL se proporcionan para un período de tiempo** específico (1 año, 60 días, etc.). Una vez que caduca un certificado, puede experimentar problemas al acceder a las páginas de aterrizaje o al usar recursos del subdominio. Para evitarlo, el Panel de control le permite supervisar los certificados SSL de los subdominios, así como iniciar el proceso de renovación.

Más detalles sobre la delegación de subdominios están disponibles [aquí](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
