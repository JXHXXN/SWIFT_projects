# MVVM 패턴
- Model(비즈니스 로직), View(UI), View Model(프레젠테이션 로직)으로 로직을 분리하는 패턴이다.
- View에 업데이트할 데이터를 View Model에서 처리함으로써 Controller가 복잡해지는것을 줄여준다.
- 로직을 분리함으로써 테스트, 유지보수, 재사용이 MVC보다 쉽다.
- Model은 ViewModel과 View를 모르고, ViewModel은 View를 모른다.

## View, 뷰
UI에 관련된 것을 다룬다.  
사용자가 보는 구조, 레이아웃, 형태를 정의한다.  
UI로직을 포함하지만 비즈니스 로직을 포함하면 안된다.
ViewModel에 있는 필드가 변경되는지 관찰하고 있다. (Observer Pattern)

## Model, 모델
데이터와 데이터에 관련된 행위를 합쳐서 모델이라 한다.  
앱에섯 사용할 비즈니스 로직을 다룬다.  

## ViewModel, 뷰모델
모델의 데이터를 가공해서 뷰에 제공한다.  
뷰에서 사용할 메서드와 필드를 뷰모델에서 구현된다.  

## Data Binding, 데이터 바인딩
View Model과 View 는 서로에게 데이터의 변경을 알려줄 수 있는 방법이다.

## 유의할 점
뷰모델이 비대해지지 않게 주의해야힌다.  
뷰 -> 뷰모델 -> 모델 이 참조 숮서를 지켜야 한다.

## MVVM 패턴의 장점
- 개발 기간동안 UI디자인이 나오지 않았더라도 미리 정의된 모델과 뷰 모델을 먼저 개발할 수 있기 때문에 개발자와 디자이너가 병렬적으로 작업할 수 있다.
- 테스트하기 쉽고 코드가 이벤트 기반이다. 
- 재사용이 용이해진다. 
- 뷰와 모델 사이에 의존성이 없다.
- command 패턴과 data binding을 사용해 뷰와 뷰모델 사이의 의존성이 없다.

## MVVM 패턴의 단점
- 복잡한 구조를 위해서 만들어진 패턴이기에 거대한 앱에서는 유용하나 소형 앱에서는 오버헤드가 커진다.
- 데이터 바인딩이 메모리 소모를 많이 한다. 
- 뷰모델의 설계가 쉽지 않다.  


<img src = "https://github.com/JXHXXN/SWIFT_projects/assets/76980015/37de1e0d-a4d8-4e5e-ad66-b6751b8dc105" />

#
#### [참고자료]
https://just-my-blog.tistory.com/14 .  https://scshim.tistory.com/407 . https://gyuios.tistory.com/87
