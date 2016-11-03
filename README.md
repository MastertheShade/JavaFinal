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
    public checkIsShape() throws IOException
    {
        checkIsShape();
    }
    void checkIsShape() throws FileNotFoundException, IOException
    {
        Scanner     keyboard = new Scanner(System.in);  //Scanner class to receive input from the keyboard
        String      shape = ""; //to get the shape user inputs
        int         rows;       //to get the amount of rows
        String      size = "";  //the size of each shape
        String      fill = "";  //To find out if user wants the shape filled
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
                    System.out.print("How large do you want the Circle? Please choose small, medium, or large: ");
                    size = keyboard.nextLine().toLowerCase();
                    if(size.equals("small"))
                    {
                        System.out.print("Would you like your Circle filled in? Please answer with a Yes or No: ");
                        fill = keyboard.nextLine().toUpperCase();
                        if(fill.equals("YES"))
                        {
                            System.out.println("You chose a "+ size +" Circle that will be filled in\n");
                        }
                        else if(fill.equals("NO"))
                        {
                            System.out.println("You chose a "+ size +" Circle\n");
                        }
                        else if(!fill.equals("YES") || !fill.equals("NO"))
                        {
                            System.out.println("You did not pick the appropriate option, try again.");
                        }
                    }
                    else if(size.equals("medium"))
                    {
                        System.out.print("Would you like your Circle filled in? Please answer with a Yes or No: ");
                        fill = keyboard.nextLine().toUpperCase();
                        if(fill.equals("YES"))
                        {
                            System.out.println("You chose a "+ size +" Circle that will be filled in\n");
                        }
                        else if(fill.equals("NO"))
                        {
                            System.out.println("You chose a "+ size +" Circle\n");
                        }
                        else if(!fill.equals("YES") || !fill.equals("NO"))
                        {
                            System.out.println("You did not pick the appropriate option, try again.");
                        }
                    }
                    else if(size.equals("large"))
                    {
                        System.out.print("Would you like your Circle filled in? Please answer with a Yes or No: ");
                        fill = keyboard.nextLine().toUpperCase();
                        if(fill.equals("YES"))
                        {
                            System.out.println("You chose a "+ size +" Circle that will be filled in\n");
                        }
                        else if(fill.equals("NO"))
                        {
                            System.out.println("You chose a "+ size +" Circle\n");
                        }
                        else if(!fill.equals("YES") || !fill.equals("NO"))
                        {
                            System.out.println("You did not pick the appropriate option, try again.");
                        }
                    }
                    else if(!size.equals("small") || !size.equals("medium") || !size.equals("large"))
                    {
                        System.out.println("Please try again.");
                    }
                    break;

                    case "BOX": //For the shape Box
                        System.out.print("How many rows/columns would you like? Please choose between 4 and 10: ");
                        rows = keyboard.nextInt();
                        
                            isBox.isBox(rows);
                                                
                    break;

                    case "X IN A BOX":
                    {
                        System.out.print("How many rows/columns would you like? Please choose between 4 and 10: ");
                        rows = keyboard.nextInt();
                        
                            isXInBox.isXInBox(rows);
                    }
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
        inputFile.close();
    }
}
