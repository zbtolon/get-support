---

copyright:

  years: 2018,2019

lastupdated: "2019-05-13"

keywords: status page, status query

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# Erweiterte Statussuche
{: #adv-search}

Sie können alle Registerkarten auf der Seite "Status" durchsuchen, aber wussten Sie, dass Sie URL-Suchwerte mithilfe von Abfrageparametern außerhalb der Konsole erstellen können?
{:shortdesc}

Die folgende Liste enthält Beispiele für URL-Suchoptionen:

* Laden Sie die Seite mit der ausgewählten Registerkarte 'Status': `console.cloud.ibm.com/status?selected=status`
* Laden Sie die Seite mit der ausgewählten Registerkarte 'Wartung': `console.cloud.ibm.com/status?selected=maintenance`
* Laden Sie die Seite mit der ausgewählten Registerkarte 'Sicherheitsbulletin': `console.cloud.ibm.com/status?selected=security`
* Laden Sie die Seite mit der ausgewählten Registerkarte 'Ankündigungen': `console.cloud.ibm.com/status?selected=announcement`
* Laden Sie die Seite mit einer eingegebenen Suchabfrage: `console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* Blättern Sie zu der Seite mit ausgewählten Filtern. Sie können zum Beispiel den Standort Nordamerika mithilfe der folgenden URL-Suche festlegen: `console.cloud.ibm.com/status?selected=status&region=na`

* Verwenden Sie eindeutige Benachrichtigungskennungen wie Suchparameter, um direkt zu den Details für die Benachrichtigung zu gelangen.  Beispiel: `query=INC1000001` hat Elemente mit der folgenden ID zum Ziel: `INC1000001`. In diesem Beispiel ist `INC1000001` die Fallnummer für eine Benachrichtigung über Wartung.

### URL-Abfragefilter:
{: #url-query}

| URL-Abfrageparameter | Beschreibung | Werte |
| ----- | ----- | ----- | ----- |
| `?type` | Ein Filter, der nur für die Registerkarte 'Status' gilt. Verwenden Sie die Abfrage `?type`, um die Registerkarte 'Status' nach Vorfällen oder Wartung zu filtern. | `=incident`, `=maintenance` |
| `?region` | Filtert die Seite nach Standorten.  | `=na`, `=eu`, `=sa`, `=ap` |
| `?component` | Filtert die Seite nach {{site.data.keyword.Bluemix_notm}}-Komponenten. Sie können zum Beispiel nach einem Service filtern, der für Sie von Interesse ist. | Gilt für die meisten globalen Katalog-IDs. So filtert zum Beispiel `?component=iotf-service` die Seite und zeigt Ereignisse an, die das Internet der Dinge betreffen.  |
{: caption="Tabelle 1. URL-Abfragefilter" caption-side="top"}

Sie können jederzeit die Filter **Filtern nach** verwenden und die generierte URL-Abfrage kopieren oder mit einen Lesezeichen versehen. Die Filter werden in Ihrer URL angezeigt und können Ihnen bei der Erstellung zukünftiger Abfragen helfen.
{: tip}
