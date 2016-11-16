import java.awt.geom.*;
import java.awt.event.*;
import java.awt.*;
import java.util.Scanner;
/**
 * This class is to show a Circle and and the user will input the size
 * @author KareemWilliams
 */
public class isCircle extends Frame
{
    Shape circle = new Ellipse2D.Float(100.0f, 100.0f, 100.0f, 100.0f);
    public void paint(Graphics g)
    {
        Graphics2D ga = (Graphics2D)g;
        ga.draw(circle);
    }
    
    public static void main(String[] args)
    {
        int x;
        int y;
        Scanner keyboard = new Scanner(System.in);
        System.out.print("How wide do you want the circle? ");
        x = keyboard.nextInt();
        System.out.print("How tall do you want the circle? ");
        y = keyboard.nextInt();
        /*Frame frame = new isCircle();
        frame.addWindowListener(new WindowAdapter()
        {
            public void windowClosing(WindowEvent we)
            {
                System.exit(0);
            }
        });
        frame.setSize(x, y);
        frame.setVisible(true);*/
    }
}
