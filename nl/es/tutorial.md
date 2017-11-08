---

copyright:
  years: 2015, 2017
lastupdated: "2017-08-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# Guía de aprendizaje: Adición de prestaciones personalizadas
{: #tutorial}

Esta guía de aprendizaje le ayuda a comprender cómo aumentar las prestaciones de su agente virtual añadiendo sus propias prestaciones.
{: shortdesc}

En esta guía de aprendizaje utilizará el espacio de trabajo que habilita la sencilla demo de {{site.data.keyword.conversationshort}} para añadir nuevas prestaciones a su agente. El espacio de trabajo simula el rol de un copiloto de alguien que conduce un coche. Puede ver la demo [icono aquí![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://conversation-simple.mybluemix.net/ "Icono de enlace externo"){: new_window}. Después de importar el espacio de trabajo en la instancia de servicio de {{site.data.keyword.watson}} {{site.data.keyword.conversationshort}} enlazará el espacio de trabajo al agente. A continuación, añadirá las intenciones del espacio de trabajo como prestaciones personalizadas y finalmente solucionará los conflictos que surjan entre las prestaciones básicas y las prestaciones que añada.

## Objetivos de aprendizaje

Cuando haya completado esta guía de aprendizaje sabrá cómo realizar las tareas siguientes:

- Enlazar un espacio de trabajo al agente
- Utilizar un espacio de trabajo enlazado para añadir prestaciones personalizadas al agente
- Solucionar los posibles conflictos entre las prestaciones existentes y las nuevas prestaciones

Tardará aproximadamente 30 minutos en terminar esta guía de aprendizaje. Si explora
otros conceptos relacionados con esta guía de aprendizaje, puede tardar más.

### Requisitos previos

Debe tener una cuenta de {{site.data.keyword.Bluemix_notm}} y haberse registrado para utilizar el servicio {{site.data.keyword.IBM_notm}} {{site.data.keyword.watson}} {{site.data.keyword.conversationshort}}. Para
obtener más información, consulte
[Guía
de inicio ![Icono de enlace
externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/docs/services/conversation/getting-started.html#gettingstarted "Icono de enlace externo"){: new_window}.

### Resultados

Después de completar esta guía de aprendizaje, además de responder a las típicas preguntas de usuario sobre la empresa, su agente podrá responder a las preguntas y solicitudes que un conductor puede hacer a su copiloto, por ejemplo, *¿Cuándo crees que llegaremos?* o *Enciende la radio.*

### Lecciones de esta guía de aprendizaje

[Lección 1: Importación de un espacio de trabajo en {{site.data.keyword.conversationshort}}](tutorial.html#tutless1)

[Lección 2: Enlace de un espacio de trabajo](tutorial.html#tutless2)

[Lección 3: Adición de prestaciones personalizadas](tutorial.html#tutless3)

[Lección 4: Prueba de prestaciones personalizadas](tutorial.html#tutless4)

[Lección 5: Resolución de conflictos entre prestaciones](tutorial.html#tutless5)

## Lección 1: Importación de un espacio de trabajo a Conversación
{: #tutless1}

En esta lección, aprenderá cómo importar un espacio de trabajo en el servicio {{site.data.keyword.IBM_notm}} {{site.data.keyword.watson}} {{site.data.keyword.conversationshort}}.

### Antes de empezar

Debe tener una cuenta de {{site.data.keyword.Bluemix_notm}} y haberse registrado para el servicio {{site.data.keyword.IBM_notm}} {{site.data.keyword.watson}} {{site.data.keyword.conversationshort}}.

### Acerca de esta tarea

Para simplificar el proceso de creación de un espacio de trabajo de {{site.data.keyword.conversationshort}}, debe importar el archivo `car_demo_workspace.json` que contiene artefactos creados previamente a partir de la sencilla demo de {{site.data.keyword.conversationshort}}.

### Procedimiento

1.  Descargue el archivo [car_demo_workspace.json ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://watson-developer-cloud.github.io/doc-tutorial-downloads/virtual-agent/car_demo_workspace.json "Icono de enlace externo"){: new_window} en su sistema.
1.  [Inicie sesión en ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.ng.bluemix.net/dashboard/watson "Icono de enlace externo"){: new_window} en su instancia de servicio de {{site.data.keyword.IBM_notm}} {{site.data.keyword.watson}} {{site.data.keyword.conversationshort}}.
1.  Pulse **Launch tool (Herramienta de lanzamiento)**.
1.  Para importar un espacio de trabajo desde un archivo JSON, pulse el icono ![Flecha hacia arriba sobre una bandeja de entrada para indicar una acción de importación](images/workspace_import.png).
1.  Pulse **Choose a file (Seleccionar un archivo)** para buscar el archivo `car_demo_workspace.json` que ha descargado anteriormente.
1.  Seleccione **Everything (Intents, Entities, and {{site.data.keyword.dialogshort}}) (Todo (intenciones, entidades y {{site.data.keyword.dialogshort}}))** y a continuación pulse **Import (Importar)**.

### Resultados

El espacio de trabajo **Car Dashboard Tutorial (Guía de aprendizaje de salpicadero)** se añade a su instancia del servicio {{site.data.keyword.conversationshort}}.

## Lección 2: Enlazar un espacio de trabajo
{: #tutless2}

En esta lección aprenderá a enlazar un espacio de trabajo del servicio {{site.data.keyword.conversationshort}} al agente.

### Procedimiento

1.  En el menú de {{site.data.keyword.watson}} {{site.data.keyword.virtualagentshort}}, seleccione **Linked Workspaces (Espacios de trabajo enlazados)**.
1.  Pulse **Link Workspace (Enlazar espacio de trabajo)**.
1.  Seleccione la instancia del servicio {{site.data.keyword.conversationshort}} en el que ha importado el espacio de trabajo en la lección anterior.
1.  Seleccione el espacio de trabajo **Car Dashboard Tutorial (Guía de aprendizaje de salpicadero)**.
1.  Pulse **Link workspaces (Enlazar espacios de trabajo)**.

## Lección 3: Añadir prestaciones personalizadas
{: #tutless3}

En esta lección aprenderá a añadir prestaciones personalizadas al agente.

### Procedimiento

1.  En el menú {{site.data.keyword.watson}} {{site.data.keyword.virtualagentshort}} seleccione **Capabilities (Prestaciones)**.
1.  Pulse el separador **Custom capabilities (Prestaciones personalizadas)**.
1.  Pulse **Add Capabilities (Añadir prestaciones)**.
1.  Pulse el espacio de trabajo **Car Dashboard Tutorial (Guía de aprendizaje de salpicadero)** y a continuación pulse **Select Workspace (Seleccionar espacio de trabajo)**.

    Ahora en la página Prestaciones personalizadas aparece una lista de prestaciones.

## Lección 4: Prueba de prestaciones personalizadas
{: #tutless4}

En esta lección obtendrá más información sobre las prestaciones personalizadas que ha añadido.

### Acerca de esta tarea

Ahora que ha añadido prestaciones al agente averigüe lo que pueden hacer.

### Procedimiento

1.  En la cabecera de {{site.data.keyword.watson}} {{site.data.keyword.virtualagentshort}} pulse **Preview (Vista previa)**.
1.  Realice una pregunta que desencadene una prestación personalizada. Especifique el texto, *¿Podemos escuchar música?*

    El agente evalúa esta solicitud y la correlaciona con la propiedad personalizada **#turn_on (#encender)**. En el espacio de trabajo enlazado se utiliza el nodo del diálogo con una condición coincidente con la intención #encender. Como resultado, el agente pregunta qué género de música se desea reproducir.

    > **Nota:** puede ver con qué prestación está correlacionada la entrada del usuario porque el nombre de la prestación se visualiza como un enlace debajo de la respuesta.

1.  Especifique un género de música, por ejemplo, *Clásica* o *Rock* para completar el diálogo.
1.  Pulse **Edit (Editar)** al lado de la prestación identificada (#turn_on) en
la vista previa de historial para abrir la página de prestaciones.
1.  Ahora realice una pregunta que desencadene una prestación básica. Especifique el texto, *Cuéntame algo sobre ti*.

    Pulse **Edit (Editar)** al lado del enlace *Información del
sistema* para abrir la página de detalles de prestaciones. Cada una de las prestaciones básicas tiene su propia página de detalles de la prestación donde se puede personalizar la respuesta.

1.  Ahora intente confundir al agente especificando el texto, *¿Podemos escuchar algo de música?*

    El agente reconoce que ya ha solicitado la reproducción de música y así se lo indica.

## Lección 5: Resolución de conflictos entre prestaciones
{: #tutless5}

En esta lección aprenderá a resolver conflictos entre prestaciones básicas y prestaciones personalizadas.

### Acerca de esta tarea

Después de enlazar con su espacio de trabajo, se le notificará que existen conflictos entre las prestaciones básicas y algunas de las prestaciones que ha añadido.

| Prestación básica    | Prestación personalizada |
|--------------------|-------------------|
| Finalización             | #adiós         |
| Buscar tienda más cercana | #localizar_servicio   |
| Mensaje de bienvenida          | #bienvenida        |
| Garantía de seguridad | #fiabilidad_sistema  |

### Procedimiento

1.  Inhabilite las prestaciones personalizadas que opte por no utilizar.

    - La finalidad de las prestaciones `Finalización` y `#adiós` se solapa completamente. Para garantizar que los usuarios tienen una experiencia coherente cuando finalizan una conversación con el agente, debe optar por utilizar una u otra, pero no ambas.

        Es habitual crear lógica que se desencadena al final de una conversación. Para garantizar que el control sobre dicho comportamiento lo mantiene el agente virtual, utilizará la prestación básica `Finalización` y no la prestación personalizada.

    - Las prestaciones `Buscar tienda más cercana` y `#localizar_servicio` se solapan. Especifique las siguientes expresiones de ejemplo en el panel Vista previa para verlo por sí mismo:

        - *buscar la tienda más cercana* se direcciona a `#localizar_servicio`.
        - *buscar mi tienda* se direcciona a `Buscar tienda más cercana`.

        La prestación personalizada `#localizar_servicio` proporciona información sobre una gama más amplia de servicios además de una tienda, pero la prestación básica tiene una buena conversación incorporada asociada que recopila un código postal del usuario y devuelve la dirección de la tienda más cercana. Para beneficiarse el comportamiento incorporado, utilice la prestación básica `Buscar tienda más cercana`.

    - Las prestaciones relacionadas con la seguridad también se solapan. Para hacerse mejor una idea de qué tipos de entrada de usuario manejan cada una, especifique estas expresiones de ejemplo en el panel Vista previa.

        - *¿Mis datos están protegidos?* se direcciona a `Garantía de seguridad`.
        - *¿Puedo confiarte mi información?* se direcciona a `#fiabilidad_sistema`.

        La prestación `#fiabilidad_sistema` tiene datos de entrenamiento limitados en comparación con la prestación `Garantía de seguridad`, así que utilizará la prestación básica en lugar de la prestación personalizada.

    Para inhabilitar una prestación personalizada, debe suprimirla del espacio de trabajo {{site.data.keyword.conversationshort}}.
    1.  En la herramienta {{site.data.keyword.conversationshort}}, expanda la intención `#adiós` en la página Intenciones y, a continuación, pulse el icono **Delete intent (Suprimir intención)*** para suprimirla del espacio de trabajo.
    1.  Expanda la intención `#localizar_servicio` y a continuación pulse el icono **Delete intent (Suprimir intención)** para suprimirla del espacio de trabajo.
    1.  Expanda la intención `#fiabilidad_sistema` y a continuación pulse el icono **Delete intent (Suprimir intención)** para suprimirla del espacio de trabajo.

1.  Cuando realiza cambios en el espacio de trabajo personalizado, este se vuelve a entrenar automáticamente con los nuevos datos. Cuando se haya completado el entrenamiento del espacio de trabajo, vuelva a {{site.data.keyword.watson}} {{site.data.keyword.virtualagentshort}}.

    En la página Prestaciones, abra el separador **Custom Capabilities (Prestaciones personalizadas)** para confirmar que las prestaciones se han eliminado (`#adiós`, `#localizar_servicio` y `#fiabilidad_sistema`) ya no aparecen en la lista.

1.  Las prestaciones `Mensaje de bienvenida` y `#bienvenida` se solapan completamente entre ellas. Deseamos que el agente exhiba un comportamiento coherente y que tenga alguna personalidad. La prestación personalizada `#bienvenida` está diseñada para mostrar un tipo de personalidad específico que refleje la marca de la empresa, así que utilizará la prestación personalizada y no la prestación básica.

    Para inhabilitar una prestación básica, debe desactivarla.
    1.  En el separador **Core Capabilities (Prestaciones básicas)** de la página Prestaciones de {{site.data.keyword.watson}} {{site.data.keyword.virtualagentshort}}, busque la prestación `Mensaje de bienvenida`.
    1.  Pulse la ficha para abrirla y a continuación pase el conmutador de Encendido a **Off (Apagado)**. Pulse la flecha atrás para volver a la página principal de configuración.

1.  Realice pruebas adicionales especificando consultas de usuario de prueba en el panel Vista previa para confirmar que la capacidad adecuada maneja la entrada del usuario de la forma esperada. Por ejemplo, puede probar de nuevo las siguientes expresiones:

    - *¿Puedo confiarte mi información?* la debe manejar la prestación `Garantía de seguridad`.
    - *buscar la tienda más cercana* la debe gestiona la prestación `Buscar tienda más cercana`.

## Resumen de la guía de aprendizaje
{: #tutless_sum}

Mientras aprendía sobre {{site.data.keyword.watson}} {{site.data.keyword.virtualagentshort}} ha aumentado el agente con prestaciones personalizadas.

### Lecciones aprendidas

Al completar esta guía de aprendizaje, habrá aprendido los siguientes conceptos:

- Espacios de trabajo enlazados
- Prestaciones
- Prestaciones en conflicto
