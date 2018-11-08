---

copyright:

  years: 1994, 2018

lastupdated: "2018-10-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Ritiro del supporto per alcuni data center US
{: #dc-migrate}

IBM sta ritirando il supporto per i seguenti data center negli Stati Uniti: 

* pod dal01 2 e 3
* pod wdc01 1 e 2
{:shortdesc}

##  Perché mi viene richiesto di passare a un altro data center?

Per continuare a offrirti il servizio, l'hardware e la connettività migliori, valutiamo continuamente tutti i nostri siti per garantire che soddisfino gli standard di rete, elettrici e di altra natura infrastrutturale. Pur essendo adeguati, questi siti non soddisfano più i nostri standard attuali.

## Devo aver eseguito completamente la migrazione entro la data elencata?

Sì. Per garantire che tu non subisca alcuna interruzione nel servizio, stiamo tentando di consentire quanto più tempo di esecuzione possibile per fare in modo che la transizione avvenga praticamente senza soluzione di continuità. Abbiamo iniziato a comunicare questo spostamento di sito nel maggio del 2018.

## Avrò mai nuovamente bisogno di spostarmi a un altro data center?

Valutiamo costantemente la qualità dei nostri siti per offrirti il servizio migliore e più affidabile. Potremmo prevedere qualche altro spostamento, man mano che continuiamo a valutare alcuni dei siti meno recenti.

## Posso scegliere qualsiasi data center US {{site.data.keyword.Bluemix_notm}}?

Sì, puoi scegliere qualsiasi sito IBM US che soddisfa le tue esigenze di ubicazione.

## Come seleziono il data center al quale eseguire la distribuzione?

IBM ha più di 60 data center in località in tutto il mondo. Visualizza la mappa dei data center nella nostra pagina dei data center globali per vedere quali sono i data center in cui puoi eseguire la distribuzione. 

I seguenti fattori potrebbero influenzare quale data center selezioni.
* Prossimità agli utenti dei sistemi
* Prossimità a qualsiasi altro sistema con cui questo server deve comunicare
* Eventuali politiche o regolamenti che richiedono che i dati siano archiviati in una specifica località

## Devo utilizzare siti US anche per il periodo di transizione?

Puoi utilizzare qualsiasi sito {{site.data.keyword.cloud_notm}} in tutto il mondo durante il tuo periodo di transizione, che dura fino a 60 giorni.

## I due mesi gratuiti di risorse del periodo di transizione sono in aggiunta al mio tempo di server esistente?

Sì. Puoi contattarci e un rappresentante del supporto appropriato ti aiuterà con la procedura di acquisizione dei tuoi server del periodo di transizione.

## Come determino la mia configurazione hardware attuale?

Esegui l'accesso al portale del cliente. Dal **Device List**, seleziona il server a cui sei interessato e trova i dettagli di configurazione del sistema. Da tale ubicazione puoi visualizzare il tipo di processore, ad esempio Single Intel Xeon E3-1270 (4 core, 3,50 GHz). Puoi anche visualizzare la quantità di memoria (RAM), archiviazione e altri dati.

## Come determino l'utilizzo del mio hardware attuale?

La maggior parte dei sistemi operativi fornisce strumenti di cui puoi fare uso per comprendere l'utilizzo del tuo sistema, ad esempio vmstat e iostat su Linux o Windows System Performance Monitor. Ci sono anche molti altri strumenti di monitoraggio delle prestazioni che potrebbero essere a tua disposizione. Il monitoraggio e l'ottimizzazione delle prestazioni è qualcosa in cui potresti investire molto tempo e notevoli sforzi. In generale, devi comprendere se ci sono delle risorse specifiche nel sistema (processore, memoria, disco, rete) che sono utilizzate in modo intensivo oppure non utilizzate come dovrebbero. Disporre di queste informazioni può aiutarti a specificare meglio la dimensione del tuo nuovo sistema. Ad esempio, un sistema in cui la capacità di memoria viene spesso sovraccaricata probabilmente trarrà vantaggio da dimensioni della memoria più grandi nel sistema di destinazione a cui esegui la migrazione.

## Come confronto i vecchi processori con quelli nuovi?

Per confrontare le specifiche di processori Intel vecchi e nuovi, vai a [https://ark.intel.com/#@Processors](https://ark.intel.com/#@Processors). Se conosci il tipo di processore, puoi spostarti nei menu. In alternativa, puoi utilizzare l'opzione di ricerca per individuare le specifiche dei due processori. I processori più recenti tendono ad avere più core di processore e di norma vengono eseguiti a velocità di clock più lente rispetto alle varianti meno recenti. Se hai un carico di lavoro associato al processore (le sue prestazioni sono limitate dalla velocità del processore), consigliamo di scegliere un processore con un numero inferiore di core e una velocità di clock maggiore. Se esegui molti carichi di lavoro che non sono particolarmente vincolati dalla velocità del processore, scegliere un processore con più core e una velocità di clock simile o inferiore potrebbe essere una scelta migliore.

## Come scelgo il mio nuovo sistema operativo?

Se il server è stato in uso per molti anni e non è stato tenuto aggiornato, è probabile che tu stia eseguendo una versione meno recente del sistema operativo. Ciò può presentare delle difficoltà quando si esegue la migrazione. Potresti non disporre del supporto di installazione per il vecchio sistema operativo da cui installare. Potresti anche rilevare che l'hardware server più recente a cui stai eseguendo la migrazione non è supportato dalla versione del sistema operativo meno recente. Pertanto, potresti dover scegliere un sistema operativo differente a cui passare.

La scelta del sistema operativo potrebbe essere stabilita dalle applicazioni che stai eseguendo. Come parte della migrazione, potresti dover eseguire l'applicazione su una versione successiva del sistema operativo. Assicurati che funzionerà sulla versione più recente.

Anche le capacità disponibili in uno specifico sistema operativo potrebbero influenzare la tua scelta. Se hai il codice sorgente per l'applicazione, assicurati che sulla nuova piattaforma siano disponibili gli strumenti di sviluppo e le funzioni middleware o di sistema operativo di supporto necessari. In generale, i sistemi di tipo Linux sono più indicati per supportare le applicazioni meno recenti su versioni più recenti del sistema operativo rispetto a Windows, ma non ci sono garanzie. 

## Quale larghezza di banda ottengo con la mia nuova configurazione ed è alla stessa velocità che ho attualmente?

Ricevi un pacchetto di larghezza di banda attuale che è correlato al massimo al pacchetto di cui disponi attualmente. La velocità per tale pacchetto è uguale a quella inclusa nel pacchetto o alla velocità attuale.

## Come copio i dati dal mio vecchio server a quello nuovo?

Dopo aver stabilito la connettività tra il server vecchio e quello nuovo, devi considerare come spostare i dati tra di essi. Presumendo che disponi di archiviazione a sufficienza nel nuovo server per contenere il volume di dati, una copia diretta da server a server è il modo più semplice per ottenere questo risultato. Ci sono molti strumenti disponibili che puoi utilizzare.  

* scp è una buona scelta per copiare in modo sicuro un file da un'origine a una destinazione. Esegue una semplice copia lineare. 
* Se devi copiare un gran numero di file, rsync su ssh è molto più rapido di scp; rsync copia anche le strutture di directory e conserva le autorizzazioni file.

In generale, devi copiare solo le applicazioni e i dati applicativi tra i sistemi. La copia di versioni meno recenti di file del sistema operativo a una versione più recente può causare dei problemi.

Arresta i database prima di copiarli tra i sistemi per assicurarti che i dati siano congruenti. Quando esegui la migrazione dei dati del database, assicurati che i dati siano migrati in un modo che non limiti le tue opzioni di importarli nel nuovo sistema. Invece di copiare i dati del database da sistema a sistema, considera di esportarli in un formato che ti consente di importarli in un database più recente. File di testo semplici, file CSV ecc. forniscono maggiori opzioni rispetto all'utilizzo di formati file proprietari o chiusi, quando si tratta di spostare i dati tra i sistemi. Verifica sempre i tuoi approcci alla migrazione dei dati su un piccolo insieme di dati di test prima di eseguire la copia ufficiale.

## Devo configurare nuovamente la mia rete sul nuovo sito?

Molto probabilmente la tua rete avrà bisogno di modifiche per funzionare con i nuovi server e il nuovo sito.  Se hai bisogno di aiuto con questo processo, contatta il team di supporto per telefono o chat.

## Cosa devo fare se non ho le competenze per eseguire la migrazione?

La migrazione di applicazioni può essere un compito complesso. Un fattore non secondario sono le competenze necessarie per eseguire tale operazione. Se sono necessarie delle modifiche al codice per l'applicazione, assicurati di avere le competenze di programmazione richieste. Ciò è soprattutto vero con i sistemi meno recenti, dove le competenze disponibili potrebbero essere limitate o dove c'è una carenza di documentazione o conoscenza relative al sistema stesso. Se lo sforzo attuato è significativo e il sistema è di particolare importanza per la tua attività aziendale, considera di investire in servizi a pagamento o altri servizi di migrazione per farti aiutare.

## Come ottengo un aiuto generico con la migrazione?

A seconda del livello di aiuto che ti serve, puoi contattare il supporto per telefono o chat. In alternativa, puoi contattare il nostro team di servizi gestiti per assistenza.

## Come stabilisco il contatto se non ho un account manager?

Puoi contattare il supporto per telefono o chat per qualsiasi tua domanda relativa alla migrazione.
