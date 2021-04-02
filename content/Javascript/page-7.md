+++
title = "Arreglos"
chapter = true
weight = 7
pre = "<b>7. </b>"
+++
## Arreglos
Los arrays son objetos similares a una lista cuyo prototipo proporciona métodos para efectuar operaciones de recorrido y de mutación. Tanto la longitud como el tipo de los elementos de un array son variables.

- Declaración:
~~~javascript
let arreglo = ["hola", 1, true, {}];
~~~
- Declración de un arreglo y recorrerlo con un **for**
~~~javascript
let arreglo = [5, 9, 6];

for (let i = 0; i < arreglo.length; i++) {
    const elemento = arreglo[i];
    console.log(elemento);
}
~~~
- Agregar y quitar elementos de un arreglo:

   - push(); **agrega un elemento al final.**
   - pop(); **quita el ultimo elemento.**
   - unshift(); **agrega un elemento al incio.**
   - shift(); **quita un elemento al inicio.**

~~~javascript
let array = [50, 53, 100, 45];

array.push(15); //agrega un elemento al final
array.pop() // quita el ultimo elemento.

array.unshift("hola"); //agrega un elemento al incio
array.shift(); //quita un elemento al inicio
console.log(array);
~~~
- Agregar y quitar elementos de un arreglo en una **posicion personalizada:**

~~~javascript
let names = ["luis", "ana", "dan", "sergio", "luchita", "concha"];
//             0       1      2       3         4          5
//splice(#indice en el que se agrgaran, #cantidad de elementos que se van a eliminar #valores que se van a aregar 1,2,3...)

names.splice(0, 0, 'Junico', 1);
console.log(names);

//Elimina el valor o valores en la poscicon descrita en este en la posicion cero vamos a eliminar 3 elementos
names.splice(0,3);
console.log(names); // ["sergio", "luchita", "concha"]

// Slice extrae en un nuevo array los valores desde [start] hasta [end -1]: No modifia el array original.
let nuevo = names.slice(1,3);
console.log(nuevo); //["ana", "dan"]
~~~
## Metodos para arreglos

**El siguiente es el arreglo que utilizaremos para ejemplos:**
~~~javascript
let arreglo = [10,42,13,34,45,];
~~~
1.- Recorrer un arreglo con **For**
~~~javascript
for (let x = 0; x < arreglo.length; x++) {
    console.log(arreglo[x]);
}
~~~
### for of
2.- Recorrer un arreglo con **for of**
~~~javascript
for (const item of arreglo) {
    console.log(item);
}
~~~
### for each
3.- **forEache()** sirve para recorrer un arreglo
~~~javascript
arreglo.forEach(elemento => {console.log(elemento);});
~~~
### some

5 **some**devuelve true en caso de que el elemento se encuentre en el arreglo
~~~javascript
console.log(arreglo.some(el => el === 45));
~~~
### filter

6 **filter()** sirve para eliminar un elemento del arreglo
~~~javascript
arreglo = arreglo.filter((del)=> del != 42)
console.log(arreglo);
~~~
### find

7 **find()** metodo para buscar un elemento dentro del arreglo
~~~javascript
elemento = arreglo.find( num => num === 10)
console.log(elemento);
~~~
### map
8 **map()** genera un nuevo arreglo para una operacion definida
~~~javascript
let  cuadrado = arreglo.map( (num) => num * num)
console.log(cuadrado);
~~~
### ordenamiento

~~~javascript
let arr = [5,6,9,8,5,1,5,8,9]

console.log(arr.sort()); //[1, 5, 5, 5, 6, 8, 8, 9, 9] ordena de menor a mayor

console.log(arr.reverse()); //[9, 9, 8, 8, 6, 5, 5, 5, 1] ordena de mayor a menor
~~~