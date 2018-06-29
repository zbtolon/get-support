---

copyright:

  years: 2015, 2018

lastupdated: "2018-06-14"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Schnelle Antworten auf ein Ticket erhalten
{: #quicktickresp}

Wenn Sie sich mit dem Support in Verbindung setzen und ein Support-Ticket öffnen, können Sie eine bestimmte Prioritätsstufe auswählen, die sich nach dem Typ und der Dringlichkeit des Problems richtet. Die Prioritätsstufe kann sich darauf auswirken, wie schnell Ihr Problem bearbeitet wird.
{:shortdesc}

Sie definieren die Priorität des Problems auf der Basis Ihrer Geschäftsanforderungen und Ihrem Support-Level. Weitere Informationen zu den verschiedenen Typen von Supportplänen finden Sie in [Supportpläne](/docs/get-support/index.html). Alle Tickets werden untersucht, um die eigentliche Ursache des Problems zu ermitteln und zu beheben. Wenn das Support-Team zur Ermittlung der zugrunde liegenden Ursache des Problems Problemdiagnosedaten benötigt, werden Sie gebeten, dem Zugriff auf Protokolldateien und anderen Problembestimmungsdaten über Ihre Anwendung zuzustimmen. Ohne diese Daten könnte sich die Lösung Ihres Problems verzögern.

## Diagnoseinformationen erfassen
{: #collecting-diagnostic-information}

Beim Diagnostizieren und Beheben von Problemen mit {{site.data.keyword.Bluemix_notm}}-Anwendungen und -Services kann es vorkommen, dass Sie vom {{site.data.keyword.Bluemix_notm}}-Support-Team aufgefordert werden, Diagnoseinformationen bereitzustellen. Gehen Sie anhand der folgenden Anweisungen vor, damit die angeforderten Informationen so schnell wie möglich erfasst und bereitgestellt werden.

Führen Sie die folgenden Schritte aus, bevor Sie Diagnoseinformationen erfassen:

1. Stellen Sie sicher, dass die jeweils aktuelle Version der Befehlszeilenschnittstelle von Cloud Foundry installiert ist. Weitere Informationen enthält [Cloud Foundry-CLI installieren](/docs/starters/install_cli.html).
>**Hinweis:** Falls Sie nicht über die neueste Version verfügen, kann es vorkommen, dass bei Ausführung des Befehls `cf logs` keine Ausgabe zurückgegeben wird, nachdem die Cloud Foundry-Befehlszeilenschnittstelle eine Verbindung zu {{site.data.keyword.Bluemix_notm}} hergestellt hat.
2. Stellen Sie durch Ausführen des Befehls `cf api` sicher, dass die Cloud Foundry-Befehlszeilenschnittstelle mit dem Ausführungsort von {{site.data.keyword.Bluemix_notm}} verbunden ist.

Verwenden Sie eines der folgenden Scripts zum Erfassen der Diagnoseinformationen:

  * Windows-Betriebssysteme: Laden Sie die Datei [bmdiag-general.bat ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} herunter und führen Sie sie aus.
  * Linux- und Mac-Betriebssysteme: Laden Sie die Datei [bmdiag-general.sh ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} herunter und führen Sie sie aus.

Von den Scripts wird die Cloud Foundry-Befehlszeilenschnittstelle zum Extrahieren der folgenden Informationen aus der Anwendungsumgebung verwendet:
  * Anwendungsprotokolle
  * Anwendungsmetadaten
  * Konfigurierte Routen
  * Ereignisse
  * Bereitgestellte Services

## Supportfälle eskalieren
{: #escalation}

Sie können weitergehende Unterstützung anfordern, indem Sie Ihren Fall an den zuständigen {{site.data.keyword.Bluemix_notm}}-Support Manager eskalieren, wenn Sie eines der folgenden Kriterien erfüllen: 
  * Sie sind ein {{site.data.keyword.Bluemix_notm}}-Kunde mit Advanced oder Premium Support.
  * Sie sind ein SoftLayer-Kunde mit einer SoftLayer-Standard-Supportvereinbarung.

Verwenden Sie den Eskalationsprozess, um kritische Probleme auf den Punkt zu bringen oder wenn Sie den Eindruck haben, dass Ihr Support-Ticket nicht angemessen gehandhabt wird. Bei Eskalation eines Falls prüft der zuständige Support Manager die Informationen im Support-Ticket, bindet die passenden Mitglieder des technischen {{site.data.keyword.Bluemix_notm}}-Supportteams ein und informiert Sie über entsprechende Updates.

Um einen Supportfall eskalieren zu können, müssen Sie über ein offenes Support-Ticket für das Problem verfügen. Stellen Sie außerdem sicher, dass Sie eine detaillierte Beschreibung des technischen Problems in das von Ihnen geöffnete Support-Ticket eingebunden haben.

 Führen Sie die folgenden Schritte aus, um einen Fall zu eskalieren:

  1. Kontaktieren Sie das {{site.data.keyword.Bluemix_notm}}-Support-Team telefonisch oder über den Chat:
    * Telefonische Kontaktaufnahme unter der folgenden Nummer: 866-403-7638.
    * Kontaktaufnahme via Chat über das {{site.data.keyword.Bluemix_notm}}-[Support Center ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} oder, falls Sie über ein SoftLayer-Konto verfügen, das nicht verknüpft ist, über das [Kundenportal ![Symbol für externen Link](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}.
  2. Geben Sie Ihre vorhandene Ticketnummer und Anforderung an, um den Fall zu eskalieren.
  3. Geben Sie die Begründung für die Eskalation und den Einfluss Ihres Falls auf die Geschäftsabläufe an.

{{site.data.keyword.Bluemix_notm}}-Support Managers sind rund um die Uhr im Einsatz. Sie binden die passenden Ressourcen für Ihren Fall ein und informieren Sie anschließend über die getroffenen Maßnahmen.
