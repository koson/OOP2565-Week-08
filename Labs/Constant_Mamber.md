# Constant example


## Constant 
```cs
namespace ConstantMemberExample
{
 
    internal class Program
    {
        static void Main(string[] args)
        {
            double radius = 5.0;
            const double PI = 3.14159;
            Console.WriteLine("Welcome, this program calculate circle area");
            Console.WriteLine($"The radius of circle is {radius:f} unit.");
            double area = PI * radius * radius;
            Console.WriteLine($"The area of circle is {area:f4} square unit.");
        }
    }
}
```


## Constant in class

```cs
namespace ConstantMemberExample
{
    class MyCircle
    {
        const double PI = 3.14159;
        public static void PrintArea(double radius)
        {
            double area = PI * radius * radius;
            Console.WriteLine($"The area of circle is {area:f4} square unit.");
        }
    }
    internal class Program
    {
        static void Main(string[] args)
        {
            MyCircle.PrintArea(5.0f);
        }
    }
}
```


## Constant in expression

```cs
namespace ConstantMemberExample
{
    class MyCircle
    {
        const double PI = 3.14159;
        const double PI2 = PI*2.0;
        public static void PrintArea(double radius)
        {
            double area = PI * radius * radius;
            Console.WriteLine($"The area of circle is {area:f4} square unit.");
        }
        public static void PrintCircumference(double radius)
        {
            double circumference = PI2 * radius;
            Console.WriteLine($"The circumference of circle is {circumference:f4} square unit.");
        }
    }
    internal class Program
    {
        static void Main(string[] args)
        {
            MyCircle.PrintArea(5.0f);
            MyCircle.PrintCircumference(5.0f);
        }
    }
}
```

## change value of constant
```cs
namespace ConstantMemberExample
{
    class MyCircle
    {
        const double PI = 3.14159;
        public static void PrintArea(double radius)
        {
            double area = PI * radius * radius;
            Console.WriteLine($"The area of circle is {area:f4} square unit.");
        }
        PI = Math.PI;  // change value of constant

    }
    internal class Program
    {
        static void Main(string[] args)
        {
            MyCircle.PrintArea(5.0f);
        }
    }
}
```

## public static constant

```cs
namespace ConstantMemberExample
{
    class MyCircle
    {
        public static const double PI = 3.14159;
        public static void PrintArea(double radius)
        {
            double area = PI * radius * radius;
            Console.WriteLine($"The area of circle is {area:f4} square unit.");
        }
    }
    internal class Program
    {
        static void Main(string[] args)
        {
            MyCircle.PrintArea(5.0f);
        }
    }
}
```