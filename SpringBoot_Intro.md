### 스프링 부트
## 1.1 스프링 부트 소개
- 스프링의 단점을 보완하고자 만든 프로젝트
- 필요한 환경 설정을 최소화하고 개발자가 비즈니스 로직에 집중할 수 있도록 도와준다.

### 1.1.1 스프링 부트 특징
- 임베디드 톰캣,제티,언더토우를 사용하여 독립 실행이 가능한 스프링 애플리케이션 개발
- 통합 스타터를 제공하여 메이븐/그레이들 구성 간소화
- 스타터를 통한 자동화된 스프링 설정 제공
- 번거로운 XML설정을 요구하지 않음
- JAR을 사용하여 자바 옵션만으로도 배포 가능
- 애플리케이션의 모니터링과 관리를 위한 스프링 액츄에이터 제공

### 1.1.2 스프링 부트와 스프링
- 스프링 부트는 스프링 프레임워크라는 큰 틀에 속하는 도구

## 1.3 스프링 부트로 커뮤니티 게시판 설계하기
- 세션 레디스 or H2: 세션을 관리하는 NoSQL과 기본 데이터 저장을 위한 RDB 사용
- 스프링 부트 웹 MVC: 기본적인 커뮤니티 페이지
- 스프링 부트 세션 레디스: 레디스를 사용한 세션 관리
- 스프링 부트 시큐리티/ 스프링 부트 OAuth2: 커뮤니티의 회원 인증 및 권한 처리
- 스프링 부트 데이터 레스트: REST API 만들기
- 스프링 부트 배치: 주기적으로 백엔드 작업 처리. 예를 들어 페이스북 API를 사용하여 게시판의 공유 개수를 DB에 저장

## 1.4 스프링 부트 스타터 들여다보기
- 스프링 부트에서는 의존 관계를 스타터를 이용해 간편하게 설정할 수 있다.

### 1.4.1 스타터의 명명규칙 알아보기
- spring-boot-starter-* : *에 스타터명을 명시하면 된다.
- spring-boot-starter-web

### 1.4.2 스타터 내부의 의존성 확인 방법
- 특정 스타터를 사용하려 하는데 의존관게가 궁금할 때: Spring-boot-starter를 참고하여 확인한다.
- 의존 관계를 확인하지 않고 spring-boot-starter를 추가했는데 의존 관계 설정이 궁금할 때
- spring-boot-starter의 여섯가지 의존성
  - spring-boot: 스프링 부트에서 기본 제공하는 의존성
  - spring-boot-autoconfigure: 스프링 부트의 자동 환경 구성에 필요한 의존성
  - spring-boot-starter-logging: 각종 로그를 사용하는데 필요한 의존성
  - javax.annotation-api: 소프트웨어의 결함을 탐지하는 어노테이션을 지원하는 의존성
  - spring-core: 스프링 코어를 사용하는 데 필요한 의존성
  - snakeyaml: yaml을 사용하는데 필요한 의존성



  ### 1.4.6 스프링 부트 장단점
- 장점
  - 각각의 의존성 버전을 올리는 것이 수월하다
  - 특정 라이브러리에 버그가 있다 하더라도 스프링팀에서 버그픽스한 버전을 받기 편리하다.
  - 어노테이션 설정이나 프로퍼티 설정으로 세부적인 설정 없이 원하는 기능 빠르게 적용 가능
  - 별도의 외장 톰캣을 설치할 필요가 없고, 톰캣 버전도 편리하게 관리한다.

- 단점
  - 설정을 개인화하면 버전을 올릴 때 기존 스프링 프레임워크를 사용하는 것과 동일한 불편함을 겪을 수 있다.
  - 특정 설정을 개인화 혹은 자체를 변경하고 싶다면 내부의 설정코드를 살펴보아야 함