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
Hemos dicho que la finalidad era obtener el valor de una opción de compra. Una opción de compra es un contrato que da al comprador el derecho pero no la obligación de comprar o vender un activo determinado al vendedor de la mima ***EJEMPLO***. El pricipio de arbitraje es por su parte, una de los conceptos más importantes que tenemos en nuestro modelo de mercado y lo que nos dice es que no podemos obtener beneficio sin correr riesgo, lo que hace que las opciones de compra en principio sean una desventaja para el vendedor de la misma. Por eso es necesrio fijar un precio inicial para adquirir el contrato, y es el problema a resolver.

### Martingalas

*The importance of the first fundamental theorem should be clear: it provides the vital link between the economically meaningful assumption of
the absence of arbitrage and the mathematical concept of the existence of
equivalent measures under which the discounted stock prices are martin-
gales. In generalising from the relatively simple context of finite market
models, one wishes to maintain the essential aspects of the equivalence
of these two conditions. In the continuous-time setting, however, the two
conditions are no longer equivalent and much work has gone into reformu-
lations that reflect the requirement that the market should be ‘essentially’
arbitrage-free while seeking to maintain a close link with the existence of
equivalent martingale measures.*

El teorema que nos interesa para resolver este problema (y para el que es necesario el teorema de separación visto) es el primer teorema fundamental de asiganción de precios. Este nos dice que en nuestro mercado tenemos ausencia de arbitraje si, y solo si, tenemos una medida martingala equivalente. Es MUY IMPORTANTE ya que nos da el vínculo necesario entre la idea económica de ausnecia de arbitraje y el concepto matemático. Que sigan una martiganla no resulta extraño ya que los elementos de la filtación F nos indican la información acerca de la evolución de los precios, entonces la esperanza condicionada solo nos indica que estamos calculando el valor esperado a partir de lo que conocemos hasta ahora. Además, para que el mercado sea “justo”, dicho valor en el futuro debería ser, en media, el que tenemos ahora.

### Precio
En nuestro caso consideramos un modelo binomial en que en cada instante de tiempo, los precios varían según la probabilidad mostrada. La medida martingala equivalente es al que hemos llamado Q y que hace que los precios actualizados se comporten según una martingala es la que se muestra (en función del retorno que es el precio en un paso entre el anterior y que es una manera habitual de ber cómo varía el precio). Destacamos que el q se le suele de nominar probabilidad de riesgo neutral. Es un objeto matemático abstracto que no
tiene que coincidir con la probabilidad real del mercado o estar relacionada con la misma y que de hecho, se conoce a priori. Sin embargo, para la valoración de opciones se utiliza q ya que es la que hace que los precios actualizados se comporten según una martingala tal y como acabamos de probar.

El precio entonces viene dado por la fórmula que vemos donde es primer paso es para actualizar los precios y lo otro poe la distribución binomial básicamente.

### Estudio del valor
* *r*: es quizás la más interesante desde el punto de vista del vendedor de
la opción. El parámetro r es en cierto modo subjetivo ya que es una estimación del
valor que tendrá el dinero en el futuro. Por ello, según los valores fijados de d y u
puede ver con qué interés obtiene el mayor beneficio. Es claro que si r menor que 0 significa que el dinero en el futuro tendrá menos valor y es una situación que en principio no la contemplamos ya que suponemos que el valor del dinero aumentará en un futuro. De todos modos, se han usado valores negativos para ver su evolución. Para r ≥ 0 vemos que en este caso la función alcanza un máximo que como hemos dicho es el valor más favorable al vendedor.
* *K*:  . Esta situación podemos considerar que es la esperada. Cuanto menor sea el precio más posibilida des tiene el propietario de ejercerla ya que es raro que en el futuro la acción tenga ese valor tan bajo. Por ello, el vendedor tiene que exigir un mayor. Por otro lado, cuanto mayor sea el precio acordado es el comprador el que corre un mayor riesgo de no ejercerla en el futuro por lo que tiene que pagar menos por ella ahora.

# INFORMÁTICA

### Problema
Es una técnica que se engloba dentro del campo de la Informática Gráfica y que se aplica a una gran cantidad de sectores: diseño industrial, arte, cine, medicina, etc. Por ejemplo, en el mundo artístico se emplea para la obtención de un modelo digital de la obra con el fin de tener una copia digital de la misma u obtener más información que puede ser de utilidad, como en los procesos de restauración, sin necesidad de tener el original. 

Los pasos que se siguen en el proceso de obtención suelen ser :

* Alinear: poner las tomas desde el mismo sistema de referencia. TRATAMOS EN ESTE
* Fusionar: eliminar repetidos.
* Triangular: construir malla.

### ICP

El primer algorimto que tratamos es el ICP (iteración sobre el punto más cercano). Primero suponemos que tenemos dos conjuntos con el mismo número de puntos y que tienen correspondencia en el orden. Entonces para minimzar la distancia meida entre ambos lo que se debe hacer es calcular los valores propios de esta matriz (que es la definición del artículo original aunque hemos visto cómo se obtiene en la memoria), esocgemos el mayor y el vector propio asociado representa la rotación pero en forma de cuaternio. Y la traslación es la que vemos ahí donde p_barra y x_barra son los centroides. Entoces con ICP calculamos cada vez los puntos más cercanos de una toma en la otra, obteniendo de ese modo un conjunto con el mismo número de puntos y podemos aplicar la optimización que hemos visto. Y repetimos hasta que no haya cambios significativos en al distancia.

### Problemas I
Convergencia local, lo que hace que las tomas estén bien posicionadas al comnezar al algoritmo. Esto hace necesario una etapa de prealineado donde se cogen tres puntos con correspondencia en ambas tomas y se hacen coincidir todo lo posible.

## Problemas II

Orden cuadrático en tiempo ya que tenmos que calcular el punto más cercano como hemos dicho lo que para cada punto de una toma tengamos que recorrer todos los de la otra. Vemos que en la toma "pequeña" tarda algo más de un minuto por iteración lo que hace que en modelos más grandes o en situaciones más reales  donde hay cientos de miles de puntos que el proceso tarde horas.

### Mejoras
Lo que hacemos para solucionar el problema del tiempo lo que hacemos es reducir el conjunto de puntos a los que aplicar el procedimiento. Para ello, detectamos puntos significativos comprobando los que tienen cambios bruscos la variación respecto a sus vecinos, detectando: esquenas, hendiduras ... También es necesario simplificar el modelo para reducir las consecuencias del ruido y a la alta densidad de puntos hace que se detecten demasiados. EL obejtivo de este es aplicarlo en las primeras iteraciones ya que para conseguir resultados óptimos se debe usar todo el modelo. De este modo, si consideramos alinear dos tomas como las que mostramos, reducimos considerablemente el número de puntos más 2 millones original, 35000 simplificada y entre 1000 2000 los puntos clave. Poco tiempo de cácluclo de normales, ptos clave e iteración.

### RANSAC

Otro algoritmo muy usado es el denominado RANSAC y se utiliza, general, para ajustar parámetros de un modelo matemático. Su funcionamiento es muy sencillo, tenemos una nube de puntos a la que queremos ajustar una recta. Lo que hacemos es escoger dos puntos aleatorios, generamos la recta que definen y vemos cómo de buena es, es decir, cúanto puntos se ajustan a ella con un determinado error. AL final nos quedamos con la que mejor resultados nos haya dado. EL numero de iteraciones necesarias depende de la probabilidad con la que queramos obtener el modelo, el número de puntos que definen el modelo y la probabilida de ser un valor atípico.

### Aplicación alineado
EN nuestro caso vamos cogiendo tres puntos aleatorios para obtener los planos tal y como se aprecia en la figura. Una vez que tenemos suficientes planos, calculamos las intersecciones entre los mismos para obtener las esquinas. Cuando tenemos calculados los mismos en las dos tomas, lo que hacemos es asociarlos en función de los ángulos que forman cada ángulo ya que se suponen que estos no variarán entre tomas. De este modo, podemos aplicar un pralineado como hacíamos antes de aplicar el paso previo en ICP. En nuestro caso, los resultados no son los esperados ya que todos los puntos tienen una valor parecido de ángulos entre planos a lo que hay que sumarle los posibles errores en la toma de muetras Además, en otras pruebas realizadas han concluido que para conseguir buneos resultados tendría que haber un mínimo de 30 planos (80%). DE todos modos, con otros modelos que presentan más diferencias entre los puntos detectados sí puede funcionar.

### Banco

El banco se ha desarrollado en C++ usando OpenGL como biblioteca gráfica y Qt para la interfaz. DEstacamos que ha sido necesario implementar un mecanismo de selección por color o hacer las manipulaciones para obtener las coordenas correctas para la selección múltiple.

