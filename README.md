PAC-MAN · edición Windows
Juego completo de Pac-Man para Windows, en un único ejecutable nativo (PacMan.exe), sin instalador, sin dependencias externas y sin conexión a Internet.
Intro animada e interactiva: Pac-Man huye de los fantasmas, aparece una píldora, se la come y pasa a perseguirlos (con puntos flotantes), con música de fondo propia.
Juego: laberinto clásico de 28 × 31, 242 puntos, 4 píldoras de poder, 4 fantasmas con personalidad propia, 10 niveles con un premio distinto en cada uno, melodía de fondo, vidas y pausa.
Pantalla de felicitación animada al terminar cada nivel, distinta en cada uno de los 10.
Después del nivel 10 puedes seguir jugando otra vuelta de 10 niveles (sumando puntos y con la dificultad acumulada) o terminar y guardar la puntuación; el final es una pantalla de felicitación animada con trofeo, confeti y el rótulo FIN. Si te quedas sin vidas, Game Over.
Tablón de puntuaciones: al terminar una partida buena escribes tu nombre y queda en un fichero cifrado (records.dat); el tablón se muestra solo en la pantalla de inicio cuando pasas unos segundos sin empezar.

Cómo jugar
Doble clic en PacMan.exe.
Tecla	Acción
Flechas o W A S D	Mover a Pac-Man
ENTER / Espacio	Empezar · saltar la felicitación · confirmar el nombre · volver del tablón
BORRAR	Borrar una letra al escribir el nombre
C	En la pantalla final: seguir jugando otra vuelta
P	Pausa
M	Silenciar / activar todo el sonido (música incluida)
F11 o Alt+Enter	Pantalla completa / volver a ventana
Botón ⛶ (esquina superior derecha)	Pantalla completa con el ratón
ESC	Salir de pantalla completa · pausa · omitir el nombre · salir
Los puntos de la esquina son píldoras de poder: al comerlas los cuatro fantasmas se vuelven azules durante unos segundos (también los que todavía están dentro de su casa) y puedes comértelos (200, 400, 800 y 1600 puntos seguidos). Al final del efecto parpadean en blanco antes de recuperar su color.
Al comer la píldora, Pac-Man hace una animación: se enciende un resplandor a su alrededor, salen tres anillos que se expanden y el personaje da un pequeño rebote. Además:
La música cambia a una melodía más rápida y tensa mientras dura el efecto, y vuelve a la original en cuanto termina.
Un fantasma que te comes vuelve a la casa y sale sin el efecto de esa píldora: sale de color normal y listo para cazarte, aunque a los demás les quede tiempo azul. La siguiente píldora sí le afecta otra vez.
Cada nivel tiene dos apariciones de su fruta de premio (a los 70 y a los 170 puntos comidos); comerla da puntos extra. El premio del nivel se muestra en la esquina inferior derecha.
Los 10 premios
Nivel	Premio	Puntos
1	Cereza	100
2	Fresa	300
3	Naranja	500
4	Manzana	700
5	Melón	1.000
6	Galaxian	2.000
7	Campana	3.000
8	Llave	5.000
9	Estrella	7.000
10	Corona	10.000
Al comer los 242 puntos de un nivel aparece la pantalla de felicitación, rediseñada:
panel con marco doble, medallón con el número de nivel, título con sombra, frase distinta en cada nivel y el premio en grande sobre un pedestal;
fondo con degradado propio de cada nivel y una decoración tenue distinta (lluvia de puntos, fuegos artificiales, globos, lluvia de frutas, fantasmas en órbita, estrellas fugaces, confeti, Pac-Man gigante, ondas de color o corona con rayos);
debajo corre la misma escena de la intro, en bucle y un poco más rápida: la huida, la píldora, el destello, los fantasmas azules y la persecución con sus puntos flotantes.
Dura 8,5 segundos (con barra de progreso) o se salta con ENTER.
Objetivo: superar los 10 niveles para llegar al final.
Tablón de puntuaciones
Al terminar una partida (superando los 10 niveles o perdiendo las 3 vidas), si la puntuación entra en el tablón se pide el nombre: 4 caracteres (A-Z y 0-9, siempre en mayúsculas; se escribe en cuatro casillas con cualquier letra, también A, S, D y W), ENTER para guardar, BORRAR para corregir y ESC para omitir.
Se guardan las 8 mejores puntuaciones con el nivel alcanzado y la fecha.
El tablón vive en records.dat, junto al ejecutable, cifrado: AES-256-CBC con IV aleatorio, clave derivada con SHA-256 y comprobación de integridad. En el fichero no se leen los nombres ni las puntuaciones, y si alguien lo manipula se descarta al cargar (el juego arranca sin tablón).
Si dejas la pantalla de inicio 10 segundos sin empezar, aparece el tablón unos segundos y vuelve sola a la pantalla inicial (ENTER también vuelve).

Qué hay dentro
Intro
Una escena de persecución en bucle, con personajes grandes:
Pac-Man entra huyendo y los cuatro fantasmas le persiguen de cerca.
A los pocos segundos aparece una píldora de poder parpadeando.
Pac-Man se la come (destello) y los fantasmas se vuelven azules.
Ahora es él quien los persigue: se los va comiendo y salen los puntos flotantes (200, 400, 800, 1600) mientras los comidos se van en forma de ojos y reaparecen.
Fundido y vuelta a empezar.
Los personajes envuelven por los lados como en los túneles del laberinto, así que la persecución nunca se sale de la pantalla. Debajo están las instrucciones, el récord guardado y «PULSA ENTER PARA JUGAR» con un pulso de color.
Juego
Laberinto clásico dibujado con contornos azules, puntos y píldoras parpadeantes.
Movimiento por casillas con giros en las intersecciones y túneles que dan la vuelta por los lados.
Cuatro fantasmas con IA distinta:
Blinky (rojo): persigue directamente a Pac-Man.
Pinky (rosa): apunta 4 casillas por delante.
Inky (cian): combina la posición de Pac-Man y Blinky.
Clyde (naranja): persigue de lejos y se dispersa al acercarse.
Alternancia dispersión / persecución por fases, como el original, y salida escalonada de la casa de los fantasmas.
Modo asustado, fantasmas comidos que vuelven a su casa siguiendo un mapa de distancias (y vuelven a salir), muerte con animación, vidas, pausa y Game Over.
Colisión "barrida": se comprueba todo el recorrido del frame, no solo la posición final, así que Pac-Man y los fantasmas no pueden cruzarse sin tocarse aunque el juego vaya a pocos FPS.
Dificultad creciente: los fantasmas aceleran nivel a nivel y el efecto de las píldoras dura algo menos.
Récord persistente en pacman_record.txt (se crea junto al ejecutable).
Después de los 10 niveles
Al superar el nivel 10 aparece la pantalla de decisión, con trofeo y confeti:
C — Seguir jugando: empieza otra vuelta de 10 niveles conservando los puntos. La dificultad sigue subiendo (los fantasmas van algo más rápidos y las píldoras duran menos), el marcador muestra «VUELTA n» y se pueden encadenar tantas vueltas como quieras.
ENTER — Terminar y guardar: pasa al final del juego y luego registra la puntuación en el tablón (si entra entre las 8 mejores, te pide el nombre).
Final
Pantalla de felicitación animada: trofeo, confeti, «¡ENHORABUENA!» con pulso, la puntuación final, el récord, el desfile de Pac-Man persiguiendo a los fantasmas y el rótulo FIN.
Sonido
Efectos generados por código (ondas cuadradas en memoria): comer puntos, píldora, fantasma comido, fruta, muerte, nivel superado, victoria y Game Over. Además hay música de fondo en bucle: en la pantalla principal suena una melodía de arpegios rápidos con onda cuadrada, al estilo del arcade original; en la partida, otra más tranquila; y una tercera, más rápida y tensa, mientras dura el efecto de la píldora de poder; una melodía tranquila en el tablón de puntuaciones (y mientras escribes el nombre); y una fanfarria alegre en las felicitaciones de nivel y en la pantalla de decisión final. El jingle de inicio también es una carrera ascendente tipo arcade. Todas se generan por código, sin ficheros de audio. La música se detiene al pausar, al morir y en las pantallas de felicitación, y M la silencia junto con los efectos.
Animación al comer la píldora
Resplandor alrededor de Pac-Man, tres anillos que se expanden y un rebote del personaje durante 0,7 s, a juego con el cambio de música.
Animación de muerte
Cuando un fantasma atrapa a Pac-Man, este gira, abre la boca hasta desaparecer, suelta chispas y termina en un pequeño destello, en lugar de simplemente encogerse.
Pantalla completa
Botón ⛶ en la esquina superior derecha (con el ratón), F11 o Alt+Enter. El juego se escala manteniendo la proporción y se centra con bandas negras; ESC vuelve a la ventana.

Detalles técnicos
Icono propio: el ejecutable lleva el icono de Pac-Man (16, 24, 32, 48, 64, 128 y 256 px, con transparencia) incrustado como recurso, y la ventana lo usa en la barra de título y en la barra de tareas. El icono del proyecto es PacMan.ico y se incrusta al compilar con /win32icon:PacMan.ico (no se regenera).
Lenguaje: C# 5, Windows Forms (GDI+), un solo archivo fuente: PacMan.cs.
Compilado con el csc.exe que ya incluye Windows (.NET Framework 4.8), sin Visual Studio ni paquetes externos: PacMan.exe es un binario nativo de ~40 KB.
Bucle a ~60 FPS con Timer y delta time; doble búfer para evitar parpadeos.
Funciona en Windows 7 SP1 o superior con .NET Framework 4.x (incluido de serie en Windows 10/11).
