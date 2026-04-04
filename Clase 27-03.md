#**CLASE P5.JS**

####**Algoritmo**

Es una secuencia de instrucciones paso a paso, LOGICAS, DEFINIDAS, FINITAS Y ORDENADAS, que permiten solucionar un problema o realizar una tarea especifica, tiene 4 caracteristicas fundamentales:

1)**Precision**: Cada paso debe estar detallado Y CLASRISIMO (sin tantas vueltas y ambiguedades)

2)**Orden**: Los pasos llevan una secuencia logica

3)**Finitud**: Tiene que terminar en un algun momento; no puede ser infinitouuuu

4)**Definicion**: Si sigues el mismo algoritmo 2 veces con los MISMOS DATOS, deberias obtener el mismo resultado!

- !LA MINISCULA Y LA mayuscula son super importantes!
- con el comando + + : se agranda la interfaz
- SI queremos MOVIMIENTO lo tenemos que colocar en **function draw**, si NO queremos MOVIMIENTO, osea que quede con estela, lo colocamos en **setup**
- No es necesario repetir los codigos en una misma figura, si cambiamos AHI SI, los escribimos de nuevo
- **comando + shift** te ORDENA el CODIGO AUTOMATICAMENTE
- SIEMPRE colocar al final del codigo **;**

###ESTRUCTURA

* Input (Entrada) : La info o los ingredientes que necesitas para empezarrr
  * Proceso:Los pasos logicos que transforman esa entrada **ALGORITMO**
    * Output (Salida):El resultado FINAL O LA SOLUCION AL PROBLEMA
--------------------------------------------------------------------------------

##**Diagrama de flujo**

-----> Representación grafica de un algoritmo o de los pasos de un proceso. En programacion, se utiliza como herramienta de planificacion para visualizar la logica de un programa antes de escribir una sola linea de codigo.

----> Se usan componentes ESTANDAR (**simbologia**), para que cualquier programdor pueda entenderlo
![imagen SIMBOLOGIA diagrama flujo](https://images.ctfassets.net/w6r2i5d8q73s/2n2DPUtFMSCmiP5s5Jdzii/ca83a6fa0cddeed0b4b10784058f627c/simbolos_diagrama_flujo.jpg) 

----------------------------------------------------------------------------------------

##LENGUAJES DE PROGRAMACION

- Existen entre 900 y 700 lenguajes de programacion que se utilizan actualmente en la industria , la academia y el desarrollo de software professional
- Si incluimos lenguajes antiguos (en desuso tamb), lenguajes creados para la invest, dialectos especificos,etc...,supera los 9.000 segun repositorios como (online historical encyclopaedia of progamming languages)

- **Proposito general** : Python,Java,C++,C#
- **Desarrollo web** : JavaScript,TypeScript, PHP, Ruby
- **Sistema de bajo nivel** : C, Rust, Go
- **Analisis de datos** : R, Phyton, Julia
- **Movil** : Swift (Ios), Kotlin (Android)

  ---------------------------------------------------------
#**P5.JS**  (Utiliza principalmente **JavaScript**)

**OJITO** SIEMPREEE SE TERMINA COLCOANDO UN ; para cerrar el codigo si no puede tener problemas!!!!!
**OJOOO PIOJOO** SIEMPRE TIENE QUE ESTAR UNA LLAVE  que se llama fuction draw ----> } , AL FINAL , SI NO LOS CODIGOS SALEN CON ERROR

-Libreria de JavaScript ----> P5.JS no es un lenguaje nuevo desde cero, sino un library de JavaScript, Que signifca esto? : Que usa toda la potencia y la sintaxis de JavaScript PEROOO te REGALA un "vocabulario" especializado para dibujar, animar y crear cosas visuales de forma mucho mais sencilla.

**FUNCIONES MAESTRAS**

1) Setup () { : Se utiliza para crear el lienzo (), Se ejecuta una vez al principio
  * Su proposito: Configurar el entorno inicial
  * Que pasa aqui? : Defines el tamaño del lienzo (createCanvas), cargas imagenes o sonidos y estableces configuraciones QUE NO CAMBIARAN (como el color del fondo inicial)

2) Draw (){ : Se ejecuta en un bucle infinito (normalmente 60 veces x segundo / lo que permite crear animaciones OMGG)
  * Su proposito: Crear movimiento y responder a la interaccion en tiempo real
  * Que pasa aqui? : Dibujos fromas que cambian de pocision, detectas donde esta el raton o cambias colores gradualmente)

----------------------------------------------------------------
**{CREATE CANVAS}**   (siempre va dentro del setup)

Sintaxis ----> createCanvas([width], [height], [renderer], [canvas]);
EJEMPLO ----> createCanvas(100, 100);

- createCanvas (width, height); ----> Sirve para para crear el lienzo del canvas y determinar su tamaño en pixeles, solo de ponde una vez y SIEMPRE dentro del setup();
- [Renderer] ----> Define el motor del renderizado (es para crear cosas 3D)
  * **P2D (default)** : Es el modo 2D, Es el que usas por defecto si no escribes nada. Esta optimizado para formas basicas, texto e imagenes planas.
    * **WEBG**: Activa el modo 3D, Utiliza la tarjeta grafica (**GPU**) de tu computadora. Es **indispensable** si quieres usar funciones como **box(), sphere(), luces o texturas complejas**.
        * **[Canvas]** : Este es el parametro "oculto" y menos utilizado, pero súper útil si eres desarrollador web. Por defecto, p5.js crea un elemento <canvas> nuevo y lo pone en tu HTML.
     
--------------------------------------------------------------------------------
**{BACKGROUND}**

Sintaxis ----> background(v1, v2, v3, [a]);

EJEMPLO ----> background(250, 150, 228,150);

- background(v1,v2,v3, [a]); -----> Nos sirve para designar **EL COLOR** de nuestro lienzo canvas / Se puede poner en el setup(); o en el draw(), pero TIENES RESULTADOS DIFERENTES
- [v1,v2,v3] ----> Son los valores de **R,G,B**. La profe nos dejo paginas para buscar colores por su codigo
  * [Htmlcolorcodes](https://htmlcolorcodes.com/)
  * [Colorspickers](https://colorspicker.net/es/#google_vignette)
- [a] ----> Es el parametro para el canal alpha, nos sirve para darle **semitransparencia** al color del fondo (0-255) / DONDE **1** es MUY transparente y **255** MUY poco transparente (se puede usar sin este parametro igual).

#BACKGROUND ESCALAS

- Escala de grises (1 n°): background(220); (donde 0 es negro y 255 blanco)
- Color RGB (3 n°): background(255,0,0) (Rojo, Verde, Azul)
- Nombres de los colores : background('blue'); (siempre entre comillas)
- Transparencia (4 n°) : background(0, 0, 255, 50); (R,G,B y el cuarto numero es el canal **"Alpha"**) osea colocamos un numero en el cuarto. 

ESPACIO DE COLOR RGB 
- R: Red [0 - 255]
- G: Green [0 - 255]
- B: Blue [0 - 255]
- WHITE : (255,255,255)
- BLACK : (0,0,0)
- colorMode(RGB); ese es el codigo
 
ESPACIO DE COLOR HSV/ HSB
- H: Hue [0 - 360o]
- S: Saturation [0 - 100%]
- B: Brightness [0 - 100%]
- colorMode(HSB); ese es el codigo (SE coloca en el SETUP!) , Ejemplo: Si le queiro bajar el brillo a un morado y que este en lila, simplemente pongo colormode y lo bajo.

ESPACIO DE COLOR HSL
- H: Hue [0 - 360o]
- S: Saturation [0 - 100%]
- L: Lightness [0 - 100%]
- colorMode(HSL); ese es el codigo

--------------------------------------------------------
Pongo el background en setup(); o en el draw(); ? -------> La pocision del background() determina si tu dibujo tiene "memoria" o si se "limpia" constantemente (igual yo lo coloco en el setup() abajo. 

-------------------------------------------------------------
**{DIBUJAR EN EL P5.JS}**

- Para dibujar ahi, tenemos que entender que el Canvas FUNCIONA CON UN **SISTEMA DE COORDENADAS** **(x,y)** como un plano cartesiano , pero hay que tener en cuenta que el punto (0,0) NO esta en el CENTRO, sino en la esquina superior izquierda.
- X es horizontal e Y es en vertical
- Ejemplos: el punto de la esquina derecha seria 400x400 (porque eso mide el canvas 400x400) , el de la izq al final seria (0,400), el de la dere (400,0) y el punto medio seria 200x200

![plano cartesiano](https://p5js.org/_astro/coordinates.DW7JVAkD_Z13e1Vf.png) 

------------------------------------------------------------------------------
#**FIGURAS GEOMETRICAS**

- point(x, y); ----> Dibujamos un solo pixel en las coordenadas dadas.
- line(x1, y1, x2, y2); ----> Dibujo una linea desde un punto inicial hasta un punto final
- rect(x, y, ancho, alto); ----> Dibujo un rectangulo, por defecto, x e y definen la esquina superior izquierda
- ellipse(x, y, ancho, alto); ----> Dibujo un ovalo o circulo, a diferencia del rectangulo, x e y definen el centro de la figura
- circle(x, y, diámetro); ---> Es una version simplificada de la elipse cuando quieres un círculo perfecto
- square(x, y, lado); ----> Es un rectangulo donde todos los lados son iguales
- triangle(x1, y1, x2, y2, x3, y3);----> Necesitamos siosi darle las coordenadas de sus tres esquinas
- quad(x1, y1, x2, y2, x3, y3, x4, y4);----> Un cuadrilatero, sirve para hacer formas irregulares de cuatro lados

-------------------------------------------------------------------------------------
#**{TAMAÑO DEL BORDE}**

- strokeWeight(); ----> Establece el tamaño del borde de las figuras o el ancho de la linea o punto / SIEMPRE SE PONDE ARRIBA DE **Stroke();**
  * Sintaxis: strokeWeight(weight);
     * Ejemplo: strokeWeight(25);

- noStroke(); ----> Se usa para que la figura este sin borde

--------------------------------------------------------------------------------------
#**{COLOR DEL BORDE}**

- stroke(); ----> Establece el color que se utiliza para dibujar puntos, lineas y contornos de figuras. Se pone SIEMPREEE arriba de la linea de codigo de la figura
  * Sintaxis: stroke(v1, v2, v3, [alpha]);
    * Ejemplo: stroke(245, 0, 0);
   
-------------------------------------------------------------------------------------
#**{FORMA DEL BORDE/LINEA}**

-strokeCap(); ----> Define la forma del borde de las lineas o el borde de la figuras (por defecto siempre es ROUND, pero esta tamb SQUARE Y PROJECT)
  * Sintaxis: strokeCap(cap);
    * Ejemplo: strokeCap(SQUARE);

-------------------------------------------------------------------------------------------
#**{RELLENO DE COLOR}** 

-fill(); ----> Establece el COLOR DE RELLENO DE LA FIGURA, se pone ARRIBA SIEMPRE de la figura que quiero pintar
  * Sintaxis: fill(v1, v2, v3, [alpha]);
    * Ejemplo: fill(252, 159, 216); (aqui se colocan los numeros del color RGB)

 ------------------------------------------------------------------------------------
 #**{FIGURAS GEOMETRICAS 2D AVANZADAS}** 

 -arc(); ---> Nos sirve para hacer arcos o medios circulos. X e Y SON LAS COORDENADAS del centro del circulo que contiene este arco, W y H SON LA ANCHURA Y EL ALTO del circulo que contiene este arco, STAR y STOP es DONDE COMIENZA y TERMINA el angulo de este arco.
   * Sintaxis: arc(x, y, w, h, start, stop)
    * Ejemplo: arc(250, 250, 100, 100, 270, 90)

 - **angleMode(DEGREES)**: La profe dijo que lo activaramos en el **function setup()** PORQUE es mas facil controlar los angulos con este codigo
  * En p5.js (y en la mayoria de los lenguajes de programación), el grado 0 NO está arriba, sino a la derecha (en el eje X positivo) , **Y se mueve en el sentido del reloj**

  - **0° / 0 rad:** A las 3 en punto (derecha)
  -  **90° / HALF_PI:** A las 6 en punto (abajo)
  - **180° / PI:** A las 9 en punto (izquierda)
  - **270° / (PI + HALF_PI):** A las 12 en punto (arriba)

![reloj angulos](https://s3.eu-central-1.amazonaws.com/studysmarter-mediafiles/media/1865576/summary_images/SexaCircunferencia.svg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4OLDUDE42UZHAIET%2F20260329%2Feu-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260329T231817Z&X-Amz-Expires=604800&X-Amz-SignedHeaders=host&X-Amz-Signature=dad677852c0af742a1c7079a843809ac60d2d802edbefe2ac796842ea94a5d1d) 

--------------------------------------------------------------------------------------------------------------------------------------------
**#SOLEMNE 1**

- Debemos hacer un dibujo en un papel milimetrado,  inspirandonos en un artista que haga obras geometricas o abstractas , puede ser de 25x25 o 50x50 (mejor estaaaa/ para que calce mejor en el canvas de p5.js)
- La entrega debe tener formato de bitacora (Github), en donde debemos presentar nuestro proyecto, comentar sobre el proceso de replica que hicimos ( de quien nos inspiramos , porque?, etcc...) , las dificultades encontradas y sus soluciones, el resultado, el código (comentado SUPERR IMPORTANTE COMENTAR AL LADO SIEMPRE) y el link a su proyecto en el editor de p5.js. Además incluir fotos de su dibujo y W.I.P.
- SE **entrega** con **link directo GITHUB** y la bitacora de github de las clases anteriores que tenemos anotada SERA EVALUADA TAMBBB

- **SE ENTREGA ANTES DEL 10 DE ABRIL, OBVIOO ANTES DE LA CLASE!!!**
- Los desafios tienen que estar publicos, YA ENTREGUEE!!!
