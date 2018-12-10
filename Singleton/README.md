# Definition
- 해당 클래스의 인스턴스가 하나만 만들어지고, 어디서든지 그 인스턴스에 접근할 수 있도록 하기 위한 패턴.

※ 게으른 인스턴스 생성(lazy instantiation)
- 인스턴스가 필요한 상황이 닥치기 전에는 아예 인스턴스를 생성하지않는다. 

TIP. 전역변수는 항상 인스턴스를 생성하지만 Singleton은 게으른 인스턴스 생성을 한다.

# Problem
- 멀티 프로세싱 환경에서 스레드가 동장한다면 인스턴스가 2개 이상이 생길 수 있다.

# Solution
<ol>
 <li>인스턴스를 필요할 때 생성하지 말고, 처음부터 만들어 버린다. => private static Singleton uniqueInstance = new Singleton(); 이러면 전역변수랑 별로 다를 것이 없다.</li></br>
 <li>동기화 시킨다.</li></br>
</ol>

# Main Source
![image](https://user-images.githubusercontent.com/21019088/49708155-bef48500-fc71-11e8-9cb1-dcd58afdce43.png)

# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49708121-97052180-fc71-11e8-85ad-749b1beb2a2e.png)

