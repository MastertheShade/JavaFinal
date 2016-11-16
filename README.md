package MidTerm;
import java.util.Scanner;
/**
 * This class is to show a Circle and and the user will input the size
 * @author KareemWilliams
 */

public class isCircle
{
    static boolean isCircle(double r)
    {
        Scanner keyboard = new Scanner(System.in);
        double r_in  = r - 1;
        double r_out = r + 1;
        boolean result = true;

        for(double i = r; i >= -r; --i )
        {
            for (double j = -r; j < r_out; j += 0.5 )
            {
                double value = i * i + j * j; 
                if ( value >= r_in * r_in && value <= r_out * r_out )
                {
                    System.out.print("*");
                }
                else
                {
                    System.out.print(" ");
                }
            }
        }
        return false;
    }
}
