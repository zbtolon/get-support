---

copyright:

  years: 2015, 2019

lastupdated: "2019-02-19"

keywords: help managing cases, resolve issues managing cases, trouble working with cases

subcollection: get-support

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Fehlerbehebung für die Verwaltung von Supportfällen
{: #Supportcases}

Es können Probleme beim Erstellen und Verwalten von {{site.data.keyword.Bluemix}}-Supportfällen auftreten. In vielen Fällen können Sie diese Probleme durch Ausführen weniger einfacher Schritte beheben.
{:shortdesc}

## Warum kann ich keinen Supportfall erstellen oder bearbeiten? 
{: #ts_service_broker}

Sie können keinen {{site.data.keyword.Bluemix_notm}}-Supportfall erstellen und es wird eine Fehlernachricht angezeigt, die besagt, dass Sie nicht über den entsprechenden Zugriff verfügen. 
{:shortdesc}

Wenn Sie versuchen, einen Fall zu erstellen, wird die folgende Fehlernachricht angezeigt:   
{: tsSymptoms}

`Sie verfügen offenbar nicht über die Zugriffsberechtigung zum Erstellen von Fällen für dieses Konto.`

Allgemeine Probleme beim Zugriff auf und der Verwaltung von Supportfällen können dadurch verursacht werden, dass die Zugriffsrichtlinie Identity and Access Management (IAM) für den Kontoverwaltungsservice des Support Centers nicht vorhanden ist. Ihnen muss die Editor- oder die Administratorrolle auf dem Kontoverwaltungsservice des Support Centers zugeordnet werden, um Fälle zu erstellen. 
{: tsCauses}

Um das Problem zu lösen, kann der Kontoeigner, ein Administrator für den Service Support Center oder der Administrator für alle Kontoverwaltungsservices eine IAM-Richtlinie für das Support Center zur Verwaltung von Fällen zuweisen. 
{: tsResolve}

Wenn Sie der Kontoeigner oder ein Administrator des Support Centers sind, führen Sie die folgenden Schritte aus, um eine Zugriffsrichtlinie für die Arbeit mit Supportfällen zu erstellen:

1. Rufen Sie **Verwalten** &gt; **Zugriff (IAM)** auf und wählen Sie dann **Benutzer** aus.
2. Wählen Sie einen Benutzernamen aus und klicken Sie auf **Zugriffsrichtlinien**. 
3. Klicken Sie auf **Zugriff zuweisen**. 
4. Wählen Sie **Zugriff auf Kontoverwaltungsservices zuweisen** aus. 
5. Wählen Sie im Menü **Service** die Option **Support Center** aus. 
6. Wählen Sie eine Rolle aus, um die Zugriffsebene für den Benutzer zu definieren. 


## Warum kann ich nicht alle Fälle im Konto anzeigen?
{: #ts_viewcasedetails}

Sie können nicht alle Fälle im Konto anzeigen, da Sie keinen Zugriff haben, um alle Benutzer im Konto anzuzeigen. 
{:shortdesc}

Wenn Sie versuchen, die Supportfälle anzuzeigen, die dem Konto zugeordnet sind, können Sie nicht alle offenen Fälle sehen. 
{: tsSymptoms}

Der Kontoeigner hat die Einstellung für die [Sichtbarkeit der Benutzerliste](/docs/iam?topic=iam-userlistview#userlistview) eingeschränkt. Wenn für die Sichtbarkeit 'eingeschränkt' eingestellt ist und Sie nicht über eine zusätzliche Zugriffsrichtlinie zur Anzeige von Benutzern im Konto verfügen, dann haben Sie nicht den erforderlichen Zugriff zur Anzeige aller Fälle im Konto. Sie können nur die Benutzer anzeigen, die Sie zum Konto eingeladen haben, mit denen Sie eine Cloud Foundry-Organisationsmitgliedschaft teilen oder Benutzer, die sich in der Benutzerhierarchie Ihrer klassischen Infrastruktur befinden. 
{: tsCauses}

Ihnen muss über eine IAM-Richtlinie mindestens die Rolle des Anzeigeberechtigtem im Benutzerverwaltungs- und Kontoverwaltungsservice
zusätzlich zu Ihrer Zugriffsrichtlinie im Kontoverwaltungsservice des Support Centers zugewiesen sein. Um Ihren aktuellen Zugriff anzuzeigen, rufen Sie **Verwalten** &gt; **Zugriff (IAM)** auf und wählen Ihren Namen auf der Seite **Benutzer** aus. Klicken Sie auf die Registerkarte **Zugriffsrichtlinien** und überprüfen Sie die zugeordneten Richtlinien. 
{: tsResolve}

Um das Problem zu beheben, setzen Sie sich mit dem Kontoeigner in Verbindung, um den entsprechenden Zugriff anzufordern. 

## Warum kann ich einen Fall, den ich zuvor erstellt habe, nicht finden? 
{: #ts_viewarchivedcase}

Sie können Ihre Fälle, die Sie vor dem erweiterten {{site.data.keyword.Bluemix_notm}}-Plattformerlebnis erstellt haben, nicht finden. 
{:shortdesc}

Sie haben im Support Center die Registerkarte **Fälle verwalten** aufgerufen. Dort werden keine Fälle angezeigt, die Sie vor dem 2. Dezember 2018 erstellt haben. 
{: tsSymptoms}

Fälle, die vor dem 2. Dezember 2018 angelegt (d. h. geöffnet) wurden, sind nur über die Anzeigeoption **Archivierte Fälle anzeigen** sichtbar. 
{: tsCauses}

Rufen Sie zum Anzeigen Ihrer Fälle **Support** auf, wählen Sie die Option **Fälle verwalten** aus und klicken Sie auf **Archivierte Fälle anzeigen**.
{: tsResolve} 






