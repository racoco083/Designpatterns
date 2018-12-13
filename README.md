# Head First Designpatterns
### 디자인 원칙
<ol>
  <li>애플리케이션에서 달라지는 부분을 찾아 내고, 달라지지 않는 부분으로부터 분리 시킨다.</li></br>
  <li>구현이 아닌 인터페이스에 맞춰서 프로그래밍한다.</li></br>
  <li>상속보다는 구성을 활용한다.</li></br>
  <li>서로 상호작용을 하는 객체 사이에서는 가능하면 느슨하게 결합하는 디자인을 사용해야 한다.</li></br>
  <li>클래스는 확장에 대해서는 열려 있어야 하지만 코드 변경에 대해서는 닫혀 있어야 한다.</li></br>
  <li>추상화된 것에 의존하도록 만들어라. 구상 클래스에 의존하도록 만들지 않도록 한다.</li></br>
  <li>정말 친한 친구하고만 얘기하라.(Principle of Least Knowledge)</li></br>
  <li>먼저 연락하지 마세요. 저희가 연락 드리겠습니다.(Hollywood Principle)</li></br>
  <li>클래스를 바꾸는 이유는 한 가지 뿐이어야 한다.(SRP: The Single Responsibility Principle)</li></br>
 </ol>
 
#### 각 디자인 원칙에 대해 이해하기 쉽도록 설명 해 놓은 사이트
http://plposer.tistory.com/13
 
 ### 패턴
 <ol>
  <li>데코레이터 패턴 : 객체를 감싸서 새로운 행동을 제공합니다.</li></br>
  <li>스테이트 패턴 : 상태를 기반으로 한 행동을 캡슐화한 다음 위임을 통해서 필요한 행동을 선택합니다.</li></br>
  <li>이터레이터 패턴 : 컬렉션이 어떤 식으로 구현되었는지 드러내진 않으면서도 컬렉션 내에 있는 모든 객체에 대한 반복 작업을 처리할 수 있게 해 줍니다.</li></br>
  <li>퍼사드 패턴 : 일련의 클래스에 대해서 간단한 인터페이스를 제공합니다.</li></br>
  <li>스트래티지 패턴 : 교환 가능한 행동을 캡슐화하고 위임을 통해서 어떤 행동을 사용할지 결정합니다.</li></br>
  <li>프록시 패턴 : 객체를 감싸서 그 객체에 대한 접근을 제어합니다.</li></br>
  <li>팩토리 메소드 패턴 : 생성할 구상 클래스를 서브클래스에서 결정합니다.</li></br>
  <li>어댑터 패턴 : 객체를 감싸서 다른 인터페이스를 제공합니다.</li></br>
  <li>옵저버 패턴 : 상태가 변경되면 다른 객체들 한테 연락을 돌릴 수 있게 해 줍니다.</li></br>
  <li>템플릿 메소드 패턴 : 알고리즘의 개별 단계를 구현하는 방법을 서브클래스에서 결정합니다.</li></br>
  <li>컴포지트 패턴 : 클라이언트에서 객체 컬렉션과 개별 객체를 똑같이 다룰 수 있도록 해 줍니다.</li></br>
  <li>싱글턴 패턴 : 딱 한 객체만 생성되도록 합니다.</li></br>
  <li>추상 팩토리 패턴 : 클라이언트에서 구상 클래스를 지정하지 않으면서도 일군의 객체를 생성할 수 있도록 해 줍니다.</li></br>
  <li>커맨드 패턴 : 요청을 객체로 감쌉니다.</li></br>
 </ol>
 
#### 각 패턴 폴더에서 좀 더 구체적으로 설명해 놓았습니다.
 
### What is the SOLID？
- S: Single responsibility
- O: Open-closed principle
- L: Liskov substitution principle
- I: Interface segregation principle
- D: Dependency inversion

#### SOLID에 대해 요약 되어 있습니다.
https://ko.wikipedia.org/wiki/SOLID_(%EA%B0%9D%EC%B2%B4_%EC%A7%80%ED%96%A5_%EC%84%A4%EA%B3%84)

#### SOLID에 대해 자세하게 설명되어 있습니다.
http://www.nextree.co.kr/p6960/


### References
https://github.com/brodieroy/Study/wiki/(U)-UML-%ED%81%B4%EB%9E%98%EC%8A%A4%EA%B0%84-%EA%B4%80%EA%B3%84(association,-composition,-aggregation,-dependency)

https://gmlwjd9405.github.io/2018/07/04/class-diagram.html

https://gmlwjd9405.github.io/tags.html#%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4

http://hyeonstorage.tistory.com/category/%3D%3D%20JAVA%20%3D%3D/Design%20Patterns

http://jusungpark.tistory.com/category/DesignPattern
