# Aula 5: Arrow functions

## Sintaxe
```js
const helloWorld = function(){
 return "Hello World";
}
```
```js
const helloWorld = () => {
 return "Hello World";
}
```
```js
const helloWorld = () => "Hello World";
```
```js
const soma = (a, b) => a + b;

soma(4, 6);
// 10
```
```js
const soma = a => a;

soma(4);
// 4
```

Caso exista apenas uma linha, pode dispensar as chaves e o return.
E caso exista apenas um parâmetro, pode dispensar os parênteses.

Correto ✔
```js
soma(2, 4);

function soma(a, b) {
 return a + b;
}
```
Errado ❌
```js
soma(2, 4)

const soma = (a, b) => a + b;
```

Arrow function **NÃO** faz hoisting!

## Outras restrições

- ```this``` sempre será o objeto global. Métodos para modificar seu valor não irão funcionar (Como call, bind ou apply).
- Não existe o objeto ```arguments```;
- O construtur (Ex: ```new MeuObjeto()```) também não pode ser utilizado.
