---

copyright:

  years: 2015, 2018

lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 내 티켓에 대한 빠른 응답은 어떻게 받습니까?
{: #quicktickresp}

지원 센터에 연락하고 지원 티켓을 열 때 문제점의 유형 및 긴급 정도에 따라 특정 심각도 레벨을 요청할 수 있습니다. 심각도 레벨은 사용자의 문제를 얼마나 신속하게 처리할 것인지 결정합니다.{:shortdesc}

문제의 심각도는 비즈니스 요구사항 및 지원 레벨에 따라 정의됩니다. 문제의 근본 원인을 식별하고 분석하기 위해 모든 티켓을 조사합니다. 문제점 진단 데이터가 문제의 근본 원인을 판별하는 데 필요한 경우 애플리케이션에서 로그 파일 및 기타 문제점 판별 데이터에 액세스하기 위한 승인을 요청받습니다. 이 데이터가 없으면 문제 해결이 지연될 수 있습니다.

진단 정보를 제공하도록 요청된 경우 다음 지시사항을 사용하여 가능한 빨리 요청된 정보를 수집하고 제공하십시오. 

## 진단 정보 수집
{: #collecting-diagnostic-information}

{{site.data.keyword.Bluemix_notm}} 애플리케이션 및 서비스에 대한 문제점을 진단하고 해결하기 위해 {{site.data.keyword.Bluemix_notm}} 지원 팀에서 진단 정보 수집을 요청할 수 있습니다.

진단 정보를 수집하기 전에 다음 단계를 수행하십시오.

1. 최신 cf 명령행 인터페이스를 설치했는지 확인하십시오. 자세한 정보는 [ cf 명령행 인터페이스 설치](/docs/starters/install_cli.html)를 참조하십시오.
>**참고:** 최신 cf 명령행 인터페이스가 설치되어 있지 않은 경우, cf 명령행이 {{site.data.keyword.Bluemix_notm}}에 연결된 후 `cf logs` 명령이 출력을 리턴하지 않을 수 있습니다.
2. `cf api` 명령을 사용하여 {{site.data.keyword.Bluemix_notm}}가 실행 중인 cf 명령행 인터페이스에 연결되었는지 확인하십시오.

다음 스크립트 중 하나를 사용하여 진단 정보를 수집하십시오.

  * Windows 운영 체제의 경우 [bmdiag-general.bat ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} 파일을 다운로드하고 이를 실행하십시오.
  * Linux 및 Mac 운영 체제의 경우 [bmdiag-general.sh ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} 파일을 다운로드하고 이를 실행하십시오.

스크립트는 cf 명령행 인터페이스를 사용하여 애플리케이션 환경에서 다음 정보를 추출합니다.
  * 애플리케이션 로그
  * 애플리케이션 메타데이터
  * 구성된 라우트
  * 이벤트
  * 프로비저닝된 서비스

## 지원 티켓을 에스컬레이션할 수 있습니까?
{: #escalation}

프리미엄 또는 표준 지원의 경우, 지원 티켓에 대해 시기 적절한 응답을 받지 못했거나 지원 티켓이 잘못 처리된다고 판단되면 지원 티켓을 에스컬레이션할 수 있습니다.   
{:shortdesc}

프리미엄 및 표준 지원에 대한 자세한 정보는 [지원 유형](/docs/get-support/getstarttssup.html#typesofsupport)을 참조하십시오. 

지원 티켓 에스컬레이션 프로세스를 통해 IBM 관리 담당자가 사용자의 문제를 검토하고 사용자와 함께 작업하여 지원 경험을 개선합니다.

에스컬레이션 요청을 제출하려면 다음 단계를 완료하십시오.
  1. 요약 **에스컬레이션 요청**으로 새 지원 티켓을 여십시오.
  2. 에스컬레이션 요청이 원래 지원 티켓과 일치하도록 다음 정보를 티켓 본문에 포함시키십시오.
      * 에스컬레이션이 필요한 열린 지원 티켓의 티켓 번호
      * 에스컬레이션이 필요한 이유에 대한 간단한 요약

## 운영 시간
{: #support-hours-operation}

심각도 1 문제는 일주일에 7일 하루 24시간 동안 모니터링됩니다. 모든 기타 심각도 레벨이 포함된 문제에 대한 양식 제출은 일요일 21:30 UTC에서 금요일 23:59 UTC까지 모니터링됩니다(휴일은 제외). 

이러한 지원 시간을 로컬 시간대로 변환하는 데 도움을 받으려면 [Timeanddate.com ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.timeanddate.com)을 참조하십시오.  휴일 스케줄에 대한 자세한 정보는 [{{site.data.keyword.Bluemix_notm}} 지원 휴일 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibm.biz/bluemixholidays)을 참조하십시오.
