import java.util.*;
public class Main
{
	public static void main(String[] args) {
		System.out.println("Hello World");
		System.out.println("Harish Mithran");
        System.out.println("Welcome to our ATM Application");
        Scanner sc=new Scanner(System.in);
        int pin=1234;
        int balance=10000; //initial balance
        int addamount=0;
        int takeamount=0;
        System.out.println("enter your pin number");
        int password=sc.nextInt();
        if(password==pin)
        {
            System.out.println("Enter your name");
            String name=sc.next();
            System.out.println("Welcome"+" "+name);
            while(true)
            {
                System.out.println("Press 1 to check your balance");
                System.out.println("Press 2 to add amount");
                System.out.println("Press 3 to take amount");
                System.out.println("Press 4 to print receipt");
                System.out.println("Press 5 to exit");
                int opt=sc.nextInt();
                switch (opt)
                {
                    case 1:
                        System.out.println("Your current balance is"+" "+balance);
                        break;
                    case 2:
                        System.out.println("How much amount did you want to add to your account");
                        addamount=sc.nextInt();
                        System.out.println("Successfully credited");
                        balance=addamount+balance;
                        break;
                    case 3:
                        System.out.println("How much do you want to take");
                        takeamount=sc.nextInt();
                        if(takeamount>balance)
                        {
                            System.out.println("Insufficient balance");
                            System.out.println("Try less than the available balance");
                        }
                        else
                        {
                            System.out.println("Your amount has been taken sucessfuly");
                            balance-=takeamount;

                        }
break;
                    case 4:
                        System.out.println("welcome to Harish Mithran bank");
                        System.out.println("Available balance is"+" "+balance);
                        System.out.println("Amount deposited"+" "+addamount);
                        System.out.println("Amount taken"+"  "+takeamount);
                        System.out.println("Thank you");
                        break;
                    default:
                        System.out.println("press the number below 5");
                        break;

}
if(opt==5)
                {
                    System.out.println("Thankyou");
                    break;

                }
            }

        }
        else{
            System.out.println("Wrong Pin number");
}

}
}
