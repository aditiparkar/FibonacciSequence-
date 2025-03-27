import java.util.Scanner;

public class FibonacciSequence {
    
    // Method to generate and print Fibonacci sequence up to a specified limit
    public static void generateFibonacci(int limit) {
        int a = 0, b = 1, c;
        
        // Printing the first two numbers in the sequence
        System.out.print("Fibonacci sequence up to " + limit + ": ");
        
        // Handling the special case for when the limit is 0 or 1
        if (limit >= 0) {
            System.out.print(a + " ");
        }
        if (limit >= 1) {
            System.out.print(b + " ");
        }

        // Generating the Fibonacci sequence
        while (true) {
            c = a + b;
            if (c > limit) {
                break;
            }
            System.out.print(c + " ");
            a = b;
            b = c;
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Prompting the user for the upper limit
        System.out.print("Enter the upper limit for Fibonacci sequence: ");
        int limit = scanner.nextInt();
        
        // Generate and print the Fibonacci sequence
        generateFibonacci(limit);
        
        scanner.close();
    }
}
