import java.util.Scanner;   //Needed for Scanner class
/**
 * This class is to show a Box, it's size and whether or not it will be filled
 * @author KareemWilliams
 */
public class isBox 
{
    static boolean isBox(int x)
    {
        Scanner keyboard = new Scanner(System.in);
        String  fill = "";
        boolean result = true;
        if(x <= 10 && x >= 4)
        {
            System.out.print("Do you want it filled? Please answer with a yes or no: ");
            fill = keyboard.nextLine();
            
            if(fill.equalsIgnoreCase("YES"))
            {
                for(int i = 1; i <= x; i++)
                {
                    for(int j = 1; j <= x; j++)
                    {
                        System.out.print("*");
                    }
                    System.out.println();
                }
            }
            else if(fill.equalsIgnoreCase("NO"))
            {
                for(int i = 1; i <= x; i++)
                {
                    for(int j= 1; j <= x; j++)
                    {
                        if(i == 1 || i == x || j == 1 || j == x)
                        {
                            System.out.print("*");
                        }
                        else
                        {
                            System.out.print(" ");
                        }
                    }
                    System.out.println();
                }
            }
            else
            {
                System.out.println("You did not input Yes or No. Try again.");
            }
        }
        else
        {
            System.out.println("The number you chose is too big/small. Try again.");
            result = false;
        }
        return result;
    }
}

