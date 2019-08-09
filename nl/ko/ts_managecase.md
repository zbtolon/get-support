---

copyright:

  years: 2015, 2019

lastupdated: "2019-07-25"

keywords: help managing cases, resolve issues managing cases, trouble working with cases

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


# 지원 케이스 관리에 대한 문제점 해결
{: #Supportcases}

{{site.data.keyword.Bluemix}} 지원 케이스 작성 및 관리에 대한 문제점이 발생할 수 있습니다. 대부분 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.
{:shortdesc}

## 지원 케이스를 작성하거나 편집할 수 없는 이유 
{: #ts_service_broker}

{{site.data.keyword.Bluemix_notm}} 지원 케이스를 작성하거나 편집할 수 없으며, 적절한 액세스 권한이 없다는 오류 메시지가 표시됩니다. 
{:shortdesc}

케이스를 작성하려고 할 때 다음 오류 메시지가 표시됩니다.   
{: tsSymptoms}

`Looks like you don't have access to create cases for this account.`

지원 케이스 액세스 및 관리에 대한 일반 문제점은 지원 센터 계정 관리 서비스의 Identity and Access Management(IAM) 액세스 정책이
없기 때문일 수 있습니다. 케이스를 작성하려면 지원 센터 계정 관리 서비스에 대한 편집자 또는 관리자 역할을 지정받아야 합니다. 
{: tsCauses}

문제를 해결하려면 계정 관리자, 지원 센터 서비스의 관리자 또는 모든 계정 관리 서비스의 관리자가 지원 센터에서 IAM 정책을 지정하여 케이스를 관리할 수 있습니다. 
{: tsResolve}

계정 소유자 또는 지원 센터의 관리자인 경우 다음 단계를 완료하여 지원 케이스 작업에 대한 액세스 정책을 작성하십시오.

1. **관리** &gt; **액세스(IAM)**로 이동하고 **사용자**를 선택하십시오.
2. 사용자 이름을 선택하고 **액세스 정책**을 클릭하십시오. 
3. **액세스 지정**을 클릭하십시오. 
4. **계정 관리 서비스에 대한 액세스 지정**을 선택하십시오. 
5. **서비스** 메뉴에서 **지원 센터**를 선택하십시오. 
6. 사용자의 엑세스 레벨을 정의하려면 역할을 선택하십시오. 


## 계정의 모든 케이스를 볼 수 없는 이유
{: #ts_viewcasedetails}

계정의 모든 사용자를 볼 수 있는 액세스 권한이 없으므로 계정의 모든 케이스를 볼 수 없습니다. 
{:shortdesc}

계정과 연관된 지원 케이스를 보려는 경우 모든 오픈 케이스를 볼 수는 없습니다. 
{: tsSymptoms}

계정 소유자가 [사용자 목록 가시성 설정](/docs/iam?topic=iam-userlistview#userlistview)을 제한됨으로 설정했습니다. 설정이 제한됨으로 설정되어 있고 계정의 사용자를 보기 위한 추가 액세스 정책이 없는 경우 계정의 모든 케이스를 보는 데 필요한 액세스 권한이 없습니다. 계정으로 초대한 사용자, Cloud Foundry 조직 멤버십을 공유할 사용자 또는 클래식 인프라 사용자 계층에 있는 사용자만 볼 수 있습니다. 
{: tsCauses}

지원 센터 계정 관리 서비스 액세스 정책 외에 사용자 관리 계정 관리 서비스에 대한 뷰어 이상의 역할을 포함한 IAM 정책이 지정되어야 합니다. 현재 액세스를 보려면 **관리** &gt; **액세스(IAM)**로 이동하고 **사용자** 페이지에서 이름을 선택하십시오. **액세스 정책** 탭을 클릭하고 지정된 정책을 검토하십시오. 
{: tsResolve}

문제를 해결하려면 계정 소유자에게 문의하여 적절한 액세스를 요청하십시오. 

## 이전에 작성한 케이스를 찾을 수 없는 이유는 무엇입니까? 
{: #ts_viewarchivedcase}

{{site.data.keyword.Bluemix_notm}} 플랫폼 경험이 개선되기 전에 작성한 케이스는 찾을 수 없습니다. 
{:shortdesc}

지원 센터의 **케이스 관리** 탭으로 이동한 후 2018년 12월 2일 전에 작성한 케이스를 찾을 수 없습니다.
{: tsSymptoms}

2018년 12월 2일 전에 열린 케이스는 **아카이브된 케이스 보기**에서만 볼 수 있습니다. 
{: tsCauses}

케이스를 보려면 **지원**으로 이동하여 **케이스 관리**를 선택한 후 **아카이브된 케이스 보기**를 클릭하십시오.
{: tsResolve} 






