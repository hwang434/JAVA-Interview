# Java Interview Questions and Answers | Java Tutorial | Java Online Training | Edureka
[출처](https://youtu.be/oYXivKMSEqM) 
<hr>

## 래퍼 클래스(Wrapper class)란 무엇인가?
 - 기본형을 객체로 다루기 위한 클래스.
 ``` java
  int i = 10;
  Integer iRef = new Integer(i);    //(Boxed)
  int j = iRef.intValue();          //(Unboxing)
  Integer kRef = i;                 //(AutoBoxing)
  int l = kRef;                     //(AutoUnboxing)

 ```
<br>
<hr>

## final, finally, finalize 차이점.

## final
 - final 클래스는 상속 불가능.
 - final 메소드는 overriding 불가능.
 - final 변수는 값 변경 불가능.

## finally
 - 중요한 코드에 사용 된다.
 - Exception이 발생하든 말든 무조건 실행.

## finalize
 - destructor(소멸자)와 비슷함.
 - Garbage Collector에 메모리가 수거 되기 전에 finalize 메서드를 수행합니다.
 - ex) 
 ``` java 
Demo d = new Demo();
d = null;
System.gc();        //Demo 클래스에 오버라이딩된 finalize 실행됨.
 ```

<hr>

## <span style="color : red;">StringBuffer</span> VS <span style="color :blue;">StringBuilder</span>

 - <span style="color : red;">StringBuffer</span> 연산들은 thread-safe하고 synchronized하다. (멀티쓰레드)
 - <span style="color : blue;">StringBuilder</span> 연산들은 thread-safe하지 않음. (단일쓰레드)

 <hr>

 ## <span style="color :red;">Stack</span>과 <span style="color : blue;">Heap</span> 메모리의 차이점
 - <span style="color : red;">Stack</span> 메모리는 1개의 쓰레드에만 사용 됨.
 - <span style="color : blue;">Heap</span> 메모리는 모든 곳에서 사용 됨.
 - <span style="color : red;">Stack</span>은 thread가 끝나기 전까지 존재.
 - <span style="color : blue;">Heap</span>은 프로그램의 시작부터 끝까지 존재.

 - <span style="color : red;">Stack</span> 예시 : 기본형 지역 변수, 참조 변수
 - <span style="color : blue;">Heap</span> 예시 : object가 만들어지면 전부 Heap에 저장됨.

 <hr>

 ## <span style="color : red;">ArrayList</span> vs <span style="color : blue;">Vector</span>
  - <span style="color : red;">Not Syncronized</span>
  - <span style="color : blue;">Synchronized</span>
  - <span style="color : red;">Not thread safe</span>
  - <span style="color : blue;">thread safe</span>
  - <span style="color : red;">fast</span>
  - <span style="color : blue;">slow</span>

<hr>

## <span style="color : red;">HahMap</span> vs <span style="color : blue;">HashTable</span>
  - <span style="color : red;">Not Syncronized</span>
  - <span style="color : blue;">Synchronized</span>
  - <span style="color : red;">Not thread safe</span>
  - <span style="color : blue;">thread safe</span>
  - <span style="color : red;">fast</span>
  - <span style="color : blue;">slow</span>
  - <span style="color : red;">null key를 허용하고 value로 null 값들이 올 수 있다.</span>
  - <span style="color : blue;">key나 value 둘다 null 허용하지 않음.</span>

<hr>

## equals() Vs ==
 - equal() 메소드는 Object에 value를 비교한다.
 - == 연산자는 reference(참조)를 비교함.

<hr>

## <span style="color : red;">Abstract Class</span> VS <span style="color : blue;">Interface</span>
 - <span style="color : yellow;">둘다 객체 생성은 불가능하다.</span>
 - <span style="color : red;">멤버나 생성자를 가짐.</span>
 - <span style="color : blue;">모든 메서드는 추상 메서드이고, 멤버는 public static final.</span>
 - <span style="color : blue;">인터페이스는 1.8 버젼부터 default, public static 메서드 지원함.</span>
``` java
abstract class AbstractClass {
    int a = 0;                      //멤버
    abstract void method01();       //추상메서드
    
    AbstractClass() {               //생성자

    }

}
interface Readable {
    int a = 4;              //public static final int a = 4;
    void method01();        //public abstract void method01();
    
    //1.8부터
    default void method02() {
        //메서드 몸통.
    }
    public static void method03() {
        //메서드 몸통.
    }

}
```

d