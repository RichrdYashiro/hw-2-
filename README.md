# hw-2-
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp6
{

    class Program
    {
        // Сысоев Андрей
        // Задание 2
        static void Main(string[] args)

        {
            Hw2();
            Console.ReadKey();
            Hw1();
            Console.ReadKey();
            Hw3();
            Console.ReadKey();
            Hw4();
            Console.ReadKey();
            
            

        }
        static void Hw2()
        {
            Console.Write("Введите число : ");
            int num = int.Parse(Console.ReadLine());
            int i = 0;
            while (num > 0)
            {
                i++;
                num /= 10;
            }
            Console.WriteLine("Количество цифр введенного числа : {0}", i);
            Console.ReadKey();

        }


        // Задание 1
        static void Hw1()
        {
            Console.Write("Введите первое число: ");
            int firstNumber = int.Parse(Console.ReadLine());
            Console.Write("Введите второе число: ");
            int secondNumber = int.Parse(Console.ReadLine());
            Console.Write("Введите третье число: ");
            int thirdNumber = int.Parse(Console.ReadLine());
            Console.WriteLine($"Минимальное число: { MinimalScore(firstNumber, secondNumber, thirdNumber)}");
            Console.ReadKey();
        }
        public static int MinimalScore(int a, int b, int c)
        {
            int score;
            if (a < b && a < c)
            {
                score = a;
            }
            else if (b < a && b < c)
            {
                score = b;
            }
            else
            {
                score = c;
            }
            return score;
        }

        //Задание 3
        static void Hw3()
        {
            int sum = 0;
            int num = 0;
            do
            {
                num = int.Parse(Console.ReadLine());
                if (num > 0 && num % 2 == 1)
                    sum += num;

            } while (num != 0);

            Console.WriteLine("Sum: " + sum);
        }
        // задание 4
        static void Hw4()
        {

            string login = "root";
            string password = "GeekBrains";

            int count = 0;
            do
            {
                Console.WriteLine("\nВведите логин: ");
                string checkLogin = Console.ReadLine();

                Console.WriteLine("Введите пароль: ");
                string checkPassword = Console.ReadLine();

                if (login == checkLogin && password == checkPassword)
                {

                    Console.WriteLine("Добро пожаловать");
                    Console.ReadLine();
                    break;
                }
                Console.WriteLine("Неверно введен логин или пароль");
                Console.ReadLine();
                ++count;
            } while (count < 4);




        }
        }
        
    }
