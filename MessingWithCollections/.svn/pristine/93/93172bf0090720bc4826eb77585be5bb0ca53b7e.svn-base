using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace MessingWithCollections
{
    public class Delegates // DELEGATES HELP US PASS METHODS AS PARAMTERS
    {




        public class Person
        {
            public string Name { get; set; }
            public int Age { get; set; }

            public Person(string name, int age)
            {
                Name = name;
                Age = age;
            }
        }

        public delegate bool FilterDelegate(Person p); // THIS DELEAGE HAS ACCESS TO ANY METHOD THAT TAKES IN A PERSON AAND RETURNS A BOOL


        public static void DisplayPeople(string title, List<Person> people, FilterDelegate filter)
        {
            Console.WriteLine(title);

            foreach (Person p in people)
            {
                if (filter(p))
                {
                    Console.WriteLine("{0}, {1} years old", p.Name, p.Age);
                }
            }
            Console.Write("\n\n");
        }

        //------------------------ FILTERS------------------------ DELEGATE HAS ACCESS TO ALL OF THESE
        public static bool IsChild(Person p)
        {
            return p.Age < 18;
        }

        public static bool IsAdult(Person p)
        {
            return p.Age >= 18;
        }

        public static bool IsSenior(Person p)
        {
            return p.Age >= 65;
        }
    }
}
