# Definition
- 집합체(PancakeHouseMenu) 내에서 어떤 식으로 일이 처리되는지에 대해 전혀 모르는 상태에서 그 안에 들어있는 모든 항목들에 대해서 반복자(PancakeHouseMenuIterator)를 통해 반복작업을 수행할 수 있습니다. 

- 각 항목에 접근할 수 있게 해 주는 기능을 집합체가 아닌 반복자 객체에서 책임지게 된다는 것도 장점으로 작용합니다. 그러면 집합체 인터페이스 및 구현이 간단해지고, 각자 중요한 일만 잘 처리할 수 있으면 되니까요.

# Main Sources
### Client
![image](https://user-images.githubusercontent.com/21019088/49788573-06ac0700-fd6d-11e8-8e47-568ec6d1aeb2.png)

### Iterator 인터페이스
![image](https://user-images.githubusercontent.com/21019088/49788617-204d4e80-fd6d-11e8-949b-28127ab70892.png)

### Menu 인터페이스
![image](https://user-images.githubusercontent.com/21019088/49788641-30fdc480-fd6d-11e8-8544-1197b4b6ef0c.png)

### PancakeHouseMenu(집합체)
![image](https://user-images.githubusercontent.com/21019088/49788692-5985be80-fd6d-11e8-91fc-ca2fd8068e8d.png)

### PancakeHouseMenuIterator(반복자)
![image](https://user-images.githubusercontent.com/21019088/49788706-64405380-fd6d-11e8-9270-b932d06cf4c6.png)

### DinerMenu(집합체)
![image](https://user-images.githubusercontent.com/21019088/49788741-7de19b00-fd6d-11e8-8b31-a93b78c1141f.png)

### DinerMenuIterator(반복자)
![image](https://user-images.githubusercontent.com/21019088/49788770-905bd480-fd6d-11e8-87e8-6fd3b73013ad.png)

# Core Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49788899-eb8dc700-fd6d-11e8-85b6-dc758d08078f.png)

# dinermerger Class Diagram
![image](https://user-images.githubusercontent.com/21019088/49789039-4c1d0400-fd6e-11e8-82eb-41ac797f94e3.png)
=> Waitress가 클라이언트라 보면 된다.
# Execute
### dinermerger/MenuTestDrive
![image](https://user-images.githubusercontent.com/21019088/49788969-1bd56580-fd6e-11e8-9638-29189084c715.png)

