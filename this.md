
# Aula 3: This

- [This](#this)
- [Manipulando seu valor](#manipulando-seu-valor)
- [Apply](#apply)
- [Bind](#bind)

## This

Apresentar a palavra "this" e seus uso e como aplicar métodos para manipular seu valor

### This
O que é

A palavra reservada **this** é uma referência de contexto. Como exemplo, this refere-se ao objeto pessoa. Seu valor pode mudar de acordo com o lugar no código onde foi chamada.

```js
const pessoa = {
 firstName: "Nathan",
 lastName: "Carvalho",
 id : 1,
 fullName : function(){
  return this.firstName + " " + this.lastName;
 },
 getId: function() {
  return this.id;
 }
};

pessoa.fullName();
// "Nathan Carvalho"

pessoa.getId();
// 1
```
| Contexto | Referência |
|--|--|
| Em um objeto (método) | Próprio objeto dono do método |
| Sozinha | Objeto global (em navegadores, window) |
| Função | Objeto global |
| Evento | Elemento que recebeu o evento |

## Manipulando seu valor

### Call
```js
const pessoa = {
 nome: 'Nathan',
};

const animal = {
 nome: 'Hercules',
};

function getSomething() {
 console.log(this.nome);
}

getSomething.call(pessoa);

// Nathan
````
Outro exemplo do this call:
```js
const pessoa = {
 nome: 'Nathan',
};

const animal = {
 nome: 'Hercules',
};

function getSomething() {
 console.log(this.nome);
}

getSomething.call(animal);

// Hercules
```
```js
const myObj = {
 num1: 2,
 num2: 4,
};

function soma(a, b) {
 console.log(this.num1 + this.num2 + a + b);
}

soma.call(myObj, 1, 5);
// 12
```

É possível passar parâmetros para essa função seperando-os por vírgulas.

## Apply
```js
const pessoa = {
 nome: 'Nathan',
};

const animal = {
 nome: 'Hercules',
};

function getSomething() {
 console.log(this.nome);
}

getSomething.apply(pessoa);

// Nathan
```
```js
const myObj = {
 num1: 2,
 num2: 4,
};

function soma(a, b) {
 console.log(this.num1 + this.num2 + a + b);
}

soma.call(myObj, [1, 5]);
// 12
```

É possível passar parâmetros para essa função dentro um array.

## Bind

O Bind, clona a estrutura da função onde é chamada e aplica o valor do objeto passado como parâmetro.

```js
const retornaNome = function () {
 return this.nome;
};

let nathan = retornaNomes.bind({ nome: 'Nathan" });

nathan();

// Nathan
```
