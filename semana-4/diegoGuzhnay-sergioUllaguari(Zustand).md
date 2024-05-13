    ##	Zustand

## Subtema: Gestión de estado con Zustand

Por: Sergio Iván Ullaguari & Diego Andres Guzhñay.

                                                      Introduccion:

Zustand por lo que investigamos es una herramienta muy innovadora recientemente
para mejorar el flujo de trabajo en el desarrollo de apps web utilizando React y TypeScript.
Combinando Zustand, la biblioteca de gestion de estado para React se implementa mejores practicas de TS para crear una experiencia de desarrollo mas fluida y segura.

Se explora como Zustand mejora de manera considerable el desarrollo de web modernas, hasta sus implementaciones mas avanzadas como gestion de estado pequeña, rapida y escalable que utiliza principios de flujo simplificados.

                                                       Reflexión:

Zustand tiene un enfoque minimalista pero poderoso para la gestion de estado en React, demostrando ser util en la exploracion hacia otros componentes.
Su API basada en hooks proporciona una experiencia de desarrollo comoda y familiar, que facilita su integracion en proyectos existentes y nuevos.

Con su uso permite estructurar una mogica de gestion de estado de una manera que se adapte a las necesidades y no restringirse por convenciones preestablecidas.

Con su gran capacidad para proporcionar un rendimiento excepcional sin sacrificar la simplicidad o escalabilidad.
A pesar de su tamaño compacto, no escatima en funcionalidad ni en robustez. Es un testimonio de cómo un diseño cuidadosamente elaborado puede ofrecer resultados sobresalientes.
Ventajas:

- Simplicidad: Esta biblioteca ofrece una documentacion facil de entender basada en hooks de React, facilitando el uso y adopcion para desarrolladores.

- Rendimiento: Al ser ligera y eficiente su rendimiento sigue en pie apesar de apps a gran escala sin sacrificar la velocidad de carga ni la capacidad de respuesta.

- Flexibilidad: Su gestion de estado no impone restricciones excesivas ni opiniones sobre la estructura de la app, permitiendo adaptar su uso segun las necesidades especificas del proyecto.

- Tipado estatico con TS: Zustand se integra con TS perfectamente, permitiendo definir tipos de estado precisos y detectar errores en tiempo de compilacion, lo que ayuda a escribir un codigo mas seguro y robusto.

- Resolucion de problemas comunes: La biblioteca aborda de manera efectiva errores comunes en la gestion de estado como el "problema del niño zombi", la concurrencia de React y la perdida de contexto entre renderizados mixtos, mejorando la estabilidad y la confiabilidad de la app.

                                                        Desventajas:

- Curva de aprendizaje inicial: Por su documentacion bien descrita y tutoriales que se ha encontrado Zustand de medianamente complejo de usar pero con el tiempo se familiariza con la API y patrones para su uso.

- Menos comunidad: La comunidad puede ser menos activa que otras bibliotecas de gestion mas establecidad.

                                                         Analogía:

Hay que imaginarse una casa en construccion que necesita un sistema de gestion para organizar todas las herramientas y materiales de construccion. En este escenario, Zustand seria como una caja de herramientas compacta pero robusta que propocionara todo lo necesario para mantener el sitio de construccion ordenado y eficiente.

    Simplicidad y Eficiencia: Al igual que una caja de herramientas bien organizada, Zustand ofrece una solución simple pero poderosa para gestionar el estado de tu aplicación. Tiene todas las herramientas esenciales que se necesita, pero sin la complejidad innecesaria que podría complicar el flujo de trabajo.

    Rendimiento y Robustez: Al igual que una caja de herramientas robusta y duradera, Zustand está diseñado para proporcionar un rendimiento excepcional y una fiabilidad sólida, incluso en proyectos de gran escala. Se puede confiar en él para mantener la aplicación funcionando sin problemas en todo momento.

    Soporte y Mantenimiento: Al igual que una caja de herramientas de calidad, Zustand viene con soporte integrado y actualizaciones periódicas para garantizar que siempre esté en óptimas condiciones. Siempre se puede contrar con él para ayudar a solucionar problemas y mantener la aplicación en funcionamiento.

                    Metodología para el Uso de Zustand en proyectos de React

1.  Instalación de Dependencias:
    Primero, se debe tener instaladas las dependencias necesarias. Utilizaremos zustand y @types/zustand para proporcionar tipado TypeScript.

        {npm install zustand @types/zustand}

2.  Diseño de la Arquitectura del Estado:
    Diseña la arquitectura del estado de la aplicación, definiendo qué datos se almacenarán en el estado global de Zustand y cómo se estructurarán. Considerar los diferentes "stores" que se necesitaran y cómo se relacionarán entre sí.

3.  Implementación de los Stores:
    Crea los stores de Zustand según el diseño de la arquitectura del estado. Utilizando la función createStore para inicializar cada store y define las acciones y selectores necesarios para interactuar con el estado.

Typescript:
{
// userStore.ts
import create from 'zustand'; //Importando la funcion 'create' de la biblioteca 'zustand' que se utiliza para crear un nuevo store en Zustand.

type User = { //Se define un tipo de datos 'user' que representa a un usuario de un app.
id: number;
name: string;
email: string;
};

type UserState = { //Se define un tipo de estado 'UserState' que representa el estado del store de usuario.
//Incluye la propiedad 'currentUser' que almacena el usuario actualmente autenticado o null si no hay usuario.
//La funcion 'setCurrentUser' se utiliza para actualizar el usuario actual.
currentUser: User | null;
setCurrentUser: (user: User) => void;
};

export const useUserStore = create<UserState>((set) => ({ //Exporta una variable llamada 'useUserStore' que contiene un nuevo store de Zustand.
//Se utiliza la funcion 'create' para crear el store, y se le pasa como argumento un callback que recibe una funcion 'set'. Dentro del callback, se inicializa como null y una funcion 'setCurrentUser' que utiliza una funcion 'set' para actualizar el estado del store con un nuevo usuario.
currentUser: null,
setCurrentUser: (user) => set({ currentUser: user }),
}));

}

4. Integración con Componentes:
   Integra los stores de Zustand en tus componentes de React utilizando los hooks proporcionados (por ejemplo, useStore). Accede al estado y a las acciones del store en los componentes para gestionar el flujo de datos y las interacciones del usuario.

Zustand useUserStore para mostrar un mensaje de bienvenida personalizado o un mensaje de inicio de sesión, dependiendo de si hay un usuario autenticado o no.

Typescript:
{
// NavigationComponent.tsx
import React from 'react';
import { useUserStore } from './userStore';
//Importa el hook useUserStore del archivo userStore.ts para acceder al estado del usuario almacenado en el store de Zustand.

const NavigationComponent: React.FC = () => {
//Define un componente funcional de React llamado NavigationComponent. Este componente no acepta props y devuelve un elemento React.

const { currentUser } = useUserStore();
// Utiliza el hook useUserStore para obtener el estado actual del usuario del store de Zustand. La destructuración se utiliza para extraer la propiedad currentUser del estado del usuario.

return (
<nav>
{currentUser ? (
<p>Welcome, {currentUser.name}!</p>
) : (
<p>Please log in.</p>
)}
</nav>
// Devuelve un elemento `<nav>` que contiene un mensaje de bienvenida personalizado si hay un usuario autenticado (`currentUser` no es nulo) o un mensaje de inicio de sesión si no hay ningún usuario autenticado. El mensaje de bienvenida incluye el nombre del usuario actual (`currentUser.name`), mientras que el mensaje de inicio de sesión simplemente dice "Please log in.".
);
};

export default NavigationComponent;
//Exporta el componente NavigationComponent como el componente predeterminado del archivo, lo que permite importarlo y utilizarlo en otros archivos de la aplicación.
}

5.  Pruebas y Depuración:
    Realizar pruebas para garantizar que los stores de Zustand funcionen correctamente en diferentes escenarios y condiciones. Utilizar herramientas de depuración como React Developer Tools para identificar y solucionar problemas potenciales.

6.  Optimización del Rendimiento:
    Se evalúa el rendimiento de los stores de Zustand y realiza optimizaciones según sea necesario. Considera técnicas como la memorización de selectores y la suspensión selectiva para mejorar la velocidad y la eficiencia de la aplicación.

7.  Documentación y Mantenimiento:
    Documentar adecuadamente los stores de Zustand, incluyendo su propósito, estructura y cómo interactuar con ellos. Manténer el código limpio y bien organizado, y asegúrse de seguir las mejores prácticas de desarrollo para facilitar futuras actualizaciones y mantenimiento.

8.  Monitoreo y Mejora Continua:
    Monitorizar el rendimiento y la estabilidad de los stores de Zustand en producción y realiza ajustes según sea necesario. Estar atento a las actualizaciones de la biblioteca y aprovechar las nuevas características y mejoras que se introduzcan.
                                                               Resumen:

En resumen su implementacion practica se integra facilmente en proyectos de React, permitiendo a desarrolladores crear stores personalizados y acceder al estado global de manera sencilla.

Ofreciendo una alternativa solida y eficiente para la gestion de estado en app web de React, especialmente cuando se busca una solucion ligera y compatible con TS, su simplicidad, rendimiento y compatibilidad lo convierte en una herramienta agil y muy valiosa para quienes buscan mejorar la calidad y la eficiencia de proyectos en React.

                                                         Blibliografia:


Patterson, C. (2021). "Introducing Zustand: The tiny State Manager for React". Medium. Disponible en: https://medium.com/swlh/introducing-zustand-the-tiny-state-manager-for-react-27c4f477b23e

Zustand Documentation.Disponible en: https://zustand.surge.sh/

TypeScript Documentation.Disponible en: https://www.typescriptlang.org/docs/

React Documentation.Disponible en: https://reactjs.org/docs/getting-started.html

Schackmann, J. (2020). "Zustand: A new way to handle state in React". Disponible en: https://react.christmas/2020/20
