¡A por los condicionales!


## CONDICIONALES

Toca el turno a los condicionales. El objetivo de los mismos es ejecutar una sentencia cuando se da una condición específica y es TRUE. En caso contrario, podría ejecutarse una sentencia diferente. La estructura sería de la siguiente manera:


### **IF-ELSE-ELSE IF**

- En caso de que únicamente queramos incluir una sentencia en caso de que se cumpla una condición, usaremos **IF**


```jsx
if ( CONDICION QUE DEBE CUMPLIRSE ) {
	//SENTENCIA QUE SE EJECUTA SI SE CUMPLE UNA CONDICIÓN
}
```


- En caso de que decidamos que si se cumple una condición ejecutemos una sentencia y si no se cumple ejecutemos otra, usaremos **IF-ELSE**


```jsx
if ( CONDICION QUE DEBE CUMPLIRSE ) {
	//SENTENCIA QUE SE EJECUTA SI SE CUMPLE UNA CONDICIÓN
} else {
	//SENTENCIA QUE SE EJECUTRA SI NO SE CUMPLE UNA CONDICIÓN
}
```


- En caso de que decidamos que si se cumple una condición ejecutemos una sentencia y si no se cumple ejecutemos volvamos a hacer otra comparación, anidando **n** comparaciones,  usaremos **IF-ELSE IF**


```jsx
if ( CONDICION QUE DEBE CUMPLIRSE ) {
	//SENTENCIA QUE SE EJECUTA SI SE CUMPLE UNA CONDICIÓN
} else if (CONDICION NUEVA QUE DEBE CUMPLIRSE ){
	//SENTENCIA QUE SI NO SE CUMPLE UNA CONDICIÓN
} else {
	//CONDICIÓN SI NO SE CUMPLE NINGUNA OTRA POSIBILIDAD
}
```


Vamos ahora a realizar una serie de ejemplos que nos permitirán entender mejor los condicionales. 

- **IF:** Imaginaos que yo tengo una web en la que quiero mostrar un mensaje de ‘¡Estoy de rebajas!’ cuando sea agosto. Lo haríamos de la siguiente manera:


```jsx
let mesActual = 8; //variable dentro de mi programa con la que controlo el mes

if ( mesActual === 8 ) {
		console.log("¡Estoy de rebajas!");
}

//Estamos indicando que si la variable que determina el mes es igual a 8 (Agosto)
//nos muestre el texto.
```


- **IF-ELSE:** Otro ejemplo que podríamos usar con estos condicionales es la selección del idioma de una web. Tenemos una tienda online donde si identificamos que la persona está en España mostramos la web en español y si está fuera de España en inglés.


```jsx
let localizacion = "spain"; //variable dentro de mi programa con la que controla la localización

if ( localizacion === "spain" ) {
	console.log("El idioma de la web tiene que ser en español");
} else {
	console.log("El idioma de la web tiene que ser en inglés");
}

/*
	Estamos indicando que si la variable que determina la localización es igual 
	a "spain", pondremos la web en español, en caso contrario, será en inglés.
*/
```


- **IF-ELSE-IF:** Estas condiciones pueden anidarse. Con este ejemplo vamos a controlar si un coche puede entrar a circular en una zona de bajas emisiones de una ciudad. Para que este vehículo pueda entrar, tiene que tener etiqueta 0 o ECO y si no, tiene que estar fabricado posteriormente a 2015


```jsx
let etiqueta = "ECO";
let anoFabricacion = 2016;

if ( etiqueta === "ECO" || etiqueta === "0") {
	console.log("El coche puede circular");
} else if (anoFabricacion > 2015){
	console.log("El coche puede circular");
} else {
	console.log("El coche no puede circular");
}
```


### TERNARIO

Se puede dar el caso en que lo que queramos con estos condicionales es asignar un valor a una variable dependiendo de una condición.


```jsx
let puedeConducir;
let edad = 20;

if ( edad >= 18 ) {
	puedeConducir = true;
} else {
	puedeConducir = false;
}
```
 

Para solucionar esto de una manera más simple y sencilla (aunque las dos opciones son válidas) podemos usar un operador ternario


```jsx
/* 
 SINTAXIS:  let resultado = condición ? valor1 : valor2;
*/

let edad = 20;
let puedeConducir = (edad >= 18 ) ? true : false;

```


Se pueden concatenar todos los que queramos  pero no lo recomendamos porque no se visualiza de manera tan cómoda como un if…else


### **SWITCH**

Cuando queremos ejecutar diferentes sentencias en función de una expresión, utilizamos SWITCH. La declaración SWITCH evalúa una expresión y lo compara con las diferentes opciones definidas, ejecutando las declaraciones asociadas a estas. Sigue la siguiente estructura:


```jsx
switch (EXPRESION) {
	case VALOR1:
		//Sentencia cuando la expresión coincide con el valor 1
		break;
	case VALOR2:
		//Sentencia cuando la expresión coincide con el valor 2
		break;
	...
	case VALORN:
		//Sentencia cuando la expresión coincide con el valor n
		break;
	default;
		break;
}
```


Veamos un ejemplo. Tenemos una tienda online de ropa donde tenemos una camiseta con tallas desde la S a la XL. La M y la L están agotadas. Nos preguntan por una talla.


```jsx
let talla = "L"

switch (talla) {
	case "S":
		console.log("Perfecto, tenemos unidades de esta talla");
		break;
	case "M":
		console.log("Lo sentimos, no tenemos unidades de esta talla");
		break;
	case "L":
		console.log("Lo sentimos, no tenemos unidades de esta talla");
		break;
	case "XL":
		console.log("Perfecto, tenemos unidades de esta talla");
		break;
	default;
		console.log("Lo sentimos, solo trabajamos con tallas desde la S a la XL");
		break;
}
```