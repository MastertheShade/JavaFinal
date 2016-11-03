import java.util.Scanner;   //Needed for Scanner class
/**
 * This class is to show a Box and it's size
 * @author KareemWilliams
 */
public class isBox 
{
    static void isBox(int filledRows)
    {
        if(filledRows < 4 || filledRows > 10)
        {
            System.out.println("The number you chose is too big/small. Try again.");
        }
        else
        {
            for(int i = 1; i <= filledRows; i++)
            {
                for(int j = 1; j <= filledRows; j++)
                {
                    System.out.print("*");
                }
                System.out.println();
            }
        }
    }
    static void isBox(double unfilledRows)
    {
        if(unfilledRows < 4 || unfilledRows > 10)
        {
            System.out.println("The number you chose is too big/small. Try again.");
        }
        else
        {
            for(int i = 1; i <= unfilledRows; i++)
            {
                for(int j= 1; j <= unfilledRows; j++)
                {
                    if(i == 1 || i == unfilledRows || j == 1 || j == unfilledRows)
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
    }
}
