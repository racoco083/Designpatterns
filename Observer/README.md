
# Definition
- 한 객체의 상태가 바뀌면 그 객체에 의존하는 다른 객체들한테 연락이 가고 자동으로 내용이 갱신되는 방식으로 일대다(one-to-many)의존성을 정의한다. Observer 인터페이스만 implements 한다면 무엇이든 Observer 클래스가 될 수 있다.

※ 느슨한 결합 
- 두 객체가 느슨하게 결합되어 있다는 것은, 그 둘이 상호작용을 하긴 하지만 서로에 대해 서로 잘 모른다는 것을 의미한다. Observer 패턴에서는 주제와 Observer가 느슨하게 결합되어 있는 객체 디자인을 제공한다.

※ JDK 내장 옵저버 패턴의 단점과 한계 (java.util.Observable)
- Observable이 클래스기 때문에 서브클래스를 만들어야 한다는 점이 문제다. 이미 다른 수퍼클래스를 확장하고 있는 클래스에 Observable의 기능을 추가할 수 없기 때문이다. 그래서 재사용성에 제약이 생긴다. (직접 구현하여 Observable을 interface로 만들면 해결된다.)

# Reason for use
- 옵저버 패턴은 주제와 옵저버가 느슨하게 결합되어있는 객체 디자인을 제공. 주제가 옵저버에 대해서 아는 것은 옵저버가 특정 인터페이스(Observer 인터페이스)를 구현 한다는 것 뿐. 옵저버는 언제든지 새로 추가할 수 있음. (주제는 Observer인터페이스 구현하는 객체 목록에만 의존하기때문) 새로운 형식의 옵저버를 추가하려해도 주제를 전혀 변경할 필요가 없음. (새로운 클래스에서 Observer 인터페이스만 구현해주면됨) 주제나 옵저버가 바뀌더라도 서로에게 전혀 영향을 주지않음. 그래서 주제와 옵저버는 서로 독립적으로 재 사용할수 있음.

- 느슨하게 결합하는 디자인을 사용하면 변경 사항이 생겨도 무난히 처리할 수 있는 유연한 객체지향 시스템을 구축할수 있다. (객체 사이의 상호 의존성을 최소화 할 수 있기 때문)
# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49686448-1262b800-fb38-11e8-8eaa-423cb2efd4c9.png)
# weather Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49686452-24445b00-fb38-11e8-85bf-59ac3a7bbd59.png)
# Execute
### weather/WeatherStation
![image](https://user-images.githubusercontent.com/21019088/49686545-68842b00-fb39-11e8-8efe-2c0be004e80c.png)
### weather/WeatherStationHeatIndex
![image](https://user-images.githubusercontent.com/21019088/49686550-7a65ce00-fb39-11e8-9773-cc3d0395cb1e.png)
### P.S
<ul>
  <li>weatherobservable는 자바 내장 Observable 클래스를 사용한 것이다.</li></br>
</ul>
