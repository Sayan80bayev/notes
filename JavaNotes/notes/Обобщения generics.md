---
aliases: дженерики
tags: Java/Обобщения
---
Обобщения (generics) - это возможность языка Java использовать обобщения типов данных. Преимущества использования обобщений:
- Безопасность типов
	Когда ошибку типа переменной можно отследить на этапе компиляции
- Повторное использование кода
	Один раз написав программу можно сделать так, чтобы она работала с разными типами или только с определенными классами.

Т.о. добавлена возможность параметризации классов, интерфейсов и методов каким-то типом.
Вместо конкретно int, String можно объявить и затем использовать некоторую переменную, в качестве которой будет поставлен тип, удовлетворяющий условиям.

### Для чего нужны дженерики
Обобщения добавляют стабильность коду, позволяя обнаруживать несоответствия типов во время компиляции.

Типизированные параметры позволяют повторно использовать один и тот же код с разными входными данными.
### Параметр Vs Аргумент в дженериках
Параметр - тип данных, которыми оперируют классы, интерфейсы указанные в дженериках. Параметр типа используется при объявлении дженерик типов. Например, Box<`T`> - это параметр типа

Аргумент типа. Тип объекта, который может использоваться вместо параметра типа. Например, Box<`Paper`> - аргумент типа.

### Ограничения generics 
1. Параметризация возможна только ссылочным типом данных
	String, Integer, int[] - пойдет; int - не пойдет
2. Внутри параметризированных классов или методов нельзя создать экземпляр или массив **T**, также не работает **instanceof**.
3. ![[Ограничения Generics.png]]

## Классы, интерфейсы, методы, конструкторы, сырые типы (raw)
 [[Параметризованные классы Generics]]

 [[Параметризованные методы и конструкторы]]

 [[Raw Type]]

### Параметризованные интерфейсы
Параметризованные интерфейсы специфицируются так же, как и обобщенные классы:

```java
public interface MyInterface<T> {
    T someMethod(T t);
}
```
## Дженерики и исключения
### Можно ли выбрасывать исключения generic-типа
Короткий ответ – да. 

Пример
```java
class MyException<T extends Exception> {
    private T exception;

    public MyException(T exception) {
        this.exception = exception;
    }

    public void handleException() {
        try {
            throw exception;
        } catch (T e) {
            System.out.println("Caught exception: " + e.getMessage());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        MyException<IOException> ioException = new MyException<>(new IOException("IO exception"));
        ioException.handleException();

        MyException<NullPointerException> nullPointerException = new MyException<>(new NullPointerException("Null pointer exception"));
        nullPointerException.handleException();
    }
}

```
### Дженерики в исключениях – что можно, а что нельзя
2. Нельзя использовать дженерик в catch.
Множественные блоки catch должны идти без повторений, в определенном порядке – от специфичного класса к более базовому. Стирание типов-параметров в связи с этими правилами добавило бы путаницу, не неся особой пользы.
3. Нельзя параметризовать класс-исключение типами.
Если вы попытаетесь скомпилировать конструкцию вида `class MyException<T> extends Throwable {}`, то увидите ошибку `generic class may not extend java.lang.Throwable`.
4. Можно реализовывать исключением generic-интерфейс.
Исключение вполне может быть, например **Comparable** или **Iterable**. Механизм обработки исключений работает на классах, никак не затрагивая интерфейсы.

>[!Note]
>Generics для исключений не является часто встречающейся практикой, и в большинстве случаев использование обычных классов исключений без generics является более удобным и простым подходом.
## Символ wildcard
<`?`> Дословно карта Джокер - любой класс. 
```java
boolean sameAvg(Average<?> ob) {
    return average() == ob.average();
}
```
Мета символ просто совпадает с любым достоверным объектом класса `Average`

Знак вопроса (?) известен как wildcard (подстановка) в generic программировании.
Wildcards можно использовать как тип параметра, поля или локальной переменной, иногда как возвращаемый тип.
## Принцип PECS 
**Принцип PECS — Producer Extends Consumer Super.**

Чтобы писать интерфейсы, абсолютно безопасные с точки зрения типов, но при этом не имеющие бессмысленных и создающих неудобства ограничений.
![[IMG PECS принцип.png]]
Для наглядности представим, что у нас есть иерархия классов, начинающаяся с Class0, который является предком для Class1, который в свою очередь является предком для Class2, и т.д. И есть некий метод, который принимает в качестве аргумента коллекцию, типизированную wildcard с верхней границей.

```java
someMethod (List<? extends Class3> list)
```
**Какие объекты можно получить из** `List<? extends Class3> list`?

Досрочный ответ очевиден: объекты, содержащиеся в list, являются потомками Class3, следовательно, из list можно получить объекты Class4, Class5, Class6 и т.д. Если вы ответили именно так, то у меня для вас плохая новость – «очко уходит телезрителям»! Следующий кусок кода не скомпилируется:

```java
public static void someMethod (List<? extends Class3> list) {    
	Class4 class4 = list.get(0); 
}
```

Зато вот такой код будет корректным:

```java
public static void someMethod (List<? extends Class3> list) {
    Class2 class2 = list.get(0);
}
```
Из данного утверждения логично вытекает следующий вопрос: **почему wildcard с super может принимать объекты, а wildcard с extend – нет?** И на него мы уже практически нашли ответ выше. `List<? extends Class3>` - на деле может оказаться листом объектов самого «младшего» класса, тогда как конструкция `List<? super Class3>` гарантирует, что при любом раскладе в листе будут объекты имеющие тип не «младше» класса Class3. Поэтому, следующий кусок кода скомпилируется

```java
public static void someMethod (List<? super Class3> list) {
    list.add(new Class4());
}
```

А такой, нет:

```java
public static void someMethod (List<? super Class3> list) {
    list.add(new Class2());
}
```
![[PECS Img.png]]
![[Инварианты и тд Img.png]]
[Подробнее про PECS](https://habr.com/ru/articles/559268/)

Источники [Дженерики Java - Java программирование | ExamClouds](https://www.examclouds.com/ru/java/java-core-russian/generics-russian#header1)
![[Ревью вопрос.png]]
