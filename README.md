// Вычислить n-ое треугольного число(сумма чисел от 1 до n), n! (произведение чисел от 1 до n).

// Внутри класса Answer напишите метод countNTriangle, который принимает число n и возвращает его n-ое треугольное число.

// Пример


// n = 4 -> 10

// n = 5 -> 15


import java.util.Scanner;

class Answer{

    public static void main(String[] args) {
        Scanner iScanner = new Scanner(System.in);
        System.out.printf("Введите первое число: ");
        int i = iScanner.nextInt();
        System.out.printf("Треугольное число: %d\n", giveMeNumber(i));
        iScanner.close();
    }

    public static int giveMeNumber(int a) {
        return (a * (a + 1)) / 2;
    }
}




// Эталонное решение от автора

class Answer {
    public int countNTriangle(int n){
        int sum = 0;
        for(int i = 1; i <= n; i++){
            sum += i;
        }
        return sum;
    }
}

class Printer {
    public static void main(String[] args) {
        int n = 0;

        if (args.length == 0) {
            n = 4;
        } else {
            n = Integer.parseInt(args[0]);
        }

        Answer ans = new Answer();
        int itresume_res = ans.countNTriangle(n);
        System.out.println(itresume_res);
    }
}


// Напишите функцию printPrimeNums, которая выведет на экран все простые числа от 1 до 1000, каждое на новой строке.

// Напишите свой код в методе printPrimeNums класса Answer.

// Пример

// 1
// 2
// 3
// 5
// 7
// 11
// ...

// 1е решение задачи

class Answer {
    public void printPrimeNums(){
    
        int min = 1;
        int max = 1001;
        Answer random = new Answer();
        for (int i = 1; i < 1001; i++) {

        System.out.println(i);
        }
    }
}

class Printer{
    public static void main(String[] args) {

        Answer ans = new Answer();
        ans.printPrimeNums();
    }
}




// 2е решение

class Answer {
   public void printPrimeNums(){
      
       boolean isPrime;
       Answer random = new Answer();
       for (int i = 1; i < 1001; i++) {
        isPrime = false;
           for (int j = 2; j < i / 2; j++) {
               if ((i%j) == 0)
               {
                isPrime = true;
               }
           }
           if (isPrime == false)
           {
                   System.out.println(i+ " ");
           }
       }
   }
}

class Printer{
   public static void main(String[] args) {

       Answer ans = new Answer();
       ans.printPrimeNums();
   }
}

// Эталонное решение от автора

class Answer {
    public void printPrimeNums(){
        boolean isPrime;
        for(int i = 1; i < 1000; i++) {
            isPrime = i == 1;
            for(int j = 2; j < 1000; j++) {
                if (i >= j && i % j == 0) {
                    if(j == i) {
                        isPrime = true;
                    }
                    break;
                }
            }
            if(isPrime) System.out.println(i);
        }
    }
}

class Printer{
    public static void main(String[] args) {

        Answer ans = new Answer();
        ans.printPrimeNums();
    }
}


// Напишите класс Calculator, который будет выполнять математические операции (+, -, *, /) 
// над двумя числами и возвращать результат. В классе должен быть метод calculate, 
// который принимает оператор и значения аргументов и возвращает результат вычислений.
// При неверно переданном операторе, программа должна вывести сообщение об ошибке "Некорректный оператор: 
// 'оператор'".


import java.util.Scanner;
class Calculator {
    public static void main(String[] args) {
        int a;
        int b;
        int ans;
        char op;
        Scanner reader = new Scanner(System.in);
        System.out.print("Введите первое число: ");
        a = reader.nextInt();
        System.out.print("\nВведите оператор (+, -, *, /): ");
        op = reader.next().charAt(0);
        System.out.print("Введите второе число: ");
        b = reader.nextInt();
        switch(op) {
            case '+': ans = a + b;
                break;
            case '-': ans = a - b;
                break;
            case '*': ans = a * b;
                break;
            case '/': ans = a / b;
                break;
            default:  System.out.printf("Ошибка! Введите правильный оператор");
                return;
        }
        System.out.print("\nРезультат:\n");
        System.out.printf(a + " " + op + " " + b + " = " + ans);
    }
}


//Дан массив целых чисел. Найти количество пар соседних элементов, где первый элемент вдвое больше второго.

class main{
public static void main(String[] args) {     
    int [] arr = {1,2,3,4,2,1};
    int count = 0;
    for (int i = 0; i < arr.length-1; i++) {
        if (arr [i] == arr[i+1]*2) {
            count++;
        }
    }
        System.out.println(count);
  }
}