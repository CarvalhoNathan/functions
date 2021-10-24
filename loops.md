# Aula 3: Loops

Como utilizar algumas das mais famosas declarações do Javascript

## If/Else
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
