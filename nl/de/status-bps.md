---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-14"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Bewährte Verfahren für die Statusüberwachung
{: #best-practices}

Verwenden Sie die folgenden bewährten Verfahren für die Überwachung des Status von {{site.data.keyword.Bluemix}}, um informiert zu bleiben und entsprechend planen zu können.{: shortdesc}

## Prüfen, ob Wartungszeiten bevorstehen
{: #monbp-checmaintwin}

Prüfen Sie mindestens einmal alle 24 Stunden, ob Wartungszeiten bevorstehen, die auf der Dashboardseite der {{site.data.keyword.Bluemix_notm}}-Konsole veröffentlicht werden; verwenden Sie hierfür eine der folgenden Optionen:
* Überprüfen Sie das Widget 'Geplante Instandhaltung' im [Dashboard ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com){: new_window}. Klicken Sie auf **Alle Ereignisse**, um alle geplanten Wartungen anzuzeigen. 
* Navigieren Sie direkt zu der Seite [Status - Geplante Instandhaltung ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/status?selected=maintenance){: new_window}.

## Prüfen, ob derzeit Wartungszeiten existieren oder ob es einen Vorfall gibt
{: #monbp-checcurmaninprog}

Wenn Sie vermuten, dass {{site.data.keyword.Bluemix_notm}} nicht wie erwartet funktioniert, überprüfen Sie die Seite 'Status' auf aktuelle Wartungszeiten oder einen aktuellen Vorfall. Um einen Vorfall zu berichten, der noch nicht auf der Statusseite aufgelistet ist, öffnen Sie einen Supportfall, indem Sie in der Menüleiste auf **Support** klicken. Klicken Sie anschließend auf der Registerkarte 'Unterstützung anfordern' auf **Neuen Fall erstellen**. 

## Nutzen Sie die Vorteile mehrerer {{site.data.keyword.Bluemix_notm}}-Standorte
{: #monbp-multpreg}

Alle Benutzer von {{site.data.keyword.Bluemix_notm}} haben automatisch Zugriff auf die Standorte Dallas, London, Frankfurt, Sydney, Washington DC und Tokio. Das Team von {{site.data.keyword.Bluemix_notm}} Global Operations verwaltet alle Standorte, um negative Auswirkungen durch die Wartungen zu vermeiden und das Risiko von Störfällen, die alle Standorte gleichzeitig betreffen, zu minimieren. 

Um zwischen Standorten hin- und herzuwechseln rufen Sie Ihr Dashboard auf und heben die Komprimierung für das Menü **STANDORT** auf. 

## Auf kleinere Unterbrechungen vorbereitet sein
{: #monbp-prepmininter}

In den meisten Fällen kann {{site.data.keyword.Bluemix_notm}} normal weiterverwendet werden, auch während der Wartungszeit. Allerdings können kleinere Unterbrechungen eines Service nicht immer vermieden werden. Aktive Anwendungen bleiben standardmäßig verfügbar, auch wenn die Anwendungsmanagementfunktionen von {{site.data.keyword.Bluemix_notm}} wie das Starten und Stoppen von Apps vorübergehend unterbrochen sind. Um die Verfügbarkeit Ihrer aktiven Anwendungen zu maximieren, führen Sie mindestens drei Instanzen jeder Anwendung aus.

## E-Mail-Benachrichtigung abonnieren

Wenn Sie ein Lite-Kontoeigner sind, können Sie auswählen, ob Sie E-Mail-Benachrichtigungen über ungeplante Ereignisse auf der {{site.data.keyword.Bluemix_notm}}-Plattform wie beispielsweise Ausfälle und geplante Ereignisse wie beispielsweise Wartungen erhalten möchten. Wenn Sie über ein Konto mit nutzungsabhängiger Zahlung oder ein Abonnementkonto verfügen, können Sie außerdem auswählen, ob Sie E-Mail-Benachrichtigungen über ungeplante  Ereignisse, Wartungen und Ankündigungen für die {{site.data.keyword.Bluemix_notm}}-Infrastruktur erhalten möchten. Weitere Informationen finden Sie in [E-Mail-Vorgaben festlegen](/docs/account/email.html).



