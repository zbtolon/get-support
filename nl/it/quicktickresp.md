---

copyright:

  years: 2015, 2018

lastupdated: "2018-03-15"

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

Puoi definire la severità del problema in base alle tue esigenze di business e al tuo livello di supporto. Tutti i ticket vengono esaminati per identificare e risolvere la causa principale del problema. Se sono richiesti i dati diagnostici del problema per determinarne la causa principale, ti verrà chiesta l'approvazione per accedere ai file di log e ad altri dati per la determinazione del problema dalla tua applicazione. Senza questi dati, la risoluzione del problema potrebbe richiedere più tempo.

Se ti viene richiesto di fornire informazioni di diagnostica, utilizza le seguenti istruzioni per raccogliere e fornire le informazioni richieste il più rapidamente possibile.

## Raccolta delle informazioni di diagnostica
{: #collecting-diagnostic-information}

Per diagnosticare e risolvere i problemi con le applicazioni e i servizi {{site.data.keyword.Bluemix_notm}},
il team di supporto {{site.data.keyword.Bluemix_notm}}
potrebbe chiederti di raccogliere informazioni di diagnostica.

Prima di raccogliere le informazioni di diagnostica, completa la
seguente procedura:

1. Assicurati di aver installato l'interfaccia riga di comando cf più recente. Per ulteriori informazioni, vedi [Installing the cf
command line interface](/docs/starters/install_cli.html).
>**Nota:** se non hai installato l'interfaccia riga di comando cf più recente, dopo aver connesso la riga di comando cf a {{site.data.keyword.Bluemix_notm}}, il comando `cf logs` potrebbe non restituire alcun input.
2. Assicurati di aver connesso l'interfaccia riga di comando cf alla posizione in cui {{site.data.keyword.Bluemix_notm}} è
in esecuzione utilizzando il comando `cf api`.

Utilizza uno sei seguenti script per raccogliere le informazioni di diagnostica:

  * Per i sistemi operativi Windows, scarica il file [bmdiag-general.bat ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} ed eseguilo.
  * Per i sistemi operativi Linux e Mac, scarica il file [bmdiag-general.sh ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} ed eseguilo.

Gli script utilizzano l'interfaccia riga di comando cf per estrarre
le seguenti informazioni dal tuo ambiente applicativo:
  * Log dell'applicazione
  * Metadati dell'applicazione
  * Rotte configurate
  * Eventi
  * Servizi con provisioning

## Posso effettuare l'escalation di un ticket di supporto?
{: #escalation}

Con un supporto premium o avanzato, se non hai ricevuto una risposta tempestiva a un ticket di supporto o ritieni che il ticket non venga affrontato in maniera appropriata, puoi effettuarne l'escalation.  
{:shortdesc}

Vedi [Tipi di supporto](/docs/get-support/getstarttssup.html#typesofsupport) per ulteriori informazioni sul supporto premium e avanzato.

Attraverso il processo di escalation del ticket di supporto, IBM prende in considerazione le tue preoccupazioni e collabora con te per migliorare la tua esperienza di supporto.

Per inoltrare una richiesta di escalation, completa la seguente procedura:
  1. Apri un nuovo ticket di supporto con riepilogo **Richiesta di escalation**.
  2. Per accertarti che venga trovata una corrispondenza tra la tua richiesta di escalation e il ticket di supporto originale, includi le seguenti informazioni nel corpo del ticket:
      * Il numero del tuo ticket di supporto aperto, che necessita di un'escalation.
      * Un breve riepilogo dei motivi per cui occorre un'escalation.

## Orario di operatività
{: #support-hours-operation}

I problemi di severità 1 vengono monitorati 24 ore al giorno, 7 giorni a settimana. Gli invii dei moduli per problemi con tutti gli altri livelli di severità vengono monitorati dalla domenica alle 21:30 UTC al venerdì alle 23:59 UTC (festività escluse).

Per assistenza nella conversione di queste ore di supporto al tuo fuso orario locale, vedi [Timeanddate.com ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.timeanddate.com). Per ulteriori informazioni sulla pianificazione delle festività, vedi [{{site.data.keyword.Bluemix_notm}} Support Holidays ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://ibm.biz/bluemixholidays).
