---
product: campaign
solution: Campaign
title: Acerca de la administración SFTP
description: Obtenga más información acerca de la administración de SFTP en el Panel de control
testing: SSECD-836 2
feature: Control Panel, SFTP Management
role: Admin
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '168'
ht-degree: 100%

---

# Acerca de la administración SFTP {#about-sftp-management}

En el Panel de control, puede interactuar con todos los servidores SFTP conectados a instancias de Campaign a las que tiene acceso. La mayoría de las instancias tienen servidores SFTP conectados (en algunos casos, es posible que las instancias de desarrollo y de fase no estén conectadas a ningún servidor SFTP).

El acceso a los servidores SFTP se realiza mediante un software cliente SFTP, que puede encontrar y descargar en línea. Para conectarse a un servidor, ya sea a través de una aplicación cliente o de una API, debe configurar una clave SSH pública y añadir a la lista de permitidos la dirección IP que se conecta al servidor SFTP.

El Panel de control le permite realizar las siguientes acciones para administrar los servidores SFTP:

* Monitorizar su **capacidad de almacenamiento**,
* Administrar **Lista de direcciones IP permitidas**: añadir o eliminar intervalos de direcciones IP para uno o varios servidores,
* Administrar **claves SSH públicas** para acceder a los servidores.

Encontrará más información sobre cada una de estas acciones en las secciones siguientes.
