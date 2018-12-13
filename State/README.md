# Definition
- 객체의 내부 상태가 바뀜에 따라서 객체의 행동을 바꿀 수 있습니다. 마치 객체의 클래스가 바뀌는 것과 같은 결과를 얻을 수 있습니다.

Question : 객체의 클래스가 바뀌는 것과 같은  이라는 표현을 쓴 이유는 무엇일까?
- 클라이언트 입장에서는 사용하는 객체의 행동이 완전히 달라진다면 마치 그 객체가 다른 클래스로부터 만들어진 객체처럼 느껴진다. 실제로는 다른 클래스로 변하는 게 아니고 구성을 통해서 여러 상태 객체를 바꿔가면서 사용한다.

# Reason for use
- 특정 클래스를 수정하지 않아도 상태만 바뀌면 메소드가 수정된 것 처럼 행동이 변하도록 하기 위해 사용한다.

# Main Sources
### Client
![image](https://user-images.githubusercontent.com/21019088/49806699-be580d80-fd9b-11e8-94c5-8bd505dc103d.png)

![image](https://user-images.githubusercontent.com/21019088/49806725-cd3ec000-fd9b-11e8-96e5-fb7346a13949.png)

### State
![image](https://user-images.githubusercontent.com/21019088/49806893-2f97c080-fd9c-11e8-9226-f1ac5f2ef642.png)

### GumballMachine
![image](https://user-images.githubusercontent.com/21019088/49806785-e9daf800-fd9b-11e8-8b61-3ab6da0d85e6.png)

![image](https://user-images.githubusercontent.com/21019088/49807086-974e0b80-fd9c-11e8-92ab-557ddc882481.png)

![image](https://user-images.githubusercontent.com/21019088/49806859-1858d300-fd9c-11e8-8eab-55ebcc8d5014.png)

# SoldOutState
![image](https://user-images.githubusercontent.com/21019088/49806940-48a07180-fd9c-11e8-9817-91f3867bfd70.png)

# NoQuarterState
![image](https://user-images.githubusercontent.com/21019088/49806986-5ce46e80-fd9c-11e8-917d-c388bd303185.png)

# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49805864-949de700-fd99-11e8-81d5-63a45c4df83c.png)

<ul>
<li>Context(GumballMachine) : 여러가지 내부 상태가 들어있을 수 있습니다. </li></br>
<li>State : 인터페이스로 모든 구상 상태 클래스에 대한 공콩 인터페이스를 정의한다.</li></br>
<li>ConcreteState(HasQuarterState, SoldState...) : Context로 부터 전달된 요청을 처리한다. 각 ConcreteState에서 그 
 요청을 처리하는 방법을 자기 나름의 방식으로 구현한다. Context에서 상태를 바꾸기만 하면 행동(insertQuarter()...)도 바뀌게 된다. 상태는 HasQuarterState, SoldState 등이 있으며 GumballMachine의 상태를 바꾸면 상태에서 동일하게 구현된 insertQuarter()의 내용은 다르므로 다른 행동을 하게 되는 것이다.</li></br>
</ul>

# gumballstatewinner Class Diagram
![18](https://user-images.githubusercontent.com/21019088/49806614-881a8e00-fd9b-11e8-831d-22ec43b26cea.gif)

# Execute
### gumballstatewinner/GumballMachineTestDrive
![image](https://user-images.githubusercontent.com/21019088/49806453-2b1ed800-fd9b-11e8-9283-2a6765c18e71.png)
