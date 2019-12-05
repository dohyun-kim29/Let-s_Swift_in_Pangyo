## 네이버 웹툰 장수한

### 느낌적인 느낌을 찾아서

UIView.isHidden (True? False?)

Why? 시각적이 아닌 데이터 관점에서 설계.

!. 2진수 토글(부정인데요, 부정이 아니에요. 반전이라는거임!!!)

```swift
if !title.isEmpty { titleLabel.text = title }
//만약에 아니면 문자열 타이틀이 빈 상태.
```

```swift
if title.isEmpty ==false { titleLabel.text = title }
```

Guard. 막는다고 부정의 결론이 남 즉 이중부정.

이분은 guard 보다는 if 를 선호하심.

Guard, 쓸모 없다고 생각하지만 엄연한 조기탈출의 기능이 있음. 빌드에러 막는 차칸넘.

Swift의 장점 : 런타임 에러가 날것들을 빌드타임에서 거의 다 막아줌. Ex) Guard, Optional.

우리가 제대로 제어를 할 수 있다면 if를 쓰자. 그냥 실력 키워서 if 쓰자.

그래도 Guard는 쓸모가 있다. if 쓸꺼 이거 쓰면 코드 깔끔해지는 경우 있음!

```swift
guard let nonOptionalTitle = title else
//guard문 밖에서도 살아있음
```

```swift
if let nonOptionalTitle = title else
//if문 안에서만 살아있음
```

**모든 기본 문법엔 이유가 있다!!!**

guard 보단 if !

**문법의 특성과 목적을 생각하여 코드를 짜자!!**

## 네이버웹툰 김형규

### 지저분한 UnwrappingCode를 깔끔하게 정리해보자!

Optional =  Stability + 귀찮음. ㅠ

1. Non-Optional/Optional 분리

2. Guard/if/coalescing unwrapping의 사용을 구분!

   Early exit (Guard!)

   분기가 필요한 부분

Collection 내의 Unwrapping 코드를 compectmap/map을 사용하여 줄여보자!

코드를 역할게 맞게 더 쪼개고, 그에 맞춰 unwrapping 코드를 분산.

Optional 변수를 unwrapping 하지 않고 사용할 방법이 없을까?

Map/flatMap을 사용하자!

```swift
func maketext( _ name: String) -> String {
  return "name is \(name)"
}
name.map(maketext)
```

input이 여러개인 경우에는? 튜플 사용

## 스타일쉐어 전수열

### 레거시 프로젝트에 의존성 주입하기

강한 의존을 약한 의존으로.

Composition Root. 의존성 그래프가 만들어지는 곳. 프로그램의 진입점 (AppDelegate

AppDependency

```swift
struct AppDependency {
  let window: UIWindow
}

extention AppDependency {
  static func resolve() {
    
}
```

AppDelegate -> AppDependency

AppDelegate 에 Override 해서 넣는다.



Composition Root가 테스트 환경에서 실행되면 안된다.

**가급적 생성자 호출 외의 코드는 자제!**(상당히 위험함)

이론은 좋지만 현실의 문제. 여러 코드들이 이렇게 완벽한 의존성 그래프에 속하지 못한다.

1. 정적 인터페이스에 의존한다.

   생성자로 인터페이스를 전달받는다.

   적어도 외부에서 의존성을 주입할수 있게 되었다. 프로토콜은 필요할때!

   심각하게 의존할 경우엔 타입 자체를 받자.

   

2. 인스턴스를 직접 생성한다.

   생성자로 팩토리를 전달받는다.

   적어도 외부에서 주입할수 있게 되었다.

   복잡한 클로저가 난무하면 Factory 타입을 정의하자.

두 해결 방법의 공통점. 의존성이 외부에 위치한다.

필요에 따라 원하는 객체를 주입할수 있다.



**궁극의 목표는 모든것이 의존성 그래프 안에.**

**현실의 목표는 어제보다 더 나은 코드를 작성.**

Https://github.com/devxoul/Pure (백과사전.)

스타일쉐어 코드를 봤어요...대박..!!



## 카카오뱅크 안정민

### 민소네 실험실 (이상적이고, 극단적인 iOS 프로젝트 구조 설계)

서브 프로젝트 사용의 장점:

빌드 속도가 빨라짐

중복된 이름 사용 가능



Dynamic Framework





