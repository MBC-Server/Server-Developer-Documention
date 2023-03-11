## 變數

首先，Java中有幾種基本變數類型，它們分別是：

1. 整數

Java中的整數類型包括byte、short、int和long。它們的區別在於能夠儲存的範圍不同，例如byte類型可以儲存-128到127之間的數字，而long類型可以儲存更大的數字。

2. 浮點數

Java中的浮點數類型包括float和double。它們用於儲存帶有小數部分的數字。double類型比float類型更精確，但也更佔空間。

3. 字符

Java中的字符類型是char，它用於儲存單個字符。例如：

```java
char c = 'A';
```
4. 布林值

Java中的布爾類型是boolean，它用於儲存true或false這樣的布爾值。
這些變數類型可以用於聲明變數。例如：

```java
int age = 20;
double salary = 10000.0;
char gender = 'M';
boolean married = false;
```

當聲明變數時，需要指定變數的類型。聲明變數可以讓我們在程序中儲存數據並進行運算，這是Java編程的基礎。

除了上述介紹的基本變數類型外，Java還有其他一些有用的變數類型，例如：

5. 字串

Java中的字符串類型是String，它用於儲存文本。例如：

```java
String name = "Alice";
```

6. 陣列

Java中的數組類型可以用於儲存多個相同類型的數據。例如：

```java
int[] nums = {1, 2, 3, 4, 5};
```

在Java中，變數的類型決定了變數能夠儲存的數據類型和操作。變數的類型必須與儲存的值的類型匹配，否則會發生類型錯誤。

值得注意的是，Java中的變數是強型別的，這意味著在聲明變數時必須指定變數的類型，並且不能將一個類型的值賦值給另一種類型的變數。


## 物件導向

Java是一種物件導向的編程語言，物件是Java中的一個重要概念。物件類型可以用於聲明物件變數。例如：

```java
Person person = new Person("Tom");
```
Java中的物件導向包括以下幾個主要概念：

1. **類別 (Class)**

是一種定義物件屬性和方法的模板。在Java中，所有的物件都是基於類別創建的。類別定義了物件的屬性和方法，並且可以創建多個物件。

下面是一個簡單的Person類的示例程式碼：

```java
public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }
}
```

在上面的程式碼中，Person類定義了兩個屬性：name和age，以及一個構造函數和兩個方法：getName和getAge。

2. **物件 (Object)** 

物件是類的實例。在Java中，可以使用關鍵字new來創建物件。下面是一個創建Person物件的示例程式碼：

```java
Person person = new Person("Alice", 20);
```

在上面的程式碼中，我們創建了一個名為person的Person物件，並傳入兩個參數："Alice"和20。

3. **繼承 (extend)**

繼承是一種定義新類時使用現有類的屬性和方法的機制。在Java中，使用關鍵字extends來創建繼承關係。下面是一個繼承Person類的Student類的示例程式碼：

```java
public class Student extends Person {
    private String grade;

    public Student(String name, int age, String grade) {
        super(name, age);
        this.grade = grade;
    }

    public String getGrade() {
        return grade;
    }
}
```

在上面的程式碼中，Student類繼承了Person類，並新增了一個major屬性和一個getMajor方法。

5. **多重繼承**
多重繼承是一種對象導向設計的概念，它允許不同的對象對相同的方法做出不同的反應。在Java中，多重繼承可以通過方法的重寫和方法的重載實現。

下面是一個展示多重繼承的示例程式碼：

```java
Copy code
public class Animal {
    public void makeSound() {
        System.out.println("The animal makes a sound");
    }
}

public class Dog extends Animal {
    public void makeSound() {
        System.out.println("The dog barks");
    }
}

public class Cat extends Animal {
    public void makeSound() {
        System.out.println("The cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal1 = new Animal();
        Animal animal2 = new Dog();
        Animal animal3 = new Cat();

        animal1.makeSound();
        animal2.makeSound();
        animal3.makeSound();
    }
}
```

在上面的程式碼中，我們定義了一個Animal類，和繼承自Animal類的Dog和Cat類。每個類都定義了自己的makeSound方法。在Main類中，我們創建了三個不同的對象：animal1、animal2和animal3。

animal1是Animal類的對象，animal2是Dog類的對象，animal3是Cat類的對象。

然後我們分別調用每個對象的makeSound方法。由於Dog和Cat類重寫了Animal類的makeSound方法，因此它們的makeSound方法會做出不同的反應。

以上是Java物件導向的基本概念，包括類、對象、繼承和多重繼承。物件導向的設計模式使得Java程式碼更具可重用性、可讀性和可維護性。