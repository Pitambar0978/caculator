# caculator

import java.util.Scanner;

class aaaa {

    // Method for Addition
    public static double add(double a, double b) {
        return a + b;
    }

    // Method for Subtraction
    public static double subtract(double a, double b) {
        return a - b;
    }

    // Method for Multiplication
    public static double multiply(double a, double b) {
        return a * b;
    }

    // Method for Division
    public static double divide(double a, double b) {
        if (b != 0) {
            return a / b;
        } else {
            System.out.println("Error: Division by zero is not allowed.");
            return 0;
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean continueCalc = true;

        while (continueCalc) {
            System.out.println("Select operation: +, -, *, /");
            char operation = scanner.next().charAt(0);

            System.out.println("Enter first number:");
            double num1 = scanner.nextDouble();

            System.out.println("Enter second number:");
            double num2 = scanner.nextDouble();

            double result = 0;
            switch (operation) {
                case '+':
                    result = add(num1, num2);
                    break;
                case '-':
                    result = subtract(num1, num2);
                    break;
                case '*':
                    result = multiply(num1, num2);
                    break;
                case '/':
                    result = divide(num1, num2);
                    break;
                default:
                    System.out.println("Invalid operation.");
                    continue;
            }

            System.out.println("Result: " + result);
            System.out.println("Do you want to perform another calculation? (yes/no)");
            String response = scanner.next();

            if (!response.equalsIgnoreCase("yes")) {
                continueCalc = false;
                System.out.println("Calculator exited.");
            }
        }

    }
}

<br>
In the above code  first it give the user to select the operation to perform.
<br> 
as the user  select the operation then it ask to give a first number and second number.
 <br>
 then it perform it task best on the user selected operations .
 <br> after that it ask  the user  taht do you want to perform the another calculation, if user choice yes the it continue again if  the user select no  then the calculator is exited.
 
