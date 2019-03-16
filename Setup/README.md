## Eggplant Functional 환경설정
------
### 트라이얼 신청, 다운로드, 설치
1. Eggplant Functional은 상용(유료) 제품입니다.
2. [신청 페이지](http://info.eggplant.io/try-eggplant)에서 30일 트라이얼 라이선스를 요청할 수 있습니다.
3. [다운로드 페이지](https://eggplant.io/eggplant-functional-downloads)에서 사용중인 OS에 맞는 인스톨러를 다운로드 합니다.
4. 모바일 기기(iOS, Android) 연결을 위해서는 [모바일 게이트웨이 프로그램](https://eggplant.io/mobile-gateways)도 다운로드 합니다.
5. 다운로드된 인스톨러를 실행하면 일반적인 프로그램 설치 과정과 동일하게 설치됩니다.
[공식 웹사이트: 시작하기](http://docs.testplant.com/ePF/gettingstarted/epf-getting-started-eggplant-functional.htm)
------
### 설치환경
1. 최소사양
   * **64-bit OS만 지원합니다.**
   * Windows 10, Windows 8, Windows 7, Windows Server 2012, Windows Server 2008
   * macOS 10.13, macOS 10.12. OS X 10.11, OS X 10.10, OS X 10.9
   * RAM: 4 GB or more, + 1 GB for each additional instance of Eggplant Functional
   * Processor: 1.5 GHz or faster
   * [공식 웹사이트: 시스템 요구사항](http://docs.testplant.com/ePF/gettingstarted/epf-installing-eggplant-functional.htm)
2. 참고
   * RAM 8GB 이상이면 원활하게 사용할 수 있습니다.
   * 빠르고 안정적인 네트워크 환경을 권장합니다. (예: 유선, 100Mbps 이상)
   * 모바일 기기와의 통신은 기본적으로 TCP 5900번 포트를 사용합니다.
   * MacOS 기기에서는 iOS, Android, MacOS, Windows 기기에 모두 접근할 수 있으나, Windows 기기에서는 애플 정책에 의해 iOS와 MacOS 기기 접근이 제한됩니다.
------
### iOS 테스트 환경
! [오버뷰 이미지]()
1. iOS 기기에 접근하기 위해서는 사용자는 애플 개발자 프로그램 (Apple Developer Program)에 가입되어 있어야 합니다.
   * 이 문서에서는 애플 개발자 프로그램에 가입되어 있는 사용자를 기준으로 설명합니다.
   * 참고: [애플 개발자 프로그램](https://developer.apple.com/kr/programs/) 둘러보기
2. Xcode 실행
   * Xcode --> Preferences... --> Accounts: 애플 개발자 ID와 패스워드를 입력합니다.
   * Xcode는 사용자와 기기 인증 및 프로비저닝에 사용됩니다. Xcode에서 스크립팅 하지 않습니다.
3. 애플 개발자 프로그램 웹사이트
   * 애플 개발자 프로그램 웹사이트에 로그인합니다.
   * 필요한 모든 설정을 위해서는 Admin 이상의 사용자 권한이 필요합니다. (Agent > Admin > 일반 유저 순서)
------
### Android 테스트 환경
1. Android 기기 설정
   * 설정 --> 개발자 옵션 --> USB 디버깅 옵션 활성화 (Enable USB Debugging)
2. Android Gateway를 통해 연결하는 방식 (In-direct way)
   * [공식 문서](http://docs.testplant.com/ePF/using/epf-getting-started-android-gateway.htm)
   * Android 기기와 Eggplant Functional이 설치된 PC를 USB 케이블로 연결합니다.
   * PC 에서 Android Gateway와 Eggplant Functional을 실행합니다.
   * Android Gateway 기기 목록에 연결하려는 기기 이름이 표시되면 'Start' 버튼을 누릅니다.
   * 기기의 IP가 표시되면 해당 IP를 복사해서 Eggplant Functional의 'Connection List'에 추가합니다.
3. Gateway를 통하지 않고 시리얼넘버를 인식하여 바로 연결하는 방식 (Direct way)
   * [공식 문서](http://docs.testplant.com/ePF/using/epf-connecting-to-android-suts.htm)
   * Android 기기와 Eggplant Functional이 설치된 PC를 USB 케이블로 연결합니다.
   * Eggplant Functional을 실행 --> Connecgion List --> Device Name 리스트 클릭
------
### PC 테스트 환경
[공식 문서](http://docs.testplant.com/ePF/using/epf-desktop-suts.htm)
1. Windows PC
   * VNC Server 프로그램을 설치하세요.
   * UltraVNC, TightVNC를 권장합니다.
2. MacOS
   * MacOS에 내장된 ScreenShare 기능을 권장합니다.
