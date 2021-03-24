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




[========]
