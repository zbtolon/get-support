---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-10"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Schnelle Antworten auf einen Fall erhalten
{: #quicktickresp}

Wenn Sie sich mit dem Support in Verbindung setzen und einen Supportfall öffnen, können Sie eine bestimmte Prioritätsstufe auswählen, die sich nach dem Typ und der Dringlichkeit des Problems richtet. Die Prioritätsstufe kann sich darauf auswirken, wie schnell Ihr Problem bearbeitet wird.
{:shortdesc}

Sie definieren die Priorität des Problems auf der Basis Ihrer Geschäftsanforderungen und Ihrem Support-Level. Weitere Informationen zu den verschiedenen Typen von Supportplänen finden Sie unter [Supportpläne](/docs/get-support/index.html). Alle Fälle werden untersucht, um die eigentliche Ursache des Problems zu ermitteln und zu beheben. Wenn Problemdiagnosedaten zur Ermittlung der zugrunde liegenden Ursache des Problems erforderlich sind, werden Sie gebeten, dem Zugriff auf Protokolldateien und anderen Problembestimmungsdaten über Ihre Anwendung zuzustimmen. Ohne diese Daten könnte sich die Lösung Ihres Problems verzögern.

## Diagnoseinformationen erfassen
{: #collecting-diagnostic-information}

Beim Diagnostizieren und Beheben von Problemen mit {{site.data.keyword.Bluemix_notm}}-Anwendungen und -Services kann es vorkommen, dass Sie vom {{site.data.keyword.Bluemix_notm}}-Support-Team aufgefordert werden, Diagnoseinformationen zu erfassen. Gehen Sie anhand der folgenden Anweisungen vor, damit die angeforderten Informationen so schnell wie möglich erfasst und bereitgestellt werden.

Führen Sie die folgenden Schritte aus, bevor Sie Diagnoseinformationen erfassen:

1. Stellen Sie sicher, dass die neueste cf-Befehlszeilenschnittstelle installiert ist. Weitere Informationen finden Sie unter [Befehlszeilenschnittstelle 'cf' installieren](/docs/starters/install_cli.html).
>**Hinweis:** Wenn die neueste cf-Befehlszeilenschnittstelle nicht installiert ist, nachdem die cf-Befehlszeile mit {{site.data.keyword.Bluemix_notm}} verbunden ist, kann es vorkommen, dass bei Ausführung des Befehls `cf logs` keine Ausgabe zurückgegeben wird.
2. Stellen Sie sicher, dass die cf-Befehlszeilenschnittstelle mit dem System verbunden ist, auf dem {{site.data.keyword.Bluemix_notm}} ausgeführt wird; führen Sie hierzu den Befehl `cf api` aus.

Verwenden Sie eines der folgenden Scripts zum Erfassen der Diagnoseinformationen:

  * Windows-Betriebssysteme: Laden Sie die Datei [bmdiag-general.bat ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} herunter und führen Sie sie aus.
  * Linux- und Mac-Betriebssysteme: Laden Sie die Datei [bmdiag-general.sh ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} herunter und führen Sie sie aus.

Von den Scripts wird die cf-Befehlszeilenschnittstelle zum Extrahieren der folgenden Informationen aus der Anwendungsumgebung verwendet:
  * Anwendungsprotokolle
  * Anwendungsmetadaten
  * Konfigurierte Routen
  * Ereignisse
  * Bereitgestellte Services

## Supportfälle eskalieren
{: #escalation}

Als {{site.data.keyword.Bluemix_notm}}-Kunde können Sie weitergehende Unterstützung anfordern, indem Sie Ihren Fall an den zuständigen {{site.data.keyword.Bluemix_notm}}-Support Manager eskalieren. Während des Eskalationsprozesses können Sie kritische Probleme auf den Punkt bringen und Ihre Sorge äußern, wenn Sie den Eindruck haben, dass Ihr Supportfall nicht angemessen bearbeitet wird. Nach der Eskalation eines Falls prüft der zuständige Support Manager die Informationen im Supportfall, bindet die passenden Mitglieder des technischen {{site.data.keyword.Bluemix_notm}}-Supportteams ein und informiert Sie über Updates. 

Um einen Supportfall zu eskalieren, müssen Sie über {{site.data.keyword.Bluemix_notm}} Advanced oder Premium Support verfügen und einen Supportfall für das Problem geöffnet haben. Stellen Sie außerdem sicher, dass das technische Problem im geöffneten Supportfall ausreichend dokumentiert ist. 

 Führen Sie die folgenden Schritte aus, um einen Fall zu eskalieren: 

  1. Kontaktieren Sie das {{site.data.keyword.Bluemix_notm}}-Support-Team via Telefon oder Chat:
    * Via Telefon unter der folgenden Nummer: 866-403-7638. 
    * Via Chat über das {{site.data.keyword.Bluemix_notm}}-[Support Center ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} oder, falls Sie über ein nicht verknüpftes SoftLayer-Konto verfügen, über das [Kundenportal ![Symbol für externen Link](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}. 
  2. Geben Sie Ihre Fallnummer und Anforderung an, um den Fall zu eskalieren. 
  3. Geben Sie die Begründung für die Eskalation und den Einfluss Ihres Falls auf die Geschäftsabläufe an. 

{{site.data.keyword.Bluemix_notm}}-Support Managers sind rund um die Uhr im Einsatz. Sie binden die passenden Ressourcen für Ihren Fall ein und informieren Sie anschließend über die getroffenen Maßnahmen. 


## Betriebszeiten
{: #support-hours-operation}

Probleme mit der Priorität 1 werden 24 Stunden täglich und jeden Tag in der Woche überwacht. Einreichungen von Formularen für Probleme mit allen anderen Prioritäten werden von Sonntag ab 21:30 Uhr UTC bis Freitag um 23:59 Uhr UTC überwacht. 

Hilfe zur Umrechnung dieser Support-Stunden in Ihre örtliche Zeitzone finden Sie unter [Timeanddate.com ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.timeanddate.com).
