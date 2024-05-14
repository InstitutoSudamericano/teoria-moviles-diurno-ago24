## Arquitectura Mutable

## Teoría
La arquitectura mutable es un enfoque en el que el estado general de una aplicación puede ser modificado directamente. En Zustand, se utiliza la función set para actualizar el estado, lo que permite realizar mutaciones directas sin necesidad de seguir una metodología estrictamente inmutable, estas actualizaciones de manera eficiente, notificando a los componentes solo cuando hay cambios relevantes, utilizando selectores y comparaciones superficiales para optimizar el rendimiento​. A diferencia de  otras bibliotecas como Redux donde el estado es inmutable y para hacer alguna actualización primero necesitamos crear una nueva copia del estado.

## Reflexión

Usar la arquitectura mutable puede llegar a ser beneficiosa en muchos casos ya que nos ofrece simplicidad y esto básicamente se refiere a un código más limpio y fácil de mantener. Sin embargo, es importante considerar que la mutabilidad puede introducir riesgos si no se maneja adecuadamente, como la posibilidad de efectos secundarios no controlados o dificultades en el seguimiento del estado.

## Analogia 

Podemos comparar esta arquitectura mutable con una libretita de notas reutilizable, donde puedes borrar y reescribir directamente sobre las páginas cuando necesitas actualizar alguna información. En contraste, Redux sería como una serie de notas adhesivas en las que, cada vez que necesitas cambiar algo, debes escribir una nueva nota y pegarla encima de la anterior.

## Resumen

La arquitectura mutable nos ofrece una forma directa y más eficiente de gestionar los estados en aplicaciones de React, ya que al permitirnos modificar directamente el estado nos ayuda a reducir el código y simplifica el desarrollo sobre todo en proyectos mas pequeños 
pero es importante utilizar esta capacidad con precaución para evitar problemas potenciales relacionados con efectos secundarios no controlados. 
