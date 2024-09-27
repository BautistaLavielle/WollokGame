# Bombs and Coins - 1 vs 1

## Objetivo del Juego
El objetivo del juego es que cada jugador recolecte 5 monedas que van apareciendo en posiciones aleatorias del mapa. Sin embargo, deben tener cuidado, ya que pueden colocar bombas y morir si colisionan con las explosiones. Además, hay un bot en el mapa que también coloca bombas al ser tocado por un jugador.

## Configuración del Juego

### Mapa
- **Player 1**: Comienza en la esquina inferior izquierda.
- **Player 2**: Comienza en la esquina superior derecha.
- **Bot**: Aparece inicialmente en el centro del mapa.

<img src="assets readme/Inicio readme.jpg" alt="Inicio del juego" style="width:50%;"/>


### Controles

#### Player 1
- **Movimiento**:
  - `W`: Moverse hacia arriba.
  - `S`: Moverse hacia abajo.
  - `A`: Moverse hacia la izquierda.
  - `D`: Moverse hacia la derecha.
- **Colocar Bomba**: Barra espaciadora (`space`).

#### Player 2
- **Movimiento**:
  - `Flecha arriba`: Moverse hacia arriba.
  - `Flecha abajo`: Moverse hacia abajo.
  - `Flecha izquierda`: Moverse hacia la izquierda.
  - `Flecha derecha`: Moverse hacia la derecha.
- **Colocar Bomba**: Tecla `Enter`.

#### General
- **Reiniciar el Juego**: Si uno de los jugadores logra recolectar 5 monedas, o si se presiona `R` se reinicia el juego, colocando en 0 el contador de monedas y en 1 el contador de bombas de ambos jugadores. Además, reaparecen tanto los jugadores como el bot en sus posiciones iniciales, y se muestra un cartel que dice 'Game Over'.

<img src="assets readme/Reinicio readme.jpg" alt="Reinicio del Juego" style="width:50%;"/>


## Dinámica del Juego

### Recolección de Monedas
- Las monedas aparecen en posiciones aleatorias del mapa.
- Al recolectar una moneda, el contador de monedas del jugador aumenta en 1.
- Para recolectar una moneda es necesario colisionar con la misma.
- Cuando un jugador recolecta una moneda, también aumenta su contador de bombas en 1, permitiéndole colocar una bomba adicional.

<img src="assets readme/Monedas readme.jpg" alt="Recoleccion de monedas" style="width:50%;"/>

### Colocación de Bombas
- Cada jugador comienza con la posibilidad de colocar una bomba (contador de bombas = 1).
- Al colocar una bomba, el contador de bombas del jugador disminuye en 1.
- La bomba explota después de un breve período de tiempo.
- **Explosión de la Bomba**: Forma una cruz que ocupa la casilla en la que se colocó la bomba y dos casillas en cada dirección (izquierda, derecha, arriba, abajo).
- Si un jugador colisiona con la explosión de una bomba, muere.

<p align="center">
  <img src="assets readme/Bombas readme.jpg" alt="Colocacion de bombas" style="width:40%;"/>
  <img src="assets readme/Explosiones readme.jpg" alt="Explosion de bombas" style="width:40%;"/>
</p>


### Muerte y Reaparición
- Si un jugador muere:
  - Pierde 1 moneda de su contador de monedas.
  - Reaparece en su posición original (esquina inferior izquierda para Player 1 y esquina superior derecha para Player 2).
- Los jugadores no pueden salir de los límites del mapa.

### Bot
- El bot se mueve aleatoriamente por el mapa cada un tiempo corto.
- Si un jugador colisiona con el bot, el bot coloca una bomba idéntica a las que colocan los jugadores.

## Fin del Juego
El juego termina cuando uno de los jugadores logra recolectar 5 monedas. 

¡Buena suerte y que gane el mejor!
