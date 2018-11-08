---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-23"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Come ottengo una risposta rapida al mio ticket?
{: #quicktickresp}

Quando contatti il supporto e apri un ticket, puoi richiedere un determinato livello di severità, a seconda del tipo e dell'urgenza del problema. Il livello di severità può incidere sulla rapidità con cui viene affrontato il tuo problema.
{:shortdesc}

Puoi definire la severità del problema in base alle tue esigenze di business e al tuo livello di supporto. Per ulteriori informazioni sui livelli dei piani di supporto, vedi [Piani di supporto](/docs/get-support/index.html). Tutti i ticket vengono esaminati per identificare e risolvere la causa principale del problema. Quando il team di supporto ha bisogno dei dati diagnostici del problema per determinarne la causa principale, ti viene richiesta l'approvazione per accedere ai file di log e ad altri dati per la determinazione dei problemi dalla tua applicazione. Senza questi dati, la risoluzione del problema potrebbe richiedere più tempo.

## Raccolta delle informazioni di diagnostica
{: #collecting-diagnostic-information}

Per diagnosticare e risolvere i problemi con le applicazioni e i servizi {{site.data.keyword.Bluemix_notm}}, il team di supporto {{site.data.keyword.Bluemix_notm}} potrebbe richiedere informazioni di diagnostica. Utilizza le seguenti istruzioni per raccogliere e fornire le informazioni richieste il più rapidamente possibile.

Prima di raccogliere le informazioni di diagnostica, completa la
seguente procedura:

1. Assicurati di aver istallato la versione più recente dell'interfaccia riga di comando Cloud Foundry. Per ulteriori informazioni, vedi [Installazione dell'interfaccia riga di comando Cloud Foundry](/docs/starters/install_cli.html).
>**Nota:** se non disponi della versione più recente, dopo aver connesso la riga di comando Cloud Foundry a {{site.data.keyword.Bluemix_notm}}, il comando `cf logs` potrebbe non restituire alcun output.
2. Assicurati di aver connesso l'interfaccia riga di comando Cloud Foundry all'ubicazione in cui {{site.data.keyword.Bluemix_notm}} è in esecuzione utilizzando il comando `cf api`.

Utilizza uno sei seguenti script per raccogliere le informazioni di diagnostica:

  * Per i sistemi operativi Windows, scarica il file [bmdiag-general.bat ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} ed eseguilo.
  * Per i sistemi operativi Linux e Mac, scarica il file [bmdiag-general.sh ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} ed eseguilo.

Gli script utilizzano l'interfaccia riga di comando Cloud Foundry per estrarre le seguenti informazioni dall'ambiente dell'applicazione:
  * Log dell'applicazione
  * Metadati dell'applicazione
  * Rotte configurate
  * Eventi
  * Servizi con provisioning

## Escalation dei casi di supporto
{: #escalation}

Utilizza il processo di escalation per dare rilievo ai problemi critici o se ritieni che il tuo caso di supporto non venga affrontato adeguatamente. Quando un caso viene inoltrato al livello superiore, il responsabile in servizio riesamina le informazioni nel caso di supporto, coinvolge i membri appropriati del team tecnico di supporto {{site.data.keyword.Bluemix_notm}} e ti fornisce gli aggiornamenti appropriati.

Puoi richiedere ulteriore assistenza eseguendo una escalation del tuo caso al responsabile del supporto {{site.data.keyword.Bluemix_notm}} in servizio come un cliente con qualsiasi sottoscrizione a pagamento. 

Per eseguire l'escalation di un caso di supporto, devi avere un caso di supporto aperto per il problema. Inoltre, assicurati di aver fornito una descrizione dettagliata del problema tecnico nel caso di supporto che hai aperto.

 Per eseguire l'escalation di un caso, completa la seguente procedura:

  1. Contatta il team di supporto {{site.data.keyword.Bluemix_notm}} telefonicamente o via chat:
    * Telefonicamente al seguente numero: 866-403-7638.
    * Via chat dal {{site.data.keyword.Bluemix_notm}} [Centro di supporto ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} o, se hai un account SoftLayer che non è collegato, dal [portale clienti ![Icona link esterno](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}.
  2. Fornisci il tuo numero del caso esistente e richiedi l'escalation del caso.
  3. Fornisci la giustificazione per l'escalation e l'impatto aziendale del tuo caso.

I responsabili del supporto {{site.data.keyword.Bluemix_notm}} sono in servizio e disponibili 24 ore al giorno, ogni giorno della settimana. I responsabili in servizio coinvolgono le risorse appropriate per risolvere il tuo caso e ti informano quindi delle azioni intraprese.
