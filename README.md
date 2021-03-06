# CURSO DE PREPROCESADORES CSS

## EVOLUCION DE LAS TECNOLOGIAS DEL FRONTEND

### INTRODUCCION A LOS PREPROCESADORES

Un preprocesador es una herramienta que nos permite escribir pseudocódigo de forma modular, más fácil de rehusar, leer, y mantener. pseudocódigo que después será convertido a CSS o HTML estándar que el navegador entiende.

Gracias a los preprocesadores podemos extender las características de CSS y HTML al nivel de otros lenguajes de programación, permitiéndonos usar características como variables, funciones y mixins.

- Variable, pedazo de memoria reservado para almacenar un valor, correspondiente a un tipo de dato. Es donde se guardan (y se recuperan) datos que se utilizan en un programa.

- Función, tiene la posibilidad de tener parámetros o argumentos, que son variables que modifican su comportamiento.

- Mixin, es una clase cuya finalidad es ofrecer una funcionalidad que pueda ser reutilizada en otras clases, pero ue no está pensada para usarse de forma autónoma.

¿Por qué utilizarlos?

- Te salva tiempo y dinero al tener la opción de rehusar código.
- Tener un código más sencillo de mantener y editar.
- Modularizar nuestros proyectos de una forma lógica y sencilla.

------------

### METODOLOGIAS PARA ESTRUCTURAR CODIGO

Las metodologías para estructurar código son sistemas preestablecidos, formales y bien documentados, que te ayudan a escribir y organizar código mantenible y escalable en sistemas grandes y complejos.

- BEM (Bloque, elemento, modificador)
- BEMIT (BEM + Triángulo invertido)
- ABEM (Atomic BEM)
- ITCSS (CSS de triángulo invertido)
- SMACSS
- ACSS (Atomic CSS)
- OOCSS (CSS orientado a objetos)
- AMCSS (Atribute Model CSS)
- SUIT CSS naming conventions


[Metodologias css 2020](https://2020.stateofcss.com/en-US/technologies/methodologies/ "Metodologias css 2020")

------------

### INTRODUCCION A BEM

El objetivo de BEM es dividir lógicamente las piezas de las que se compone una web.

BEM establece que debemos usar clases para nuestro selectores, clases que se dividen en:

- Bloques. Los bloques son nuestros contenedores más grandes que a su vez contienen elementos u otros bloques.

        .bloque{}
        .galeria{}
  
- Elementos. Los elementos siempre forman parte de un bloque, normalmente son los botones, textos, imágenes etc.

        .bloque__elemento{}
        .galeria__foto{}


- Modificadores. Los modificadores se usan para establecer estilos diferentes a un mismo bloque o elemento.
    
        .bloque__elemento{}
        .galeria__foto{}

**Ventajas de BEM**

- Menos repetición
- Los bloques tienen Independencia absoluta
- Mejoría en la herencia multiple
- Evitar la especificidad (no se sentirá la necesidad de usar !important nunca más)

[Official BEM](http://getbem.com/ "Official BEM")

------------

### GUÍAS PARA CREACIÓN Y MANTENIMIENTO DE CÓDIGO

La meta de tener una guía de código es hacer que luzca como si una sola persona lo haya escrito para que se entendible por todo el equipo.

Para nuestro proyecto PlatziGames vamos a tener una guía en la que definimos:

- Ser consistentes con la indentación.
- Consistencia con espacios, corchetes, puntos y comas.
- Consistencia de números, de selectores y divisiones.
- Agrupaciones de propiedades.
- Uso de ID’s y clases.

[Diseño Atlassian](https://atlassian.design/ "Diseño Atlassian")

[Salesforce Design](https://lightningdesignsystem.com/ "Salesforce Design")

[Guia de codigo](https://static.platzi.com/media/public/uploads/guia-de-codigo-platzi-games_f19c63bf-af70-4aeb-8ac1-3e905bc140ab.pdf "Guia de codigo")


------------

### INSTALACIÓN DE HERRAMIENTAS DE COMPILACIÓN

Pug no es html por lo tanto tenemos que convertirlo para que el navegador lo entienda.
Para compilarlo tenemos “2” opciones:

- Un cliente visual puede ser PREPROS.
- También podemos compilar usando la terminal de comandos.
	En la terminal.

	1. Debemos tener instalado nodeJS.
	2. Vamos a instalar la interfaz de comandos de pug con el comando npm install pug-cli -g
	3. ¿Como compilamos?
		3,1. pug archivo.pug //Compila solo una vez
		3,2. pug -w archivo.pug //Compila cada vez que el archivo cambia pero con un html comprimido.
		3.3 pug -w --pretty archivo.pug //Compila cada vez que el archivo cambia pero con un html bonito



[Editor de codigo](https://code.visualstudio.com/ "Editor de codigo")

[Compilador de preprocesador](https://codekitapp.com/ "Compilador de preprocesador")

[Compilacion MAC](https://prepros.io/ "Compilacion MAC")

[Extension VSC preprocesador](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass "Extension VSC preprocesador")


------------



[========]

## PREPROCESADORES PARA HTML

### INTRODUCCION A PUG

Pug es un generador de templates implementado con Javascript que nos permite escribir un pseudocódigo limpio y fácil de leer que será compilado a HTML.

[Pug js](https://pugjs.org/api/getting-started.html "Pug js")


------------


### SINTAXIS

Si quieren compilar los archivos Pug primero necesitan instalar NodeJS.
Luego desde la terminal instalar pug :

>>npm install pug-cli -g

y ya pueden compilar desde visual studio code


>>pug archivo.pug  
 compila una sola vez

>>pug -w archivo.pug
 compila cada vez que el archivo cambia, genera un HTML minificado

>>pug -w --pretty archivo.pug
 compila un HTML identado

>>pug directorio
 compila todos los archivos dentro de ese directorio
 

------------

### INTERPOLACION

La interpolación es cuando se tienen variables y se le quiere concatenar texto que usualmente ser haría así

    - var user = "Alejandra"; 
    h1 "Hola " + user + ", cómo estas?"
Se realice de la siguiente forma

    h1 Hola #{user}, cómo estas?

------------

### VARIABLES

Las variables no vienen de forma nativa en HTML pero con PUG podemos usarlas. En ellas almacenamos datos y los reutilizarlos en todo nuestro archivo HTML evitándonos tener que escribir lo mismo una y otra vez.

sintaxis para declarar una variable en pug.

    -var titulo = "Subtítulo Principal"
    -var titulos = ["Título Principal", "Subtitulo 1", "Subtitulo 2", "Subtitulo 3"]



------------



### CONDICIONALES Y LOOPS

Un condicional nos permite evaluar cierta condición y bifurcar entre dos caminos dependiendo de si se cumple o no.

Un loop es un fragmento de código que va a ejecutar de forma repetitiva hasta que cumpla una condición.


------------

### MIXINS

Su finalidad es ofrecer una funcionalidad que pueda ser reutilizada en otras clases pero que no está pensada para usarse de forma autónoma. Nos permite crear bloques reusables de código que cambian su resultado dependiendo del parámetro que enviemos.

Con los mixin logramos escribir menos código, produciendo un código más claro, más expresivo y sobre todo más fácil de mantener.

La forma de llamar un mixin es con "+" seguido del nombre del mixin


------------

### INCLUDES Y EXTENDS

Pug funciona como un generador de plantillas, dos de sus principales características para lograrlo son Includes y Extends.

Los includes sirven para incluir un archivo de extensión *.pug dentro de otro.

Los extends te permiten adicionar bloques de código a una página.

El include te trae sin mas el fragmento de código del archivo al que haces referencia y no puedes meter código pero el extends no solo te trae el código sino que puedes decirle en qué posición de ese código que te traes puedes colocar un nuevo código.

El extends funciona como un mixin ya al que le pasas “parámetros” (pero en el extends sería el nombre que le das al bloque) cuando lo ejecutas y luego lo utilizas en donde le especifiques.
Por ejemplo:

	mixin prueba(texto) // este es el parámetro al que hago referencia
	p= texto // Acá lo utilizas

En cambio si usas el extends

	// Primero definirías tu archivo al que vas a extender posteriormente
	div.contenedor
	img(src="images/image.png")
	block texto

	// Y luego lo usarías
	extends archivo.pug
	block texto
	p	Texto de pruebas // Esto es lo que pasaría a ser como el parámetro del mixin ya que se incluirá en donde tú definiste el block


------------


[========]

## LESS
### INTRODUCCION A LESS

Less es un preprocesador para CSS que nos permite trabajar hojas de estilo con funcionalidades de un lenguaje de programación.

El ampersand (&) es un selector en Less que sirve para referenciar la estructura completa hacia arriba, desde donde se utiliza. es un comodín para sustituir el elemento padre (pero no solo el elemento padre, sino el padre con todos sus padres).

Si lo quieren ejecutar desde la terminal lo pueden hacer de la siguiente manera:

    npm install -g less
    lessc platzigames.less platzigames.css

------------

### ANIDAMIENTOS E IMPORTS

Creamos un archivo nuevo que contentra el estilo del intro, llamado intros.less

	.intro {
    width: 1340px;
    height: 650px;
    padding: 10px;
    margin: 0 auto;
    position: relative;
    
    // Aca se indica que esa clase esta dentro de intro
    /* .intro__imagen {
        width: 1320px;
        position: absolute;
    } */
    
    // Aca el signo & indica que la primera parte tiene la misma clase  en este caso intro

    &__imagen {
        width: 1320px;
        position: absolute;
        img{
            width: 100%;
            height: 624px;
            object-fit: cover;
        }
    }

    &__contenido{
        width: 50%;
        margin: 0 auto;
        position:absolute;
        top:156px;
        left: 0;
        right: 0;
        text-align: center;
        color: white;
    }
    &__categoria{
        font-family: 'Oswald',sans-serif;
        text-transform: uppercase;
    }

    &__titulo{
        font-family: 'Oswald',sans-serif;
        text-transform: uppercase;
        font-size: 50px;
    }

    &__autor{
        width: 150px;
        margin: 0 auto;
        position: absolute;
        top: 400px;
        left:0;
        right: 0;
        color: white;
        img{
            width: 60px;
            height: 50px;
            float: left;
            padding-right: 10px;
            border-radius: 10em;
        }
        span{
            display: inline-block;
        }
    }
	}

Nuestro archivo platzigames.less

	@import "globales.css";
	@import "intros.css";

------------



### VARIABLES

En las variables almacenamos datos que se puede reutilizar en todas nuestras hojas de estilos. Así evitamos tener que escribir lo mismo una y otra vez cuando se realiza algún cambio, ya que sólo vamos a modificar el valor de la variable y se aplicará a todos los lugares donde sea usada.

Comúnmente almacenamos en variables las guías de estilo de nuestro sitio, como pueden ser los colores y fuentes.

Añadir a globales.less las siguientes variables

    @color-claro: #FFF;
    @color-primario: #333;
    @color-secundario: #8841da;
    @color-variacion: #012179;
    @Fuente1: 'Lato', sans-serif;
    @Fuente2: 'Oswald', sans-serif;
	

Reemplazar las fuentes y los colores por el nombre de las variables


------------

### FUNCIONES

La diferencia entre mixins y funciones es que las funciones por general hacen cálculos y regresan un resultado que es usado como valor de alguna propiedad.

Las funciones en Less ya están prediseñadas.

[Documetacion oficial](http://lesscss.org/#functions "Documetacion oficial")



------------


### MIXIN

Su finalidad es ofrecer una funcionalidad que pueda ser reutilizada en otras clases pero que no está pensada para usarse de forma autónoma. Nos permite crear bloques reusables de código que cambian su resultado dependiendo del parámetro que enviemos.

Con los mixins logramos escribir menos código, produciendo un código más claro, más expresivo y sobre todo más fácil de mantener.



------------


[========]

## SASS

### INTRODUCCION A SASS

Sass (Syntactically Awesome StyleSheets) es una extensión de CSS que añade características muy potentes y elegantes a este lenguaje de estilos.

Sass es basado en Ruby a diferencia de Less y Stylus que se basan en Javascript.

Instalar sass

`npm install -g sass`

Compilar de sass a css

`sass --watch ejercicio-sass.scss ejercicio-sass.css`



------------

### VARIABLES

En las variables almacenamos datos que se puede reutilizar en todas nuestras hojas de estilos. Así evitamos tener que escribir lo mismo una y otra vez cuando se realiza algún cambio, ya que sólo vamos a modificar el valor de la variable y se aplicará a todos los lugares donde sea usada.

Comúnmente almacenamos en variables las guías de estilo de nuestro sitio, como pueden ser los colores y fuentes.

    // Asi se declaran variables
    $Fuente1:'Lato',sans-serif;
    $Fuente2:'Oswald',sans-serif;
    $color-primario:#333333;
    $color-claro:#FFFFFF;
    $color-secundario:#8841DA;
    $color-variacion:#3F579A;
    
    *{
        box-sizing: border-box;
    }
    
    body{
        margin: 0;
        font-family: $Fuente1; // Asi como se usan
    }

------------

### IMPORT Y EXTENDS

Import nos permite escribir código modular separando en diferentes archivos para después importarlos todos en uno solo y tener una base código mucho más ordenada.

Extends sirve para insertar los estilos de un selector en otro.


------------

### MIXIN

Su finalidad es ofrecer una funcionalidad que pueda ser reutilizada en otras clases pero que no está pensada para usarse de forma autónoma. Nos permite crear bloques reusables de código que cambian su resultado dependiendo del parámetro que enviemos.

Con los mixin logramos escribir menos código, produciendo un código más claro, más expresivo y sobre todo más fácil de mantener.

    @mixin caja {
    	border-radius: 20px;
    	box-shadow: 0px 20px 33px 0px rgba(0, 0, 0, 0.50);
    	color: $color-primario;
    	background-color: $color-claro;
    }

Se lo llama en el archivo con la palabra include y el nombre del mixin

	@include caja 

------------



### FUNCIONES

La diferencia entre mixins y funciones es que las funciones por general hacen cálculos y regresan un resultado que es usado como valor de alguna propiedad.

Crear archivo _galerias.scss
Añadir un include en nuestro archivo compilado

    .galeria {
        width: 50%;
        height: 250px;
        margin: 10px auto;
        padding: 20px 0 0 30px;
        justify-content: space-evenly;
        @include caja;
        &__foto-principal {
            float: left;
            margin-right: 10px;
        }
        &__fotos-adicionales img {
            height: 70px;
            margin-right: 5px;
            margin-bottom: 5px;
        }
        h2 {
            margin-bottom: 10px;
            text-transform: uppercase;
            font-weight: 600;
            font-size: 20px;
            font-family: $Fuente2;
        }
    
        img {
            border-radius: 10px;
        }
    }

Crear funcion en _globales.scss

    @function get-opacity ($color, $nivel) {
    	@return rgba($color, $nivel);
    }


------------


### CONDICIONALES Y LOOPS

Un condicional nos permite evaluar cierta condición y bifurcar entre dos caminos dependiendo de si se cumple o no.

Un loop es un fragmento de código que va a ejecutar de forma repetitiva hasta que cumpla una condición.

    @mixin titulos ($fuente) {
    	@if $fuente==$Fuente1 {
    		font-family: $Fuente1;
    	} @else {
    		font-family: $Fuente2;
    		text-transform: uppercase;
    	}
    }
    
    
    @each $header, $size in (h1: 30px, h2: 25px, h3: 20px) {
    	#{$header} {
    		font-size: $size;
    		margin: 0;
    	}
    }

------------


### FINALIZANDO EJERCICIO



<img src="https://static.platzi.com/media/user_upload/2020-09-12%2000_58_30-PlatziGames-d07ad39c-4e83-45e9-96bc-9ef38b0e6863.jpg" alt="reto">

Crear mixin

    @mixin mode-background ($color) {
    	@if $color == $color-primario {
    			background-color: $color-primario;
    			color: $color-claro;
    			.perfil__nombre{
    				color: $color-secundario;
    				@include titulos($Fuente2);
    			}
    
    			.perfil__titulo{
    				color: $color-variacion;
    				@include titulos($Fuente2);
    			}
    
    			.perfil__boton {
    				color: $color-claro;
    				background-color: $color-variacion;
    			}
    
    	} @else  {
    			background-color: $color-claro;
    			color: $color-primario;
    		.perfil__nombre{
    			color: $color-secundario;
    			@include titulos($Fuente2);
    		}
    
    		.perfil__titulo{
    			color: $color-variacion;
    			@include titulos($Fuente2);
    		}
    
    		.perfil__boton {
    			color: $color-claro;
    			background-color: $color-variacion;
    		}
    	}
    }


Agregar el mixin a _perfiles.scss

    .perfil {
    	width: 40%;
    	padding-top: 50px;
    	color: $color-claro;
    	background-color: $color-secundario;
    	@include mode-background ($color-claro);
    	&__avatar {
    		display: block;
    		margin: 0 auto;
    		border-radius: 50em;
    	} ...... //Continua parte del codifo hecho en las clases


Agregar el Mixion en _articulos.scss

    .articulos {
    	width: 60%;
    	padding: 50px 0 0 50px;
    	@include mode-background ($color-primario);
    }
	

<img src="https://static.platzi.com/media/user_upload/2020-09-12%2000_58_30-PlatziGames-d07ad39c-4e83-45e9-96bc-9ef38b0e6863.jpg" alt="reto">


------------





[========]


## STYLUS

### INTRODUCCION A STYLUS

**Instalar Stylus en la terminal**

`npm install -g stylus`

**Compilar de Stylus a Css [deben estar en la carpeta /css]**

`stylus -w ejercicio-stylus.styl`

-w hace que espere los cambios para poder compilar automaticamente.

[Official Page](https://stylus-lang.com/ "Official Page")

------------

### VARIABLES

En las variables almacenamos datos que se puede reutilizar en todas nuestras hojas de estilos. Así evitamos tener que escribir lo mismo una y otra vez cuando se realiza algún cambio, ya que sólo vamos a modificar el valor de la variable y se aplicará a todos los lugares donde sea usada.

Comúnmente almacenamos en variables las guías de estilo de nuestro sitio, como pueden ser los colores y fuentes.

Variables

    Fuente1 = 'Lato', sans-serif
    Fuente2 = 'Oswald', sans-serif
    color-primario = #333333
    color-secundario = #8841da
    color-claro = #FFFFFF


------------


### MIXINS

Su finalidad es ofrecer una funcionalidad que pueda ser reutilizada en otras clases pero que no está pensada para usarse de forma autónoma. Nos permite crear bloques reusables de código que cambian su resultado dependiendo del parámetro que enviemos.

Con los mixins logramos escribir menos código, produciendo un código más claro, más expresivo y sobre todo más fácil de mantener.

Se declara: 
	`nombreMixin()`

Se manda a llamar de la misma manera
	`nombreMixin()`


Mixin


```
contenedor()
	display: flex
	width 90%
	margin 0 auto
	padding: 30px 0

caja-sombra()
	background-color: color-claro
	box-shadow: 0px 20px 33px 0px rgba(0,0,0,0.20)

```

Codigo añadido


```
.contenido 
	margin-bottom 40px
	justify-content: space-evenly
	contenedor()

.caja
	max-width: 400px
	caja-sombra()

	&__contenido 
		padding: 20px
		background-color: color-claro
		span
			text-transform: uppercase 
			color: color-secundario
			font-family: Fuente2 
		h3 
			text-transform: uppercase 
			font-weight: normal
			font-family: Fuente2 

```


------------



###  FUNCIONES

La diferencia entre mixins y funciones es que las funciones por general hacen cálculos y regresan un resultado que es usado como valor de alguna propiedad.

Archivo raiz



```
@import "../componentes/globales.styl"
@import "../componentes/buscadores.styl"
@import "../componentes/filtros.styl"
@import "../componentes/cajas.styl"
@import "../componentes/estadisticas.styl"
```

Funcion en archivo globlales.stly



```
opacidad(color, cantidad)
	alpha(color, cantidad)
```

Archivo estadisticas.styl


```
.estadistica--articulos
    height: 70px
    padding: 20px
    border-top: 1px solid color-primario
    ul
        display: flex 
        margin: 0
        padding: 0
        justify-content: space-evenly
        li 
            list-style: none
            color: opacidad(color-primario, .30)
        span
            margin-left: 10px
```


------------

### CONDICIONALES Y LOOPS

Un condicional nos permite evaluar cierta condición y bifurcar entre dos caminos dependiendo de si se cumple o no.

Un loop es un fragmento de código que va a ejecutar de forma repetitiva hasta que cumpla una condición.

    titulos(fuente)
    	if fuente == Fuente1
    		font-family: Fuente1
    	else 
    		font-family: Fuente2
    		font-weight: 600
    		text-transform: uppercase
    

Reto

<img src="https://static.platzi.com/media/user_upload/Platzi%20Games%20-%20Reto%20Stylus-31d921fc-026f-4ff2-a117-4d551629884c.jpg" alt="reto">



------------





[========]






