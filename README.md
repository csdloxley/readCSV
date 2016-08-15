using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.IO;
namespace ReadCSV2
{
    class Program
    {
        static void Main(string[] args)
        {
            string[] filePaths = Directory.GetFiles("D:\\", "*.csv");
            System.Diagnostics.Process pauseProc =
            System.Diagnostics.Process.Start(new System.Diagnostics.ProcessStartInfo() { FileName = "cmd", Arguments = "/C pause", UseShellExecute = false });

            foreach (var file in filePaths)
            {
                //  string[] datacsv = System.IO.File.ReadAllLines("D:\\LP02_1506172300.csv");
                string[] datacsv2 = System.IO.File.ReadAllLines(file);

                foreach (string textcsv in datacsv2)
                {
                    Console.WriteLine(textcsv);


                }

            }
            pauseProc.WaitForExit();
        }
    }
}
