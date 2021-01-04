# Cheatsheet + Documentación Javascript💻

¿Este es un cheatsheet mas de Javascript? No. Este cheatshet tambien contiene un wiki con la documentación mas importante de python acá:
[Wiki Documentación Javascript](https://github.com/fabiansato/javascript-cheatsheet/wiki "Documentación de Javascript")

------------------------------
# Introducción a los conceptos básicos de JavaScript
------------------------------
## Condiciones
Javascript es case-sensitive
Javascript es flexible, una variable puede ser int, luego string etc

## Mostrar datos por pantalla
La función ```console.log(<mensaje /  variables / funciones>)``` muestra un mensaje por consola /  variables / funciones

## Adjuntar javascript
podemos ponerlo en el mismo html como
```html
<script>
  aca va el codigo
</script
```
o podemos agregarlo a otro archivo con src
  
```html
  <script src="codigo.js"></script>
```

---------------------------------
### Comentarios

Hay 2 tipos de comentarios:
```javascript
// este es un comentario de una sola línea
```
otro tipo:
```javascript
/*
Esto es un comentario de varias líneas linea 1
linea 2
linea 3 Ultima linea!
*/
```

------------------------------
# Variables en JS
------------------------------

## Variables
### Tipo de variables
En javascript podemos encontrar este tipo de variables:
```javascript
Numericas, strings, arrays, booleans
```

### Carga de variables
tipo var (Se puede asignar con '' o con "") (es valida fuera del for)
```javascript
var nombre = 'juan';
```

tipo let (Se puede asignar con '' o con "") (solo es valido en un fragmento de codigo, ejemplo dentro solo de un for)
```javascript
let nombre = 'juan';
```

tipo const (Se asigna una vez pero no se puede volver a asignar:
```javascript
const nombre = 'juan';
```

booleanos (true o false | 1 o 0):
```javascript
var esbooleano = true;
```
Javascript permite cambiar de tipos de variables y eso hay que tener cuidado! Podemos tener una variable en string y cambiarla a numerica!

---------------------------------
### Carga de vectores
Podemos cargar info de un vector así:
```javascript
var meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre']; //vector con cantidad de meses

```
Podemos cargar vectores vacios:
```javascript
var meses = []; 
```
Todos los indices de los vectores empiezan en 0.

------------------------------
# Estructura de datos en JS
------------------------------
## Estructura IF:

```javascript
If (<condiciones>) {
// Código a ejecutar cuando se cumplen las condiciones
} else {
// Código a ejecutar cuando NO se cumple alguna de las condiciones
}
```

## Bucle FOR
```javascript
for(let contador=1; contador<=10; contador++) { 
console.log(contador);
}
```

## Bucle While
```javascript
var contador = 1; 
while(contador<=10) {
console.log(contador);
contador++;
}
```

## Funciones
```javascript
function sumar(valor1, valor2) { 
return valor1 + valor2;
}
```
y llamamos la funcion asi:
```javascript
var total = sumar(10,20); 
console.log(total);
```
------------------------------
# Introducción y manejo del DOM
------------------------------
## Árbol de nodos:

<img src="https://fabiansato.github.io/imagenes/javascript-nodos2.gif">

## Tipos de nodos creados:
```html
●	Document, nodo raíz del que derivan todos

●	Element, cada una de las etiquetas. Único nodo que puede contener atributos y del que pueden derivar otros nodos.

●	Attr, se define uno para cada par atributo=valor

●	Text, contiene el texto encerrado por una etiqueta

●	Comment, representa los comentarios incluidos en la página.
```
## Hay 3 funciones para acceder directamente a un nodo:
```javascript
getElementsByTagName(nombreEtiqueta)
getElementsByClassName(nombreAtributo)
getElementById(id)
```

## ** Crear un nodo
-------------------------

Recordar que cada elemento genera 2 nodos. 4 pasos:
1.	Creación de un nodo de tipo Element que represente al elemento.
2.	Creación de un nodo de tipo Text que represente el contenido del elemento.
3.	Añadir el nodo Text como nodo hijo del nodo Element.
4.	Añadir el nodo Element a la página,en forma de nodo hijo del nodo correspondiente al lugar en el que se quiere insertar el elemento.

## Implica utilizar 3 funciones DOM:

●	`createElement(etiqueta):` crea un nodo de tipo Element que representa al elemento cuya etiqueta se pasa como parámetro.
●	`createTextNode(contenido):` crea un nodo de tipo Text que almacena el
contenido textual de los elementos.
●	`nodoPadre.appendChild(nodoHijo)`: añade un nodo como hijo de otro nodo. Se debe utilizar al menos dos veces con los nodos habituales: en primer lugar se añade el nodo Text como hijo del nodo Element y a continuación se añade el nodo Element como hijo de algún nodo de la página.


Ejemplo para la creación de un párrafo
```javascript
// Crear nodo de tipo Element
var parrafo = document.createElement("p");

// Crear nodo de tipo Text
var contenido = document.createTextNode("Hola Mundo!");

// Añadir el nodo Text como hijo del nodo Element 
parrafo.appendChild(contenido);

// Añadir el nodo Element como hijo de la página 
document.body.appendChild(parrafo);
```
## Eliminar un nodo
Afortunadamente, eliminar un nodo del árbol DOM de la página es mucho más sencillo que añadirlo. En este caso, solamente es necesario utilizar la función  `removeChild(nodo)` que debe ser invocada desde el elemento padre. Para acceder al padre de un nodo: `nodoHijo.parentNode`
```javascript
var parrafo = document.getElementById("provisional");
parrafo.parentNode.removeChild(parrafo);
```
```html
<p id="provisional">...</p>
```


------------------------------
# AAAAAAAAAAAA
------------------------------

