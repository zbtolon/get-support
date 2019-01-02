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

# Assegnazione dell'accesso utente per lavorare con i casi di supporto
{: #access}

Per impostazione predefinita, gli utenti nel tuo account non hanno accesso per creare, aggiornare, cercare o visualizzare i casi. Come proprietario dell'account, devi fornire agli utenti l'accesso assegnando una politica di accesso IAM (Identity and Access Management). Utilizza il servizio di gestione account Centro di supporto per assegnare agli utenti l'accesso per lavorare con i casi di supporto.
{:shortdesc}

Le politiche di accesso del Centro di supporto forniscono agli utenti l'accesso per lavorare con casi di supporto. Tuttavia, tali politiche di accesso non forniscono agli utenti l'accesso per visualizzare altri utenti nell'account. Quindi, se un proprietario di account ha impostato l'[**impostazione di visibilità dell'elenco utenti**](/docs/iam/userlist.html#userlistview) su **Visualizzazione limitata**, gli utenti che dispongono dell'accesso per gestire i casi potrebbero non essere in grado di accedere ai casi assegnati ad altri utenti o al proprietario dell'account. Per garantire che gli utenti possano visualizzare tutti i casi, devi fornire un accesso aggiuntivo assegnando anche una politica di accesso IAM per il servizio di gestione account Gestione utenti con il ruolo di visualizzatore assegnato. 

Per fornire a utenti specifici l'accesso completo a determinati casi nell'account anziché l'accesso a tutti i casi utilizzando una politica di accesso IAM, aggiungili al caso immettendo la loro email quando crei il caso. Aggiungendo un utente a un caso che crei, tale utente ha accesso per visualizzare, modificare e aggiornare solo quel caso nell'account. Inoltre riceve notifiche quando ci sono aggiornamenti al caso.

Per gli utenti dell'infrastruttura classica che in precedenza utilizzavano le autorizzazioni dell'infrastruttura classica per assegnare l'accesso ai casi di supporto, tali autorizzazioni sono ora disponibili nei [gruppi di accesso alle autorizzazioni dell'infrastruttura classica migrati](/docs/iam/infrastructureaccess.html#predefined). I gruppi di accesso alle autorizzazioni migrati includono la politica IAM sul servizio Gestione utenti con il ruolo di visualizzatore assegnato.

Per assegnare a un utente una politica di accesso IAM su un servizio di gestione account, come il servizio Centro di supporto o il servizio Gestione utenti, completa la seguente procedura:

1. Dalla barra dei menu, fai clic su **Gestisci** &gt; **Accesso (IAM)** e seleziona **Utenti**.
2. Seleziona un utente dall'elenco.
3. Fai clic su **Politiche di accesso**.
4. Fai clic su **Assegna accesso**.
5. Seleziona **Assegna l'accesso ai servizi di gestione account**.
6. Seleziona un servizio dall'elenco. 
5. Seleziona un ruolo per assegnare l'accesso previsto.

Controlla la seguente tabella per capire esattamente quali autorizzazioni sono incluse in ogni ruolo.

| Ruolo | Azione | 
|--------|---------------|
|Visualizzatore  | Visualizza e cerca i casi |
|Amministratore | Visualizza, cerca, crea e aggiorna i casi|
{: caption="Tabella 1. Ruoli e azioni per il servizio Centro di supporto" caption-side="top"}

