# EP 16-21

# EP 16 : IE

## **인터넷 익스플로러가 구닥다리가 되어버린 이유는?**

```html
**인터넷 익스플로러(IE)는 한때 지배적인 웹 브라우저였지만, 이후 구글 크롬, 모질라 파이어폭스, 애플 사파리와 같은 다른 브라우저들에게 시장 점유율을 빼앗겼다. IE가 이러한 다른 브라우저들보다 뒤처진 몇 가지 이유가 있다:

업데이트 및 지원 부족: 마이크로소프트는 2016년 IE에 대한 주류 지원을 중단했고, 더 이상 보안 업데이트를 받지 않아 해킹 및 악성 프로그램 공격에 더욱 취약하다.

제한된 피쳐 세트: 다른 브라우저들은 계속해서 새로운 기능을 추가하고 성능을 향상시켰지만, IE는 이러한 발전을 따라가지 못했다.

호환성 부족: 일부 웹 사이트와 웹 응용 프로그램은 IE가 아닌 다른 브라우저의 최신 버전에서만 작동하도록 설계되었습니다.

성능 저하: Internet Explorer(인터넷 익스플로러)는 리소스를 많이 사용하고 속도가 느리기 때문에 사용자 환경이 좋지 않을 수 있습니다.

더 나은 대안: Chrome, Firefox, Safari와 같은 다른 브라우저들은 많은 사용자들의 기본 브라우저가 되었고, 그것들은 더 많은 기능, 더 나은 성능, 그리고 더 나은 보안을 제공한다.

전반적으로, 인터넷 익스플로러의 쇠퇴의 이유는 다면적이지만, 주요 요인은 지원과 개선의 부족, 낮은 호환성, 낮은 성능, 더 나은 대안의 부상이다.**
```

## **웹 브라우저의 핵심 프로그램은 '렌더링 엔진'이라고 부르는데, 각각 대표적인 브라우저들이 어떻게 이것을 활용하는가?**

```html
**The rendering engine, also known as the layout engine or web engine, is the core component of a web browser that is responsible for displaying the content of a web page. Different web browsers use different rendering engines, each with its own strengths and weaknesses.

Here are a few examples of how some popular web browsers use their rendering engines:

1. Google Chrome: Chrome uses the Blink rendering engine, which is a fork of the WebKit engine. Blink is known for its high performance, fast page loading times, and support for modern web technologies.

2. Mozilla Firefox: Firefox uses the Gecko rendering engine. Gecko is known for its support for web standards and its ability to display complex web pages. It also has a powerful layout engine that can handle large and complex web pages more efficiently.

3. Apple Safari: Safari uses the WebKit rendering engine, which is known for its high performance and support for web standards. It is designed to work well with the Mac and iOS operating systems, and it is optimized to display pages quickly and smoothly on mobile devices.

4. Internet Explorer: Internet Explorer used to use Trident rendering engine, it was known for its support for the ActiveX technology, which allowed for the use of rich multimedia content and interactive web pages.

5. Microsoft Edge: Edge uses the EdgeHTML rendering engine, which is derived from Trident. EdgeHTML is designed to be more efficient and modern than Trident, and it has better support for web standards and newer technologies.

It's worth noting that some browsers such as Microsoft Edge uses Chromium, which is an open-source project that provides the rendering engine and other components for Chrome, and other Chromium-based browsers.

In summary, different web browsers use different rendering engines, each with its own strengths and weaknesses. They all have different ways of utilizing their engines to display web pages. Some of the popular browsers like Chrome and Safari use Webkit, Firefox uses Gecko, Internet Explorer used to use Trident and Edge uses EdgeHTML.**
```

# EP17 : HTTP Cookie(HyperText Transfer Protocol)

## Cookie란?

```html
**HTTP 쿠키는 사용자가 웹 사이트를 방문할 때 웹 브라우저에 의해 사용자의 장치에 저장되는 작은 텍스트 파일입니다. 사용자의 기본 설정, 검색 기록 및 웹 사이트와의 상호 작용과 관련된 기타 정보를 저장하는 데 사용됩니다.

쿠키는 다음과 같은 다양한 용도로 사용됩니다:

1. 사용자 기본 설정 저장: 웹 사이트는 쿠키를 사용하여 사용자의 기본 설정(예: 기본 언어 또는 글꼴 크기)에 대한 정보를 저장할 수 있습니다.

2. 사용자 로그인 유지: 웹 사이트는 사용자가 브라우저를 닫은 후에도 쿠키를 사용하여 계정에 로그인한 상태로 유지할 수 있습니다.

***3. 사용자 동작 추적: 웹 사이트는 쿠키를 사용하여 사용자의 검색 기록을 추적할 수 있으며, 이는 대상 광고 또는 분석에 사용될 수 있습니다.

4. 사용자 환경 개인 설정: 웹 사이트는 쿠키를 사용하여 관심사와 관련된 내용을 표시하는 등 사용자의 경험을 개인화할 수 있습니다.

쿠키는 HTTP 요청 및 응답의 헤더에 있는 브라우저와 서버 간에 전송됩니다. 브라우저는 웹 사이트에 대한 모든 쿠키를 요청 헤더의 서버로 보내고 서버는 해당 정보를 사용하여 사용자 지정 응답을 반환할 수 있습니다.

It's worth noting that cookies can be deleted or blocked by the user, and many browsers provide options to manage cookies. Also, many websites are required by law to provide clear and comprehensive information about their use of cookies and to obtain the user's consent to store and access cookies on their device.**
```

## Cookie를 활용한 tarketed AD?

```html
**it is common for services like Instagram and Naver to track users' behavior through the use of cookies and other technologies, and to use that data to display targeted advertisements to users. This is done by collecting data on a user's browsing history, search queries, and interactions with the website and using that data to display ads that are relevant to the user's interests. It is a common practice among various websites and apps, especially those that rely on advertising revenue, as targeted ads tend to be more effective in terms of generating revenue.

It's worth noting that many websites are required by law to provide clear and comprehensive information about their use of cookies and to obtain the user's consent to store and access cookies on their device. So, these platforms also have their own privacy policy that explains how they use cookies and other technologies to track user behavior and show targeted ads, and users have the options to manage their preferences.**
```

## ‘쿠키는 HTTP 요청의 헤더에 포함된다’의 의미는?

```html
**브라우저가 서버에 HTTP 요청을 발송할 때 요청에 대한 추가 정보를 제공하는 헤더 집합을 포함합니다. 쿠키는 브라우저가 사용자의 환경설정 및 검색 기록에 대한 정보를 서버로 보내는 방법으로 HTTP 요청의 헤더에 포함됩니다.

쿠키는 세미콜론으로 구분된 이름-값 쌍의 문자열을 포함하는 "Cookie" 헤더의 형태로 HTTP 요청의 헤더에 포함됩니다. 예를 들어, 이름이 "cookie_id"이고 값이 "cookie"인 쿠키는 "cookie: session_id=cookie123"으로 헤더에 포함됩니다.

이렇게 하면 서버가 쿠키에 저장된 정보를 읽고 응답을 사용자 정의하는 데 사용할 수 있습니다. 예를 들어, 서버가 세션 ID가 포함된 쿠키와 함께 요청을 수신할 경우, 서버는 사용자가 브라우저를 닫더라도 해당 ID를 사용하여 사용자를 식별하고 로그인 상태를 유지할 수 있습니다.

쿠키를 사용하여 사용자의 검색 기록, 검색 쿼리 및 웹 사이트와의 상호 작용과 같은 사용자의 동작 및 기본 설정을 추적할 수도 있습니다. HTTP 요청의 헤더에 쿠키를 포함시킴으로써 브라우저는 이 정보를 서버로 전송하여 관심사와 관련된 내용을 표시하거나 대상 광고를 표시하는 등 사용자의 경험을 사용자 정의하는 데 사용할 수 있습니다.

HTTP는 일반 텍스트 프로토콜이기 때문에 쿠키도 일반 텍스트로 전송되므로 제3자에 의해 가로채기에 취약하다는 점에 주목할 필요가 있다. 이러한 이유로 암호나 신용 카드 번호와 같은 중요한 정보를 저장하는 데 쿠키를 사용하면 안 됩니다.**
```

## 제3자가 가로채지 못하도록 하는 해결방안

```html
**제3자가 쿠키를 가로채거나 쿠키에 포함된 정보를 읽는 것을 방지하는 몇 가지 방법이 있습니다:

HTTPS 사용: HTTP Secure(HTTP Secure)는 브라우저와 서버 간에 전송되는 데이터를 암호화하는 HTTP의 보다 안전한 버전입니다. HTTPS를 사용하면 쿠키가 암호화되어 브라우저와 서버에서만 읽을 수 있으므로 제3자가 쿠키를 가로채고 읽기가 훨씬 어려워집니다.

HttpOnly 및 보안 플래그 사용: 쿠키는 HttpOnly로 표시될 수 있으며, 이는 페이지에서 실행 중인 자바스크립트 코드가 아닌 브라우저에서만 액세스할 수 있음을 의미합니다. 이를 통해 공격자가 쿠키를 훔치려고 페이지에 악의적인 코드를 주입하는 XSS(사이트 간 스크립팅) 공격을 방지할 수 있습니다. 쿠키를 보안으로 표시할 수도 있습니다. 즉, HTTP가 아닌 HTTPS를 통해서만 전송됩니다.

동일 사이트 쿠키 사용: 동일한 사이트 쿠키는 사이트 간 요청 위조(CSRF) 공격의 위험을 완화하는 방법입니다. 웹 사이트가 쿠키를 설정한 동일한 웹 사이트에서 요청한 경우에만 쿠키를 전송하도록 지정할 수 있습니다.

쿠키 범위를 제한합니다: 특정 경로 및 도메인에 대해 쿠키를 설정하여 쿠키 범위를 제한합니다. 이렇게 하면 쿠키가 의도한 페이지에만 전송되고 의도하지 않은 사용자가 액세스할 수 없습니다.**
```

## HTTP와 HTTPS의 성능 차이는?

```html
**성능 면에서 HTTPS와 HTTP는 약간의 차이가 있을 수 있지만 이러한 차이가 전체 성능에 미치는 영향은 특정 사용 사례에 따라 달라질 수 있습니다.

HTTPS는 브라우저와 서버 간에 데이터를 교환하기 전에 보안 연결을 설정해야 하므로 요청-응답 프로세스에 약간의 지연 시간을 추가할 수 있습니다. 이는 보안 *SSL/TLS 연결을 설정하는 추가 단계 때문입니다.

또한 HTTPS는 HTTP보다 더 많은 리소스를 사용합니다. 각 요청에는 SSL/TLS 핸드셰이크가 필요하므로 서버와 클라이언트 시스템에 더 많은 부하를 줄 수 있습니다.

반면, HTTP는 데이터 암호화 및 암호 해독과 관련된 오버헤드가 없기 때문에 이미지 및 텍스트와 같은 정적 콘텐츠를 제공할 때 HTTPS보다 빠를 수 있습니다.

그러나 사용자를 추적하는 데 사용할 수 있는 타사 스크립트, 쿠키 및 기타 리소스가 늘어나고 정교한 사이버 공격이 증가함에 따라 웹이 더욱 복잡해짐에 따라 HTTPS의 보안 이점이 더욱 중요해지고 작은 성능 저하를 능가하고 있습니다.

요약하자면, HTTP와 HTTPS의 성능 차이는 다를 수 있지만, HTTPS의 보안 이점은 일반적으로 잠재적인 성능 저하를 능가합니다. 따라서, 대부분의 웹 사이트는 현재 웹 사이트를 보호하기 위한 표준으로 HTTPS를 사용하고 있습니다.**
```

# EP19 Server

## Server란?

```html
**네이버에 접속하면, 메인 화면이 나온다. 이것은 '사용자가 www.naver.com이라고 요청을 보내면 네이버 메인 화면에 맞는 자료를 모두 넘겨줘'라는 코드가 실행된 것이다. 즉, 서버는 우리가 웹 사이트 주소를 입력하기를 기다렸다가 해당 주소가 입력되면 이에 맞는 웹 페이지를 꺼내서 보여 주는 코드라고 생각하면 된다.**
```

# EP20 Full-stack Dev

## Devops

```html
**데브옵스란 소프트웨어 개발과 운영의 합성어입니다. 소프트웨어 개발자와 정보 기술 전문가 사이에 소통, 협업 통합을 강조하는 개발 환경이나 문화를 말합니다.

DevOps는 소프트웨어 개발 팀과 IT 운영 팀 간의 협업과 커뮤니케이션을 개선하여 소프트웨어와 서비스를 보다 빠르고 안정적으로 제공하는 것을 목표로 하는 일련의 관행 및 문화입니다. 개발과 운영의 간극을 메우는 방식으로 자동화, 모니터링과 테스트, 지속적인 통합과 배치를 강조하는 업무 방식이다.

데브옵스의 주요 측면은 다음과 같다:

자동화: 테스트, 구현 및 인프라 관리와 같은 반복적인 작업을 자동화하면 팀의 이동 속도가 빨라지고 오류 위험이 줄어듭니다.

CI/CD(Continuous Integration and Deployment): 이 방법을 통해 팀은 새로운 코드 변경 사항을 지속적으로 공유 코드 저장소에 통합하고 코드를 자동으로 구축 및 테스트한 다음 스테이징 또는 프로덕션 환경에 배포할 수 있습니다.

모니터링 및 로깅: DevOps 팀은 모니터링 및 로깅 도구를 사용하여 시스템의 성능과 상태를 주시하고 문제를 신속하게 식별하고 해결합니다.

협업: DevOps 팀은 개발자, 운영 및 기타 이해관계자와 긴밀하게 협력하여 소프트웨어가 빠르고 안정적으로 제공되도록 보장합니다.

문화: 데브옵스는 단순한 도구나 관행의 집합이 아니라 협업, 커뮤니케이션, 지속적인 개선의 문화이다.

조직은 DevOps 관행을 통해 소프트웨어와 서비스를 더 빠른 속도로 제공하고 더 높은 안정성과 보안을 제공할 수 있습니다. 이를 통해 조직은 출시 기간을 단축하고 변화하는 비즈니스 요구사항에 보다 신속하게 대응할 수 있습니다. 조직들이 급변하는 디지털 환경에서 경쟁력을 유지하기 위해 보다 민첩하고 유연한 작업 방식으로 전환하고자 함에 따라 DevOps의 중요성이 점점 커지고 있습니다**

```

# EP21 서버리스

## AWS 람다, Google Cloud Function, Apex

```html
**AWS 람다, 구글 클라우드 함수, 에이펙스는 모두 개발자가 서버를 프로비저닝하거나 관리하지 않고 코드를 실행할 수 있는 "서버리스" 컴퓨팅 플랫폼의 예입니다. 개발자가 HTTP 요청이나 큐의 메시지와 같은 특정 이벤트에 응답하여 실행되는 코드를 작성할 수 있다는 점에서 유사하다. 그러나 기능과 기능 면에서 약간의 차이가 있습니다.

AWS 람다: AWS 람다(AWS Lambda)는 아마존 웹 서비스(AWS)에서 제공하는 컴퓨팅 서비스로, 개발자가 서버를 프로비저닝하거나 관리하지 않고도 코드를 실행할 수 있게 해준다. 광범위한 프로그래밍 언어를 지원하며 S3, 디나모DB, SNS 등 다른 AWS 서비스와의 통합 생태계가 넓다.

Google 클라우드 기능: 구글 클라우드 함수(Google Cloud Functions)는 구글 클라우드가 제공하는 서버리스 컴퓨팅 플랫폼으로, 개발자가 서버를 프로비저닝하거나 관리하지 않고도 코드를 실행할 수 있도록 한다. AWS 람다와 비슷한 범위의 프로그래밍 언어를 지원하며 클라우드 스토리지, Pub/Sub 등의 다른 구글 클라우드 서비스와 통합된다.

에이펙스: 에이펙스는 개발자들이 AWS 람다에서 서버리스 애플리케이션을 구축할 수 있는 오픈 소스 프레임워크이다. 람다 기능을 쉽게 관리하고 배포할 수 있는 간단한 명령줄 도구를 제공하며, S3, DynamoDB 등 다른 AWS 서비스와 함께 사용할 수 있다.

장점 측면에서 AWS 람다와 구글 클라우드 기능은 모두 크고 성숙한 생태계를 가지고 있으며, 많은 통합과 도구를 사용할 수 있다. 반면에, 에이펙스는 오픈 소스 프로젝트이기 때문에 더 유연하고 사용자 정의가 가능할 수 있다.

궁극적으로 사용 사례에 가장 적합한 플랫폼은 사용해야 하는 프로그래밍 언어, 통합하려는 서비스 및 필요한 지원 수준과 같은 특정 요구사항에 따라 달라집니다. 플랫폼마다 가격 모델이 다르기 때문에 서비스 운영 비용도 고려해 볼 만하다.**
```