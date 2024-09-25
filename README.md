# listaExercicios02Fabricio
//Marco Paulo Soares Rodrigues 924150819.
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

import java.util.Scanner; 

class Main {
  public static void main(String[] args) {
   
    Scanner entrada = new Scanner(System.in);
   
   // Um programa que calcule produto A (número real) por B (número inteiro),
  //ou seja, A*B, por intermédio de adições sucessivas.
  //Tanto A quanto B devem ser fornecidos pela pessoas utilizadora do programa.
   
    double numeroA;
    int numeroB;
    double produto;
    
    System.out.println("Digite o valor de A: ");
    numeroA = entrada.nextDouble();
    System.out.println("Digite o valor de B: ");
    numeroB = entrada.nextInt();
    
    produto = 0;
    
    while(produto != numeroA*numeroB){
      System.out.println(numeroA +"+"+ numeroA+ "="+ (numeroA+numeroA));
      produto = (numeroA+numeroA);
      
    }
    
    System.out.println(numeroA*numeroB);
    
    
   
  }
}

\\Projeto 03:

Double massa;
    Double perda = 0.25;
    Double tempo;
    Double temp;
    
    System.out.println("Informe o valor da massa a ser calculado:");
    massa = entrada.nextDouble();
    temp = massa;
    for(int tempo = 0;massa > 0.10; tempo +=30){System.out.println();}

    \\Projeto 04:
int produtoImpares = 1;
        int somaPares = 0;
        boolean encontrouImpar = false;

        while (true) {
            System.out.print("Digite um número inteiro positivo (ou um negativo para sair): ");
            int numero = entrada.nextInt();

            if (numero < 0) {
                break;
            }

            if (numero % 2 == 0) {
                somaPares += numero;
            } else {
                produtoImpares *= numero;
                encontrouImpar = true;
            }
        }

        if (encontrouImpar) {
            System.out.println("Produto dos números ímpares: " + produtoImpares);
        } else {
            System.out.println("Nenhum número ímpar foi inserido.");
        }
        System.out.println("Soma dos números pares: " + somaPares);
        
        entrada.close();

    \\Projeto 05:

        int idadeSuperior50 = 0;
        double somaAlturas = 0;
        int contIdade10a20 = 0;
        int contPesoInferior40 = 0;
        
        for (int i = 0; i < 10; i++) {
            System.out.print("Digite a idade da pessoa " + (i + 1) + ": ");
            int idade = scanner.nextInt();
            System.out.print("Digite a altura da pessoa " + (i + 1) + " (em metros): ");
            double altura = scanner.nextDouble();
            System.out.print("Digite o peso da pessoa " + (i + 1) + " (em quilos): ");
            double peso = scanner.nextDouble();

            if (idade > 50) {
                idadeSuperior50++;
            }

            if (idade >= 10 && idade <= 20) {
                somaAlturas += altura;
                contIdade10a20++;
            }

            if (peso < 40) {
                contPesoInferior40++;
            }
        }

        double mediaAlturas = (contIdade10a20 > 0) ? (somaAlturas / contIdade10a20) : 0;
        double porcentagemPesoInferior40 = (contPesoInferior40 / 10.0) * 100;

        System.out.println("Quantidade de pessoas com idade superior a 50 anos: " + idadeSuperior50);
        System.out.println("Média das alturas das pessoas com idade entre 10 e 20 anos: " + mediaAlturas);
        System.out.println("Porcentagem de pessoas com peso inferior a 40 quilos: " + porcentagemPesoInferior40 + "%");
        
        scanner.close();
    }

    \\Projeto 06:
        int totalKills = 0;
        int totalDeaths = 0;
        int totalAssists = 0;

        while (true) {
            System.out.print("Digite o número de kills na rodada: ");
            int kills = entrada.nextInt();
            System.out.print("Digite o número de deaths na rodada: ");
            int deaths = entrada.nextInt();
            System.out.print("Digite o número de assists na rodada: ");
            int assists = entrada.nextInt();

            totalKills += kills;
            totalDeaths += deaths;
            totalAssists += assists;

            if (kills <= 5) {
                System.out.println("noob");
            } else if (kills >= 20) {
                System.out.println("master");
            }

            if (deaths >= 20) {
                System.out.println("Houston, we have a problem");
            }

            if (assists >= 20) {
                System.out.println("team work");
            }

            System.out.print("Há um vencedor? (s/n): ");
            char vencedor = entrada.next().charAt(0);
            if (vencedor == 's' || vencedor == 'S') {
                break;
            }
        }

        System.out.println("Total de kills: " + totalKills);
        System.out.println("Total de deaths: " + totalDeaths);
        System.out.println("Total de assists: " + totalAssists);
        
        entrada.close();
    }

    \\Projeto 07:
        while (true) {
            System.out.println("Escolha uma forma geométrica:");
            System.out.println("1. Retângulo");
            System.out.println("2. Diagonal Superior Esquerda");
            System.out.println("3. Diagonal Superior Direita");
            System.out.println("4. Diagonal Inferior Esquerda");
            System.out.println("5. Diagonal Inferior Direita");
            System.out.println("6. Sair");
            System.out.print("Opção: ");
            int opcao = entrada.nextInt();

            if (opcao == 6) {
                break;
            }

            System.out.print("Informe a quantidade de colunas: ");
            int colunas = entrada.nextInt();
            int linhas = 5; // Definindo um número fixo de linhas

            switch (opcao) {
                case 1:
                    for (int i = 0; i < linhas; i++) {
                        for (int j = 0; j < colunas; j++) {
                            System.out.print("* ");
                        }
                        System.out.println();
                    }
                    break;
                case 2:
                    for (int i = 0; i < linhas; i++) {
                        for (int j = 0; j < colunas; j++) {
                            if (j <= i) {
                                System.out.print("* ");
                            } else {
                                System.out.print("  ");
                            }
                        }
                        System.out.println();
                    }
                    break;
                case 3:
                    for (int i = 0; i < linhas; i++) {
                        for (int j = 0; j < colunas; j++) {
                            if (j >= colunas - i - 1) {
                                System.out.print("* ");
                            } else {
                                System.out.print("  ");
                            }
                        }
                        System.out.println();
                    }
                    break;
                case 4:
                    for (int i = 0; i < linhas; i++) {
                        for (int j = 0; j < colunas; j++) {
                            if (j == 0 || i >= j) {
                                System.out.print("* ");
                            } else {
                                System.out.print("  ");
                            }
                        }
                        System.out.println();
                    }
                    break;
                case 5:
                    for (int i = 0; i < linhas; i++) {
                        for (int j = 0; j < colunas; j++) {
                            if (j == i) {
                                System.out.print("* ");
                            } else if (j < i) {
                                System.out.print("* ");
                            } else {
                                System.out.print("  ");
                            }
                        }
                        System.out.println();
                    }
                    break;
                default:
                    System.out.println("Opção inválida! Tente novamente.");
            }
            System.out.println();
        }

        entrada.close();
        */
    }
  
  
  }

