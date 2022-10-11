
Задайте список из нескольких чисел.
Напишите программу,
которая найдёт сумму элементов списка,
стоящих на нечётной позиции.
Пример:
- [2, 3, 5, 9, 3] -> на нечётных позициях элементы 3 и 9, ответ: 12
~~~
list_numb = [2, 3, 5, 9, 3]
summ = 0
for i in range(1, len(list_numb), 2):
    summ += list_numb[i]        
print(summ)
~~~
Напишите программу, которая найдёт
произведение пар чисел списка.
Парой считаем первый и последний элемент,
второй и предпоследний и т.д.
Пример:
- [2, 3, 4, 5, 6] => [12, 15, 16];
- [2, 3, 5, 6] => [12, 15]

~~~
list = [2, 5, 9, 8, 4]
s = 0
if len(list) % 2 == 0:
    l = len(list) // 2
else:
    l = len(list) // 2 + 1
for i in range(l):
    s = list[-i - 1] * list[i]
    print(s)
~~~
Задайте список из вещественных чисел.
Напишите программу, которая найдёт 
разницу между максимальным и минимальным
значением дробной части элементов.
Пример:
- [1.1, 1.2, 3.1, 5, 10.01] => 0.19
~~~
float_list = [1.1, 1.2, 3.1, 5, 10.01]
list = [round(i % 1,2) for i in float_list if i % 1 != 0]
print(max(list) - min(list))
~~~
Напишите программу, которая 
будет преобразовывать десятичное
число в двоичное.
Пример:
- 45 -> 101101
- 3 -> 11
- 2 -> 10
~~~
numb = int(input('Введите число: '))
b = ""
while numb != 0:
    b = str(numb % 2) + b
    numb = numb //2
print(b) 
~~~
Задайте число. Составьте 
список чисел Фибоначчи,
в том числе для 
отрицательных индексов.
Пример:
- для k = 8 список будет выглядеть так:
[-21 ,13, -8, 5, −3, 2, −1, 1, 0, 1, 1, 2, 3, 5, 8, 13, 21]
~~~
def Fibonacci(n):
    if n in [1, 2]:                       
        return(1)
    else:
        return Fibonacci(n-1) + Fibonacci(n-2)

def NegaFibonacci(n):
    if n == 1:                       
        return 1
    elif n == 2:                       
        return -1
    else:
        num1, num2 = 1, -1
        for i in range(2, n):
            num1, num2 = num2, num1 - num2
        return num2

list = [0]
number = int(input('Введите число: '))
for e in range(1, number + 1):
    list.append(Fibonacci(e))
    list.insert(0, NegaFibonacci(e))
print(list)
~~~
