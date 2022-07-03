## Java Programs
* Program to demonstrate use of implementing interface and extending interfaces.
``` Java
import java.util.Scanner;

interface Area
{
    public double getArea(double radius, double height);
}

interface Volume extends Area
{
    public double getVolume(double radius, double height);
}

class Cylinder implements Volume
{
    public double getArea(double radius, double height)
    {
        return 2 * Math.PI * radius * (radius + height);
    }

    public double getVolume(double radius, double height)
    {
        return Math.PI * radius * radius * height;
    }
}

public class CylinderSample
{
    public static void main(String[] args)
    {
        Cylinder cylinder = new Cylinder();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the radius of the cylinder: ");
        double radius = scanner.nextDouble();

        System.out.println("Enter the height of the cylinder: ");
        double height = scanner.nextDouble();

        System.out.printf("Surface Area of the Cylinder : %.3f \n", cylinder.getArea(radius, height));
        System.out.printf("Volume of the Cylinder : %.3f", cylinder.getVolume(radius, height));

        scanner.close();

    }
}
```
