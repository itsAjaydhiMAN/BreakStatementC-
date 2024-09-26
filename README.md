# BreakStatementC-

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using System.Threading.Tasks;

namespace BreakStatement
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int TotalCoffee = 0;

        Start:

            Console.WriteLine("Please Select your coffee size : 1- Small , 2- Medium , 3- Large");
            int UserChoice = int.Parse(Console.ReadLine());

            switch (UserChoice)
            {
                case 1:
                    TotalCoffee += 1;
                    break;

                case 2:
                    TotalCoffee += 2;
                    break;
                   
                case 3: 
                    TotalCoffee += 3;
                    break;
                 
                default:
                    Console.WriteLine("Your Choice {0} is invalid",UserChoice);
                    goto Start;
            }
        Deecide:

            Console.WriteLine("Do you want to buy another coffee - YES or NO?");
            string UserDecision = Console.ReadLine();

            switch (UserDecision.ToUpper())
            {
                case "YES":
                    goto Start;
                case "NO":
                    break;
                default:
                    Console.WriteLine("Your Choice {0} is invalid. Please try again.....",UserDecision);
                    goto Deecide;

            }
            Console.WriteLine("Thank you for shopping with us");
            Console.WriteLine("Bill Amount = {0}",TotalCoffee);
        }
    }
}
