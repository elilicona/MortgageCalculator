package Main.java;
import java.text.NumberFormat;
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		
		double PERCENT = 100;
		double MONTH = 12;
	
		
		Scanner scan = new Scanner(System.in);
		
		System.out.println("Principal: "); //M
		double principal = scan.nextDouble();
		
		System.out.println("Annual Interest Rate: ");  //R
		double annualInterestRate = scan.nextDouble();
		
		System.out.println("Period(Years)");
		int period = scan.nextInt();
		
		float monthlyRate = (float) (annualInterestRate / PERCENT / MONTH);
		int numberOfPayments = (int) (period * MONTH);
		
		double calcPow = Math.pow(1 + monthlyRate, numberOfPayments);
		
		double monthlyPayment = principal * (monthlyRate * calcPow / (calcPow - 1));
		
		String monthlyPaymentF = NumberFormat.getCurrencyInstance().format(monthlyPayment);
		
		System.out.println("Your monthly Payment rate is: " + monthlyPaymentF);

		
		
		
		
		
		
		
		

		
			
		
		
		

		
		




		
		
		
		
		
		
	}

}
