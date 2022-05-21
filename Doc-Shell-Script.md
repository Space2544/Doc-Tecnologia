Escrito por: Artur de Oliveira Barbosa

GitHub: https://github.com/Space2544

Email: arturoliveira886@gmail.com 

#### “conhecimento é poder” -Francis Bacon
___
# Documentação Shell & Shell Script

### Aviso:

Esta será uma documentação/anotação sobre o Python, que na minha opinião é uma das linguagens de programação mais interessantes que tem por ai. É uma junção de cursos, documentações, fóruns, livros, vídeos que assisti, que eu fiz uma leitura e resolvi anotar pra formar essa documentação.

# Prefácio

Shell do inglês “casca” nesse caso de um sistema operacional, é onde a maioria ou quase todos os processos acontecem,  e claro você pode usar isso ao seu favor para por exemplo criar um arquivo que pode ser lido no “shell” que é apelidado de “Script”, no caso “Shell Script”, um script pode funcionar de inúmeras maneiras inclusive para automação de processos no linux ou no windows por exemplo.
 E claro esse processo requer um conhecimento sobre o sistema, que no nosso caso é o linux ou melhor dizendo, Unix, já que o linux é da família unix,
e no windows o processo é semelhante em alguns pontos, como o comando echo que serve pra mostrar algo na tela.
 Lembrando que normalmente se caso você precisar de ajuda em relação o que mais cada comando faz você pode colocar --help na frente de determinada função.
 Exemplo: mkdir --help
___

## Comandos básicos

 O shell do linux tem uma curva de aprendizado bem razoavél e claro, só de aprender shell scripting você facilita e muito sua vida usando o linux e demais distribuições ou até mesmo alguns sistemas da família Unix.
 Por exemplo você pode pegar um comando como: sudo apt update && sudo apt upgrade e resumir em uma palavra só, como por exemplo update ou fazer um script que lança os programas de sua preferência só apertando um botão.
 Mas antes de aprender isso, vamos ao básico.

___
Comandos: 

**cd**: **c**(hange) **d**(irectory), esse comando serve para trocar de diretorio, que por padrão você está na /home, mas quer se deslocar para outro diretorio, então o comando cd é necessario.
 Vamos supor que você queira entrar no diretorio downloads, mas você não sabe como fazer isso no terminal pra instalar algo ou que alguma coisa precisa ser feita dentro dessa pasta, pra isso você vai dar o comando:

```bash
$ cd Downloads/
```
(obs, não precisa do $, isso é pra representar o bash).
 Mas se caso esse não for o nome da pasta você pode apertar a tecla Tab que serve pra "autocompletar" e mostrar quais os possíveis diretorios que podem ser acessados dentro da /home por exemplo:
```bash
$ cd 
Downloads/				Música/			.config/
Documentos/			   Modelos/			.local/
```
 (Logo após escrever cd e apertar a tecla espaço e depois tab, haverá uma lista semelhante a essa a cima.)
 Esse exemplo acima foi o que pode aparecer no terminal quando você digita cd, e nesse exemplo mostra também os diretorios que começam com ponto.
  Esses diretorios ou arquivos são “escondidos” já que são do sistema ou que é pra ser escondido do usuario mesmo, por exemplo se eu quiser criar um arquivo escondido eu posso usar .(nome do arquivo ou pasta) e assim ficará “invisivel” quando usar um gerenciador de arquivos. 
 Mas por exemplo se caso você quiser modificar algo, normalmente fica dentro da pasta .config, e nisso você tem um leque de possibilidades muito grande, e dai acaba surgindo customizações na interface da sua distribuição linux. 
 Bem mas como faria pra retornar se caso eu entrei na pasta downloads?, pra isso você precisa adicionar dois pontos depois do **cd**.
Exemplo:
```bash
/Downloads $ cd .. 
```
 E quando pressionar enter você subirá uma pasta acima, ou seja, vai voltar pra home denovo, e se você quiser retornar de vez sem ser um diretorio por vez, apenas digite **cd** e vai retornar para a /home.
___
 **ls**: **l**i**s**t, **ls** é um comando que serve para **listar** arquivos e pastas ou diretorios, ou seja você pode ter uma visualização fixa de quais diretorios e arquivos estão dentro de por exemplo /downloads  ou /home, e só é necessario dar apenas ls  para mostrar o conteúdo dentro.
Exemplo:
```bash
/Download $ ls
image001.jpg
image002.jpg
image003.jpg
image004.jpg
image01.svg
image1.png
```
___

 **mkdir**: **m**a**k**e **dir**ectory, como o próprio comando já diz, faz um diretorio, e claro, pra que esse diretorio possa ser criado é necessario fazer o seguinte, vamos usar o Download como uma pasta para esse exemplo:
```bash
$ sudo mkdir Downloads/teste
```
 Mas você se perguntou o que é sudo?, sudo é uma maneira de fazer com que você através desse comando tenha “poder” administrativo ou seja você “vira” um super usuario ao dar esse comando, normalmente não é necessario esse comando mas se caso aparecer um aviso de que “você precisa ser um super usuario para fazer tal ação”, ai você pode utilizar, mas toma muito cuidado, qualquer ação que altere algo do sistema e que o sistema avisa que pode haver alterações, primeiro pesquisa e tente entender o que você esta fazendo e como que isso pode afetar ou não o sistema, dado o aviso vamos voltar ao assunto.

 Depois de ter criado a pasta teste em Downloads/, você pode criar arquivos com o comando **touch**, touch serve para “tocar”, criar um arquivo com a extensão (.txt, .svg, .jpg, .docx …) de sua preferência e necessidade, logo temos algo que facilita e muito quando quisermos criar um arquivo dentro de alguma pasta sem precisar necessariamente de uma interface guiada (conhecida também por GUI).
 Logo para se criar um arquivo é usado o comando dessa maneira:

```bash
$ touch ‘nome do arquivo. extensão de sua preferência’ 
```
 E assim você cria um arquivo com touch, mas vamos criar um arquivo que seja adequado:

 ```bash
 Downloads/teste $ touch ‘teste_001.txt’
 ```

 Quando adicionamos  _ o texto fica armazenado sem problemas e é mais recomendavel assim visto que pode causar problemas no arquivo e dentre outras coisas. Agora você tem uma pasta, um arquivo, conhecimento de como sair e entrar dentro de pastas, mas como fazer pra editar esse arquivo de texto?
 Uma das varias opções que temos é o editor de texto, mas qual?, por padrão como o Linux é kernel do Gnu, logo temos inumeras ferramentas que aliás estão disponiveis na Free Software Foundation, se caso quiser se aprofundar mais por lá é só clicar aqui [Free Software Foundation](https://www.fsf.org/pt-br) (é recomendável que se pesquise o nome em si da FSF por segurança.)
 E dentro do Gnu/Linux temos um editor de texto que já vem por padrão que se chama **nano**, nano é um editor de texto bem simples para editar/escrever/modificar textos, assim fazendo com que seja bem fácil a sua utilização. E para lançar esse editor de texto é bem simples:

```bash
Downloads/teste $ nano teste_001.txt
```
 E então você estará na tela do nano, o que você precisa saber agora é o que faz cada comando abaixo:

**Ctrl + S**: (^S) serve para salvar o arquivo, ou seja, quando você terminou de escrever algo, você vai e faz o comando Ctrl e pressiona em seguida S.

**Ctrl + X**: Como o próprio nano mostra, serve para sair do nano e ir de volta para o terminal.

 O sinal de **^** quer dizer que é a tecla CTRL deve ser combinada junto com as teclas alfabéticas para você conseguir fazer o que se precisa.

 O resto é um tanto que auto explicativo, e passando para aproveitar, existe um “manual” que pode ser instalado no linux, que se chama man, man é um acrônimo para manual, e você pode pesquisar no próprio terminal se existe um manual sobre o nano por exemplo.
 Para instalar vai depender da sua distribuição, mas irei mostrar como em algumas das distros mais famosas:

Arch Linux e derivados.
```bash
sudo pacman -S man
```

Ubuntu/Linux mint/ Debian.
```bash
sudo apt install man
```
 Bem essas são uma das maiores que temos, mas lembre-se, sempre vai no site da companhia/grupo onde foi baixada sua distro e veja a documentação se possível sobre como fazer uma instalação pelo terminal.
 Até aqui você sabe criar um arquivo, criar um diretorio, editar um arquivo, entrar em uma pasta e isso tudo pelo terminal, mas você deve estar pensando, como eu faço pra saber exatamente em qual diretorio eu estou?
 Quando você clica na barra de pastas do seu gerenciador de arquivos normalmente mostra as pastas e onde você está no momento, e no Shell isso é possível com um único comando:

 **pwd**: **P**rint **W**orking **D**irectory, esse comando serve para mostrar onde você está, e como o próprio nome já diz, imprimir diretorio funcionando, (ou trabalhando mas isso depende da tradução). 
 E nisso esse comando mostra qual diretorio esse comando foi executado, exemplo:

```bash
$ pwd
/home/(nome do usuario)
```
 e então isso vai te ajudar a saber onde você está exatamente, mas e se eu quiser por exemplo copiar algo pra dentro de algum diretorio?, pra isso serve esse comando:

 **cp**: copy, como o nome já diz, esse comando irá copiar o arquivo de uma pasta, ou se prefirir, você pode duplicar o arquivo copiando e colando dentro da mesma pasta, mas precisa ser feito manualmente na maioria dos casos, exemplo:

```bash
$ cp teste_001 txt teste_002.txt 
```
e então você terá dois arquivos dentro da pasta quando digitar **ls**:

```bash
$ ls 
teste_001.txt
teste_002.txt
```

e claro você também pode como por exemplo copiar diretorios dessa maneira:

```bash
$ cp -r Downloads/teste /desktop/
```
(Observação: desktop é área de trabalho em inglês.)
O menos **-r** serve para copiar essa pasta e tudo que está dentro de maneira **recursiva** assim, tudo será copiado e colado no lugar que você deseja. 
 E pronto, agora você copiou esses arquivos que estavam em teste na área de trabalho.
 E claro, você consegue copiar muito mais do que um arquivo, basta você fazer nesse estilo:

```bash 
$ cp -r 1/ 2/ 3/ 4/ 5/ desktop/
```

 E então as pastas 1,2,3,4,5 irão pro desktop, lembrando que, o ultimo é o destino dessas copias e o que antecede o ultimo é o que vai ser copiado, ou seja 5, 4, 3, 2, 1.
 E também tem como você copiar tudo o que está dentro da pasta sem digitar nome por nome:

```bash
$ cp -r * (e aqui você especifica o diretorio de destino).
```
 Dessa forma tudo o que está dentro dessa pasta vai para o diretório de sua preferência.
___

 Agora que você viu tudo isso, que tal a gente aprender a como "apagar" alguns arquivos, pastas e coisas do tipo?
 Vamos supor que você não queria mais alguns arquivos que estão em /Downloads e como você faria isso pelo terminal do linux?, pra isso existe o comando **rm**

 **rm**: rm ou do inglês remove, serve para **remover** arquivos e pastas, dessa maneira:

```bash
$ rm (nome do arquivo)
```

 Dependendo da situação, é necessário você usar o comando sudo, já que pode ser que peça a autorização de "super-usuario" pra isso. Logo, "com grandes poderes vem grandes responsabilidades" 
 E pra remover um arquivo é necessario colocar **-rf**

```bash
$ rm -rf (nome da pasta)
```
(essa opção -rf quer dizer que, vai remover de maneira **recursiva**, e o f faz com que não peça confirmação de maneira **forçada**, e a proposito, você pode combinar essas opções pra ter uma remoção mais "segura" e clara do que está fazendo, para saber mais sobre utilize, man rm, assim você poderá consultar o manual do rm pelo terminal ou se prefirir, veja videos ou leia artigos sobre.)

 Mas tome muito cuidado ao fazer isso, já que isso é eliminado de maneira direta.
 E tem também a opção **-i** que faz uma pergunta pra confirmar se você quer remover mesmo algum arquivo, e então você poderá ter essa decisão onde você responde **yes** ou **no** (**sim** ou **não**).
___

 E além de copiar, colar, a gente pode também mover algum arquivo pra algum lugar com o comando:

 **mv**: mv ou move, é um comando que serve para **mover** e renomear arquivos e pastas para o local desejado ou mudar para o nome que prefirir, e para fazer isso é dessa forma:
 ```bash
 $ mv (nome da pasta e arquivo) (diretorio desejado)
 ```
 E sim esse negocio do espaço é necessario para que o shell saiba a onde exatamente você quer levar, mover esse diretorio e também para não dar nenhum tipo de erro, obeserve:
```bash
$ mv imagem.jpg /imagens
```
 E nisso a imagem.jpg será movida para o diretorio imagens, dessa forma tudo ficará mais atrativo de se usar o terminal, o que deixa tudo muito mais interessante mesmo.
 E para renomear é só fazer isso:
 ```bash
 $ mv teste.txt testezinho.txt
 ```
 Nesse exemplo o arquivo teste foi renomeado para testeizinho.txt, mas e se eu quiser mover o arquivo e renomear de uma só vez, pra isso você pode seguir a estrutura desse exemplo:
 ```bash
 $ mv testezinho.txt downloads/teste1.txt
 ```
 E então o testezinho.txt vai ser renomeado para teste1.txt e será movido para a pasta de downloads.
___

 Já imaginou se você pudesse procurar por uma pasta ou por algum arquivo no terminal?, sim isso é possivel mas não da maneira que talvez você esteja pensando, vamos supor que você precisa saber o porque uma dependencia está dando problema, e então você não tem ideia nenhuma de qual é a localização pra corrigir isso, e então é ai onde esse comando entra em ação, e seu nome é: 
 **find**: find do inglês significa procurar, encontrar, serve para encontrar o caminho do arquivo ou pasta que você está procurando, mas claro, tem que ser de maneira especifica, exemplo:
```bash
$ find . -name Downloads
```
 Nesse momento o computador vai entregar o resultado da pesquisa, e assim mostrará o que você provavelmente está procurando.
 Esse **.** após o find quer dizer em que local o computador deve procurar por esse arquivo, diretorio e etc.
 então se quiser você pode ir e colocar algo mais especifico como **/** que é a raiz do sistema, exe,plo:
```bash
$ find / -name imagem.png
```
 e claro o **-name** é pra especificar o nome, no nosso caso o nome é **imagem.png**.
___

 O terminal tem um comando muito interessante chamado:

 **file**: file ou do inglês arquivo, serve para mostrar detalhes do que é tal arquivo, e tem como saber se algo é ou não um diretorio, um arquivo de imagem sem extensão, exemplo:
```bash
$ file hello
hello: Bourne-Again shell script, ASCII text executable
```
 então como podemos ver acima **hello** é um arquivo de shell script mas sem a extensão **.sh**, e é só seguir o exemplo acima, colocar o comando file mais o nome do arquivo que você quer saber sobre.
___
 Outro comando muito interessante é o:

 **cat**: cat é um acrônimo para concatenate, que traduzido significa concatenar, esse comando serve para exibir o conteúdo dos arquivos e dentre outras coisas a mais, e claro serve também como um "editor de texto" muito, mas muito simples. O comando cat é muito útil mesmo, ao ponto de você nem precisar por exemplo visualizar um arquivo com algum editor de texto como o nano, ou seja, tudo fica muito mais rápido e fácil de visualisar o que tem esse arquivo. Aqui a baixo vai alguns exemplos:
```bash
$  cat test.txt
```
 No exemplo acima vai ser possivel ver o conteúdo de uma maneira simples, mas se quiser utilizar contando a quantidade de linhas é só colocar **-n** na frente de cat e após isso o nome do arquivo que deseja visualizar.
 E para "editar" e criar um arquivo com o cat, você pode utilizar dessa forma:
```bash
$ cat > (nome do arquivo)
```
 E para parar de digitar é só combinar as teclas CTRL + D. E então o arquivo será salvo com o que foi escrito.
 E tem como por exemplo "concatenar" arquivos, vamos supor que você tenha 3 arquivos e você queira juntar em um, pra isso você pode seguir esse pequeno exemplo abaixo:
 ```bash
 $ cat a.txt b.txt > ab.txt
 ```
 E então você consegue "juntar" dois arquivos em um, e tem como também anexar algum arquivo dentro de outro, pra isso você precisa mostrar o caminho do diretório com o arquivo que você deseja anexar e mostrar a qual arquivo você quer anexar, veja no exemplo abaixo:
 ```bash
 $ cat /etc/passwd >> teste.txt
 ```
 E assim todo o conteúdo de passwd será anexado ao teste.txt, e então você poderá também anexar outras coisas dessa forma.
___
 Temos um comando no shell que se assemelha muito ao find, mas serve para encontrar uma linha especifica no arquivo, e esse comando se chama:

 **grep**: grep é um comando muito utilizado para por exemplo pesquisar determinada palavra em um determinado arquivo, exemplo:
```bash
$ grep bash /etc/passwd
```

 O que eu estou procurando é alguma linha que tenha a palavra "bash" no arquivo do passwd, e temos a opção -i pra procurar até mesmo o que está em maiusculo, -o pra somente mostrar o que você procura mesmo sem ser a linha inteira e etc. Lembrando que essas opções você coloca na frente do grep:

```bash
 $ grep -i ...
 $ grep -o ...
```
 E então você dá a continuidade a o que quer procurar em um determinado arquivo.
___
 Um comando que te ajuda a poupar muito tempo é o:
 **cut**: Cut do inglês, cortar, serve parar **cortar** uma parte de um        documento de texto (por exemplo) que é especificada pelo usuario.
 Dessa forma você pode pegar informações úteis sem precisar gastar seu tempo:
```bash
$ cut -c '1-4' teste.sh
echo
```
 Essa opção -c quer dizer que é pra apenas cortar **caracteres**, e nesse caso quisemos que mostrasse apenas do 1 até 4, então apareceu assim. Ou se prefirir pode digitar dessa forma também: **'1,2,3,4'**. Além dessa opção temos também a opção -d e a -f, **-d** serve para delimitar até que "ponto"
é pra manter, então quando você faz isso o resto é "eliminado". Usando aspas simples '' você coloca o delimitador de sua preferencia.
Já a opção **-f** serve para delimitar o "campo", então vamos com um exemplo aqui abaixo de como você pode combinar esses dois:
```bash
$ cut -d ',' -f  '1-2' test.txt
echo this is a tiny, very tiny test
```
 Dessa forma pegamos o que está no primeiro campo e no segundo, agora de forma separada vai ser mais fácil de entender:
```bash
$ cut -d ',' -f  '1' test.txt
echo this is a tiny
```
 Foi possível ver que só pegou o primeiro **campo** que foi **determinado** pela virgula. Agora a segunda parte:
```bash
$ cut -d ',' -f  '2' test.txt
very tiny test
```
 E assim o segundo campo apareceu. Se quiser, você pode determinar qualquer pontuação por exemplo dentro das aspas da opção **-d**, assim é possível fazer também com o número de campos dentro de **-f**.
 E o melhor de tudo é que você pode fazer com que tudo o que você colocou para cortar e etc pode ser passado pra um outro arquivo com todas as alterações sem precisar se quer dar CTRL + Shift + C e CTRL + Shift + V.
 Pra isso é utilizado essa opção aqui **>**, e dessa forma você consegue mandar tudo para o arquivo que você quer criar:
```bash
$ cut -d ',' -f  '1' test.txt > test2.txt
```
___
