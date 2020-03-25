# Spring(SpringMVC)과 Spring Boot
## 1. Spring
### 1_1. Spring이란?
앤터프라이즈급 애플리케이션을 자바로 개발하는데 있어 유용하고 편리한 기능을 제공하는 프레임워크입니다.  
의존성 주입(DI, Dependency Injection)과 제어의역전(IOC, Inversion Of Control)은 스프링에서  
가장 중요한  특징중 하나이며, 이 것들로 인해 결합도를 낮추는 방식으로 개발을 할수 있으며  
이러한 개발방식으로  개발한 응용프로그램은 단위 테스트가 용이하기 때문에 보다 퀄리티 높은  
프로그램을 개발 할 수 있습니다.  

앤터프라이즈급 개발이란 기업을 대상으로 하는 개발이란 뜻 입니다. 즉, 대규모데이터 처리와 트랜잭션이  
동시에 여러 사용자로 부터 행해지는 매우 큰 규모의 환경을 엔터프라이즈 환경을 말합니다.

### 1_2. Spring 특징
### IOC (Inversion Of Control)
IOC(Inversion Of Control)는 한국말로하면 제어의 역전입니다. 제어의 역전이란?  
일반적으로 프로그래밍은 객체 선언 및 생성 -> 의존성 객체 생성 -> 객체 내의 메소드 호출하는 방식입니다.  
즉, 모든작업을 사용자가 제어하는 구조 입니다.  

하지만, IOC에서는 이 흐름의 구조를 바꿔, IOC에서의 객체는 자기가 사용할 객체를 선택하거나 생성하지 않으며  
또한 자신이 어디서 만들어지고 어떻게 사용되는지 모릅니다. 자신의 모든권한을 다른 대상에 위임함으로 써  
제어권한을 위임받은 특별한 객체에 의해 결정되고 만들어집니다.  
즉, 제어의 흐름을 사용자가 컨트롤 하지 않고 위임한 특별한 객체에 모든 것을 맡기는 것입니다.  

__IOC란 기존 사용자가 모든 작업을 제어하던 것을 특별한 객체에 모든 것을 위임하여 객체의 생명주기 등  
모든 객체에 대한 제어권이 넘어 간 것을 IOC, 제어의 역전이라고 합니다.__

IOC는 DI와 DL로 구성됩니다. DI와 DL에 대해 알아보겠습니다.

DL (Dependency Lookup) - 의존성 검색  
컨테이너에서는 객체들을 관리하기 위해 별도의 저장소에 빈을 저장하는데 개발자들이  
컨테이너에서 제공하는 API를 이용하여 사용하고자 하는 빈을 검색하는 방법입니다.

DI (Dependency Injection) - 의존성 주입  
의존성 주입이란 객체가 서로 의존하는 관계가 되게 의존성을 주입하는 것으로 객체지향 프로그램에서 의존성이란  
하나의 객체가 어떠한 다른 객체를 사용하고 있음을 말합니다. 여기서 말하는 IOC의 DI는 각 클래스 사이에 필요로  
하는 의존관계를 빈 설정 정보를 바탕으로 컨테이너가 자동으로 연결해 주는 것입니다.

### POJO (Plan Old Java Object)
POJO(Plan Old Java Object)란 자바 오브젝트를 말합니다.  
POJO는 getter/setter를 가진 단순 자바 오브젝트로 정의를 하고 있으며 이러한 단순 오브젝트는 의존성이 없고  
나중에 테스트 및 유지보수가 편리한 유연성의 장점을 가집니다. 이러한 장점들로 인해 객체지향적인 다향한 설계와  
구현이 가능해지고 POJO의 기반의 Framework가 조명을 받고 있습니다.  

### AOP (Aspect Oriented Programming)
AOP(Aspect Oriented Programming)란 관점 지향 프로그래밍을 말합니다.  
대부분 소프트웨어 개발 프로세스에서는 OOP(Object Oriented Programming)인 객체지향이 원칙입니다. OOP는  
객체 지향 원칙에 따라 관심사가 같은 데이터를 한 곳에 모아 분리하고 낮은 결합도를 갖게하여 독릭접이고  
유연한 모듈로 캡슐화를 하는 것을 말합니다. 하지만 중복된 코드들이 많아지고 가독성, 확장성, 유지보수성 등 을  
떨어 뜨려 이러한 문제를 보완하기 위해 AOP가 나왔다고 합니다. 

AOP에서 핵심기능과 공통기능을 분리시켜 핵심 로직에 영향을 끼치지 않게 공통기능을 끼워 넣는 개발 형태 이며  
이로인해 중복되는 코드를 한 곳에 모아 중복 되는 코드를 제거 할 수 있어지고 공통기능을 한 곳에 보관해 공통  
기능 하나의 수정으로 모든 핵심기능들의 공통기능을 수정 할 수 있어 효율적인 유지보수가 가능하며 재활용성이  
극대화 됩니다. 추가로 AOP로 만들 수 있는 기능은 OOP로 구현이 가능 합니다.

### MVC(model 2)
MVC는 Model, View, Controller구조로 사용자 인터페이스와 비지니스 로직을 분리하여 개발 하는 것으로 MVC에서는  
Model1과 Model2로 나누어져 있고 MVC는 Model2를 지칭합니다.

Model : 데이터 처리를 담당하며 Service와 DAO로 나뉘며 Service부분은 불필요하게 HTTP통신을 하지 않아야 하며  
request나 respose와 같은 객체를 매개변수로 받아서 안됩니다. 또한 Service는 view에 종속적인 코드가 없어야  
하고 View부분이 변경되도 Service부분은 재사용이 되어야 합니다.

View : 사용자Interface를 담당하며 사용자에게 보여지는 부분으로 Controller를 통해 모델에 데이터에 대한 시각화를  
담당하며 View는 자신이 요청을 보낼 Controller의 정보만 알고 있어야 합니다.

Controller : View에서 받은 요청을 가공하여 Model에 전달하며 Model로 부터 받은 결과를 View에 넘겨줍니다.  
View와 Controller에 정보를 알고 있어야 합니다.

이렇게 나누는 이유는 소스를 분리함으로서 각 소스의 목적이 명확해지고 유지보수가 용이하기 때문입니다.

### 1_3. Spring의 구조
![Spring구조](https://t1.daumcdn.net/cfile/tistory/99A523405B9E2C1510)

## 2. Spring Boot?
Sptring Boot는 Spring 프레임웍을 사용하는 프로젝트를 아주 간편하게 셋업할 수 있는 스프링 프레임웍의  
서브 프로젝트 입니다. 독립 컨테이너에서 동작할 수 있기에 JAVA만 설치 되어 있으면 개발하기 수월 하며  
또한 빌드 후에 jar파일이 생성되고, 별도의 서버 설치 없이 embeded tomcat이 자동으로 실행됩니다.  
프로젝트 생성시에 기존의 Spring에서 하듯 복잡한 설정이 아닌 통합된 설정파일인 application.yml로  
쉽게 사용할 수 있습니다.

## 3. Spring(SpringMVC)과 Spring Boot 선택
WEB기반인 어플리케이션은 Tomcat이나 WAS같이 Web Container가 설치 되어 있어야 합니다.  
하지만 비교적 규모가 작은 형태의 에플리케이션을 싱행시키기 위해 그보다 큰 WAS를 따로 설치하기에는  
효율 적이지 않습니다.그래서 작은 규모의 프로젝트에서는 embeded container에서 자신의 어플리케이션을  
실행시키는 Spring Boot를 쓰는게 맞다고 합니다.

하지만 비교적 규모가 큰 웹 사이트 같은 경우 이런 구조로 만드는 것 보단 Spring MVC형태로 만들어 WAS에  
배포하는 스타일이 낫습니다. embeded container에서 어플리케이션을 실행시키기에는 불안정하기도 하며  
WAS에서 관리되는 데이터 소스나 메시지 서비스를 이용할 수 있기 때문입니다.

결론은 어느정도의 크기의 서비스를 하는지에 따라 선택이 달라진다고 합니다.

<hr/>

## * 참고
<https://sas-study.tistory.com/274>  
<https://annajinee.tistory.com/20>  
<https://velog.io/@max9106/Spring-spring%EC%9D%B4%EB%9E%80-x7k4r8d5ij>  
<https://khj93.tistory.com/entry/Spring-Spring-Framework%EB%9E%80-%EA%B8%B0%EB%B3%B8-%EA%B0%9C%EB%85%90-%ED%95%B5%EC%8B%AC-%EC%A0%95%EB%A6%A>