## Eggplant Functional 환경설정
------

### 트라이얼 신청, 다운로드, 설치
[공식 웹사이트: 시작하기](http://docs.testplant.com/ePF/gettingstarted/epf-getting-started-eggplant-functional.htm)
1. Eggplant Functional은 상용(유료) 제품입니다. 트라이얼 버전도 30일 제한만 있을 뿐 기능은 동일합니다.
2. [신청 페이지](http://info.eggplant.io/try-eggplant)에서 30일 트라이얼 라이선스를 요청할 수 있습니다.
   * 처음 신청하는 경우 Eggplant 세일즈팀이나 TAM (Technical Account Manager)에게서 영문 이메일이 올 수 있습니다.
   * 차분하게 Eggplant Functional 트라이얼을 사용하고 싶다고 답장해주시면 라이선스 키가 포함된 이메일을 받아보실 수 있습니다.
3. [다운로드 페이지](https://eggplant.io/eggplant-functional-downloads)에서 사용중인 OS에 맞는 인스톨러를 다운로드 합니다.
4. 모바일 기기(iOS, Android) 연결을 위해서는 [모바일 게이트웨이 프로그램](https://eggplant.io/mobile-gateways)도 다운로드 합니다.
5. 다운로드된 인스톨러를 실행하면 일반적인 프로그램 설치 과정과 동일하게 설치됩니다.
6. 처음 실행 시 아래 이미지와 같은 라이선스 창이 표시됩니다. 지급된 라이선스 키만 입력하고 'Add' 누르면 활성화 됩니다.
![licensing img](https://user-images.githubusercontent.com/42508143/54485799-c788d700-48c2-11e9-8f75-1d7ddd154dcc.png)
------

### 설치환경
[공식 문서: 시스템 요구사항](http://docs.testplant.com/ePF/gettingstarted/epf-installing-eggplant-functional.htm)
1. 최소사양
   * **64-bit OS만 지원합니다.**
   * Windows 10, Windows 8, Windows 7, Windows Server 2012, Windows Server 2008
   * macOS 10.13, macOS 10.12. OS X 10.11, OS X 10.10, OS X 10.9
   * RAM: 4 GB or more, + 1 GB for each additional instance of Eggplant Functional
   * Processor: 1.5 GHz or faster
2. 참고
   * RAM 8GB 이상이면 원활하게 사용할 수 있습니다.
   * 빠르고 안정적인 네트워크 환경을 권장합니다. (예: 유선, 100Mbps 이상)
   * 모바일 기기와의 통신은 기본적으로 TCP 5900번 포트를 사용합니다.
   * MacOS 기기에서는 iOS, Android, MacOS, Windows 기기에 모두 접근할 수 있으나, Windows 기기에서는 애플 정책에 의해 iOS와 MacOS 기기 접근이 제한됩니다.
------

### iOS 테스트 환경
![overview img](https://user-images.githubusercontent.com/42508143/54477473-8acdc900-484b-11e9-851c-621d739b5183.png)
1. iOS 기기에 접근하기 위해서는 사용자는 애플 개발자 프로그램 (Apple Developer Program)에 가입되어 있어야 합니다.
   * 이 문서에서는 애플 개발자 프로그램에 가입되어 있는 사용자를 기준으로 설명합니다.
   * [애플 개발자 프로그램](https://developer.apple.com/kr/programs/) 살펴보기
   * **중요: iOS, MacOS, tvOS 기기에 접근하려면 해당 기기, MacOS, 애플개발자 ID 세 가지가 모두 필요합니다.**
   
2. Xcode 설정
   * Xcode --> Preferences... --> Accounts: 애플 개발자 ID와 패스워드를 입력합니다.
      * Xcode는 사용자와 기기 인증 및 프로비저닝에만 사용됩니다. Xcode에서 코딩이나 스크립트 편집을 하지 않습니다.
![xcode img](https://user-images.githubusercontent.com/42508143/54485847-81804300-48c3-11e9-877d-829761420c50.png)
   * Xcode --> Windows --> Devices and Simulators
      * 테스트에 사용할 iOS 기기를 맥에 연결하고 Xcode에서 확인합니다.
      * 최초 연결시 몇 분 정도 소요될 수 있습니다. 기기 정보가 아래 이미지와 같이 에러없이 표시되면 정상입니다.
![xcode window img](https://user-images.githubusercontent.com/42508143/54486181-e047bb80-48c7-11e9-9df7-3b90fd99eb81.png)
      
3. 애플 개발자 프로그램 웹사이트
   * 애플 개발자 프로그램 웹사이트에 로그인합니다. 필요한 모든 설정을 위해서는 Admin 이상의 사용자 권한이 필요합니다.
   * 권한 순서: Agent (대표자) > Admin (중간 관리자) > Member (일반 사용자)
   * 아래 이미지는 개인 자격으로 애플 개발자 프로그램에 가입한 예제입니다.
![apple dev website img](https://user-images.githubusercontent.com/42508143/54485976-1899ca80-48c5-11e9-8dc7-7bf3d795338b.png)
   
3-1. Certificates, Identifiers & Profiles
   * Certificate를 생성/등록하는 단계 입니다. 사용자와 맥 장비를 인증/등록하는 과정입니다.
   * 우측 상단의 + 버튼을 눌러서 새로운 Certificate 등록을 시작합니다.
   * Development > iOS App Development 항목을 선택하고 다음 단계로 넘어갑니다. 아랫쪽 Production 항목은 선택하지 않습니다.
   * CSR 등록 단계입니다. 화면의 안내에 따라 맥 > 유틸리티 > Keychain Access 앱에서 CSR 파일을 생성해줍니다.
   * 생성된 CSR 파일을 애플 개발자 웹사이트에 업로드 합니다.
   * 등록 완료된 Certificate 파일을 다운로드 후, 더블클릭하면 Keychain Access에 자동 등록됩니다.
   
3-2. App ID
   * Eggplant Functional을 위한 App ID를 등록하는 과정입니다.
   * 팀(조직/회사)마다 처음 한번만 등록해두면 됩니다.
   * App ID 이름은 자유롭게 적용하면 되고, 실제 ID는 **com.testplant.*** 일치해야 합니다.
   * 개발 목적으로 등록하는 App ID 이므로, 실제 적용되는 ID는 *<team ID.com.testplant.*>* 와 같이 적용됩니다.
![App ID img](https://user-images.githubusercontent.com/42508143/54486270-4b45c200-48c9-11e9-917b-7071635039a5.png)
------

### Android 테스트 환경
1. Android 기기 설정
   * 설정 --> 개발자 옵션 --> USB 디버깅 옵션 활성화 (Enable USB Debugging)

2. Android Gateway를 통해 연결하는 방식 (In-direct way)
   * [공식 문서: 안드로이드 게이트웨이 연결](http://docs.testplant.com/ePF/using/epf-getting-started-android-gateway.htm)
   * Android 기기와 Eggplant Functional이 설치된 PC를 USB 케이블로 연결합니다.
   * PC 에서 Android Gateway와 Eggplant Functional을 실행합니다.
   * Android Gateway 기기 목록에 연결하려는 기기 이름이 표시되면 'Start' 버튼을 누릅니다.
   * 기기의 IP가 표시되면 해당 IP를 복사해서 Eggplant Functional의 'Connection List'에 추가합니다.

3. Gateway를 통하지 않고 시리얼넘버를 인식하여 바로 연결하는 방식 (Direct way)
   * [공식 문서: 안드로이드 기기 직접 연결](http://docs.testplant.com/ePF/using/epf-connecting-to-android-suts.htm)
   * Android 기기와 Eggplant Functional이 설치된 PC를 USB 케이블로 연결합니다.
   * Eggplant Functional을 실행 --> Connecgion List --> Device Name 리스트 클릭
------

### PC 테스트 환경
[공식 문서: 데스크탑 연결](http://docs.testplant.com/ePF/using/epf-desktop-suts.htm)
1. Windows PC
   * VNC Server 프로그램을 설치하세요.
   * UltraVNC, TightVNC를 권장합니다.
2. MacOS
   * MacOS에 내장된 ScreenShare 기능을 권장합니다.
