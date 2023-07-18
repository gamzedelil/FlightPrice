# FlightPrice

package flightprice;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		double distance, perkm = 0.10, newtotal,agesale,typesale;
		int age,type;
		
		Scanner inp = new Scanner(System.in);
		
		System.out.println("Enter the distance(KM):");
		distance = inp.nextDouble();
		
		System.out.println("Enter the age:");
		age = inp.nextInt();
		
		System.out.println("Enter the flight type: (One way:1 or Round trip:2) ");
		type = inp.nextInt();

		double total = (distance * perkm);
		System.out.println("Total is:" +total);
	
	 
		switch (type) {
		
		case 2:

			if (age<12) {
				agesale = total * 0.5 ;
				System.out.println("Age sale is:" +agesale);
				newtotal = (total - agesale);
				System.out.println("New total:" +newtotal);
			    typesale = newtotal * 0.2 ;
			    System.out.println("Type sale is:" +typesale);
			    newtotal = (total - typesale);
			    System.out.println("New total:" +newtotal);
			}
			else if (age >=12 && age <= 24) {
				agesale = total * 0.1 ;
				System.out.println("Age sale is:" +agesale);
				newtotal = (total - agesale);
				System.out.println("New total:" +newtotal);
				typesale = newtotal * 0.2 ;
			    System.out.println("Type sale is:" +typesale);
			    newtotal = (total - typesale);
			    System.out.println("New total:" +newtotal);
			}
			
			else if (age>65) {
				agesale = total * 0.3 ;
				System.out.println("Age sale is:" +agesale);
				newtotal = (total - agesale);
				System.out.println("New total:" +newtotal);
				typesale = newtotal * 0.2 ;
			    System.out.println("Type sale is:" +typesale);
			    newtotal = (total - typesale);
			    System.out.println("New total:" +newtotal);
			}
			    break;

		case 1: 
			total = total ; 
			break;	
			
		default: System.out.println("Incorrect type choice.Try again.");
		}
		
		if (distance < 0 || age < 0 ) {
			System.out.println("Incorrect distance. Try again.");
		}
	}
}
