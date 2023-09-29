---
product: campaign
solution: Campaign
title: Añadir registros DMARC
description: Obtenga información sobre cómo agregar un registro DMARC para un subdominio.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: f87a13c8553173e4303c9b95cfea5de05ff49cee
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---


# Añadir registros DMARC {#dmarc}

## Acerca de los registros DMARC {#about}

Autenticación de mensajes, creación de informes y conformidad basados en dominio (DMARC) es un estándar de protocolo de autenticación de correo electrónico que ayuda a las organizaciones a proteger sus dominios de correo electrónico de ataques de suplantación de identidad y suplantación de identidad. Permite decidir cómo debe gestionar un proveedor de buzones los correos electrónicos que no superan las comprobaciones SPF y DKIM, lo que proporciona una forma de autenticar el dominio del remitente y evitar el uso no autorizado del dominio con fines malintencionados.

<!--Detailed information on DMARC implementation is available in [Adobe Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)-->

## Limitaciones y requisitos previos {#limitations}

* Los registros SPF y DKIM son requisitos previos para crear un registro DMARC.
* Los registros DMARC solo se pueden agregar para subdominios que utilizan delegación de subdominios completa. [Más información sobre los métodos de configuración de subdominios](subdomains-branding.md#subdomain-delegation-methods)

## Añadir un registro DMARC para un subdominio {#add}

Para añadir un registro DMARC para un subdominio, siga estos pasos:

1. En la lista de subdominios, haga clic en el botón de puntos suspensivos situado junto al subdominio deseado y seleccione **[!UICONTROL Subdomain details]**.

1. Haga clic en **[!UICONTROL Add TXT record]** y luego elija **[!UICONTROL DMARC]** desde el **[!UICONTROL Record Type]** lista desplegable.

   ![](assets/dmarc-add.png)

1. Elija la **[!UICONTROL Policy Type]** que el servidor de destinatario debe seguir cuando falla uno de los correos electrónicos. Los tipos de directivas disponibles son:

   * **[!UICONTROL None]**,
   * **[!UICONTROL Quarantine]** (ubicación de la carpeta de correo no deseado),
   * **[!UICONTROL Reject]** (bloquear el correo electrónico).

   Como práctica recomendada, se recomienda implementar lentamente la implementación de DMARC escalando la política de DMARC de p=none, p=quarantine, p=reject a medida que se obtiene la comprensión de DMARC del impacto potencial de DMARC.

   * **Paso 1:** Analice los comentarios que recibe y utiliza (p=ninguno), lo que indica al destinatario que no realice ninguna acción contra los mensajes que no se autentican correctamente, pero que envíe informes de correo electrónico al remitente. Además, revise y corrija los problemas con SPF/DKIM si los mensajes legítimos fallan en la autenticación.

   * **Paso 2:** Determine si SPF y DKIM están alineados y pasa la autenticación para todo el correo electrónico legítimo y, a continuación, mueva la directiva a (p=quarantine), que indica al servidor de correo electrónico receptor que ponga en cuarentena el correo electrónico que falla en la autenticación (esto generalmente significa colocar esos mensajes en la carpeta de correo no deseado). Si la directiva está configurada para poner en cuarentena, se recomienda que comience con un pequeño porcentaje de los correos electrónicos.

   * **Paso 3:** Ajustar directiva a (p=reject). NOTA: Utilice esta directiva con precaución y determine si es apropiada para su organización. La directiva p= reject indica al destinatario que deniegue (devuelva) completamente cualquier correo electrónico del dominio que falle en la autenticación. Con esta directiva habilitada, solo los correos electrónicos verificados como 100 % autenticados por el dominio tendrán la oportunidad de colocar la bandeja de entrada.

   >[!NOTE]
   >
   > La creación de registros BIMI no está disponible con un tipo de directiva de registro DMARC establecido en &quot;Ninguno&quot;.

1. Rellene las direcciones de correo electrónico que deben recibir los informes DMARC. Cuando uno de los correos electrónicos falla, los informes DMARC se envían automáticamente a la dirección de correo electrónico que elija:

   * Los informes DMARC agregados proporcionan información de alto nivel como, por ejemplo, el número de correos electrónicos con errores durante un periodo determinado.
   * Los informes de errores de DMARC forenses proporcionan información detallada como, por ejemplo, la dirección IP desde la que se originan los mensajes de correo electrónico erróneos.

1. Si la política DMARC está establecida en &quot;Ninguno&quot;, introduzca un porcentaje que se aplique al 100% de los correos electrónicos.

   Si la directiva se establece en &quot;Rechazar&quot; o &quot;Cuarentena&quot;, se recomienda que comience con un pequeño porcentaje de los correos electrónicos. A medida que más correos electrónicos de su dominio pasen la autenticación con servidores de recepción, actualice su registro lentamente con un porcentaje más alto.

   >[!NOTE]
   >
   >Si su dominio utiliza BIMI, su política DMARC debe tener un valor porcentual del 100%. BIMI no admite directivas DMARC con este valor establecido en menos del 100%.

   ![](assets/dmarc-add2.png)

1. Los informes DMARC se envían cada 24 horas. Puede cambiar la frecuencia de envío de los informes en la **[!UICONTROL Reporting Interval]** field. El intervalo mínimo autorizado es de 1 hora, mientras que el valor máximo autorizado es de 2190 horas (es decir, 3 meses).

1. En el **SPF** y **[!UICONTROL DKIM Identifier Alignment]** , especifique lo estrictos que deben ser los servidores de destinatarios al comprobar las autenticaciones SPF y DKIM de un correo electrónico.

   * **[!UICONTROL Relaxed]** mode: el servidor acepta la autenticación incluso si el correo electrónico se envía desde un subdominio,
   * **[!UICONTROL Strict]** El modo de solo acepta autenticación cuando el dominio del remitente coincide exactamente con un dominio SPF y DKIM.

   Digamos que estamos trabajando con el `http://www.luma.com` dominio. En el modo &quot;Relajado&quot;, los correos electrónicos procedentes del `marketing.luma.com` El servidor autorizará el subdominio, mientras que se rechazarán en el modo &quot;Estricto&quot;.

1. Clic **[!UICONTROL Add]** para confirmar la creación del registro DMARC.

Una vez procesada la creación del registro DMARC (aproximadamente 5 minutos), este se muestra en la pantalla de detalles de los subdominios. [Obtenga información sobre cómo supervisar registros TXT para los subdominios](gs-txt-records.md#monitor)