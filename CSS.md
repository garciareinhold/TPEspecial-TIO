"# TPEspecial-TIO"

# Sintaxis en CSS

## Primera Parte

Partiendo del comienzo, CSS se compone de dos bloques:

* **Propiedades:** Son identificadores que indican a las personas qué característica de estilo (ancho, color de fondo, fuente) queremos cambiar.
* **Valores:** A cada propiedad se le da un valor, que indica cómo queremos cambiar esta característica (por ejemplo qué fuente, qué ancho o qué color usar).

El par formado por una propiedad y un valor se denomina declaración CSS. Las declaraciones CSS forman bloques declarativos. Los bloques de declaraciones CSS emparejados con selectores forman _Conjuntos de Reglas_

### Declaraciones CSS

La principal función del lenguaje CSS es asignar valores a las propiedades CSS. El motor CSS calcula qué declaraciones debe aplicar a cada elemento de una página para mostrarla y darle estilo de manera adecuada. Lo importante es recordar que tanto las propiedades como los valores son modificables en CSS. Los pares propiedad y valor, se separan por dos puntos (:).

![Alternative Text!](/images/css-syntax-1.png )
### Bloques declarativos en CSS

Las declaraciones están agrupadas por bloques, en los que el conjunto de declaraciones se encuentra enumerado entre corchetes, uno inicial ({) y otro final (}). Cada declaración contenida en un bloque declarativo deber estar separada por un punto y coma (;), sino el código no funcionará (o producirá resultados inesperados). La última declaración de un bloque no necesita llevar (;), aunque se considera buena práctica añadirlo, para prevenir olvidos cuando se añaden más declaraciones al bloque.

![Alternative Text!](/images/css-syntax-2.png )

## Segunda Parte

### Selectores y reglas CSS

Pero, en este rompe cabezas falta una pieza — y es aprender a identificar los elementos a los que afectará nuestro bloque declarativo. Esto lo conseguiremos añadiendo a cada bloque declarativo un prefijo a modo de selector — un módulo que identificará a ciertos elementos de nuestra página. Las declaraciones asociadas se aplicarán solo a estos elementos. El selector más el bloque declarativo se llama regla o regla-conjunto.

![Alternative Text!](/images/css-syntax-3.png  )

Los selectores (filtros) pueden llegar a ser bastante complicados — se puede establecer una regla que afecte a múltiples elementos separándolos en el selector por comas, y estos pueden ser identificados en conjunto, por ejemplo: Seleccionar los elementos de la clase "blah", pero solo los que estén dentro de un

### Reglas CSS

Las Reglas CSS son los bloques principales de un documento de estilos — el bloque más usual que veremos en un CSS. Pero nos podemos encontrar con otros tipos de bloques — Las reglas CSS son uno de los tipos de declaraciones CSS. Los otros son:

* **Reglas-@:** Usadas en CSS para definir metadatos, información condicional u otra información descriptiva. Comienzan con el símbolo (@), seguido del identificador del tipo de regla, luego un bloque sintáctico correspondiente y terminará con un (;). Cada tipo de Regla-@ definido por un identificador dispondrá de su propia sintaxis y semántica internas. Ejemplos:

  - @charset y @import (metadatos)
  - @media o @document (información condicional, llamada también declaraciones anidadas)
  - @font-face (información descriptiva)

* **Declaraciones anidadas:** son un subtipo de Reglas-@, su sintaxis es un bloque de reglas CSS anidadas que solo afectará al documento bajo ciertas condiciones:

  - El contenido de la regla-@ @media se aplicará solo si el dispositivo que ejecuta el navegador cumple la condición expresada.
  - El contenido de la regla-@ @supports se aplicará solo si el navegador soporta la característica mencionada.
  - El contenido de la regla-@ @document se aplicará solo si la página actual cumple ciertas condiciones.

 * **Ejemplo de sintaxis:**

    @media (min-width: 801px) {
      body {
        margin: 0 auto;
        width: 800px;
      }
    }
  
  Esta regla anidada solo se aplicará cuando el ancho de la página sea superior a 800 pixels.

  ### Buenas Practicas en CSS

  Como podemos comprobar, la sintaxis CSS no es difícil de escribir: podemos escribir reglas y si cometemos errores simplemente serán ignoradas. Pero, aunque funcionen, hay algunas buenas prácticas que debemos conocer para hacer el código CSS más fácil de usar y de mantener.

  #### Espaciado

  El espacio en blanco se refiere a la barra espaciadora, tabulador o cambio de línea. Podemos añadir espacio en blanco para hacer más 'legibles' nuestros documentos de estilo.

  Al igual que en HTML, el navegador suele ignorar la mayoría del espacio en blanco en nuestro CSS; mucho espacio en blanco está ahí solo como ayuda a la lectura. En el siguiente ejemplo vemos que cada declaración (y de inicio/fin de regla) está en una línea diferente — esta es sin duda una buena forma de escribir CSS, ya que lo hace fácil de entender y de mantener:

![Alternative Text!](/images/css-syntax-4.png )

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

  ![Muestra selectores](/images/css-syntax-5.png "CSS Sintax")

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

  #### Una sencilla hoja de estilos:

  /* All p elements are red */
  p {
    color: red;
  }

  /* All div elements are blue */
  div {
    color: blue;
  }
  

  #### Obteniendo el siguiente resultado:

  ![Selectores de tipos](/images/css-syntax-9.png "Selectores de elementos")

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

  ![Selectores de clases](/images/css-syntax-10.png "CSS Sintax")

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

  #### Dara el siguiente resultado

  ![Selectores de ID](/images/css-syntax-12.png "CSS Sintax")

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

  #### Nos dara el siguiente resultado

  ![Selector universal](/images/css-syntax-11.png "CSS Sintax")

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

  #### El resultado sera

  ![Selectores](/images/css-syntax-13.png "CSS Sintax")

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

  #### Con las nuevas reglas el resultado sera

  ![Selectores](/images/css-syntax-14.png "CSS Sintax")

  #### Pseudo-clases y pseudo-elementos

  Veremos los pseudo-selectores — llamados así por no seleccionar elementos, sino ciertas partes de estos o solo bajo determinadas circunstancias. Hay de dos tipos: pseudo-clases y pseudo-elementos.

  * **Pseudo-clases**

  Una pseudo-clase CSS consta de una clave precedida de dos puntos (:) que añadiremos al final del selector para indicar que daremos estilo a los elementos seleccionados solo cuando estos se encuentren en un estado determinado. Por ejemplo podríamos querer dar estilo a un elemento cuando este se muestre al pasarle el puntero del ratón, o una caja de selección al estar habilitada o deshabilitada o cuando un elemento es hijo directo de su padre en el árbol DOM.

    :active
    :any
    :checked
    :default
    :dir()
    :disabled
    :empty
    :enabled
    :first
    :first-child
    :first-of-type
    :fullscreen
    :focus
    :hover
    :indeterminate
    :in-range
    :invalid
    :lang()
    :last-child
    :last-of-type
    :left
    :link
    :not()
    :nth-child()
    :nth-last-child()
    :nth-last-of-type()
    :nth-of-type()
    :only-child
    :only-of-type
    :optional
    :out-of-range
    :read-only
    :read-write
    :required
    :right
    :root
    :scope
    :target
    :valid
    :visited
  No profundizaremos en cada una de las pseudo-clases — no es objetivo del Area de Aprendizaje presentarlas todas exhaustivamente, y se irán viendo con más detalle a lo largo del curso en el momento oportuno.

  * **Ejemplo de pseudo-clase**
  Por ahora, veamos un ejemplo de cómo usarlas. Primero, un fragmento de HTML:

  <a href="https://developer.mozilla.org/" target="_blank">Mozilla Developer Network</a>

  * **Y las reglas CSS:**

  /* These styles will style our link
     in all states */
  a {
    color: blue;
    font-weight: bold;
  }

  /* We want visited links to be the same color
     as non visited links */
  a:visited {
    color: blue;
  }

  /* We highlight the link when it is
     hovered (mouse), activated
     or focused (keyboard) */
  a:hover,
  a:active,
  a:focus {
    color: darkred;
    text-decoration: none;
  }

  ![Pseudo-clases](/images/css-syntax-15.png "CSS Sintax")

  * **Pseudo-elementos**

  Los pseudo-elementos son parecidos a las pseudo-clases, con alguna diferencia. Estos son claves — ahora precedidas por (::) — que se añaden al final del selector para elegir cierta parte de un elemento.

    ::after
    ::before
    ::first-letter
    ::first-line
    ::selection
    ::backdrop
  Todos disponen de comportamientos específicos e interesantes características que escapan a nuestros objetivos de aprendizaje por el momento.

  * **Ejemplo de pseudo-elemento**
  Mostramos a continuación un ejemplo sencillo de CSS que selecciona los espacios situados justo después de todos los enlaces absolutos y en su lugar añade una flecha:

  <ul>
    <li><a href="https://developer.mozilla.org/en-US/docs/Glossary/CSS">CSS</a> defined in the MDN glossary.</li>
    <li><a href="https://developer.mozilla.org/en-US/docs/Glossary/HTML">HTML</a> defined in the MDN glossary.</li>
  </ul>

   * **Añadamos ahora la regla CSS:**

  /* All elements with an attribute "href", which values
     start with "http", will be added an arrow after its
     content (to indicate it's an external link) */
  [href^=http]::after {
    content: '⤴';
  }

  ![Pseudo-elementos](/images/css-syntax-16.png "CSS Sintax")

  #### Combinaciones y selectores múltiples

  * **Combinaciones**

  El uso de un selector cada vez puede ser útil, pero ineficiente en algunas situaciones. Los selectores CSS pueden ser más prácticos cuando los combinamos para refinar las selecciones. En CSS tenemos varias maneras para seleccionar unos elementos respecto a su relación con otros. Estas relaciones se expresan mediante combinaciones de la siguiente forma (A y B representan cualquiera de los selectores vistos hasta ahora):

  Combinación	Selecciona
  A, B	Cualquier elemento seleccionado por A y/o B (ver Varios selectores en una regla, más adelante).
  A B	Cualquier elemento seleccionado por B descendiente de un elemento seleccionado por A (o sea, un hijo, un hijo de otro hijo, etc.).
  A > B	Cualquier elemento seleccionado por B y es hijo directo de un elemento seleccionado por A.
  A + B
  Cualquier elemento seleccionado por B y es el siguiente hermano de un elemento seleccionado por A (o sea, el siguiente hijo del mismo padre).

  A ~ B	Cualquier elemento seleccionado por B y es uno de los siguientes hermanos del elemento seleccionado por A (uno de los siguientes hermanos del mismo padre).
  Ejemplo de combinaciones
  Veamos un ejemplo de todo esto actuando a la vez:

  <table lang="en-US" class="with-currency">
  <thead>
      <tr>
      <th scope="col">Product</th>
      <th scope="col">Qty.</th>
      <th scope="col">Price</th>
      </tr>
  </thead>
  <tfoot>
      <tr>
      <th colspan="2" scope="row">Total:</th>
      <td>148.55</td>
      </tr>
  </tfoot>
  <tbody>
      <tr>
      <td>Lawnchair</td>
      <td>1</td>
      <td>137.00</td>
      </tr>
      <tr>
      <td>Marshmallow rice bar</td>
      <td>2</td>
      <td>1.10</td>
      </tr>
      <tr>
      <td>Book</td>
      <td>1</td>
      <td>10.45</td>
      </tr>
  </tbody>
  </table>
  Y utilicemos la siguiente hoja de estilos:

  /* Basic table setup */
  table {
    font: 1em sans-serif;
    border-collapse: collapse;
    border-spacing: 0;
  }

  /* All <td>s within a <table> and all <th>s within a <table>
    Comma is not a combinator, it just allows you to target
    several selectors with the same CSS ruleset */
  table td, table th {
    border : 1px solid black;
    padding: 0.5em 0.5em 0.4em;
  }

    /* All <th>s within <thead>s that are within <table>s */
    table thead th {
    color: white;
    background: black;
    }

    /* All <td>s preceded by another <td>,
    within a <tbody>, within a <table> */
    table tbody td + td {
    text-align: center;
    }

    /* All <td>s that are a last child,
    within a <tbody>, within a <table> */
    table tbody td:last-child {
    text-align: right
    }

    /* All <th>s, within a <tfoot>s, within a <table> */
    table tfoot th {
    text-align: right;
    border-top-width: 5px;
    border-left: none;
    border-bottom: none;
    }

    /* All <td>s preceded by a <th>, within a <table> */
    table th + td {
    text-align: right;
    border-top-width: 5px;
    color: white;
    background: black;
    }

    /* All pseudo-elements "before" <td>s that are a last child,
    appearing within elements with a class of "with-currency" that
    also have an attribute "lang" with the value "en-US" */
    .with-currency[lang="en-US"] td:last-child::before {
    content: '$';
    }

    /* All pseudo-elements "after" <td>s that are a last child,
    appearing within elements with the class "with-currency" that
    also have an attribute "lang" with the value "fr" */
    .with-currency[lang="fr"] td:last-child::after {
    content: ' €';
    }

   #### El resultado de estilo es bastate bonito en la siguiente tabla

  ![Pseudo-elementos](/images/css-syntax-17.png "CSS Sintax")

   #### Varios selectores en una regla

  Hemos ya visto varios ejemplos, pero vamos a dar un par de ejemplos para mayor claridad. Se pueden escribir varios selectores separados por comas para aplicar la misma regla a varios elementos seleccionados a la vez. Ej.:

  p, li {
    font-size: 1.6em;
  }
  
  o también:

  h1, h2, h3, h4, h5, h6 {
    font-family: helvetica, 'sans serif';
  }

  ## Tercera Parte

  ##### En la parte anterior hemos hablado de los distintos selectores CSS. Podemos encontrar varios selectores de reglas CSS afectando al mismo elemento, en estos casos, ¿Qué regla será la que finalmente se aplicará al elemento? Esto está regulado por un mecanismo llamado Cascada; también está relacionado con la Herencia (unos elementos toman "heredan" valores de las propiedades de sus padres, pero otros no). En este artículo definiremos el concepto de cascada, especificidad e importancia y cómo se heredan las propiedades de distintas reglas.

  Podemos dar estilo a un elemento desde distintos sitios que pueden interactuar de forma compleja. Esta interacción compleja hace potente a CSS, pero también puede hacerlo confuso y dificil de depurar. Este artículo tratará de clarificar algo esta complejidad; es normal que no lo comprendamos de manera inmediata — esta es una de las partes más duras de entender de la teoría de CSS. La idea es proporcionar un primer acercamiento y ofrecer una guía para futuras consultas sobre cascada y herencia.

  ### La cascada

  CSS (Cascading Style Sheets) ya nos indica que cascada es un concepto importante. A su nivel más básico indica que el orden de las reglas CSS importa, pero es algo más que eso. Que prevalezcan unos selectores sobre otros en la cascada depende de tres factores (en orden de importancia — los primeros prevalecen sobre los últimos):

  1. Importancia
  2. Especificidad
  3. Orden del codigo

  #### Importancia

  En CSS, hay un trozo de sintaxis que podemos usar para asegurarnos que una determinada regla siempre "gane" sobre todas las demás: !important.

  Veamoslo en un ejemplo:

  ![Alternative text](/images/css-syntax-6.png "CSS Sintax")

  Que produce el siguiente resultado

  ![Alternative text](/images/css-syntax-7.png "CSS Sintax")

  Vemos que ha pasado

  1. Vemos que se han aplicado los valores de color y padding, pero no el de background-color ¿Porqué? En realidad deberían haberse aplicado las tres pues las reglas declaradas más tarde normalmente prevalecen sobre las anteriores.
  2. Sin embargo, ganan las reglas anteriores, pues los selectores de ID/clase son más específicos que los selectores de elemento (lo veremos en la siguiente sección).
  3. Ambos elementos pertenecen a la class better, pero el 2do tiene además la id winning. Las IDs son más específicas que las clases (solo podemos tener un elemento para cada ID en una página, pero podemos tener varios elementos de la misma clase — los selectores ID son muy específicos en aquello que seleccionan), el fondo de color rojo y el borde de 1px negro se deberían aplicar al segundo elemento, y el primer elemento tomará el fondo gris, sin borde, como indica la clase.
  4. El 2do elemento toma el fondo rojo, pero no el borde. ¿Porqué? La declaración !important de la segunda regla — declarada después de (border: none) hará que esta declaración prevalezca sobre el valor del borde de la regla anterior, incluso aunque ID tenga una especificidad mayor.

  Es útil saber que !important existe para poder reconocerlo en el código escrito por otros, PERO, no debemos usarlo a menos que sea estrictamente necesario. Una de estas ocasiones la encontramos cuando estamos trabajando un CMS y no podemos editar los módulos principales de CSS, y queremos sobrescribir un estilo que no puede sobrescribirse de ningún otro modo. NO lo usaremos si lo podemos evitar. Pues !important cambia la forma de trabajo de la cascada, y puede causar problemas de dificil solución en el depurado de CSS, especialmente en CSS grandes.

  Es útil conocer que la importancia de una declaración CSS depende de los estilos que son especificados en la misma — los usuarios pueden establecer estilos propios que prevalezcan sobre los del desarrollador. Si, por ejemplo, usuarios disminuidos visuales quisieran usar un tamaño de fuente el doble de lo normal en todas las páginas para facilitar su lectura.

  De existir conflicto, las declaraciones se aplicarán en el siguiente orden, donde las últimas prevalecen sobre las primeras:

  1. Declaraciones en el documento de estilos del usuario (como los estilos por defecto del navegador, usados cuando no hay otros estilos fijados)
  2. Declaraciones normales en el documento de estilos del usuario (establecidos por el propio usuario)
  3. Declaraciones normales en el documento de estilos del autor (los estilos establcidos por nosotros, los desarrolladores web)
  4. eclaraciones !Important en el documento de estilos del autor
  5. Declaraciones !Important en el documento de estilos del usuario

  Tiene sentido que el documento de estilos del desarrollador prevalezca sobre el del usuario, pues así se puede mantener el diseño establecido, pero en determinadas ocasiones los usuarios pueden tener buenas razones para sobrescribir los estilos del desarrollador como ya se ha mencionado anteriormente — esto se consigue usado la declaración !Important en sus reglas.

  #### Especificidad

  La **Especificidad** es en sí una medida de cómo de específico es un selector — cuantos elementos puede seleccionar. Como hemos mostrado en el ejemplo anterior, los selectores de elementos son poco específicos. Los selectores de clase son más específicos, por lo que prevalecen sobre los selectores de elementos. Los selectores ID son todavía más específicos, por lo tanto ganan frente a los de clase. La única forma de vencer a los selectores ID es usando la declaración !important.

  La especificidad que tiene un selector se mide mediante 4 valores (o componentes) diferentes, podemos pensar en ellos como en 4 columnas de unidades de millar, centenas, decenas y unidades:

  1. Unidades de millar: Puntúa 1 en esta columna si la declaración está dentro de un atributo style (como las declaraciones que no tienen selectores, que su especificidad es siempre 1000). Sino puntúa 0.
  2. Centenas: Puntúa 1 en esta columna por cada selector ID contenido en el selector.
  3. Decenas: Puntúa 1 en esta columna para cada selector de clase, selector de atributo o de pseudo-clase contenidos en el selector.
  4. Unidades: Puntúa 1 en esta columna por cada selector de elemento o pseudo-elemento contenidos en el selector

  La siguiente tabla muestra algunos ejemplos sueltos para meternos en tarea. Intentemos comprenderlos y entender porqué tienen la especificidad que se les ha atribuido.

  ![Alternative text](/images/css-syntax-8.png "CSS Sintax")

  #### Orden del código

  Orden del código
  Como hemos mencionado, si varios selectores competidores tienen la misma importancia y especificidad, el tercer factor que interviene para decidir qué regla vence es el orden del código — las últimas reglas prevalecen sobre las primeras.

  #### Una nota en la combinación de reglas

  Cuando estudiamos la teoría sobre la cascada, y el porqué unos estilos se aplican y otros no, es que esto ocurre a nivel de las propiedades — unas propiedades prevalecen sobre otras, pero no reglas enteras prevaleciendo sobre otras reglas. Cuando varias reglas CSS apuntan al mismo elemento, todas se aplican sobre él. Solo después de esto se evalúan los conflictos entre las propiedades para saber qué estilos prevalecerán sobre los otros.

  ### Herencia

  La **herencia** en CSS es la última pieza que necesitamos conocer para tener la información completa y comprender qué estilo se aplicará a un elemento. La idea es que unos elementos se heredarán por los elementos hijos, y otros no.

  * Por ejemplo, tiene sentido que font-family y color sean heredadas, pues nos facilita establecer un ancho de fuente básico aplicando una familia de fuentes al elemento ; después podemos reemplazar las fuentes de elementos individuales si es necesario. Sería realmente molesto tener que establecer la fuente base para cada elemento por separado.
  * Otro ejemplo: tiene sentido que margin, padding, border, y background-image NO se hereden. Imaginemos el lio de formato/estilo que ocurriría si aplicamos estas propiedades en un elemento y fuera heredado por todos y cada uno de sus hijos, y después tener que "desaplicarlas" a todos los elementos también.

  Las propiedades que se heredan por defecto y las que no, viene marcado en gran medida por el sentido común. Pero para estar seguros podemos consultar la Referencia CSS — cada propiedad viene en una página que comienza con una tabla resumen que incluye diversos detalles sobre cada elemento, incluyendo si se hereda o no.

  ##### Control de la herencia

  CSS dispone de tres valores especiales para manejar las herencias:

  * inherit : Este valor establece el valor de la propiedad de un elemento seleccionado en el mismo que su elemento padre.
  * initial : Este valor establece el valor de la propiedad de un elemento seleccionado en el valor por defecto que establece la hoja de estilos del navegador, si este no existe, la propiedad se hereda naturalmente, adoptando el valor de inherit.
  * unset : Este valor reestablece la propiedad a su valor natural, esto es: si la propiedad se hereda de forma natural entonces actuará como inherit, sino, actuará como initial.

  El valor inherit es el más interesante — nos permite, de forma explícita, hacer que un elemento herede de su padre el valor de una propiedad.

  #### Echemos un vistazo a un ejemplo. Primero, como siempre, el HTML:

  <ul>
    <li>Default <a href="#">link</a> color</li>
    <li class="inherit">Inherit the <a href="#">link</a> color</li>
    <li class="initial">Reset the <a href="#">link</a> color</li>
    <li class="unset">Unset the <a href="#">link</a> color</li>
  </ul>

  Y el CSS para dar estilo:

  body {
    color: green;
  }

  .inherit a {
    color: inherit;
  }

  .initial a {
    color: initial
  }

  .unset a {
    color: unset;
  }

  Resultado:

  ![Herencia](/images/css-syntax-18.png "CSS Sintax")
