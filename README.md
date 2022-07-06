# Iniciando con JSDOC 3

## Indice de contenidos

1. Qué es JSDOC
2. Añadiendo comentarios de documentación al código
3. generación de un sitio web con JSDOC

<style>
    p{
        font-family:Arial;
    }
</style>

## Qué es JSDOC
**JSDoc 3** es una API de generación de documentación de código JavaScript. similar a Javadoc o phpDocumentator.
en ella añades los comentarios de documentación del código fuente justo al lado del propio código. finalmente
la herramienta de JSDoc analiza el código fuente y genera un sitio web en html con la documentación del código.

## Añadiendo comentarios de documentación al código
El propósito de JSDoc es el documentar la API de una aplicación o librería JavaScript. asumiendo que se desea
documentar cosas como módulos, namespaces, clases, metodos, parámetros, etc.

los comentarios de JSDoc deben de se generalmente puestos inmediatamente antes del codigo a documentar. para ello
cada commentario debe de iniciar con > /** para que sean reconocidos por JSDoc. Los comentarios que comiencen con
/* , /*** ó más de 3 asteriscos serán ignorados, siendo esta una característica que te permite suprimir el análisis de bloques de comentarios.

la documentación más simple es sólo una descripción: 

´´´

/** Esta es una descripción de la función suma. */
function suma(a, b) {
    return a + b;
    }

´´´

Añadir una descripción es simple, sólo añade la descripción que gustes en el comentario de documentación

## Tabla 
 <table>
    <thead>
        <tr>
            <th> Nombre </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td> 
                <code type='javascript'>
                    
                </code>
            </td>
        </tr>
    </tbody>
 </table>

