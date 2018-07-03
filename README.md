# ship
**Java College Level Project

package ship;
import java.util.*;

public class ShipDemo 
{
	public static void main(String[] args) 
	{
		Scanner input = new Scanner(System.in);
		
		//Variables
		int choice = 0;
		String name; //ship name
		String year; //year
		int pass; //passengers
		int tons; //tons
		menu();
		choice = input.nextInt();		
		
		while (choice != -1)
		{
			if (choice > 0 && choice < 4)
			{
				
				switch (choice)
				{
				case 1:
					System.out.println("Enter the ship's name:  ");
					name = input.nextLine();	
					input.nextLine();
					System.out.println("Enter the year the ship was built: ");
					year = input.nextLine();
					Ship myShip = new Ship(name, year);
					System.out.println("The ship's info is: " + myShip.toString());
					break;
				case 2:
					System.out.println("Enter the ship's name:  ");
					name = input.nextLine();	
					input.nextLine();
					System.out.println("Enter the year the ship was built: ");
					year = input.nextLine();
					System.out.println("Enter the # of passengers on the cruise ship: ");
					pass = Integer.parseInt(input.nextLine());
					CruiseShip myCruiseShip = new CruiseShip (pass, name, year);
					System.out.println("The cruise ship's info is: " + myCruiseShip.toString());
					break;
				case 3:
					System.out.println("Enter the ship's name:  ");
					name = input.nextLine();	
					input.nextLine();
					System.out.println("Enter the year the ship was built: ");
					year = input.nextLine();
					System.out.println("Enter the # of tons on the ship: ");
					tons = Integer.parseInt(input.nextLine());
					CargoShip myCargoShip = new CargoShip (tons, name, year);
					System.out.println("The cargo ship's info is: " + myCargoShip.toString());
					break;
				}//end switch
			}//end if
			else
				System.out.println("Incorrect entry.");
			menu();
			choice = input.nextInt();
		}//end while
	}//end main
	
public static void menu()
{
	System.out.println("Enter 1 for a Ship. ");
	System.out.println("Enter 2 for a Cruise Ship. ");
	System.out.println("Enter 3 for a Cargo Ship.");
	System.out.println("Enter -1 to Exit.");
	System.out.println("Please enter your choice: ");
}
}//end class
