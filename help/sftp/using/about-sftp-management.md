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
TQID: https://experienceleague.adobe.com/UZHhTNCld6p1RFGh3DY-2r3VRiLNxCtP0anuPxPnWVE
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: tm+mt
source-wordcount: 168
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
