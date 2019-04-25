---

copyright:

  years: 2018,2019

lastupdated: "2019-04-18"

keywords: access to cases, get access for cases, assign cases

subcollection: get-support

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Benutzerzugriff für die Arbeit mit Supportfällen zuweisen
{: #access}

Standardmäßig haben Benutzer in Ihrem Konto keinen Zugriff zum Erstellen, Aktualisieren, Suchen oder Anzeigen von Fällen. Als Kontoeigner müssen Sie Benutzern erst Zugriff gewähren, indem Sie eine IAM-Zugriffsrichtlinie (IAM, Identitäts- und Zugriffsmanagement) zuweisen. Verwenden Sie den Kontenverwaltungsservice des Support Centers, um Benutzern Zugriffsrecht auf die Arbeit mit Supportfällen zuzuweisen. 
{:shortdesc}

Wenn Sie einen Fall erstellen, können Sie anderen Benutzern den uneingeschränkten Zugriff auf bestimmte Fälle im Konto gewähren, indem Sie deren E-Mail-Adresse im Feld **Andere Person zu diesem Fall hinzufügen** ... angeben. Alle hinzugefügten Benutzer erhalten Zugriff zum Anzeigen, Bearbeiten und Aktualisieren für genau diesen Fall im Konto. Sie erhalten außerdem Benachrichtigungen, wenn der Fall aktualisiert wird.
{: tip}

Für Benutzer der klassischen Infrastruktur stehen die Berechtigungen für die Zuweisung von Zugriff auf Supportfälle nun in [migrierten Zugriffsgruppen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#predefined) zur Verfügung. Die Zugriffsgruppen für migrierte Berechtigungen umfassen die IAM-Richtlinie für den Benutzerverwaltungsservice mit der zugeordneten Rolle als Anzeigeberechtigter (viewer).

## Zugriffsgruppe für das Arbeiten mit Fällen erstellen
{: #creating-access-group}

Sie können den Prozess der Zugriffszuweisung optimieren, wenn Sie Benutzern anhand von Zugriffsgruppen eine Richtlinie zuweisen. Führen Sie die folgenden Schritte aus, um eine Zugriffsgruppe mit Zugriff auf den Support Center-Service zu erstellen:

1. Navigieren Sie in der Menüleiste zu **Verwalten** &gt; **Zugriff (IAM)**, wählen Sie **Zugriffsgruppen** aus und klicken Sie auf **Erstellen**. 
2. Geben Sie einen Namen und eine Beschreibung für die Zugriffsgruppe ein und klicken Sie dann auf **Erstellen**. 
3. Klicken Sie auf **Zugriffsrichtlinien** > **Zugriff zuweisen**.
4. Wählen Sie **Zugriff auf Kontoverwaltungsservices zuweisen** aus.
5. Wählen Sie **Support Center** aus.
6. Wählen Sie abhängig davon, welche Art von Zugriff diese Gruppe erhalten soll, die Rolle **Anzeigeberechtigter** (Viewer), **Bearbeiter** (Editor) oder **Administrator** aus und klicken Sie auf **Zuweisen**.

Wenn Ihre Benutzer in der Lage sein sollen, alle übrigen Benutzer im Konto anzuzeigen, können Sie zu Ihrer Zugriffsgruppe auch die Rolle des Anzeigeberechtigten für das Benutzermanagement wie folgt hinzufügen:

1. Klicken Sie auf **Zugriffsrichtlinien** > **Zugriff zuweisen**.
2. Wählen Sie **Zugriff auf Kontoverwaltungsservices zuweisen** aus.
3. Wählen Sie **Benutzermanagement** aus.
4. Wählen Sie **Anzeigeberechtigter** aus und klicken Sie auf **Zuweisen**.

Die folgende Tabelle enthält eine Auflistung der Berechtigungen, die in den einzelnen Rollen für das Arbeiten mit Fällen enthalten sind.

| Rolle | Aktion | 
|--------|---------------|
|Anzeigeberechtigter  | Fälle anzeigen und durchsuchen |
|Bearbeiter | Fälle anzeigen, durchsuchen, erstellen und aktualisieren|
|Administrator | Fälle anzeigen, durchsuchen, erstellen und aktualisieren; Support Center-Rollen für andere Benutzer verwalten|
{: caption="Tabelle 1. Rollen und Aktionen für den Support Center-Service" caption-side="top"}

## Benutzer zur Zugriffsgruppe für das Fallmanagement hinzufügen
{: #add-user-access-group} 

Nachdem Sie die Zugriffsgruppe erstellt haben, können Sie nun Benutzer zu ihr hinzufügen:

1. Klicken Sie auf der Registerkarte **Benutzer** für Ihre Zugriffsgruppe auf **Benutzer hinzufügen**.
2. Wählen Sie den Benutzer aus, den Sie zur Gruppe hinzufügen möchten, und klicken Sie auf **Zu Gruppe hinzufügen**.

## Einzelperson Zugriff auf Fälle erteilen 

Die Verwendung von Zugriffsgruppen für die Zuweisung von Support Center- und Benutzermanagementservices stellt die effizienteste Methode zum Erteilen von Zugriff dar. Dieselben Berechtigungen können Sie aber auch einzelnen Benutzern zuweisen. 

1. Klicken Sie auf **Verwalten** &gt; **Zugriff (IAM)** und wählen Sie **Benutzer** aus. 
2. Klicken Sie auf **Zugriffsrichtlinien** > **Zugriff zuweisen**.
3. Wählen Sie **Zugriff auf Kontoverwaltungsservices zuweisen** aus.
4. Wählen Sie **Support Center** aus.
5. Wählen Sie abhängig davon, welche Art von Zugriff diese Gruppe erhalten soll, die Rolle **Anzeigeberechtigter** (Viewer), **Bearbeiter** (Editor) oder **Administrator** aus und klicken Sie auf **Zuweisen**.
6. Wenn ein Benutzer in der Lage sein soll, alle übrigen Benutzer im Konto anzuzeigen, können Sie ihm auch die Rolle des Anzeigeberechtigten für das Benutzermanagement zuweisen. 
