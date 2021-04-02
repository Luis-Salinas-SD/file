+++
title = "Condicionales"
chapter = true
weight = 2
pre = "<b>2. </b>"
+++

## Condicionales
Los condiconales funcionan de la siguiente manera:

Si la primer condicion se cumple, la siguiente no se ejecuta, pero si la primera condición no se cumple se ejecuta la segunda o la siguiente hasta que se cumpla la condicion.
### **if**

- condicion **_if_**

```javascript
if (24 === 24 || "hola" === "hola") {
  alert(true);
} else {
  alert(false);
}
//true
```
### **if-else**
- condicion **_if( ){ }else{ }_**

```javascript
let nota = 10;

if (nota <= 7) {
  console.log("malo");
} else if (nota == 8) {
  console.log("regular");
} else if (nota == 9) {
  console.log("bueno");
} else {
  console.log("Excelente");
}
```
