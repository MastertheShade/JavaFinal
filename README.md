/**
 * This is to show an X and it's size
 * @author KareemWilliams
 */
public class isX 
{
    static boolean isX(int x)
    {
        boolean result = true;
        if((x >= 4 && x <= 10))
        {
            for(int i = 0; i < x; i++)
            {
                for(int j = 0; j < x; j++)
                {
                    if(i == j || i + j == x - 1)
                    {
                    System.out.printf("*");
                    }
                    else
                    {
                        System.out.print(" ");
                    }
                }
                System.out.println();
            }
        }
        else if(x < 4 || x > 10)
        {
            System.out.println("Out of range. Please reenter: ");
            result = false;
        }
        return result;
    }
}
