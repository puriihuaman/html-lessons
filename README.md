# HTML

## ¿Qué es HTML?

HTML (HyperText Markup Language, por sus siglas en inglés) es un lenguaje de marcado que indica a los navegadores web cómo estructurar las páginas web que visita.  
Puede ser tan complicado o tan simple como el desarrollador web quiera que sea. HTML consiste en una serie de elementos, que utiliza para encerrar, envolver o marcar diferentes partes del contenido para que aparezca o actúe de cierta manera. Las etiquetas pueden convertir el contenido en un hipervínculo para conectarse a otra página, poner palabras en cursiva, etc. Por ejemplo, considere la siguiente línea de texto:

## Etiquetas vs Elementos

### Etiqueta:

Las etiquetas son los marcadores que indican el inicio y el final `<>`.

### Elemento:

Son conjuntos de las partes, etiqueta, atributos y contenido `<p id="text">Contenido</p>`.

## Elementos (Etiquetas)

### `doctype`

**Descripción**:  
Todos los documentos `HTML` deben comenzar con una declaración `<!DOCTYPE html>`, para especificar el uso de `HTML5`.  
No es una etiqueta HTML, es "información" para el navegador sobre qué tipo de documento esperar.  
**Código**:

```
<!DOCTYPE html>
```

### `html`

**Descripción**:  
Envuelve todo el contenido de la página. También conocido como elemento raíz.  
**Atributos**:  
`lang`: Estable el idioma de la página, lo podemos establecer en diferentes etiquetas.  
**Código**:

```
  <html lang="es"></html> // Español
  <html lang="en"></html> // Inglres
  <html lang="es-MX"></html> // Español Mexico
  <html lang="ja"></html> // Japones
```

### `head`

**Descripción**:  
Entre el `head` va todo lo que se desea incluir en la página HTML, y **que no es el contenido** que la página va a mostrar al usuario final.  
Podremos incluir palabras claves, descripción de la página que apareceran en los busquedas, CSS para dar estilos.  
**Código**:

```
<head></head>
```

### `meta`

**Descripción**:  
Representan metadatos, que estos no pueden ser representados por elementos HTML.  
Algunos elementos meta: `<base>`, `<link>`, `<script>`, `<style>`, `<title>`.  
**Atributos**:  
`charset`: Especifica la codificación de caracteres para el documento HTML con el valor `utf-8`. `utf-8` incluye la mayoria de caracteres de los lenguajes humanos escritos.  
`name`: `viewport` se refiere a la configuración de la representación de la página en el navegador.  
`content`: `width=device-width, initial-scale=1.0`, especifica el ancho total del dispositivo(`movil`, `pc`, `laptop`, `table`), con una escala inicial equivalente al 100% (importante para el responsive design).  
**Código**:

```
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

### [`link`](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#agregar_iconos_personalizados_a_tu_sitio)

**Descripción**:  
Permite agregar una icono (`.ico`) cuadrado de 16 píxeles, que se muestran en la pestaña del navegador de cada página abierta.  
También acepta los formatos `.gif`, `.png`

**Código**:

```
<head>
  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />
</head>
```

### `title`

**Descripción**:  
Establece el título de una página web.  
Este título aparece en la pestaña del navegador.

**Código**:

```
<title></title>
```

### `body`

**Descripción**:  
Contiene todo el contenido que se va a ser visible de la página, incluyendo _texto_, _imágenes_, _videos_, _audios_, o cualquier otras cosa.  
**Código**:

```
<body></body>
```

### `encabezados`

**Descripción**:  
Existen 6 elementos de encabezado: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` y `<h6>`.  
Cada encabeado indica un nivel de contenido diferente.  
`<h1></h1>`: Representa el título principal  
`<h2></h2>`: Representa el subtítulo  
`<h3></h3>`: Representa el subtítulo del subtítulo y así sucesivamente.  
**Atributos**:
Algunos atributos que podemos agregarlo: `class`, `id`

**Código**:

```
<h1>Soy el título principal</h1>
```

### `párrafo`

**Descripción**:
**Atributos**:
**Código**:

### `<a>Ancla</a>`:

### [`<form></form>`](https://developer.mozilla.org/es/docs/Web/HTML/Element/form)

**Descripción**:  
Obtener data de los usuarios.
**Atributos**:  
`action` es la acción que llama al formulario cuando hacemos click en el botón enviar.  
Este puede ser un archivo `php` o otro.  
**Código**:

### `<label></label>`

**Descripción**:  
Nos proporcionan el nombre o la descripción de la data que estamos requiriendo.
**Atributos**:
`for` hace que mantenga una relación con la etiqueta input a traves de su atributo `id`.

### [`<input />`](https://developer.mozilla.org/es/docs/Web/HTML/Element/input)

**Descripción**:  
Son los campos donde se van a ingresar los datos requeridos del usuario.  
Existen muchos tipos de inputs (`radio`, `text`, `checkbox`, `number`, etc).  
**Atributos**:
`type` define un input de tipo texto.
`id` hace que se mantenga una relación con la etiqueta label atraves de su atributo `for`.  
`name` permite identificar el campo o agrupar opciones.  
`checked` es un atributo booleano, que marca una opción en `radio button`, `checkbox` como seleccionada.  
`value` es el valor que va a tener un input, el cual va a ser procesado.  
`selected` selecciona por defecto un opción del `select`  
`size` indica el tamaño, en un `select` indica cuantas opciones se van a mostrar.  
`multiple` permite selecionar multiples opciones, con ayuda del control.  
**Código**:

```
  <!-- radio -->
	<label for="man">Hombre</label>
  <input type="radio" name="gender" id="man" checked />
  <label for="woman">Mujer</label>
  <input type="radio" name="gender" id="woman" />

  <!-- checkbox -->
  <label for="html">HTML</label>
  <input type="checkbox" name="tech" id="html" value="html" />
  <label for="css">CSS</label>
  <input type="checkbox" name="tech" id="css" value="css" />
  <label for="js">JavaScript</label>
  <input type="checkbox" name="tech" id="js" value="js" />

  <!-- select -->
  <select name="flag" id="flag" size="3" multiple>
    <option value="arg">Argentina</option>
    <option value="pe" selected>Perú</option>
    <option value="br">Brasil</option>
    <option value="ur">Uruguay</option>
  </select>

  <!-- textarea -->
  <textarea name="message" id="message" cols="20" rows="10"></textarea>
```

### `<div></div>`

**Descripción**:  
`div` proviene de la palabra _division_(división).  
Es un contenedor de `bloque` para agrupar elementos.
**Atributos**:
**Código**:

```
<div>
  <h2>Subtítulo</h2>
  <p>Una de mis películas favoritas es <i>Rapidos y Furiosos</i>.</p>
</div>
```

### `<section></section>`

**Código**:

```
<section id="about"></section>
<section id="testimonials"></section>
<section id="contact"></section>
```

### `<article></article>`

### div vs section vs article

`div` para agrupar y aplicar estilos comunes de todos los hijos. NO aporta valor semántico a la estructura.  
`section` permite dividir el contenido en secciones. Ejemplo en landingpage podemos dividir en secciones (acerde, servicios, proyectos/productos, contacto, etc.). Una sección puede contener un articulo.  
`article` contenido que por si solo tiene un contexto completo. Ejemplo un blog o libro o tesis.

### `<details></details>`

**Descripción**:
**Código**:

```
<details>
  <summary>Presiona para ver más detalles</summary>
  <div>
    Este es el contendio que se mostrará cuando hagas click en más
    detalles
  </div>
</details>
```

### `<em></em>`

**Descripción**:  
Se utiliza para enfatizar text, indicando un cambio en la entonación o importancia del contenido.

### `<i></i>`

**Descripción**:  
Proviene de `italic` en ingles, que traducida al español sería `cursiva`.  
Se usar para indicar un enfacis diferente (como un estado de animo, un tecnisismo, un pensamiento, un nombre, terminos, etc.).  
**Código**:

```
<div>
  <h2>Subtítulo</h2>
  <p>Una de mis películas favoritas es <i>Rapidos y Furiosos</i>.</p>
</div>
```

### `<dialog></dialog>`:

**Descripción**:  
`dialog` significa _dialogo_ en español.  
Permite crear un cuadro de diálogo o un ventana modal que se va a mostrar en una página web.  
Por defecto tiene el estilo `display`:`none`, no se muestra, normalmente lo usamos con JS.  
**Atributos**:  
**Código**:

```
<button>Mostrar Diálogo</button>

<dialog>
  ¡Hola! Este es un cuadro de diálogo simple.
  <button>Cerrar</button>
</dialog>
```

## [Atributos](https://developer.mozilla.org/es/docs/Web/HTML/Attributes)

Los atributos contienen información adicional sobre el elemento que no se muestran con el contenido.  
Muchos atributos son compartidos entre elementos (algunos, `class`, `id`), algunos solo son especificos de algunas etiquetas (`<img/>`, `src`, `alt` o `<a></a>`, `href`)

### [Atributos globales](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes)

#### identificador (id)

Permite darle un identificador único a un elemento (etiqueta).  
Como buena prática debería ser único.  
Este identificador te puede permitir dar estilos o seleccionar con JS para poder acceder a su información.

#### class

Permite definir una clase que se va a asignar a un elemento (etiqueta).
A traves de estas clases se define bloques de código css.  
Este atributo se puede compartir con otros elementos.

#### onclick

Permite asociar el envento `click` a una función definida en JS.

### Atributos del elemento `<img>`

| Atributos | Descripción                                        |
| --------- | -------------------------------------------------- |
| `src`     | Es requerido, especifica la ubicación de la imagen |
| `alt`     | Descripción en texto sobre la imagen               |
| `width`   | Especifica el ancho en píxeles                     |
| `height`  | Especifica el alto en píxeles                      |

`title`: Proporcina una descripción completa de un termino

### Atributos booleanos

Estos atributos son escritos sin valor.  
Los atributos booleanos solo pueden tener un valor, la mayoria de veces es el mismo que el nombre del atributo.  
Ejemplo: `disabled`, deshabilita el elemento (no deja ingresar información en un input), toma un aspecto gris.

```
// Está deshabilitado, impide ingresar texto
<input type="text" disabled />

// No está deshabilitado, permite ingresar texto
<input type="text" />
```
