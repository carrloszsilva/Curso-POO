# Sistema para controle de Despesas.

## Elaboração de documentação.

## Introdução.
Este documento apresenta o sistema de controle de despesas que foi desenvolvido para ajudar a gerenciar e controlar as despesas de forma eficiente. O sistema é fácil de usar e foi projetado para ser intuitivo, mesmo para aqueles que não têm experiência com esse tipo de software.

## Funcionalidades.

**Entradas:** O sistema permite o cadastro de despesas por categorias, facilitando a organização e o controle das mesmas.

**Gerenciamento:** É possível gerenciar as despesas pagas e em aberto, garantindo que todas as contas sejam pagas em dia.

**Relatórios:** O sistema possui um menu onde é possível acessar relatórios com a quantidade total de despesas, permitindo uma visão geral dos gastos.

**Cadastro de usuários:** O sistema possui um submenu para cadastro e gerenciamento de usuários, com login e senha. É possível definir diferentes níveis de acesso para os usúarios do sistema.

`Sugestão de protótipo para o Sistema`

O protótipo de tela para o sistema de controle de despesas pode ter um design limpo e moderno, com cores suaves e fontes legíveis. Na parte superior da tela, pode haver um menu com opções para acessar as diferentes funcionalidades do sistema, como entradas, gerenciamento de despesas e relatórios. Abaixo do menu, pode haver uma área para exibir informações sobre as despesas cadastradas, como a data, a categoria e o valor. Também pode haver opções para filtrar as despesas por data ou categoria. Na parte inferior da tela, pode haver um gráfico mostrando a evolução das despesas ao longo do tempo.

## Gerenciamento de relatórios.

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
5. Escolha um local para salvar o arquivo txt e clique em "Salvar".

## Definição de requisitos

*O programa contará com um menu de opções para que o usuário possa escolher o que será executado.
Esse menu pode ser criado usanto uma condição que será executada equanto a condição de saida não 
for acionada.
* Cada opção terá um metodo para cadastrar uma despesa, listar a despesas por tipo, pagas, em aberto

## Classe
Uma classe **Despesa**.

Essa classe terá atributos como valor, data e descrição e seu metodos. Na classe principal do sistema (por exemplo, Main) implemetar um método para cadastrar novas despesas. Esse método deve solicitar ao usuário os dados da despesa (valor, data, descrição, etc.) e criar um novo objeto da classe Despesa com essas informações.

*Um metodo de sobreescrita para que o usúario possa entrar com os dados de cada despesa deve ser implementado.*

Para armazenar as Despesas pode-se criar uma lista por exemplo, ArrayList de despesas , para armazenar os objetos Despesa. Criar um atributo na classe Main do tipo lista, e sempre que uma nova despesa for cadastrada, adicione-a a essa lista

## Encapsulamento
É recomedavél encapsular os atributos valor - Ao encapsular o atributo valor, ele não pode ser alterado diretamente, o que garante que o valor seja imutável. Isso evita erros causados por modificações acidentais. Para manipular o valor encapsulado em uma classe, é necessário definir métodos de acesso, também conhecidos como getters e setters. Pode-se controlar o acesso e a manipulação do valor na classe, garantindo maior segurança. Pois acidentalemte a dona encrenca pode querer alterar o valor que gostou no salão de beleza...

## Herança
**Classes filhas** da classe Despesa pode-se criar tipos (categorias) de despesas como
**DespesaAlimentação** - **DespesaTransporte**. As classes filhas herdam os métodos e atributos da classe mãe. Elas podem usar e executar os métodos da classe mãe, bem como acessar e modificar os atributos da classe mãe. Além disso, as classes filhas também podem adicionar métodos e atributos adicionais específicos a elas.

## Gerenciar Despesas.
Para gerenciar as despesas criar uma classe principal que contenha uma lista de todas as despesas criadas. Pode-se criar uma Lita do tipo ArrayList para armazenar os objetos Despesas. Nessa classe principal terá métodos para adicionar, editar, alterar ou excluir uma despesa 

No GerenciadorDespesa(){

Pode-se criar um menu de opções para executar o metodo desejado.

}

## Gerenciar  usúario
Para criar um usúario do sistema - definir nome do usuário e uma senha.
Existi um usuário que tem privilegios - Portanto deve-se criar uma classe Usuário mãe.
Nesta classe mãe terá os atributos nome, senha e um e-mail. 
Para um usuário com privilegios além da senha será solicitado o cpf na hora de logar no sistema
Apenas usuários com privilegios podem cadastrar e exluir novos usúarios e excluir Despesas.

Deve conter um metodo de sobreecrita com o mesmo nome da Classe para que seja possivel entrar com os dados ao criar os novos objetos Usúario. As **senhas** devem ser criptografadas e conter uma regra - **Senhas** devem ter letras maisculas e minusculas, números, ao menos um elemento especial # * ; e no mínimo 10 caracteres. Ao digitar a senha incorreta por 3 vezes o usário será bloqueado. Este deve ir na opção esqueceu senha e informar seu dados, nome, e-mail e cpf. Uma link para redefinição de senha será enviado para o e-mail cadatrado. A nova senha não pode ser igual a anterior.

## Exportando relátorios
Para gerar um relatório de Despesas criar um metodo que receba como parametro a lista de Despesas 
cadastradas. Deve conter uma variavel para receber o relatório. Percorrer a lista de Despesa add as informaçoes para o gerar o relatório, mome, categoria ou data. Especifique o caminho e o nome do arquivo onde o relatório será salvo. Por exemplo, você pode usar o caminho absoluto da pasta + o nome do arquivo (ex: "/caminho/para/pasta/relatorio_despesas.txt").

Certifique-se de fechar o arquivo após salvar o relatório usando o método close.


## Considerações Finas - POO.

A Programação Orientada a Objetos (POO) é um padrão de desenvolvimento de software amplamente utilizado em muitas linguagens de programação atuais, como Java, C#, PHP, Python, C++, entre outras. A POO permite que você representar melhor o mundo real em seus programas, tornando-os mais fáceis de ler e entender. Além disso, pode ser mais rápido programar com POO e é mais fácil criar grandes programas. Os programas POO também são mais fáceis de modificar e manter. A POO traz grandes benefícios aos setores de tecnologia da informação das empresas na construção de seus sistemas e softwares ou hardwares. A orientação a objetos confere aos sistemas maior clareza, distribuição mais adequada de responsabilidades, encapsulamento de atributos e comportamentos, dentre muitas outras características. Isso torna o código mais seguro e confiável. No entanto, é importante notar que a programação orientada a objetos pode apresentar desafios e não basta apenas conhecer sua estrutura e conceitos para resolvê-los, é preciso dominá-los. Além disso, pode haver situações em que aplicar a POO pode não ser a melhor opção. É importante avaliar cuidadosamente cada caso para determinar se a POO é a abordagem mais adequada.

Fontes: https://www.devmedia.com.br/vantagens-e-desvantagens-da-poo/32655