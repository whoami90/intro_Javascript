# introdução ao Javascript

JavaScript é a linguagem de programação da Web mais utilizada pelos sites. Além disso, todos os navegadores - estejam eles em desktops, jogos, consoles, tablets ou smartphones - incluem interpretadores JavaScript, fazendo dele a linguagem de programação mais onipresente da história.

É possível integrar Javascript com HTML e utilizá-lo desde tarefas básicas, como manipular a interface DOM, as tarefas mais complexas, como transmitir dados entre o cliente e o servidor de forma assíncrona. 

## Conceitos e sintaxe do Javascript

Faz parte da tríade de tecnologias que compõe o ambiente web, junto com HTML e CSS, sua função é cuidar do ambiente, é cuidar do comportamento e da interatividade das páginas web. 

Javascript é uma linguagem interpretada e multiparadigma, uma vez que possui suporte à programação estruturada, orientada a objetos e funcional. Também chamado de JS, foi criado inicialmente para o lado cliente, entretanto, evoluiu ao ponto de atualmente ser utilizado também do lado servidor, alem de ser uma das principais linguagens para o desenvolvimento mobile. 

## Arvore DOM

**O que é manipular a interface ou arvore DOM?**

A sigla DOM *(DOCUMENT OBJECT MODEL)* significa modelo de documento de objeto, trata-se de uma interface que permite a manipulação, via programação, de documentos HTML (e outros como o XML). 

A árvore DOM é composta por nós e objetos, ambos possuindo propriedades e métodos, além de eventos. Por meio dessa estrutura, é possível acessar, por exemplo, o conteúdo textual de um elemento − como a tag <p> −, recuperar e até mesmo alterar o seu valor.

Embora frequentemente associados, o DOM não faz parte da linguagem JavaScript, podendo também ser manipulado por outras linguagens. Neste tema, ficaremos restritos à manipulação do DOM por meio do JavaScript.

A imagem a seguir ilustra a árvore DOM e seus elementos:

Arvore DOM

*vide 1-imagemarvoreDOM.png na pasta mídias*

## Manipulando o DOM com Javascript

Por meio do JavaScript, é possível inserir dinamicamente, em tempo de execução, novos elementos à árvore DOM, mesmo que eles não façam parte da estrutura inicial da página. Da mesma forma, é possível excluir e alterar elementos preexistentes ou dinamicamente criados.

Esses elementos, porém, existirão somente enquanto durar a sessão atual do usuário. Ou seja, trata-se de uma manipulação dinâmica e dependente de estado, de ações e interações por parte do usuário, mas que se perderão quando ele sair da página.


## Incorporando o Javascript à HTML 

A incorporação pode ser realizada de duas maneiras: 

*   Código no corpo da página 
    *   Incluindo os códigos diretamente no corpo da página - dentro da seção < head> e da tag < script>

*   Arquivos externos 
    *   Mediante arquivos externos, com a extensão js, linkados ao documento também dentro da seção < head>


*Para a otimização do desempenho do carregamento da página, deve-se mover todo o código JavaScript para o seu final, após o fechamento da tag < /body>.*

> Deve-se tomar cuidado para não mover códigos ou scripts incluídos que sejam necessários à correta visualização ou aos comportamentos da página, já que os códigos movidos para o final só serão lidos e interpretados após todo o restante da página.

**Vide exemplo de inserção na pasta exemplo1**

## Sintaxe JavaScript

**Exemplos:**
~~~~~~~
<script>
    var a = 10.5;       // atribuir variável, colocar var antes do nome. 
    
    let b = "XPTO";     // sempre usar ';'.
    
    const c = true;

    a += 12;

    if (a<=20){
        a *= 5;    // se for usar mais de uma linha, tem que usar chaves. 
    }
</script>

~~~~~~~

~~~~~~~
<script>
    function somar(a,b) {
        return a + b;
    }

    let somar2 = (a,b) => {
        return a + b;
    }
    let somar3 = (a,b) => a + b;
</script>
~~~~~~~
### Vetores
~~~~~~~
<script>
    let v1 = new Array(15,21,32);
    let v2 = [13,26,37]
</script>
~~~~~~~

### Operadores aritméticos 
**+**  - Soma valores, concatena strings
**-** - subtrai valores
**'*'** - multiplica valores
**/** - divide valores
**%** - resto da divisão

### Operadores lógicos

**&&**
**||**
**!**

### Operadores relacionais

**==** - Comparação
**!=** - Diferença
**>=** - Maior ou igual
**<=** - Menor ou igual

**++** - Incremento
**--** - Decremento

**Teoria na prática**
**Vide exercicios1**


# ESTRUTURAS DE DECISÃO E DE REPETIÇÃO

## Estrutura de decisão

Estruturas de decisão, também conhecidas como “condicionais”, são instruções que executam ou pulam outras instruções dependendo do valor de uma expressão especificada. São os pontos de decisão do código, também conhecidos como ramos, uma vez que podem alterar o fluxo do código, criando um ou mais caminhos.

Para melhor assimilação do conceito, vamos usar um exemplo a partir do código construído no módulo anterior que vamos a seguir:

**Exemplo estrutura_decisao**

As orientações do programa dizem que deve ser realizada a divisão de dois números inteiros positivos.

> O que acontece se o usuário inserir um número inteiro que não seja positivo? Ou como forçá-lo a inserir um número positivo?

Para essa função, podemos utilizar uma condição. Ou seja, se o usuário inserir um número inteiro não positivo, avisar que o número não é válido, solicitando que seja inserido um número válido.

Nesse caso, o fluxo normal do programa é receber dois números positivos, calcular a divisão e exibir o resultado. Perceba que a condição cria um novo fluxo, um novo ramo, em que outro diálogo é exibido e o usuário, levado a inserir novamente o número.

O fluxo normal e o fluxo resultado da condicional podem ser vistos na imagem a seguir. Nela, são apresentados os passos correspondentes ao nosso exercício, separando as ações do programa e também as do usuário.

Repare que a verificação “é um nº inteiro positivo” permite apenas duas respostas: “sim” e “não”. Tal condição, mediante a resposta fornecida, é responsável por seguir o fluxo normal do código ou o alternativo.

Nas linguagens de programação, utilizamos as instruções condicionais para implementar o tipo de decisão apresentado no exemplo. Em JavaScript, estão disponíveis as instruções **"if/else"** e **"switch"** como veremos a seguir.

### If

A sintaxe da instrução "if/else" em JavaScript possui algumas formas. A primeira e mais simples é apresentada do seguinte modo:

if (condição) instrução.

Nessa forma, é verificada uma única condição. Caso seja verdadeira, a instrução será executada. Do contrário, não. Antes de continuarmos, é importante destacar os elementos da instrução:

É iniciada com a palavra reservada “if”.
É inserida, dentro de parênteses, a condição (ou condições, como veremos mais adiante).
É inserida a instrução a ser executada caso a condição seja verdadeira.

Outro detalhe importante: caso exista mais de uma instrução para ser executada, é necessário envolvê-las em chaves. Veja o exemplo:

~~~~
     if (condição1 && condição2){
     instrução1;
     instrução2;
      }
~~~~

Nesse segundo caso, além de mais de uma instrução, também temos mais de uma condição. Quando é necessário verificar mais de uma condição, em que cada uma delas precisará ser verdadeira, utilizamos os caracteres “&&”.

Na prática, as instruções 1 e 2 só serão executadas caso as condições 1 e 2 sejam verdadeiras. Vamos a outro exemplo:

~~~~
      if (condição1 || condição2){
      instrução1;
      instrução2;
      }
~~~~

Repare que, nesse código, os caracteres “&&” foram substituídos por “||”. Esses últimos são utilizados quando uma ou outra condição precisa ser verdadeira para que as instruções condicionais sejam executadas.

> E o que acontece se quisermos verificar mais condições?

Nesse caso, podemos fazer isso tanto para a forma em que todas precisam ser verdadeiras, separadas por “&&”, quanto para a forma em que apenas uma deve ser verdadeira, separadas por “||”. Além disso, é possível combinar os dois casos na mesma verificação. Veja o exemplo:

~~~~
      if ( (condição1 && condição2) || condição3){
      instrução1;
      instrução2;
      }
~~~~

Nesse fragmento, temos as duas primeiras condições agrupadas por parênteses. A lógica aqui é:

Execute as instruções 1 e 2 SE ambas forem verdadeiras OU se a condição 3 for verdadeira.

Por fim, há outra forma: a de negação.

> Como verificar se uma condição é falsa (ou não verdadeira)?

~~~~
      if (!condição1){
      instrução1;
      instrução2;
      }
~~~~

O sinal “!” é utilizado para negar a condição. As instruções 1 e 2 serão executadas caso a condição 1 não seja verdadeira.

Agora vamos praticar um pouco. Nos três emuladores de código a seguir, apresentamos as estruturas de decisão vistas até aqui. No primeiro emulador, temos o uso da estrutura de decisão if de maneira simples, contendo apenas uma única condição:”

**vide exercicio 2**

Já no emulador seguinte, a estrutura de decisão if é implementada com duas condições, além dos operadores lógicos AND ( && ) e OR ( || ):

**vide exercicio 3**

Por fim, no emulador a seguir, temos a estrutura if sendo usada de uma maneira mais elaborada, com mais de duas condições, combinação dos operadores && e II, assim como o uso do operador lógico de negação NOT ( ! ):

### else

A instrução "else” acompanha a instrução "if". Embora não seja obrigatória, como vimos nos exemplos, sempre que a primeira for utilizada, deve vir acompanhada da segunda. O "else" **indica se alguma instrução deve ser executada caso a verificação feita com o "if" não seja atendida.** Vejamos:

~~~~
if(número fornecido é inteiro e positivo){

    Guarde o número em uma variável;

}else{

    Avise ao usuário que o número não é válido;

    Solicite ao usuário que insira novamente um número;

}
~~~~

Perceba que o "else" (senão) acompanha o "if" (se). Logo, **SE as condições forem verdadeiras, faça isto. SENÃO, faça aquilo.**

É importante mencionar que no último fragmento foi utilizado, de modo proposital, português-estruturado nas condições e instruções. Isso porque, mais adiante, você mesmo codificará esse "if/else" em JavaScript.

## else if

~~~~
      if (numero1 < 0){
      instrução1;
      }else if(numero == 0){
       instrução2;
      }else{
       instrução3;
      }
~~~~

Repare que uma nova instrução foi utilizada no fragmento. Trata-se da **"else if", utilizada quando queremos fazer verificações adicionais sem agrupá-las todas dentro de um único "if"**. Além disso, repare que, ao utilizarmos essa forma, caso nenhuma das condições constantes no "if" e no(s) "if else" seja atendida, a instrução "else" será executada obrigatoriamente ao final.

Otimize os códigos presentes nos emuladores anteriores, usando o else if. Como exemplo, apresentamos o código do primeiro emulador modificado, no qual as 4 estruturas de decisão com if foram transformadas em uma única estrutura de decisão.

> Note que antes eram geradas duas saídas redundantes (“a é maior que b” e “b é menor que a”), pois tratavam-se de 4 estruturas independentes e por isso todas elas eram avaliadas.

Isso não ocorrerá mais com o uso de uma estrutura de decisão composta de if e else if, pois quando a primeira condição verdadeira for encontrada (“a é maior que b”), nenhuma das outras condições será avaliada:

~~~~
var a = 10;
 var b = 3;

 console.log ("if com uma única condição:");
 if (a > b){
	console.log("a é maior que b");
 } else if (a == b){
	console.log("a é igual a b"); 
 } else if (a < b){
	console.log("a é menor que b");
 } else if (b < a){
	console.log("b é menor que a");
 }
~~~~

### switch

A instrução "switch" é bastante útil quando uma série de condições precisa ser verificada. É bastante similar à "else if". Vejamos:

~~~~
switch(numero1){
 	case 0:
      		instrução1;
      		break;
	case 1:
      		instrução2;
      		break;
	default:
      		instrução3;
     		break;
 }
~~~~
De maneira geral, o switch é usado quando temos uma série de condições, nas quais diversos valores para a mesma variável são avaliados. A seguir, detalhamos o código anterior:


*   No código anterior, após o "swicth" dentro de parênteses, temos a condição a ser verificada.

*   A seguir, temos os “case”, em quantidade equivalente às condições que queremos verificar.

*   A seguir, dentro de cada “case”, temos a(s) instrução(ões) e o comando “break”.

*   Por fim, temos a instrução “default”, que será executada caso nenhuma das condições representadas pelos “case” sejam atendidas.

Vamos colocar a mão na massa? Modifique o código do emulador seguinte fazendo uso da instrução switch:

**vide exercicio 5**


