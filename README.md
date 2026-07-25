# basic_calculate
basic calculations with help of java using switchimport java.util.Scanner;

public class Basic_Calculater {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char choice;

        System.out.println("=== Basic Java Calculator ===");

        do {
            System.out.print("Enter first number: ");
            double num1 = sc.nextDouble();

            System.out.print("Enter operator (+, -, *, /): ");
            char operator = sc.next().charAt(0);

            System.out.print("Enter second number: ");
            double num2 = sc.nextDouble();

            double result;

            switch (operator) {
                case '+':
                    result = num1 + num2;
                    System.out.println("Result: " + result);
                    break;

                case '-':
                    result = num1 - num2;
                    System.out.println("Result: " + result);
                    break;

                case '*':
                    result = num1 * num2;
                    System.out.println("Result: " + result);
                    break;

                case '/':
                    if (num2 != 0) {
                        result = num1 / num2;
                        System.out.println("Result: " + result);
                    } else {
                        System.out.println("Error: Division by zero is not allowed.");
                    }
                    break;

                default:
                    System.out.println("Invalid operator. Please use +, -, * or /.");
            }

            System.out.print("Do you want to calculate again? (y/n): ");
            choice = sc.next().charAt(0);
            System.out.println();

        } while (choice == 'y' || choice == 'Y');

        System.out.println("Calculator closed.");
        sc.close();
    }
}
