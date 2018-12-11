# Definition
- 객체들을 트리 구조로 구성하여 부분과 전체를 나타내는 계층구조로 만들 수 있습니다. 이 패턴을 이용하면 클라이언트에서 개별 객체와 다른 객체들로 구성된 복합 객체(composite)를 똑같은 방법으로 다룰 수 있습니다. (이터레이터 패턴과 함께 쓰이면 효율적이다.)

# Main Sources
### Client
![image](https://user-images.githubusercontent.com/21019088/49791967-e84a0980-fd74-11e8-9591-39f32f75b8d8.png)

![image](https://user-images.githubusercontent.com/21019088/49791994-ff88f700-fd74-11e8-8e44-f9f9b771c763.png)

![image](https://user-images.githubusercontent.com/21019088/49792029-116a9a00-fd75-11e8-9938-08776e822801.png)

![image](https://user-images.githubusercontent.com/21019088/49792046-1d565c00-fd75-11e8-9bdd-9b42603293ee.png)

### Waitress
![image](https://user-images.githubusercontent.com/21019088/49792128-4971dd00-fd75-11e8-9be4-202855501022.png)

### MenuComponent
![image](https://user-images.githubusercontent.com/21019088/49792217-81792000-fd75-11e8-94c4-149adaf490e3.png)

### Menu
![image](https://user-images.githubusercontent.com/21019088/49792237-90f86900-fd75-11e8-9818-393e43929bbb.png)

![image](https://user-images.githubusercontent.com/21019088/49792999-6effe600-fd77-11e8-89d9-ec77fbaf56a9.png)
=> menuComponent는 자료형이 Menu나 MenuItem일 수 있다. 재귀적으로 자식으로 이동하다 보면 결국엔 MenuItem의 print()사용

### MenuItem
![image](https://user-images.githubusercontent.com/21019088/49792295-b71e0900-fd75-11e8-84cf-b343e4a099d5.png)

![image](https://user-images.githubusercontent.com/21019088/49792319-c735e880-fd75-11e8-937c-b7f9af6abcb3.png)

CompositeIterator와 NullIterator는 없다고 생각하면 된다. 쓰이지도 않으니..

# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49792802-fb5dd900-fd76-11e8-994b-e6defd4f09bb.png)

# menuIterator Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49792851-192b3e00-fd77-11e8-9d04-921de35132e9.png)

# Execute
### menuiterator/MenuTestDrive
![image](https://user-images.githubusercontent.com/21019088/49792894-2ea06800-fd77-11e8-8db2-e4d03b6b2959.png)


