                 Afectación de React al ciclo de vida de un componente.
1. Ciclo de vida de un componente
Cuando creamos un componente de clase, tenemos la ventaja, que al extenderlo de React.Component nos va a proporcionar más métodos y propiedades, que van a mejorar de manera exponencial el componente.
Ejemplo:

class Title extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!!!</h1>;
  }
}

ReactDOM.render(<Title name="Mauricio" />, document.getElementById("root"));

Para entender mejor el ejemplo, es necesario saber qué React.Component, tiene tres ciclos de vida:
1 Montaje (Mounting)
Cuando se crea una instancia de un componente y se inserta en el DOM
2 Actualización (Updating)
Cuando sufre algún cambio las propiedades (props) o el estado (state) del componente.
3 Desmontaje (Unmounting)
Cuando el componente se elimina del DOM.

Informacion extraida de Medium: https://mauriciogc.medium.com/3-react-ciclo-de-vida-de-un-componente-propiedades-y-estado-a1b1d9965af1

Analogia

Imaginemos que tenemos una planta en nuestra casa

-El estado seria la condicion actual de la planta: El estado de dicha planta puede cambiar con el tiempo, puede estar creciendo, floreciendo o marchitandose. El estado de la planta puede ser influenciado por diferentes factores , como la cantidad de agua, etc.

-El ciclo de vida seria como las diferentes estapas de crecimientos de la planta, desde que plantas la semilla hasta que la planta madura y florece. Cada etapa tiene sus propias características y necesidades específicas.

Ahora como se relaciona esto con React

El Estado de un componente de React es como la condición actual de la planta: Puede cambiar con el tiempo en respuesta a eventos o interacciones del usuario. Por ejemplo, un componente puede estar mostrando información, esperando una respuesta del servidor, o en un estado de error.

El Ciclo de Vida de un componente de React es como las diferentes etapas del crecimiento de la planta: El componente pasa por diversas etapas, como el montaje, la actualización y el desmontaje. Cada etapa tiene sus propias funciones y se ejecutan en momentos específicos durante la vida útil del componente.

Resumen

Así como cuidar una planta requiere entender y responder a sus necesidades en cada etapa de su crecimiento, trabajar con el Estado y Ciclo de Vida en React implica comprender cómo manejar y responder a los cambios en el estado de un componente en cada etapa de su ciclo de vida.

Link del repositorio anterior, donde subi la teoria a tiempo:
https://github.com/kevinnncr/teoriacolaboratva.git


