---

copyright:

  years: 1994, 2019

lastupdated: "2019-05-16"

keywords: data centers, data center support, dal01 pod, wdc01 pod 

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Zurückziehung der Unterstützung für einige US-Rechenzentren
{: #dc-migrate}

IBM bietet keine weitere Unterstützung für folgende Rechenzentren in den Vereinigte Staaten: 

* dal01 Pods 2 und 3
* wdc01 Pods 1 und 2
{:shortdesc}

##  Warum muss ich zu einem anderen Rechenzentrum wechseln?
{: #required-data}

Um Ihnen weiterhin den besten Service, die beste Hardware und die beste Konnektivität zu bieten, werden alle Standorte kontinuierlich evaluiert, um sicherzustellen, dass sie die Standards bezüglich Netzbetrieb und Elektrik sowie andere Infrastrukturstandards erfüllen. Auch wenn diese Standorte angemessene Bewertungen aufweisen, erfüllen Sie nicht mehr die sich weiterentwickelnden Standards.

## Muss die Migration bis zum angegebenen Datum vollständig abgeschlossen sein?
{: #data-list}

Ja. Um sicherzustellen, dass keine Betriebsunterbrechung notwendig wird, versuchen wir, so viel Vorlaufzeit wie möglich zu ermöglichen, um den Übergang für Sie einfach zu gestalten. Wir haben diese Standortverschiebung bereits im Mai 2018 angekündigt.

## Muss ich mit einem erneuten Wechsel zu einem anderen Rechenzentrum rechnen?
{: #move-data}

Wir evaluieren ständig die Qualität unserer Standorte, um Ihnen den besten und verlässlichsten Service zu bieten. Es kann zu weiteren Standortwechseln kommen, da wir damit fortfahren, einige unserer alten Standorte zu evaluieren.

## Kann ich ein beliebiges {{site.data.keyword.Bluemix_notm}}-Rechenzentrum in den USA auswählen?
{: #us-data}

Ja, sie können ein beliebiges Rechenzentrum in den USA auswählen, dass Ihren Anforderungen vor Ort genügt.

## Wie wähle ich das Rechenzentrum aus, in dem die Bereitstellung erfolgen soll?
{: #deploy-data}

IBM verfügt weltweit über mehr als 60 Rechenzentren an verschiedenen Standorten. Sehen Sie sich die Karte auf unserer Seite mit den globalen Rechenzentren an, um zu sehen, in welchen Rechenzentren eine Bereitstellung möglich ist. 

Die folgenden Faktoren können beeinflussen, welches Rechenzentrum Sie auswählen:
* Nähe zu den Benutzern der Systeme
* Nähe zu allen anderen Systemen, mit denen dieser Server kommunizieren muss
* Alle Datenrichtlinien oder Regelungen, die es erforderlich machen, Daten an einem bestimmten Standort zu speichern

## Muss ich auch US-Sites für den Übergangszeitraum verwenden?
{: #transition}

Während der 60 Tage dauernden Übergangszeit können Sie einen beliebigen {{site.data.keyword.cloud_notm}}-Standort weltweit verwenden.

## Sind diese beiden freien Monate der Übergangszeit Ressourcen, die zusätzlich zu meiner vorhandenen Serverzeit gelten?
{: #free}

Ja. Sie können sich mit einem entsprechenden Supportmitarbeiter in Verbindung setzen, der Ihnen dabei hilft, Ihre Server für die Übergangszeit anzufordern. 

## Wie bestimme ich meine aktuelle Hardwarekonfiguration?
{: #current-hardware}

Melden Sie sich beim Kundenportal an. Wählen Sie in der **Einheitenliste** den gewünschten Server aus und suchen Sie die Details der Systemkonfiguration. Von dort aus können Sie den Prozessortyp anzeigen, z. B. Single Intel Xeon E3-1270 (4 Cores, 3,50 GHz). Sie können auch die Speicherkapazität (RAM), weiteren Speicherplatz und andere Daten anzeigen.

## Wie stelle ich die Auslastung meiner aktuellen Hardware fest?
{: #utilization} 

Die meisten Betriebssysteme stellen Tools bereit, die Sie verwenden können, um die Auslastung Ihres Systems zu analysieren, z. B. vmstat und iostat unter Linux oder Windows System Performance Monitor. Es gibt darüber hinaus viele andere Tools zur Leistungsüberwachung, die Ihnen zur Verfügung stehen. Leistungsüberwachung und Optimierung sind Themen, auf die Sie viel Zeit und Mühe verwenden können. Im Allgemeinen müssen Sie wissen, ob bestimmte Ressourcen im System vorhanden sind (Prozessor, Speicher, Platte, Netz), die sehr stark ausgelastet sind oder nicht verwendet werden. Mit diesen Informationen können Sie dazu beitragen, die Größe Ihres neuen Systems besser zu veranschlagen. Ein System, das zum Beispiel häufig überbelegte Speicherkapazität aufweist, kann von einer größeren Speicherkapazität in einem Zielsystem profitieren, in das Sie die Migration vornehmen.

## Wie kann ich alte und neue Prozessoren vergleichen?
{: #old-new}

Um die Spezifikationen alter und neuer Intel-Prozessoren zu vergleichen, wechseln Sie zu [https://ark.intel.com/#@Processors](https://ark.intel.com/#@Processors){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link"). Wenn Sie den Prozessortyp kennen, können Sie durch die Menüs navigieren. Alternativ können Sie die Suchoption verwenden, um die Spezifikationen der beiden Prozessoren zu lokalisieren. Neuere Prozessoren weisen tendenziell mehr Prozessorkerne auf und werden in der Regel mit langsameren Taktgeschwindigkeiten ausgeführt als ältere Varianten. Wenn Ihre Auslastung prozessorgebunden ist (ihre Leistung wird durch die Geschwindigkeit des Prozessors begrenzt), raten wir Ihnen, einen Prozessor mit weniger Kernen und einer höheren Taktgeschwindigkeit auszuwählen.  Wenn Sie viele Workloads ausführen, die nicht durch die Prozessorgeschwindigkeit eingeschränkt sind, kann die Auswahl eines Prozessors mit mehr Kernen und einer ähnlichen oder langsameren Taktgeschwindigkeit eine bessere Wahl sein.

## Wie wähle ich mein neues Betriebssystem aus?
{: #operating-system}

Wenn der Server seit vielen Jahren im Gebrauch ist und nicht auf dem neuesten Stand gehalten wurde, führen Sie wahrscheinlich eine ältere Version des Betriebssystems aus. Dies kann bei der Migration Herausforderungen darstellen. Sie verfügen möglicherweise nicht über den Installationsdatenträger für das alte Betriebssystem, von dem installiert werden soll.  Möglicherweise stellen Sie auch fest, dass die neuere Server-Hardware, auf die Sie migrieren, von der alten Betriebssystemversion nicht unterstützt wird. Es kann daher erforderlich sein, für die Migration ein anderes Betriebssystem auszuwählen.

Die Flexibilität bei der Betriebssystemauswahl ist möglicherweise durch die Anwendungen eingeschränkt, die ausgeführt werden. Als Teil der Migration müssen Sie möglicherweise die Anwendung auf einer späteren Version des Betriebssystems ausführen. Stellen Sie sicher, dass sie auch auf der neueren Version ausgeführt werden kann.

Die verfügbaren Kenntnisse in einem bestimmten Betriebssystem können ebenfalls Einfluss auf Ihre Auswahl haben. Wenn Sie den Quellcode für die Anwendung haben, stellen Sie sicher, dass die erforderlichen Entwicklungstools und unterstützende Betriebssystem- oder Middlewarefunktionen auf der neuen Plattform verfügbar sind. Im Allgemeinen sind Linux-Systeme besser bei der Unterstützung älterer Anwendungen auf neueren Versionen des Betriebssystems als Windows-Systeme. 

## Welche Bandbreite erhalte ich mit meiner neuen Konfiguration und gilt dabei derselbe Preis?
{: #bandwidth}

Sie erhalten ein aktuelles Paket mit der Bandbreite, die am ehesten mit dem Paket übereinstimmt, das Sie aktuell verwenden. Der Preis für dieses Paket entspricht dem aktuellen Preis bzw. dem aktuellen Paketumfang.

## Wie kann ich Daten von meinem alten Server auf den neuen Server kopieren?
{: #old-server}

Nachdem Sie die Verbindung zwischen dem alten und dem neuen Server hergestellt haben, sollten Sie darüber nachdenken, wie Sie Daten zwischen den beiden Servern verschieben können.  Angenommen, Sie haben genügend Speicherplatz auf dem neuen Server, um das Datenvolumen aufzunehmen, dann ist eine direkte Server-zu-Server-Kopie die einfachste Möglichkeit.  Es stehen viele Tools zur Verfügung, die Sie dafür verwenden können.  

* So ist zum Beispiel 'scp' eine gute Wahl, um eine Datei sicher von der Quelle zum Ziel zu kopieren. Es führt eine einfache lineare Kopie durch. 
* Wenn Sie zahlreiche Dateien kopieren müssen, ist 'rsync' über 'ssh' viel schneller als 'scp'. Außerdem kopiert 'rsync' auch Verzeichnisstrukturen und erhält die Dateiberechtigungen.

Im Allgemeinen sollten Sie Anwendungen und Anwendungsdaten nur zwischen Systemen kopieren. Das Kopieren älterer Versionen von Betriebssystemdateien auf neuere Versionen kann zu Problemen führen.

Beenden Sie die Datenbanken, bevor Sie sie zwischen den Systemen kopieren, um sicherzustellen, dass die Daten konsistent sind. Stellen Sie bei der Migration der Datenbankdaten sicher, dass die Daten auf eine Weise migriert werden, die Ihre Möglichkeiten beim Import in ein neues System nicht einschränkt. Anstatt Datenbankdaten von einem System auf ein anderes System zu kopieren, sollten Sie sie in ein Format exportieren, das es Ihnen ermöglicht, sie in eine neuere Datenbank zu importieren. Unstrukturierte Textdateien, CSV-Dateien und andere Dateien bieten mehr Optionen als die Verwendung proprietärer oder geschlossener Dateiformate, wenn es um das Verschieben von Daten zwischen Systemen geht. Testen Sie Ihre Datenmigrationsmethoden immer mit einem kleinen Satz von Testdaten, bevor Sie den kompletten Kopiervorgang ausführen.

## Muss ich die Vernetzung auf der neuen Site erneut konfigurieren?
{: #networking}

Höchstwahrscheinlich müssen Sie die Vernetzung ändern, um mit den neuen Servern und dem neuen Standort arbeiten zu können. Wenn Sie dabei Hilfe benötigen, setzen Sie sich telefonisch oder per Chat mit dem Support in Verbindung.

## Was mache ich, wenn ich nicht über die Fähigkeiten verfüge, die Migration durchzuführen?
{: #migrate-skills}

Die Anwendungsmigration kann ein komplexes Unterfangen sein. Nicht zuletzt sind auch die Fähigkeiten komplex, die dazu erforderlich sind. Wenn Codeänderungen für die Anwendung erforderlich sind, stellen Sie sicher, dass die erforderlichen Programmierkenntnisse vorhanden sind. Dies ist bei älteren Systemen wichtig, in denen die Kenntnisse möglicherweise selten sind oder die Dokumentation oder die Kenntnisse über das System selbst fehlen. Wenn erhebliche Anstrengungen unternommen werden müssen und das System kritisch für das Unternehmen ist, sollten Sie in die bezahlten Services oder in andere Migrationsservices investieren, damit Ihnen professionell geholfen wird.

## Wie bekomme ich allgemeine Hilfe bei der Migration?
{: #gen-migration}

Abhängig von der Art der erforderlichen Hilfe, können Sie sich telefonisch oder per Chat an den Support wenden. Oder Sie können unser Managed Service-Team kontaktieren. 

## An wen kann ich mich wenden, wenn ich keinen Account-Manager habe?
{: #account-contact}

Sie können die Unterstützung per Telefon oder Chat bei allen Migrationsfragen, die Sie haben, kontaktieren.
