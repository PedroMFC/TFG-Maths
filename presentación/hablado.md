# MATEMÁTICAS

### Desarrollo 
En primer lugar, presentamos un esquema  con los resultados/temas que se han desarrollado en el trabajo así como las relaciones entres los mismos. Este ha consistido principalmente en en el campo de la optimización, teoremas de la alternativa y su aplicación en el campo de las finanzas, que es el culmen de esta parte del trabajo. Más concretamente, esta última parte se centra en obtener el precio de las denominadas opciones de compra, que explicaremos más adelante, y que estudiaremos cómo varía en función de sus parámetros. Para este caso, ha sido preciso también una incursión en el mundo de las matemáticas financieras para conocer conceptos o el modelo de mercado con el que estamos trabajando.

### H-B y M-O-K 
El trabajo comienza con una versión muy simple del conocido teorema de Hanh-Banach, conocio como el teorema de Mazur-Orlicz-König. 

*Explicar las diferencias entre unos y otro*

El teorema de M-O-K nos sirve para probar el lema de **Simons** y que es un resultado cobre funciones convexas y cierta condición de optimalidad que nos dice que dos funciones distintas poseen el mimso ínfimo en un convexo.

### Gordan

Gracias al lema de Simons, podemos probar uno de los teoremas de la alternativa que se han estudiado, el Teorema de la Alternativa de Gordan. En realidad, se prueba una versión convexa del mismo que es más general y que es equivalente al lema de Simons.

*Explicar la versión convexa del mismo y decir que es más visual y explicarlo*

Otro de los teoremas de la alternativa que se ha tratado es el lema de Farkas y que se ha usado para demostrar el teorema de dualidad en programación lineal.

### Optmización
Una de las aplicaciones que le hemos dado al teorema de la alternativa de Gordan es el uso en optimización, que el campo original donde surgieron los teoremas de la alternativa. Por ejemplo, podemos probar el teorema de Fritz John que nos dice los siguiente

*Queremos encontrar las soluciones del problema (1) con f función objetivo, g las restricciones que es parecido al vector de los multiplicadores de Lagrange*

Este resultado tiene un problema y es posible que el lamba_0 es 0 y por ello, hacer que la función objetivo sea independiente de las restricciones. Esto se soluciona imponiendo la llamada condición de Magasarian-Fromovitz que nos asegura que los productos escalares de las derivadas de g con una dirección del espacio es negativa. Esto nos aporta el teorema de Karush-Kuhn-Tucker y que sí da el vector de multiplicadores de Lagrange.

### Minimax
La segunda aplicación del teorema de la alternativa de gordan es en la teoría minimax. Surgió de la mano de J. von Neuman en la toería de juagos aunque nosostros lo usaremos para probar resultados de separación de convexos.

*Explicar qué es un teorema minimax, superiormente semicontinua (más débil que continua ¿ejemplo?), destacar las mismas propiedad de ínfimo y en compactos que las continuas*


### Separación
Como hemos dicho, aplicamos la teoría minimax para obtener resultados de separación de convexos. La situación general de separación de convexos es la siguiente .... Si suponemos algunas hipétsis extra a los conjuntos (cerrado y compacto) obtenemos el siguiente resultado y que es equivalente al teorema de la alternativa de Gordan.

Gordan también nos sirve para probar otros teoremas de separaicón más débiles(tesis más hipóteis), solo en el ámbito finito dimensional.


### Preliminares financieros
Hemos dicho que la finalidad era obtener el valor de una opción de compra. 

(Pág. 72/80)

The importance of the first fundamental theorem should be clear: it
provides the vital link between the economically meaningful assumption of
the absence of arbitrage and the mathematical concept of the existence of
equivalent measures under which the discounted stock prices are martin-
gales. In generalising from the relatively simple context of finite market
models, one wishes to maintain the essential aspects of the equivalence
of these two conditions. In the continuous-time setting, however, the two
conditions are no longer equivalent and much work has gone into reformu-
lations that reflect the requirement that the market should be ‘essentially’
arbitrage-free while seeking to maintain a close link with the existence of
equivalent martingale measures.
