# Atividade prática

## Atividade 1: Alunos aprovados

1. Crie uma função que recebe o array ```alunos``` e um número que irá representar a média final.
2. Percorra o array e popule e um novo array auxiliar apenas com os alunos cujas notas são maiores ou iguais à média final.
3. Utilize a técnica ``"object destruturing"`` para manipular as propriedades desejadas de cada aluno.

Projeto da atividade - [Alunos aprovados](https://github.com/CarvalhoNathan/functions/blob/main/alunosAprovados.js)

## Atividade 2: This

Dada a função ```calculaIdade```, utilize os métodos call e apply para modificar o valor de ```this```. Crie seus próprios objetos para essa atividade!
```js
function calculaIdade(anos) {
	return `Daqui a ${anos} anos, ${this.nome} terá ${
		this.idade + anos
	} anos de idade.`;
}
```
Projeto da atividade - [This](https://github.com/CarvalhoNathan/functions/blob/main/this.js)

<p align="center">
  Readme by <a href="https://github.com/CarvalhoNathan"> Nathan Carvalho </a> <br>
</p>
