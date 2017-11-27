## Java Factory Pattern
자바의 디자인 패턴 중에 하나로 원하는 클래스를 공장에서 찍어내듯 생성할 수 있다고 해서 ```Factory Patter``` 이라고 부른다.

<br>


## How to use
.```Dog```, ```Cat```, ```Cow``` 클래스를 ```AnimalFactory``` 클래스로 생성할 수 있다.


#### AnimalFactory.java
```Java
class AnimalFactory {
  public static Animal Create(String animalName) {
    if(animalName.equals("")) {
      System.out.println("생성할 클래스가 없습니다.");
    }

    if (animalName.equals("강아지")) {
      return new Dog();
    }else if(animalName.equals("고양이")) {
      return new Cat();
    }else if (animalName.equals("소")) {
      return new Cow();
    }
    return null;
  }

}
```
