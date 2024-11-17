using System;
using System.Collections.Generic; 
class Program
{ 
    static void Main() 
    { 
        
            Console.WriteLine("Enter minNumber:");
            
            int minNumber = int.Parse(Console.ReadLine()); 
               Console.WriteLine("Enter maxNumber:"); 
            int maxNumber = int.Parse(Console.ReadLine());
            int[] counts = new int[maxNumber - minNumber + 1];
            Random random = new Random(); 
 for (int i = 0; i < 1000; i++)
            {
                int number = random.Next(minNumber, maxNumber + 1);
                counts[number - minNumber]++;
            }
                Console.WriteLine("Number\tFrequency");
                for (int i = 0; i < counts.Length; i++) 
                { Console.WriteLine($"{i + minNumber}\t{counts[i]}"); 
                    
                } 
   }
    
}
