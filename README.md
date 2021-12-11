# Javascript Fundamentos
Neste readme temos um resumo das variáveis primitivas encontradas no Javascript, bem como seus principais métodos.
<a href="https://www.linkedin.com/in/anderson-liege-67b38b98/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   

## Variáveis
Os tipos de variáveis no Javascript podem ser divididas em duas categorias:
primitivas e objetos. 
Os tipos primitivos são:

- Number
- String
- Boolean
- Symbol
- Null
- Undefined

Os demais tipos de variáveis em Javascript são um objeto. 
Um objeto é uma coleção de propriedades onde cada propriedade
possui um nome e um valor. 

 ### Numbers ###
Existem dois tipos de dados no Javascript para 
representação de um número:

- Inteiros
- Float (ponto flutuante)

 #### Inteiros ####
No Javascript, um inteiro de base 10 é escrito como uma 
sequência de dígitos, por exemplo:


## Variáveis
Os tipos de variáveis no Javascript podem ser divididas em duas categorias:
primitivas e objetos. 
Os tipos primitivos são:

- Number
- String
- Boolean
- Symbol
- Null
- Undefined

Os demais tipos de variáveis em Javascript são um objeto. 
Um objeto é uma coleção de propriedades onde cada propriedade
possui um nome e um valor. 

 ### Numbers ###
Existem dois tipos de dados no Javascript para 
representação de um número:

- Inteiros
- Float (ponto flutuante)

 #### Inteiros ####
No Javascript, um inteiro de base 10 é escrito como uma 
sequência de dígitos, por exemplo:

```javascript
0
10
33
```
Também podemos ter a representação de um número 
em base hexadecimal. Para isso é necessário começarmos
sua declaração com 0x ou 0X seguido pela string que representa
aquele número, exemplo:

```javascript
0xff // valor em inteiro decimal = 255
0xAA // valor em inteiro decimal = 170 
0xAB // valor em inteiro decimal = 171 
```
Após a ES6, podemos também ter a representação em base binária (base 2) ou octal (base 8),
usando os prefixos 0b e 0o (ou 0B e 0O):
```javascript
0b1010 // valor em inteiro decimal = 10
0o377  // valor em inteiro decimal = 255
```

 #### Float ####
 Números ditos do tipo float, são aqueles que possuem casas decimais.
 Eles são a representação de um número real na matemática. Exemplo:
```javascript
2.33
3.14
.345
```
 #### Aritmética no Javascript ####
 Os operadores matemáticos encontrados no Javascript são:
```javascript
+   // soma
-   // subtração
*   // multiplicação
/   // divisão
%   // módulo da divisão
**  // exponenciação 
```
Além desses operadores matemáticos usuais, o Javascript
suporta mais operações complexas através de um set de funções e 
constantes definidas como propriedades do objeto Math. Exemplo:

```javascript
Math.pow(2,53) // => 9007199254740992: 2 elevado a 53
Math.round(.6) // => 1.0: arredonda para o inteiro mais próximo
Math.ceil(.6) // => 1.0: arredendo para o inteiro mais próximo que está acima desse valor
Math.floor(.6) // => 0.0: arredendo para o inteiro mais próximo que está abaixo desse valor
Math.abs(-5) // => 5: retorna o valor absoluto passado 
Math.max(x,y,z) // retorna o argumento de maior valor
Math.min(x,y,z) // retorna o argumento de menor valor
Math.random() // seudo-random number x onde 0 <= x < 1.0
Math.PI //  o valor de pi
Math.E // e: base do logaritmo natural
Math.sqrt(3) // => 3**0.5: raiz quadrada
Math.pow(3, 1/3) // => 3**(1/3): raiz cúbica
Math.sin(0) // trigonometria: seno de 0,  também temos Math.cos, Math.atan, etc.
Math.log(10) //logaritmo natural de 10
Math.log(100)/Math.LN10 // logaritmo de 100 na base 10
```

### String ###
O tipo de dado que representa um texto em Javascript é a string. Para incluir uma string em seu 
código Javascript, basta por os caracteres entre aspas simples ou duplas, exemplo:
```javascript 
"" // string vazia
'pode ser assim também' // com aspas simples
var = 'hello world' // declarando uma variável com valor string
```
As strings no Javascript assim como os numbers também possuem algumas funções nativas, a seguir pode-se analisar algumas delas:
 ```javascript
let s = "Hello, world"; // iniciando a variável com algum texto

/* Os métodos que podemos utilizar em uma string */

// Obtendo partes de uma string
s.substring(1,4) // => "ell": index [1] até [4], onde o [4] não é incluído  
s.slice(1,4) // => "ell": possui o mesmo efeito do método anterior
s.slice(-3) // => "rld": coletando os últimos 3 caractéres 
s.split(", ") // => ["Hello", "world"]: separa a string com o argumento passado, removendo o argumento 

// Procurando na string 
s.indexOf("l") // => 2: posição da primeira letra l
s.indexOf("l", 3) // => 3: posição do primeiro "l" após o index [3] ou no index[3] 
s.indexOf("zz") // => -1: s não possui a string "zz"
s.lastIndexOf("l") // => 10: posição da última letra l

// Métodos que retornam um valor booleano (true ou false)
s.startsWith("Hell") // => true: a string começa com o argumento passado?
s.endsWith("!") // => false: s termina com "!"?
s.includes("or") // => true: s possui a substrgin "or"?

// Criando versões modificadas da string
s.replace("llo", "ya") // => "Heya, world"
s.toLowerCase() // => "hello, world"
s.toUpperCase() // => "HELLO, WORLD"
s.normalize() // Unicode NFC normalização: ES6
s.normalize("NFD") // NFD normalização. Também temos "NFKC", "NFKD"

// Inspecionando caracteres individuais da string de 16-bits
s.charAt(0) // => "H": primeiro caractere
s.charAt(s.length-1) // => "d": último caractere
s.charCodeAt(0) // => 72: representação da string em inteiro de 16-bits (UTF-16)
s.codePointAt(0) // => 72: ES6, valor do ponto de código inteiro > 16 bits

// Adicionando padding as strings - ES2017
"x".padStart(3) // => " x": adciona 3 espaços a esquerda da string
"x".padEnd(3) // => "x ": adciona 3 espaços a direita da string
"x".padStart(3, "*") // => "**x": adciona asterisco a esquerda com 3 de espaçamento
"x".padEnd(3, "-") // => "x--": adiciona hífens a direita com espaçamento de 3 

// Funções de trim (remoção). trim() is ES5; 
" test ".trim() // => "test": remove espaços no inicio e final da string
" test ".trimStart() // => "test ": remove espaços a esquerda. Pode-se usar também trimLeft
" test ".trimEnd() // => " test": remove a direita. Pode-se usar também trimRight

// Outros métodos 
s.concat("!") // => "Hello, world!": Pode-se usar o operador + 
"<>".repeat(5) // => "<><><><><>": concatena n cópias. ES6

```

**Lembre-se que strings são imutáveis no Javascript. Métodos como replace() e toUpperCase() retornam novas
strings, eles não modificam a string que está sendo passada como argumento.** 

As strings também podem ser tratadas como arrays de apenas leitura, pode-se acessar individalmente cada 
caractere usando [index], exemplo:

```javascript 
let s = "hello, world";
s[0] // => "h"
s[s.length-1] // => "d"
```

### Boolean ###
Uma variável booleana possui apenas dois valores possíveis, verdadeiro (true) ou falso (false). 
Valores booleanos geralmente são resultados de comparação que fazemos no programa, exeplo:

```javascript 
a === 4
```
Esse código checa se a variável **a** é igual a 4, se sim, o resultado retornado é igual a **true**, se não,
o resultado retornado é igual a **false**.

### Symbols ###
Symbols foram introduzidos na ES6 para servir como nomes de propriedades não string. Para entender melhor
Symbols, você precisa saber que os tipos de objetos fundamentais no javascript são uma coleção de 
propriedades não ordenadas, onde cada propriedade possui um nome e um valor. Nomes de propriedade são
tipicamente strings. Porém na ES6 e posteriores, Symbols também podem servir a esse propósito. 

### Null e Undefined ###
O tipo de dado null é uma palavra reservada do Javascript utilizada para indicar que aquela variável
não possui nenhum valor, seu valor é nulo. O undefined também indica a ausência de valor, porém 
em um nível mais profundo. É quando não iniciamos uma variável sem valor por exemplo.

```javascript 
let strname = "string name"; // string sendo utilizada como propriedade de um nome
let symname = Symbol("propname"); // symbol sendo utilizado como propriedade de um nome
typeof strname // => "string": strname é uma string
typeof symname // => "symbol": symname é um  symbol
let o = {}; // criando um objeto vazio 
o[strname] = 1; // definindo a propriedade do objeto de chave 1 com a string
o[symname] = 2; // definindo a propriedade do objeto de chave 2 com o symbol
o[strname] // => 1: acessando a propriedade string name
o[symname] // => 2: acessando a propriedade symbol name
console.log(o) 
// saída do console.log(o)
{string name: 1, Symbol(propname): 2}
string name: 1
Symbol(propname): 2
[[Prototype]]: Object
//
```
