+++
title = "Funciones, Closure y Callback"
chapter = true
weight = 4
pre = "<b>4. </b>"

+++

## Funciones Closure y callbacks

- La definición de una función consiste de la palabra clave (reservada) function, seguida por:
  - El **nombre** de la función (opcional).
  - Una lista de **argumentos** para la función, encerrados entre paréntesis y separados por comas (,).
  - Las **sentencias** JavaScript que definen la función, encerradas por llaves, { }.
- Ejemplo:

```javascript
function cuadrado(number) {
  return number * number;
}
```

### Funciones **declarativas** y **anónimas**

### Funciones Declarativas:

- En las funciones declarativas, utilizamos la palabra reservada **function** al inicio para poder declarar la función:

```javascript
function saludar(nombre) {
  console.log(`Hola ${nombre}`);
}

saludar("Diego");
```

### Funciones Anónimas:

- La declaración se inicia con la palabra reservada (**var, let, const**), donde se generará una variable que guardará un función anónima.

```javascript
var nombre = function (nombre) {
  console.log(`Hola ${nombre}`);
};

nombre(`Diego`);
```

#### En una funcion imprime un numero del 0 hasta el que el usuario quiere:

```javascript
var num = prompt("introduce un numero");

function cuenta(num) {
  for (var i = 1; i <= num; i++) {
    document.write(i + "\n");
  }
}
cuenta(num);
```

#### Funcion que convierte cadenas con minusculas a cadenas con mayusculas

```javascript
var nom = prompt("Ingresa tu nombre");
function NombreMayus(nom) {
  nombre = nom.toUpperCase();
  console.log(nombre);
}
NombreMayus(nom);
```

#### Funcion que calcula el cuadrado de una funcion

```javascript
function cuadrado(numero) {
  return numero * numero;
}
console.log(cuadrado(5));
```

## Closure
### Definicion:
Un closure es una **función dentro de otra funcion** que está disponible sólo dentro del cuerpo de esa fucnión y que tiene accesos a las variables de la función dónde fue declarda(funcion padre).

- sintaxis

```javascript
// funcion padre
function iniciar() {
  let name = "luis";
  // funcion hijo
  function mostrar() {
    console.log(name);
  }
  mostrar();
}
iniciar();
```
### Ámbito Léxico
Las funciones tienen su propio ámbito léxico, lo que depende de **cómo son declaradas y no de cúando se ejecutan.**

**Cómo funciona el ámbito léxico.**
El compilador de comprueba si la variable ésta declarada dentro de la función dónde se invocó y **si no** la busca en el ámbito de la funcion que la contenta y así hasta llegar al ámbito global.
```javascript
function padre() {
    let name = "Luisin"; //variable en el ámbito lexico de la funcion padre.

    function hijo() {

        function hijo2() {
            console.log("Bienvenido " + name);
        } hijo2()
    }
    hijo()
}
padre()
```
### Ejemplo de closure

Ejemplo 1: Contador

```javascript
function crearContador() {
  let contador = 0;
  return function incrementar() {
    contador = contador + 1;
    return contador;
  };
}
const result = crearContador();
```
Ejemplo 2: Suma de dos numeros.
```javascript
function fext(par1, par2, par3) {
    let variableLocal = 95;
    return function fint() {
        return `El resultado de ${par1} más ${variableLocal} es igual a: ` + (par1 + variableLocal)
    }
}
var l = fext(5, 1, 1);

console.log(l());
```
## Callback
Un callback es una **function** que se pasa a otra fucntion como un ***parametro***, y la accion a realizar la ejecute la función que recibe nuestro parametro.



- El ejemplo siguiente es una **callback** sincrónica, ya que se ejecuta inmediatamnete.
```javascript
function saludo(nombre) {
  console.log('Hola ' + nombre +' estas en la funcion 1');
}

//callback

function proceso(argumento) {
  var nombre = 'Luis';
  argumento(nombre);
}
proceso(saludo);
```
