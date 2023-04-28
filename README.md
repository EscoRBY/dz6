# dz6
// dotnet new console
// dotnet run
// Zadacha 1:  Пользователь вводит с клавиатуры M чисел. Посчитайте, сколько чисел больше 0 ввёл пользователь.
//Code
using System;

class Program {
    static void Main(string[] args) {
        Console.WriteLine("Введите кол-во одномерных чисел");
        int m = int.Parse(Console.ReadLine());// считываем количество чисел
         Console.WriteLine("Введите числа"); 
        int count = 0; // счетчик чисел больше 0
        for (int i = 0; i < m; i++) {
            int num = int.Parse(Console.ReadLine()); // считываем число
            if (num > 0) {
                count++; // увеличиваем счетчик, если число больше 0
            }
        }
       
        Console.WriteLine("Количество чисел больше 0: " + count);
    }
}
/END
// Zadacha 2:Напишите программу, которая найдёт точку пересечения двух прямых, заданных уравнениями y = k1 * x + b1, y = k2 * x + b2; значения b1, k1, b2 и k2 задаются пользователем.
//Code
using System;

class Program {
    static void Main(string[] args) {
        double b1, k1, b2, k2;
        Console.WriteLine("Введите значения b1, k1, b2, k2 c пробелом:");
        string[] input = Console.ReadLine().Split();
        b1 = double.Parse(input[0]);
        k1 = double.Parse(input[1]);
        b2 = double.Parse(input[2]);
        k2 = double.Parse(input[3]);

        double x = (b2 - b1) / (k1 - k2);
        double y = k1 * x + b1;

        Console.WriteLine("Точка пересечения: ({0}; {1})", x, y);
    }
}
//END
