Las Props son la forma de enviar y recibir información en nuestros componentes. Son la forma de comunicar cada componente con el resto de la aplicación. Son muy parecidas a los parámetros y argumentos de las funciones en cualquier lenguaje de programación.

Los componentes de React utilizan props para comunicarse entre sí. Cada componente padre puede enviar información a sus componentes hijos mediante el uso de props. Las props pueden parecerte similares a los atributos HTML, pero permiten pasar cualquier valor de JavaScript a través de ellas, como objetos, arrays y funciones.
## Pasar props al component hijo 
Primero, pasa algunas props al elemento . Por ejemplo, vamos a asignar dos props: person (un objeto) y size (un número):

export default function Profile() {
  return (
    <Perfil
      person={{ name: 'keeevin', imageId: '36514635' }}
      size={100}
    />
  );
}
## Acceder a props dentro del componente hijo 
Puedes acceder a estas props especificando sus nombres person, size separados por comas dentro de ({ y }) justo después de function Avatar. Esto te permitirá utilizarlas dentro del código de Avatar como si fueran variables.

function Perfil({ person, size }) {
  ## se puede acceder a los valores de person y size desde aquí
}

Las props te permiten considerar de forma independiente los componentes padre e hijo. Por ejemplo, puedes modificar las props person o size dentro del componente Profile sin preocuparte por cómo serán utilizadas por el componente Perfil. De manera similar, puedes cambiar la forma en que Perfil utiliza estas props sin necesidad de revisar el componente Profile