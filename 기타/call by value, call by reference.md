### call by value

값에 의한 호출

함수에 변수의 복사본이 전달되어 함수 내에서 해당 값이 변경되어도 호출자의 변수는 영향을 받지 않는다

원래의 값에 영향이 없어 안전하지만 복사를 위해 메모리 사용량이 늘어난다

```java
public class Main {
    public static void main(String[] args) {
        int num = 10;
        System.out.println("Before : " + num);

        // call by value
        square(num);
        System.out.println("After : " + num);
    }
    public static void square(int x) {
        x *= x;
        System.out.println("Inside : " + x);
    }
}

```

```c
Before : 10
Inside : 100
After : 10
```


### call by reference

참조에 의한 호출

함수에 변수의 참조 값을 전달해, 함수 안에서 인자의 값이 변경되면 호출자의 변수값도 변경된다

자바에는 인자 전달이 call by value 이기 떄문에 call by reference방식은 지원하지 않는다. 
하지만 객체를 통한 참조를 통해 객체의 상태를 변경할 수 있다

```java

class Dog {
    String name;
    Dog(String name) {
        this.name = name;
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog("Buddy");
        System.out.println("Before : " + dog.name);
        
        // call by value for objects
        changeName(dog);

        System.out.println("After : " + dog.name);
    }

    public static void changeName(Dog dog) {
        dog.name = "Max";
        System.out.println("Inside : " + dog.name);
    }
}

```

```c
Before : Buddy
Inside : Max
After : Max

```


---
### 출처
[[개발자의 교양] C언어에는 call by reference가 없다고???](https://velog.io/@ksk0605/%EA%B0%9C%EB%B0%9C%EC%9E%90%EC%9D%98-%EA%B5%90%EC%96%91-C%EC%96%B8%EC%96%B4%EC%97%90%EB%8A%94-call-by-reference%EA%B0%80-%EC%97%86%EB%8B%A4%EA%B3%A0)