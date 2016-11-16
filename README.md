package MidTerm;
import java.util.Scanner;
import java.io.PrintWriter;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileWriter;
import java.io.IOException;

/**
 * This is to combine and showcase the different classes representing each shape
 * @author KareemWilliams
**/
public class checkIsShape 
{
    public checkIsShape()
    {
        checkIsShape();
    }
    void checkIsShape()
    {
        Scanner     keyboard = new Scanner(System.in);  //Scanner class to receive input from the keyboard
        String      shape = ""; //to get the shape user inputs
        int         rows;       //to get the amount of rows
        int         str = 1;   //the size of each shape
        double      size = 1;
        String      fileName;
        boolean     endLoop = true;
        
        /*System.out.print("Enter the filename: ");
        fileName = keyboard.nextLine();
        FileWriter fwriter = new FileWriter(fileName, true);
        PrintWriter outputFile = new PrintWriter(fwriter);
        File myFile = new File(fileName);
        Scanner inputFile = new Scanner(myFile);*/

        while(endLoop)
        {
            System.out.println("****************************************************************");
            System.out.println("*********** X, Circle, Box, X in a box.*************************");
            System.out.println("******** Enter one of the options you would like to see ********");
            System.out.println("******** or write done to end: ********");
            shape = keyboard.nextLine().toUpperCase();

            if(!shape.equals("DONE"))
            {
                switch (shape)
                {
                    case "X":   //For the shape X
                    System.out.print("How many rows will you like to see? Please choose between 4 and 10: ");
                    rows = keyboard.nextInt();
                                        
                    isX.isX(rows);
                               
                    break;

                    case "CIRCLE": //For the shape Circle
                    System.out.print("How large do you want your number? Pick a number up to 50: ");
                    size = keyboard.nextDouble();
                    
                    isCircle.isCircle(size);
                    
                    break;

                    case "BOX": //For the shape Box
                        System.out.print("How many rows/columns would you like? Please choose between 4 and 10: ");
                        rows = keyboard.nextInt();
                        
                            isBox.isBox(rows);
                                                
                    break;

                    case "X IN A BOX":
                    
                        System.out.print("How many rows/columns would you like? Please choose between 4 and 10: ");
                        str = keyboard.nextInt();
                        
                            isXInBox.isXInBox(str);
                    
                    break;

                    default:
                    {
                        System.out.println(shape+ " did not match the options given.");
                    }
                    break;
                }
            }
            else
            {
                System.out.println("Good bye.....");
                endLoop = false;
            }
        }
        //inputFile.close();
    }
}
