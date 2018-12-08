
# Definition
- 교환 가능한 행동을 캡슐화하고 위임을 통해서 어떤 행동을 사용할지 결정한다. 
# Reason for use
- 아래의 Class Diagram을 참고하여 100마리의 Duck이 있다고 하고 울음소리는 "꽥꽥"이다. "콱콱"으로 수정한다면 오리들의 울음소리 메소드를 오버라이딩 하니 모든 오리의 메소드를 수정해야 한다. 하지만 100마리 각각에 Quack을 생성하도록 하면 Quack의 quack 메소드만 "꽥꽥"에서 "콱콱"으로 수정해 주면된다.
# Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49685508-bdb74100-fb27-11e8-993b-a65c673623e8.png)
# Execute
### MiniDuckSimulator
![image](https://user-images.githubusercontent.com/21019088/49685483-86489480-fb27-11e8-92f1-07dbbb82a813.png)
### MiniDuckSimulator1
![image](https://user-images.githubusercontent.com/21019088/49685500-9d878200-fb27-11e8-9685-ba02abea2375.png)

