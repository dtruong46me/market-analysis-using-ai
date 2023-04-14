# Problem Tasks
- [x] 2.2.1 HelloWorld.java
- [x] 2.2.2 FirstDialog.java
- [x] 2.2.3 HelloNameDialog.java
- [x] 2.2.4 ShowTwoNumbers.java
- [x] 2.2.5 CalculateTwoNums.java
- [ ] 2.2.6 
- [x] 6.1 ChoosingOption.java
- [x] 6.2 InputFromKeyboard.java
- [x] 6.3 DisplayTriangle.java


# Solutions Detail

## 2.2.1 HelloWorld.java
Write, compile the first Java application

    package lab1;
    public class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello World");
        }
    }

## 2.2.2 FirstDialog.java
Write, compile the first dialog Java program

    package lab1;

    import javax.swing.JOptionPane;

    public class FirstDialog {
        public static void main(String[] args) {
            JOptionPane.showMessageDialog(null, "Hello world! How are you?");
            System.exit(0);
        }
    }


## 2.2.3 HelloNameDialog.java
Write, compile the first dialog Java application

    package lab1;

    import javax.swing.JOptionPane;

    public class HelloNameDialog {
        public static void main(String[] args) {
            String result;
            result = JOptionPane.showInputDialog("Please enter your name: ");
            JOptionPane.showMessageDialog(null, "Hi "+result+"!");
            System.exit(0);
        }
    }

## 2.2.4 ShowTwoNumbers.java
Write, compile, and run the following example

    package lab1;

    import javax.swing.JOptionPane;

    public class ShowTwoNumbers {
        public static void main(String[] args) {
            String strNum1, strNum2;
            String strNotification = "You're just entered: ";

            
            strNum1 = JOptionPane.showInputDialog(null, 
                "Please input the first number: ", "Input the first number", 
                JOptionPane.INFORMATION_MESSAGE);
            strNotification += strNum1 + " and ";

            strNum2 = JOptionPane.showInputDialog(null, 
                "Please input the second number: ", "Input the second number",
                JOptionPane.INFORMATION_MESSAGE);
            strNotification += strNum2;

            JOptionPane.showMessageDialog(null, strNotification,
                "Show two numbers", JOptionPane.INFORMATION_MESSAGE);

            System.exit(0);
        }
    }

## 2.2.5 CalculateTwoNums.java
Write a program to calculate sum, difference, product and quotient of 2 double numbers which are entered by users.

    package lab1;

    import javax.swing.JOptionPane;

    public class CalculateTwoNums {
        public static void main(String[] args) {
            String strNum1, strNum2;
            double sum, diff, prod, quot;
            String msg1, msg2;

            strNum1 = JOptionPane.showInputDialog(null,
                "Enter the first number: ", "Input the first number",JOptionPane.INFORMATION_MESSAGE);

            strNum2 = JOptionPane.showInputDialog(null,
                "Enter the first number: ", "Input the first number",JOptionPane.INFORMATION_MESSAGE);

            double num1 = Double.parseDouble(strNum1);
            double num2 = Double.parseDouble(strNum2);
            
            if (num2 == 0) {
                sum = num1 + num2;
                diff = num1 - num2;
                prod = num1 * num2;
                msg2 = "Sum = " + sum + "\n" + 
                    "Difference = " + diff + "\n" + 
                    "Product = " + prod + "\n" + 
                    "The division equals to 0";

                    JOptionPane.showMessageDialog(null, msg2, 
                    "Calculate two numbers", JOptionPane.INFORMATION_MESSAGE);
        
            } else {
                sum = num1 + num2;
                diff = num1 - num2;
                prod = num1 * num2;
                quot = num1 / num2;
        
                msg1 = "Sum = " + sum + "\n" +
                    "Difference = " + diff + "\n" +
                    "Product = " + prod + "\n" + 
                    "Quotient = " + quot + "\n";
        
                JOptionPane.showMessageDialog(null, msg1, 
                    "Calculate two numbers", JOptionPane.INFORMATION_MESSAGE);
        
            }
            System.exit(0);
        }
    }

## 2.2.6

## 6.1 ChoosingOption.java
Write, compile and run the *ChoosingOption program:*

    package lab1;

    import javax.swing.JOptionPane;

    public class ChoosingOption {
        public static void main(String[] args) {
            int option = JOptionPane.showConfirmDialog(null, 
                "Do you want to change to che first class ticket?");
            
            JOptionPane.showMessageDialog(null, "You've chosen: " + (option==JOptionPane.YES_OPTION ? "Yes" : "No"));

            System.exit(0);
        }
    }

## 6.2 InputFromKeyboard.java
Write a program for input/output from keyboard

    package lab1;

    import java.util.Scanner;

    public class InputFromKeyboard {
        public static void main(String[] args) {
            Scanner keyboard = new Scanner(System.in);

            System.out.println("What's your name?");
            String strName = keyboard.nextLine();

            System.out.println("How old are you?");
            int iAge = keyboard.nextInt();

            System.out.println("How tall are you (m)?");
            double dHeight = keyboard.nextDouble();

            System.out.println("Mr/Mrs/Ms." + strName +
                    ", " + iAge + " years old. " + 
                    "Your height is " + dHeight + ".");
            
            keyboard.close();
        }
    }

## 6.3 DipsplayTriangle.java
Write a program to display with a height of `n` stars ("`*`"), `n` is entered by users.

E.g. n = 5

         *
        ***
       *****
      *******
     *********
    *********** 

Here is the solution in Java

    package lab1;

    import java.util.Scanner;

    public class DisplayTriangle {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            
            int n = sc.nextInt();

            System.out.println("");

            for (int i = 1; i < n+1; i++) {
                for (int j = 0; j < n-i; j++) {
                    System.out.print(" ");
                }
                for (int k = 0; k < 2*i-1; k++) {
                    System.out.print("*");
                }
                System.out.println("");
                // for (int k = )
            }

            sc.close();
        }
    }