ENLACE DE PLATZI A LA CLASE 

https://platzi.com/home/clases/10002-python/70197-proyecto-final-guerra-naval/

Resumen

En este proyecto, crearás un juego de Batalla Naval (Battleship) en Python, donde dos jugadores colocan sus barcos en un tablero y se turnan para atacar las posiciones del oponente hasta que uno de los jugadores hunda todos los barcos del otro. Sigue estos pasos detallados para construir el juego.

Paso 1: Define la Clase Ship
Crea la clase Ship:
Define el constructor __init__ que reciba name y size como parámetros.
Agrega atributos: self.name, self.size, self.positions (una lista vacía para las posiciones del barco) y self.hits (inicializado en 0).
Método place_ship:
Este método coloca el barco en el tablero (board) según la posición inicial (start_row, start_col) y la dirección (direction).
Verifica si el barco cabe en el tablero. Si no cabe, devuelve False.
Si la posición está libre (' '), almacena las posiciones en la lista positions. Si no, devuelve False.
Actualiza el tablero con el símbolo del barco (self.name[0]), almacena las posiciones en self.positions, y devuelve True.
Método hit:
Incrementa el contador self.hits.
Devuelve True si el número de impactos (self.hits) es igual al tamaño del barco (self.size), indicando que el barco ha sido hundido.
Paso 2: Define Clases Específicas de Barcos
Crea las subclases:

Crea una clase Destroyer que herede de Ship y tenga un tamaño de 2.
Crea una clase Submarine que herede de Ship y tenga un tamaño de 3.
Crea una clase Battleship que herede de Ship y tenga un tamaño de 4.
class Destroyer(Ship):
    def __init__(self):
        super().__init__('Destructor', 2)

class Submarine(Ship):
    def __init__(self):
        super().__init__('Submarino', 3)

class Battleship(Ship):
    def __init__(self):
        super().__init__('Acorazado', 4)
Paso 3: Define la Clase Player
Crea la clase Player:
Define el constructor __init__ que reciba name como parámetro.
Crea un tablero self.board de 10x10, representado por una lista de listas, inicializado con espacios en blanco ' '.
Crea una lista self.ships para almacenar los barcos del jugador.
Crea un segundo tablero self.hits para registrar los ataques.
Método place_ships:
Crea instancias de Destroyer, Submarine y Battleship.
Para cada barco, pide al jugador que ingrese la fila, columna y dirección (H para horizontal, V para vertical) donde desea colocar el barco.
Llama a place_ship para intentar colocar el barco. Si no es posible, solicita nuevamente la entrada del usuario.
Método print_board:
Imprime el tablero de juego para mostrar la posición actual de los barcos o los impactos.
Método attack:
Solicita al jugador la fila y columna para atacar.
Verifica si la posición es válida y si el ataque es un impacto o agua.
Actualiza el tablero del oponente y el tablero de impactos del jugador en consecuencia.
Si se impacta un barco, verifica si ha sido hundido.
Método all_ships_sunk:
Devuelve True si todos los barcos del jugador han sido hundidos.
Paso 4: Define la Clase BattleshipGame
Crea la clase BattleshipGame:
Define el constructor __init__ que inicialice dos jugadores (player1 y player2).
Método play:
Pide a cada jugador que coloque sus barcos en el tablero.
Alterna turnos entre los jugadores para atacar el tablero del oponente.
Finaliza el juego cuando todos los barcos de un jugador han sido hundidos, declarando al otro jugador como ganador.
Paso 5: Ejecuta el Juego
Crea una instancia de BattleshipGame y llama al método play() para iniciar el juego.

game = BattleshipGame()
game.play()
Al ejecutar el programa, los jugadores podrán colocar sus barcos en el tablero y se turnarán para atacar hasta que uno de los jugadores hunda todos los barcos del oponente, ganando así el juego.

Este proyecto te permitirá practicar la manipulación de listas, clases, métodos, y cómo gestionar la interacción entre varias clases en Python.

¡Diviértete creando tu propio juego de Batalla Naval!