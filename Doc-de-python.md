Escrito por: Artur de Oliveira Barbosa
GitHub: https://github.com/Space2544 
Email: arturoliveira886@gmail.com 

#### “conhecimento é poder” -Francis Bacon
___
# Documentação de Python

### Aviso:

Esta será uma documentação/anotação sobre o Python, que na minha opinião é uma das linguagens de programação mais interessantes que tem por ai. É uma junção de cursos, documentações, fóruns, livros, vídeos que assisti, que eu fiz uma leitura e resolvi anotar pra formar essa documentação.


# Prefácio

 Python é uma linguagem de programação de alto nível, interpretada de script, imperativa, orientada a objetos, funcional, de tipagem dinâmica e forte. Foi lançada por Guido van Rossum em 1991. 
 Atualmente, possui um modelo de desenvolvimento comunitário, aberto e gerenciado pela organização sem fins lucrativos Python Software Foundation. Apesar de várias partes da linguagem possuírem padrões e especificações formais, a linguagem, como um todo, não é formalmente especificada. O padrão de facto é a implementação CPython.

 A linguagem foi projetada com a filosofia de enfatizar a importância do esforço do programador sobre o esforço computacional. Prioriza a legibilidade do código sobre a velocidade ou expressividade. Combina uma sintaxe concisa e clara com os recursos poderosos de sua biblioteca padrão e por módulos e frameworks desenvolvidos por terceiros.
 Python é uma linguagem de propósito geral de alto nível, multiparadigma, suporta o paradigma orientado a objetos, imperativo, funcional e procedural.

 Possui tipagem dinâmica e uma de suas principais características é permitir a fácil leitura do código e exigir poucas linhas de código se comparado ao mesmo programa em outras linguagens. 
  Devido às suas características, ela é utilizada, principalmente, para processamento de textos, dados científicos e criação de CGI’s para páginas dinâmicas para a web.

 Foi considerada pelo público a 3ª linguagem "mais amada", de acordo com uma pesquisa conduzida pelo site Stack Overflow em 2018 e está entre as 5 linguagens mais populares, de acordo com uma pesquisa conduzida pela RedMonk.

 O nome Python teve a sua origem no grupo humorístico britânico Monty Python, criador do programa Monty Python's Flying Circus, embora muitas pessoas façam associação com o réptil do mesmo nome (em português, píton ou pitão). [wikipedia](https://pt.wikipedia.org/wiki/Python).
___
 Como foi possível ver, a historia das linguagens de programação sempre envolveram muitas coisas e situações que aconteciam e que foram feitas pra resolver determinado problema e claro isso não foi diferente com o `Python`.

 O bom de se aprender Python é que essa é uma das linguagens que podem ser usadas pra mais de uma única coisa e ainda fazer relativamente bem essa função e de facil compreensão, desde data science, machine learning e até mesmo criação de apps e jogos.

 Agora que sabemos um pouco mais sobre a história dessa linguagem vamos para os exemplos de `comandos básicos`.
___
 # Comandos Básicos

`Print ()`: Essa função serve para escrever um texto, comentário dentro de parênteses, mas se quiser escrever algo será necessário aspas. 

### Input:
```Python
print('hello, world!')
```

### Output:
```
hello, world!
```
___

`=` : O simbolo de “igual” em Python significa “recebe”. Ou seja uma variável vai receber tal valor.

`,` : O simbolo da “virgula” em Python tem a função de juntar letras,  números e etc. Ou simplesmente fazer uma “pausa” se caso você quer que duas variáveis apareçam na mensagem. 

### Input
```Python
x = 1
y = 2
print(x,y)
```
### Output:
```
1 2
```
___
`Input()`: A função `input()` serve para você colocar um valor na sua variável.

### Input:
```Python
x = input('coloque um valor: )
y = input('coloque outro valor: )
print('a junção desses dois números é: ', x + y)
```

### Output:
```
coloque um valor: 10
coloque outro valor: 20
a junção desses dois números é: 1020
```

Nesse exemplo acima, o sinal de adição foi usado pra "juntar" e não "somar".

___

# Tipos Primitivos

 Em python temos vários comandos que são denominados tipos primitivos, cada um desses comandos fazem algo em relação a uma determinada função que você quer que o computador execute, ou melhor dizendo o seu script e etc.
 Citarei 4 desses Tipos primitivos e o que cada um faz:
___

 `Int()`: É uma função que converte todo o valor colocado dentro de () em um número `int`eiro, ou seja se você digitar algum número de ponto flutuante ou melhor dizendo “quebrado” como por exemplo o pi (3.1415…) vai dar erro pelo fato de não ser um número inteiro.

### Input:

```Python
x = int(input('coloque um valor para teste: ))
```

### Output:
```
coloque um valor para teste: 0.1

Erro
```
___

`Float()`: Transforma todo o valor colocado dentro em um ponto flutuante ou seja, se colocar 1, vai virar 1.0, e esse ponto flutuante também é conhecido como número “quebrado”.

### Input:

```Python
x = int(input('coloque um valor quebrado: ))
```

### Output:
```
coloque um valor quebrado: 3.1415

```

Dessa vez não aconteceu erros, por conta que foi aplicado corretamente o valor a função.

___

