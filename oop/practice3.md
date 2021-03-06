# 作業練習（三）

新增一個「科目」（Subject）的類別，提供學生作為學習的目標物。

## 需求描述

學生除了擁有一般人的屬性與行為外，還可以學習指定的科目。

## 使用 UML 設計

使用案例圖：學生。

```uml
@startuml
:student: -right-> (學習)
@enduml
```

類別圖。

```uml
@startuml
Class Person {
    String name
    int birthYear
    + void hello()
}

Class Student {
    String school
    + void study(Subject subject)
}

Class Subject {
    String name
}

Person <|-- Student
Student "0..*" -- "0..1" Subject
@enduml
```

## 使用 BlueJ 實作

程式碼範例。

```java
class Person {
    String name;
    int birthYear;
    
    void hello() {
        System.out.println("Hi, My name is " + name + ".");
    }
}
```

Student。

```java
class Student {
    String school;
    
    void study(Subject subject) {
        //...
    }
}
```

Subject。

```java
class Subject {
    String name;
}
```

請將參考 UML 設計完成以上的程式碼練習，程式執行結果須符合以下的要求。

1. 建立一位或多位學生的物件。
2. 建立兩筆以上的科目物件，例如數學與國文。
3. 讓學生進行學習（study）每個科目。
