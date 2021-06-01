# Factory Method Pattern (수정 필요)
## Definition
- 사용하는 서브클래스에 따라 생산되는 객체 인스턴스가 결정되는 것.
pizzaStore의 createPizza가 팩토리 메소드이다. pizzaStore는 클라이언트가 시카고의 피자를 주문하는지 뉴욕의 피자를 주문하는지 모른다. 뉴욕인지 시카고 인지는 pizzaStore의 서브클래스인 NYPizzaStore, ChicagoPiazzaStore에서 결정한다.
## Reason for use
※ 의존성 뒤집기 원칙
- 추상화된 것에 의존하도록 만든다. 구상 클래스에 의존하도록 만들지 않도록 한다.

PizzaStore -> NYStyleCheesePizza
PizzaStore -> ChicagoStypeCheesePizza
PizzaStore -> NYStyleVeggiePizza
이런식으로 의존이 되던 좋지않은 디자인이

PizzaStore -> Pizza
Pizza <- NYStyleCheesePizza
Pizza <- ChicagoStyleCheesePizza
Pizza <- NYStyleVeggiePizza
이런식으로 의존관계게 뒤집어지는 형상.

팩토리 메소드 패턴을 적용하고 나면 고수준 구성요소(PizzaStore)와 저수준 구성요소(NYStyleCheesePizza, ChicagoStylePizza, ..) 들이 모두 추상 클래스인 Pizza에 의존하게됨. (고수준 모듈과 저수준 모듈이 둘다 하나의 추상 클래스에 의존)

팩토리 메소드 패턴이 의존성 뒤집기 원칙을 준수하기 위해 쓸 수 있는 유일한 기법은 아니지만 가장 적합한 벙법 가운데 하나.
### 의존성 뒤집기 원칙에 위배되는 객체지향 디자인을 피하는데 도움이 되는 가이드.
![image](https://user-images.githubusercontent.com/21019088/49694723-abdea800-fbd2-11e8-96cc-7d56d914c3a0.png)

## Main Sources
### fmClient
![fmclient](https://user-images.githubusercontent.com/21019088/49694780-f6145900-fbd3-11e8-8dcf-a488fdc33713.PNG)
### fmPizzaStore
![fmpizzastore](https://user-images.githubusercontent.com/21019088/49694782-fa407680-fbd3-11e8-9aab-9da865306af9.PNG)
### fmNYPizzaStore
![fmnypizzastore](https://user-images.githubusercontent.com/21019088/49694784-fe6c9400-fbd3-11e8-923f-d180b0eaf926.PNG)
## Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49694732-e6e0db80-fbd2-11e8-968e-28da2c69a6bd.png) 
## pizzafm Class Diagram
![11](https://user-images.githubusercontent.com/21019088/49695064-63c28400-fbd8-11e8-8a69-d2620c68a850.gif)
## Execute
### pizzafm/PizzaTestDrive
![image](https://user-images.githubusercontent.com/21019088/49694757-8605d300-fbd3-11e8-84cc-9f10cddb2d87.png)

# Abstract Factory Pattern
## Definition
-  제품군을 생성하기 위한 인터페이스를 생성 그 인터페이스를 구성하여 사용할수 있게끔 하는것. 소스코드는 팩토리 메소드 패턴이 적용되었지만 다른 패턴을 적용할 수도 있다.
## Reason for use
- 일련의 제품들(ThinCrustDough, FreshClams...)을 생성하는 데 쓰일 인터페이스를 정의하기 위해 만들어진다.
## Main Sources
### afClient
![afclient](https://user-images.githubusercontent.com/21019088/49695101-f2cf9c00-fbd8-11e8-96dd-5d1c4040d239.PNG)
### afPizzaIngredientFactory
![afpizzaingredientfactory](https://user-images.githubusercontent.com/21019088/49695104-f82ce680-fbd8-11e8-83a3-6f2980d39d1e.PNG)
### afNYPizzaIngredientFactory
![afnypizzaingredientfactory](https://user-images.githubusercontent.com/21019088/49695108-fcf19a80-fbd8-11e8-8b0f-a14bf3fdde3b.PNG)
## Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49694965-bb5ff000-fbd6-11e8-94ed-b0a849354b76.png)
### 역할이 수행하는 작업
#### AbstractFactory
실제 팩토리 클래스의 공통 인터페이스
#### ConcreteFactory
구체적인 팩토리 클래스로 AbstractFactory 클래스의 추상 메서드를 오버라이드함으로써 구체적인 제품을 생성한다.
#### AbstractProduct
제품의 공통 인터페이스
#### ConcreteProduct
구체적인 팩토리 클래스에서 생성되는 구체적인 제품
## pizzaaf Class Diagram
![10](https://user-images.githubusercontent.com/21019088/49695039-16461700-fbd8-11e8-89e7-a7db5fa11a5b.gif)
## Execute
### pizzaaf/PizzaTestDrive
![image](https://user-images.githubusercontent.com/21019088/49694993-4e008f00-fbd7-11e8-8c3c-a2b74c18fdd2.png)

# Diffences between af and fm
- fm은 fmPizzaStore에서 메소드를 만들어 서브클래스에서 오버라이딩 하도록 하였다. afPizzaIngredientFactory는 제품 인터페이스들을 구성하여 제품군을 형성하였다.
# P.S
- af : abstract factory
- fm : factory method
