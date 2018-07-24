---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-14"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Come ottengo una risposta rapida al mio caso?
{: #quicktickresp}

Quando contatti il supporto e apri un caso, puoi richiedere un determinato livello di severità, a seconda del tipo e dell'urgenza del problema. Il livello di severità può incidere sulla rapidità con cui viene affrontato il tuo problema.
{:shortdesc}

Puoi definire la severità del problema in base alle tue esigenze di business e al tuo livello di supporto. Consulta [Piani di supporto](/docs/get-support/index.html) per ulteriori informazioni sui livelli di piani di supporto. Tutti i casi vengono esaminati per identificare e risolvere la causa principale del problema. Se sono richiesti i dati diagnostici del problema per determinarne la causa principale, ti viene chiesta l'approvazione per accedere ai file di log e ad altri dati per la determinazione del problema dalla tua applicazione. Senza questi dati, la risoluzione del problema potrebbe richiedere più tempo.

## Raccolta delle informazioni di diagnostica
{: #collecting-diagnostic-information}

Per diagnosticare e risolvere i problemi con le applicazioni e i servizi {{site.data.keyword.Bluemix_notm}},
il team di supporto {{site.data.keyword.Bluemix_notm}}
potrebbe chiederti di raccogliere informazioni di diagnostica. Utilizza le seguenti istruzioni per raccogliere e fornire le informazioni richieste il più rapidamente possibile.

Prima di raccogliere le informazioni di diagnostica, completa la
seguente procedura:

1. Assicurati di aver installato l'interfaccia riga di comando Cloud Foundry più recente. Per ulteriori informazioni, vedi [Installazione dell'interfaccia riga di comando Cloud Foundry](/docs/starters/install_cli.html).
>**Nota:** se non hai installato l'interfaccia riga di comando Cloud Foundry più recente, dopo aver connesso la riga di comando cf a {{site.data.keyword.Bluemix_notm}}, il comando `cf logs` potrebbe non restituire alcun output.
2. Assicurati di aver connesso l'interfaccia riga di comando Cloud Foundry alla posizione in cui {{site.data.keyword.Bluemix_notm}} è in esecuzione utilizzando il comando `cf api`.

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

Come cliente {{site.data.keyword.Bluemix_notm}}, puoi richiedere ulteriore assistenza eseguendo una escalation del tuo caso al responsabile del supporto {{site.data.keyword.Bluemix_notm}} in servizio. Il processo di escalation ti consente di dare rilievo ai problemi critici e anche di esprimere la tua preoccupazione se ritieni che non ci si stia occupando in modo adeguato del tuo caso di supporto. Dopo l'esecuzione dell'escalation di un caso, il responsabile in servizio riesamina le informazioni nel caso di supporto, coinvolge i membri appropriati del team tecnico di supporto {{site.data.keyword.Bluemix_notm}} e ti fornisce gli aggiornamenti appropriati.

Per eseguire l'escalation di un caso di supporto, devi disporre di un supporto avanzato o premium {{site.data.keyword.Bluemix_notm}} e devi aver aperto un caso di supporto per il problema. Assicurati inoltre che il problema tecnico sia ben documentato nel caso di supporto da te aperto.

 Per eseguire l'escalation di un caso, completa la seguente procedura:

  1. Contatta il team di supporto {{site.data.keyword.Bluemix_notm}} telefonicamente o via chat:
    * Telefonicamente al seguente numero: 866-403-7638.
    * Via chat dal {{site.data.keyword.Bluemix_notm}} [Centro di supporto ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} o, se hai un account SoftLayer che non è collegato, dal [portale clienti ![Icona link esterno](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}.
  2. Fornisci il tuo numero del caso esistente e richiedi l'escalation del caso.
  3. Fornisci la giustificazione per l'escalation e l'impatto aziendale del tuo caso.

I responsabili del supporto {{site.data.keyword.Bluemix_notm}} sono in servizio e disponibili 24 ore al giorno, ogni giorno della settimana. I responsabili in servizio coinvolgono le risorse appropriate per risolvere il tuo caso e ti informano quindi delle azioni intraprese.
