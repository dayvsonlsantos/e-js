# Operações

- Adição (+)
- Substração (-)
- Multiplicação (*)
- Divisão (/)
- Módulo (%)
- Incremento (++)
- Descremento (--)

# Strings -> Number

- parseInt(variável)
- parseFloat(variável)

# Alert | Prompt

- alert: Para exibir mensagens;
- prompt: Solicita uma informação ao usuário; 

# Operador Ternário

- verificação ? ação : ação

# Array

- Forma 01 -> var vetor = new Array();

- Forma 02 -> var vetor = [];

# Função Anônima

```
  var media = function (n1, n2){
    return (n1+n2)/2;
  }
```

# Arrow Function

```
  var media = (n1, n2) => {
    return (n1+n2)/2;
  }
```

# Objeto

```
  var aluno = {
    nome: "João",
    notas: [7.5, 5.0]
  }

  outra forma: var aluno = new Object();

  console.log(aluno.notas[1])
  console.log(aluno["notas"][1])

  Esse segundo formato é interessante, quando pensamos na seguinte situação:

  var novaProp = "Lastname"

  aluno[novaProp] = "Oliveira"

  Assim, é possível tornar mais dinâmico a criação de novas propriedades.
```

## Métodos


```
  var aluno = {
    nome: "João",
    notas: [7.5, 5.0]
    
    media: function(n1, n2) {
      return (n1+n2)/2;
    } 
  }

  console.log(aluno.nome)
  console.log(aluno.media(aluno.notas[0], aluno.notas[1]))

  Mas, para simplificar o console.log acima, podemos fazer da seguinte forma:

   calcular_media(){
    return (this.notas[0] + this.notas[1])/2;
   }

   var aluno = {
    nome: "João",
    notas: [7.5, 5.0]
    
    media: calcular_media

    console.log(aluno.media())
  }

```
Esse this, é usado para que o código entenda que é aquele objeto

# Construtores

Dessa forma o criarAluno não é um objeto em si, mas retorna um objeto
```
function criarAluno(nome, n1, n2){
  return {
    nome: nome,
    notas1: n1,
    notas2: n2,
    media: function(){
      return (this.nota1 + this.nota2)/2
    }
  }
}

var turma = [
  criarAluno("Igor", 9, 6)
  criarAluno("João", 10, 2)
]

turma.forEach(function (elemento) {
  console.log(elemento)
})
```
forEach varre o array, e trás cada elemento

Também pode ser feito com for:

```
for(var aluno of turma){
  console.log(aluno.nome + " - " + aluno.media())
}
```

# Instanciando um Objeto

Dessa forma é um objeto
```
function aluno(nome, n1, n2){
  this.nome = nome;
  this.nota1 = n1,
  this.nota2 = n2,

  this.media = function(){
   return (this.nota1+this.nota2)/2
  }
}

var aluno1 = new aluno("Igor", 8, 7)

console.log(aluno1)

```

# Data

Dia atual:
```
var d = new Date()

console.log(d)
```



Dia de forma personalizada:
```
var d = new Date(2018, 08, 12)

console.log(d)
```
*É impresso setembro, pois a data funciona como o Array. Onde 0 representa Jan, e 11 Dez.



Ao passar apenas um argumento, esse é considerado como milisegundos
A data inicial é 31/12/1969 as 16:00:00
```
var d = new Date(1000)

console.log(d)
```
Assim, será impresso 31/12/1969 as 16:00:01



Formato de strings (deve ser em inglês):
```
var d = new Date("sep 05 2017")

console.log(d)
```


## Formas de instanciar uma Data:

var d = new Date();
var d = new Date(milliseconds);
var d = new Date(dateString);
var d = new Date(year, month, day, hours, minutes, seconds, milliseconds);​

## ​Métodos para manipular datas:

- getDate()	Returns the day of the month (from 1-31)
- getDay()	Returns the day of the week (from 0-6)
- getFullYear()	Returns the year
- getHours()	Returns the hour (from 0-23)
- getMilliseconds()	Returns the milliseconds (from 0-999)
- getMinutes()	Returns the minutes (from 0-59)
- getMonth()	Returns the month (from 0-11)
- getSeconds()	Returns the seconds (from 0-59)
- getTime()	Returns the number of milliseconds since midnight Jan 1 1970, and a specified date
- getTimezoneOffset()	Returns the time difference between UTC time and local time, in minutes
- getUTCDate()	Returns the day of the month, according to universal time (from 1-31)
- getUTCDay()	Returns the day of the week, according to universal time (from 0-6)
- getUTCFullYear()	Returns the year, according to universal time
- getUTCHours()	Returns the hour, according to universal time (from 0-23)
- getUTCMilliseconds()	Returns the milliseconds, according to universal time (from 0-999)
- getUTCMinutes()	Returns the minutes, according to universal time (from 0-59)
- getUTCMonth()	Returns the month, according to universal time (from 0-11)
- getUTCSeconds()	Returns the seconds, according to universal time (from 0-59)
- getYear()	Deprecated. Use the getFullYear() method instead
- now()	Returns the number of milliseconds since midnight Jan 1, 1970
- parse()	Parses a date string and returns the number of milliseconds since January 1, 1970
- setDate()	Sets the day of the month of a date object
- setFullYear()	Sets the year of a date object
- setHours()	Sets the hour of a date object
- setMilliseconds()	Sets the milliseconds of a date object
- setMinutes()	Set the minutes of a date object
- setMonth()	Sets the month of a date object
- setSeconds()	Sets the seconds of a date object
- setTime()	Sets a date to a specified number of milliseconds after/before January 1, 1970
- setUTCDate()	Sets the day of the month of a date object, according to universal time
- setUTCFullYear()	Sets the year of a date object, according to universal time
- setUTCHours()	Sets the hour of a date object, according to universal time
- setUTCMilliseconds()	Sets the milliseconds of a date object, according to universal time
- setUTCMinutes()	Set the minutes of a date object, according to universal time
- setUTCMonth()	Sets the month of a date object, according to universal time
- setUTCSeconds()	Set the seconds of a date object, according to universal time
- setYear()	Deprecated. Use the setFullYear() method instead
- toDateString()	Converts the date portion of a Date object into a readable string
- toGMTString()	Deprecated. Use the toUTCString() method instead
- toISOString()	Returns the date as a string, using the ISO standard
- toJSON()	Returns the date as a string, formatted as a JSON date
- toLocaleDateString()	Returns the date portion of a Date object as a string, using locale conventions
- toLocaleTimeString()	Returns the time portion of a Date object as a string, using locale conventions
- toLocaleString()	Converts a Date object to a string, using locale conventions
- toString()	Converts a Date object to a string
- toTimeString()	Converts the time portion of a Date object to a string
- toUTCString()	Converts a Date object to a string, according to universal time
- UTC()	Returns the number of milliseconds in a date since midnight of January 1, 1970, according to UTC time
- valueOf()	Returns the primitive value of a Date object


# var X let X const

## const
- Constante, não pode ser reatribuida, ou seja, só pode receber o valor uma vez;
- Só que, o valor pode mudar, só não pode ser reatribuida. 
- Exemplo - Reatibuindo:
```
const numero3 = {}

numero3 = {nome: "João"}
<!-- Assim dará erro, pois estou reatribuindo -->
```
- Exemplo - Mudando o valor:
```
const numero3 = {}

numero3.nome = "João"
<!-- Assim não dará erro, pois não reatribui, apenas mudei o valor -->
```
*Da mesma forma ocorre com o array, conseguimos modificar os valores dentro, usando o push por exemplo.

## let e var

A diferença delas é o escopo. Ou seja, onde a variável existe e você pode acessá-la. E onde ela não existe.

- Let e const, possuem escopo local, ou seja, só funciona dentro do bloco de código que foi criado.
- Já o var, possui o escopo global, funcionando em todo o código.

```
{
  var numero1 = 4;
  let numero2 = 3;
  const numero3 = 5;
}

console.log(numero1)
console.log(numero2)
console.log(numero3)
```
*Dessa forma, apenas o numero1 poderá ser impresso, pois o console.log está fora do escopo em que se encontram o numero2 (let) e o numero3 (const);