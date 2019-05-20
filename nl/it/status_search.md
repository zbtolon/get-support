---

copyright:

  years: 2018,2019

lastupdated: "2019-05-13"

keywords: status page, status query

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# Ricerca avanzata dello stato
{: #adv-search}

Puoi eseguire ricerche in tutte le schede della pagina Stato, ma sapevi che puoi creare valori di ricerca degli URL utilizzando parametri di query dall'esterno della console?
{:shortdesc}

Il seguente elenco include esempi di opzioni di ricerca URL:

* Caricare la pagina con la scheda Stato selezionata: `console.cloud.ibm.com/status?selected=status`
* Caricare la pagina con la scheda Manutenzione pianificata selezionata: `console.cloud.ibm.com/status?selected=maintenance`
* Caricare la pagina con la scheda Bollettino di sicurezza selezionata: `console.cloud.ibm.com/status?selected=security`
* Caricare la pagina con la scheda Annunci selezionata: `console.cloud.ibm.com/status?selected=announcement`
* Caricare la pagina con una query di ricerca immessa: `console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* Indirizzare alla pagina con i filtri selezionati. Ad esempio, puoi impostare l'ubicazione geografica su Nord America utilizzando la seguente ricerca URL: `console.cloud.ibm.com/status?selected=status&region=na`

* Utilizza identificativi di notifica univoci come parametro di ricerca per accedere direttamente ai dettagli della notifica.  Ad esempio, `query=INC1000001` identifica gli elementi con ID: `INC1000001`. In questo esempio, `INC1000001` è il numero del caso per una notifica di manutenzione.

### Filtri di query URL:
{: #url-query}

| Parametro di query URL | Descrizione | Valori |
| ----- | ----- | ----- | ----- |
| `?type` | Un filtro che si applica solo alla scheda Stato. Utilizza la query `?type` per filtrare la pagina Stato per incidenti o manutenzione. | `=incident`, `=maintenance` |
| `?region` | Filtra la pagina per ubicazione geografica.  | `=na`, `=eu`, `=sa`, `=ap` |
| `?component` | Filtra la pagina per componenti {{site.data.keyword.Bluemix_notm}}. Ad esempio, puoi filtrare in base al servizio a cui sei interessato. |Si applica alla maggior parte degli ID di catalogo globale; ad esempio, `?component=iotf-service` filtra la pagina e mostra gli eventi che interessano la piattaforma Internet of Things |
{: caption="Tabella 1. Filtri di query URL" caption-side="top"}

Puoi sempre utilizzare i filtri **Filtra per** e quindi copiare o aggiungere ai preferiti la query URL che viene generata. I filtri sono visualizzati nel tuo URL e possono aiutarti a creare query future.
{: tip}
