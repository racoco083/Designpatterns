# Definition
- 컴파운드 패턴이란 반복적으로 생길 수 있는 문제를 해결하기 위한 용도로 두 개 이상의 패턴을 결합하여 사용하는 것을 뜻합니다.

# combining.observer에 적용한 패턴
<ol>
<li>처음에 수많은 Quackable 들이 존재</li></br>
<li>갑자가 거위가 나타나서는 자기도 Quackable이 되고 싶다고함 (어댑터 패턴)</li></br>
<li>꽥학자들이 등장해서 꽥소리 회수를 세고 싶다고함 (데코레이터 패턴)</li></br>
<li>꽥학자들이 QuackCounter로 장식되지 않은 Quackable 객체가 있을것을 걱정 (추상팩토리 패턴)</li></br>
<li>모든 오리와 거위, Quackable 객체들을 관리하는 게 힘들어지기 시작 - 오리떼로 관리 (컴포지트 패턴)</li></br>
<li>꽥학자들은 Quackable에서 꽥소리를 냈을 때 그런 일이 있었다는 것을 연락받고 싶어함 (옵저버 패턴)</li></br>
</ol>

# combining.observer Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49939910-76fb8980-ff21-11e8-8829-7bebe2823b21.png)

# Execute
![image](https://user-images.githubusercontent.com/21019088/49939867-5a5f5180-ff21-11e8-9b83-f4cc24b44125.png)
