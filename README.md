package projeto1;

import java.util.Scanner;


public class Projeto1 {


    public static void main(String[] args) {
          Scanner scanner = new Scanner(System.in);
        
        System.out.print("Digite um numero inteiro positivo: ");
        int numero = scanner.nextInt();
        
        if (numero <= 1) {
            System.out.println("O numero nao e primo.");
            return;
        }
        
        boolean ehPrimo = true;
        
        for (int i = 2; i <= Math.sqrt(numero); i++) {
            if (numero % i == 0) {
                ehPrimo = false;
                break;
            }
        }
        
        if (ehPrimo) {
            System.out.println("O numero e primo.");
        } else {
            System.out.println("O numero não e primo.");
        }
        
        scanner.close();
    }
}
