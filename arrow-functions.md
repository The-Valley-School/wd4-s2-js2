Se trata de una forma más compacta de generar funciones y cuya sintaxis llama la atención ya que sustituimos la palabra function por =>

Ya hablaremos del objeto **this**, con lo que nos quedamos ahora es que estas funciones pueden capturar este objeto del contexto donde la arrow se ejecuta.


```jsx
// Nuestra primera función arrow
let getAge = () => {
  return 31;
};

let age = getAge();
console.log(age);

// Podemos también omitir el return y hacerlo en una línea
let getAge = () => 31;

let age = getAge();
console.log(age);

// Podríamos devolver un objeto inline
let getTeacher = () => ({name:'Edu', age:31});
console.log(getTeacher());

// Si queremos tener más sentencias dentro de la función ya nos iríamos a esto
let getAge = () => {
	let message = 'Tengo 30 años';
	return message;
};

let age = getAge();
console.log(age);
```


¿Y cómo pasamos parámetros?


```jsx
// Nuestra primera función arrow
let ageMessage = age => {
  return 'Hola, tengo ' + age;
};

console.log(ageMessage(19));

// Si pasamos varios parámetros
let getSum = (a,b) => a + b ;
let sum = getSum(3,10);
console.log(sum);
```