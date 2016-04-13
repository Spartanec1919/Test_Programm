using System;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            double A, B, C, p, S;
            Console.WriteLine("Введите сторону A: ");
            A = Convert.ToDouble(Console.ReadLine());

            Console.WriteLine("Введите сторону B: ");
            B = Convert.ToDouble(Console.ReadLine());

            Console.WriteLine("Введите сторону C: ");
            C = Convert.ToDouble(Console.ReadLine());

            if (Math.Pow(C, 2) == Math.Pow(A, 2) + Math.Pow(B, 2))
                S = A * B / 2;            
            else if (Math.Pow(A, 2) == Math.Pow(B, 2) + Math.Pow(C, 2))
                S = B * C / 2;
            else if (Math.Pow(B, 2) == Math.Pow(C, 2) + Math.Pow(A, 2))
                S = C * A / 2;
            else
            {
                Console.WriteLine("Треугольник не является прямоугольным!");
                //p = (A + B + C) / 2;
                //S = Math.Sqrt(p * (p - A) * (p - B) * (p - C));
            }

            Console.WriteLine("Площадь равна: {0}", S);
            Console.ReadLine();
        }
    }
}
