# GameplayKit 으로 상태표시 UI 쉽게 만들기 - 노수진.네이버웹툰

https://github.com/nsoojin/VoiceControlSample-iOS



//저한텐 간단하지 않은거 같아요...역시 갓갓..

Finite-State Machines(유한 상태 기계) 한번에 오로지 하나의 상태만을 가질수있고, 어떠한 사건에 의해 변화할수있다. - 자판기

3가지 정의 요소 - 상태, 변화의 조건, 초기 상태

GameplayKit - Pathfinding(나중에 알아봐야징) 

UIKit이랑 같이 사용 가능함 !

State Machines (GamePlayKit 내부에 있음)

GKState - 상속 받아서 오버라이드를 통해 상태별 동작과 전환의 조건을 정의

GKStateMachine - 초기 상태 지정

Core Animation, Lottie(이거좀....)사용

//Lottie 별로 안간단하던데...내가 못하는거쥐 이거..ㅠㅠㅜㅜ 왜 내코드만 안돌아갈까..

바로 GKSkate를 상속받지 말고, 공통 SuperClass State로 공유 자원 및 반복 로직을 관리

도중에도 쉽게 dismiss 할수 있게 해주면 좋아요

음석인식 버튼을 UIResponder처럼!

inputView 



# App Store Commerce - 애플 직원(Amy)

애플이 우리가 돈을 벌수 있게 도와주는것..?

한국 특: 무료앱+광고붙이기

인앱결제를 넣어보기, or 구독 아이템..?

### 30프로를 애플에게 가져다 바쳐야 한다고 합니다..

애플페이 추가좀("야, 애플")

작년부터 카드 여러개 추가가 가능합니다.

Appstore에서는 87개의 티어와 free로 나뉘어져있다.

이게 막는게 아니라 더 잘팔리는 가격이라 이렇게 한거래요. 조사 많이 했다고, 장점이 많대요

애플에서 세금 납부도 대행해준대요(그래도 20프로잖아)

한국에서는 대행 안해준대요 (헬조선 되는게 뭐임)

작년부터 원화결제, 카카오페이 등이 된대요

## Consumable, Non-Consumable, Auto Renewable Subscription

Subscription이 요즘 뜨고있대요(아직 실제론 10프로정도..?)

1년이 지난 구독자에 대해서는 애플이 15프로만 떼어간대요

구독은 가격을 나라별로 다르게 정할수 있대요!

앱을 통해 받는 월세..?(이표현 맘에들어 ㅎ)

가장 기본적이고 중요한 기능을 무료로 풀고, 취침 데이터 분석이나 알람 소리 번경 등 additional 한것을 premium으로 푸는걸 애플에서는 좋게 보고 장려함.

재결제에 대한 가치

새로운 결제 수단이 아닌, 추가적인 경험으로서의 구독

프리미엄 콘텐츠 또는 기능에 대한 탐색

다양한 디바이스 접근 가능성

(이거 그냥 Netfilx 아님??)



Appstore Connect 에서 group 생성 하고 그 안에 넣는 방식.

티어를 줄 수도 있고, duration에 variation을 줄 수도 있다.

두세개의 비교군을 만들어놓고 가장 팔고싶은것을 강조하는듯한 UI를 만들어 놓는것이 구조적으로 잘팔린다고 한다.

Apple에서도 iCloud나 AppleMusic애서 사용한다고 한다.



StoreKit을 Import를 하고, 옵저버를 등록해 앱스토어와 통신을 해 결제 구현이 가능함

App Store connect 에서 http통신으로 notification을 보내주기도 한다.

올해에 인앱결제 테스트가 쉬워진다고 해요



App Store Receipt

folder에 Bundle 안에 있는건데 이거 바꿔치기되기 은근 쉽다고 함.

서버로 올려서 앱스토어 서버로 보내서 검증하는게 쉬움

이때 가장 최신에 이 고객이 결제한 영수증 100개를 보내준다고 한다.

그냥 토큰 다루듯이 추출해서 보내면 된다고함.

docs에 자세히 있대요.

디바이스에서 검증하려면 암호 풀어야함 ㅡㅡ

한국에서 StoreKit 옵저버를 등록하지 않아서 생긴 오류들이 많대요.

Appstore에 광고해준대요 꽁짜로!

초기에 고객을 유인하는 방법으로 free trial 이 존재한다.

subscription offer라고 나가는 사람들에게 조금 더 싸게 유인할수있는것도 있다.

문제가 생기면 Feedback Assistant에 올리면 된다.



































