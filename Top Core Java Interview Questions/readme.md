# Top Core Java Interview Questions || Core Java Interview Questions and Answers [MOST ASKED]

[출처](https://youtu.be/PwiuAebCruY) 
<hr>

## 자바가 100% 객체 지향이 아닌 이유.
 - 기본형 자료형 때문이다. <br>
   100% 자료형으로 사용하기 위해선 기본형을 Boxing하는 wrapper 클래스를 사용하면 된다.
<br>

## 자바에서 <span style="color:red; text-decoration:underline;">포인터</span>를 쓰지 않는 이유.
 - 메모리를 직접 제어하는 건 안전하지 않다.
 - 자바의 경우 간결한 코드로 알려져 있는데, 포인터를 사용하면 이와 모순되는 언어가 된다.
 - JVM<에서 메모리를 할당하기 때문에, 포인터를 쓸 이유가 없다.

## JIT 컴파일러란?

![컴파일 과정](/images/topcore/01.png)

 - Interpreter : 한 줄씩 해석.
 - JIT compiler : 같은 코드를 매번 해석하지 않고 캐싱하여, 바뀐 부분만 컴파일하고 나머지는 캐싱된 코드를 사용합니다. <span style="text-decoration:underline;">[출처](https://medium.com/@ahn428/java-jit-%EC%BB%B4%ED%8C%8C%EC%9D%BC%EB%9F%AC-c7d068e29f45)</span>

## 자바에서 String은 불변하는가?
- String의 리터럴들은 String pool에 저장되는데, 동일한 리터럴이면 String pool에서 같은 리터럴을 공유한다. <br>
만약 String이 변한다면 같은 리터럴을 참조하는 다른 곳에도 영향이 가기 때문에, String은 불변한다.
- 보안을 위해서. String은 File System, DB 커넥션, 네트워킹 등에 사용 된다.<br>
만약 String이 변경이 가능하다면 이러한 설정 등에 보안이 취약해질 수 있다.

## marker interface란?
- 멤버나 멤버 함수 같이 내부에 아무 것도 없는 인터페이스.
- JDK나 컴파일러에 meta 데이터를 주는 용도.
- ex) Serialzable, Cloneable

## private이나 static 메소드는 override 할 수 있나?
 - 할 수 없다.
 - sub class에서 super class에 private 요소들은 접근이 불가능하다.
 - sub class에 super class와 똑같은 static 메소드를 만들면 super class에 static 메소드를 숨겨준다. (Method hiding)

 ## finally는 항상 실행 되나?
 - System.exit() 메서드가 호출 될 경우 실행 되지 않음.
 - 시스템 에러가 발생할 경우, 실행 되지 않음.

