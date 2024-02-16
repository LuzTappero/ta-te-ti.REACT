# ProyectoReact2

Explicación del codigo paso a paso

TURNS: Este objeto parece ser una constante que define los posibles valores de turno en el juego. En este caso, X representa al jugador X y O representa al jugador O.

Square: Este es un componente funcional que representa un cuadrado en el tablero del juego. Recibe las siguientes props:

children: Contenido dentro del cuadrado, posiblemente el valor del turno ('X' u 'O').
isSelected: Un booleano que indica si este cuadrado está seleccionado o no.
updateBoard: Una función que se llama cuando se hace clic en el cuadrado. Probablemente se use para actualizar el estado del tablero en el componente App.
index: El índice del cuadrado en el tablero.

Dentro de este componente, se define una variable className que se utiliza para aplicar una clase CSS condicionalmente. Si isSelected es true, se agrega la clase 'is-selected' a la clase 'square', lo que probablemente cambia el estilo visual del cuadrado para indicar que está seleccionado.

El componente renderiza un <div> que representa el cuadrado en el juego. Cuando se hace clic en este <div>, se llama a la función handleClick, que a su vez llama a updateBoard con el índice del cuadrado, lo que probablemente actualiza el estado del tablero en el componente App.

useState: Esta función es un hook de React que permite añadir estado a componentes funcionales. En este caso, board es un estado que representa el estado actual del tablero del juego, inicializado como un array de 9 elementos null (que representan los cuadrados vacíos del tablero). turn es un estado que representa el turno actual del jugador, inicializado como 'X' usando la constante TURNS.

updateBoard: Esta función se utiliza para actualizar el turno del jugador. Si el turno actual es 'X', cambia a 'O' y viceversa. Esta función se pasa como prop al componente Square y se ejecuta cuando un cuadrado se hace clic.

return: La función App retorna el JSX que representa la estructura del juego. Incluye un encabezado <h1> con el título del juego, un <section> que contiene los cuadrados del tablero (renderizados usando el componente Square en un bucle map), y otro <section> que muestra el turno actual del jugador ('X' o 'O') utilizando el componente Square.

Los cuadrados del tablero se renderizan como instancias del componente Square, cada uno con un índice único (key={index}) y el valor del cuadrado (board[index]), que se actualiza cuando el jugador hace clic en el cuadrado.
El componente Square que muestra el turno actual tiene la propiedad isSelected establecida en true si el turno actual coincide con el valor del cuadrado ('X' o 'O'). Esto probablemente se usa para resaltar visualmente cuál jugador tiene el turno.
