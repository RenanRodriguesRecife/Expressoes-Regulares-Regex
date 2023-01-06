# Expressões Regulares (Regex) 

O que é uma Expressão Regular?
Uma expressão regular, ou Regex, são padrões utilizados para identificar determinadas combinações ou cadeias de caracteres em uma string. Ela faz parte do dia a dia de todos os programadores e administradores de infra. Por meio dela, podemos validar a entrada de usuários ou encontrar alguma informação em logs, documentação ou saída de comando. O mais legal é que as Regex são escritas independentes de uma linguagem de programação.

Site usado para fazer teste de Expressões Regulares:
https://regexr.com/

1 - toda expressão regular fica entre duas barras:
```
/expressão regular/
```

### Opções de Execução - Flags

2 - Flags são as letras que ficam no final da expressão regular EX:
```
/expressão regular/g
```
g - (global): Diz que ele vai selecionar todas as ocorrencias que encontrar não só a primeira.

i - (case insensitive): Não vai fazer distinsão entre maiúsculo e minúsculo

m - (multiline): modifica o significado de ^ e $, assim ele executa associandoo inicio e fim, respectivamente, de alguma linha

### Teste de Expressão regular (java script)

- Tem duas formas: Usando uma string para testar um expressão e usando uma expressão para testar uma string.

Usando o texto para testar a expressão regular:
```javascript

let text = 'este é um texto';
let regex = /texto/g;

let results = text.match(regex);
console.log(results);
```

usando uma expressão para testar uma string.
```javascript

let text = 'este é um texto';
let regex = /texto/g;

let results = regex.exec(text);
console.log(results);

//ou

let results = regex.test(text);
console.log(results);
```

### sintaxe

. - qualquar caractere exceto o '\n'

<img src="01.JPG">

Quando você coloca um acaracter mais um ponto: Ele vai selecioar apenas o que tem o caractere seguido de qualquer outra letra.

<img src="02.JPG">

| (ou) ou ele vai pegar um elemento ou outro

Ex: Você quer selecionar um "e" ou "é"

<img src="03.JPG">

agrupamento: Você usa o () para formar um grupo

<img src="04.JPG">

padrão: é usado []. ele pega cada caractere individulmente (ele não pega sequencialmente).

<img src="05.JPG">

Repare que ele não pega a palavra texto e sim cada caractere individual

Isso é muito usado para uma sequencia de caracteres:

Ex: 
- Pegar todas as letras de "a" a "e"

```
/[a-e]/g
```

<img src="06.JPG">

- Pegar todas as letras de "a" a "z"

```
/[a-z]/g
```

<img src="07.JPG">

- Pegar todos os algarismos de 0 a 9

```
/[0-9]/g
```

<img src="08.JPG">

^ (negar) - significa que vai pegar todos os elementos **menos** os caracteres destacados

<img src="09.JPG">

note que ele pegou todos os caracteres menos o "e" eo "t"

22:20

https://www.youtube.com/watch?v=tlVI8mV1dQY

