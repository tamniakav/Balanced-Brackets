# Balanced-Brackets
Just another repository
using System;

namespace _15.Balanced_Brackets
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int firstBracket = 0;
            int secondBracket = 0;

            for (int i = 0; i < n; i++)
            {
                string brackets = Console.ReadLine();

                if (brackets == "(")
                {
                    firstBracket++;
                }
                else if (brackets == ")")
                {
                    if (firstBracket > secondBracket)
                    {
                        secondBracket++;
                    }
                    else
                    {
                        secondBracket++;
                        break;
                    }
                }
                if (firstBracket < secondBracket)
                {
                    break;
                }
            }

            if (firstBracket == secondBracket)
            {
                Console.WriteLine("BALANCED");
            }
            else
            {
                Console.WriteLine("UNBALANCED");
            }
        }
    }
}
