# Definition
- 객체에 추가적인 요건을 동적으로 첨가한다. 데코레이터는 서브클래스를 만드는 것을 통해서 기능을 유연하게 확장할 수 있는 방법을 제공한다.

# Reason for use
- DarkRoast에 Mocha 2번,Whip한 번이 추가된다면 Decorator pattern을 적용하기 전에는 DarkRoastWithMocha2ansWhip이란 구상 클래스를 만들어주어야 한다. 이런식으로 클래스를 하나하나 만든다면 셀수도 없는 많은 클래스를 만들어야 한다. Decorator pattern을 적용하면
Beverage beverage2 = new DarkRoast();
beverage2 = new Mocha(beverage2);
beverage2 = new Mocha(beverage2);
beverage2 = new Whip(beverage2);
이런식으로 필요할 때마다 동적으로 첨가해 주면 클래스는 DarkRoast와 Mocha, Whip이 3개만 있으면 된다.
# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49693311-690cd800-fbb2-11e8-8c6a-c7bee33bf16c.png)
# Decorator pattern 적용 전 Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49693318-96598600-fbb2-11e8-863d-bace9614b505.png)
# starbuzzWithSizes Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49693326-c99c1500-fbb2-11e8-980b-456ac80c0980.png)
# Decorator pattern이 적용 된 Java.io Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49693334-ffd99480-fbb2-11e8-8515-558e8816f182.png)
InputStream 이 추상구성요소이고 모든 보조스트림의 조상인 FilterInputStream 이 추상 데코레이터 이다. FilterInputStream을 상송받아 구현하는 BufferedInputStream 클래스들이 구상 데코레이터이다. InputStream을 상속받는 FileInputStream 같은 기반 스트림들은 데코레이터로 포장될 구상 구성요소 역할을 한다.
# Execute
### starbuzzWithSizes/StarbuzzCoffee
![image](https://user-images.githubusercontent.com/21019088/49693355-83938100-fbb3-11e8-84f4-23285d72cde7.png)

