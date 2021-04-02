+++
title = "arrow-function"
chapter = true
weight = 5
pre = "<b>5. </b>"
+++
## Funcion flecha

Una expresión de **función flecha** es una alternativa compacta a una expresión de función tradicional, **pero es limitada y no se puede utilizar en todas las situaciones.**

- **Arrow-function**

La sintaxis básica de una _**arrow-function**_ es la siguiente:
~~~javascript
name_function = (parametros) => {cuerpo_funcion}
~~~
~~~javascript
suma = (a, b) => a + b //arrow-function

console.log(suma(5, 5)); //10
~~~

### Ejemplos:
1.- imprimir los numeros en pantalla hasta el numero que el usuario teclea
~~~javascript
var n = prompt("introduce el numero:");

cuenta = (n) => {
    for (i = 0; i <= n; i++) {
        document.writeln(i);
    }//for
}//arrow-function cuenta
cuenta(n);
~~~
2.- Aqui hay un objeto llamdo **tutor** y dentro de sus propiedades se encunetra una funcion, que lo que hace es imprimir el nombre con ayuda del metodo **setTimeout** despues de cierto tiempo. 

La propiedad que contiene esta funcion es **fullNombre.**
~~~javascript
let tutor = {
    nombre: "Luis",
    apellido: "Salinas",
    fullNombre: function () {
        setTimeout(() => { console.log(this.nombre + " " + this.apellido); }, 1000)
    }
}
// console.log(tutor.apellido);
tutor.fullNombre();
~~~