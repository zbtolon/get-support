---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-04"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Systemstatus und Benachrichtigungen anzeigen
{: #viewing-bluemix-status}

Die Seite 'Status' ist die zentrale Position für die Suche nach Benachrichtigungen und Ankündigungen in Bezug auf bedeutende Ereignisse, die die {{site.data.keyword.Bluemix_notm}}-Plattform und die übergeordneten Services betreffen.
{:shortdesc}

Auf der Seite 'Status' sind die folgenden Informationen zu finden:

  * Der aktuelle Status von Services und Komponenten in allen {{site.data.keyword.Bluemix_notm}} Foundry-Serviceregionen.
  * Eine Liste mit Ankündigungen in chronologischer Reihenfolge zu Wartungszwecken und zur Behebung von Vorfällen. Für weitere Details können Sie die Liste filtern oder eine einzelne Ankündigung öffnen.
  * Geplante Wartungszeiten, die im Voraus angekündigt werden, außer in extremen Situationen.
  * Ungeplante Vorfälle oder Ausfallzeiten, die mitgeteilt werden, sobald das {{site.data.keyword.Bluemix_notm}}-Team diese bemerkt. Benachrichtigungen zu Vorfällen werden regelmäßig aktualisiert, bis die Probleme behoben sind.
  * Referenzen auf Sicherheitsbulletins, die die verschiedenen {{site.data.keyword.Bluemix_notm}}-Services oder die Plattform betreffen.
  * Weitere plattformweite Ankündigungen allgemeiner Art, die Sie interessieren könnten.
  * [Ein RSS-Feed, den Sie abonnieren können](#subscribing-rss-feed).

Die Seite 'Status' wird angezeigt, wenn Sie eine der beiden folgenden Optionen auswählen:

  * Melden Sie sich bei der {{site.data.keyword.Bluemix_notm}}-Konsole an. Klicken Sie in der Menüleiste auf **Support** und wählen Sie **Status** aus. Prüfen Sie die aufgelisteten Ressourcen auf das Symbol ![Probleme](images/some_issues.svg). Dieses Symbol könnte auf einen Ausfall hinweisen.
  * Greifen Sie direkt über [{{site.data.keyword.Bluemix_notm}} - Status ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/status){: new_window} darauf zu.


## Bewährte Verfahren für die Statusüberwachung
{: #best-practices}

Verwenden Sie die folgenden bewährten Verfahren für die Überwachung des Status von {{site.data.keyword.Bluemix_notm}}, um informiert zu bleiben und entsprechend planen zu können.

### Prüfen, ob Wartungszeiten bevorstehen
{: #monbp-checmaintwin}

Prüfen Sie mindestens einmal alle 24 Stunden, ob Wartungszeiten bevorstehen, die auf der Statusseite veröffentlicht werden; verwenden Sie hierfür eine der folgenden Optionen:
* Direktes Navigieren zur Seite [Status ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/status){: new_window}
* Verwenden des RSS-Feeds oder eines Weiterleitungsservers, der RSS-Feeds an eine E-Mail-Adresse weiterleitet

### Prüfen, ob derzeit Wartungszeiten existieren oder ob es einen Vorfall gibt
{: #monbp-checcurmaninprog}

Wenn Sie vermuten, dass {{site.data.keyword.Bluemix_notm}} nicht wie erwartet funktioniert, überprüfen Sie die Seite 'Status' auf aktuelle Wartungszeiten oder einen aktuellen Vorfall. Wenn Sie einen Vorfall melden möchten, der noch nicht auf der Seite 'Status' aufgeführt ist, öffnen Sie ein Support-Ticket, indem Sie auf **Support** klicken und die Option **Ticket hinzufügen** in der Menüleiste auswählen. Alternativ können Sie auch auf die Hilfeseite [{{site.data.keyword.Bluemix_notm}}-Support ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://www.ibm.biz/bluemixsupport){: new_window} zugreifen.

### Nutzen der Vorteile mehrerer {{site.data.keyword.Bluemix_notm}} Foundry-Serviceregionen
{: #monbp-multpreg}

Alle Benutzer von {{site.data.keyword.Bluemix_notm}} Public verfügen automatisch über Zugriff auf die Regionen 'Vereinigte Staate (Süden)', 'Vereinigtes Königreich', 'Deutschland', 'Sydney', 'Vereinigte Staaten (Osten)' und 'Asien-Pazifik (Norden)'. Das {{site.data.keyword.Bluemix_notm}} Global Operations-Team verwaltet alle Regionen, um Auswirkungen von Instandhaltungsmaßnahmen zu verhindern und um das Risiko von Zwischenfällen zu minimieren, die sich auf alle Regionen gleichzeitig auswirken.

Zum Wechseln der Regionen erweitern Sie in der {{site.data.keyword.Bluemix_notm}}-Menüleiste das Regionsmenü und wählen Sie dann eine andere Region aus.

### Auf kleinere Unterbrechungen vorbereitet sein
{: #monbp-prepmininter}

In den meisten Fällen kann {{site.data.keyword.Bluemix_notm}} normal weiterverwendet werden, auch während der Wartungszeit. Allerdings können kleinere Unterbrechungen eines Service nicht immer vermieden werden. Aktive Anwendungen bleiben standardmäßig verfügbar, auch wenn die Anwendungsmanagementfunktionen von {{site.data.keyword.Bluemix_notm}} wie das Starten und Stoppen von Apps vorübergehend unterbrochen sind. Um die Verfügbarkeit Ihrer aktiven Anwendungen zu maximieren, führen Sie mindestens drei Instanzen jeder Anwendung aus.

## RSS-Feed abonnieren
{: #subscribing-rss-feed}

Durch ein Abonnement des RSS-Feeds für die {{site.data.keyword.Bluemix_notm}}-Seite 'Status' können Sie Alerts über Benachrichtigungen empfangen. Auf diese Weise haben Sie die Möglichkeit, Updates ohne regelmäßiges Besuchen der Seite 'Status' zu erhalten.

Führen Sie die folgenden Schritte durch, um einen RSS-Feed zu abonnieren:

1. Laden Sie einen RSS-Reader herunter und installieren Sie ihn.
2. Verwenden Sie Ihren Reader, um den Feed über eine der folgenden Methoden zu abonnieren:
    * Ziehen Sie das RSS-Symbol ![RSS](images/rss.svg) in den RSS-Reader.
    * Klicken Sie mit der rechten Maustaste auf das RSS-Symbol, wählen Sie die Option zum Kopieren der Linkadresse aus und fügen Sie die URL in Ihren RSS-Reader ein.

Weitere Informationen finden Sie in der **Hilfe** Ihres Readers. 	   

Weitere Methoden zum Lesen von RSS-Feeds stehen über Web-Browser-Plug-ins zur Verfügung:
  * [RSS Feed ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://feeder.co/){: new_window} Reader für Chrome
  * [Add-on Brief ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} für Firefox

Neue Quellen wie die folgenden bieten ebenfalls Möglichkeiten zum Lesen von RSS-Feeds:
  * [Feedly ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://www.feedly.com/){: new_window}
  * [G2reader ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://www.g2reader.com/en/){: new_window}

Sie können auch einen Drittanbieterservice nutzen, damit automatisch eine E-Mail für die einzelnen RSS-Updates gesendet wird. In der folgenden Liste sind einige Beispiele für Drittanbieterservices aufgeführt:

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com

Für {{site.data.keyword.Bluemix_notm}} gibt es standardmäßig ungefähr 50 Updates pro Monat.


## Benachrichtigungen zu Vorfällen und Wartungsmaßnahmen einrichten
{: #setting-up-notifications}

Bei {{site.data.keyword.Bluemix_notm}} Public können Sie sich für Plattformbenachrichtigungen anmelden. Dabei handelt es sich um optionale E-Mail-Alerts bei Vorfall- und Wartungsereignissen für die Plattform. Klicken Sie auf **Verwalten** > **Konto** > **Benachrichtigungen** und wählen Sie die Registerkarte **Plattform** aus, um Benachrichtigungen einzurichten. 
