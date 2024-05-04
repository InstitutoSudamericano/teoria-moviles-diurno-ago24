# MANEJO DE EVENTOS Y HOOKS EN REACT

## Teoría:

React te permite añadir controladores de eventos a tu JSX. Los controladores de eventos son tus propias funciones que se ejecutarán en respuesta a interacciones como hacer clic, hover, enfocar inputs en formularios, entre otras.
Para agregar un controlador de evento, primero definirás una función y luego la pasarás como una prop a la etiqueta JSX apropiada. Por ejemplo, este es un botón que no hace nada todavía.
En el contexto del desarrollo de software, la teoría puede referirse a los principios y conceptos fundamentales que sustentan la programación, la arquitectura de software, entre otros aspectos.

## Reflexión:

Las funciones controladoras de evento:

Usualmente están definidas dentro de tus componentes.
Tienen nombres que empiezan con handle, seguido del nombre del evento.
Por convención, es común llamar a los controladores de eventos como handle seguido del nombre del evento. A menudo verás   `onClick={handleClick}` , `onMouseEnter={handleMouseEnter}` , etcétera.

Por otro lado, puedes definir un controlador de evento en línea en el JSX:
En el desarrollo de software, la reflexión puede referirse a la capacidad de un programa para examinar y modificar su propia estructura y comportamiento durante la ejecución.

## Analogía:

La analogía es una herramienta cognitiva que consiste en establecer una relación de semejanza entre dos cosas o situaciones diferentes.
En el ámbito académico, la analogía se utiliza para explicar conceptos complejos mediante la comparación con situaciones más familiares o simples.
En el desarrollo de software, la analogía puede utilizarse para explicar conceptos de programación mediante comparaciones con situaciones cotidianas.

## Resumen:

Recapitulación
Puedes controlar eventos pasando una función como prop a un elemento como  `<button>`.
Los controladores de eventos deben ser pasados, ¡no llamados!  `onClick={handleClick}` , no  `onClick={handleClick()}`.
Puedes definir una función controladora de evento de manera separada o en línea.
Los controladores de eventos son definidos dentro de un componente, así pueden acceder a las props.
Puedes declarar un controlador de evento en un padre y pasarlo como una prop al hijo.
Puedes definir tus propias props controladoras de evento con nombres específicos de aplicación.
Los eventos se propagan hacia arriba. Llama e.stopPropagation() en el primer parámetro para evitarlo.
Los eventos pueden tener comportamientos por defecto del navegador no deseados. Llama e.preventDefault() para prevenirlo.
Llamar explícitamente a una prop controladora de evento desde un controlador hijo es una buena alternativa a la propagación.

https://es.react.dev/learn/responding-to-events


