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


# Schnelle Antworten auf ein Ticket erhalten
{: #quicktickresp}

Wenn Sie sich mit dem Support in Verbindung setzen und ein Support-Ticket öffnen, können Sie eine bestimmte Prioritätsstufe auswählen, die sich nach dem Typ und der Dringlichkeit des Problems richtet. Die Prioritätsstufe kann sich darauf auswirken, wie schnell Ihr Problem bearbeitet wird.
{:shortdesc}

Sie definieren die Priorität des Problems auf der Basis Ihrer Geschäftsanforderungen und Ihrer Supportstufe. Alle Tickets werden untersucht, um die eigentliche Ursache des Problems zu ermitteln und zu beheben. Wenn Problemdiagnosedaten zur Ermittlung der zugrunde liegenden Ursache des Problems erforderlich sind, werden Sie gebeten, dem Zugriff auf Protokolldateien und anderen Problembestimmungsdaten über Ihre Anwendung zuzustimmen. Ohne diese Daten könnte sich die Lösung Ihres Problems verzögern.

Wenn Sie zur Übermittlung von Diagnoseinformationenen aufgefordert werden, gehen Sie anhand der folgenden Anweisungen vor, damit die angeforderten Informationen so schnell wie möglich erfasst und bereitgestellt werden.

## Diagnoseinformationen erfassen
{: #collecting-diagnostic-information}

Beim Diagnostizieren und Beheben von Problemen mit {{site.data.keyword.Bluemix_notm}}-Anwendungen und -Services kann es vorkommen, dass Sie vom {{site.data.keyword.Bluemix_notm}}-Support-Team aufgefordert werden, Diagnoseinformationen zu erfassen.

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

## Kann ich ein Support-Ticket eskalieren?
{: #escalation}

Wenn Sie auf ein Support-Ticket der Prioritätsstufe 'Premium' oder 'Standard' keine zeitgerechte Reaktion erhalten oder wenn Sie den Eindruck haben, dass Ihr Support-Ticket nicht angemessen bearbeitet wird, können Sie das Support-Ticket eskalieren.  
{:shortdesc}

Weitere Informationen zu den Supporttypen 'Premium' und 'Standard' finden Sie unter [Supporttypen](/docs/get-support/getstarttssup.html#typesofsupport).

Durch den Eskalationsprozess für das Support-Ticket prüft das IBM Management Ihre Problematik erneut und arbeitet mit Ihnen zusammen, um die Supporterfahrung zu verbessern.

Führen Sie die folgenden Schritte aus, um einen Eskalationsprozess anzufordern:
  1. Öffnen Sie ein neues Support-Ticket mit dem Stichwort **Escalation Request** (Eskalationsanforderung).
  2. Geben Sie die folgenden Informationen im Hauptteil des Tickets an, um sicherzustellen, dass Ihre Eskalationsanforderung mit dem ursprünglichen Support-Ticket abgeglichen werden kann:
      * Die Ticketnummer Ihres geöffneten Support-Tickets, das eine Eskalation erfordert.
      * Eine kurze Zusammenfassung der Gründe, aus denen die Eskalation erforderlich ist.

## Betriebszeiten
{: #support-hours-operation}

Probleme mit der Priorität 1 werden 24 Stunden täglich und 7 Tage die Woche überwacht. Einreichungen von Formularen für Probleme mit allen anderen Prioritäten werden von Sonntag ab 21:30 Uhr UTC bis Freitag um 23:59 Uhr UTC überwacht (Feiertage ausgenommen).

Hilfe zur Umrechnung dieser Support-Stunden in Ihre örtliche Zeitzone finden Sie unter [Timeanddate.com ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.timeanddate.com). Weitere Informationen zum Feiertagsplan finden Sie unter [{{site.data.keyword.Bluemix_notm}} Support Holidays ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://ibm.biz/bluemixholidays).
