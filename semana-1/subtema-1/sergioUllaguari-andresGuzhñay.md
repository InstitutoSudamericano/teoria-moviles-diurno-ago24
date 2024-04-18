                        “Fundamentos de React & JSX”

Ventajas y desventajas de JSX en el desarrollo de aplicaciones React

Por:  Sergio Iván Ullaguari & Diego Andres Guzhñay.

                                    Resumen

En el contexto del desarrollo de aplicaciones utilizando React, un framework para la construcción de UI interactivas.
JSX permite al desarrollador de React escribir código con la particularidad que combina elementos de JavaScript y XML.

                                Introduccion

El framework React ha sido adoptado para mejorar la productividad de los desarrolladores asi pudiendo optimizar sus aplicaciones.
Suele presentar desafíos únicos y decisiones criticas que los equipos de desarrollo deben resolver cuidadosamente.
Se trata de profundizar en los aspectos positivos y negativos de JSX.

                                    Ventajas                         

1.- Sintaxis familiar: JSX esta basado en HTML, lo que facilita a el desarrollador front-end que como lenguaje nativo se acostumbra rápidamente a la implementación de React, reduciendo asi la curva de aprendizaje.

2.- Mezcla de HTML y JavaScript: Esto permite combinar las expresiones fácilmente dentro de la estructura de la UI.
Esto facilita el trabajar con datos dinámicos y lógica en un mismo lugar de la UI.

3.- Verificación de errores tempranos: JSX se compila en JavaScript antes de subir al navegador. Pudiendo React reconocer errores de sintaxis u lógica durante el tiempo de compilación.

4.-Optimización del rendimiento: Siendo la compilación encargada, React puede optimizar el rendimiento durante el proceso de compilación, como eliminar código basura y la compresión del tamaño del archivo final. 
Mejorando su rendimiento.

                                 Desventajas   

1.- Curva de aprendizaje inicial: Aunque JSX se parezca a HTML, puede resultar algo desafiante para desarrolladores que no acostumbra a usar dicho lenguaje o solo usan plantillas ya adaptadas.

2.- Necesidad de herramientas de construcción: Para utilizar JSX en un proyecto React, de requiere usualmente un framework para compilar el código JSX en JavaScript que se puede interpretar por el navegador.

3.- Posible confusión entre JavaScript y HTML: Al mezclar JavaScript y HTML dentro de JSX, puede ser difícil diferenciar y tener una separación clara entre la lógica de la APP y su UI, lo que desencadenaría problemas al llevar un código menos legible y mantenible si no se maneja correctamente.

4.-Posible sobrecarga cognitiva: En casos el desarrollador acude a trabajar con plantillas lo que le puede resultar abrumador y llevar a una mayor carga cognitiva durante el desarrollo.
 

                                Metodología

En revisión de paginas web, literatura y analizando con IA las cualidades del lenguaje se pudo evaluar el rendimiento y usabilidad de APP en React.

                    Implementación JSX en un componente React

{import React from 'react';

Se importa el módulo React.}

{const hello = () => {}

Se define un componente funcional llamado hello.

Dentro de la función flecha, se utiliza JSX para definir la estructura de la interfaz de usuario del componente.}

{return (
    <div> 
      <h1> Hello World</h1>
      <p>JSX</p>
    </div>
);

Se devuelve un elemento <div> que contiene un encabezado <h1> y un párrafo <p>, todo escrito usando la sintaxis de JSX.}

{export default hello;

El componente se exporta al final del archivo para que pueda ser utilizado en otros archivos de React.}  

                                Conclusiones

React es una librería adecuada en muchos tipos de proyectos distintos, permite un desarrollo ágil, ordenado y con una modularidad que se mantiene, focalizada en componentes y que ofrece un constante desarrollo.