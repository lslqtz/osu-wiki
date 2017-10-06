# BBCode

![La caja de edición en los foros](img/forums.jpg "La caja de edición en los foros")

**BBCode** es un lenguaje de marcado que se utiliza en los foros de osu! y, en mayor medida, en la gran mayoría de los foros de Internet para permitir el formato de texto enriquecido.
Se compone de etiquetas que rodean el texto para enriquecer y, en ocasiones, dar atributos al mismo.

En la web de osu!, BBCode se utiliza en los mensajes del foro, las firmas y las páginas de usuario.

## Notas

Mientras que el editor del mensaje proporciona algunas herramientas de formato básico, es posible escribir manualmente el BBCode.

Las etiquetas BBCode son insensibles a las mayúsculas: `[centre]texto[/centre]` dará el mismo resultado que `[cEnTRe]texto[/ceNTRE]`.

### Comportamiento del Botón BBCode

Sin ningún texto resaltado, al hacer clic en el botón las etiquetas se colocarán alrededor del cursor en el editor de mensajes.

Con texto resaltado en el editor de mensajes, al hacer clic en el botón las etiquetas se situarán alrededor del texto resaltado.

### Combinación de etiquetas

Las etiquetas se pueden combinar para tener un formato más sofisticado.

El orden de las etiquetas **debe** ser respetado cuando se combinan las etiquetas. Un orden incorrecto puede romper el formato del mensaje.

Por ejemplo (presta atención al orden del código):

- `[centre]` `[b]` _texto_ `[/ b]` `[/ centre]` es correcto, pero
- `[b]` `[centre]` _texto_ `[/ b]` `[/ centre]` está mal.

## Lista de etiquetas BBCode

### Negrita

**Enfatiza** palabras o un párrafo entero de una manera **más intensa que** [cursiva](#cursiva).

- Botón dedicado: ![Botón negrita](img/bold.jpg "Botón negrita")
- Notas:
   * Utilizar con moderación. El uso excesivo puede crear incomodidad y hacer que el mensaje sea más difícil de leer.
- Sintaxis:
```prolog
[b] ... [/b]
```

### Cursiva

**Enfatiza** palabras o un párrafo entero de una manera *menos intensa que* [negrita](#negrita).

- Botón dedicado: ![Botón itálico](img/italic.jpg "Botón itálico")
- Notas:
  * Utilizar con moderación. El uso excesivo debilitará la eficacia del énfasis.
- Sintaxis:
```prolog
[i] ... [/i]
```

### Subrayado

**Dibuja una línea horizontal debajo** de la(s) palabra(s) o un párrafo entero.

- Botón dedicado: ![Botón Subrayado](img/underline.jpg "Botón Subrayado")
- Notas:
  * Utilizar con moderación. El uso excesivo puede crear incomodidad y hacer que el mensaje sea más difícil de leer.
- Sintaxis:
```prolog
[u] ... [/u]
```

### Tachado

**Traza una línea horizontal a través del centro** de la(s) palabra(s) o un párrafo entero.

- Botón dedicado: ![Botón Tachado](img/strike.jpg "Botón Tachado")
- Notas:
  * Utilizar con moderación. El uso excesivo puede crear incomodidad y hacer que el mensaje sea más difícil de leer.
- Sintaxis:
```prolog
[strike] ... [/strike]
```
  * Alternativamente, se puede utilizar:
```prolog
[s] ... [/s]
```

### Color

_BBCode llama a este "Color" ._

**Añade color** a algún texto.

- Botones dedicados:
![La caja de color](img/colour.jpg "La caja de color")
- Notas:
  * El cuadro de color se encuentra en el lado derecho del cuadro de texto.
  * Utiliza esta etiqueta con moderación.
  * El uso excesivo de esto creará incomodidad a los ojos del lector.
  * El mal uso de esto hará que tu texto sea ilegible.
  * Si eliges un color, asegúrate de que contraste con el fondo para que sea legible.
  * El argumento `HEXCODE` no debe usar comillas.
- Sintaxis:
  * Donde `HEXCODE` es un color en hexadecimal o nombre de color.
    - Para hexadecimal, debe comenzar con `#`, seguido por 6 caracteres hexadecimales (0 - 9, A - F).
    - Para el nombre del color, debe ser un color HTML válido.
```prolog
[color=HEXCODE] ... [/color]
```

Para obtener una lista de nombres de color, consulta [nombres de color X11](https://en.wikipedia.org/wiki/X11_color_names#Color_name_chart).

### Tamaño de fuente

Ajusta relativamente el tamaño del texto.

- Botones dedicados:
![Opciones de tamaño de fuente](img/font-size.jpg "Opciones de tamaño de fuente")
- Notas:
  * Utiliza esta etiqueta con moderación.
  * Sólo hay 4 tamaños que puede utilizar:
    - `50` (diminuto)
    - `85` (pequeño)
    - `100` (normal, predeterminado)
    - `150` (grande)
  * Si introduces un valor que no es uno de los enumerados anteriormente, utilizarás el tamaño de fuente predeterminado.
  * El argumento `NUMBER` no debe usar comillas.
- Sintaxis:
  * Cuando `NUMBER` sea uno de los tamaños indicados anteriormente:
```prolog
[size=NUMBER] ... [/size]
```

### Spoiler

_No debe confundirse con [Spoilerbox](#spoilerbox)._

**Cubre el texto** con un fondo negro.

Esto puede ser útil si estás hablando de una escena crítica en un programa de televisión, película o anime, pero no quieres estropearlo para otros.
El lector, sin embargo, todavía puede leer el texto, resaltándolo.

- Botón dedicado: ![Botón Spoiler](img/spoiler.jpg "Botón Spoiler")
- Notas:
  * Si utilizas la etiqueta [color](#color) junto con esto, el color tendrá un fondo negro.
- Sintaxis:
```prolog
[spoiler] ... [/spoiler]
```

### Caja spoiler

_No debe confundirse con [Box](#box) o [Spoiler](#spoiler)._

**Oculta un párrafo** dentro de una caja previamente nombrada `collapsed text`.
El lector, sin embargo, puede leer el párrafo haciendo clic en la spoilerbox para mostrar el párrafo oculto.

- Botón dedicado: ![Botón Spoilerbox](img/spoilerbox.jpg "Botón Spoilerbox")
- Notas:
  * Esto creará un cuadro [Box](#) con el texto de encabezado `collapsed text`.
- Sintaxis:
```prolog
[spoilerbox]
...
[/spoilerbox]
```

### Caja

_No debe confundirse con [Spoilerbox](#spoilerbox)._

**Oculta un párrafo** dentro de un cuadro identificable por el lector.
El lector puede mostrar el párrafo haciendo clic en el nombre del cuadro.

Estos se utilizan comúnmente para ocultar imágenes grandes o una gran cantidad de imágenes.

- Botón dedicado: ![Botón de caja](img/box.jpg "Botón de caja")
- Notas:
  * De forma predeterminada, se creará un cuadro con el texto sin encabezado.
    - Si deja el argumento `NAME` en blanco (o no incluye uno), la altura de la caja será muy pequeña!
  * El argumento `NAME` no debe usar comillas.
  * El argumento `NAME` puede contener espacios.
- Sintaxis:
  *  `NAME` será el nombre de la caja.
```prolog
[box=NAME]
...
[/box]
```

### Cita

Cita la(s) palabra(s) o párrafo(s) dado(s).

- Botón dedicado: ![Botón de cita](img/quote.jpg "Botón de cita")
- Notas:
  * Es conveniente tener en cuenta al autor de la cita si estás citando a alguien (usa el argumento `NAME`).
  * El argumento `NAME` **debe** usar comillas.
  * Hay un botón de cita por mensaje (esquina inferior derecha) que citará automáticamente el texto de un usuario.
    - Si hiciste esto, el mensaje (cuando hagas clic en `Post`) se publicará en el hilo actual.
- Sintaxis:
  * `NAME` es a quién/qué se citará (**debe** ir entre comillas).
```prolog
[quote=NAME]
...
[/quote]
```

### Código

Formatea el texto con una familia de fuentes monoespaciada y la coloca dentro de una caja gris. Esto es muy útil cuando estás publicando código para un [storyboard](/wiki/storyboard) o código fuente de un proyecto.

- Botón dedicado: ![Botón de código](img/code.jpg "Botón de código")
- Notas:
  * Esto conservará el espaciado en blanco, lo que implica que ninguna de las líneas se romperá a menos que las rompas.
  *  El desbordamiento de líneas de texto habilitará una caja de desplazamiento horizontal.
- Sintaxis:
```prolog
[code]
...
[/code]
```

### Centrar

Alinear un párrafo al centro; típicamente para títulos o encabezados.

- Botón dedicado: ![Botón central](img/centre.jpg "Botón central")
- Notas:
  * Las etiquetas **deben** estar escritas como `centre` no `center` (ten en cuenta las dos últimas letras).
- Sintaxis:
```prolog
[centre]
...
[/centre]
```

### URL

Agrega un enlace.

No es necesario utilizar esta etiqueta si no deseas utilizar el texto del enlace.
Los foros de osu! enlazarán automáticamente las URL pegadas dentro del mensaje.

- Botón dedicado: ![Botón URL](img/url.jpg "Botón URL")
- Notas:
  * El argumento `ENLACE` no debe usar comillas.
- Sintaxis:
  * `ENLACE` es la url.
  * Donde `TEXTO` es el texto del enlace.
```prolog
[url=ENLACE]TEXTO[/url]
```

### Perfil

Vincula un perfil de usuario utilizando el nombre del usuario.

¡El uso de este botón **no es recomendable**! El problema con el uso de esta etiqueta es que los nombres de usuario pueden cambiarse una vez obtenida una [tag de osu! Supporter](/wiki/osu!supporter). Y una vez que lo hacen, el enlace fallará.

Se recomienda utilizar [URL](#url) en su lugar (utilizando el número de identificación del usuario).

- Botón dedicado: ![Botón Perfil](img/profile.jpg "Botón Perfil")
- Notas:
  * ¡No recomendado!
  * El argumento `USER` tiene que estar definido.
- Sintaxis:
  *  `USER` es el nombre del usuario.
```prolog
[profile]USUARIO[/profile]
```

### Google

Enlaza automáticamente a una búsqueda de Google con el texto proporcionado.

- Botón dedicado: ![Botón de Google](img/google.jpg "Botón de Google")
- Notas:
  * Esto no dará a todos los mismos resultados.
    - Algunos resultados de búsqueda están ocultos debido al idioma/ubicación.
- Sintaxis:
```prolog
[google] ... [/google]
```

### Suerte

**Agrega un enlace directo a una página** usando el botón de Google *I'm Feeling Lucky* usando el texto proporcionado.

- Botón dedicado: ![Botón de la suerte](img/lucky.jpg "Botón de la suerte")
- Notas:
  * Esto no dará a todos los mismos resultados.
    - Algunos resultados de búsqueda están ocultos debido al idioma/ubicación.
- Sintaxis:
```prolog
[lucky] ... [/lucky]
```

### Lista

Formatea el texto en una lista.

En BBCode, hay dos partes para hacer la lista: la envoltura y los puntos.
Los puntos se colocan dentro de la envoltura.

- Botones dedicados:
  * Lista: ![Botón Lista](img/list.jpg "Botón Lista")
  * Tipo de lista: ![Botón Tipo de lista](img/list-type.jpg "Botón Tipo de lista")
  * Lista de viñetas: ![Botón Lista de viñetas](img/list-bullet.jpg)
- Notas:
  * Todos los puntos deben estar rodeados por las etiquetas de tipo lista / lista.
  * Estos son los argumentos válidos para `TYPE`:
    -  _(vacío)_ - con puntos
    -  `1` - numerado
    -  `a` - letras (minúsculas)
    -  `A` - letras (mayúsculas)
    -  `i` - numeral romano (minúsculas)
    -  `I` - numeral romano (mayúsculas)
  * De forma predeterminada, las listas con puntos utilizan puntos cuadrados.
  * Las listas dentro de otras listas suelen traer problemas con el formato.
- Sintaxis:
  * Cuando `TYPE` sea uno de los tipos definidos más arriba.
  * Si `TYPE` no está definido, se utilizarán puntos de forma predeterminada.
```prolog
[list=TYPE]
[*] ...
[/list]
```

### Imagen

**Mostrar una imagen de una fuente de imagen en línea**.

Las imágenes se pueden obtener desde cualquier página, siempre y cuando la imagen exista desde la url dada.

**No vincules la imagen directamente desde un directorio local**. Usar `C:\Users\Name\Pictures\image.jpg` **no funcionará.**

Por favor, sube la imagen a sitios de intercambio de imágenes de buena reputación como [imgur](https://imgur.com/ "imgur") o [puush](https://puush.me/ "puush"). Una vez que la imagen se cargue correctamente, copia y pega el vínculo directo proporcionado entre las etiquetas de imagen.

También ten en cuenta que algunos sitios web no aceptan los enlaces directos a sus imágenes (también conocidos como _hotlinks_). Los sitios de intercambio de imágenes, como los mencionados anteriormente, son más adecuados con enlaces directos, ya que son sitios de intercambio de imágenes.

- Botón dedicado: ![Botón de imagen](img/image.jpg "Botón de imagen")
- Notas:
  * Si tiene muchas imágenes o imágenes grandes, se recomienda colocarlas dentro de una [Caja](#Caja).
- Sintaxis:
  * `LINK` es un enlace directo a una imagen.
```prolog
[img]LINK[/img]
```

### YouTube

Incluye un vídeo de YouTube en tu publicación.

- Botón dedicado: ![Botón de imagen](img/youtube.jpg "Botón de imagen")
- Notas:
  * Si tiene muchas imágenes o imágenes grandes, se recomienda colocarlas dentro de una [Caja](#Caja).
- Sintaxis:
  * `YT-ID` es el ID de vídeo de YouTube (11 caracteres), ¡**no** toda la url!
    - El ID de video de YouTube se encuentra después del parámetro url `?V=`.
```prolog
[youtube]YT-ID[/youtube]
```

### Encabezado (v1)

Añade un encabezado rosa elegante.
Esto se utiliza generalmente para marcar una nueva sección en tu mensaje.

- Botón dedicado: _ninguno_
- Notas:
  * Debes escribir la sintaxis tú mismo.
- Sintaxis:
```prolog
[heading] ... [/heading]
```

### Encabezado (v2)

Añade un encabezado sofisticado púrpura con una línea horizontal.
Esto se utiliza generalmente para denotar una nueva sección en tu mensaje.

- Botón dedicado: _ninguno_
- Notas:
  * ¡Esto sólo funciona en el foro de beatmaps!
  * Esto sólo aparece después de la publicación, no en la vista previa.
  * Debes escribir la sintaxis tú mismo.
- Sintaxis:
```prolog
[...]
```

### Anuncio

Coloca el párrafo dentro de un cuadro blanco.

- Botón dedicado: _ninguno_
- Notas:
  * Debes escribir la sintaxis tú mismo.
- Sintaxis:
```prolog
[notice]
...
[/notice]
```

### Trivia

- Guía original: [HOW TO: Forum BBCodes (inglés)](https://osu.ppy.sh/forum/t/445599) por [Stefan](https://osu.ppy.sh/u/626907)

### Historia

- Hay un error de color en los foros actuales de la web de osu!, si usas el color `transparent`, hará que el texto sea transparente.
  * Este error fue sin embargo, resuelto en el nuevo diseño.
