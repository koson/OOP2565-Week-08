# properties example

``` cs
namespace PropertyExample
{

    class Cat
    {
        public int Age { get; set; }

    }
    internal class Program
    {
        static void Main(string[] args)
        {
            var Garfield = new Cat();
            Garfield.Age = 5;
            Console.WriteLine(Garfield.Age);
        }
    }
}
```

## add more property
```cs
namespace PropertyExample
{

    class Cat
    {
        public int Age { get; set; }
        public Color SkinColor { get; set; }

    }
    internal class Program
    {
        static void Main(string[] args)
        {
            var Garfield = new Cat();
            Garfield.Age = 5;
            Garfield.SkinColor = Color.Orange;

            Console.WriteLine(Garfield.Age);
            Console.WriteLine(Garfield.SkinColor);
        }
    }
}
```


## calling getter/setter
``` cs
namespace PropertyExample
{

    class Cat
    {
        public int Age { get; set; }
        public Color SkinColor { get; set; }

    }
    internal class Program
    {
        static void Main(string[] args)
        {
            var Garfield = new Cat();
            // callint setter
            Garfield.Age.set(5);

            // calling getter
            int catAge = Garfield.Age.get();
            Console.WriteLine(catAge);
        }
    }
}
```


## properties calculation

``` cs
namespace PropertyExample
{

    class Cat
    {
        public int Age { get; set; }
        public int YearOfBirth { get; set; }

    }
    internal class Program
    {
        static void Main(string[] args)
        {
            var Garfield = new Cat();
            Garfield.YearOfBirth = 2015;
            int GarAge = 2023 - Garfield.YearOfBirth;
            Console.WriteLine($"Garfield's age = {GarAge}");
        }
    }
}
```


``` cs
namespace PropertyExample
{

    class Cat
    {
        public int Age {
            get { return DateTime.Now.Year - YearOfBirth; }
            set { Age = value; } 
        }
        public int YearOfBirth { get; set; }

    }
    internal class Program
    {
        static void Main(string[] args)
        {
            var Garfield = new Cat();
            Garfield.YearOfBirth = 2015;
            Console.WriteLine($"Garfield's age = {Garfield.Age}");
        }
    }
}
```





```cs
namespace PropertyExample
{

    class Cat
    {
        int age;
        int yearOfBirth;
        public int Age {
            get {  return DateTime.Now.Year - YearOfBirth;  }
            set 
            { 
                age = value;
                yearOfBirth = DateTime.Now.Year - age;
            } 
        }
        public int YearOfBirth {
            get { return yearOfBirth; }
            set { 
                yearOfBirth = value;
                age = DateTime.Now.Year - YearOfBirth;
            }
        }
    }
    internal class Program
    {
        static void Main(string[] args)
        {
            var Garfield = new Cat();
            Garfield.YearOfBirth = 2015;
            Console.WriteLine($"Garfield's age = {Garfield.Age}");
        }
    }
}
```

