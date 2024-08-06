![metodologia BEM](/public/img/Metodología%20BEM.png)

# Que es BEM

BEM sirve para que nuestras clases de CSS estén más organizadas, no tengan problemas de especificidad y el código sea mucho más mantenible.

> En la metodologia BEM se usan solo clases.

## Que significa cada una de sus letras

- B significa bloque.
- E significa elemento
- M significa modificador

### Bloque

Es un contenido de la página que tiene significado por sí solo, es decir, podrías ponerlo en cualquier parte de la página y tendrá sentido.

**Algunos ejemplos de bloque.**

- Un footer
- Un menú de navegación.
- Una galería.
- un carrusel.

Estos elementos, donde sea que los pongamos, tendrán sentido por sí solos, no necesitan ayuda de algún otro elemento para tener significado.

#### ¿Como nombro a un bloque?

Imagina que tenemos el bloque de nav para escribirlo. En BEM usaremos esta clase.

##### Ejemplo

```html
<nav class="nav"></nav>
```

Llamaremos a nuestra clase CCS igual que a nuestro elemento HTML.

### Elemento

Un elemento no tiene significado por sí solo. Los elementos se crean dentro de los bloques.

> Importante: Un elemento no puede existir sin un bloque.

**Algunos ejemplos de elementos.**

- ul dentro de un menú de navegación.
- Un p dentro de una carta.
- Un logo dentro de un menú.
- enlaces dentro de un footer.

#### Como nombro a un elemento

**Sintaxis:** nombre del bloque + \_\_nombre del elemento

Siempre será el nombre del bloque, luego ponemos 2 barras bajas y, por último, el nombre del elemento.

##### Ejemplo

```html
nav__list nav__item
```

### Modificadores

Se aplican tanto a elementos como a bloques. Como su nombre indica, modifica los mismos.

**Algunos ejemplos de modificadores.**

- Bloque modificado, menú, cambio de color.
- Elemento modificado un botón para agrandar tamaño.

#### Como nombro a un modificador

Los modificadores se nombran con --

**Ejemplo de modificador en un bloque**

```html
nav--dark
```

**Ejemplo con un modificador en un elemento**

```html
nav__item__link--active
```

### ¿Pero mi BEM es muy largo como lo reduzco?

Podemos reducirlo de la siguiente manera, pero antes mira este ejemplo de HTML. Sin reducir, cabe aclarar que esto funciona perfectamente, pero si seguimos así, nuestras clases serán inmensas, como por ejemplo esta clase **nav\_\_list\_\_item\_\_link**

```html
<template>
	<nav class="nav">
		<ul class="nav__list">
			<li class="nav__list__item">
				<a class="nav__list__item__link" href="#enlace1">enlace1</a>
			</li>

			<li class="nav__list__item">
				<a class="nav__list__item__link" href="#enlace2">enlace2</a>
			</li>

			<li class="nav__list__item">
				<a
					class="nav__list__item__link  nav__list__item__link--active"
					href="#enlace3"
					>enlace3</a
				>
			</li>

			<li class="nav__list__item">
				<a
					class="nav__list__item__link  nav__list__item__link--hover"
					href="#enlace4"
					>enlace4</a
				>
			</li>
		</ul>
	</nav>
</template>
```

Como podemos ver en este ejemplo de arriba el elemento ul tiene esta clase **nav\_\_list** dentro de este tenemos un elemento de lista li con la clase **nav_list_item** y por último una etiqueta a con esta clase **nav\_\_list\_\_item\_\_link**, pero como nuestro elemento **li** está dentro de un **ul** podemos hacer la clase más corta y lo mismo pasa con el enlace

Vamos a ver cómo se hace de una mejor manera haciendo las clases más cortas.

```html
<nav class="nav">
        <ul class="nav__list">

            <li class="nav__item">
                <a class="nav__item__link" href="#enlace1">enlace1</a>
            </li>

            <li class="nav__item">
                <a class="nav__item__link" href="#enlace2">enlace2</a>
            </li>

            <li class="nav__item">
                <a class="nav__item__link  nav__item__link--active" href="#enlace3">enlace3</a>
            </li>

            <li class="nav__item">
                <a class="nav__item__link  nav__item__link--hover" href="#enlace4">enlace4</a>
            </li>
        </ul>
    </nav>
</template>
```

> Inportante esto es lo mismo que arriba pero refactorizado.

#### ¿Qué cambios hemos hecho?

1. Como nuestro elemento li está dentro de un elemento ul nosotros podemos quitar esta parte **\_\_list**, ya que se sobrentiende que un ul está dentro de un elemento li y así nuestra clase queda más limpia.

2. Nuestro elemento a podemos dejarlo así **nav\_\_item\_\_link** quitando la parte de **\_\_list**
   o incluso mejor, de esta manera que no está en el código **nav\_\_link** porque se sobrentiende que está dentro de un elemento li y no podemos repetir la clase porque esta misma se haría más larga.

## Conclusiones

1. BEM sirve para mejorar especificidad.

2. No tener problemas para saber dónde está un elemento.

3. Cuidado con las clases demasiado largas, procuremos quitar partes que no sean necesarias, como vimos en el apartado de qué cambios hemos hecho.
