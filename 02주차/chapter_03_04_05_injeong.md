# 3장. 기본 도구
- 도구가 더 훌륭하고 여러분이 더 사용법에 능숙해질수록 여러분의 생산성은 더 높아질 것이다.
- 언제나 일을 하는 데에 더 나은 방법이 없는지 살펴라.

### Topic 17. 셸 가지고 놀기
- GUI의 단점
    - 자동화, 매크로 못함
    - WYSIAYC( What You See Is All You Get)
        - 여러분이 보는 것이 여러분이 얻는 전부라는 것

- 명령어 셸의 힘을 사용하라.
    - 셸 자동화
    - 자신만의 셸

### Topic 18. 파워 에디팅
- 에디터를 유창하게(fluency) 쓸 수 있게 하라.
    - 무언가 같은 일은 반복하는 것을 발견할 때마다 이렇게 생각하는 습관을 들여라. '분명 더 나은 방법이 있을 텐데'. 그리고 더 나은 방법이 있는지 찾아보라
    - 유용한 기능을 찾았다면 몸이 기억해서 반사적으로 사용하도록 만들어라.
    - 우리가 아는 유일한 방법은 반복이다.

### Topic 19. 버전 관리
- 버전 관리 시스템 Version Control System
- 언제나 버전 관리 시스템을 사용하라
    - 혼자서 하더라도, 나중에 버릴 프로토타입이라도, 소스코드가 아닐지라도
    - 모든 것으 버전 관리 아래에 둬라

### Topic 20. 디버깅
- '버그'라는 단어는 14세기 이래 '공포의 대상'을 지칭하는 단어로 사용되어 왔다 ㅋㅋ
- 소프트웨어 결험은 요구사항을 오해하는 것부터 코딩 오류에 이르기까지 여러 모습으로 나타난다.
- 디버깅의 심리
    - 디버깅은 단지 **문제 풀이**일 뿐이라는 사실을 받아들이고, 그런 마음으로 공략하라
    - 비난 대신에 문제를 해결하라.
- 디버깅 사고 방식
    - 당황하지 말라
    - 버그라고 생각하는 증상의 원인이 무엇일지 진짜로 **생각**해보는 것이 정말 중요하다.
    - 근시안의 함정에 주의하라. 표면에 보이는 증상만 고치려는 욕구를 이겨내라.
- 실마리 찾기
    - 버그 제보자와 인터뷰 하기
    - 인공적인 테스트 X
    - 체계적인 테스트 O 경계조건과 실제 최종 사용자 사용 패턴 모두를 철저히 테스트
        - **이 맥락 안에서, 이 데이터로, 이 경계 조건하에서 증명하라.**
        - 가정하지 말라. 증명하라
- 디버깅 전략
    - 버그 재현하기 
    - **코드를 고치기 전 실패하는 테스트부터.**
    - 버그가 방생하는 상황을 다른 것들로부터 분리하다 보면 어떻게 고쳐야 할지에 대한 통찰을 얻기도 한다.
    - 그놈의 오류 메세지 좀 읽어라.
    - 이진 분할 활용하기
    - 로깅과 트레이싱
    - 고무오리
    - 소거법
- **왜 이 문제가 더 일찍 발견되지 않았을까 생각해 봐야 한다.**
    - 버그를 미리 잡을 수 있도록 단위 테스트나 다른 테스트를 수정할 필요가 있는지 고민해 보라.
    - 이것과 동일한 버그가 있을 법한 다른 코드가 있는지 살펴보자.
    - 한 사람이 오해했다면 다른 사람들도 그럴 수 있다.

### Topic 22. 엔지니어링 일지
- 무엇을 했고 무엇을 배웠는지, 떠오르는 생각을 그려본 것, 방금 읽은 계기판의 눈금 등 기본적으로 업무에 관한 건 무엇이든지 적기
- 일지를 쓰면 좋은 점
    - 기억보다 더 믿을 만하다.
    - 진행 중인 작업과 직접적인 관계가 없는 발상을 일단 쌓아 놓을 수 있는 곳이 생긴다. 위대한 발상을 잊어버릴 걱정 없이 지금 하는 일에 계속해서 집중할 수 있다.
    - 고무 오리와 같은 역할을 할 수 있다.

<br>

# 4장. 실용주의 편집증
- 여러분은 완벽한 소프트웨어를 만들 수 없다. 삶의 공리로 인정하고 받아들여라.
- 방어적으로 코딩하라. 실용주의 프로그래머는 자기 자신 역시 믿지 않는다.

### Topic23. 계약에 의한 설계
- DBC **Design By Contract**
    - 프로그램의 정확성을 보장하기 위해 소프트웨어 모듈의 권리와 책임을 문서화하고 합의하는 데에 초점을 맞추는 개념
    - 선행조건, 후행조건, 클래스 불변식
- '게으름뱅이' 코드를 작성하라.
    - 시작하기 전에 자신이 수용할 것은 엄격하게 확인하고, 내어 줄 것에 대해서는 회소한도를 약속하는 것이다.
    - 생각하고 행동에 옮기기
- DBC 구현
    - 코드를 작성하기 전에 유효한 입력 범위가 무엇인지, 경계조건이 무엇인지, 루틴이 뭘 전달한다고 약속하는지, 혹은 더 중요하게는 무엇을 약속하지 않는지 등을 나열하는 것만으로도 더 나은 소프트웨어를 작성하는 데에 엄청난 도움이 된다.
- 일찍 작동을 멈춰라.
    - 문제를 찾고 원인을 밝히기 위해서는 사고가 난 지점에서 일찍 멈추는 것이 유리하다.
- 의미론적 불변식 semantic invariant
    - 어떤 종류의 문제가 발생하든 오류가 있다면 거래를 처리하지 않아야지 거래를 중복으로 처리하면 안된다.
    - 어겨서는 안되는 고정된 규칙인 요구사항과 경영진이 바뀌면 얼마든지 없어질 수 있는 단순한 정책을 혼동하지 말아야 한다.
    의미론적 불변식은 무언가가 품은 **진짜 의미의 중심**이 되어야 하며, 훨씬 역동적으로 변하는 비즈니스 규칙처럼 일시적인 정책에 영향을 받으면 안된다.
    - 불변신의 자격이 있는 요구 사항을 찾았다면 여러분이 작성하는 모든 문서에 잘 드러나도록 만들어라.

### Topic 24. 죽은 프로그램은 거짓말을 하지 않는다.
- '있을 수 없는 일'이 발생했을 때 우리는 그 사실을 알아야 한다.
- '그런 일은 절대 일어날 리 없어.' 라는 사고에 빠지기 쉽다.
- 문제의 코드는 정상적인 상황에서는 실패하지 않았을 것이다. 하지만 우리는 지금 **방어적으로 코딩**하고 있다.
- 모든 오류는 정보를 준다.
- 일단 작동을 멈춰라. 망치지 말고 멈춰라.
    - 얼랭 창시자 "방어적 프로그래밍은 시간 낭비다. 그냥 멈추는게 낫다!"
    - 얼랭과 엘릭서 : 슈퍼바이저 트리. 슈퍼바이저의 슈퍼바이저가 실패를 관리함

### Topic 25. 단정적 프로그래밍
- 단정문으로 불가능한 상황을 예방하라
- 명시적으로 검사하라
- 하지만 진짜 오류 처리를 해야하는 곳에 단정을 대신 사용하지는 말라
- **단정은 결코 일어나면 안 되는 것들을 검사한다.**
- 단정문에 대한 오해
    - 코드를 느리게 만든다
    - 디버깅 도구일 뿐이다. 테스트되고 배포된 다음에는 더 이상 단정이 필요하지 않다.
- 테스트가 모든 버그를 발견한다는 가정은 틀렸다.
- 낙관주의자들은 여러분의 프로그램이 험한 세상에서 돌아간다는 사실을 잊는다.
- 결론, 성능 문제가 있다 하더라도 정말 문제가 되는 단정문만 끄도록 하자.

### Topic 26. 리소스 사용의 균형
- 리소스 할당과 해제
    - **자신이 시작한 것은 자신이 끝내라.**
- 잘 모르겠을 땐 언제나 스코프를 줄이는 편이 낫다.
- 지역적으로 행동하라
- 중첩 할당 시,
    - 리소스를 할당한 순서의 역순으로 해제하라
    - 여러 곳에서 동일한 구성의 리소스들을 할당하는 경우에는 언제나 같은 순서로 할당해야 교착 deadlock 가능성을 줄일 수 있다.

### Topic 27. 헤드라이트를 앞서가지 말라
- 우리는 너무 먼 미래는 내다볼 수 없고, 정면에서 벗어난 곳일수록 더 어둡다.
- 작은 단계들을 밟아라. 언제나.
- 더 진행하기 전에 피드백을 확인하고 조정하라. 피드백의 빈도를 여러분의 제한 속도라고 생각하라.
    - 피드백: REPL의 결과, 단위 테스트, 사용자와의 대화 등
- 너무 큰 작업은 무엇일까? '예언'을 해야하는 모든 작업이다.
    - 그 너머는 경험에 기반한 추측을 벗어난 무모한 억측의 영역이다.
- 틀릴 가능성 -> 언제나 교체 가능한 코드를 작성하여 대비하면 된다.
- 블랙 스완
    - 아웃라이어는 통계적으로 드물더라도 그 여파는 훨씬 더 컸다.
    - 예언하지 말라.

<br>

# 5장. 구부러지거나 부러지거나
- 삶은 멈추지 않는다. **빠른 변화 속도**를 따라가려면 모든 수단을 동원하여 가능한 한 **느슨하고 유연한 코드**를 작성해야 한다.
- 결합도와 유연함

### Topic 28. 결합도 줄이기
- 높은 결합도는 변경의 적이다.
- 소프트웨어의 구조는 유연해야 한다. 유연하려면 각각의 부품이 다른 부품에 가능한 한 조금만 연결되어야 한다.
- 결함도가 낮은 코드가 바꾸기 쉽다.
    - 열차 사고(train wreck) 연쇄 메서드 호출
    - 글로벌화: 정적인 것의 위험함
    - 상속
    - -> 주의해야할 것
- 묻지 말고 말하라 Tell, Don't Ask (TDA)
    - 다른 객체의 내부 상태에 따라 판단을 내리고 그 객체를 갱신해서는 안된다는 것
    - TDA는 자연법칙이 아니다. 문제를 알아볼 수 있게 도와주는 패턴일 뿐
    - 실용적인 판단을 하라 (무조건적으로 지키기 보다)
- 데메테르 법칙, 디미터 법칙
    - 보다 깨끗하고 결합도가 낮은 함수를 작성하는 방법
    - 메서드 호출을 엮지 말라
    - 엮는 것들이 절대로 바뀌지 않을 것 같다면 이 규칙을 지키지 않아도 된다.
    - 사실 여러분의 애플리케이션에 있는 것은 모두 바뀌리라 생각해야 한다.
- 전역 데이터를 피하라.
    - 싱글턴도 전역 데이터다.
    - 외부 리소스도 전역 데이터다.
    - 전역적이어야 할 만큼 중요하다면 API로 감싸라
- 상속은 결합을 늘린다.
- 결국은 모두 ETC (변경하기 쉬워야 한다.)
    - 직접적으로 아는 것만 다루는 부끄럼쟁이 코드를 계속 유지하라.

### Topic 29. 실세계를 갖고 저글링하기
- FSM Finite State Machine 유한 상태 기계
- 감시자 패턴의 단점
    - 모든 감시자가 감시 대상에 등록을 해야하기 때문에 결합이 생김
    - 동시적 처리의 특성상 콜백 실행이 끝날 때까지 감시 대상이 계속 기다려야 함
- 게시-구독 전략으로 해결 (Publish-Subscribe)
    - 게시자와 구독자를 채널(공통 인터페이스)로 연결함으로서 결합로를 줄임
- 어디에나 이벤트가 있다.

### Topic 30. 변환 프로그래밍
- 자신이 하고 있는 걸 하나의 과정으로 서술할 수 없다면, 자기가 뭘 하고 있는지 모르는  것이다
- 모든 프로그램은 데이터를 변환한다. 받은 입력을 출력으로 바꾼다. 하지만 우리는 설계를 고민할 때 변환을 만드는 것에 대해서는 거의 생각하지 않는다.
- 우리는 이렇게 코드에만 집중하면 핵심을 놓칠 수 있다고 본다. **프로그램이란 입력을 출력으로 바꾸는 것이라는 사고방식으로 돌아갈 필요가 있다.**
- 프로그래밍은 코드에 관한 것이지만 프로그램은 데이터에 관한 것이다.
- 더 작은 변환들로 나누기
- 상태를 쌓아 놓지 말고 전달하라.
- 변환은 프로그래밍을 변환한다.
    - 코드를 일련의 변환으로 생각하는 접근 방식은 프로그래밍을 해방시킨다.
    - 익숙해지는 데는 시간이 좀 걸리지만, 일단 습관을 들이면 여러분의 코드가 더 명확해지고, 함수는 짧아지며, 설계는 단순해질 것이다.

### Topic 31. 상속세
- 상속도 일종의 결합이다.
- 타입을 정의하기 위해 상속을 쓸 때의 문제
    - 클래스 사이의 아주 작은 미묘한 차이까지 잡아내서 표현하기 위해 계층 위에 계층을 덧붙이다 보면, 클래스의 계층도는 순식간에 벽면 전체를 덮는 괴물로 자라단다.
    이런 복잡도는 애플리케이션을 더 취약하게 만든다.
    - 다중 상속 문제
- 상속세를 내지 말라
- 상속의 대안
    - 인터페이스와 프로토콜
    - 위임
    - 믹스인과 트레이트
- 위임
    - 상속은 개발자들이 점점 더 많은 클래스를 만들도록 유도한다.
    - 서비스에 위임하라. Has-A가 Is-A 보다 낫다.
- 믹스인
    - 기존의 것과 새로운 것의 기능 집합을 합치는 것
    - 영속성
    - 검증
    - 믹스인으로 기능을 공유하라
- 상속이 답인 경우는 드물다.
    - **타입 정보를 공유하고 싶은 건지, 기능을 더하고 싶은 건지, 메서드를 공휴하고 싶은 건지에 따라 의도를 잘 드러내는 기법을 사용하라.**

### Topic 32. 설정
- 외부 설정으로 애플리케이션을 조정할 수 있게 하라
- 도도 코드를 작성하지 말라


