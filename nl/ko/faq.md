---

copyright:

  years: 2019

lastupdated: "2019-07-25"

keywords: frequently asked question, faq, support cases, email preferences, access for cases, support faq 

subcollection: get-support 

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# FAQ
{: #get-supportfaq}

## 지원 케이스를 볼 수 없는 이유
{: #view-support-cases}
{: faq}

IBM Cloud에서는 이제 티켓을 케이스라고 부릅니다. 지원 케이스에 액세스하려면 **지원** > **케이스 관리**로 이동하십시오. 

케이스를 볼 수 없는 경우 **아카이브된 케이스 보기**를 클릭해 보십시오. 계속해서 케이스를 볼 수 없으면 필요한 권한이 없는 것일 수도 있습니다. 지원 케이스 액세스 그룹을 추가하려면 계정 소유자에게 문의하십시오. 자세한 정보는 [SoftLayer 계정 권한](https://test.cloud.ibm.com/docs/iam?topic=iam-migrated_permissions)을 참조하십시오.

## 계획된 유지보수는 어떻게 확인합니까?
{: #planned_maintenance_gs}
{: faq}

최소한 24시간마다 한 번씩 IBM Cloud 콘솔 대시보드 페이지를 사용하여 추후 유지보수를 확인할 수 있습니다. 다음 옵션 중 하나를 사용할 수 있습니다. 

1. [IBM Cloud 대시보드](https://cloud.ibm.com/)의 계획된 유지보수 위젯에서 **이벤트 보기**를 선택하십시오. 
2. [상태 - 계획된 유지보수 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/status?selected=maintenance){: new_window} 페이지로 바로 이동하십시오.

## 지원 케이스를 에스컬레이션하시겠습니까? 
{: #escalate_support}
{: faq}

IBM Cloud 고객은 중요한 문제를 표면화하기 위해 지원 케이스를 에스컬레이션할 수 있습니다. 케이스가 에스컬레이션되면 IBM Cloud 지원 팀에서 정보를 검토한 후 업데이트로 대응합니다. 

지원 케이스를 에스컬레이션하려면 다음 단계를 완료하십시오. 
1. 전화 또는 채팅으로 IBM Cloud 지원 팀에 문의하십시오.
    * +1-866-403-7638로 전화를 거십시오.
    * [지원 센터 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/unifiedsupport/supportcenter){: new_window}에서 채팅을 통해.
2. 기존 케이스 번호를 제공하고 케이스 에스컬레이션을 요청하십시오. 
3. 문제점에 대한 에스컬레이션 이유와 비즈니스 영향을 제공하십시오. 

## 알림에 대한 이메일 환경 설정을 어떻게 변경합니까? 
{: #email_preferences_gs}
{: faq}

수신하는 이메일 수가 너무 많은 경우, 프로파일 설정에서 계획된 이벤트, 계획되지 않은 이벤트 및 공지에 대해 수신할 이메일 알림을 변경할 수 있습니다. 이메일 환경 설정을 변경하려면 다음 옵션 중 하나를 선택하십시오. 

1. 프로파일 설정의 [알림](https://cloud.ibm.com/user/notifications)으로 이동하십시오.
1. 각 유형의 이벤트에 대해 이메일 알림 수신 여부를 선택하십시오.

`control.softlayer.com`의 경우, **계정** > **사용자** > **이메일 환경 설정**으로 이동하여 이메일 환경 설정을 변경할 수 있습니다. 

## 지원 케이스에 대해 작업해야 하는 액세스는 무엇입니까? 
{: #access_supportcases}
{: faq}

기본적으로 계정의 사용자에게 케이스를 작성하거나 업데이트하거나 검색하거나 보는 데 필요한 액세스가 없습니다. 계정 소유자는 Identity and Access Management(IAM) 액세스 정책을 지정하여 사용자 액세스를 제공해야 합니다. 

케이스를 작성할 때는 다른 사용자의 이메일을 **이 케이스에 다른 사람 추가** 필드에 추가하여 해당 사용자에게 해당 케이스에 대한 전체 액세스 권한을 부여할 수 있습니다. 추가된 사용자는 계정의 해당 케이스에 대해서만 보고, 편집하고 업데이트할 수 있는 액세스 권한을 갖습니다. 또한 이들은 해당 케이스가 업데이트된 경우 알림을 수신합니다. 

클래식 인프라 사용자의 경우, 지원 케이스 액세스 권한을 지정할 권한은 이제 [마이그레이션된 클래식 인프라 권한 액세스 그룹](/docs/iam?topic=iam-predefined)에서 사용할 수 있습니다.

## 지원 케이스를 열기 전에 수행할 수 있는 단계에는 무엇이 있습니까? 
{: #steps_before_opencase}
{: faq}

지원 케이스를 열기 전에 사용자의 질문 또는 문제가 이미 해결되었는지 알아보려면 다음 리소스를 탐색하십시오. 

1. [문서](https://cloud.ibm.com/docs)를 검토하십시오. 
2. [지원 센터 FAQ](https://cloud.ibm.com/unifiedsupport/supportcenter)를 확인하십시오. 
3. [FAQ 라이브러리](https://cloud.ibm.com/docs/faqs)로 이동하십시오. 
4. [Stack Overflow ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://stackoverflow.com/questions/tagged/ibm-bluemix){: new_window}로 이동하여 {{site.data.keyword.Bluemix_notm}} 플랫폼과 서비스를 사용한 앱 개발에 대해 기술적인 질문을 하십시오.
5. [IBM Developer Answers ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/answers/smart-spaces/12/bluemix.html){: new_window}로 이동하여 {{site.data.keyword.Bluemix_notm}} 오퍼링 및 시작하기 지시사항에 대한 일반적인 질문을 할 수 있습니다.
