# Desafio de JavaScript 1

## Ambiente

- Instalar a extenção "EditorConfig for VS Code"
- Instalar a versão LTS do Node

## Preparação

O entendimento de alguns conceitos será importante para o cumprimento do desafio. O primeiro conceito é a __CRUD__. Essa sigla representa as 4 operações básicas que podemos fazer em um dado armazenado. O "C" vem de "create", que é a criação de dados novos. O "R" vem de "read", que é a leitura dos dados armazenados. O "U" vem de "update", que é a atualização de dados já existentes. E, finalmente, o "D" vem de "delete", que é a remoção de dados já existentes.

O segundo conceito é a __Imutabilidade__. Quando manipulamos dados no JavaScript, em alguns casos é importante manter os dados imutáveis. Na prática, isso significa que ao alterar um array, por exemplo, não devemos modificar o array original e sim criar um novo (baseado no original) e só após isso substituí-lo. Ferramentas como o React dependem dessa prática para que possam funcionar corretamente, pois assim ele consegue saber com mais facilidade quando algum dado mudou e assim disparar uma re-renderização de algum componente da tela.

Além desses conceitos é bom ter conhecimento dos métodos de array do JavaScript. Basicamente existem 2 tipos de métodos. O primeiro tipo é o que altera o array original e o segundo tipo é o que não altera o array original e, em vez disso, retorna um novo array. Para este desafio, apenas o segundo tipo deve ser usado, pois ele respeita a imutabilidade dos dados.

Antes de começar o desafio em si, é necessário encontrar os métodos que podem ser usados. Como os array no JavaScript possuem muitos métodos (documentação disponível [aqui](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array)), a busca pode se concentrar apenas nos seguintes:

- `concat()`
- `filter()`
- `find()`
- `forEach()`
- `map()`
- `pop()`
- `push()`
- `shift()`
- `unshift()`

## Desafio

O desafio simula a manipulação de dados referentes à lista de colaboradores de uma empresa. Os dados estão armazenados em um array de objetos chamado `colaboradores`. Cada item dessa array é um objeto que representa 1 colaborador, contendo as chaves `matricula` (o identificador do colaborador), `nome` (o nome do colaborador) e `cargo` (o cargo ocupado pelo colaborador na empresa).

O desafio consiste em escrever as funções que serão responsáveis por manipular os dados da lista de colaboradores. São 4 funções e cada uma representa uma ação da CRUD.

A primeira é a `contratarColaborador` e representa o create da CRUD. Essa função deve receber `nome` e `cargo` como parâmetros, mas ela deve gerar a `matricula` internamente. Para gerar a `matricula`, a função deve considerar a posição que o novo colaborador vai assumir no array de colaboradores. Aqui é importante lembrar que o index no JavaScript começa pelo número 0, então a `matrícula` não é igual ao index, mas deriva dele.

A segunda é a `mostrarColaboradores` e representa o read da CRUD. De todas as funções, esta é a mais simples e deve apenas mostrar o array completo de colaboradores ao ser executada. Esta função não precisa receber parâmetros e não deve utilizar métodos de array.

A terceira é a `promoverColaborador` e representa o update da CRUD. Esse função deve receber como parâmetro a `matricula` e o novo `cargo` do colaborador. A `matricula` vai servir para encontrar o colaborador no meio do array e, assim que encontrado, o objeto que representa o colaborador deve ser atualizado trocando o `cargo` antigo pelo novo recebido. As outras informações devem se manter inalteradas.

A quarta e última é a `demitirColaborador` e representa o delete da CRUD. Essa função precisa receber apenas a `matricula` para encontrar o colaborador e assim removê-lo do array de colaboradores.
