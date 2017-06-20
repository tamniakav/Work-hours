using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Work_hours
{
    class Program
    {
        static void Main(string[] args)
        {
            int neededHours = int.Parse(Console.ReadLine());
            int workers = int.Parse(Console.ReadLine());
            int days = int.Parse(Console.ReadLine());

            int workingHours = workers * days * 8;

            if (workingHours >= neededHours)
            {
                int restHours = workingHours - neededHours;
                Console.WriteLine("{0} hours left", restHours);
            }
            else
            {
                int moreHours = neededHours - workingHours;
                int penalty = moreHours * days;

                Console.WriteLine("{0} overtime", moreHours);
                Console.WriteLine($"Penalties: {penalty}");
            }
        }
    }
}
