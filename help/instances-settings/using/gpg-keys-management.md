---
product: campaign
solution: Campaign
title: Administración de claves GPG
description: Obtenga información sobre cómo administrar claves GPG para cifrar y descifrar datos en Adobe Campaign.
feature: Control Panel
role: Admin
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 15%

---

# Administración de claves GPG {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="Acerca de las claves GPG"
>abstract="En esta pestaña, puede instalar y/o generar claves GPG en una instancia de marketing para cifrar los datos enviados desde Campaign y descifrar datos entrantes."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=es" text="Acerca de la monitorización del rendimiento"

## Acerca del cifrado GPG {#about-gpg-encryption}

El cifrado GPG permite proteger los datos mediante un sistema de pares de claves públicas-privadas que siguen el [OpenPGP](https://www.openpgp.org/about/standard/) especificación.

Una vez implementada, puede descifrar los datos entrantes y cifrar los datos salientes antes de que se produzca la transferencia para garantizar que nadie sin un par de claves coincidente válido pueda acceder a ellos.

Para implementar el cifrado GPG con Campaign, un usuario administrador debe instalar y/o generar claves GPG en una instancia de marketing directamente desde el Panel de control.

Esto le permite:

* **Cifrado de datos enviados**: Adobe Campaign envía datos después de cifrarlos con la clave pública instalada.

* **Descifrado de datos entrantes**: Adobe Campaign recibe datos cifrados desde un sistema externo mediante una clave pública descargada de la Panel de control de Campaign. Adobe Campaign descifra los datos con una clave privada que se genera desde la Panel de control de Campaign.

## Cifrado de datos {#encrypting-data}

Panel de control le permite cifrar datos procedentes de la instancia de Adobe Campaign.

Para ello, debe generar un par de claves GPG a partir de una herramienta de cifrado PGP e instalar la clave pública en Panel de control de Campaign. A continuación, podrá cifrar los datos antes de enviarlos desde su instancia. Para realizar esto, siga los pasos a continuación.

>[!NOTE]
>
>Puede instalar hasta 60 claves GPG en Panel de control de Campaign.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](#video)

1. Genere un par de claves pública y privada mediante una herramienta de cifrado PGP siguiendo el [Especificación de OpenPGP](https://www.openpgp.org/about/standard/). Para ello, instale una utilidad GPG o software GNuGP.

   >[!NOTE]
   >
   >El software libre de código abierto para generar claves está disponible. Sin embargo, asegúrese de seguir las directrices de su organización y utilizar la utilidad GPG recomendada por su organización de TI/seguridad.

1. Una vez instalada la utilidad, ejecute el siguiente comando, en Mac Terminal o Windows command.

   `gpg --full-generate-key`

1. Cuando se le solicite, especifique los parámetros deseados para la clave. Los parámetros obligatorios son:

   * **tipo de clave**: RSA
   * **longitud de clave**: 3072 - 4096 bits
   * **nombre real** y **dirección de email**: Permite rastrear quién creó el par de claves. Introduzca un nombre y una dirección de correo electrónico vinculados a su organización o departamento.
   * **comentario**: añadir una etiqueta al campo de comentario le ayudará a identificar fácilmente la clave que debe utilizar para cifrar los datos.
     >[!IMPORTANT]
     >
     >Asegúrese de que este campo no se deja vacío y de que se rellena un comentario.

   * **vencimiento**: Fecha o &quot;0&quot; para la que no hay fecha de caducidad.
   * **frase de contraseña**

   ![](assets/do-not-localize/gpg_command.png)

1. Una vez confirmado, el script genera una clave con su huella digital asociada, que puede exportar a un archivo o pegar directamente en el Panel de control de Campaign. Para exportar el archivo, ejecute este comando seguido de la huella digital de la clave generada.

   `gpg -a --export <fingerprint>`

1. Para instalar la clave pública en el Panel de control de Campaign, abra el **[!UICONTROL Configuración de instancia]** , luego seleccione la **[!UICONTROL Claves GPG]** y la instancia que desee.

1. Haga clic en **[!UICONTROL Clave de instalación]** botón.

   ![](assets/gpg_install_button.png)

1. Pegue la clave pública generada desde la herramienta de cifrado PGP. También puede arrastrar y soltar directamente el archivo de clave pública exportado.

   >[!NOTE]
   >
   >La clave pública debe tener el formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Haga clic en **[!UICONTROL Clave de instalación]** botón.

Una vez instalada la clave pública, se muestra en la lista. Puede usar el complemento **...** para descargarlo o copiar su huella digital.

![](assets/gpg_install_download.png)

La clave está disponible para su uso en flujos de trabajo de Adobe Campaign. Puede utilizarlo para cifrar datos al utilizar actividades de extracción de datos.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](#video)

Para obtener más información, consulte la documentación de Adobe Campaign:

**Campaign 7/8:**

* [Compresión o cifrado de un archivo](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html)
* [Caso de uso: codificación y exportación de datos con una clave instalada en el Panel de control](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [Administración de datos cifrados](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: codificación y exportación de datos con una clave instalada en el Panel de control](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html#use-case-gpg-encrypt)

## Descifrado de datos {#decrypting-data}

El Panel de control de Campaign de le permite descifrar datos externos que llegan a las instancias de Adobe Campaign.

Para ello, debe generar un par de claves GPG directamente desde la Panel de control de Campaign.

* El **clave pública** se compartirá con el sistema externo, que lo utilizará para cifrar los datos que se enviarán a Campaign.
* El **clave privada** Campaign utilizará para descifrar los datos cifrados entrantes.

![](assets/do-not-localize/how-to-video.png)[ Descubra esta función en vídeo](#video)

Para generar un par de claves en Panel de control de Campaign, siga estos pasos:

1. Abra el **[!UICONTROL Configuración de instancia]** , luego seleccione la **[!UICONTROL Claves GPG]** y la instancia de Adobe Campaign que desee.

1. Haga clic en **[!UICONTROL Generar clave]** botón.

   ![](assets/gpg_generate.png)

1. Especifique el nombre de la clave y haga clic en **[!UICONTROL Generar clave]**. Este nombre le ayudará a identificar la clave que debe utilizar para el descifrado en los flujos de trabajo de Campaign

   ![](assets/gpg_generate_name.png)

Una vez generado el par de claves, la clave pública se muestra en la lista. Tenga en cuenta que los pares de claves de descifrado se generan sin fecha de caducidad.

Puede usar el complemento **...** para descargar la clave pública o copiar su huella digital.

![](assets/gpg_generate_list.png)

La clave pública está disponible para compartirse con cualquier sistema externo. Adobe Campaign podrá utilizar la clave privada en las actividades de carga de datos para descifrar datos que se hayan cifrado con la clave pública.

Para obtener más información, consulte la documentación de Adobe Campaign:

**Campaign 7 y 8:**

* [Descompresión o desencriptado de un archivo antes de procesarlo](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html)
* [Caso de uso: importación de datos cifrados con una clave generada por el Panel de control](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [Administración de datos cifrados](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: importación de datos cifrados con una clave generada por el Panel de control](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## Monitorización de claves GPG

Para acceder a las claves GPG instaladas y generadas para las instancias, abra el **[!UICONTROL Configuración de instancia]** , luego seleccione la **[!UICONTROL Claves GPG]** pestaña.

![](assets/gpg_list.png)

La lista muestra todas las claves GPG de cifrado y descifrado que se han instalado y generado para las instancias con información detallada sobre cada clave:

* **[!UICONTROL Nombre]**: Nombre que se ha definido al instalar o generar la clave.
* **[!UICONTROL Caso de uso]**: Esta columna especifica el caso de uso de la clave:

  ![](assets/gpg_icon_encrypt.png): la clave se ha instalado para el cifrado de datos.

  ![](assets/gpg_icon_decrypt.png): la clave se ha generado para permitir el descifrado de datos.

* **[!UICONTROL Huella digital]**: la huella digital de la clave.
* **[!UICONTROL Caduca]**: la fecha de caducidad de la clave. Tenga en cuenta que el Panel de control de Campaign proporcionará indicaciones visuales a medida que la clave se aproxime a su fecha de caducidad:

   * Urgente (rojo) se muestra 30 días antes.
   * El aviso (amarillo) se muestra 60 días antes.
   * Se mostrará el aviso rojo &quot;Caducado&quot; cuando caduque una clave.

  >[!NOTE]
  >
  >Tenga en cuenta que no se enviará ninguna notificación por correo electrónico por Panel de control de Campaign.

Como práctica recomendada, le recomendamos que elimine todas las claves que ya no necesite. Para ello, haga clic en el **...** y luego seleccione **[!UICONTROL Eliminar clave].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Antes de eliminar una clave, asegúrese de que no se utilice en ningún flujo de trabajo de Adobe Campaign para evitar errores.

## Tutorial en vídeo {#video}

El siguiente vídeo muestra cómo generar e instalar claves GPG para el cifrado de datos.

Hay disponibles más vídeos de procedimientos relacionados con la administración de claves GPG en  [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html#instance-settings) y [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html#instance-settings) páginas de tutoriales de.

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
