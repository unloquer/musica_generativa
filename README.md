
# Música generativa para principiantes 
## ¿De qué se trata esto?
Imaginar los componentes musicales como organismos nos permite crear unidades generadoras con una serie de condiciones que podrían crear música.

Para este taller usaremos el lenguaje de programación [ChucK](http://chuck.cs.princeton.edu/) que nos permitirá hacer prototipos de soluciones a los retos propuestos.
## Prácticas
Vamos a considerar algunos elementos de composición
### Groove / Agitación / Ritmo
#### => Genere un sonido rítmico
Escriba la forma más simple para que se genere un sonido cada determinado tiempo.   
+ Solución que genera un tick cada cierto tiempo https://raw.githubusercontent.com/son0p/algo0ritmos/master/practicas/100while.ck
  

#### => Aplique una curva de probabilidad
Escriba una curva de probabilidad que describa los momentos en que un instrumento debe sonar o permanecer en silencio.
+ Solución con tres instrumentos (bombo, redoblante, charles) https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_agitation_001.ck


### Alturas / Melodías
#### => Genere notas aleatorias
Escriba una función que permita generar notas aleatorias
+ Solución que genera notas aleatorias sobre una base rítmica https://github.com/son0p/algo0ritmos/blob/master/practicas/alturas_002.ck
  
### Densidades / Armonías
#### => Genere acorde
Escriba una función que genere un acorde
+ Solución que genera un acorde apilando terceras mayores o menores https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_densidad_001.ck
    
#### => Generador de progresiones armónicas
Escriba una función que seleccione una progresión armónica dentro de un grupo de opciones.

### Timbre / Textura / Color / Tesitura
#### => Variación de un filtro
Escriba una función que altere el centro de frecuencia de un filtro al final de cada compas.

### Intensidad / Volumetría / Dinámica
#### => Variación de la dinámica
Escriba una función que defina los acentos en un ritmo.

### Espacialidad
#### => Generador de apertura
Escriba una un función que posicione los sonidos mas al centro o más hacia los lados según unas condiciones determinadas.

### Transientes
#### => Generador de transientes
Escriba una función que permita manipular el transiente de un sonido según unas condiciones.



## Rutinas

## Herramientas

### ChucK 
+ Descargar:  http://chuck.cs.princeton.edu/release/ 
 


### Algoritmos 
+  Concurso para determinar si un algoritmo que selecciona música como un DJ pasa el touring test ( via @danielgomezmarin ) http://bregman.dartmouth.edu/turingtests/algorhythms 

### Markov
+ A visual explanation by Victor Powell http://setosa.io/blog/2014/07/26/markov-chains/index.html

+  En este link explican como usar cadenas de markov para hacer strings( o textos) más confusos https://bwall.github.io/markov-chains-keyed-obfuscation/

## ¿Cómo replicar este taller?

