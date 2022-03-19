##### Escrito por: Artur de Oliveira Barbosa

##### Meu [GitHub](https://github.com/Space2544)

##### Email: arturoliveira886@gmail.com

##### “conhecimento é poder” -Francis Bacon
___
# Documentação Rust

### Aviso:

 Esta é uma documentação/anotação sobre o Rust, uma das linguagens mais intuitivas e viciantes que tem por ai e ainda te ajuda a entender como funciona a memoria,
compilação de outra maneira.
 Essa documentação é uma junção de cursos, documentações, fóruns, livros, vídeos que assisti, que eu fiz uma leitura e resolvi anotar pra formar essa documentação.
De qualquer forma obrigado por estar lendo.

# Prefácio

 Rust, uma linguagem de programação de multiparadigmas (varios propósitos/objetivos), com tipagem estática (sintaxe analisada e checada em tempo de compilação),
compilada (adaptável ao hardware), simplicidade de uma lingugagem de alto nivel que tem uma performance e controle de baixo nivel, ou seja, você tem uma linguagem capaz de fazer algo 
semelhante ao que C e C++ fazem mas sem se preocupar se terá vazamento de memória, já que tecnicamente Rust não tem um "garbage collector" ou melhor dizendo,
não tem um gerenciador de memoria tudo é feito na hora da compilação por conta da sua "feature" chamada "Borrowing" e "Ownership" (Emprestar e Pertencer), que é definida pelo programador.
___
# Começo

 Nessa documentação abordarei o que eu basicamente aprendi em relação a o que aprendi com Rust, desde do que eu aprendi com o compilador até o que eu entendi sobre como Rust se sobresai em
relação a outras linguagens de programação. Logo presuponho que você já fez a instalação disponivel no site oficial da documentação do [Rust](https://livro.rustbr.org/ch01-01-installation.html).
 De qualquer forma, espero que entenda minha explicação.
___
## Desenvolvendo as primeiras linhas de código em Rust.

 Se caso você tem algum conhecimento em alguma linguagem de programação como Python, C/C++ e dentre outras, de certa forma Rust vai ficar muito mais simples do que aparenta ser, ou seja
ficará bem tranquilo de entender após eu explicar tudo, mas se caso você não tem conhecimento sobre, eu irei tentar deixar o mais simples possivel de entender.
 Então nada melhor do que começarmos com um bom e velho "programa"  que mostre hello world, e depois irei "dissecar" todo o código e então irei explicar o que é cada coisa.

**Input:** 
```rust
fn main() {
    println!("hello, world");
}
```

 Bem vamos primeiro enteder os que as 3 linhas fazem começando pela...

 **Primeira linha:**
___

 A primeira é basicamente onde o código vai ser executado, ou melhor dizendo, é a função principal do código que
está em parênteses o que quer dizer que é uma função, mas está vazia, logo não temos "parâmetros" para essa função, em seguida temos "abre chaves" e então o código é introduzido.
___

 **Segunda linha:**

 Na segunda linha temos uma macro que é indicada pelo ponto de exclamação (!), e essa macro também é uma função que vai imprimir o que está escrito entre parênteses e aspas duplas, e a linha
é finalizada com ; que indica que essa linha tem um "ponto final".
___

 **Terceira linha:**

 E na terceira linha vemos o "fecha chaves", agora é só testarmos no compilador (rustc) ou se você criou isso com cargo, pode utilizar cargo build,
um pequeno detalhe é que se você tem algum conhecimento em inglês e alguns acrônimos por exemplo, dá pra você saber exatamente o que o código está fazendo.
 E lembrando toda função é reconhecida apartir de parênteses e claro **fn main()** tem que ser a primeira função antes de começar a escrever o seu código entre chaves, 
isso dá um redirecionamento ao compilador saber o que fazer. 

 Agora você aprendeu a como fazer o seu "Hello World" em Rust. Bem, agora vamos pra algo mais aprofundado, bem vamos ver como funciona a ferramenta Cargo.
___

 **Cargo**: Uma ferramenta pra organizar o seu projeto, seja um software ou simplesmente um "script" de maneira simples e intuitiva, ou seja, cargo te ajudará a fazer seu software mais
organizado e indicando as dependências que são necessarias para que seu programa seja 100% funcional.
 Vamos ver então como se cria, verifica e claro compila seu projeto/software que você criou usando o cargo abaixo:

 **Cargo new**: Como nome já diz, serve para criar um **novo** cargo, e assim você cria a pasta do projeto/software onde você colocou o nome após "new", e nessa pasta você é introduzido ao
arquivo "cargo.toml" e a pasta src que quer dizer source (src), e claro, source é fonte, ou melhor dizendo é ali onde está todo o código fonte do seu projeto, mas antes vamos ver como
funciona o cargo.toml:

```toml
[package]  
name = "The-life-of-a-rustacian"
version = "0.1.0"
edition = "2021"

[dependencies]
  
```

 Bem vamos entender o que está dizendo aqui, começando por:

 **Package**: é onde as principais informações sobre o seu projeto estarão, incluindo o autor do projeto onde é possivel colocar (caso não tiver como no exemplo acima) e claro devo lembrar
que tem que ser da mesma forma ali em cima, exemplo: author = "Ferris, The Crab", e dessa forma você mostra que é o autor/idealizador do projeto, e temos também como informação o nome e a 
versão do projeto, e sim, isso tem tudo a ver com o sistema de versionamento git, onde é possivel fazer uma "integração", ou seja, ir e criar varias versões do seu projeto e sempre que
possivel saber e revisitar tudo isso.



