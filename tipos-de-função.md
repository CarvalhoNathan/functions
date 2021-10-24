# Aula 1 - Tipos de função:

Apresentar a estrutura de uma função, e alguns outros tipos de funções e como são utilizadas.

## Estrutura (Definição comum de uma função):
```js
function nome(parametros) {
 // instruções
}
```
Variáveis criadas dentro de uma função, podem ser utilizadas apenas dento dela.
```js
function nome(parametros) {
 // instruções
 return; // valor de retorno
}
```
Quando invocamos o "return", a função para de ser executada.

### Função anônima (Funções que representam expressões):
```js
const soma = function (a, b) {
 return a + b;
}

soma(1, 2) // retorna 3
soma(5, 4) // retorna 9
```
Uma variável pode armazenar uma função.

### Função autoinvocável (IIFE  - Immediately Invoked Function Expression):
```js
(
 function() {
  let name = "Digital Innovation One"
  return name;
 }
)();

// Digital Innovation One
```
Uma função anônima entre parênteses, seguida por outro par de parênteses, que representa sua chamada.
```js
(
 function(a, b) {
  return a + b;
 }
)(1, 2);

//

const soma3 = (
 function() {
  return a + b;
 }
)(1, 2);

console.log(soma3) // 3
```
Também pode ser utilizada com parâmetros ou armazenada em uma variável

### Callbacks (Uma função passada como argumento para outro):

```js
const calc = function(operacao, num1, num2){
 return operacao(num1, num2);
}

const soma = function(num1, num2){
 return num1 + num2;
}

const sub = function(num1, num2){
 return num1 - num2;
}

const resultSoma = calc(soma, 1,2);
const resultSub = calc(sub, 1,2);

console.log(resultSub); // -1
console.log(resultSoma); // 3
```

Utilizando callbacks, você tem maior controle da ordem de chamadas.
