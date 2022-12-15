Vamos a ver ahora una serie de conceptos que nos van a ser gran ayuda ahora que ya empezamos a conocer como funciona Javasicript.

- Scope
- Var, let, const
- Hoisting
- This
- Clousure


### SCOPE

Cuando hablamos de SCOPE hablamos del alcance que tendrá una variable en el código, es decir, a qué variables tienes acceso en cada parte de tu código.

Este alcance puede ser global o local

- Global: Una variable que puede ser accesible desde cualquier parte del código.
- Local: Esta función solo es accesible desde la parte de código que la contiene


```jsx
// DECLARACIÓN GLOBAL

let singer = 'Maluma';

function showSinger() {
 console.log('in function ' + singer);
}

showSinger();
console.log('out function ' + singer);

// DECLARACIÓN LOCAL
// Función
function showSinger() {
 let singer = 'Maluma';
 console.log('in function ' + singer);
}

showSingerlobal();
console.log('out function ' + singer); //error

```


### VAR, LET y CONST

**Var** y **let** ya las hemos visto, **const** hace referencia a una variable cuyo valor se asigna al inicializar esa variable y ya no se cambia, como si fuese una constante.

Var y let se diferencian en el scope de actuación de dichas variables


### HOISTING

¿Qué mostrará este código?


```jsx
let x = 'global value';
function foo() {
	console.log(x); 
	// undefined 
	let x = 'local value';
	console.log(x); 
	// local value
} 
foo();
```


Seguramente pensemos que primero ‘global value’ y luego ‘local value’, pero no es así. El hoisting es algo a tener en cuenta a la hora de desarrollar y así evitar errores..

Javascript interpreta el código de esta manera, de ahí que la solución sea ‘undefined’ y ‘local value’. Sube a las primeras posiciones del scope donde actúa la declaración de la variable, lo que permite en cierto punto utilizar variables antes de definirlas.


```jsx
let x;
x = 'global value';
function foo() {
	let x;
  console.log(x); 
	x = 'local value';
	console.log(x); 
} 
foo();
```


### THIS

**This** es una palabra reservada y que sirve como  herramienta que nos permite referenciar un objeto desde una función, es decir, acceder a los valores y propiedades de dicho objeto.

Esta referencia se crea cuando una función es invocada, no declarada. Tenemos que tener lozalizado el lugar de invocación para tener claro como se comporta this. 


### CLOUSURE

Una clousure permite acceder al ámbito de una función exterior desde una función interior.

Vamos a ver el funcionamiento


```jsx
let a = 'Hola'
function global(){
	let b = ' Don ';
	function local(){
		let c = 'Pepito';
		return a+b+c;
	}
	return local;
}

//para llamar a esta función
global ()();

//para llamar a esta última sentencia hacemos esto
let clousure = global();
clousure();
```

 