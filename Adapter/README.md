# Definition
- 한 클래스의 인터페이스를 클라이언트에서 사용하고자 하는 다른 인터페이스로 변환합니다. 어댑터를 이용하면 인터페이스 호환성 때문에 같이 쓸 수 없는 클래스들을 연결해서 쓸 수 있습니다.

# Example
- ducks 패키지를 예를 들어 클라이언트에서 testDuck(turkeyAdapter); turkeyAdapter는 Duck을 implements하고 생성 시 turkey 인스턴스를 매개변수로 받아 Duck.quack()을 turkey.gobble()로 Duck.fly()의 내용인 System.out.println("I'm flying")을 for(int i=0; i < 5; i++) {turkey.fly();}로 바꾼다. 클라이언트는 Turkey 인터페이스를 사용하기 위해 Duck 인터페이스를 Turkey 인터페이스로 변환해 주는 TurkeyAdapter를 사용하였다.  

# Main Sources
### Client(DuckTestDrive)
![image](https://user-images.githubusercontent.com/21019088/49719973-0abf2280-fca2-11e8-8e05-244708577973.png)

### Turkeyadapter
![image](https://user-images.githubusercontent.com/21019088/49720128-5e317080-fca2-11e8-8f21-4fb00a136117.png)

### Duck 인터페이스
![image](https://user-images.githubusercontent.com/21019088/49720155-68536f00-fca2-11e8-8959-7cd58c955af1.png)

### Turkey 인터페이스
![image](https://user-images.githubusercontent.com/21019088/49720174-7903e500-fca2-11e8-8819-3b085ed10c00.png)

# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49718861-b0709280-fc9e-11e8-9e2b-f1d3bad5cdb5.png)

# ducks Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49718905-d5fd9c00-fc9e-11e8-9bd8-038b8d609c3b.png)

# Execute
### ducks/DuckTestDrive
![image](https://user-images.githubusercontent.com/21019088/49719164-b2872100-fc9f-11e8-9e65-f02758967be2.png)

