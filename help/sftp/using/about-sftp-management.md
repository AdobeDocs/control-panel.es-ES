---
title: Acerca de la administración SFTP
description: Más información sobre la administración de SFTP en el Panel de control de Campaign
testing: SSECD-836 2
translation-type: tm+mt
source-git-commit: 9fe5f25ef2f3d7dafe9ae63d430279c354fce25a
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 3%

---


# Acerca de la administración SFTP {#about-sftp-management}

En el Panel de control de Campaign, puede interactuar con todos los servidores SFTP conectados a instancias de Campaña a los que tiene acceso. La mayoría de las instancias tienen servidores SFTP conectados (en algunos casos, es posible que las instancias de desarrollo y de etapa no estén conectadas a ningún servidor SFTP).

El acceso a los servidores SFTP se realiza mediante un software cliente SFTP, que puede encontrar y descargar en línea. Para conectarse a un servidor, ya sea a través de una aplicación cliente o una API, debe configurar la clave SSH pública y agregar la dirección IP que se conecta a su servidor SFTP a la lista de permitidos.

El panel de control permite realizar las siguientes acciones para administrar los servidores SFTP:

* Supervisar su capacidad **de** almacenamiento,
* Administrar direcciones **IP permiten la enumeración**: agregar o eliminar intervalos de direcciones IP para uno o varios servidores,
* Administre las claves **SSH** públicas para acceder a los servidores.

En las secciones siguientes encontrará información detallada sobre cada una de estas acciones.
