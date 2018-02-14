---

copyright:

  years: 2015, 2018

lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} 상태 및 알림 보기
{: #viewing-bluemix-status}

상태 페이지는 {{site.data.keyword.Bluemix_notm}} 플랫폼 및 주요 서비스에 영향을 주는 주요 이벤트에 대한 알림 및 공지사항을 찾기 위한 중심 위치입니다.
{:shortdesc}

상태 페이지에서는 다음과 같은 정보를 찾을 수 있습니다.

  * 모든 {{site.data.keyword.Bluemix_notm}} Foundry 서비스 지역에 있는 컴포넌트 및 서비스의 현재 상태
  * 인시던트 및 유지보수에 대한 공지사항 목록(시간 순서). 목록을 필터링하거나 개별 공지사항을 열어 자세한 내용을 확인할 수 있습니다.
  * 계획된 유지보수 기간(극한 상황을 제외하고 최소한 24시간 전에 게시됨)
  * 계획되지 않은 인시던트 또는 정전({{site.data.keyword.Bluemix_notm}} 팀에서 인식하는 즉시 게시됨). 인시던트 알림은 해결될 때까지 정기적으로 업데이트됩니다.
  * 다양한 {{site.data.keyword.Bluemix_notm}} 서비스 또는 플랫폼에 영향을 미치는 보안 게시판 참조
  * 사용자가 일반적으로 관심을 가지는 기타 플랫폼 전반의 공지사항
  * [구독할 수 있는 RSS 피드](#subscribing-rss-feed).

다음 옵션 중 하나를 선택하여 상태 페이지를 찾을 수 있습니다.

  * {{site.data.keyword.Bluemix_notm}} 콘솔에 로그인하십시오. 메뉴 표시줄에서 **지원**을 클릭하고 **상태**를 선택하십시오. ![몇 가지 문제](images/some_issues.svg) 아이콘에 대해 나열된 리소스를 확인하십시오. 이 아이콘은 가동 중단을 표시합니다.
  * [{{site.data.keyword.Bluemix_notm}} - 상태 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/status){: new_window}에 직접 액세스하십시오.


## 상태 모니터링의 우수 사례
{: #best-practices}

계속 정보를 받고 이에 알맞게 계획하려면 {{site.data.keyword.Bluemix_notm}}의 상태를 모니터링하기 위한 다음 우수 사례를 사용하십시오.

### 다가오는 유지보수 기간 확인
{: #monbp-checmaintwin}

다음 옵션 중 하나를 사용하여 최소한 24시간마다 한 번씩 상태 페이지에 게시된 예정된 유지보수 기간을 확인하십시오.
* [상태 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/status){: new_window} 페이지로 직접 이동
* RSS 피드 또는 RSS-to-email 전달자 사용

### 진행 중인 인시던트 또는 현재 유지보수 기간 확인
{: #monbp-checcurmaninprog}

{{site.data.keyword.Bluemix_notm}}가 예상대로 작동되지 않는다고 의심되면, 진행 중인 인시던트 또는 현재 유지보수 기간에 대해 상태 페이지를 확인하십시오. 상태 페이지에 아직 나열되지 않은 인시던트를 보고하려면 **지원**을 클릭하고 메뉴 표시줄에서 **티켓 추가**를 선택하거나 [{{site.data.keyword.Bluemix_notm}} 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://www.ibm.biz/bluemixsupport){: new_window} 도움말 페이지에 액세스하여 지원 티켓을 여십시오.

### 다중 {{site.data.keyword.Bluemix_notm}} Foundry 서비스 지역 활용
{: #monbp-multpreg}

{{site.data.keyword.Bluemix_notm}} 퍼블릭의 모든 사용자는 자동으로 US-SOUTH, US-EAST, EU-GB, EU-DE 및 AU-SYD 지역에 액세스할 수 있습니다. {{site.data.keyword.Bluemix_notm}} 글로벌 오퍼레이션 팀에서 전체 지역을 관리하여 유지보수에 미치는 영향을 방지하고 동시에 모든 지역에 영향을 미치는 인시던트의 발생 위험을 최소화합니다.

지역을 전환하려면 {{site.data.keyword.Bluemix_notm}} 메뉴 표시줄에서 지역 메뉴를 펼쳐서 다른 지역을 선택하십시오.

### 사소한 인터럽트에 대비
{: #monbp-prepmininter}

대부분의 경우 {{site.data.keyword.Bluemix_notm}}는 정상적으로 계속 사용할 수 있습니다(유지보수 기간에 있는 동안에도 마찬가지임). 하지만 사소한 서비스 인터럽트를 항상 방지할 수는 없습니다. 실행 중인 애플리케이션은 {{site.data.keyword.Bluemix_notm}}의 애플리케이션 관리 기능(예: 앱 시작 및 중지)이 일시적으로 인터럽트되는 경우에도 일반적으로 계속 사용할 수 있습니다. 실행 중인 애플리케이션의 가용성을 최대화하려면 각 애플리케이션의 인스턴스를 셋 이상 실행하십시오.

## RSS 피드 구독
{: #subscribing-rss-feed}

{{site.data.keyword.Bluemix_notm}} 상태 페이지에 대한 RSS 피드를 구독하여 알림의 경보를 수신합니다. 이 접근 방법은 상태 페이지를 정기적으로 확인하지 않고도 업데이트를 받는 방법을 제공합니다.

구독하려면 다음 단계를 수행하십시오.

1. RSS 리더를 다운로드하여 설치하십시오.
2. 다음 방법 중 하나를 사용하여 리더를 통해 피드를 구독하십시오.
    * RSS ![RSS](images/rss.svg) 아이콘을 RSS 리더로 끄십시오.
    * 마우스 오른쪽 단추로 RSS 아이콘을 클릭하고 **링크 주소 복사**를 선택한 다음 URL을 RSS 리더에 붙여넣으십시오.

자세한 정보는 리더의 **도움말** 섹션을 참조하십시오. 	   

RSS 피드를 읽는 다른 방법은 다음과 같은 웹 브라우저 플러그인을 통해 확인할 수 있습니다.
  * Chrome용 [RSS Feed ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://feeder.co/){: new_window} 리더
  * Firefox용 [Brief ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} 추가 기능

다음 사이트와 같은 뉴스 소스도 RSS 피드를 읽는 방법을 제공합니다.
  * [Feedly ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://www.feedly.com/){: new_window}
  * [G2reader ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://www.g2reader.com/en/){: new_window}

써드파티 서비스를 사용하여 각 RSS 업데이트에 대한 이메일을 자동으로 전송할 수도 있습니다. 다음 목록은 써드파티 서비스의 예입니다.

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com

{{site.data.keyword.Bluemix_notm}}에는 일반적으로 매월 약 50개의 업데이트가 있습니다.


## 인시던트 및 유지보수 이메일 알림 설정
{: #setting-up-notifications}

{{site.data.keyword.Bluemix_notm}} 퍼블릭의 경우 플랫폼 알림을 등록할 수 있습니다. 플랫폼 알림은 {{site.data.keyword.Bluemix_notm}} 플랫폼의 인시던트 및 유지보수 이벤트와 관련된 선택적 이메일 경보입니다. **관리** > **계정** > **알림**을 클릭하고 **플랫폼** 탭을 선택하여 이러한 이메일 알림을 수신하도록 선택할 수 있습니다. 계정 알림 설정에 대한 자세한 정보는 [알림 설정](/docs/account/notifications.html#setting-notifications)을 참조하십시오.
