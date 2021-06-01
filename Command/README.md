# Definition
- 커맨드 패턴을 이용하면 요구 사항을 객체로 캡슐화(리시버(Light)와, undo, excute메서드를 캡슐화 한 LightOnCommand) 할 수 있으며, 매개변수를 써서 여러 가지 다른 요구 사항을 집어넣을 수 있다. (클라이언트에서 인보커의 setCommand메서드를 실행시킬 때 요구사항(LightOnCommand...)을 매개변수로 넣는다.) 또한 요청 내역을 큐에 저장하거나 로그로 기록할 수도 있으면, 작업취소 기능도 지원 가능하다.

식당을 예로들어보자.

1. 손님이 웨이터에게 주문을 한다.
2. 웨이터가 고객의 주문을 주문서에 적는다.
3. 웨이터는 주문서를 주방에 전달하여 주문을 요청한다.
4. 요리사는 주문서에 적힌 주문대로 음식을 자신의 노하우로 만든다.

손님        ==    클라이언트    ==    RemoteLoader</br>
웨이터    ==    인보커 객체   ==    RemoteControlWithUndo</br>
주문서    ==    커맨드 객체   ==    LightOnCommand</br>
주방장    ==    리시버 객체   ==    Light</br>
주문을 하는것 == setCommand()</br>
주문을 요청하는것 == execute()</br>

# Reason for use
※ 일급 객체
- 다른 객체들에 적용 가능한 연산을 모두 지원하는 객체를 가리킨다.
<ol>
<li>커맨드를 이용하면 컴퓨테이션(computation)의 한 부분(리시버와 일련의 행동)을 패키지로 묶어서 일급 객체 형태로 전달하는 것도 가능하다.</li></br>
<li>요청을 로그에 기록하기도 좋다. 각 커맨드가 실행될 때 마다 디스크에 그 내역을 저장한다. 시스템이 다운된 후에, 객체를 다시 로딩하고 순서대로 작업을 다시 처리 하여 복구하기에 적합하다.</li></br>
</ol>

# Question
#### 항상 리시버가 필요한가요? 커맨드 객체에서 execute()를 구현해 버리면 안 되나요?
- 물론 커맨드 객체에서 대부분의 행동을 처리해도 됩니다. 하지만 그렇게 하면 여기에서 우리가 했던 수준으로 인보커와 리시버를 분리시키는 것이 불가능해진다.(인보커에서 setCommand의 매개변수로 LightOnCommand를 받는데 이게 리시버이면서 커맨드 객체가 되면 분리가 불가능 하다는 말이다.)
# undo Main Sources
## Client
![image](https://user-images.githubusercontent.com/21019088/49713751-6f23b700-fc8d-11e8-8c94-88c27efa2343.png)
## Invoker
![image](https://user-images.githubusercontent.com/21019088/49713790-a003ec00-fc8d-11e8-8799-0480a73cdd85.png)
## Command
![image](https://user-images.githubusercontent.com/21019088/49713848-d3df1180-fc8d-11e8-8ed5-da210f654762.png)
## Receiver (Light와 LightOnCommand는 연관관계가 될 수 있다. this.right = new Light를 호출하는 함수가 안 쓰일수도 있기 때문이다.)
![image](https://user-images.githubusercontent.com/21019088/49713866-e3f6f100-fc8d-11e8-941a-a86d52b2ebc5.png)
## ConcreteCommand
![image](https://user-images.githubusercontent.com/21019088/49713882-f4a76700-fc8d-11e8-90c4-7c74c4043ee3.png)

# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49713617-e147cc00-fc8c-11e8-92a9-766f36dbcdbc.png)

# undo Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49713677-1b18d280-fc8d-11e8-872e-573dc34aa2cc.png)

# Execute
![image](https://user-images.githubusercontent.com/21019088/49713934-31735e00-fc8e-11e8-84f0-62aa9e30c886.png)

