---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-02"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 내 티켓에 대한 빠른 응답은 어떻게 받습니까?
{: #quicktickresp}

지원 센터에 문의하고 지원 티켓을 열 때 문제점의 유형 및 긴급 정도에 따라 특정 심각도 레벨을 요청할 수 있습니다. 심각도 레벨은 사용자의 문제를 얼마나 신속하게 처리할 것인지 결정합니다.
{:shortdesc}

문제의 심각도는 비즈니스 요구사항 및 지원 레벨에 따라 정의됩니다. 지원 플랜 레벨에 대한 자세한 정보는 [지원 플랜](/docs/get-support/index.html)을 참조하십시오. 문제의 근본 원인을 식별하고 분석하기 위해 모든 티켓을 조사합니다. 지원 팀에서 문제의 근본 원인을 판별하기 위해 문제점 진단 데이터를 필요로 하는 경우에는 사용자 애플리케이션의 로그 파일 및 기타 문제점 판별 데이터에 액세스하는 데 필요한 승인이 사용자에게 요청됩니다. 이 데이터가 없으면 문제 해결이 지연될 수 있습니다.

## 진단 정보 수집
{: #collecting-diagnostic-information}

{{site.data.keyword.Bluemix_notm}} 애플리케이션 및 서비스에 대한 문제점을 진단하고 해결하기 위해 {{site.data.keyword.Bluemix_notm}} 지원 팀에서 진단 정보를 요청할 수 있습니다. 다음 지시사항을 사용하여 가능한 빨리 요청된 정보를 수집하고 제공하십시오.

진단 정보를 수집하기 전에 다음 단계를 수행하십시오.

1. 최신 Cloud Foundry 명령행 인터페이스 버전이 설치되어 있는지 확인하십시오. 자세한 정보는 [Cloud Foundry 명령행 인터페이스 설치](/docs/starters/install_cli.html)를 참조하십시오.
>**참고:** 최신 버전이 없는 경우에는 Cloud Foundry 명령행이 {{site.data.keyword.Bluemix_notm}}에 연결된 후 `cf logs` 명령이 출력을 리턴하지 않을 수 있습니다.
2. `cf api` 명령을 사용하여 Cloud Foundry 명령행 인터페이스를 {{site.data.keyword.Bluemix_notm}}가 실행 중인 위치에 연결했는지 확인하십시오.

다음 스크립트 중 하나를 사용하여 진단 정보를 수집하십시오.

  * Windows 운영 체제의 경우 [bmdiag-general.bat ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} 파일을 다운로드하고 이를 실행하십시오.
  * Linux 및 Mac 운영 체제의 경우 [bmdiag-general.sh ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} 파일을 다운로드하고 이를 실행하십시오.

스크립트는 Cloud Foundry 명령행 인터페이스를 사용하여 애플리케이션 환경에서 다음 정보를 추출합니다.
  * 애플리케이션 로그
  * 애플리케이션 메타데이터
  * 구성된 라우트
  * 이벤트
  * 프로비저닝된 서비스

## 지원 케이스 에스컬레이션
{: #escalation}

중요한 문제를 표면화하려는 경우나 지원 케이스가 적절하게 처리되고 있지 않다고 생각하는 경우에는 에스컬레이션 프로세스를 사용하십시오. 케이스가 에스컬레이션되면 근무 중인 관리자가 지원 케이스의 정보를 검토한 후 {{site.data.keyword.Bluemix_notm}} 기술 지원 팀의 구성원을 배정하고 적절한 업데이트 내용을 고객에게 제공합니다.

근무 중인 {site.data.keyword.Bluemix_notm}} 지원 관리자에게 케이스를 에스컬레이션하여 추가 지원을 요청할 수 있습니다. 

지원 케이스를 에스컬레이션하려면 문제에 대해 열린 지원 케이스가 있어야 합니다. 또한 연 지원 케이스에 기술 문제에 대한 자세한 설명을 제공했는지 확인하십시오.

 케이스를 에스컬레이션하려면 다음 단계를 완료하십시오.

  1. 전화 또는 채팅으로 {{site.data.keyword.Bluemix_notm}} 지원 팀에 문의하십시오.
    * 866-403-7638으로 전화를 거십시오.
    * {{site.data.keyword.Bluemix_notm}} [지원 센터 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} 또는 연결되지 않은 SoftLayer 계정이 있는 경우 [고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}에서 채팅으로 문의하십시오.
  2. 기존 케이스 번호를 제공하고 케이스 에스컬레이션을 요청하십시오.
  3. 케이스에 대한 에스컬레이션 사유와 비즈니스 영향을 설명하십시오.

{{site.data.keyword.Bluemix_notm}} 지원 관리자는 연중무휴 24시간 근무합니다. 근무 중인 관리자는 케이스를 해결할 적임자를 지정한 후 고객에게 수행한 조치를 알려줍니다.
