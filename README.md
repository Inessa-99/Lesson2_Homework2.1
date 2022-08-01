Домашнее задание после семинара №2.



Задача 1
/*
Задача 10: Напишите программу, которая принимает на вход трёхзначное число и на выходе показывает вторую цифру этого числа.

456 -> 5
782 -> 8
918 -> 1
*/

Console.WriteLine("Введите трехзначное число: ");
int a = int.Parse(Console.ReadLine());

int result = secondNum(a);
Console.WriteLine(result);

int secondNum(int num)
{
    int twoDigit = num % 100;
    int singleDigit = twoDigit / 10;
    int result = singleDigit;
    return result;
}





Задача 2
/*Напишите программу, которая выводит третью цифру заданного числа или сообщает, что третьей цифры нет.

645 -> 5
78 -> третьей цифры нет
32679 -> 6
*/

Console.WriteLine("Введите число: ");
int a = int.Parse(Console.ReadLine());
int add = 0;

if (a / 100 != 0)
{
    int result = thirdNum(a, add);
    Console.WriteLine(result);
}
else
{
    Console.WriteLine("третьей цифры нет");
}

int thirdNum(int number, int number2)
{
    while (number > 999)
    {
        number2 = number/10;
        number = number2;
    }
    return (number%10);
}







Задача 3
/*
Задача 15: Напишите программу, которая принимает на вход цифру, обозначающую день недели, и проверяет, является ли этот день выходным.
6 -> да
7 -> да
1 -> нет
*/

Console.WriteLine("Введите число: ");
int a = int.Parse(Console.ReadLine());

if (weekend(a))
{
Console.WriteLine("Да");
}
else
{
Console.WriteLine("Нет");
}

bool weekend(int num)
{
    if (num == 6 || num == 7)
    {
        return true;
    }
    else
    {
        return false;
    }
}

