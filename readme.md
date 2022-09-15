## ¿Cuál es la utilidad de un sistema de diseño?

La principal ventaja de implementar un sistema de diseño es que **facilita las tareas** de diseñadores y desarrolladores en el proceso de **creación**. También **agiliza la toma de decisión** entre equipos.

### Profundiza en este tema:

[Curso de sistemas de diseño](https://platzi.com/cursos/sistemas-diseno/)

[Curso de sistemas de diseño para desarrolladores](https://platzi.com/cursos/diseno-desarrolladores/)

## Variables en CSS

En CSS, llamamos variables a las **propiedades personalizadas**.
Contienen **valores específicos** que se pueden reutilizar muchas veces en un documento.

Se establecen mediante la **notación** de dos guiones

```css
--nombre-variable: valor;
```

Se **acceden** mediante la función var()

```css
propiedad: var(--nombre-variable);
```

Normalmente las declaramos dentro del selector ***:root*** para que su alcance (scope) sea global.

**Nuestro proyecto quedaría así:**

```css
:root {
            --black:#000000;
            --white: #FFFFFF;
            --very-light-pink: #C7C7C7;
            --text-input-field: #F7F7F7;
            --dark: #232830;
            --hospital-green: #ACD9B2;
        }
```

*También puedes* ***nombrar a tus variables según su función.***

*Ejemplos: --background-color, --primary-color, etcétera.*

## Fonts

Buscaremos las fuentes propuestas por diseño en [Google fonts](https://fonts.google.com/specimen/Quicksand)
Colocamos los links dentro de la etiqueta head del HTML

```html
<head>
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
   <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&display=swap" rel="stylesheet">
</head>
```

Dentro de la etiqueta ***style*** le decimos a CSS que la implemente

```html
body {
            font-family: 'Quicksand', sans-serif;
        }
```

## *Display Grid* para centrar elementos
Cómo puedes ver en nuestra clase ***login*** con solo dos líneas de código podemos centrar nuestro contenido

```css
display: grid;
place-items: center;
```

El ***shorthand property place-items*** te permite alinear elementos, tanto **horizontal** como **verticalmente**, en un contendor con Grid o Flexbox. Es decir, es la **abreviatura** de las propiedades ***align-items*** y ***justify-items***.

Si no le estableces el segundo valor va a utilizar el primero para ambas alineaciones.

Prueba diferentes combinaciones y observa que ocurre:

```css
place-items: center stretch;
place-items: center start;
place-items: start end;
place-items: end center;
```
Profundiza más sobre este tema con esta [clase](https://platzi.com/clases/2474-css-grid/42185-propiedades-de-alineacion/) del **curso de CSS Grid básico**.

## Cómo ordenar los estilos
Una manera de hacerlo es **según su propósito**. Siguiendo el siguiente orden:

1. Posicionamiento
2. Modelo de caja
3. Tipografía
4. Visuales
5. Otros

Mira [aquí](https://platzi.com/clases/2030-mobile-first/32304-estilos-base/) la explicación detallada.

## Responsive dising
Nuestro proyecto es responsive, es decir, se **adapta a diferentes tamaños de pantalla**. Para lograrlo implementamos *[media queries](https://platzi.com/clases/2467-frontend-developer/40845-responsive-design/)*.

```css
@media (max-width: 640px)
```

* Los estilos que se encuentran **fuera** son para ***desktop***.
  
* Los que están **dentro** aplicarán cuando el **viewport sea menor** a 640 píxeles.

Existe **otra forma de maquetación** *responsive* que es justo a la inversa. Primero pensamos en los estilos para móviles y luego vamos “subiendo” hasta llegar a web. Esto se conoce como **Maquetación Mobile First**. [Cliquea para ir al curso](https://platzi.com/cursos/mobile-first/).

## Uso de Figma

Ingresando al diseño en esta plataforma podrás hacer clic sobre los diferentes elementos y **ver su código css**. Incluso se te permite copiarlo. Claro está, ***si deseas practicar es mejor que tú no lo memorices y escribas el código css***.

![](https://static.platzi.com/media/user_upload/Sin%20t%C3%ADtulo-9e863521-12f0-40e4-8988-c3cda09f6aac.jpg)

Recuerda que para poder hacerlo primero debes **crearte una cuenta en Figma**.

![](https://static.platzi.com/media/user_upload/Figma1-7b5103f2-9958-4973-bcfb-966b573e569c.jpg)

Luego abre este [link](https://www.figma.com/file/bcEVujIzJj5PNIWwF9pP2w/Platzi_YardSale?node-id=0%3A617) y selecciona la opción “Open in Editor”

![](https://static.platzi.com/media/user_upload/Figma2-413c961e-7981-4082-aaf1-f428cfc5cd7f.jpg)

Haciendo esto, también dispondrás del texto que lee el usuario.

![](https://static.platzi.com/media/user_upload/Figma3-4a8a09a9-c516-47fc-82c7-8dac3a2851fc.jpg)

Si **te gustaría dominar esta herramienta** puedes completar los siguientes cursos:

* [Curso de Figma](https://platzi.com/cursos/figma/)
* [Curso de Figma avanzado](https://platzi.com/cursos/figma-avanzado/)

## ¿Cómo alinear el botón del formulario?

Tal como ocurrió en el reto anterior, esta pantalla en su versión móvil despega el botón del formulario llevándolo hasta abajo. Una de las maneras más sencillas y efectivas de hacer esto es usando **Flexbox**.

Comenzamos dando a nuestro **contenedor y formulario un alto del 100%**. Como este último ya es **flexible** y tiene la **dirección de columnas**, solo debemos agregarle en la mediaquery: ***justify-content: space-between***.

Esta propiedad posiciona el contenido horizontalmente cuando el valor de flex-direction es row. **En nuestro caso, el valor es columns por lo que justify-content va a aplicar verticalmente**.

***Space-beetween*** distribuye los items uniformemente dejando **el primer elemento al inicio y el último al final**.

```html
👉 Repasa sobre [Flex](https://platzi.com/clases/2008-html-css/31055-display-flex/).
```

## Cómo colocar imágenes en HTML
El elemento HTML ***img*** **incrusta** una imagen dentro de un documento. Su atributo de ***“src”*** es para mostrar en **dónde se encuentra** la imagen. Puede ser en alguna carpeta o una URL.

Por su parte, alt sirve para **agregar una descripción** a nuestra imagen. Esto es útil por cuestiones de SEO (optimización para buscadores) y también para mejorar la accesibilidad del sitio.

```html
Repasa esta información [aquí](https://platzi.com/clases/2008-html-css/31082-etiqueta-img/) 👈
```

**¿Qué contenedores usar?**

Existen dos etiquetas que nos permiten organizar imágenes de una manera semántica.

* [Figure](https://platzi.com/clases/2008-html-css/31081-etiqueta-figure/)

* [Picture](https://platzi.com/clases/2008-html-css/31222-imagenes-responsive/)

**Haz clic** en su respectivo **enlace** para descubrir sus principales características y formas de implementación.

## ¿Qué logra object-fit en CSS?

A las imágenes le aplicamos la propiedad **object-fit**, ya que resuelve **como el contenido se ajustará a su contendor**.

Sus valores pueden ser:

* *contain* → mantiene la relación de **aspecto** mientras **le ajusta dentro** del contendedor.
* *cover* → **mantiene** la realción de **aspecto**, pero la ajusta para **llenar el contenedor**.
* *fill* → **modifica su tamaño** para llenar el contenedor.
* *none* → no se redimensiona.
* *scale-down* → el contenido se dimensiona como si none o contain estuvieran especificados, lo que resulta en un **tamaño de objeto concreto más pequeño**.
  
[Documentación](https://developer.mozilla.org/es/docs/Web/CSS/object-fit).

## Cómo hacer un menu en HTML5

* Para crear un menú en HTML5 se emplea la etiqueta ***nav***. Este elemento respeta la [semántica](https://platzi.com/clases/2467-frontend-developer/40832-que-es-html-semantico/), puesto que representa una sección de la página cuyo propósito es **proporcionar enlaces de navegación**.
  
Estos enlaces de navegación pueden ser **etiquetas a** dentro de listas o **íconos**.

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/detalle.png)

## Uso de aside en HTML5

Esta vista la podemos incluir dentro de la etiqueta ***aside***, puesto que este elemento representa una sección de la página que consiste en **contenido que está indirectamente relacionado** con el principal del documento.

## ¿Qué es tranform en CSS?

***Transform*** que es una propiedad de CSS que nos permite **trasladar, rotar, escalar o sesgar** elementos.
Se implementan principalmente para desarrollar animaciones. Para rotar la flechita lo empleamos.

**¿Te gustaría animar con CSS?**
* [Curso de animaciones con CSS](https://platzi.com/cursos/animaciones-css/)
* [Curso práctico de maquetación y animaciones con CSS](https://platzi.com/cursos/animaciones-css-practico/)