import java.util.Scanner;

public class Calculator {

public static void main(String[] args) {

    Menu m = new Menu();
    m.getMenu();

  }    
}       



class Menu {    
    public void getMenu() {
        Scanner scan = new Scanner(System.in);

        System.out.println("Welcome to 00 Calculator menu, this calculator has the following options:");
        System.out.println("1 - Add " + "\n" + "2 - Subtract" + "\n"
                + "3 - Multiply" + "\n" + "4 - Divide" + "\n" 
                + "5 - Square" + "\n" + "6 - Modulus" + "\n" + "0 - Quit" );
        int optionInt = scan.nextInt();

         if (optionInt == 0) {
            System.out.println("Goodbye!"); 
            return;

        }else if (optionInt == 5) {
            System.out.println("Enter the first number :");
            double num1 = scan.nextDouble();
        }else {
            System.out.println("Enter the first number :");
            double num1 = scan.nextDouble();
            System.out.println("Enter the second number :");
            double num2 = scan.nextDouble();

            double result;
            Action option = new Action();


            switch (optionInt) {
            case 1:
                result = option.addValues(num1, num2);
                option.displayResult(result);
                break;
            case 2:
                result = option.subtractValues(num1, num2);
                option.displayResult(result);
                break;
            case 3:
                result = option.multiplyValues(num1, num2);
                option.displayResult(result);
                break;  
            case 4:
                result = option.divideValues(num1, num2);
                option.displayResult(result);
                break;  
            case 5:
                result = option.squareValues(num1, num2);
                option.displayResult(result);
                break;  
            case 6:
                result = option.modulusValues(num1, num2);
                option.displayResult(result);
                break;          
            default:
                System.out.println("You entered an incorrect option.  Goodbye.");
           } 
        }   
    }
}


class Action {

public double divideValues(double d1, double d2) {
    double result = d1 / d2;
    return result;
}

public double multiplyValues(double d1, double d2) {
    double result = d1 + d2;
    return result;
}

public double subtractValues(double d1, double d2) {
    double result = d1 - d2;
    return result;
}

public double addValues(double d1, double d2) {
    double result = d1 + d2;
    return result;
}

public double squareValues(double d1, double d2) {
    double result = Math.pow(d1, 2);
    return result;
}

public double modulusValues(double d1, double d2) {
    double result = d1 % d2;
    return result;
}

public void displayResult(double result) {
    System.out.println("The answer is " + result);
 }

}
