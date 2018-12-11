# Definition
- 메소드에서 알고리즘의 골격을 정의합니다. 알고리즘의 여러 단계 중 일부는 서브클래스에서 구현할 수 있습니다. 템플릿 메소드를 이용하면 알고리즘의 구조는 그대로 유지하면서 서브클래스에서 특정 단계를 재정의할 수 있습니다.

※ Hook
- 여러가지 용도로 쓰인다. 알고리즘에서 필수적이지 않은 부분을 필요에 따라 서브클래스에서 구현하든 말든 하도록 하는 경우에 후크를 쓰 수 있습니다. 또는 템플릿 메소드에서 앞으로 일어날 일 또는 막 일어난 일에 대해 서브클래스에서 반응할 기회를 제공하기 위한 용도로도 쓰일 수 있습니다. 예를 들어, 내부적으로 어떤 목록을 재정렬한 후에 서브클래스에서 어떤 작업(화면상에 표시되는 내용을 다시 보여주는 등)을 수행하도록 하고 싶은 경우에 justReOrderList() 같은 이름을 가진 후크 메소드를 쓸 수도 있겠죠. 실행황면에서 보듯이 서브클래스에서 진행되는 작업에 대한 결정을 내리는 기능을 부여하기 위한 용도로 후크를 쓸 수도 있습니다.
# Main Sources
### Client
![image](https://user-images.githubusercontent.com/21019088/49780149-998a7880-fd50-11e8-8408-753bbb5578f1.png)

### CaffeineBeverageHook
![image](https://user-images.githubusercontent.com/21019088/49780379-9cd23400-fd51-11e8-9a31-e816da1b627c.png)

#### prepareRecipe가 템플릿 메소드이다.
#### customerWantsCondiments가 Hook이다. 이걸 서브클래스에서 오버라이딩 하여 목적에 맞게 사용한다.

### CoffeeWithHook
![image](https://user-images.githubusercontent.com/21019088/49780404-ba070280-fd51-11e8-98ce-9ab58d2abdef.png)

![image](https://user-images.githubusercontent.com/21019088/49780420-cdb26900-fd51-11e8-98f4-8910f8bf64f7.png)

# barista Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49780483-10744100-fd52-11e8-9f27-3013724f1d9a.png)

# Execute
### barista/BeverageTestDrive
![image](https://user-images.githubusercontent.com/21019088/49780513-2f72d300-fd52-11e8-91c9-acba573a102f.png)
