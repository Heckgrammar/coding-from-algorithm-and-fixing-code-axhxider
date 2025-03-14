![image](https://github.com/MrAStone/StartEndCodeFixingTask/assets/60425249/d34dad5e-a403-4d6e-863f-2d3ebcd4b873)

In your notes copy the table and complete it.

![image](https://github.com/MrAStone/StartEndCodeFixingTask/assets/60425249/2c96d63f-1681-4b62-b50b-48fb68eba186)

Do the coding task in C#



Test type 

Test data 

valid\Choice 

difference 

normal 

startYear = 1995, endYear = 2010 

False 

        - 

erroneous 

startYear = 2015, endYear = 2000 

False  

        - 

boundary 

startYear = 2000, endYear = 2023 

True  

       23 





//coding


using System;
					
public class Program
{
	public static void Main()
	{
		bool validChoice = false;
        int startYear, endYear, difference = -1;

        do
        {
            Console.Write("Enter a start year: ");
            startYear = int.Parse(Console.ReadLine());

            Console.Write("Enter an end year: ");
            endYear = int.Parse(Console.ReadLine());

            if (startYear >= endYear)
            {
                Console.WriteLine("Start year must be before end year");
            }
            else if (startYear < 2000)
            {
                Console.WriteLine("Start year must be 2000 or later");
            }
            else
            {
                validChoice = true;
            }

        } while (!validChoice);

        difference = endYear - startYear;
        Console.WriteLine("Difference: " + difference);
    }	
	
}
