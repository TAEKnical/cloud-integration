# iPaaS (integration Platform as a Service)

---

# 0. 목차

### [1. 사전 지식](#사전-지식)

1) IaaS vs PaaS vs SaaS

2) 서비스 통합의 역사

3) 기타

### [2. iPaaS](#iPaaS)

1) iPaaS의 정의

2) iPaaS의 필요성

### [3. iPaaS의 특징](#iPaaS의-특징)

1) iPaaS의 장점

2) iPaaS의 단점

### [4. 결론](#결론)

<br>

---

# 1. 사전 지식

## 1) IaaS vs PaaS vs SaaS

![iPaaS%20(integration%20Platform%20as%20a%20Service)%2015d235bed90846faa1422d743dd2c037/Untitled.png](iPaaS%20(integration%20Platform%20as%20a%20Service)%2015d235bed90846faa1422d743dd2c037/Untitled.png)

<br>

### [1] SaaS

---

서비스로서의 소프트웨어를 뜻한다. 소프트웨어 자체를 서비스로 제공하는 것으로 세 가지 유형 중 가장 일반에 익숙한 개념이다. 로컬 환경에 인스톨러를 다운로드하는 등의 번거로운 설치과정을 거치지 않고 인터넷 브라우저에 접속해서 바로 사용할 수 있도록 클라우드 형태로 관리 및 제공되는 서비스들이 더 많아졌다. 대표적으로 Google Docs나 Dropbox, 네이버 클라우드, Notion, Slack 등이 SaaS에 해당하는 서비스이다.

서비스를 이용하고자 할 때 언제 어디서든 접속해서 사용하는 구조이며, 이 때 소프트웨어의 업데이트 및 보안 패치 관리 등은 사용자가 신경쓸 필요가 없다. 소프트웨어를 사용하기 위해 필요한 것들에 대하여 A to Z로 모두 관리해주는 서비스이다. 일반적으로 소프트웨어 서비스에 접속해서 계정을 만들고 얼마의 기간동안 사용할건지를 선택하고 비용을 지불하는 방식이다. 우리가 이미 알고있는 개념과 결합하여 생각해보면 SAAS의 경우는, 가전 렌탈과 비슷하다고 할 수 있다.

공기청정기나 정수기 같은 가전 렌탈은 청정이 얼마나 되었는지, 물을 얼마나 사용했는지에 비례하여 사용 금액을 산정하는 것이 아니라 사용 기간을 약정하여 비용을 청구한다. 렌탈비용에 관리비까지 포함되어 있기 때문에 필터 교체 등과 같이 사용과 관련없는 작업들을 모두 관리해주는 개념도 유사하다. 이러한 형태의 서비스를 Subscribtion형 서비스 운영이라고 지칭한다.

<br>

### [2] IaaS

---

사용자가 API에 요청하는 과정을 거쳐야 하면 이를 IaaS로 분류한다. 예를 들어 API에 요청해서 VM instance를 생성한다면 이는 IaaS에 해당한다. 웹 개발을 위해 특정 버전의 OS와 웹 서버, DB 환경을 설치하는 요청을 보낸다면 이 역시 IaaS이다. 환경 구축에 대한 선택권의 대부분이 사용자에게 넘어가고, 요청한 컴퓨팅 환경만 제공받는 형태이다. 대표적으로 AWS EC2, GCP Google Compute Engine, Azure Virtual Machines 등을 모두 IaaS로 분류할 수 있다.

사용자는 자신이 사용하기로 요청한 리소스에 대해서 직접 관리해야한다. 즉, 사용자가 구축하고자 하는 환경을 위한 리소스가 클라우드 환경에 미리 준비되어 있고 사용자는 그 위에서 어떤 OS와 어떤 어플리케이션을 동작시킬지만 결정하면 된다. 관리 측면에서 보면 개발자와 인프라 관리자의 역할을 분리시킬 수 있기에 하위 레이어에 대해서는 고민할 필요가 없다는 특징이다. 이는 IaaS의 장점이자 단점이 될 수 있다.

IaaS는 고객이 원하는 인프라를 제공하고 제공한 리소스만큼 비용을 청구하는 형태로 운영된다.

<br>

### [3] PaaS

---

플랫폼 자체를 서비스(상품)으로서 제공하는 형태의 서비스이다. 개발자 입장에서 서버, 스토리지, 백업과 같은 작업들은 피하고 싶은 대상이다. 개발 환경 구축을 위한 기반 인프라에 대해 신경쓰지 않고 오로지 개발에만 집중하여 애플리케이션을 개발하고 테스트할 수 있도록 하는 일련의 서비스를 PaaS로 정의한다. 따라서 PaaS에서는 개발을 위한 안정적인 환경(Platform) 뿐만 아니라 그 환경을 바탕으로 하는 애플리케이션을 개발할 수 있는 API까지 제공한다. 대표적으로 Google App Engine, Salesforce Heroku, OpenShift가 PaaS로 분류된다.

PaaS 에서는 하드웨어는 물론 운영체제, 네트워크 구축까지 전혀 고민할 필요 없이 어떤 애플리케이션을 구축해서 실행할 것인지만 고민하고 개발 소스코드만 작성하면 된다. IaaS에 더하여 OS가 미리 설치되고 그 위에 nodejs, java와 같은 런타임이 미리 설치되어 있어서 소스코드만 준비되면 바로 동작시킬 수 있는 환경이다.

<br>

<br>

## 2) 서비스 통합의 역사

### [1] Legacy

---

### ![iPaaS%20(integration%20Platform%20as%20a%20Service)%2015d235bed90846faa1422d743dd2c037/Untitled%201.png](iPaaS%20(integration%20Platform%20as%20a%20Service)%2015d235bed90846faa1422d743dd2c037/Untitled%201.png)

기업이 업무를 처리하기 위해서는 각종 시스템이 필요하다. 인사 관리 시스템, 회계 시스템, 재무 시스템 등 수 많은 시스템이 필요하다. 초기에 시스템의 수가 얼마 되지 않을 때는 P2P 방식으로 연결해주었으나, 시간이 지나면서 시스템의 수는 기하급수적으로 늘어나게 되었고 기존의 연결 방식은 사용성 뿐만 아니라 관리 측면에서도 문제를 야기하였다.

<br>

### [2] EAI(Enterprise Application Integeration)

---

![iPaaS%20(integration%20Platform%20as%20a%20Service)%2015d235bed90846faa1422d743dd2c037/Untitled%202.png](iPaaS%20(integration%20Platform%20as%20a%20Service)%2015d235bed90846faa1422d743dd2c037/Untitled%202.png)

이를 해결하기 위하여 EAI가 등장하였고, 시스템들의 한 가운데 일종의 허브(미들웨어)로서 EAI를 두어 모든 통신이 EAI를 거치도록 하였다. 기존의 아키텍처에서 각각의 시스템은 서로 다른 환경을 가지고 있으며 서로 다른 데이터 포맷을 사용하므로 이들 시스템간에는 어떤 표준화도 이루어지지 않은 상태였는데, EAI는 모든 시스템에 대하여 각각의 어댑터를 가지고 있어서 제각기 전달된 데이터 포맷을 대상 시스템의 어댑터를 통하여 포맷에 맞게끔 전달해 주어 기존 P2P 아키텍처의 문제를 해결할 수 있었다.

EAI를 기반으로 하는 기업 환경의 변화는 유지보수의 편의와 신속한 의사결정을 이루어냈다. 덕분에 EAI 아키텍처는 아직도 많은 기업에서 쓰이고 있지만 EAI 아키텍처에도 단점이 존재한다. 새로운 서비스가 추가되면 이에 해당하는 어댑터를 추가해 주어야 한다는 번거로움이 있다는 점이다. 따라서 관리와 서비스 확장을 위한 비용이 많이 들 수 밖에 없다.

<br>

### [3] SOA(Service Oriented Architecture)

---

![iPaaS%20(integration%20Platform%20as%20a%20Service)%2015d235bed90846faa1422d743dd2c037/Untitled%203.png](iPaaS%20(integration%20Platform%20as%20a%20Service)%2015d235bed90846faa1422d743dd2c037/Untitled%203.png)

각 시스템을 서비스로 취급하며 XML 기반의 웹 인터페이스로 접근하고 관리할 수 있는 아키텍처이다. 시간이 지날 수록 시스템이 다양화 되면서 이기종간의 통합이 더욱 요구되었고, 때문에 매번 서비스가 추가될 때 마다 어댑터를 추가하기보다는 아예 시스템간 표준화를 지향하면서 SOA가 등장하게 되었다. 웹 서비스 기반으로 데이터 송수신을 표준화 시켰기 때문에 서비스간의 통신에 더이상 EAI에 있었던 어댑터 개념이 필요치 않게 되었다. 대신 서비스간의 통신을 위하여 서비스 버스 개념이 도입되었는데, 이를 ESB(Enterprise Service Bus)라고 하며 SOA의 기반이 되는 아이디어이다.

<br>

<br>

## 3) 기타

### [1] **OAuth**

---

OAuth는 기존의 쿠키와 세션 기반의 사용자 인증 방식을 보완한 토큰 기반의 인증 방식이다. 엄밀히 말하면, 사용자 인증을 인가하는 방식이라고 할 수 있다.

<br>

### [2] J**WT (JSON Web Tokens)**

---

JWT는 Json 포맷을 이용하여 사용자에 대한 속성을 저장하는 Claim 기반의 Web Token이다. JWT 토큰은 발급자, 제목 (클레임), 만료 시간 등에 대한 정보를 포함하는 JSON 인코딩 된 데이터 구조다. 변조 및 신뢰성을 위해 서명되며 대칭 또는 비대칭 접근 방식을 사용하여 토큰 정보를 보호하기 위해 암호화 될 수 있다.

<br>

### [3] **ODATA (Open Data Protocol)**

---

OADTA는 단순하고 표준적인 방법으로 쿼리 가능하고 상호 운용 가능한 REST API를 생성하고 사용할 수있는 개방형 프로토콜이다.

<br>

### [4] **OPENID**

---

OpenID는 현재 구글 뿐만 아니라 많은 글로벌 플랫폼들이 다른 서비스에게 사용자 인증을 제공을 위해 사용하고 있는 프로토콜이다. OpenID Connect는 기본적으로 OAuth 프로토콜을 기반으로 작동하는 프로토콜이기 때문에 기술적으로 사용하는 방법이 매우 유사하지만 사용하는 목적에서는 큰 차이가 있다. OPENID는 인증(Authentication)을 위해서 사용하고, OAuth는 인가(Authroization)를 위해서 사용한다.

<br>

### [5] **REST API**

---

REST API는 REST 아키텍처의 제약 조건을 준수하는 애플리케이션 프로그래밍 인터페이스다. REST API를 통해 중요한 데이터를 은행 또는 의료 앱과 같은 모바일 앱에 쉽게 연결할 수있는 iPaaS 솔루션을 사용하면 기업이 보다 민첩해져 디지털 비즈니스 가치를 더 빠르고 정확하게 제공 할 수 있다.

<br>

<br>

<br>

# 2. iPaaS

## 1) iPaaS 개요

# ![https://user-images.githubusercontent.com/69182192/91016099-2fe6f680-e627-11ea-9ebe-40665d388895.png](https://user-images.githubusercontent.com/69182192/91016099-2fe6f680-e627-11ea-9ebe-40665d388895.png)

iPaaS 는 소프트웨어 엔지니어가 응용 프로그램 및 서비스를 배포, 관리 및 통합 할 수있는 클라우드 기반 도구 모음이다. iPaaS를 통해 사용자는 클라우드 또는 온-프레미스<sup>[1](#footnote_1)</sup>에 있는 응용 프로그램을 연결하는 통합 흐름을 개발한 다음 일일이 하드웨어를 관리하거나 미들웨어를 설치하지 않아도 서비스를 배포할 수 있다. 

<a name="footnote_1">1</a>온-프레미스 : 온프레미스(On-premise)란 소프트웨어 등 솔루션을 클라우드 같이 원격 환경이 아닌 자체적으로 보유한 전산실 서버에 직접 설치해 운영하는 방식을 말한다.

<br>

<br>

## 2) iPaaS의 필요성

엔터프라이즈 기업들이 업무용으로 다양한 SaaS를 도입하면서 기존에 구축한 시스템과 애플리케이션 등을 SaaS에 연계시키는 제품이 주목받고 있다. AWS와 Azure기반 위에서 제공하거나 독자적으로 서비스를 제공하는 기업들이 늘면서 시장 요구를 수용하기 위해 스타트업들과 기존 기업들이 관련 기능을 제공한다. 이미 클라우드 시장이 일반화된 해외의 경우 iPaaS 시장 경쟁이 치열하게 이루어지고 있고, 국내에서도 대기업들이 SaaS를 도입하기 시작하면서 iPaaS에 대한 관심은 빠르게 늘어날 것으로 예상된다.

<br>

<br>

<br>

# 3. iPaaS의 장단점

## 1) iPaaS의 장점

### [1] 접근성

---

인터넷 연결을 통해 어디서나 액세스 할 수 있는 웹 인터페이스를 제공한다.

<br>

### [2] 연결성

---

일반적으로 통합 flow와 API 개발 속도를 높이고 효율적으로 하기 위해서 사전 구축된 커넥터와 비즈니스 규칙 등을 제공한다. 사전 구축된 커넥터를 통해 여러 SaaS 애플리케이션과 일반적인 데이터베이스 (SQL, MySQL, ORACLE) 및 API와의 통신을 수월하게 하기 위해 REST 및 JSON과 같은 최신 메시징 및 문서 형식을 지원한다.

<br>

### [3] 통합성

---

조직 내부의 온프레미스 환경과 클라우드 환경에서의 솔루션 및 데이터를 통합해준다. 기업은 온프레미스, 클라우드 또는 하이브리드 환경을 사용하여 애플리케이션 및 데이터를 통합함으로써 차별화되고 경쟁력 있는 서비스를 제공할 수 있다.

<br>

### [4] 실시간 처리

---

효율적인 의사 결정을 가능하게 해주며 신속한 처리로 고객 응답 시간을 개선할 수 있다.

<br>

### [5] 비용 절감

---

하드웨어나 미들웨어의 구매 및 관리 비용이 따로 들지 않아 비용을 절감시킬 수 있다. 기능이나 데이터를 신속하게 추가 또는 제거할 수 있으므로 장애나 다운타임 및 개발 시간을 감축할 수 있으므로 유지보수 및 개발비용의 절감을 기대할 수 있다.

<br>

<br>

## 2) iPaaS의 단점

### [1] 버그 발생 가능성

---

 복잡한 수준의 시스템 통합 및 Work-flow에는 버그가 발생할 수 있다.

<br>

### [2] 일부 앱 제한적

---

 공식적으로 지원되는 앱만 사용하도록 제한한다.

<br>

<br>

<br>

# 4. 결론

iPaaS 환경에서는 소프트웨어 엔지니어가 응용 프로그램 및 서비스를 배포, 관리 및 통합 할 수있는 클라우드 기반 도구 모음으로써 iPaaS를 통해 사용자는 클라우드 또는 온-프레미스에 있는 응용 프로그램을 연결하는 통합 흐름을 개발한 다음 일일이 하드웨어를 관리하거나 미들웨어를 설치하지 않아도 서비스를 배포할 수 있기 때문에 서비스를 제공하는 기업들이 기존에 구축한 시스템과 애플리케이션 등을 SaaS에 연계시키는 작업을 최적화 할 수 있다.

<br>

<br>

<br>

# 5. 작성자

이진태 (**blog :**  [https://blog.naver.com/ilikebigmac](https://blog.naver.com/ilikebigmac) ,  **github:**  https://github.com/TAEKnical ) 

신길용 ()

강혜수 ()

정미영 ()

<br>

<br>

<br>

# 참고 문헌

### What ESB and SOA are anyway

[https://zato.io/docs/intro/esb-soa.html](https://zato.io/docs/intro/esb-soa.html)

### SOA 실현의 핵심, ESB - 1. 기업 환경 통합을 위한 해법 EAI에서 ESB까지

[https://www.kdata.or.kr/info/info_04_view.html?field=&keyword=&type=techreport&page=271&dbnum=127134&mode=detail&type=techreport](https://www.kdata.or.kr/info/info_04_view.html?field=&keyword=&type=techreport&page=271&dbnum=127134&mode=detail&type=techreport)

### TOPIC 7 Enterprise Application Architecture (EAI)

[https://slideplayer.com/slide/10318069/](https://slideplayer.com/slide/10318069/)

### IPaaS Managed Service

[https://www.indiamart.com/easystepin-it-services-private-limited/ipaas-managed-services.html](https://www.indiamart.com/easystepin-it-services-private-limited/ipaas-managed-services.html)

### What is iPaaS (Integration Platform as a Service) and why does your company need it

[https://www.edicomgroup.com/en_ES/news/11980-what-is-ipaas-integration-platform-as-a-service-and-why-does-your-company-need-it.html](https://www.edicomgroup.com/en_ES/news/11980-what-is-ipaas-integration-platform-as-a-service-and-why-does-your-company-need-it.html)