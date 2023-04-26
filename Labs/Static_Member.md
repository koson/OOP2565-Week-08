



```cs
namespace StaticMemberExample
{
    class Cat
    {
        public int legs = 4;
    }

    class Duck
    {
        public static int legs = 2;
    }

    internal class Program
    {
        static void Main(string[] args)
        {
            Cat cat = new Cat();
            Console.WriteLine($"Cat has  {cat.legs} legs.");
            Console.WriteLine($"Duck has  {Duck.legs} legs");
        }
    }
}

```



```cs
namespace StaticMemberExample
{
    class Cat
    {
        public int legs = 4;
        public static int count = 0;
        public Cat()
        {
            count++;
        }
    }

    internal class Program
    {
        static void Main(string[] args)
        {
            Cat cat = new Cat();
            Console.WriteLine($"There is (are) {Cat.count} cat(s).");
            Cat cat1 = new Cat();
            Console.WriteLine($"There is (are) {Cat.count} cat(s).");
            Cat[] catArray = new Cat[10];
            Console.WriteLine($"There is (are) {Cat.count} cat(s).");
            for (int i = 0; i < catArray.Length; i++)
            {
                catArray[i] = new Cat();
            }
            Console.WriteLine($"There is (are) {Cat.count} cat(s).");
        }
    }
}

```



```cs
namespace StaticMemberExample
{
    class Cat
    {
        public int legs = 4;
        public static int count = 0;
        public Cat()
        {
            count++;
        }
        public static void PrintCatCount()
        {
            if (count == 1)
                Console.WriteLine($"There is {count} cat");
            else if (count > 1)
                Console.WriteLine($"There are {count} cats");
            else
                Console.WriteLine($"Invalid number of cats");
        }
    }

    internal class Program
    {
        static void Main(string[] args)
        {
            Cat cat = new Cat();
            Cat.PrintCatCount();
            Cat cat1 = new Cat();
            Cat.PrintCatCount();
            Cat[] catArray = new Cat[10];
            Cat.PrintCatCount();
            for (int i = 0; i < catArray.Length; i++)
            {
                catArray[i] = new Cat();
            }
            Cat.PrintCatCount();
        }
    }
}
```




## คำถาม

```cs
namespace StaticMemberExample
{
    class Cat
    {
        public int legs = 4;
        public static int count = 0;
        public Cat()
        {
            count++;
        }
        public static void PrintCatCount()
        {
            if (count == 1)
                Console.WriteLine($"There is {count} cat");
            else if (count > 1)
                Console.WriteLine($"There are {count} cats");
            else
                Console.WriteLine($"Invalid number of cats");
        }
    }

    internal class Program
    {
        static void Main(string[] args)
        {
            Cat cat = new Cat();
            Cat.PrintCatCount();
            Cat cat1 = new Cat();
            cat1.PrintCatCount();
        }
    }
}
```