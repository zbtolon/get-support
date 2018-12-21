---

copyright:

  years: 2018

lastupdated: "2018-11-13"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# 고급 상태 검색
{: #adv-search}

상태 페이지의 모든 탭에서 검색할 수 있지만, 콘솔 외부에서 조회 매개변수를 사용하여 URL 검색 값을 빌드할 수 있는지 알고 있었습니까?
{:shortdesc}

다음 목록에는 URL 검색 옵션 예가 있습니다.

* 상태 탭이 선택된 페이지 로드: `console.cloud.ibm.com/status?selected=status`
* 계획된 유지보수 탭이 선택된 페이지 로드: `console.cloud.ibm.com/status?selected=maintenance`
* 보안 공지 탭이 선택된 페이지 로드: `console.cloud.ibm.com/status?selected=security`
* 공지사항 탭이 선택된 페이지 로드: `console.cloud.ibm.com/status?selected=announcement`
* 검색 조회가 입력된 페이지 로드: `console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* 필터가 선택된 페이지 도달. 예를 들어, 다음 URL 검색을 사용하여 지리적 위치를 북미로 설정할 수 있습니다. `console.cloud.ibm.com/status?selected=status&region=na`

* 고유 알림 ID를 검색 매개변수로 사용하여 알림에 대한 세부사항으로 직접 이동하십시오. 예를 들어, `query=INC1000001`은 ID가 `INC1000001`인 항목을 대상으로 지정합니다. 이 예에서 `INC1000001`은 유지보수 알림에 대한 케이스 번호입니다.

### URL 조회 필터:

| URL 조회 매개변수 |설명 | 값 |
| ----- | ----- | ----- | ----- |
| `?type` | 상태 탭에만 적용되는 필터. 인시던트 또는 유지보수를 기준으로 상태 탭을 필터링하려면 `?type` 조회를 사용하십시오. | `=incident`, `=maintenance` |
| `?region` | 지리적 위치를 기준으로 페이지를 필터링하십시오. | `=na`, `=eu`, `=sa`, `=ap` |
| `?component` | {{site.data.keyword.Bluemix_notm}} 컴포넌트를 기준으로 페이지를 필터링하십시오. 예를 들어, 관심 있는 서비스를 기준으로 필터링할 수 있습니다. | 대부분의 글로벌 카탈로그 ID에 적용됩니다. 예를 들어, `?component=iotf-service`는 페이지를 필터링하고 IoT(Internet of Things) 플랫폼에 영향을 주는 이벤트만 표시합니다. |
{: caption="표 1. URL 조회 필터" caption-side="top"}

항상 **필터링 기준** 필터를 사용한 다음 생성된 URL 조회를 복사하거나 책갈피로 표시할 수 있습니다. 필터는 URL에 표시되며 향후 조회를 빌드하는 데 도움이 될 수 있습니다.
{: tip}
