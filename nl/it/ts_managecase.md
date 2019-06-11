---

copyright:

  years: 2015, 2019

lastupdated: "2019-05-16"

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


# Risoluzione dei problemi relativi alla gestione dei casi di supporto
{: #Supportcases}

Potresti riscontrare dei problemi con la creazione e la gestione dei casi di supporto {{site.data.keyword.Bluemix}}. In molti casi, puoi risolvere questi problemi seguendo pochi semplici passi.
{:shortdesc}

## Perché non posso creare o modificare i casi di supporto? 
{: #ts_service_broker}

Non puoi creare o modificare un caso di supporto {{site.data.keyword.Bluemix_notm}} e ricevi un messaggio di errore che indica che non disponi dell'accesso appropriato.
{:shortdesc}

Quando tenti di creare un caso, viene visualizzato il seguente messaggio di errore:   
{: tsSymptoms}

`Sembra che tu non abbia l'accesso per creare i casi per questo account.`

I problemi generali relativi all'accesso e alla gestione dei casi di supporto potrebbero essere causati
dalla mancanza della politica di accesso IAM (Identity and Access Management) per il servizio di gestione account Centro di supporto. Per creare i casi, è necessario che ti venga assegnato il ruolo di editor o di amministratore sul servizio di gestione account del centro di supporto. 
{: tsCauses}

Per risolvere il problema, il proprietario dell'account, un amministratore del servizio del centro di supporto o l'amministratore di tutti i servizi di gestione account possono assegnare una politica IAM sul centro di supporto per gestire i casi.
{: tsResolve}

Se sei il proprietario dell'account o un amministratore del Centro di supporto, completa la seguente procedura per creare una politica di accesso per lavorare con i casi di supporto:

1. Vai a **Gestisci** &gt; **Accesso (IAM)** e seleziona **Utenti**.
2. Seleziona un nome utente e fai clic su **Politiche di accesso**. 
3. Fai clic su **Assegna accesso**. 
4. Seleziona **Assegna l'accesso ai servizi di gestione account**. 
5. Dal menu **Servizio**, seleziona **Centro di supporto**. 
6. Seleziona un ruolo per definire il livello di accesso per l'utente. 


## Perché non posso visualizzare tutti i casi nell'account?
{: #ts_viewcasedetails}

Non puoi visualizzare tutti i casi nell'account perché non disponi dell'accesso per visualizzare tutti gli utenti nell'account. 
{:shortdesc}

Quando tenti di visualizzare i casi di supporto associati all'account, non puoi visualizzare tutti i casi aperti. 
{: tsSymptoms}

Il proprietario dell'account ha impostato l'[impostazione di visibilità dell'elenco utenti](/docs/iam?topic=iam-userlistview#userlistview) su limitato. Quando l'impostazione è impostata su limitato e non disponi di un'altra politica di accesso per la visualizzazione degli utenti nell'account, non disponi dell'accesso necessario per visualizzare tutti i casi nell'account. Puoi visualizzare solo gli utenti che hai invitato all'account, con cui condividi un'appartenenza all'organizzazione Cloud Foundry, o gli utenti che si trovano nella tua gerarchia di utenti dell'infrastruttura classica. 
{: tsCauses}

È necessario che ti venga assegnata una politica IAM con almeno il ruolo di visualizzatore nel servizio di gestione account Gestione utenti oltre alla tua politica di accesso al servizio di gestione account Centro di supporto. Per visualizzare il tuo accesso corrente, vai a **Gestisci** &gt; **Accesso (IAM)** e seleziona il tuo nome dalla pagina **Utenti**. Fai clic sulla scheda **Politiche di accesso** e rivedi le tue politiche assegnate. 
{: tsResolve}

Per risolvere il problema, contatta il proprietario dell'account per richiedere l'accesso appropriato. 

## Perché non riesco a trovare un caso che ho creato in precedenza? 
{: #ts_viewarchivedcase}

Non riesci a trovare i tuoi casi che hai creato prima dell'esperienza della piattaforma {{site.data.keyword.Bluemix_notm}} migliorata. 
{:shortdesc}

Dopo essere andato alla scheda **Gestisci casi** nel Centro di supporto, non riesci a trovare alcun caso che hai creato prima del 2 dicembre 2018.
{: tsSymptoms}

I casi aperti prima del 2 dicembre 2018 sono visibili solo da **Visualizza casi archiviati**.
{: tsCauses}

Per visualizzare i tuoi casi, vai a **Supporto**, seleziona **Gestisci casi** e fai clic su **Visualizza casi archiviati**.
{: tsResolve} 






