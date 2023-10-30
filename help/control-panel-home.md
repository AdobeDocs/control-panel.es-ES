---
title: Documentación del producto
description: Documentación del Panel de control.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: 5980b9d978e20996ac58fb730a286f0c0b92b781
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 62%

---

# Centro de ayuda {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="Acerca del Panel de control"
>abstract="La página de inicio del Panel de control le permite acceder a todas las acciones que se pueden realizar en las instancias de Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=es" text="Acceso al Panel de control"

El Panel de control de Campaign le ayuda a aumentar la eficiencia de su trabajo como administrador de productos de las versiones 7 y 8 y de Campaign Standard, lo que le permite administrar la configuración y rastrear los usos de cada una de sus instancias de Campaign.

## Novedades

**Interfaz de usuario**

* El Panel de control de Campaign ya está disponible en otros idiomas. [Más información](discover/using/discovering-the-interface.md#supported-languages-languages)

**Supervisión de perfiles activos**

* Ahora puede monitorizar el número de perfiles activos a los que tiene derecho para su organización y el recuento total de perfiles utilizados en su organización en todas las instancias, si utiliza varias instancias. [Más información](performance-monitoring/using/active-profiles-monitoring.md)

**Registros DMARC**

* Ahora, varias direcciones de correo electrónico pueden recibir correos electrónicos de informes acumulados e informes de errores. [Más información](subdomains-certificates/using/dmarc.md)
* Se han realizado cambios si existen registros DMARC y BIMI para un subdominio:

   * Los registros DMARC no se pueden eliminar. Si desea eliminar uno, primero debe eliminar el registro BIMI.
   * Los registros DMARC se pueden editar, pero no se permite reducir la categoría de la directiva a &quot;Ninguno&quot; y su valor porcentual debe ser 100.

>[!CAUTION]
>
>* El acceso al Panel de control está restringido a los usuarios administradores. [Más información](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=es#discover-control-panel)
>
>* Para la versión 7 de Campaign, se aplican restricciones de implementación. [Más información](faq.md#v7-restrictions)

## Recursos adicionales {#additional-resources}

<table>
    <tr>
        <td><b>Campaign Standard</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/control-panel-overview.html?lang=es">Tutoriales en vídeo de Panel de control</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=es">Documentación del producto de Campaign Standard</a></li>
        </ul>
        </td>
        <td><b>Versión 7 de Campaign</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/control-panel-overview.html?lang=es">Tutoriales en vídeo de Panel de control</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic/using/campaign-classic-home.html?lang=es">Documentación del producto de la versión 7 de Campaign</a></li>
        </ul>
        </td>
        <td><b>Versión 8 de Campaign</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-learn/control-panel/control-panel-overview.html?lang=es">Tutoriales en vídeo del Panel de control</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/campaign-home.html?lang=es">Documentación del producto de Campaign v8</a></li>
        </ul>
        </td>
    </tr>
</table>
