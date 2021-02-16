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

<<<<<<< HEAD
 - <span style="color : red;">StringBuffer</span> 연산들은 thread-safe하고 synchronized하다. (멀티쓰레드)
 - <span style="color : blue;">StringBuilder</span> 연산들은 thread-safe하지 않음. (단일쓰레드)

 <hr>
=======
 - Interpreter : 한 줄씩 해석.
 - JIT compiler : 같은 코드를 매번 해석하지 않고 캐싱하여, 바뀐 부분만 컴파일하고 나머지는 캐싱된 코드를 사용합니다. <span style="text-decoration:underline;">[출처](https://medium.com/@ahn428/java-jit-%EC%BB%B4%ED%8C%8C%EC%9D%BC%EB%9F%AC-c7d068e29f45)</span>

## 자바에서 String은 불변하는가?
- String의 리터럴들은 String pool에 저장되는데, 동일한 리터럴이면 String pool에서 같은 리터럴을 공유한다. <br>
만약 String이 변한다면 같은 리터럴을 참조하는 다른 곳에도 영향이 가기 때문에, String은 불변한다.
- 보안을 위해서. String은 File System, DB 커넥션, 네트워킹 등에 사용 된다.<br>
만약 String이 변경이 가능하다면 이러한 설정 등에 보안이 취약해질 수 있다.
>>>>>>> beebf771ac12590845c9eff993c42a65635b62b4

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
  - <span style="color : blue;"></span>
  - <span style="color : red;"></span>
  - <span style="color : blue;"></span>
  - <span style="color : red;"></span>
  - <span style="color : blue;"></span>