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

# Código utilizando Herança / Polimorfismo.

// Classe despesas com atributos privados

public class Despesa {
    private double valor;
    private String data;
    private String descricao;

	// Metodo de sobreescrita do metodo construtor

    public Despesa(double valor, String data, String descricao) {
        this.valor = valor;
        this.data = data;
        this.descricao = descricao;
    }
       // Metodo de sobrecarga. Possui somente os atributos valor e descrição

    public Despesa(double valor, String descricao) {
        this.valor = valor;
        this.descricao = descricao;

    public double getValor() {
        return valor;
    }

    public String getData() {
        return data;
    }

    public String getDescricao() {
        return descricao;
    }
}

// classe filha utilizando o conceito de herança e polimorfismo

// Esta classe terá um comportamento diferente pois tem 

// o atributo restaurante, além de herdar os demais da classe mãe.

public class DespesaAlimentacao extends Despesa {
    private String restaurante;

    public DespesaAlimentacao(double valor, String data, String descricao, String restaurante) {
        super(valor, data, descricao);
        this.restaurante = restaurante;
    }

    public String getRestaurante() {
        return restaurante;
    }
}

// classe filha utilizando o conceito de herança e polimorfismo

// Esta classe terá um comportamento diferente pois tem 

// o atributo meioDeTransporte, além de herdar os demais da classe mãe.

public class DespesaTransporte extends Despesa {
    private String meioDeTransporte;

    public DespesaTransporte(double valor, String data, String descricao, String meioDeTransporte) {
        super(valor, data, descricao);
        this.meioDeTransporte = meioDeTransporte;
    }

    public String getMeioDeTransporte() {
        return meioDeTransporte;
    }
}

### Exemplo de uso

List<Despesa> despesas = new ArrayList<>();

despesas.add(new DespesaAlimentacao(50.0, "25/08/2023", "Jantar", "Pavan"));

despesas.add(new DespesaTransporte(10.0, "20/08/2023", "TCCC", "Ônibus"));

## Código em Linguagem Java - Sistema de Despesas.

# Analise das classes e metodos. 
Será apresentado a explicação de dos blocos do código.

//classes importadas 

import java.util.ArrayList;

import java.util.Date;

import java.util.List;

import java.util.Scanner;

//a classe possui uma lista despesa, tipoDespesa e usúario do tipo list que serão inializados no 

//costrutor da classe. A classe também possui um objeto chamado scanner, do tipo Scanner, que é 

//utilizado para fazer a leitura de dados do usuário a partir do teclado. Esse objeto é inicializado

//como um novo Scanner(System.in) no construtor da classe.

public class SistemaDespesa {

    private static final Usuario getUsuario = null;

    private static List<Despesa> despesas;

    private static List<TipoDeDespesa> tiposDeDespesa;

    private static List<Usuario> usuarios;

    private static Scanner scanner;


    public SistemaDespesa() {

        despesas = new ArrayList<>();

        tiposDeDespesa = new ArrayList<>();

        usuarios = new ArrayList<>();

        scanner = new Scanner(System.in);
    }

    public List<Despesa> getDespesas() {
        return despesas;
    }

    public List<TipoDeDespesa> getTiposDeDespesa() {
        return tiposDeDespesa;
    }

    public List<Usuario> getUsuarios() {
        return usuarios;
    }

    public void adicionarDespesa(Despesa despesa) {
        despesas.add(despesa);
    }

    public void removerDespesa(Despesa despesa) {
        despesas.remove(despesa);
    }

    public void listarDespesas() {
        for (Despesa despesa : despesas) {
            System.out.println(despesa);
        }
    }

    public void adicionarTipoDeDespesa(TipoDeDespesa tipoDeDespesa) {
        tiposDeDespesa.add(tipoDeDespesa);
    }

    public void removerTipoDeDespesa(TipoDeDespesa tipoDeDespesa) {
        tiposDeDespesa.remove(tipoDeDespesa);
    }

  
    public void adicionarUsuario(Usuario usuario) {
        usuarios.add(usuario);
    }

    public void removerUsuario(Usuario usuario) {
        usuarios.remove(usuario);
    }

    public static void listarUsuarios() {
        for (Usuario usuario : usuarios) {
            System.out.println(usuario);
        }
    }

    //criado metodo main  - 

    //exibe um menu com várias opções e permite ao usuário selecionar uma opção digitando o número

    //correspondente. O programa executa diferentes funções de acordo com a opção escolhida pelo usuário.

    //O programa começa criando um objeto Scanner para receber as entradas do usuário. Em seguida, há 

    //um loop while que continuará sendo executado até que a variável "sair" seja definida como "true".

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean sair = false;
        while (!sair) {
            System.out.println("Menu principal");
            System.out.println("1. Entrar despesa");
            System.out.println("2. Anotar pagamento");
            System.out.println("3. Listar despesas em aberto");
            System.out.println("4. Listar despesas pagas");
            System.out.println("5. Gerenciar tipos de despesa");
            System.out.println("6. Gerenciar usuários");
            System.out.println("7. Sair");
            int opcao = scanner.nextInt();
            switch (opcao) {
                case 1:
                    entrarDespesa();
                    break;
                case 2:
                    anotarPagamento();
                    break;
                case 3:
                    listarDespesasEmAberto();
                    break;
                case 4:
                    listarDespesasPagas();
                    break;
                case 5:
                    gerenciarTiposDeDespesa();
                    break;
                case 6:
                    gerenciarUsuarios();
                    break;
                case 7:
                    sair = true;
                    break;
                default:
                    System.out.println("Opção inválida!");
            }
        }
    }

 //criado os metodos para gerenciar as despesas - Ao entrar com um nova despesa, será criado um

 //novo objeto do tipo despesa que sera armazenado no ArrayList Despesa
   
 public static void entrarDespesa() {
        // Implementação do método de entrar despesa
        System.out.println("Entrar despesa");
        System.out.print("Valor: ");
        double valor = scanner.nextDouble();
        scanner.nextLine();
        System.out.print("Data de vencimento (dd/MM/yyyy): ");
        String dataDeVencimentoStr = scanner.nextLine();
        Date dataDeVencimento = Util.parseDate(dataDeVencimentoStr);
        System.out.print("Categoria: ");
        String categoria = scanner.nextLine();
        TipoDeDespesa tipoDeDespesa = getTipoDeDespesa(categoria);
        if (tipoDeDespesa == null) {
            tipoDeDespesa = new TipoDeDespesa(categoria);
            tiposDeDespesa.add(tipoDeDespesa);
        }
        Despesa despesa = new Despesa(valor, dataDeVencimento, tipoDeDespesa);
        despesas.add(despesa);
    }
private static TipoDeDespesa getTipoDeDespesa(String categoria) {
        return null;
    }

    ///////////////////////////////////////////////////////////////////////////////////////
    public static void anotarPagamento() {
        // Implementação do método de anotar pagamento
        System.out.println("Anotar pagamento");
         listarDespesasEmAberto();
        System.out.print("ID da despesa: ");
        int idDaDespesa = scanner.nextInt();
        Despesa despesa = getDespesa(idDaDespesa);
        if (despesa == null) {
            System.out.println("ID da despesa inválido!");
            return;
        }
        System.out.print("Valor do pagamento: ");
        double valorDoPagamento = scanner.nextDouble();
        scanner.nextLine();
        System.out.print("Data do pagamento (dd/MM/yyyy): ");
        String dataDoPagamentoStr = scanner.nextLine();
        Date dataDoPagamento = Util.parseDate(dataDoPagamentoStr);
        Pagamento pagamento = new Pagamento(valorDoPagamento, dataDoPagamento);
        despesa.anotarPagamento(pagamento);
    }
private static Despesa getDespesa(int idDaDespesa) {
        return null;
    }

    ////////////////////////////////////////////////////////////////////////////////////
    public static void listarDespesasEmAberto() {
        // Implementação do método de listar despesas em aberto
        System.out.println("Listar despesas em aberto");
          Despesa[] despendings;
        for (Despesa despesa : despendings) {
            if (!despesas.isPaga()) {
                System.out.println(despendings);
            }
        }
    }
//////////////////////////////////////////////////////////////////////////////////
    public static void listarDespesasPagas() {
        // Implementação do método de listar despesas pagas
        System.out.println("Listar despesas pagas");
           for (Despesa despensa : despesas) {
            if (despensa.isPaga()) {
                System.out.println(despesas);
            }
        }
    }
///////////////////////////////////////////////////////////////////////////////////