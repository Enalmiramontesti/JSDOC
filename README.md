# Iniciando con JSDOC 3

## Indice de contenidos

1. Qué es JSDOC
2. Añadiendo comentarios de documentación al código
3. generación de un sitio web con JSDOC


## Qué es JSDOC
**JSDoc 3** es una API de generación de documentación de código JavaScript. similar a Javadoc o phpDocumentator.
en ella añades los comentarios de documentación del código fuente justo al lado del propio código. finalmente
la herramienta de JSDoc analiza el código fuente y genera un sitio web en html con la documentación del código.

## Añadiendo comentarios de documentación al código
El propósito de JSDoc es el documentar la API de una aplicación o librería JavaScript. asumiendo que se desea
documentar cosas como módulos, namespaces, clases, metodos, parámetros, etc.

los comentarios de JSDoc deben de se generalmente puestos inmediatamente antes del codigo a documentar. para ello
cada commentario debe de iniciar con ``` /** ``` para que sean reconocidos por JSDoc. Los comentarios que comiencen con
``` /* ``` , ``` /*** ``` ó más de 3 asteriscos serán ignorados, siendo esta una característica que te permite suprimir el análisis de bloques de comentarios.

la documentación más simple es sólo una descripción: 

```javascript

/** Esta es una descripción de la función suma. */
function suma(a, b) {
    return a + b;
    }
```


Añadir una descripción es simple, sólo añade la descripción que gustes en el comentario de documentación

Las etiquetas de documentación especiales pueden ser utilizadas para dar más información, por ejemplo, si la funcion es el constructor de una clase, puedes indicar esto añadiendo la etiqueta ``` @constructor ```

**Utilizando una etiqueta de documentación especial**
```javascript	
/**
 * Este constructor representa un cliente
 * @constructor
 */
 function Cliente(nombre, apellido){
 }
```

Así mismo se pueden añadir más etiquetas para brindar más información, en la tabla inferior se encuentran las etiquetas reconocidas por JSDoc 3.


***Añadiendo más información con etiquetas***

```javascript
/**
 * Este constructor representa un cliente
 * @constructor
 * @param {string} nombre - El nombre del cliente
 * @param {string} apellido - El apellido del cliente
 */
 function Cliente(nombre, apellido){
 }
```

## generación de un sitio web con JSDOC


Una vez que tu código está comentado, puedes utilizar la herramienta JSDoc 3 para generar un sitio web HTML a partir de tus archivos fuente.

por defecto, JSDoc utiliza la plantilla "default" para convertir la documentación en HTML. Puedes editar esta plantilla para que se adapte a tus necesidades o crear una plantilla completamente nueva si es lo que prefieres.

Ejecutar el generador de documentación en la línea de comandos
``` jsdoc book.js ```
Este comando creará un directorio llamado out/ en el directorio de trabajo actual. Dentro de ese directorio, encontrarás las páginas HTML generadas.



## Tabla 

 <table>
    <thead>
        <tr>
            <th> Etiqueta </th>
            <th> Descripción </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td> @abstract </td>
            <td> This member must be implemented (or overridden) by the inheritor. </td>
        </tr>
        <tr>
            <td> @access </td>
            <td> especifica el nivel de acceso de este miembro (private, package-private, public, ó protected). </td>
        </tr>
        <tr>
            <td> @alias </td>
            <td> trata el miembro como si tuviera un nombre diferente. </td>
        </tr>
        <tr>
            <td> @async </td>
            <td> indica que una función es asíncrona. </td>
        </tr>
        <tr>
            <td> @augments (synonyms: @extends) </td>
            <td> Indica que el simbolo se hereda desde, y se añade a el símbolo padre </td>
        </tr>
        <tr>
            <td> @author </td>
            <td> Identifica el autor. </td>
        </tr>
        <tr>
            <td> @borrows </td>
            <td> este objeto usa algo desde otro objeto. </td>
        </tr>
        <tr>
            <td> @callback </td>
            <td> Documenta una función Callback. </td>
        </tr>
        <tr>
            <td> @class (synonyms: @constructor) </td>
            <td> documenta una clase. </td>
        </tr>
        <tr>
            <td> @classdesc </td>
            <td> documenta la descripción de una clase. </td>
        </tr>
        <tr>
            <td> @constant (synonyms: @const) </td>
            <td> Documenta un objeto como constante. </td>
        </tr>
        <tr>
            <td> @constructs </td>
            <td> Esta función miembro será el constructor de la clase previa. </td>
        </tr>
        <tr>
            <td> @copyright </td>
            <td> Documenta información de copyright. </td>
        </tr>
        <tr>
            <td> @default (synonyms: @defaultvalue) </td>
            <td> Documenta el valor por defecto. </td>
        </tr>
        <tr>
            <td> @deprecated </td>
            <td> Documenta algo obsoleto </td>
        </tr>
        <tr>
            <td> @description (synonyms: @desc) </td>
            <td> Describe un simbolo. </td>
        </tr>
        <tr>
            <td> @enum </td>
            <td> Documenta una colección de propiedades relacionadas. </td>
        </tr>
        <tr>
            <td> @event </td>
            <td> Documenta un evento. </td>
        </tr>
        <tr>
            <td> @example </td>
            <td> provee un ejemplo de cómo utilizar el item documentado </td>
        </tr>
        <tr>
            <td> @exports </td>
            <td> identifica un miembro que es exportado desde un módulo javascript (O typescript). </td>
        </tr>
        <tr>
            <td> @file (synonyms: @fileoverview, @overview) </td>
            <td> Describe un archivo. </td>
        </tr>
        <tr>
            <td> @fires </td>
            <td> Este objeto emite un evento. </td>
        </tr>
        <tr>
            <td> @function (synonyms: @func) </td>
            <td> Documenta una función. </td>
        </tr>
        <tr>
            <td> @global </td>
            <td> This symbol is meant to be global. </td>
        </tr>
        <tr>
            <td> @ignore </td>
            <td> This symbol is meant to be ignored. </td>
        </tr>
        <tr>
            <td> @implements </td>
            <td> This symbol implements an interface. </td>
        </tr>
        <tr>
            <td> @inheritdoc </td>
            <td> This symbol inherits the documentation from a parent symbol. </td>
        </tr>
        <tr>
            <td> @inner </td>
            <td> This symbol is an inner symbol. </td>
        </tr>
        <tr>
            <td> @instance </td>
            <td> This symbol is an instance member. </td>
        </tr>
        <tr>
            <td> @interface </td>
            <td> This symbol is an interface. </td>
        </tr>
        <tr>
            <td> @kind </td>
            <td> Document the kind of symbol. </td>
        </tr>
        <tr>
            <td> @lends </td>
            <td> This symbol is a property of another symbol. </td>
        </tr>
        <tr>
            <td> @license </td>
            <td> Document the license information. </td>
        </tr>
        <tr>
            <td> @listens </td>
            <td> This object listens for an event. </td>
        </tr>
        <tr>
            <td> @member </td>
            <td> This symbol is a member of a parent symbol. </td>
        </tr>
        <tr>
            <td> @memberof </td>
            <td> This symbol is a member of a parent symbol. </td>
        </tr>
        <tr>
            <td> @method </td>
            <td> Document a method. </td>
        </tr>
        <tr>
            <td> @mixes </td>
            <td> This symbol mixes in the properties of another symbol. </td>
        </tr>
        <tr>
            <td> @mixin </td>
            <td> This symbol is a mixin. </td>
        </tr>
        <tr>
            <td> @module </td>
            <td> This symbol is a module. </td>
        </tr>
        <tr>
            <td> @name </td>
            <td> Document the name of a symbol. </td>
        </tr>
        <tr>
            <td> @namespace </td>
            <td> This symbol is a namespace. </td>
        </tr>
        <tr>
            <td> @param </td>
            <td> Document a parameter. </td>
        </tr>
        <tr>
            <td> @private </td>
            <td> This symbol is private. </td>
        </tr>
        <tr>
            <td> @property </td>
            <td> Document a property. </td>
        </tr>
        <tr>
            <td> @protected </td>
            <td> This symbol is protected. </td>
        </tr>
        <tr>
            <td> @public </td>
            <td> This symbol is public. </td>
        </tr>
        <tr>
            <td> @readonly </td>
            <td> This symbol is read-only. </td>
        </tr>
        <tr>
            <td> @requires </td>
            <td> This symbol requires another symbol. </td>
        </tr>
        <tr>
            <td> @returns </td>
            <td> Document the return value. </td>
        </tr>
        <tr>
            <td> @see </td>
            <td> Document a related symbol. </td>
        </tr>
        <tr>
            <td> @since </td>
            <td> Document the version of the software that first provided this symbol. </td>
        </tr>
        <tr>
            <td> @static </td>
            <td> This symbol is static. </td>
        </tr>
        <tr>
            <td> @summary </td>
            <td> Document a summary of the symbol. </td>
        </tr>
        <tr>
            <td> @this </td>
            <td> This symbol is a property of the current object. </td>
        </tr>
        <tr>
            <td> @throws (synonyms: @exception)</td>
            <td> This function throws an error. </td>
        </tr>
        <tr>
            <td> @type </td>
            <td> Document the type of a symbol. </td>
        </tr>
        <tr>
            <td> @typedef </td>
            <td> Document a type definition. </td>
        </tr>
        <tr>
            <td> @version </td>
            <td> Document the version of the software that first provided this symbol. </td>
        </tr>
        <tr>
            <td> @yield </td>
            <td> This function yields a value. </td>
        </tr>
        <tr>
            <td> @yields </td>
            <td> This function yields a value. </td>
        </tr>  
    </tbody>
 </table>



Copyright © 2011-2017 the contributors to the JSDoc 3 documentation project.


JSDoc is freely distributable under the terms of the MIT license.

traducido por:
[@Enalmiramontesti](https://github.com/Enalmiramontesti)
[@Airdel](https://github.com/Airdel)
