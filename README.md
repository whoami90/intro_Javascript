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
