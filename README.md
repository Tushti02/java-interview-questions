# java-interview-questions


# Java Interview Code Questions

## 1. code review (Question)

There are 4-5 pointers for improving this code for clean code, resusability, DRY, SOLID etc. Your junior comes to you with this code, what will you ask them to improve?

```java
import java.util.List;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.stream.Collectors;

public class Program {
    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
        List<Integer> evenNumbers = GetEvenNumbers(numbers);
        System.out.println("Even Numbers: " + String.join(", ", evenNumbers.stream().map(String::valueOf).collect(Collectors.toList())));
    }

    public static List<Integer> GetEvenNumbers(List<Integer> numbers) {
        List<Integer> evenNumbers = new ArrayList<>();
        for (int number : numbers) {
            if (number % 2 == 0) {
                evenNumbers.add(number);
            }
        }
        return evenNumbers;
    }

    public static int SumEvenNumbers(List<Integer> numbers) {
        int sum = 0;
        for (int i = 0; i < numbers.size(); i++) {
            if (numbers.get(i) % 2 == 0) {
                sum += numbers.get(i);
            }
        }
        return sum;
    }
}
```


## 1. Get Even Numbers and Sum from a List (Answer)

Write a Java program that accepts a list of integers and returns the even numbers from the list. Also, return the sum of the even numbers.

```java

import java.util.*;
import java.util.stream.Collectors;

public class EvenNumbers {
    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
        List<Integer> evenNumbers = getEvenNumbers(numbers);
        int sumEvenNumbers = sumEvenNumbers(numbers);

        System.out.println("Even Numbers: " + evenNumbers);
        System.out.println("Sum of Even Numbers: " + sumEvenNumbers);
    }

    private static List<Integer> getEvenNumbers(List<Integer> numbers) {
        return numbers.stream().filter(n -> n % 2 == 0).collect(Collectors.toList());
    }

    private static int sumEvenNumbers(List<Integer> numbers) {
        return numbers.stream().filter(n -> n % 2 == 0).mapToInt(Integer::intValue).sum();
    }
}
```

---

# interviewquestions
```java

public class Container
{
    public int Value;
}

public class Program
{
    static void Main()
    {
        int x = 10;
        Container container = new Container();
        container.Value = x;

        x = 20;
        container.Value = 30;

        Console.WriteLine("x: " + x);
        Console.WriteLine("container.Value: " + container.Value);
    }
}
```
###########################################################################################################
```java
public class Program {
    public static void main(String[] args) {
        int x = 123;
        Object obj = x; // Boxing
        int y = (int)obj; // Unboxing
        
        x = 456;
        
        System.out.println("x: " + x);
        System.out.println("obj: " + obj);
        System.out.println("y: " + y);
    }
}
```
###########################################################################################################



```java
class Person {
    public String name;
}

public class Program {
    static void modifyValue(int value) {
        value = 100;
    }

    static void modifyReference(Person person) {
        person.name = "Charlie";
    }

    public static void main(String[] args) {
        int x = 50;
        Person person = new Person();
        person.name = "Alice";

        modifyValue(x);
        modifyReference(person);

        System.out.println("x: " + x);
        System.out.println("person.name: " + person.name);
    }
}
```
###########################################################################################################



```java
class Person {
    public String name;
}

public class Program {
    public static void main(String[] args) {
        Person person1 = new Person();
        person1.name = "Alice";

        Person person2 = person1;
        person2.name = "Bob";
        
        System.out.println("person1.name: " + person1.name);
        System.out.println("person2.name: " + person2.name);
    }
}

```
###########################################################################################################



```java
public class Program {
    public static void main(String[] args) {
        int a = 5;
        int b = a;
        b = 10;
        
        System.out.println("a: " + a);
        System.out.println("b: " + b);
    }
}
```
###########################################################################################################
___


# task
```java
public class Program
{
    public static async Task Main()
    {
        Task<int> task = GetNumberAsync();
        Console.WriteLine("Waiting for the task to complete...");
        int result = await task;
        Console.WriteLine($"Result: {result}");
    }

    public static async Task<int> GetNumberAsync()
    {
        await Task.Delay(2000); // Simulate a delay
        return 42;
    }
}

```
###########################################################################################################



```java
public class Program
{
    public static async Task Main()
    {
        Task<int> task = GetNumberAsync();
        Console.WriteLine("Waiting for the task to complete...");
        int result = await task;
        Console.WriteLine($"Result: {result}");
    }

    public static async Task<int> GetNumberAsync()
    {
 Console.WriteLine("called");
        await Task.Delay(2000); // Simulate a delay
        return 42;
    }
}
```

***


```javascript
<!DOCTYPE html>
<html>
<head>
<title>InnerHTML Example</title>
</head>
<body>
 
<h1 id="myHeading">Hello, World!</h1>
<button onclick="updateHeading()">Update Heading</button>
 
<script>
//your code goes here
</script>
 
</body>
</html>
```

***
Write a recursive Java program to find the factorial of a number.
Write a Java program to check if a string is a palindrome.
Write a Java program to check if a given number is prime.









