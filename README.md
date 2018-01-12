import java.util.Scanner;
import java.io.InputStreamReader;

public class Deliverables {
public static void main (String [] args) {
	
	Scanner scnr = new Scanner(System.in);
	
	int userNum1 = 0; //userNum1 to be assigned by user
	int userNum2 = 0; //userNum2 to be assigned by user
	boolean isNum1Int; //used to validate user input
	boolean isNum2Int; // used to validate user input
	String num1AsString; // initialized to be able to convert int to String to use Char operations
	String num2AsString; // initialized to be able to convert int to String to use Char operations
	
	
		do { //loop used to validate user input will be an int
			System.out.println("Please enter a 3 digit number: ");
			if (scnr.hasNextInt()) {
				userNum1 = scnr.nextInt();
				isNum1Int = true;
			} else {
				System.out.println("Not a valid entry");
				System.out.println("");
				isNum1Int = false;
				scnr.next();
			}
		} while (!(isNum1Int));
		
	System.out.println("You entered: " + userNum1); // userNum1 to be displayed
	System.out.println("");
	
		do { // loop used to validate user input will be an int
			System.out.println("Please enter a 3 digit number: ");
			if (scnr.hasNextInt()) {
				userNum2= scnr.nextInt();
				isNum2Int = true;
			} else {
				System.out.println("Not a valid entry.");
				System.out.println("");
				isNum2Int = false;
				scnr.next();
			}
		} while (!(isNum2Int));
	
	System.out.println("You entered: " + userNum2); // userNum2 to be displayed
	System.out.println("");
	
	num1AsString = Integer.toString(userNum1); // convert int userNum1 to String
	num2AsString = Integer.toString(userNum2); // convert int userNum2 to String
	
	/*
	System.out.println("The following is now a string: " + num1AsString); // used to test conversion
	System.out.println("The following is now a string: " + num2AsString); // used to test conversion
	*/
	
	int sumChar0 = (num1AsString.charAt(0) + num2AsString.charAt(0)); //int sumChar0 is the sum of the 1st digit from both inputs
	int sumChar1 = (num1AsString.charAt(1) + num2AsString.charAt(1)); //int sumChar1 is the sum of the 2nd digit from both inputs
	int sumChar2 = (num1AsString.charAt(2) + num2AsString.charAt(2)); //int sumChar2 is the sum of the 3rd digit from both inputs
	
	if ((sumChar0 == sumChar1) && (sumChar0 == sumChar2)) { // If the sum of each individual digit is equal it prints, if not it prints false
		System.out.println("");
		System.out.println("True");
		}
		else {
			System.out.println("");
			System.out.println("False");
	}
}

}
