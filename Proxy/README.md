# Definition
- 어떤 객체에 대한 접근을 제어하기 위한 용도로 대리인이나 대변인에 해당하는 객체를 제공하는 패턴

# Reason for use
- 실제 작업을 행하는 오브젝트를 감싸서, 실제 오브젝트를 요청하기 전이나 후에 인가 처리(보호)나, 생성 자원이 많이 드는 작업에 대해 백그라운드 처리 (가상), 원격 메소드를 호출하기 위한 작업(원격 프록시) 등을 하는데 사용한다.

# Example
### 방화벽 프록시
- 일련의 네트워크 자원에 대한 접근을 제어함으로써 주 객체를 "나쁜" 클라이언트들로부터 보호해 줍니다.

### Smart Reference Proxy
- 주 객체가 참조될 때마다 추가 행동을 제공합니다. 객체에 대한 레퍼런스 개수를 센다든가 하는 식으로 말이죠.

### Caching Proxy
- 비용이 많이 드는 작업의 결과를 임시로 저장해 줍니다. 여러 클라이언트에서 결과를 공유하게 해줌으로써 계산 시간 또는 네트워크 지연을 줄여주는 효과도 있습니다.

### Synchronization Proxy
- 여러 스레드에서 주 객체에 접근하는 경우에 안전하게 작업을 처리할 수 있게 해 줍니다.

### Complexity Hiding Proxy
- 복잡한 클래스들의 집합에 대한 접근을 제어하고, 그 복잡도를 숨겨줍니다. Facade Proxy라고 부르기도 합니다. 이 프록시와 퍼사드 패턴의 차이점은 프록시에서는 접근을 제어한다는 차이가 있습니다.

### Dynamic Proxy
- 프로그램 실행 중 동적으로 만들어지는 프록시

# Main Sources (Dynamic Proxy)
### Client
![image](https://user-images.githubusercontent.com/21019088/49913859-78ea2c00-fed2-11e8-9383-949f2124a779.png)

![image](https://user-images.githubusercontent.com/21019088/49913878-928b7380-fed2-11e8-9b5d-5ab3280bfb88.png)

![image](https://user-images.githubusercontent.com/21019088/49913905-adf67e80-fed2-11e8-829a-52527f464f95.png)

getOwnerProxy를 통해 실행 중에 Proxy.newProxyInstance로 Proxy를 생성하며 이때 PersonBean(Subject)를 implements하고, 이 Proxy는 OwnerInvocationHandler(InvocationHandler)를 구성한다.

### PersonBean
![image](https://user-images.githubusercontent.com/21019088/49915968-c919bc00-fedb-11e8-85f7-bf9fad2f9830.png)

### OwnerInvocationHandler
![image](https://user-images.githubusercontent.com/21019088/49915945-abe4ed80-fedb-11e8-8f23-22634263f2a8.png)

### PersonBeanlmpl
![image](https://user-images.githubusercontent.com/21019088/49915982-e51d5d80-fedb-11e8-8475-ef40b97cddab.png)

![image](https://user-images.githubusercontent.com/21019088/49915992-f6666a00-fedb-11e8-82a9-ef48366b0703.png)

# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49913436-ec8b3980-fed0-11e8-88fd-d9ebf3834c7b.png)

- Subject : 인터페이스로 Proxy와 RealSubject 모두 Subject 인터페이스를 구현합니다. 이렇게 하면 어떤 클라이언트에서든 프록시를 주 객체하고 똑같은 식으로 다룰 수 있습니다.

- RealSubject : 실제 작업을 대부분 처리하는 객체를 나타냅니다. Proxy는 이 객체에 대한 접근을 제어하는 객체죠.

- Proxy : 실제 작업을 처리하는 객체에 대한 레퍼런스가 들어있습니다. 실제 객체가 필요하면 그 레퍼런스를 이용해서 요청을 전달하죠. Proxy에서 RealSubject의 인스턴스를 생성하거나, 그 객체의 생성과정에 관여하는 경우가 많습니다.

# Dynamic Proxy Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49916194-1e0a0200-fedd-11e8-9cda-798b4fa92bcd.png)

Proxy에서 메소드 호출을 받으면 항상 InvocationHandler에 진짜 작업을 부탁한다고 생각하면 된다.

# javaproxy Class Diagram
![19](https://user-images.githubusercontent.com/21019088/49916032-49402180-fedc-11e8-85be-ddc71927134e.gif)

# Execute
![image](https://user-images.githubusercontent.com/21019088/49916067-6c6ad100-fedc-11e8-8750-9fa794d3685d.png)

