# java_while
반복문 문법


"인간은 반복적인 작업을 잘하지 못한다. 실수하고, 지루해한다. 컴퓨터는 이런 반복적인 작업을 대행하기 위해서 만들어진 기계다. 인간이 하기 싫어하는 바로 그 일을 컴퓨턱 대신하도록 하는 것이 반복문(loop,iteration)이다.

[반복문의 문법]
반복문의 문법은 몇 가지가 있다. 각각의 구문은 서로 대체 가능하기 때문에 상황과 취향에 따라서 선택해서 사용하면 된다.

while 문의 형식은 아래와 같다.

    while(조건) {
    반복 실행 영역
    }
    
아래의 예제를 실행해보자.

    package org.opentutuorials.javatutorials.loop;

    public class WhileDemo {
    
      public static void main(String[] args) {
      
        while (true) {
            System.out.println("Coding Everybody");
            
        }
        }
        }
        
이번에는 true를 false로 바꾼 아래의 예제를 실행해보자. 아래 코드는 아예 컴파일 조차 되지 않을 것이다. 반복 조건이 false이기 때문에 반복문이 한 번도 실행되지 않을 것이기 때문에 컴파일러가 오류를 발생시키는 것이다.

      While (false) {
      
      System.out.println("Coding Everyday");
      
      }
      
while 문은 반복조건이 참(true)이면 중괄호 구간을 반복적으로 실행한다. 조건이 false면 반복문이 실행되지 않는다. 여기서 true와 false는 반복의 종료조건이 되는데, 반복문에서 종료조건을 잘못 지정하면 무한 반복이 되거나, 반복문ㅇ 실행되지 않는다.

아래으 반복문은 i의 값을 1씩 순차적으로 증가시킴으로써 반복의 지속 여부를 결정하고 있다. 주석으로 첨부한 설명을 주의 깊게 살펴보자. 변수 i는 관습적으로 반복의 조건으로 사용하는 임의의 변수다. 변수 이름으로 다른 것을 사용해도 무방하다.


    int i = 0;
    
i의 값이 10보다 작다면 true, 크다면 false가 된다. 현재 i의 값은 0이기 때문에 이 반복문은 실행 된다.
    
    while (i<10) {
        System.out.println("Coding Everybody"+i);
        
 i의 값에 1을 더한다. 반복문의 중괄호으 마지막 라인에 도달하면 반복문은 반복문을 재호출 한다. 이때 i<10의 값을 검사하게 된다.
        
        i++;
        }
      
      
  [for]
  
 while문을 보면 반복의 횟수를 지정하기 위해서 while문 외부에 변수 i의 값을 초기화하고, while문 안에서 i의 값을 증가시키고 있다.
 이것은 코드를 산만하게 할 수 있다. 반복문에서 자주 사용하는 이런 패턴을 문법적인 형태로 만든 것이 for문이다.
 
 for문은 특정한 횟수만큼 반복 실행을 하는 경우에 자주 사용된다. 하지만 for문이나 while문이나 서로 대체 가능하다.
 취향에 따라서 서낵하면 된다. while과 for의 관계는 조건문으로 비유해서 생각해 볼수도 있을 것 같다.
 조건문의 핵심은 if이지만 연관된 로직들의 응집성을 높이기 위해서 else if, else 등이 도입된 것과 비슷한 관점으로 볼 수 있겠다. 이러한        방향성을 자신의 코드에 적용할 수 있도록 노력하자.
 
 형식은 아래와 같다.
 
    for(초기화; 종료조건; 반복실행) {
          반복적으로 실행될 구문
          }
          
  다음 예제를 보자.
  
  
     package org.opentutorials.javatutorials.loop;
     
     public class forDemo {
     
          public static void main(String [] args) {
          
          for (int i = 0; i < 10;, i++) {
          
          System.out.println("Coding Everybody" + i);
          
          }
          }
          }
          
  for문의 괄호 안에는 반복으 종료 조건이 들어온다. 종료 조건은 크게 3개의 부품으로 구성되는데 아래와 같다.
  
  * 초기화 : 반복문이 실행될 때 1호 실행된다.
  * 종료조건 : 초기화가 실행된 후에 종료조건이 실행된다. 종료조건의 값이 false일 때까지 반복문의 중괄호 구간의 코드가 반복 실행된다.
  * 중괋 구간의 실행이 끝나면 반복 실행이 실행된다. 일반적으로 이 곳에 i++와 같이 변수를 증가시키는 로직이 위치하고, 이것ㅇ 실행된 후에       종료조건이 실행된다. 종료조건이 false가 될 때까지 이 과정이 반복된다.
  
  
  coding everybody 뒤에 붙는 숫자를 2의 배수하고 싶다면 어떻게 해야 할까? 반복문이 없다면 한줄 한줄 수정해야 할 것이다. 반복문에서는 내용으 조금만 변경하면 된다.
  
     int i = 0;
     while (i < 10) {
        System.out.println("Coding everyday" +(i+1)*2);
        i++;
        }
        
        
 [반복문의 제어]
 반복자업을 중간에 중단시키고 싶다면 어떻게 해야할까.?
 
    package org.opentutorial.javatutorials.loop;
 
    public class BreakDemo {
    
      public static void main(String[] args) {
      
          for (int i = 0; i<10; i++) {
          
              if (i == 5)
              
              break;
              
              System.out.println("Coding Everyday" + i);
              }}}
              
              
              
[continue]

그럼 실행을 즉시 중단하면서 반복은 지속해각 하려면 어떻게 해야 할까? 설명이 어렵다면 예제를 보자. 이전 예제의 break르 continue로 변경했을 뿐이지만 결과는 전혀 다르다. continue 구문은 이명령이 나타나는 이후으 로직을 실행하지 않도록 하고 반복문은 중단하지 않고 다시 실행된다.
 
 
[반복문의 중첩]

    package org.opentutorials.javatutorials.loop;

    public class LoopDepthDemo {

      public static void main(String[] args) {
      for (int i = 0; i<10; i++ ) {
           for (int j = 0; j < 10; j++) {
           System.out.println(i + "" + j);
           }
          }
         }
         
 단순히 글자를 반복적으로 출력학 위해서 반복문을 사용한다 생각할 수도 있다. 하지만 반복문의 진가는 배열과 결합했을 때 나타난다.
 다음 토픽인 배열에서 반복문의 진가를 살펴보자..
         
         
         
         
