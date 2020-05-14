---
title: Versiones del Panel de control
translation-type: tm+mt
source-git-commit: 88fd5b8853864ed25a3c6f2dfb5da718d0fc8d11
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 31%

---


# Control Panel releases {#control-panel-releases}

Aquí encontrará información sobre las últimas versiones del Panel de control.

>[!NOTE]
>
>Tenga en cuenta que el Panel de control está disponible para clientes alojados en AWS solamente, excepto para entornos híbridos que aún no son compatibles. No se requiere ninguna actualización para acceder al Panel de control. Asegúrese de que es un usuario administrador para acceder a él.

## Mayo de 2020 (#may-2020)

**Gestión de claves GPG**

Instale y/o genere claves GPG en una instancia de marketing, para cifrar los datos enviados desde la Campaña y descifrar los datos entrantes. [Más información](../..//instances-settings/using/gpg-keys-management.md)

**Administración de certificados para subdominios CNAME**

El Panel de control ahora le permite renovar los certificados SSL de sus subdominios delegados con el método CNAME. [Más información](../../subdomains-certificates/using/renewing-subdomain-certificate.md)

## de abril de 2020 {#april-2020}

**Administración de registros TXT de Google**

Añada el registro de verificación del sitio TXT de Google a todos los subdominios utilizados para enviar correos electrónicos a las direcciones de Gmail a través del Panel de control de Campañas. [Más información](../../subdomains-certificates/using/managing-txt-records.md)

**Supervisión del espacio de la base de datos**

El Panel de control de Campaña está equipado con capacidades de monitoreo de bases de datos, lo que le permite realizar vistas en el uso del espacio de la base de datos a pedido y con el paso del tiempo. [Más información](../../performance-monitoring/using/database-monitoring.md)

**Alertas por correo electrónico**

El Panel de control de Campaña está equipado con funciones de alerta por correo electrónico en tiempo real, que le permiten iniciar sesión en el Panel de control y registrarse para recibir alertas cuando el sistema está en riesgo de deterioro del rendimiento, o bien se requiere una acción para garantizar un alto rendimiento en el futuro. [Más información](../../performance-monitoring/using/email-alerting.md)

## Enero de 2020 {#january-2020}

*22 de enero de 2020*

Hemos agregado nuevas funciones para que los usuarios administradores deleguen subdominios y renueven certificados SSL desde el Panel de control.

Para obtener más información, consulte estas páginas:
* [Configuración de un nuevo subdominio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renovación del certificado SSL de un subdominio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Estas funciones estarán disponibles en versión beta y sujetas a frecuentes actualizaciones y modificaciones sin previo aviso.

## Septiembre de 2019 {#september-2019}

*16 de septiembre de 2019*

Hemos agregado nuevas funciones para los usuarios administradores a la lista blanca de direcciones IP para conectarse a instancias de Campaign Classic.
Además, los usuarios administradores ahora pueden vista la lista de las instancias de Campaign Classic y los requisitos para las actualizaciones de la compilación.

Para obtener más información, consulte la [documentación especializada](instances-settings/using/ip-whitelisting-instance-access.md).

## Agosto de 2019 {#august-2019}

Hemos añadido nuevas funcionalidades para que los administradores reciban notificaciones antes de que expiren los certificados SSL para sus dominios. Para obtener más información, consulte la [documentación detallada](subdomains-certificates/using/monitoring-ssl-certificates.md).

Además, los administradores ahora pueden borrar las claves SSH que se añadieron para acceder a los servidores SFTP.

## Julio de 2019 {#july-2019}

Hemos agregado nuevas funciones para habilitar a los usuarios administradores para que tomen bueno control de la configuración de instancias de Campaign Classic. Las nuevas funcionalidades del Panel de control incluyen la posibilidad de añadir las URL a las que se conecta Adobe Campaign para las transferencias de datos o archivos.

Para obtener más información, consulte la [documentación detallada](instances-settings/using/url-permissions.md).
