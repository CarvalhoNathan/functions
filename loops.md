# Aula 3: Loops

Nessa aula foi ensinado como utilizar algumas das mais famosas declarações do Javascript.

- [If Else](#if-else)
- [Switch](#switch)
- [For](#for)
- [While](#while)
- [DoWhile](#dowhile)

## If Else
```js
function numeroPositivo(num) {
 let resultado;

 if(num < 0) { // Condição, se num for menor que 0
  resultado = false; // Declaração 1 (dentro de if): Ocorre caso a condição seja verdadeira
 } else {
  resultado = true; // Declaração 2(dentro do else): Ocorre caso a condição seja falsa
 }

 return resultado;
}

numeroPositivo(2)
// true

numeroPositivo(-9)
// false
```

Outro exemplos de **If/else**
```js
function numeroPositivo(num) {
 let resultado;

 const ehNegativo = num < 0;

 if(ehNegativo) {
  resultado = false;
 } else {
   resultado = true;
 }

 return resultado;
}
```
```js
function numeroPositivo(num) {
 const ehNegativo = num < 0;
 
 if(ehNegativo) {
  return false;
 }

 return true;
}
```
```js
function numeroPositivo(num) {
 const ehNegativo = num < 0;
 const maiorQueDez =num > 10;

 if(ehNegativo) {
  return "Esse número é negativo!";
 } else if (!ehNegativo && maiorQueDez) {
   return "Esse número é positivo e maior que 10!"
 }

 return "Esse número é positivo!";
}
```

## Switch

### Switch/case

- Equivale a uma comparação de tipo e valor (===) 
- Sempre precisa de um valor "default"
- Ideal para quando se precisa comparar muitos valores
```js
function getAnimal(id) {
 switch(id) {
  case 1:
   return "cão";
  case 2:
   return: "gato";
  case 3:
   return: "pássaro";
  default:
   return: "peixe";
 }
}

getAnimal(1) // cão
getAnimal(4) // peixe
getAnimal("1") // peixe
```

## For

Loops dentro de elementos iteráveis (arrays, strings).
```js
function multiplicaPorDois(arr) {
 let multiplicados = [];
 
 for(let i = 0; i < arr.length; i++) {
  multiplicados.push(arr[i] * 2);
 }

 return multiplicados;
}

const meusNumeros = [2, 33, 456, 356, 40];

multiplicadosPorDois(meusNumeros);
// [4, 66, 912, 712, 80]
```

## For... in

Loop entre propriedades enumeráveis de um objeto.
```js
function forInExemplo(obj) {
 for(prop in obj) {
  console.log(prop);
 }
}

const meuObjeto = {
 nome: "Nathan",
 idade: "19",
 cidade: "São Paulo"
}

forInExemplo(meuObjeto);
// nome
// idade
// cidade
```
Outro exemplo de for in:
```js
function forInExemplo(obj) {
 for(prop in obj) {
  console.log(obj[prop]);
 }
}

const meuObjeto = {
 nome: "Nathan",
 idade: "19",
 cidade: "São Paulo"
}

forInExemplo(meuObjeto);
// Nathan
// 19
// São Paulo
```
## For...of

Loop entre estruturas iteráveis (arrays, strings).
```js
function logLetras(palavra) {
 for(letra of palavra) {
  console.log(letra);
 }
}

const palavra = "abacaxi";

logLetras(palavra)
// a
// b
// a
// c
// a
// x
// i
```
```js
function logNumeros(nums) {
 for(letra of nums) {
  console.log(num);
 }
}

const nums = [30, 20, 233, 2];

logLetras(nums)
// 30
// 20
// 233
// 2
```

## While e do...while

### While
```js
function exemploWhile() {
 let num = 0
 
 while(num <= 5){
  console.log(num);
  num++;
  }
}

exemploWhile()
// 0
// 1
// 2
// 3
// 4
// 5
```
Executa instruções até que a condição se torne falsa.

## Do...while
```js
function exemploDoWhile() {
 let num = 0;

 do {
  console.log(num);
  num++;
 } while(num <= 5)
}

exemploDoWhile()
// 0
// 1
// 2
// 3
// 4
// 5
```
Outro exemplo de DoWhile:
```js
function exemploDoWhile() {
 let num = 6;
 
 do {
  console.log(num);
  num++;
 } while(num <= 5)
}

exemploDoWhile()
// 6
```

Ele executa instruções até que a condição se torne falsa, porém a primeira execução sempre ocorre.

<p align="center">
  Readme by <a href="https://github.com/CarvalhoNathan"> Nathan Carvalho </a> <br>
</p>
