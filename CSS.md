"# TPEspecial-TIO"

# Sintaxis en CSS

## Primera Parte

Partiendo del comienzo, CSS se compone de dos bloques:

* **Propiedades:** Son identificadores que indican a las personas qué característica de estilo (ancho, color de fondo, fuente) queremos cambiar.
* **Valores:** A cada propiedad se le da un valor, que indica cómo queremos cambiar esta característica (por ejemplo qué fuente, qué ancho o qué color usar).

El par formado por una propiedad y un valor se denomina declaración CSS. Las declaraciones CSS forman bloques declarativos. Los bloques de declaraciones CSS emparejados con selectores forman _Conjuntos de Reglas_

### Declaraciones CSS

La principal función del lenguaje CSS es asignar valores a las propiedades CSS. El motor CSS calcula qué declaraciones debe aplicar a cada elemento de una página para mostrarla y darle estilo de manera adecuada. Lo importante es recordar que tanto las propiedades como los valores son modificables en CSS. Los pares propiedad y valor, se separan por dos puntos (:).

![Alternative Text!](/images/css-sintax-1 )
### Bloques declarativos en CSS

Las declaraciones están agrupadas por bloques, en los que el conjunto de declaraciones se encuentra enumerado entre corchetes, uno inicial ({) y otro final (}). Cada declaración contenida en un bloque declarativo deber estar separada por un punto y coma (;), sino el código no funcionará (o producirá resultados inesperados). La última declaración de un bloque no necesita llevar (;), aunque se considera buena práctica añadirlo, para prevenir olvidos cuando se añaden más declaraciones al bloque.

![Alternative Text!](/images/css-sintax-2 )

### Selectores y reglas CSS

Pero, en este rompe cabezas falta una pieza — y es aprender a identificar los elementos a los que afectará nuestro bloque declarativo. Esto lo conseguiremos añadiendo a cada bloque declarativo un prefijo a modo de selector — un módulo que identificará a ciertos elementos de nuestra página. Las declaraciones asociadas se aplicarán solo a estos elementos. El selector más el bloque declarativo se llama regla o regla-conjunto.

![Alternative Text!](/images/css-sintax-3 )

Los selectores (filtros) pueden llegar a ser bastante complicados — se puede establecer una regla que afecte a múltiples elementos separándolos en el selector por comas, y estos pueden ser identificados en conjunto, por ejemplo: Seleccionar los elementos de la clase "blah", pero solo los que estén dentro de un

### Reglas CSS

Las Reglas CSS son los bloques principales de un documento de estilos — el bloque más usual que veremos en un CSS. Pero nos podemos encontrar con otros tipos de bloques — Las reglas CSS son uno de los tipos de declaraciones CSS. Los otros son:

* **Reglas-@:**Usadas en CSS para definir metadatos, información condicional u otra información descriptiva. Comienzan con el símbolo (@), seguido del identificador del tipo de regla, luego un bloque sintáctico correspondiente y terminará con un (;). Cada tipo de Regla-@ definido por un identificador dispondrá de su propia sintaxis y semántica internas. Ejemplos:

  - @charset y @import (metadatos)
  - @media o @document (información condicional, llamada también declaraciones anidadas)
  - @font-face (información descriptiva)

* **Declaraciones anidadas:**son un subtipo de Reglas-@, su sintaxis es un bloque de reglas CSS anidadas que solo afectará al documento bajo ciertas condiciones:

  - El contenido de la regla-@ @media se aplicará solo si el dispositivo que ejecuta el navegador cumple la condición expresada.
  - El contenido de la regla-@ @supports se aplicará solo si el navegador soporta la característica mencionada.
  - El contenido de la regla-@ @document se aplicará solo si la página actual cumple ciertas condiciones.

  ### Buenas Practicas en CSS

  Como podemos comprobar, la sintaxis CSS no es difícil de escribir: podemos escribir reglas y si cometemos errores simplemente serán ignoradas. Pero, aunque funcionen, hay algunas buenas prácticas que debemos conocer para hacer el código CSS más fácil de usar y de mantener.

  #### Espaciado

  El espacio en blanco se refiere a la barra espaciadora, tabulador o cambio de línea. Podemos añadir espacio en blanco para hacer más 'legibles' nuestros documentos de estilo.

  Al igual que en HTML, el navegador suele ignorar la mayoría del espacio en blanco en nuestro CSS; mucho espacio en blanco está ahí solo como ayuda a la lectura. En el siguiente ejemplo vemos que cada declaración (y de inicio/fin de regla) está en una línea diferente — esta es sin duda una buena forma de escribir CSS, ya que lo hace fácil de entender y de mantener:

![Alternative Text!](/images/css-sintax-4.png )

  La apariencia del código es una preferencia personal, aunque cuando se trabaja en equipo, normalmente cada equipo tiene su propia guía de estilo que indica las convenciones a seguir.

  #### Comentando el código

  Al igual que en HTML, se aconseja incluir comentarios en el CSS para ayudar a entender el funcionamiento del código al tiempo de haberlo programado, además de ayudar a otros a entenderlo. Los comentarios son prácticos cuando se está probando ciertas partes del código, por ejemplo para averiguar que parte del código está causando el error encontrado.

  Los comentarios en CSS comienzan con /* y acaban con */.

  #### Abreviadas

  Algunas propiedades como: font, background, padding, border, y margin se llaman propiedades abreviadas — permiten establecer varios valores a la vez en una sola línea, ahorrando tiempo y haciendo el código más limpio.

  Ejemplo: padding: 10px 15px 15px 5px;
