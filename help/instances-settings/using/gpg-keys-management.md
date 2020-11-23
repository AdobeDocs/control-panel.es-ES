---
product: campaign
solution: Campaign
title: Administración de claves GPG
description: Obtenga información sobre cómo administrar claves GPG para cifrar y descifrar datos en Adobe Campaign.
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 13%

---


# Administración de claves GPG {#gpg-keys-management}

## Acerca del cifrado GPG {#about-gpg-encryption}

El cifrado GPG le permite proteger sus datos mediante un sistema de pares de claves público-privadas que siguen la especificación [OpenPGP](https://www.openpgp.org/about/standard/) .

Una vez implementados, los datos entrantes se pueden descifrar y los datos salientes se pueden cifrar antes de que se produzca la transferencia para garantizar que nadie tenga acceso a ellos sin un par de claves coincidentes válido.

![](assets/do-not-localize/how-to-video.png) Descubrir esta función en vídeo mediante [Campaign Classic](https://docs.adobe.com/content/help/es-ES/campaign-classic-learn/tutorials/administrating/control-panel-acc/gpg-key-management/gpg-key-management-overview.html) o [Campaign Standard](https://docs.adobe.com/content/help/es-ES/campaign-standard-learn/tutorials/administrating/control-panel/gpg-key-management/gpg-key-management-overview.html)

Para implementar el cifrado GPG con Campaign, un usuario administrador debe instalar y/o generar claves GPG en una instancia de marketing directamente desde el Panel de control de Campaign.

Esto le permite:

* **Cifrar datos** enviados: Adobe Campaign envía los datos después de cifrarlos con la clave pública instalada.

* **Descifrar datos** entrantes: Adobe Campaign recibe datos cifrados desde un sistema externo mediante una clave pública descargada del Panel de control de Campaign. Adobe Campaign descifra los datos mediante una clave privada generada a partir del Panel de control de Campaign.

## Cifrar datos {#encrypting-data}

El panel de control de Campaign le permite cifrar datos procedentes de la instancia de Adobe Campaign.

Para ello, debe generar un par de claves GPG a partir de una herramienta de cifrado PGP y luego instalar la clave pública en Panel de control de Campaign. Luego podrá cifrar los datos antes de enviarlos desde su instancia. Para realizar esto, siga los pasos a continuación.

![](assets/do-not-localize/how-to-video.png) Descubra cómo generar e instalar claves GPG en vídeo con [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/generating-and-installing-gpg-keys-for-data-encryption.html?lang=en#instance-settings) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/generating-and-installing-gpg-keys-for-data-encryption.html?lang=en#instance-settings)

1. Genere un par de claves pública y privada utilizando una herramienta de cifrado PGP siguiendo la especificación [OpenPGP](https://www.openpgp.org/about/standard/). Para ello, instale una utilidad GPG o un software GNuGP.

   >[!NOTE]
   >
   >El software libre de código abierto para generar claves está disponible. Sin embargo, asegúrese de seguir las directrices de su organización y utilizar la utilidad GPG recomendada por su organización de TI/seguridad.

1. Una vez instalada la utilidad, ejecute el comando siguiente, en el comando de Mac Terminal o Windows.

   `gpg --full-generate-key`

1. Cuando se le solicite, especifique los parámetros deseados para la clave. Los parámetros requeridos son:

   * **tipo** de clave: RSA
   * **longitud** de clave: 1024 - 4096 bits
   * **nombre** real y dirección **de** correo electrónico: Permite rastrear quién creó el par de claves. Escriba un nombre y una dirección de correo electrónico vinculados a su organización o departamento.
   * **comentario**: agregar una etiqueta al campo de comentarios le ayudará a identificar fácilmente la clave que utilizar para cifrar sus datos.
   * **caducidad**: Fecha o &quot;0&quot; sin fecha de caducidad.
   * **frase de contraseña**

   ![](assets/do-not-localize/gpg_command.png)

1. Una vez confirmada, la secuencia de comandos generará una clave con su huella digital asociada, que puede exportar a un archivo o pegar directamente en el Panel de control de Campaign. Para exportar el archivo, ejecute este comando seguido de la huella digital de la clave que ha generado.

   `gpg -a --export <fingerprint>`

1. Para instalar la clave pública en Panel de control de Campaign, abra la **[!UICONTROL Instance settings]** tarjeta y, a continuación, seleccione la **[!UICONTROL GPG keys]** ficha y la instancia que desee.

1. Haga clic en el botón **[!UICONTROL Install Key]**.

   ![](assets/gpg_install_button.png)

1. Pegue la clave pública que se ha generado a partir de la herramienta de cifrado PGP. También puede arrastrar y soltar directamente el archivo de clave pública exportado.

   >[!NOTE]
   >
   >La clave pública debe tener el formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Haga clic en el botón **[!UICONTROL Install Key]**.

Una vez instalada la clave pública, esta se muestra en la lista. Puede usar el **...** para descargarlo o copiar su huella digital.

![](assets/gpg_install_download.png)

La clave está disponible para su uso en flujos de trabajo de Adobe Campaign. Puede utilizarla para cifrar datos al utilizar actividades de extracción de datos.

Para obtener más información sobre este tema, consulte la documentación de Adobe Campaign:

**Campaign Classic:**

* [Comprimir o encriptar un archivo](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file)
* [Caso de uso: codificación y exportación de datos con una clave instalada en el Panel de control de Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [Administración de datos cifrados](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: codificación y exportación de datos con una clave instalada en el Panel de control de Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

![](assets/do-not-localize/how-to-video.png) Descubra cómo cifrar datos en vídeo mediante [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/using-a-gpg-key-to-encrypt-data.html?lang=en#instance-settings) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/using-a-gpg-key-to-encrypt-data.html?lang=en#instance-settings)

## Descifrado de datos {#decrypting-data}

Panel de control de Campaign le permite descifrar datos externos que llegan a las instancias de Adobe Campaign.

Para ello, debe generar un par de claves GPG directamente desde el Panel de control de Campaign.

* The **public key** will be shared with the external system, which will use it to encrypt the data to send to Campaign.
* The **private key** will be used by Campaign to decrypt the incoming encrypted data.

![](assets/do-not-localize/how-to-video.png) Descubrir esta función en vídeo mediante [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/decrypting-data.html?lang=en#decrypting-data) o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/decrypting-data.html?lang=en#instance-settings)

Para generar un par de claves en Panel de control de Campaign, siga estos pasos:

1. Abra la **[!UICONTROL Instance settings]** tarjeta y, a continuación, seleccione la **[!UICONTROL GPG keys]** ficha y la instancia de Adobe Campaign que desee.

1. Haga clic en el botón **[!UICONTROL Generate Key]**.

   ![](assets/gpg_generate.png)

1. Especifique el nombre de la clave y haga clic en **[!UICONTROL Generate Key]**. Este nombre le ayudará a identificar la clave que se utilizará para el descifrado en Flujos de trabajo de la campaña

   ![](assets/gpg_generate_name.png)

Una vez generado el par de claves, la clave pública se muestra en la lista. Tenga en cuenta que los pares de claves de descifrado se generan sin fecha de caducidad.

Puede usar el **...** para descargar la clave pública o copiar su huella digital.

![](assets/gpg_generate_list.png)

La clave pública está disponible para compartirse con cualquier sistema externo. Adobe Campaign podrá utilizar la clave privada en actividades de carga de datos para descifrar los datos que se han cifrado con la clave pública.

Para obtener más información sobre esto, consulte la documentación de Adobe Campaign:

**Campaign Classic:**

* [Descompresión o desencriptado de un archivo antes de procesarlo](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing)
* [Caso de uso: importación de datos cifrados con una clave generada por el Panel de control de Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [Administración de datos cifrados](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: importación de datos cifrados con una clave generada por el Panel de control de Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## Control de claves GPG

Para acceder a las claves GPG instaladas y generadas para sus instancias, abra la **[!UICONTROL Instance settings]** tarjeta y seleccione la **[!UICONTROL GPG keys]** ficha.

![](assets/gpg_list.png)

La lista muestra todas las claves GPG de cifrado y descifrado que se han instalado y generado para las instancias con información detallada sobre cada clave:

* **[!UICONTROL Name]**:: Nombre que se ha definido al instalar o generar la clave.
* **[!UICONTROL Use case]**:: Esta columna especifica el caso de uso de la clave:

   ![](assets/gpg_icon_encrypt.png):: La clave se ha instalado para el cifrado de datos.

   ![](assets/gpg_icon_decrypt.png):: La clave se ha generado para permitir el descifrado de datos.

* **[!UICONTROL Fingerprint]**:: la huella digital de la llave.
* **[!UICONTROL Expires]**:: Fecha de caducidad de la clave. Tenga en cuenta que el Panel de control de Campaign proporcionará indicaciones visuales a medida que la clave se acerca a su fecha de caducidad:

   * Urgente (rojo) se muestra 30 días antes.
   * La advertencia (amarilla) se muestra 60 días antes.
   * Una vez que caduque una clave, se mostrará una pancarta roja &quot;Caducada&quot;.

   >[!NOTE]
   >
   >Tenga en cuenta que el Panel de control de Campaign no enviará ninguna notificación por correo electrónico.

Como práctica recomendada, le recomendamos que elimine cualquier clave que ya no necesite. To do this, click the **...** button then select **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Antes de quitar una clave, asegúrese de que no se utiliza en ningún flujo de trabajo de Adobe Campaign para evitar que falle.
