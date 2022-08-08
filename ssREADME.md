using System;
using uni;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace week3
{
    class Program
    {
        static void Main(string[] args)
        {

            Subject u1 = new Subject("C#");
            Subject u2 = new Subject("Java");

            Student s1 = new Student("Dick");
            Student s2 = new Student("Johnson");
            Student s3 = new Student("Sarah");

            u1.enrol(s1);
            u1.enrol(s2);

            u2.enrol(s1);
            u2.enrol(s3);

            Console.WriteLine("Enrolled students in " + u1.Name);

            foreach (Student s in u1.getStudents())
            {
                Console.WriteLine("\t" + s.Name);
            }

            Console.WriteLine();
            Console.WriteLine(s1.Name + "'s Subjects: \n");
            foreach (Subject s in s1.getSubjects())
            {
                Console.WriteLine("\t" + s.Name);
            }

            Console.WriteLine("\n\nPress any key to continue ...");
            Console.ReadKey();

        }
    }

    
