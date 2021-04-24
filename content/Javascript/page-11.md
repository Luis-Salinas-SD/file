+++
title = "Promesas"
chapter = true
weight = 11
pre = "<b>11. </b>"

+++

## Promesas

Las **promesas** en Javascript son utilizadas en Javascript para gestionar el codigo asíncrono.

### Sincrono
La instrucción se ejecutrá en secuencia hasta terminar.

### Asíncrono
Puede que algunas instrucciones se ejecuten a destiempo.

## Estados de una promesa.

Las promesas tienen 3 estados.

- se cumple (fulfilled).
- no se cumple (rejected).
- pendiente (pending).

## Estructura
Una promesa recibe como parametro **una función con 2 parametros**(*resolve,reject*).

```javascript
var myPromise = new Promise(
    (resolve,reject)=>{
    if(/* condicion */) {
   		resolve('Success!');
 	} else {
   		 reject('Failure!');
 	}
    }
)//promesa

//Mandar a llamarla.
myPromise.then(function){
    //hacer algo en el resolve.
}.catch(fucntion(){
	//hacer algo en el reject.     
})
```

### Metodos

Las promesas en Javascript se representan a traves de un `object` y se pueden utilizar los siguientes metodos.

| Método                                       | Descripción                                                  |
| -------------------------------------------- | ------------------------------------------------------------ |
| .then(`function` resolve)                    | Ejecuta la función callback `resolve` cuando la promesa se cumple. |
| .catch(`function` reject)                    | Ejecuta la función callback `reject` cuando la promesa se rechaza. |
| .catch(`function` resolve `function` reject) | Método equivalente a las dos anteriores en el mismo `.then()`. |
| .finally(`function` end)                     | Ejecuta la función callback `end` tanto si se cumple como si se rechaza. |

*Podemos encontrar más informacion en la siguiente liga:*

- [Javascript - promises](https://lenguajejs.com/javascript/asincronia/promesas/)