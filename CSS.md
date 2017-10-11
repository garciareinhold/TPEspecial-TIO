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

  #### Selectores en CSS

  En CSS, los selectores se usan para elegir los elementos HTML que queremos estilizar de nuestra web. Disponemos de gran variedad de selectores CSS, que proporcionan mucha precisión para seleccionar el elemento deseado. En los siguientes artículos veremos los distintos tipos con más detalle y su funcionamiento.

  #### Selectores básicos

  En el último artículo vimos Sintaxis y terminología CSS. Resumiendo, los selectores forman parte de las reglas CSS y van justo antes de los bloques declarativos.

  ![Muestra selectores](/images/css-sintax-5.png "CSS Sintax")

  #### Tipos de selectores
  Podemos dividir los selectores en las siguientes categorías:

  * **Selectores simples:** Seleccionan los elementos por el nombre del tipo de elemento, class, o su id.
  * **Selectores de atributos:** Seleccionan los elementos por los valores de sus atributos.
  * **Pseudo-clases:** Seleccionan los elementos por el estado en que se encuentran, cómo haber aparecido al pasar el ratón, o el tic deshabilitado o seleccionado, o por ser el primer hijo de su padre en el árbol DOM.
  * **Pseudo-elementos:** Selecciona los elementos por su situación en relación a otro elemento, por ejemplo: la primera palabra de cada párrafo, o el contenido que se encuentra justo después de un elemento.
  * **Combinaciones:** No son en sí mismos selectores, sino formas de combinar dos o más selectores de forma práctica para una selección especial. Por ejemplo, se pueden seleccionar párrafos que sean descendientes de divs, o párrafos situados justo después de títulos.
  * **Selectores múltiples:** Tampoco son selectores en sí mismos; podemos agrupar múltiples selectores en la misma regla CSS separados por comas, para aplicarlos a una de las declaraciones o a todos los elementos seleccionados por estos selectores.

  #### Selectores simples

  En nuestro primer artículo sobre selectores estudiaremos los selectores "simples", así llamados porque referencian directamente a uno o más elementos de un documento en función del tipo de elemento(o su class o id).

  #### Selector de elementos (selector de tipos)

  Este selector hacer referencia directamente a un tipo de elemento HTML. Es la manera más sencilla para hacer referencia a todos los elementos de un mismo tipo. Veamos el ejemplo:

  * **Dado el siguiente código HTML:**

  <p>What color do you like?</p>
  <div>I like blue.</div>
  <p>I prefer red!</p>
  Una sencilla hoja de estilos:

  /* All p elements are red */
  p {
    color: red;
  }

  /* All div elements are blue */
  div {
    color: blue;
  }

  #### Selectores de clases

  El selector de clase se forma con un punto, '.', seguido de un nombre de clase. Un nombre de clase puede ser cualquier valor sin espacios usado dentro de un atributo HTML class. Podemos elegir el nombre que deseemos para la clase. Es conveniente saber que en un mismo documento varios elementos pueden compartir el mismo valor de clase y que un elemento puede tener varios nombres de clases separados por un espacio en blanco. Veamos un rápido ejemplo:

  * **Sea el siguiente código HTML:**

  <ul>
    <li class="first done">Create an HTML document</li>
    <li class="second done">Create a CSS style sheet</li>
    <li class="third">Link them all together</li>
  </ul>
  
  * **Y un sencillo documento de estilos:**

  /* The element with the class "first" is bolded */
  .first {
    font-weight: bold;
  }

  /* All the elements with the class "done" are strike through */
  .done {
    text-decoration: line-through;
  }

  #### Selectores ID

  El selector ID está formdo por una almohadilla (#), seguida del nombre ID de determinado elemento. Cualquier elemento puede tener un único nombre ID fijado con el atributo id. Podemos usar cualquier nombre de nuestra elección para el ID. Es la forma más efectiva de selecionar un solo elemento.

  Important: El nombre ID debe ser único en el documento. No podemo saber que sucedera con IDs duplicados, en algunos navegadores solo contará la primera ocurrencia, las demás serán ignoradas.

  * **Veamos un rápido ejemplo — dado el código HTML:**

  <p id="polite"> — "Good morning."</p>
  <p id="rude"> — "Go away!"</p>
  Y un sencillo documento de estilos:

  #polite {
    font-family: cursive;
  }

  #rude {
    font-family: monospace;
    text-transform: uppercase;
  }

  #### Selector Universal

  El selector universal (*) es el comodín. Nos permite seleccionar todos los elementos de una página, se suele usar en combinación con otros selectores (ver Combinators más adelante).

  Importante: Cuidado al utilizar el selector universal. Al afectar a todos los elementos, usarlo en grandes páginas web grandes puede afectar al rendimiento, ralentizando el tiempo de carga de las páginas más de lo esperado. No tendremos necesidad de usarlo muy a menudo.

   * **Ahora como ejemplo; dado un código HTML:**

  <div>
    <p>I think the containing box just needed
    a <strong>border</strong> or <em>something</em>,
    but this is getting <strong>out of hand</strong>!</p>
  </div>
  
  * **Y su correspondiente hoja de estilos:**

  * {
    padding: 5px;
    border: 1px solid black;
    background: rgba(255,0,0,0.25)
  }

  #### Selectores de atributos
   
  Los selectores de atributos realiza la selección de los elementos afectados por la declaración en función de los attributes y sus valores. Su sintaxis consiste en la inclusión del nombre del atributo entre corchetes seguido opcionalmente de la condición respecto del valor del atributo. Los selectores de atributos se dividen en dos tipos dependiendo de la forma en que seleccionan los valores del atributo: Selectores de atributo de presencia y valor y selectores de atributo de valor textual.

  * **Selectores de presencia y valor**

  Estos selectores de atributos afectarán a los elementos cuyo valor coincida exactamente con el valor del atributo especificado:

  [attr] : Este selector 'seleccionará' todos los elementos que contengan el atributo attr, sin importar el valor que tenga.
  [attr=val] : Este, seleccionará los elementos con el atributo attr, pero solo aquello cuyo valor coincida con val.
  [attr~=val]: Este selector afectará a los elementos con el atributo attr, pero solo si el valor val está contenido en la lista de valores (separados por espacios) incluidos en el valor de attr, por ejemplo una de las clases contenida en una lista de clases (separadas por espacios).
  Veamos como ejemplo el siguiente fragmento de código HTML:

  Ingredients for my recipe: <i lang="fr-FR">Poulet basquaise</i>
  <ul>
    <li data-quantity="1kg" data-vegetable>Tomatoes</li>
    <li data-quantity="3" data-vegetable>Onions</li>
    <li data-quantity="3" data-vegetable>Garlic</li>
    <li data-quantity="700g" data-vegetable="not spicy like chili">Red pepper</li>
    <li data-quantity="2kg" data-meat>Chicken</li>
    <li data-quantity="optional 150g" data-meat>Bacon bits</li>
    <li data-quantity="optional 10ml" data-vegetable="liquid">Olive oil</li>
    <li data-quantity="25cl" data-vegetable="liquid">White wine</li>
  </ul>
  Y un sencillo documento de estilos CSS:

  /* All elements with the attribute "data-vegetable"
     are given green text */
  [data-vegetable] {
    color: green;
  }

  /* All elements with the attribute "data-vegetable"
     with the exact value "liquid" are given a golden
     background color */
  [data-vegetable="liquid"] {
    background-color: goldenrod;
  }

  /* All elements with the attribute "data-vegetable",
     containing the value "spicy", even among others,
     are given a red text color */
  [data-vegetable~="spicy"] {
    color: red;
  }

  * **Selector de atributos por valor textual**

  También conocidos como "RegExp-like selectors", pues proporcionan una forma de selección similar a las expresiones normales regular expression (aunque siendo estrictos, estos selectores no son verdaderas expresiones normales):

  [attr|=val] : Este selector elegirá todos los elementos con el atributo attr cuyo valor sea exactamente val o empieza por val- (nota: el guion no es un error, se usa para manejar códigos de lenguaje de programación).

  [attr^=val] : Seleccionará todos los elementos cuyo atributo attr comienza por el valor val.
  [attr$=val] : Este selector elegirá todos los elementos cuyo atributo attr termina por el valor val.
  [attr*=val] : Este seleccionará todos los elementos cuyo atributo attr contiene la cadena val (al contrario que [attr~=val], este selector no considera los espacios como separador de valores sino como parte del valor del atributo).
  Continuemos con el ejemplo previo y añadámosle las siguientes reglas CSS:

  /* Classic usage for language selection */
  [lang|=fr] {
    font-weight: bold;
  }

  /* All elements with the attribute "data-quantity", for which
     the value starts with "optional" */
  [data-quantity^="optional"] {
    opacity: 0.5;
  }

  /* All elements with the attribute "data-quantity", for which
     the value ends with "kg" */
  [data-quantity$="kg"] {
    font-weight: bold;
  }

  /* All elements with the attribute "data-vegetable" containing
     the value "not spicy" are turned back to green */
  [data-vegetable*="not spicy"] {
    color: green;
  }
 