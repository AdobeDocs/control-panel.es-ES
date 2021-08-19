---
product: campaign
solution: Campaign
title: Administración de claves GPG
description: Obtenga información sobre cómo administrar claves GPG para cifrar y descifrar datos en Adobe Campaign.
feature: Panel de control de Campaign
role: Architect
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: 1bf4f7b6f6d4d9a47f6496299ca1c155eec4a2f3
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 14%

---

# Administración de claves GPG {#gpg-keys-management}

## Acerca del cifrado GPG {#about-gpg-encryption}

El cifrado GPG le permite proteger sus datos mediante un sistema de pares de claves pública y privada que siguen la especificación [OpenPGP](https://www.openpgp.org/about/standard/).

Una vez implementados, los datos entrantes se pueden descifrar y los datos salientes se pueden cifrar antes de la transferencia para garantizar que nadie sin un par de claves coincidentes válido no pueda acceder a ellos.

Para implementar el cifrado GPG con Campaign, un usuario administrador debe instalar y/o generar claves GPG en una instancia de marketing directamente desde el Panel de control de Campaign.

Esto le permite:

* **Codificar datos** enviados: Adobe Campaign envía los datos después de cifrarlos con la clave pública instalada.

* **Descifrar datos** entrantes: Adobe Campaign recibe datos cifrados desde un sistema externo mediante una clave pública descargada del Panel de control de Campaign. Adobe Campaign descifra los datos mediante una clave privada generada a partir del Panel de control de Campaign.

## Codificación de datos {#encrypting-data}

El panel de control de Campaign le permite cifrar datos procedentes de la instancia de Adobe Campaign.

Para ello, debe generar un par de claves GPG a partir de una herramienta de cifrado PGP y luego instalar la clave pública en Panel de control de Campaign. Puede cifrar los datos antes de enviarlos desde la instancia. Para realizar esto, siga los pasos a continuación.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](#video)

1. Genere un par de claves pública y privada usando una herramienta de encriptación PGP siguiendo la [especificación OpenPGP](https://www.openpgp.org/about/standard/). Para ello, instale una utilidad GPG o software GNuGP.

   >[!NOTE]
   >
   >El software libre de código abierto para generar claves está disponible. Sin embargo, asegúrese de seguir las directrices de su organización y utilizar la utilidad GPG recomendada por su organización de TI/seguridad.

1. Una vez instalada la utilidad, ejecute el siguiente comando, en Mac Terminal o en el comando Windows.

   `gpg --full-generate-key`

1. Cuando se le pida, especifique los parámetros deseados para la clave. Los parámetros necesarios son:

   * **tipo** de clave: RSA
   * **longitud de clave**: 1024 - 4096 bits
   * **nombre real** y dirección de  **correo electrónico**: Permite rastrear quién creó el par de claves. Introduzca un nombre y una dirección de correo electrónico vinculados a su organización o departamento.
   * **comentario**: agregar una etiqueta al campo de comentarios le ayudará a identificar fácilmente la clave que debe utilizar para cifrar los datos.
   * **caducidad**: Fecha o &quot;0&quot; sin fecha de caducidad.
   * **frase de contraseña**

   ![](assets/do-not-localize/gpg_command.png)

1. Una vez confirmada, la secuencia de comandos genera una clave con su huella digital asociada, que puede exportar a un archivo o pegar directamente en el Panel de control de Campaign. Para exportar el archivo, ejecute este comando seguido de la huella digital de la clave que ha generado.

   `gpg -a --export <fingerprint>`

1. Para instalar la clave pública en Panel de control de Campaign, abra la tarjeta **[!UICONTROL Instance settings]** y seleccione la pestaña **[!UICONTROL GPG keys]** y la instancia que desee.

1. Haga clic en el botón **[!UICONTROL Install Key]**.

   ![](assets/gpg_install_button.png)

1. Pegue la clave pública que se ha generado desde la herramienta de cifrado PGP. También puede arrastrar y soltar directamente el archivo de clave pública exportado.

   >[!NOTE]
   >
   >La clave pública debe tener el formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Haga clic en el botón **[!UICONTROL Install Key]**.

Una vez instalada la clave pública, esta se muestra en la lista. Puede utilizar el **...** para descargarlo o copiar su huella digital.

![](assets/gpg_install_download.png)

La clave está disponible para su uso en flujos de trabajo de Adobe Campaign. Puede utilizarla para cifrar datos al utilizar actividades de extracción de datos.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](#video)

Para obtener más información sobre este tema, consulte la documentación de Adobe Campaign:

**Campaign Classic v7 y Campaign v8:**

* [Compresión o cifrado de un archivo](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html)
* [Caso de uso: codificación y exportación de datos con una clave instalada en el Panel de control de Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [Administración de datos cifrados](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: codificación y exportación de datos con una clave instalada en el Panel de control de Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html#use-case-gpg-encrypt)

## Descifrado de datos {#decrypting-data}

Panel de control de Campaign le permite descifrar datos externos que llegan a las instancias de Adobe Campaign.

Para ello, debe generar un par de claves GPG directamente desde el Panel de control de Campaign .

* La **clave pública** se compartirá con el sistema externo, que la utilizará para cifrar los datos que se enviarán a Campaign.
* Campaign utilizará la **clave privada** para descifrar los datos cifrados entrantes.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](#video)

Para generar un par de claves en el Panel de control de Campaign, siga estos pasos:

1. Abra la tarjeta **[!UICONTROL Instance settings]** y seleccione la pestaña **[!UICONTROL GPG keys]** y la instancia de Adobe Campaign que desee.

1. Haga clic en el botón **[!UICONTROL Generate Key]**.

   ![](assets/gpg_generate.png)

1. Especifique el nombre de la clave y haga clic en **[!UICONTROL Generate Key]**. Este nombre le ayudará a identificar la clave que se utilizará para el descifrado en los flujos de trabajo de Campaign

   ![](assets/gpg_generate_name.png)

Una vez generado el par de claves, la clave pública se muestra en la lista. Tenga en cuenta que los pares de claves de descifrado se generan sin fecha de caducidad.

Puede utilizar el **...** para descargar la clave pública o copiar su huella digital.

![](assets/gpg_generate_list.png)

La clave pública está disponible para compartirse con cualquier sistema externo. Adobe Campaign podrá utilizar la clave privada en las actividades de carga de datos para descifrar datos que se hayan cifrado con la clave pública.

Para obtener más información, consulte la documentación de Adobe Campaign:

**Campaign Classic v7 y Campaign v8:**

* [Descompresión o desencriptado de un archivo antes de procesarlo](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html)
* [Caso de uso: importación de datos cifrados con una clave generada por el Panel de control de Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [Administración de datos cifrados](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: importación de datos cifrados con una clave generada por el Panel de control de Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## Supervisión de claves GPG

Para acceder a las claves GPG instaladas y generadas para las instancias, abra la tarjeta **[!UICONTROL Instance settings]** y seleccione la pestaña **[!UICONTROL GPG keys]** .

![](assets/gpg_list.png)

La lista muestra todas las claves GPG de cifrado y descifrado que se han instalado y generado para sus instancias con información detallada sobre cada clave:

* **[!UICONTROL Name]**: El nombre que se ha definido al instalar o generar la clave.
* **[!UICONTROL Use case]**: Esta columna especifica el caso de uso de la clave:

   ![](assets/gpg_icon_encrypt.png): La clave se ha instalado para el cifrado de datos.

   ![](assets/gpg_icon_decrypt.png): La clave se ha generado para permitir el descifrado de datos.

* **[!UICONTROL Fingerprint]**: la huella digital de la clave.
* **[!UICONTROL Expires]**: La fecha de caducidad de la clave. Tenga en cuenta que el Panel de control de Campaign proporcionará indicaciones visuales a medida que la clave se acerque a su fecha de caducidad:

   * Urgente (rojo) se muestra 30 días antes.
   * La advertencia (amarillo) se muestra 60 días antes.
   * Se mostrará un banner rojo &quot;Caducado&quot; una vez que la clave caduque.

   >[!NOTE]
   >
   >Tenga en cuenta que no se enviará ninguna notificación por correo electrónico por Panel de control de Campaign.

Como práctica recomendada, le recomendamos que elimine todas las claves que ya no necesite. Para ello, haga clic en **...Botón** y seleccione **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Antes de quitar una clave, asegúrese de que no se utiliza en ningún flujo de trabajo de Adobe Campaign para evitar que falle.

## Tutorial en vídeo {#video}

El siguiente vídeo muestra cómo generar e instalar claves GPG para el cifrado de datos.

Hay disponibles vídeos de procedimientos adicionales relacionados con la administración de claves GPG en las páginas de tutoriales [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings) y [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings).

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
