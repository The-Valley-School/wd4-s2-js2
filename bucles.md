## BUCLES

A la hora de trabajar en JS, muchas veces nos encontraremos ante la necesidad de realizar tareas repetitivas. Para optimizar este proceso podemos hacer uso de los bucles que nos permiten de una manera rápida, realizar una tarea **n** veces, pudiendo ejecutar un trozo de código tantas veces como queramos sin tener que duplicar o triplicar esas lineas.


### **BUCLE FOR**

El bucle FOR nos va a permitir repetir un trozo de código el número de veces que le digamos.

La sintaxis para trabajar con bucles FOR es la siguiente


```jsx
for ( EXPRESION INICIAL; CONDICION; EXPRESION FINAL){
	//Sentencia que se repite 
}
```


- Expresión inicial:  Expresión o declaración de variable. Suele ser para inicializar un contador.
- Condición: Expresión que usamos para la continuidad del bucle, mientras sea verdadera sigo iterando
- Expresión final: Expresión evaluada tras cada iteración. Suelen ser incrementos o decrementos.

Posiblemente todavía te suene a chino, pero con un ejemplo seguro que lo entendemos mejor. Vamos a imprimir por consola los números del 1 al 10.


```jsx
for (let i = 0; i <= 10; i++){
	 console.log(i);
} 
```


Analizamos detalladamente:

- Nuestra expresión inicial es **let i = 0** , estamos declarando una variable **i**  que vale 0
- Con la condición **i ≤ 10** indicamos que vamos a ejecutar el bucle hasta que la variable **i** valga 10. Cada vez que se itere en el bucle se validará esta condición
- La expresión final **i++** nos indica que cuando se termine una iteración se le añadirá un +1 a nuestra variable **i.**
- El bucle terminará cuando **i** sea mayor que 10, según la condición propuesta.

Si quisiésemos contar hacia atrás podríamos hacerlo:


```jsx
for (let i = 10; i >= 0; i--){
	 console.log(i);
} 
```


En este caso, iríamos reduciendo la variable **i** que utilizamos como índice para contar hacia atrás.

Al poner en la expresión final **i—** estamos indicamos que estamos reduciendo 1 en cada iteración al valor de **i.**

Vamos a realizar otro ejemplo para seguir trabajando con los bucles FOR. En esta ocasión vamos a crear la tabla de multiplicar del 7 y mostrar los resultados por pantalla.


```jsx
for (let i = 0; i <= 10; i++){
	 console.log(7 * i);
} 
```


Estamos recorriendo el bucle 11 veces, desde que **i = 0,** hasta que **i = 10**. En cada iteración estamos multiplicando el 7 y aprovechando el valor de **i** para ir haciendo la tabla de multiplicar.

Por último, vamos a hacer un ejercicio con textos. La propiedad **.length** nos devuelve el número total de caracteres dentro de un string, así que vamos a recorrer uno y lanzar por consola cada una de las letras. Para conseguir un caracter específico de una cadena de texto debemos de seleccionar la variable junto con el índice del caracter que queremos de tal forma → **texto[i]**


```jsx
let palabra = "Pepito";
let primeraLetraPalabra = palabra[0] 
console.log(primeraLetraPalabra) // Pinta la letra P, en programación se empieza a contar desde el 0
```


Sabiendo como seleccionar un caracter vamos a proceder a realizar la iteración 


```jsx
let palabra = "Pepito";

for (let i = 0; i <= palabra.length; i++){
	 console.log(palabra[i]);
} 
```


### FOREACH

El bucle foreach te permite recorrer ciertas estructuras de elementos sin tener que preocuparte por el número de elementos que tenga.


```jsx
let futuramaList = ['Blender', 'Fry', 'Leela', 'Zoiberg'];

futuramaList.forEach(
	function(element){
		console.log(element);	
	}
);
```
 

### FOR…OF

Un bucle con contador internos que nos va dando el valor actual


```jsx
let futuramaList = ['Blender', 'Fry', 'Leela', 'Zoiberg'];

for ( let element of futuramaList){
	console.log(element);
}
```


La diferencia principal con el forEach es que el for…of nos permite recorrer varios tipos de elementos iterables mientras que el forEach está pensado para arrays


### FOR…IN

For…in nos da la posiblidad de recorrer todos los índices de un objeto, de esta manera tendremos la propiedad inmutable


```jsx
//Ejemplo con objeto
let naveFuturama = {
	conductor: 'Leela',
	color: verde,
	combustible: diesel
}

for (let clave in naveFuturama){
	console.log("La nave de futurama tiene la clave " + clave + " y el valor " + naveFuturama[clave]);
}

//Ejemplo con array
let futuramaList = ['Blender', 'Fry', 'Leela', 'Zoiberg'];

for ( let clave in futuramaList){
	console.log("Este personaje de futurama tiene la posición " + clave + " y el valor " + naveFuturama[clave]);
}
```


La diferencia es que le for…of solo puede funcionar con objetos iterables.

### **BUCLE WHILE**

El bucle WHILE nos permite iterar un trozo de código mientras se cumpla una condición. 

La sintaxis es la siguiente:


```jsx
while (CONDICION) {
	// sentencia que se repite
}
```


El bucle WHILE se seguirá repitiendo mientras se cumpla la condición. Esta condición se evalúa al iniciar cada iteración. Vamos a ver un ejemplo:


```jsx
let n = 0;

while (n <= 3){
    console.log ("La variable n vale: " + n );
    n++;
}
```


En cada iteración vamos aumentando el valor de n. El bucle se repetirá hasta que n valga 3.


### **BUCLE DO…WHILE**

El bucle DO..WHILE nos permite también iterar un trozo de código mientras se cumpla una condición. La diferencia con el bucle WHILE es que la comprobación se realiza al finalizar la iteración por lo que como mínimo siempre va a pasar una vez por el bucle. La sintaxis es la siguiente:


```jsx
do {
   //sentencia que se repite
} while(CONDICION);
```


En cada iteración vamos aumentando el valor de a, al igual que en el WHILE, hasta que se cumpla la condición para salir del bucle.


```jsx
let a = 0;

do {
    console.log ("La variable a vale: " + a );
    a++;
} while (a <= 3);
```