# Scientific-Calculator---Java
# Mini - Project: Scientific calculator using java for beginners
import java.util.Scanner;//Import the Java.util package

public class ScientificCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Scientific Calculator");
        System.out.println("---------------------");

        while (true) {
            System.out.println("Choose an operation:");
            System.out.println("1. Addition (+)");
            System.out.println("2. Subtraction (-)");
            System.out.println("3. Multiplication (*)");
            System.out.println("4. Division (/)");
            System.out.println("5. Sine (sin)");
            System.out.println("6. Cosine (cos)");
            System.out.println("7. Tangent (tan)");
            System.out.println("8. Square Root (sqrt)");
            System.out.println("9. Logarithm (log)");
            System.out.println("0. Exit");

            int choice = scanner.nextInt();
            double result = 0;

            if (choice == 0) {
                System.out.println("Exiting...");
                break;
            }

            switch (choice) {
                case 1:
                    System.out.println("Enter first number:");
                    double num1 = scanner.nextDouble();
                    System.out.println("Enter second number:");
                    double num2 = scanner.nextDouble();
                    result = num1 + num2;
                    break;
                case 2:
                    System.out.println("Enter first number:");
                    num1 = scanner.nextDouble();
                    System.out.println("Enter second number:");
                    num2 = scanner.nextDouble();
                    result = num1 - num2;
                    break;
                case 3:
                    System.out.println("Enter first number:");
                    num1 = scanner.nextDouble();
                    System.out.println("Enter second number:");
                    num2 = scanner.nextDouble();
                    result = num1 * num2;
                    break;
                case 4:
                    System.out.println("Enter first number:");
                    num1 = scanner.nextDouble();
                    System.out.println("Enter second number:");
                    num2 = scanner.nextDouble();
                    if (num2 != 0) {
                        result = num1 / num2;
                    } else {
                        System.out.println("Error! Division by zero.");
                    }
                    break;
                case 5:
                    System.out.println("Enter the angle in degrees:");
                    double angle = scanner.nextDouble();
                    result = Math.sin(Math.toRadians(angle));
                    break;
                case 6:
                    System.out.println("Enter the angle in degrees:");
                    angle = scanner.nextDouble();
                    result = Math.cos(Math.toRadians(angle));
                    break;
                case 7:
                    System.out.println("Enter the angle in degrees:");
                    angle = scanner.nextDouble();
                    result = Math.tan(Math.toRadians(angle));
                    break;
                case 8:
                    System.out.println("Enter the number:");
                    double number = scanner.nextDouble();
                    result = Math.sqrt(number);
                    break;
                case 9:
                    System.out.println("Enter the number:");
                    number = scanner.nextDouble();
                    result = Math.log10(number);
                    break;
                default:
                    System.out.println("Invalid choice! Please choose a valid operation.");
                    continue;
            }

            System.out.println("Result: " + result);
        }

        scanner.close();
    }
}
