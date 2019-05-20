---

copyright:

  years: 2018,2019

lastupdated: "2019-05-13"

keywords: access to cases, get access for cases, assign cases

subcollection: get-support

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Assegnazione dell'accesso utente per lavorare con i casi di supporto
{: #access}

Per impostazione predefinita, gli utenti nel tuo account non hanno accesso per creare, aggiornare, cercare o visualizzare i casi. Come proprietario dell'account, devi fornire agli utenti l'accesso assegnando una politica di accesso IAM (Identity and Access Management). Utilizza il servizio di gestione account Centro di supporto per assegnare agli utenti l'accesso per lavorare con i casi di supporto. 
{:shortdesc}

Quando crei un caso, puoi dare ad altri utenti un accesso completo a tale caso aggiungendo la loro email nel campo **Aggiungi un'altra persona a questo caso**. Gli utenti aggiunti hanno un accesso per visualizzare, modificare e aggiornare solo tale caso nell'account. Ricevono anche delle notifiche quando il caso viene aggiornato.
{: tip}

Per gli utenti dell'infrastruttura classica, le autorizzazioni per assegnare l'accesso ai casi di supporto sono ora disponibili nei [gruppi di accesso di autorizzazione dell'infrastruttura classica migrati](/docs/iam?topic=iam-infrapermission#predefined). I gruppi di accesso di autorizzazione migrati includono la politica IAM sul servizio di gestione utenti con assegnato il ruolo visualizzatore.

## Creazione di un gruppo di accesso per la gestione dei casi
{: #creating-access-group}

Per semplificare il processo di assegnazione dell'accesso, puoi avvalerti dell'assegnazione di una politica agli utenti tramite i gruppi di accesso. Completa la seguente procedura per creare un gruppo di accesso con l'accesso al servizio Centro di supporto:

1. Dalla barra dei menu, vai a **Gestisci** &gt; **Accesso (IAM)**, seleziona **Gruppi di accesso** e fai clic su **Crea**. 
2. Immetti un nome e una descrizione del gruppo di accesso e fai clic su **Crea**. 
3. Fai clic su **Politiche di accesso** > **Assegna accesso**.
4. Seleziona **Assegna l'accesso ai servizi di gestione account**.
5. Seleziona **Centro di supporto**.
6. Seleziona il ruolo **Visualizzatore**, **Editor** o **Amministratore** a seconda del tipo di accesso che vuoi abbia questo gruppo e fai clic su **Assegna**.

Se desideri che i tuoi utenti possano visualizzare tutti gli altri utenti nell'account, puoi anche aggiungere il ruolo visualizzatore di gestione utenti al tuo gruppo di accesso:

1. Fai clic su **Politiche di accesso** > **Assegna accesso**.
2. Seleziona **Assegna l'accesso ai servizi di gestione account**.
3. Seleziona **Gestione utenti**.
4. Seleziona **Visualizzatore** e fai clic su **Assegna**.

La seguente tabella elenca le autorizzazioni incluse in ciascun ruolo per la gestione dei casi.

| Ruolo | Azione | 
|--------|---------------|
|Visualizzatore  | Visualizza e cerca i casi |
|Editor | Visualizza, cerca, crea e aggiorna i casi|
|Amministratore | Visualizza, cerca, crea e aggiorna i casi; gestisci i ruoli del centro di supporto per gli altri utenti|
{: caption="Tabella 1. Ruoli e azioni per il servizio Centro di supporto" caption-side="top"}

## Aggiunta di utenti al tuo gruppo di accesso di gestione dei casi
{: #add-user-access-group} 

Ora che hai creato il gruppo di accesso, aggiungi gli utenti: 

1. Dalla scheda **Utenti** per il tuo gruppo di accesso, fai clic su **Aggiungi utenti**.
2. Seleziona l'utente che desideri aggiungere al gruppo e fai clic su **Aggiungi al gruppo**.

## Concessione a singoli utenti dell'accesso ai casi 

Utilizzare i gruppi di accesso per assegnare i servizi di gestione utenti e del centro di supporto è il modo più efficiente a tua disposizione per assegnare l'accesso ma puoi anche assegnare le stesse autorizzazioni a singoli utenti. 

1. Fai clic su **Gestisci** &gt; **Accesso (IAM)** e seleziona quindi **Utenti**. 
2. Fai clic su **Politiche di accesso** > **Assegna accesso**.
3. Seleziona **Assegna l'accesso ai servizi di gestione account**.
4. Seleziona **Centro di supporto**.
5. Seleziona il ruolo **Visualizzatore**, **Editor** o **Amministratore** a seconda del tipo di accesso che vuoi abbia questo gruppo e fai clic su **Assegna**.
6. Se desideri che un utente possa visualizzare tutti gli altri utenti nell'account, puoi anche assegnargli il ruolo visualizzatore di gestione utenti. 
