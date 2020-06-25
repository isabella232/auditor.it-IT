---
description: 'null'
seo-description: 'null'
seo-title: Domande frequenti su Auditor
title: Domande frequenti su Auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: ht
source-git-commit: 631656ed4442f7f0083b1c99a725328a1c51ff9f
workflow-type: ht
source-wordcount: '938'
ht-degree: 100%

---


# Domande frequenti su Auditor {#auditor-faq}

Questo articolo contiene le risposte alle domande frequenti su Adobe Experience Platform Auditor.

* [Cos’è Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [La mia azienda può usare Auditor?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Quali tecnologie Adobe sono valutate da Auditor?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Quanti controlli di audit posso eseguire?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [Su cosa viene eseguito il crawling durante un controllo di audit?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Quanto tempo ci vuole per eseguire un controllo di audit?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Quali informazioni vengono fornite in un rapporto?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [In che misura sono utilizzabili quelle informazioni?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Auditor può controllare la tecnologia non Adobe?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Posso approvare i miei indirizzi IP per consentire la scansione di pagine?](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Auditor utilizza gli stessi intervalli IP di ObservePoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Cos’è Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Auditor è un servizio di Adobe Experience Cloud che è stato co-sviluppato con ObservePoint, esperti nella convalida delle implementazioni digitali.

Con Auditor, i clienti possono scansionare fino a 500 pagine web alla volta e ricevere un rapporto che mostra come migliorare le loro implementazioni Adobe Experience Cloud in modo da ottenere il valore completo del loro investimento Adobe.

## Posso utilizzare Auditor? {#section-f90094050d1e44929066a942833435cf}

A tutte le organizzazioni dei clienti Adobe Experience Cloud è concesso l’accesso gratuito ad Auditor (dal 1° maggio 2018). Ogni utente deve accettare i termini di utilizzo di Adobe/ObservePoint nell’interfaccia utente di Adobe Experience Cloud prima di accedere alla funzionalità. Per rifiutare, contatta il tuo Account Manager.

## Come posso accedere ad Auditor? {#section-531ff85f94384831a89cbb4109549daf}

Dopo aver effettuato l’accesso a [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), per trovare Auditor fai clic su **[!UICONTROL Activation]** nella navigazione superiore. Puoi anche accedere direttamente a [https://auditor.adobe.com](https://auditor.adobe.com).

## Quali tecnologie Adobe sono valutate da Auditor? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Servizio Experience Cloud ID (ex servizio Marketing Cloud ID)
* Target

Le seguenti soluzioni Adobe non sono attualmente incluse nella categoria di test. Il supporto per queste soluzioni è pianificato per gli aggiornamenti futuri.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## Quanti controlli di audit posso eseguire? {#section-caac1e50ce1249aeba76308f3ef03fa0}

Non esiste alcun limite al numero di controlli di audit che è possibile eseguire. Gli utenti possono eseguire un solo controllo di audit alla volta. Se si tenta di avviare un controllo di audit con le stesse impostazioni di quello in esecuzione, si verifica un errore.

## Su cosa viene eseguito il crawling durante un controllo di audit? {#section-6d068ed69ece4a1bb6d0c34454550c45}

La tecnologia ObservePoint esegue il crawling degli URL che si trovano nei collegamenti dei documenti. Non viene eseguito il crawling su collegamenti presenti in pulsanti, widget di impaginazione e altri elementi di pagina di questo tipo.

## Come suggerisco nuovi criteri per i test di Auditor? {#section-926e6ef9225b4f0bb19c2927d634cd77}

Per inviare i suggerimenti del test tramite la community di Auditor, fai clic su **[!UICONTROL Share Feedback]** (Condividi feedback) in questa pagina: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Quanto tempo ci vuole per eseguire un controllo di audit? {#section-5086ae27ef1f4671a9d951348654633a}

Esistono molti fattori che contribuiscono al tempo necessario per completare un controllo di audit, tra cui:

* Tempo di caricamento della pagina

   Il motore ObservePoint carica ogni pagina del controllo di audit in un browser. Più velocemente viene caricata una pagina, più veloce sarà il completamento del controllo di audit.
* Connessioni simultanee

   Adobe Auditor utilizza una singola connessione per visitare ogni pagina. Gli account ObservePoint completi utilizzano fino a 10 motori alla volta.
* Silenzio rete

   Dopo il caricamento di ogni pagina, il controllo di audit attende un silenzio di rete di sette secondi prima di procedere alla pagina successiva. Se una pagina invia molte richieste di rete che si verificano dopo il caricamento della pagina, l’attesa si interrompe dopo 60 secondi.
* Tentativi pagina

   Se non è possibile trovare una pagina o un tag, il controllo di audit memorizza tale URL e vi ritorna successivamente nel controllo di audit. Il controllo di audit visiterà una pagina fino a tre volte per assicurarsi che l’errore non sia stato causato da un problema transitorio.
* Elaborazione

   Dopo l’esecuzione di un controllo di audit, tutti i dati raccolti vengono elaborati e filtrati attraverso le regole. Questo tempo di elaborazione è significativo, anche se non richiede tanto tempo quanto la scansione stessa.

>[!NOTE]
>
>Adobe Auditor esegue una sola scansione alla volta. Gli account ObservePoint completi possono eseguire molti controlli di audit consecutivamente.

## Quali informazioni vengono fornite in un rapporto? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Ogni analisi genera un rapporto che mostra gli URL analizzati, i problemi riscontrati in tali pagine web e raccomandazioni su come correggere i problemi rilevati.

I risultati delle scansioni sono suddivisi in tre categorie:

* Configurazione
* Coerenza tag
* Presenza tag

Oltre a queste tre categorie, il rapporto fornisce avvisi contenenti informazioni di cui dovresti essere a conoscenza ma che non richiedono necessariamente un’azione immediata.

Le raccomandazioni che rientrano in queste categorie sono quindi suddivise in tre categorie aggiuntive:

* Altamente consigliato
* Consigliato
* Superato

## In che misura sono utilizzabili quelle informazioni? {#section-9308c1ea882048b781087ae6d2eee9f0}

Tutte le raccomandazioni fornite tramite Auditor sono volte ad aiutarti a risolvere un problema relativo all’implementazione delle soluzioni Adobe Experience Cloud, come DTM o Target. Per facilitare questa fase, il team di Auditor ha lavorato a lungo per fornire istruzioni molto dettagliate su cosa occorre fare dove. Puoi esportare un foglio di calcolo contenente tutti gli URL analizzati e tutti i risultati del test in modo da individuare facilmente le aree problematiche. Esempio di una raccomandazione per un’implementazione DTM:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom callback last</b> </p> <p>Per una corretta implementazione DTM è necessaria una funzione _satellite.pageBottom(). Aggiungi lo script in linea immediatamente prima del tag &lt;/body&gt; di chiusura per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Auditor può controllare la tecnologia non Adobe? {#section-f6e73c56083b4815bbf901296038bcd4}

No. Tuttavia, l’offerta completa di ObservePoint consente ai clienti di controllare e monitorare tutti i tag e le tecnologie di marketing. Come cliente Adobe puoi accedere a un account di prova gratuito. Per accedere al tuo account di prova visita la pagina [Auditor di ObservePoint](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## Posso approvare i miei indirizzi IP per consentire la scansione di pagine protette da un login? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Questa funzionalità non è attualmente supportata senza l’offerta completa ObservePoint.

## Auditor utilizza gli stessi intervalli IP di ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

La ricerca per indicizzazione viene eseguita da ObservePoint, quindi vengono utilizzati gli stessi indirizzi IP.

Per ulteriori informazioni, consulta la [documentazione di ObservePoint](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list).
