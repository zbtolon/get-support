---

copyright:

  years: 2015, 2018

lastupdated: "2019-05-16"

keywords: upcoming maintenance, stay up-to-date, monitor status

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 상태 모니터링의 우수 사례
{: #best-practices}

플랜을 작성하고 계속 정보를 받으려면 {{site.data.keyword.Bluemix}}의 상태를 모니터하기 위한 다음 우수 사례를 사용하십시오.
{: shortdesc}

## 다가오는 유지보수 기간 확인
{: #monbp-checmaintwin}

다음 옵션 중 하나를 사용하여 최소한 24시간마다 한 번씩 {{site.data.keyword.Bluemix_notm}} 콘솔 대시보드 페이지에 게시된 예정된 유지보수 기간을 확인하십시오.
* [대시보드 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com){: new_window}에서 계획된 유지보수 위젯을 확인하십시오. 계획된 모든 유지보수를 보려면 **모든 이벤트**를 클릭하십시오.
* [상태 - 계획된 유지보수 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/status?selected=maintenance){: new_window} 페이지로 직접 이동하십시오.

## 진행 중인 인시던트 또는 현재 유지보수 기간 확인
{: #monbp-checcurmaninprog}

{{site.data.keyword.Bluemix_notm}}가 예상대로 작동되지 않는다고 의심되면, 진행 중인 인시던트 또는 현재 유지보수 기간에 대해 상태 페이지를 확인하십시오. 상태 페이지에 아직 나열되지 않은 인시던트를 보고하려면 메뉴 표시줄에서 **지원**을 클릭하여 지원 케이스를 여십시오. 그런 다음 지원 받기 탭에서 **케이스 새로 작성**을 클릭하십시오.

## 다중 {{site.data.keyword.Bluemix_notm}} 위치 활용
{: #monbp-multpreg}

{{site.data.keyword.Bluemix_notm}}의 모든 사용자는 댈러스, 런던, 프랑크푸르트, 시드니, 워싱턴 DC 및 도쿄 위치에 대한 액세스를 자동으로 갖습니다. {{site.data.keyword.Bluemix_notm}} 글로벌 오퍼레이션 팀에서 모든 위치를 관리하여 유지보수에 미치는 영향을 방지하고 동시에 모든 위치에 영향을 미치는 인시던트의 발생 위험을 최소화합니다.

위치를 전환하려면 대시보드로 이동하고 **위치** 메뉴를 펼치십시오.

## 사소한 인터럽트에 대비
{: #monbp-prepmininter}

대부분의 경우 {{site.data.keyword.Bluemix_notm}}는 정상적으로 계속 사용할 수 있습니다(유지보수 기간에 있는 동안에도 마찬가지임). 하지만 사소한 서비스 인터럽트를 항상 방지할 수는 없습니다. 실행 중인 애플리케이션은 {{site.data.keyword.Bluemix_notm}}의 애플리케이션 관리 기능(예: 앱 시작 및 중지)이 일시적으로 인터럽트되는 경우에도 일반적으로 계속 사용할 수 있습니다. 실행 중인 애플리케이션의 가용성을 최대화하려면 각 애플리케이션의 인스턴스를 셋 이상 실행하십시오.

## 이메일 알림 구독
{: #monbp-subscribing}

Lite 계정 소유자인 경우 {{site.data.keyword.Bluemix_notm}} 플랫폼의 계획되지 않은 이벤트(예: 정전)와 계획된 이벤트(예: 유지보수)에 대한 이메일 알림을 수신할지 여부를 선택할 수 있습니다. 또는 종량과금제 또는 구독 계정이 있는 경우 계획되지 않은 이벤트, 유지보수 및 공지사항에 대한 {{site.data.keyword.Bluemix_notm}} 인프라 이메일 알림을 수신할지 여부를 선택할 수 있습니다. 자세한 정보는 [이메일 환경 설정](/docs/account?topic=account-email-prefs)을 참조하십시오.



