import java.util.*;

public class EarningCalculator
{
  public static void main(String[] args)
  {
    double wage;
    double wage2;
    double wageTotal;
    double wage2Total;
    int hours;
    Scanner userInput = new Scanner(System.in); 
    
    System.out.println("Please input your first wage.");
    wage = userInput.nextDouble();
    
    System.out.println("Please input your secondary wage.");
    wage2 = userInput.nextDouble();
    
    System.out.println("Please enter the number of hours worked a week.");
    hours = userInput.nextInt();
    wageTotal = wage*(hours*24);
    wage2Total = wage2*(hours*24);
    System.out.println("Over a six month period, you would have made $" + wageTotal + " with your first job." +
                      " With your second job, you would have made $" + wage2Total + ".");
    if( wageTotal > wage2Total)
    {
      System.out.println("You will make " + (wageTotal - wage2Total) + " more in 6 months with your first job, than your second job.");
      System.out.println("That is approximately an extra $" + ((wage - wage2)*hours) + " a week in your pocket.");
    }else{
      System.out.println("You will make " + (wage2Total - wageTotal) + " more in 6 months with your second job, than your first job.");
      System.out.println("That is approximately an extra $" + ((wage2 - wage)*hours) + " a week in your pocket.");
    }
        
                      
  }
}
