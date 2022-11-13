# Manual-Vetores
Trabalhando Vetores

## EXEMPLO 01 - Criando um vertor n posições, adicionando valores e tirando media.

package program;

import java.time.LocalDate;
import java.util.Locale;
import java.util.Scanner;

public class Vetores {

	public static void main(String[] args) {
		
		//Armazenar valores
		Locale.setDefault(Locale.US);
		Scanner sc = new Scanner(System.in);
		
		System.out.print("Digite valor de n: ");
		int n = sc.nextInt();
		double[] vect = new double[n];
		
		for (int i = 0; i < n; i++) {
			System.out.print("Digite valor da posicao " + i + ":");
			vect[i] = sc.nextDouble();
			
		}
		double sum = 0.0;
		
		for(int i = 0; i < n; i++) {
			sum += vect[i];
			
		}
		double avg = sum / n;
		
		System.out.printf("Average height: %.2f", avg);
		System.out.print("\nAverage height: " + String.format("%.2f", avg));
		sc.close();

	}

}
