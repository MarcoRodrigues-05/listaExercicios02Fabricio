# listaExercicios02Fabricio
2º lista de exercícios do professor Fabrício

\\Projeto 01:

import java.util.Scanner;
class Main {
  public static void main(String[] args) {
    
    Scanner entrada = new Scanner(System.in);
    
        int valorInicial;
    
    System.out.println("informe o valor inicial: ");
    valorInicial = entrada.nextInt();
    
    for (int i=0; i<100;i++){
      valorInicial = valorInicial+1;
      System.out.println(i+1 + "->" + valorInicial);
            }
  }
}

\\Projeto 02:
