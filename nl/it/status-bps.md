---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-14"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Procedure consigliate per il monitoraggio dello stato
{: #best-practices}

Per rimanere informato e pianificare di conseguenza, utilizza le seguenti procedure consigliate per monitorare lo stato di {{site.data.keyword.Bluemix}}.
{: shortdesc}

## Controlla le prossime finestre di manutenzione
{: #monbp-checmaintwin}

Controlla le prossime finestre di manutenzione pubblicate nella pagina Dashboard di {{site.data.keyword.Bluemix_notm}}, almeno una volta ogni 24 ore, utilizzando una delle seguenti opzioni:
* Controlla il widget Manutenzione pianificata nel [Dashboard ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com){: new_window}. Fai clic su **Tutti gli eventi** per visualizzare tutte le manutenzioni pianificate.
* Vai direttamente alla pagina [Stato - Manutenzione pianificata ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/status?selected=maintenance){: new_window}

## Controlla le finestre di manutenzione correnti o un incidente in corso
{: #monbp-checcurmaninprog}

Se hai il sospetto che {{site.data.keyword.Bluemix_notm}} non funzioni nel modo previsto, consulta la pagina Stato per controllare le finestre di manutenzione correnti o un incidente in corso. Per segnalare un incidente non ancora elencato nella pagina Stato, apri un caso di supporto facendo clic su **Supporto** dalla barra dei menu. Quindi, fai clic su **Crea nuovo caso** nella scheda Come ottenere supporto.

## Usufruisci di più ubicazioni {{site.data.keyword.Bluemix_notm}}
{: #monbp-multpreg}

Tutti gli utenti di {{site.data.keyword.Bluemix_notm}} hanno automaticamente accesso alle ubicazioni di Dallas, Londra, Francoforte, Sydney, Washington DC e Tokyo. Il team di {{site.data.keyword.Bluemix_notm}} Global Operations gestisce tutte le ubicazioni per evitare impatti sulla manutenzione e ridurre al minimo il rischio di incidenti che influiscano contemporaneamente su tutte le ubicazioni.

Per cambiare le ubicazioni, vai al tuo dashboard ed espandi il menu **UBICAZIONE**.

## Prepararsi a piccole interruzioni
{: #monbp-prepmininter}

Nella maggior parte dei casi, si può continuare a utilizzare {{site.data.keyword.Bluemix_notm}}
normalmente, anche durante la finestra di manutenzione. Tuttavia, non è sempre possibile evitare delle brevi interruzioni di servizio. In genere, le applicazioni in esecuzione rimangono disponibili anche se le funzioni
di gestione applicazione di {{site.data.keyword.Bluemix_notm}},
come l'avvio o l'arresto di applicazioni, vengono temporaneamente interrotte. Per
massimizzare la disponibilità delle tue applicazioni in esecuzione, esegui almeno
tre istanze di ciascuna applicazione.

## Sottoscrizione alle notifiche email

Se sei il proprietario di un account Lite, puoi scegliere se ricevere notifiche email sugli eventi non pianificati della piattaforma {{site.data.keyword.Bluemix_notm}}, come le interruzioni, e sugli eventi pianificati, come la manutenzione. Inoltre, se hai un account Pagamento a consumo o Sottoscrizione, puoi scegliere se ricevere notifiche email dell'infrastruttura {{site.data.keyword.Bluemix_notm}} sugli eventi non pianificati, la manutenzione e gli annunci. Per ulteriori informazioni, vedi [Impostazione delle preferenze email](/docs/account/email.html).



