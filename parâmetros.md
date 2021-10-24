# Aula 2: Parâmetros

Como manipular parâmetros de uma função, e técnicas para lidar com números indefinidos de parâmetros.

## Valores padrão:

Pré-ES2015: ⬇
```js
function exponencial(array, num) {
 if (num === undefined) {
  num = 1;
 }

 const result = [];
 
 for(let i = 0; i < array.lenght; i++) {
  result.push(array[i] ** num);
 }

 return result;
}

exponencial([1, 2, 3, 4])
// [1, 2, 3, 4]

exponencial([1, 2, 3, 4], 4)
// [1, 8, 27,64]
```
Pós-ES2015: ⬇
```js
function exponencial(array, num = 1) {
 const result = [];
 
 for(let i = 0; i < array.lenght; i++) {
  result.push(array[i] ** num);
 }

 return result;
}

exponencial([1, 2, 3, 4])
// [1, 2, 3, 4]

exponencial([1, 2, 3, 4], 4)
// [1, 8, 27,64]
```

### Objeto "arguments":

```js
function findMax() {
 let max = -Infinity;
 
 for(let i = 0; i < arguments.length; i++) {
  if (arguments[i] > max) {
   max = arguments[i];
  }

  return max;
}
```
Um array com todos os parâmetros passados quando a função for invocada.
```js
function showArgs() {
 return arguments;
}
```
# Arrays e objetos:
## Arrays ⬇

### Spread: É uma forma de lidar separadamente com elementos
```js
function sum(x, y, z) {
 return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
````

O que era parte de um array se torna um elemento independente.

### Rest: Combina os argumentos em um array
```js
function confereTamanho(...args) {
 console.log(args.length)
}

confereTamanho() // 0
confereTamanho(1, 2) // 2
confereTamanho(3, 4, 5) // 3
```

O que era um elemento independente se torna parte de um array.

## Objetos ⬇

### Object Destructuring:

```js
const user = {
 id: 19,
 displayName: 'NCarv',
 fullName: {
  firstName: 'Nathan'
  lastName: 'Carvalho'
 }
};

function userId({id}) {
 return id;
}

function getFullName({fullName: {firstName: first, lastName: last}}) {
 return `${first} ${last}`;
}

userId(user)
// 19

getFullName(user)
// Nathan Carvalho
```

Entre chaves {} podemos filtrar apenas os dados que nos interessam em um objeto.

<p align="center">
  Readme by <a href="https://github.com/CarvalhoNathan"> Nathan Carvalho </a> <br>
</p>

