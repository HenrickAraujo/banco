public class ContaCorrente {
    public static int qtdContas;
    private double valor, saldo, renda;
    private int numeroConta, idade, agencia;
    private String nome, endereco, profissao;
    private long cpf;

    public ContaCorrente(String nome, String endereco, long cpf, String profissao, double renda, int agencia) {
        this.nome = nome;
        this.endereco = endereco;
        this.cpf = cpf;
        this.profissao = profissao;
        this.agencia = agencia;
        this.renda = renda;
        this.saldo = saldo;
        this.valor = valor;

        qtdContas++;
        numeroConta = qtdContas;
    }

    public int getNumConta() {
        return numeroConta;
    }

    public void sacar(double valor) {
        if (saldo < valor) {
            System.out.println("Saldo insuficiente para saque.");
        } else {
            saldo -= valor;
            System.out.println("Saque realizado!");
        }
    }

    public void depositar(double valor) {
        if (valor > 0) {
            saldo += valor;
            System.out.println("Saldo: R$ " + saldo);
        } else {
            System.out.println("Valor de dep�sito inv�lido!");
        }
    }

    public String informacoes() {
        return("" +
                "Nome: " + nome +
                "\nN�mero da Conta: " + numeroConta +
                "\nSaldo: R$ " + saldo +
                "\nEndere�o: " + endereco +
                "\nCPF: R$ " + cpf +
                "\nProfiss�o: R$ " + profissao +
                "\nRenda: R$ " + renda );
    }
}



