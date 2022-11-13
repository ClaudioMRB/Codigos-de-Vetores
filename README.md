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

## EXEMPLO 02 - Manipulação de vetor de elementos tipo referência (classe) parte 1/2
package program;

import java.util.Locale;
import java.util.Scanner;

import entities.Products;

public class Vetores {

	public static void main(String[] args) {
		
		//Manipulação de vetor de elementos tipo referência (classe)
		Locale.setDefault(Locale.US);
		Scanner sc = new Scanner(System.in);
		
		System.out.println("Digite quantos produtos sera cadastrado");
		int n = sc.nextInt();
		///vetor do tipo referencia
		Products[] vect = new Products[n];
		
		for(int i = 0; i < vect.length; i++) {
			
			System.out.println("Digite nome do produto " + (i+1));
			sc.nextLine();
			String name = sc.nextLine();
			System.out.println("Digite preco do produto " + (i+1));
			double price = sc.nextDouble();
			vect[i] = new Products(name, price);
		}

		double sum = 0.0;
		for(int i = 0; i < vect.length; i++) {
			sum += vect[i].getPrice();
			
		}
		double avg = sum / n;
		System.out.println("Average price = " + String.format("%.2f", avg));
		
		sc.close();

	}

}
## EXEMPLO 02 - Manipulação de vetor de elementos tipo referência (classe) parte 2/2
package entities;

public class Products {

	private String name;
	private double price;
	
	
	public Products(String name, double price) {
		this.name = name;
		this.price = price;
	}


	public String getName() {
		return name;
	}


	public void setName(String name) {
		this.name = name;
	}


	public double getPrice() {
		return price;
	}


	public void setPrice(double price) {
		this.price = price;
	}
	
	
	
	
}


