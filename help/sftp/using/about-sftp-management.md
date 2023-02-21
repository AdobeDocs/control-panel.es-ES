---
product: campaign
solution: Campaign
title: Acerca de la administración SFTP
description: Obtenga más información sobre la administración de SFTP en el Panel de control de Campaign
testing: SSECD-836 2
feature: Control Panel
role: Architect
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 16%

---

# Acerca de la administración SFTP {#about-sftp-management}

En el Panel de control de Campaign, puede interactuar con todos los servidores SFTP conectados a instancias de Campaign a las que tiene acceso. La mayoría de las instancias han conectado servidores SFTP (en algunos casos, es posible que las instancias de desarrollo y ensayo no estén conectadas a ningún servidor SFTP).

El acceso a los servidores SFTP se realiza mediante un software de cliente SFTP, que puede encontrar y descargar en línea. Para conectarse a un servidor, ya sea a través de una aplicación cliente o una API, debe configurar la clave SSH pública y añadir la dirección IP que se conecte al servidor SFTP a la lista de permitidos.

El panel de control de Campaign le permite realizar las siguientes acciones para administrar los servidores SFTP:

* Monitorice sus **capacidad de almacenamiento**,
* Administrar **Listas de direcciones IP permitidas**: agregar o eliminar intervalos de direcciones IP para uno o varios servidores,
* Administrar **claves SSH públicas** para acceder a sus servidores.

Encontrará información detallada sobre cada una de estas acciones en las secciones siguientes.
