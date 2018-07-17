## Toma 1: Presentación de Ret


--------------------------------
Hola, hoy trabajaremos sobre una teoría particular.
Sea 'tau ret' un tipo sin nombres de constantes, con nombres de funcion 'i' y 's', ambos de
aridad 2 y con un nombre de relación 'menor o igual' también de aridad 2.
Sea Ret la teoría de tipo 'tau ret' cuyo conjunto de axiomas es 'sigma Ret' , donde
sigma Ret es el siguiente conjunto de sentencias.


--------------------------------
Notemos que tenemos axiomas que hablan sólo con respecto a la relación 'menor o
igual' y otros que hablan, también, de las funciones 's' e 'i'
$$$$ Esperar 4 segundos

--------------------------------
Sobre esta teoría, daremos pruebas formales de las siguientes sentencias


--------------------------------
$$$$$$$$$ Esperar 4 segundos


--------------------------------

A partir de ahora, llamaremos FI a la primera sentencia y PSI a la segunda.
$$$$$$$$$ Esperar 6 segundos


# Toma 2

--------------------------------

Comenzaremos estudiando un poco qué significa cada axioma de Ret.

Observemos primero que una estructura 'A' satisface los 3 primeros axiomas de 'ret' si y solo si el par
[A, menor o igual supra A] es un poset.


--------------------------------

Otra observación importante es que una estructura A de tipo 'tau ret'  puede
satisfacer los 3 axiomas mencionados antes pero esto no implica que las
operaciones 'S supra A' e 'I supra A' deban ser las operaciones infimo y supremo
respecto al orden menor o igual supra A.


# Toma 3
--------------------------------


Notar que una estructura A que satisfaga los 3 axiomas del orden satisfará el
axioma 'A s es C' si y solo si cualesquiera sean los elementos 'a', 'b' [la
interpretación de s en A, aplicada a 'a' y 'b'] es cota
superior del conjunto formado por a y b en el poset (A, menor o igual supra A).



--------------------------------

Similarmente, una estructura A que satisfaga los 3 axiomas del orden cumplirá
'A s menor o igual C' si y solo si para todo 'a', 'b' [a s supra A b] es menor o
igual a toda cota superior del conjunto formado por a y b.


--------------------------------

Osea que lo anteriormente visto dice que una estructura A cumplirá los 5 axiomas
mencionados si y sólo si, [menor o igual supra A] es un orden parcial y
la interpretación de s en A es la operación supremo respecto del orden
[menor o igual supra A]


# Toma 4
--------------------------------

Razonando en forma similar obtenemos que una estructura A de tipo [tau ret]
satisface los axiomas de Ret, es decir es un modelo de Ret, si y solo si se
cumple la siguiente condición:

--------------------------------
(A, menor o igual supra A) es un orden parcial


--------------------------------
La interpretación de s en A es el supremo del poset


--------------------------------
La interpretación de i en A es el infimo del poset


# Toma 5

--------------------------------

A continuación mostraremos cómo encontrar una prueba formal en Ret de la
sentencia en pantalla.

$$$ ESPERAR 3 SEGUNDOS

Pero nosotros sabemos, por matemática básica, que en un modelo A de Ret la
operación [s supra A] es asociativa. Es decir, que todo modelo de Ret satisface
la sentencia a probar.


--------------------------------

La forma que utilizaremos para encontrar la prueba formal será la siguiente:


--------------------------------
Primero, haremos una prueba matemática, imaginando que somos un matemático que
piensa en un modelo genérico de Ret y prueba en forma elemental, la sentencia
FI. Aquí por elemental entenderemos que sólo se podrá escribir sentencias de
tipo tau ret con posibles constantes extras y, además, lo único que se puede
usar son los axiomas de Ret y las típicas deducciones usadas en las pruebas
matemáticas.

 Además, siempre imaginaremos un modelo genérico de Ret, es decir no podremos
 usar nada de algún modelo particular concreto ya que queremos que la prueba
 obtenida sea válida para cualquier modelo de Ret.


 --------------------------------

Luego, usando la prueba matemática como guía, construiremos la prueba formal.


# Toma 6
--------------------------------
Daremos entonces, primero, la prueba matemática de la sentencia FI.
Sea A un modelo fijo, pero arbitrario, de Ret
Sean a, b y c elementos de A fijos.


--------------------------------
Probaremos que '(a s b) s c' es menor o igual que 'a s (b s c)'


--------------------------------
Sabemos, por el axioma 'A s es cota' que
'a es menor o igual que 'a s (b s c)' ' y también que
'b s c es menor o igual que 'a s (b s c)''


--------------------------------
Si aplicamos nuevamente el axioma, pero esta vez sobre 'b s c', sabemos que
'b es menor o igual que (b s c)' y que
'c es menor o igual que (b s c)'

--------------------------------
Por dos y tres, y aplicando transitividad obtenemos
'b es menor o igual que 'a s (b s c)'


--------------------------------
 y por 2, 4 y transitividad obtenemos
'c es menor o igual que 'a s (b s c)'.

--------------------------------
Es decir que ahora hemos probado 7, 8 y 9



--------------------------------
Pero por el axioma 'A 's' es menor o igual que toda cota', tomando
'x igual a "a"', 'ye igual a "b"' y 'z igual a ("a s (b s c)")'
tenemos que
'(a s b) es menor o igual que 'a s (b s c)' '


--------------------------------
Y, finalmente, si aplicamos nuevamente el axioma, pero esta vez tomando
'x igual a (a s b)', 'y igual a c' y 'z igual a ('a' s (b s c))'

obtenemos que

''(a s b) s c' es menor o igual que 'a s (b s c)' '


-------------------------------
Y así, como a, b y c eran elementos cualesquiera, probamos de manera matemática
que la sentencia FI se cumple en 'A'.


-------------------------------

Ahora daremos la prueba formal en Ret de la sentencia en cuestión


--------------------------------

$$$$$ Esperar 1 seg        [1]

--------------------------------
Notemos que nos tomaremos una pequeña licencia del formalismo aplicando
más de una vez algunas reglas. Por ejemplo, en 2, aplicamos 2 veces la regla
de particularización.
En estos casos, el nombre de la regla irá seguido de [la letra X y el número
correspondiente a la cantidad de aplicaciones sucesivas de la regla]

$$$$$ Esperar 1 seg
--------------------------------

Notemos que en 1, 2 y 3 aplicamos el axioma (A s es cota) tomando
[x igual a 'a'] y [ye igual a (b s c)] para obtener
que [b s c es menor o igual a 'a s (b s c)'], como habiamos visto en la prueba
matemática.

--------------------------------

$$$$$ Esperar 1 seg      [4]
--------------------------------

Esta vez, en 1, 4 y 5 aplicamos el mismo axioma que antes, pero esta vez tomando [x igual a b] y [ye igual a c] para obtener que
[b es menor o igual a '(b s c)']
--------------------------------

$$$$$ Esperar 1 seg        [6]
--------------------------------

$$$$$ Esperar 1 seg        [7]
--------------------------------

En este caso, en 7 y 8, aplicamos el Axioma de transitividad tomando
[x igual a 'b', ye igual a (b s c) y 'z' igual a ('a' s (b s c))]

$$$$$ Esperar 1 seg

--------------------------------
Usando el resultado 6 y dada la aplicación del axioma expresada en 8, podemos
concluir, en 9, que [b es menor o igual que (a s (b s c))]. Como bien habiamos
visto en la prueba matemática

--------------------------------
$$$$$ Esperar 1 seg           [10]
--------------------------------
$$$$$ Esperar 1 seg           [11]
--------------------------------

Ahora, en 12, particularizamos el axioma de transitividad, pero esta vez tomando
[x igual a 'c', ye igual a (b s c) y 'z' igual a (a s (b s c))]
--------------------------------
Ahora bien, usando 11, podemos aplicar la regla de modusponens con 12 y así
concluir que [c es menor o igual a (a s (b s c))]. Resultado parcial
que se corresponde con el obtenido en la prueba matemática
--------------------------------
$$$$$ Esperar 1 seg           [14]
--------------------------------
$$$$$ Esperar 1 seg           [15]
--------------------------------
$$$$$ Esperar 1 seg           [16]
--------------------------------

Bueno, ahora en 16 y 17 particularizamos el axioma [A s es menor cota] tomando
[x igual a 'a', 'ye' igual a 'b'  y 'z' igual a (a s (b s c) )]
--------------------------------

Y utilizando 15 y la particularización en 17, obtenemos que
[(a s b) es menor o igual a (a s (b s c))].
--------------------------------

Por última vez, utilizamos la particularizacion del axioma de [A s es menor cota]
tomando [x igual a (a s b), ye igual a 'c' y z igual a (a s (b s c))]

--------------------------------

$$$$$ Esperar 1 seg           [20]
--------------------------------
Finalmente, igual que en la prueba matemática, por 20 y la particularizacion usada en 19, por modusponens, concluimos a que
[(a s b) s 'c' es menor o igual a ('a' s (b s c))]
--------------------------------
$$$$$ Esperar 1 seg           [22]
--------------------------------
Y así, notar que dado que no hay ninguna constante que dependa de 'a', 'b' o 'c',
podemos usar la regla de generalización para concluir que nuestro resultado es
válido para todo 'x', todo 'ye' y todo 'z'.


----------------------------------------------------
--------------------------------

Ahora encontraremos una prueba formal en Ret de la sentencia Psi
Notese que Dis1 nos dice que se cumple la distributividad de i respecto del s.
Y la sentencia 'CansDobl' nos dice que en la estructura puede interpretarse
como una ley de cancelación doble en el sentido de que si x e y son elementos
para los cuales hay un z tal que se cumplen las igualdades [que corresponden,
agregarlas] entonces podemos cancelar tal 'z' y obtener la igualdad [x = y]


--------------------------------

Para ello, utilizaremos la misma metodología que usamos anteriormente:
Primero buscamos la prueba matemática y luego la formal.



--------------------------------

Usaremos el teorema auxiliar en pantalla, el cual llamaremos a partir de ahora
"teoremaAbsorv".

Recomendamos que se realice la prueba del mismo como ejercicio.



--------------------------------

Ahora estamos en condiciones de dar la prueba matemática de la sentencia que
queríamos.


--------------------------------

Primero supongamos que se cumple Dis1, es decir que
(para todo x), (para todo ye) y (para todo z) se da que
[(x i y) s (x i z)] es igual que [x i (y s z)]



--------------------------------

Probaremos, entonces, que se cumple CansDobl, es decir la propiedad en pantalla
[esperar 3 segundos]



--------------------------------

Sean a y b dos elementos de A fijos


--------------------------------

Probaremos, entonces, que se cumple la siguiente propiedad:
[esperar 4 segundos]


--------------------------------

Supongamos que se cumple el antecedente de la implicación, es decir la sentencia en pantalla.
[esperar 2seg]


--------------------------------

Sea 'c' un elemento que cumple con la propiedad expresada en el antecedente.

Es decir:
[(a i c) es igual que (b i c)] y que [(a s c) es igual a (b s c)]


--------------------------------

Probemos entonces que ['a' es igual a 'b']



--------------------------------

Por TeoremaAbsorv, sabemos que

[(b s c) i b] es igual que 'b'

--------------------------------------------------------------

--------------------------------

Así, por el resultado (2) sabemos que [(a s c) es igual que (b s c)], por lo que

[(b s c) i b] es igual que [(a s c) i b]



--------------------------------

Y por Dis1, tenemos que

[(a s c) i b] es igual que [(a i b) s (c i b)]


--------------------------------

Aplicando, nuevamente, el resultado 2 obtenemos que

[(a i b) s (c i b)] es igual que [(a i b) s (c i a)]


--------------------------------

Ahora, de nuevo por Dis1 y por conmutatividad de i (cuya prueba se deja
para el estudiante), sabemos  que

[(a i b) s (c i a)] es igual que [(b s c) i a]


--------------------------------

Y así, por 2

[(b s c) i a] es igual que [(a s c) i a]



--------------------------------

Finalmente, por el TeoremaAbsorv demostrado anteriormente,

[(a s c) i a] es igual que 'a'



--------------------------------

Pero esto quiere decir que
'a' es igual que 'b'



--------------------------------

Como 'a' y 'b' eran elementos cualesquiera de A, hemos demostrado que,
se cumple CancDobl
--------------------------------


Por lo tanto, cumple la sentencia inicial que queriamos probar.



--------------------------------

Ahora procederemos a dar la prueba formal en Ret de la sentencia en cuestión


--------------------------------

Para hacerla, utilizaremos los siguientes teoremas cuyas pruebas formales son dejadas
al lector

--------------------------------

[esperar 3 segundos]


--------------------------------

Primero, tomamos como hipótesis inicial la hipótesis del enunciado que queremos
probar. Es decir, Dis1.
$$$$$ Esperar 1 seg           
--------------------------------
Ahora, tomaremos la segunda hipótesis del enunciado fijando
[x igual a 'a' y 'ye' igual a 'b']

--------------------------------
En 3 aplicamos la regla de eleccion con constante 'e'.


--------------------------------

$$$$$ Esperar 1 seg           [4]
--------------------------------

En 4 y 5 particularizamos el TeoremaAbsorv tomando [x igual a 'b' y 'ye' igual a 'e']

--------------------------------
$$$$$ Esperar 1 seg           [6]
--------------------------------

Dados los resultados 5 y 6, podemos aplicar la regla de reemplazo y así obtener
que [(a s e) i b es igual a 'b']

--------------------------------

$$$$$ Esperar 1 seg           [8]
--------------------------------

$$$$$ Esperar 1 seg           [9]
--------------------------------

$$$$$ Esperar 1 seg           [10]
--------------------------------

Particularizamos el TeoremaConmut tomando [x igual a 'b' y ye igual a (a s e)]
para luego aplicar el reemplazo entre 7 y 10
--------------------------------

En 8, particularizamos la hipótesis 1 tomando
[x igual a 'b', ye igual a 'a' y z igual a 'e'] para luego aplicar el reemplazo
entre 8 y 11, y así obtener que [(b i a) s (a i e) es igual a 'b'] como vimos
en la prueba matemática
--------------------------------
$$$$$ Esperar 1 seg           [13]
--------------------------------
$$$$$ Esperar 1 seg           [14]
--------------------------------
$$$$$ Esperar 1 seg           [15]
--------------------------------
En 13, 14 y 15 aplicamos una serie de reglas para luego, en 16, aplicando el
TeoremaConmut obtener que [(a i b) s (a i e) es igual a b]
--------------------------------
$$$$$ Esperar 1 seg           [17]
--------------------------------
$$$$$ Esperar 1 seg           [18]
--------------------------------
$$$$$ Esperar 1 seg           [19]
--------------------------------
$$$$$ Esperar 1 seg           [20]
--------------------------------

En 17, 18, 19 y 20, utilizamos la particularización de la hipótesis 1 y aplicando una
serie de reglas, análogas a las que aplicamos en la prueba matemática, obtenemos
en 21 que [(a s e) i a es igual a 'b']
--------------------------------
Ahora bien, si particularizamos el TeoremaAbsorv con
[x igual a 'a' y ye igual a 'e'] claramente obtenemos que
(a s e) i a es igual a 'a'
--------------------------------

Lo cual, por los resultados 21 y 22, tal y como vimos en la prueba matemática,
nos dice que [a es igual a 'b'].

--------------------------------
Y así, podemos cerrar el bloque correspondiente a la Hipotesis 2
--------------------------------
Y así, dado que ni en la sentencia 24 ni en sus Hipotesis ocurren constantes que dependan de 'a' o de 'b' se puede generalizar y concluir 25.


--------------------------------
Luego, podemos cerrar el bloque de la Hipotesis 1 y así concluir la sentencia que buscábamos.

--------------------------------
