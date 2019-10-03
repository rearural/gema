### Presentaciones usando Reveals con Javascrip

1) Descargar la carpeta de https://github.com/rearural/prueba/tree/gh-pages con el boton verde de "clone or download"

2) Descargar el editor de texto [sublime](https://www.sublimetext.com/)

3) Abrir el archivo tutorial.html con el navegador y con sublime

4) Caracteristicas de Reveals:

__Teclas útiles durante una presentación__:
-  ESC muestra el esquema de la presentación
-  Control o Alt + click hace zoom en donde hice click
- B o . ponen negro el fondo de la presentación

__Agregar diapositiva:__ todo lo que este entre "section" es una diapositiva
<section>

</section>

- __Agregar diapositiva vertical:__ 2 "section" dentro de otra "section" que las agrupa es una diapositiva con otra hacia abajo
<section>
  <section>

  </section>
  <section>

  </section>
</section>

- __Agregar texto:__
_<p>texto</p>_ donde dentro de "texto" escribo lo que va en esa diapositiva
_<h1> titulo </h1>_ titulo grande
<h2> titulo mas chico
<h3> subtitulo y asi sucesivamente

// para exportar a pdf (solo desde chrome o chromium)
<a href="https://github.com/presentacion.js#pdf-export">exportar a PDF esta presentación</a>

- __Cambiar el fondo__: en la primera parte del cuerpo del archivo (antes de las diapositivas) en la línea:
_<link rel="stylesheet" href="css/theme/color.css" id="theme">_ pudiendo cambiar _"color"_ por "black", "white, "sky", "beige", "simple", "serif", "blood", "night", "moon", "solarized"

- __Cambiar el fondo de una diapositiva específica independiente del resto del fondo de la presentacion:__ en la apertura de la diapositiva o "section":
	_<section data-background="color">_ donde "color" es cualquier color de fondo de los mencionados arriba

- __cambiar la transicion de fondo de una diapositiva a otra__
  <section data-transition="convex" data-background="white" data-background-transition="zoom">
	donde ahi el texto aparece de forma "convex" el fondo pasa a ser blanco y la transicion de fondo es con "zoom"
otras: none/fade/slide/convex/concave/zoom

// imagen para que sea el fondo
<section data-background="imagen.jpg">
<section data-background="imagen.jpg" data-background-repeat="repeat" data-background-size="500px"> para que se repita tipo cuadrille

// video de fondo
<section data-background-video="video.webm">
 y capaz hace falta agregar esto (no lo probe): data-background-color="#000000">
  <div style="background-color: rgba(0, 0, 0, 0.9); color: #fff; padding: 20px;">

// para insertar una presentacion dentro de una diapositiva
<iframe data-src="https://www.presentacion1.com" width="445" height="355" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:3px solid #666; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe>


// para agregar imagen en la diapositiva
<img src="imgagen.png"/>

// para escribir mas chico
<p o h1 o h2> <small> Lo que quiero escribir </small> </p o /h1 o /h2>

// para poner espacios o bajar el renglon
<BR>

// para crear un hipervinculo o link:
 <a href="https://pagina_web">lo q aparece en la diapositiva</a>

// Cursiva
 <em>lo que quiero escribir</em>


// para hacer una lista con viñetas
 <ul>
	 <li>una cosa</li>
	 <li>otra cosa</li>
	 <li>etc</li>

// para hacer lista numerica
	 <ol>
		 <li>lo que va 1ro</li>
		 <li>lo que va 2do</li>

// para hacer una Tabla
<table>
	<thead>
		<tr>
			<th>Item</th>
			<th>Value</th>
			<th>Quantity</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Apples</td>
			<td>$1</td>
			<td>7</td>
		</tr>
		<tr>
			<td>Lemonade</td>
			<td>$2</td>
			<td>18</td>
		</tr>
		<tr>
			<td>Bread</td>
			<td>$3</td>
			<td>2</td>
		</tr>
	</tbody>
</table>


 // Para hacer aparecer un texto
 <p o h1 o h2 class="fragment"> Texto</p o h1 o h2>
 Donde fragment puede ser: - "fragment grow" y se agranda
                           - "fragment shrink" y se achica
                           - "fragment fade-out" y desaparece
                           - "fragment fade-in-then-out"> aparece y desaparece
                           - "fragment fade-in-then-semi-out" aparece y se pone en gris

// Si quiero aparecer una imagen:
	<p class="fragment"> <img src="imagen.jpg"/> </p> por ejemplo

// Aparecer de distinta forma:
<span style="display: inline-block;" class="fragment fade-right"> texto que aparece desde la izquierda, </span>
 y cambiando "fragment fade-up/down/left" para cambiar desde donde aparece (arriba, abajo, derecha)

 // Pintar algo de color:
 <span class="fragment highlight-red">texto q se pinta</span> pinta en rojo
 "fragment highlight-blue" pinta azul
 "fragment highlight-green" pinta verde

// cosas de la configuracion del script:
- numero de pagina de la diapositiva: slideNumber: true, para que aparezcan o false para que no
- Transition style: transition: 'slide', // none/fade/slide/convex/concave/zoom
- Transition speed: transitionSpeed: 'default', // default/fast/slow
- Transition style for full page slide backgrounds: backgroundTransition: 'fade', // none/fade/slide/convex/concave/zoom (no me funciona)

3) para subir a la web (git-huib) en la terminal:
- en prueba git:(gh-pages):
 git status  
 git add "archivos modificados"
 git commit -m "descripcion del cambio"
 git push origin gh-pages
