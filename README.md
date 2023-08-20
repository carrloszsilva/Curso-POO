# Curso-POO - Sistema para controle de Despesas.

# Elaboração de documento para Cliente.

## Introdução.
Este documento apresenta o sistema de controle de despesas que foi desenvolvido para ajudar a gerenciar e controlar as despesas de forma eficiente. O sistema é fácil de usar e foi projetado para ser intuitivo, mesmo para aqueles que não têm experiência com esse tipo de software.

## Funcionalidades
O sistema possui diversas funcionalidades para ajudar no gerenciamento das despesas, incluindo:

**Entradas:** O sistema permite o cadastro de despesas por categorias, facilitando a organização e o controle das mesmas.

**Gerenciamento:** É possível gerenciar as despesas pagas e em aberto, garantindo que todas as contas sejam pagas em dia.

**Relatórios:** O sistema possui um menu onde é possível acessar relatórios com a quantidade total de despesas, permitindo
 uma visão geral dos gastos.

**Cadastro de usuários:** O sistema possui um submenu para cadastro e gerenciamento de usuários, com login e senha. É possível definir diferentes níveis de acesso para os usúarios do sistema.

## Protótipo de tela.
Sugestão de protótipo de tela para o sistema:

O protótipo de tela para o sistema de controle de despesas pode ter um design limpo e moderno, com cores suaves e fontes legíveis. Na parte superior da tela, pode haver um menu com opções para acessar as diferentes funcionalidades do sistema, como entradas, gerenciamento de despesas e relatórios. Abaixo do menu, pode haver uma área para exibir informações sobre as despesas cadastradas, como a data, a categoria e o valor. Também pode haver opções para filtrar as despesas por data ou categoria. Na parte inferior da tela, pode haver um gráfico mostrando a evolução das despesas ao longo do tempo.

## Gerencimento de relatórios.

Para acessar os relatórios no sistema de controle de despesas, você pode seguir os seguintes passos:

1. Abra o sistema e faça login com suas credenciais de usuário.
2. Na parte superior da tela, clique no menu e selecione a opção "Relatórios".
3. Você será redirecionado para a página de relatórios, onde poderá visualizar informações sobre as despesas cadastradas.
4. É possível filtrar os relatórios por data ou categoria para obter informações mais específicas.
Esses são os passos básicos para acessar os relatórios no sistema de controle de despesas

* É possível exportar os relatórios do sistema de controle de despesas para um arquivo txt.
Para fazer isso, você pode seguir os seguintes passos:

1. Abra o sistema e faça login com suas credenciais de usuário.
2. Na parte superior da tela, clique no menu e selecione a opção "Relatórios".
3. Você será redirecionado para a página de relatórios, onde poderá visualizar informações sobre as despesas cadastradas.
4. Clique no botão "Exportar" e selecione a opção "txt" no menu suspenso.
5. Escolha um local para salvar o arquivo TXT e clique em "Salvar".

* Esses são os passos básicos para exportar os relatórios do sistema de controle de despesas para um arquivo txt.

# Explicações Tecnicas do Sistema.
## Herança e Polimorfismo. 

Herança e polimorfismo são conceitos importantes da programação orientada a objetos que podem ajudar a criar um código mais limpo e organizado. No contexto do sistema de controle de despesas, usa-se a herança para criar uma hierarquia de classes que representam diferentes tipos de despesas. Por exemplo, pode-se ter uma classe mãe `Despesa` que define propriedades e métodos comuns a todas as despesas, como valor, data e descrição. Em seguida, você pode criar classes filhas para representar diferentes categorias de despesas, como `DespesaAlimentacao`, `DespesaTransporte` e `DespesaMoradia`, que herdam as propriedades e métodos da classe `Despesa` e adicionam suas próprias propriedades e métodos específicos.

O polimorfismo permite que você use um único tipo de variável para armazenar objetos de diferentes classes relacionadas por herança. Isso significa que você pode ter uma lista de despesas do tipo `List<Despesa>` que pode armazenar objetos das classes `DespesaAlimentacao`, `DespesaTransporte` e `DespesaMoradia`. Quando você percorre a lista, pode chamar métodos comuns a todas as despesas, como `getValor()` ou `getData()`, sem se preocupar com o tipo específico de cada despesa.

Esses conceitos podem ajudar a tornar o código mais limpo, organizado e fácil de entender, pois permitem que criar uma estrutura clara para representar as diferentes entidades do sistema e reutilizar código comum entre elas. Além disso, o polimorfismo permite que você escreva código mais genérico e flexível, que pode lidar com diferentes tipos de despesas de maneira uniforme.