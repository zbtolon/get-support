---

copyright:

  years: 2018

lastupdated: "2018-11-28"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Benutzerzugriff für die Arbeit mit Supportfällen zuweisen
{: #access}

Standardmäßig haben Benutzer in Ihrem Konto keinen Zugriff zum Erstellen, Aktualisieren, Suchen oder Anzeigen von Fällen. Als Kontoeigner müssen Sie Benutzern erst Zugriff gewähren, indem Sie eine IAM-Zugriffsrichtlinie (IAM, Identitäts- und Zugriffsmanagement) zuweisen. Verwenden Sie den Kontenverwaltungservice des Support Centers, um Benutzern Zugriffsrecht auf die Arbeit mit Supportfällen zuzuweisen. {:shortdesc}

Die Zugriffsrichtlinien des Support Centers bieten Benutzern Zugriff auf die Arbeit mit Supportfällen. Diese Zugriffsrichtlinien bieten jedoch für Benutzer keinen Zugriff, um andere Benutzer in dem Konto anzuzeigen. Wenn ein Kontoeigner für die Einstellung [**Sichtbarkeit der Benutzerliste**](/docs/iam/userlist.html#userlistview) die Option **Eingeschränkte Ansicht** festgelegt hat, können Benutzer, die Zugriff auf die Verwaltung der Fälle haben, möglicherweise nicht auf die Fälle zugreifen, die anderen Benutzern oder dem Kontoeigner zugewiesen sind. Um sicherzustellen, dass Benutzer alle Fälle anzeigen können, müssen Sie weiteren Zugriff erteilen, in dem Sie zusätzlich eine IAM-Zugriffsrichtlinie für den Kontoverwaltungsservice der Benutzerverwaltung mit der zugeordneten Rolle als Anzeigeberechtigter zuweisen.  

Um bestimmten Benutzern den uneingeschränkten Zugriff auf bestimmte Fälle im Konto zu gewähren, anstatt den Zugriff auf alle Fälle mithilfe einer IAM-Zugriffsrichtlinie zu gewähren, fügen Sie die Benutzer dem Fall hinzu, indem Sie deren E-Mail eingeben, wenn Sie den Fall erstellen. Durch das Hinzufügen eines Benutzers zu dem Fall, den Sie erstellen, erhalten diese Benutzer Zugriff zum Anzeigen, Bearbeiten und Aktualisieren für genau diesen Fall im Konto. Die Benutzer erhalten ferner Benachrichtigungen, wenn Aktualisierung zum Fall vorliegen. 

Für Benutzer der klassischen Infrastruktur, die bisher Berechtigungen für die klassische Infrastruktur verwendet haben, um den Zugriff auf Supportfälle zuzuweisen, stehen diese Berechtigungen nun in [migrierten Zugriffsgruppen für klassische Infrastruktur](/docs/iam/infrastructureaccess.html#predefined) zur Verfügung. Die migrierten Zugriffsgruppen umfassen die IAM-Richtlinie für den Benutzerverwaltungsservice mit der zugeordneten Rolle als Anzeigeberechtigter (Viewer).

Führen Sie die folgenden Schritte aus, um einem Benutzer eine IAM-Zugriffsrichtlinie in einem Kontoverwaltungsservice wie dem Support Center-Service oder dem Benutzerverwaltungsservice zuzuweisen. 

1. Klicken Sie in der Menüleiste auf **Verwalten** &gt; **Zugriff (IAM)** und wählen Sie anschließend **Benutzer** aus.
2. Wählen Sie einen Benutzer aus der Liste aus. 
3. Klicken Sie auf **Zugriffsrichtlinien**.
4. Klicken Sie auf **Zugriff zuweisen**.
5. Wählen Sie **Zugriff auf Kontoverwaltungsservices zuweisen**.
6. Wählen Sie einen Service aus der Liste aus. 
5. Wählen Sie eine Rolle aus, um den beabsichtigten Zugriff zuzuweisen. 

Überprüfen Sie die folgende Tabelle, um genau nachzuvollziehen, welche Berechtigungen in jeder Rolle enthalten sind. 

| Rolle | Aktion | 
|--------|---------------|
|Viewer (Anzeigeberechtigter)  | Fälle anzeigen und durchsuchen |
|Administrator | Fälle anzeigen, durchsuchen, erstellen und aktualisieren |
{: caption="Tabelle 1. Rollen und Aktionen für den Support Center-Service" caption-side="top"}

