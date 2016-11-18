
# Música generativa para principiantes 
_"Así pues, el mundo oculto de que nos habla el físico contemporáneo es de esencia matemática" Gastón Bachelard en Estudios_
## ¿De qué se trata esto?
Imaginar los componentes musicales como organismos nos permite crear unidades generadoras con una serie de condiciones que podrían crear música.

Para este taller usaremos el lenguaje de programación [ChucK](http://chuck.cs.princeton.edu/) que nos permitirá hacer prototipos de soluciones a los retos propuestos.

+ El compositor que desea liberarse de la materialización estricta e inmovil de una creación.
+ Que larga dictadura la que a padecido la música bajo la pluma del compositor, 
+ Indicios de autonomía de la máquina
+ Algunos espíritus que solo soportan la aleatoriedad unos minutos
+ La vieja idea de una música producida por un grupo de algoritmos matemáticos
+ Cuando la formula empieza a ser más valorada que el resultado
+ La curiosidad de modelar matemáticamente el tipo de música electrónica que pone un DJ en la pista de baile


## Prácticas
Vamos a considerar algunos elementos de composición
### Groove / Agitación / Ritmo
#### => Genere un sonido rítmico
Escriba la forma más simple para que se genere un sonido cada determinado tiempo.   
+ Solución que genera un tick cada cierto tiempo: https://raw.githubusercontent.com/son0p/algo0ritmos/master/practicas/100while.ck
  

#### => Aplique una curva de probabilidad
Escriba una curva de probabilidad que describa los momentos en que un instrumento debe sonar o permanecer en silencio.
+ Solución con tres instrumentos (bombo, redoblante, charles): https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_agitation_001.ck


### Alturas / Melodías
#### => Genere notas aleatorias
Escriba una función que permita generar notas aleatorias
+ Solución que genera notas aleatorias sobre una base rítmica: https://github.com/son0p/algo0ritmos/blob/master/practicas/alturas_002.ck
+ Solución basada en la explicación de williamsharkey: https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_transients_001.ck
  + Despues de la nota raíz hay 100% de probabilidad que suene una octava arriba
  + Después de la octava arriba hay 50% de probabilidad que suene la nota raíz y 50% que suene la octava.
  
### Densidades / Armonías
#### => Genere acorde
Escriba una función que genere un acorde
+ Solución que genera un acorde apilando terceras mayores o menores: https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_densidad_001.ck
    
#### => Generador de progresiones armónicas
Escriba una función que seleccione una progresión armónica dentro de un grupo de opciones.

### Timbre / Textura / Color / Tesitura
#### => Variación de un filtro
Escriba una función que altere el centro de frecuencia de un filtro al final de cada compas.
+ Solución que filtra un ruido subiendo el centro de frecuencia al final del ciclo: https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_texture_001.ck 

### Intensidad / Volumetría / Dinámica
#### => Variación de la dinámica
Escriba una función que defina los acentos en un ritmo.
+ Solición que altera la dinámica de un hi hat según una curva fija: https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_dynamics_001.ck

### Espacialidad
#### => Generador de apertura
Escriba una un función que posicione los sonidos mas al centro o más hacia los lados según unas condiciones determinadas.
+ Solición que altera el paneo de un hi hat según una curva fija: https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_spaciality_001.ck

### Transientes
#### => Generador de transientes
Escriba una función que permita manipular el transiente de un sonido según unas condiciones.
+ Solución que va aumentando la presencia de un componente transiente en un bajo: https://github.com/son0p/algo0ritmos/blob/master/generatives/gen_transients_001.ck



## Rutinas

## Herramientas

### ChucK 
+ Descargar:  http://chuck.cs.princeton.edu/release/ 
 


### Algoritmos 
+  Concurso para determinar si un algoritmo que selecciona música como un DJ pasa el touring test ( via @danielgomezmarin ) http://bregman.dartmouth.edu/turingtests/algorhythms 

### Markov

+ A visual explanation by Victor Powell http://setosa.io/blog/2014/07/26/markov-chains/index.html

+  En este link explican como usar cadenas de markov para hacer strings( o textos) más confusos https://bwall.github.io/markov-chains-keyed-obfuscation/

##### Explicación de williamsharkey 

After a kick, there is a 100% chance of a snare. 
After a snare there is a 50% chance of a snare, and a 50% chance of a kick. 

Here is what the Probability matrix would look like: 

```
Code:
                c u r r e n t 

                kick   snare 
            +-----------------+ 
n   kick    |   0    |  0.5   | 
e           +--------+--------+ 
x   snare   |   1    |  0.5   | 
t           +--------+--------+
```

Is this not an elegant way to describe what is happening? It can be expanded for more states, perhaps a state for a woodblock, or a rest. 

Math stuff: 
1. Each column must add up to 1. That means there is a 100% chance that there is a "next time". 

2. "Whats the probability that 100 beats from now, it will play a snare?!" Well, just take the matrix to the 100th power. Then add up the column called snare. That's the answer! This assumes a 50/50 chance of starting on snare/kick.
Last edited by williamsharkey on Tue Dec 18, 2007 9:43 am; edited 1 time in total

## ¿Cómo replicar este taller?

