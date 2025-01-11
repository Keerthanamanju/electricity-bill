import java.util.Scanner;
public class Hello {
public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);



        // Input: Units consumed
        System.out.print("Enter the number of units consumed: ");
        double units = scanner.nextDouble();

        double billAmount;

        // Electricity bill calculation based on slab rates
        if (units <= 100) {



            billAmount = units * 1.5; // Rate for first 100 units
        } else if (units <= 300) {
            billAmount = (100 * 1.5) + ((units - 100) * 2.5); // Next 200 units
        } else {
            billAmount = (100 * 1.5) + (200 * 2.5) + ((units - 300) * 4); // Beyond 300 units
        }

        // Add fixed charge
        double fixedCharge = 50;
        billAmount += fixedCharge;

        // Output: Total bill amount
        System.out.println("Electricity Bill: ₹" + billAmount);

        scanner.close();
    }
}

OUTPUT:




PS C:\Users\MY\OneDrive\Pictures\Documents\java emc 1>  
Enter the number of units consumed: 250
Electricity Bill: ?575.0
PS C:\Users\MY\OneDrive\Pictures\Documents\java emc 1> 


