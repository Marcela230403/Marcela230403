package Projeto;

//Classe base
public class Produto {
 private String nome;
 private double preco;

 public Produto(String nome, double preco) {
     this.nome = nome;
     this.preco = preco;
 }

 public String getNome() {
     return nome;
 }

 public double getPreco() {
     return preco;
 }

 public void exibirDetalhes() {
     System.out.println("Nome: " + nome + ", Preço: " + preco);
 }
}

//Televisor
public class Televisor extends Produto {
 private int tamanhoTela;

 public Televisor(String nome, double preco, int tamanhoTela) {
     super(nome, preco);
     this.tamanhoTela = tamanhoTela;
 }


 public void exibirDetalhes() {
     super.exibirDetalhes();
     System.out.println("Tamanho da tela: " + tamanhoTela + " polegadas");
 }
}

//Geladeira
public class Geladeira extends Produto {
 private int capacidade;

 public Geladeira(String nome, double preco, int capacidade) {
     super(nome, preco);
     this.capacidade = capacidade;
 }

 
 public void exibirDetalhes() {
     super.exibirDetalhes();
     System.out.println("Capacidade: " + capacidade + " litros");
 }
}

//Fogão
public class Fogão extends Produto {
 private int quantidadeBocas;

 public Fogão(String nome, double preco, int quantidadeBocas) {
     super(nome, preco);
     this.quantidadeBocas = quantidadeBocas;
 }

 public void exibirDetalhes() {
     super.exibirDetalhes();
     System.out.println("Quantidade de bocas: " + quantidadeBocas);
 }
}

//Automóvel
public class Automovel extends Produto {
 private String modelo;

 public Automovel(String nome, double preco, String modelo) {
     super(nome, preco);
     this.modelo = modelo;
 }


 public void exibirDetalhes() {
     super.exibirDetalhes();
     System.out.println("Modelo: " + modelo);
 }
}

//TelevisorComDVD (Herda de Televisor)
public class TelevisorComDVD extends Televisor {
 private boolean temDVD;

 public TelevisorComDVD(String nome, double preco, int tamanhoTela, boolean temDVD) {
     super(nome, preco, tamanhoTela);
     this.temDVD = temDVD;
 }


 public void exibirDetalhes() {
     super.exibirDetalhes();
     System.out.println("Inclui DVD: " + (temDVD ? "Sim" : "Não"));
 }
}

public class TestaProdutos {
    public static void main(String[] args) {
        Produto televisor = new Televisor("LG Ultra HD", 2500.00, 55);
        Produto geladeira = new Geladeira("Brastemp Frost Free", 1800.00, 500);
        Produto fogao = new Fogão("Consul 5 bocas", 1200.00, 5);
        Produto automovel = new Automovel("Honda Civic", 90000.00, "EX");
        Produto televisorComDVD = new TelevisorComDVD("Samsung 4K", 3000.00, 65, true);

        televisor.exibirDetalhes();
        geladeira.exibirDetalhes();
        fogao.exibirDetalhes();
        automovel.exibirDetalhes();
        televisorComDVD.exibirDetalhes();
    }
}
