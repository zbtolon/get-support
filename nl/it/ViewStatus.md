---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-04"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Visualizzazione delle notifiche e dello stato del sistema
{: #viewing-bluemix-status}

La pagina Stato è la posizione centrale per trovare notifiche e annunci sugli eventi chiave che interessano la piattaforma {{site.data.keyword.Bluemix_notm}} e i servizi principali.
{:shortdesc}

Nella pagina Stato, puoi trovare le seguenti informazioni:

  * Lo stato corrente di servizi e componenti in tutte le regioni del servizio {{site.data.keyword.Bluemix_notm}} Foundry.
  * Un elenco di annunci, in ordine cronologico, per la manutenzione
e gli eventi imprevisti. Puoi filtrare l'elenco o aprire un singolo annuncio
per ulteriori dettagli.
  * Finestre di manutenzione pianificata per le quali è fornito un preavviso, tranne in circostanze estreme.
  * Interruzioni o eventi imprevisti non pianificati, che vengono pubblicati non appena il team di {{site.data.keyword.Bluemix_notm}} ne
viene a conoscenza. Le notifiche sugli eventi imprevisti vengono regolarmente aggiornati finché non
vengono risolti.
  * Riferimenti a bollettini di sicurezza che incidono sulla piattaforma e sui vari servizi {{site.data.keyword.Bluemix_notm}}.
  * Altri annunci a livello di piattaforma di interesse generale per te.
  * [Un feed RSS a cui puoi sottoscrivere](#subscribing-rss-feed).

Puoi individuare la pagina Stato scegliendo una delle seguenti opzioni:

  * Accedi alla console {{site.data.keyword.Bluemix_notm}}. Dalla barra dei menu, fai clic su **Supporto** e seleziona **Stato**. Controlla le risorse elencate per l'icona di ![alcuni problemi](images/some_issues.svg). Questa icona potrebbe indicare un'interruzione.
  * Accedi direttamente alla pagina [{{site.data.keyword.Bluemix_notm}} - Stato ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/status){: new_window}.


## Procedure consigliate per il monitoraggio dello stato
{: #best-practices}

Utilizza le seguenti procedure consigliate per monitorare lo stato di {{site.data.keyword.Bluemix_notm}} per rimanere informato e pianificare di conseguenza.

### Controlla le prossime finestre di manutenzione
{: #monbp-checmaintwin}

Controlla le finestre di manutenzione in arrivo pubblicate nella pagina Stato, almeno una volta ogni 24 ore, utilizzando una delle seguenti opzioni:
* Andando direttamente alla pagina [Stato ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/status){: new_window}
* Utilizzando il feed RSS o un'utilità di inoltro da RSS a e-mail

### Controlla le finestre di manutenzione correnti o un evento imprevisto in corso
{: #monbp-checcurmaninprog}

Se hai il sospetto che {{site.data.keyword.Bluemix_notm}} non funzioni nel modo previsto, consulta la pagina Stato per controllare le finestre di manutenzione correnti o un evento imprevisto in corso. Per segnalare un evento imprevisto non ancora elencato nella pagina Stato, apri un ticket di supporto facendo clic su **Supporto** e selezionando **Aggiungi ticket** nella barra dei menu o accedendo alla pagina di assistenza [Supporto {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://www.ibm.biz/bluemixsupport){: new_window}.

### Usufruisci di più regioni del servizio {{site.data.keyword.Bluemix_notm}} Foundry
{: #monbp-multpreg}

Tutti gli utenti di {{site.data.keyword.Bluemix_notm}} pubblico hanno automaticamente accesso alle regioni Stati Uniti Sud, Regno Unito, Germania, Sydney, Stati Uniti Est e Asia Pacifico Nord. Il team di {{site.data.keyword.Bluemix_notm}} Global Operations gestisce tutte le regioni per evitare impatti sulla manutenzione e ridurre al minimo il rischio di eventi imprevisti che influiscano contemporaneamente su tutte le regioni.

Per cambiare regione, dalla barra dei menu di {{site.data.keyword.Bluemix_notm}}, espandi il menu della regione e seleziona quindi un'altra regione.

### Prepararsi a piccole interruzioni
{: #monbp-prepmininter}

Nella maggior parte dei casi, si può continuare a utilizzare {{site.data.keyword.Bluemix_notm}}
normalmente, anche durante la finestra di manutenzione. Tuttavia, non è sempre possibile evitare delle brevi interruzioni di servizio. In genere, le applicazioni in esecuzione rimangono disponibili anche se le funzioni
di gestione applicazione di {{site.data.keyword.Bluemix_notm}},
come l'avvio o l'arresto di applicazioni, vengono temporaneamente interrotte. Per
massimizzare la disponibilità delle tue applicazioni in esecuzione, esegui almeno
tre istanze di ciascuna applicazione.

## Sottoscrizione a un feed RSS
{: #subscribing-rss-feed}

Ricevi gli avvisi di eventuali notifiche sottoscrivendo il feed RSS per la pagina Stato di {{site.data.keyword.Bluemix_notm}}. In questo modo puoi ottenere gli aggiornamenti senza dover consultare regolarmente la pagina Stato.

Per eseguire la sottoscrizione, completa la seguente procedura:

1. Scarica e installa un lettore RSS.
2. Utilizza il tuo lettore per sottoscrivere il feed con uno dei seguenti
metodi:
    * Trascina l'icona RSS ![RSS](images/rss.svg) nel tuo lettore RSS.
    * Fai clic con il tasto destro del mouse sull'icona RSS, seleziona **Copia indirizzo link** e incolla l'URL
nel tuo lettore RSS.

Per ulteriori informazioni, vedi la sezione della **Guida** del tuo lettore. 	   

Altri metodi di lettura dei feed RSS sono disponibili tramite plug-in del browser Web come:
  * [RSS Feed ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://feeder.co/){: new_window} Reader for Chrome
  * [Brief ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} add-on for Firefox

Fonti di notizie, come i seguenti siti, forniscono anche dei metodi per la lettura dei feed RSS:
  * [Feedly ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://www.feedly.com/){: new_window}
  * [G2reader ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://www.g2reader.com/en/){: new_window}

Puoi inoltre
utilizzare un servizio di terze parti per inviare automaticamente un'e-mail
per ogni aggiornamento RSS. Il seguente elenco riporta alcuni esempi di servizi di terze parti:

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com

{{site.data.keyword.Bluemix_notm}} solitamente
ha circa 50 aggiornamenti al mese.


## Configurazione di notifiche per incidenti e manutenzione
{: #setting-up-notifications}

Per {{site.data.keyword.Bluemix_notm}} pubblico, puoi registrarti per ricevere le notifiche della piattaforma, che sono avvisi e-mail facoltativi per eventi di incidenti e manutenzione relativi alla piattaforma. Per configurare le notifiche, fai clic su **Gestisci** > **Account** > **Notifiche** e seleziona la scheda **Piattaforma**. 
