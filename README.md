# Que es BEM

BEM sirve para que nuestras clases de CSS esten mas organizadas no tengan problemas de especificidad y el codigo sea mucho mas mantenible.

> En la metodologia BEM se usan solo clases.


## Que significa cada una de sus letras

 - B  significa bloque.
 - E significa elemento
 - M  significa modificador 

### Bloque

  Es un contenido de la pagina que tiene significado por si solo es decir podrias ponerlo en cualquier parte de la pagina y tendra sentido.

 **Algunos ejemplos de bloque.**

  - Un footer 
  - un menu de navegacion
  - una galeria
  - un carrusell

Estos elementos donde sea que los pongamos tendran sentido por si solos no necesitan ayuda de algun otro elemento para tener significado.

#### Como nombro a un bloque?

Imagina que tenemos el bloque de nav para escribirlo en Bem usaremos esta clase.

##### Ejemplo
```html
<nav class="nav"></nav>
```

LLamaremos a nuestra clase CCS igual que a nuestro elemnto HTML.

### Elemento

Un elemento no tiene significado por si solo los elementos se crean dentro de los bloques

> Inportante: Un elemento no puede existir sin un bloque.


**Algunos ejemplos de elementos.**

- ul dendro de un menu de navegacion.
- Un p dentro de una carta.
- un logo dentro de un menu.
- enlaces dentro de un footer.


#### Como nombro a un elemento

**Sintaxis:** nombre del bloque + __nombre del elemento

Siempre sera nombre del bloque luego ponemos 2 barra baja y por ultimo el nombre del elemento.

##### Ejemplo

```html
nav__list
nav__item
```


### Modificadores

Se aplican tanto a elementos como a bloques. Como su nombre indica modifica los mismos.

**Algunos ejemplos de modificadores.**

- bloque modificado menu cambio de color.
- elemento mdifiado boton agrandar tamaño.

#### Como nombro a un modificador

Los modifocadores se nombran con --


**Ejemplo de modificador en un bloque**

```html
nav--dark
```

**Ejemplo con un modificador en un elemento**

```html
nav__item__link--active
```


### Pero mi BEM es muy largo como lo reduzco?

Podemos reducirclo de la siguente manera mira este ejemplo de HTML sin reducir.