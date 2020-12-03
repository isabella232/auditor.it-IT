---
description: Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Adobe Experience Platform Auditor per la configurazione.
seo-description: Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Adobe Experience Platform Auditor per la configurazione.
seo-title: Configurazione
title: Configurazione
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 100%

---


# Configurazione

Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Adobe Experience Platform Auditor per la configurazione.

I test di configurazione eseguono la ricerca di impostazioni, valori o potenziali conflitti specifici nell’implementazione. Platform Auditor valuta i tag rispetto ad altre regole e best practice consigliate.

<table id="table_A8A1FC360482447185C8460A18426638"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Criteri </th> 
   <th colname="col3" class="entry"> Consiglio </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - I nomi di conversione utilizzano solo caratteri alfanumerici</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p>Il parametro <span class="codeph"> ev_conversion_property_name</span> deve contenere solo valori numerici e decimali ECCETTO per il parametro "<span class="codeph"> ev_transid</span>" (il valore <span class="codeph"> ev_transid</span> può contenere valori di testo o numerici) </p> <p>Cerca i pixel <span class="codeph"> everesttech.net</span> che contengono un parametro URL che inizia con <span class="codeph"> ev_</span>. </p> <p>Esempio: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Assicurati che i parametri delle proprietà della transazione contengano solo valori numerici e decimali. </p> <p> <p>Avviso: qualsiasi altro tipo di valore potrebbe causare la perdita di dati. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - I nomi di conversione usano caratteri URL-safe</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p> I nomi delle proprietà di conversione non devono contenere una e commerciale o un punto interrogativo. </p> <p> Esempio: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Assicurati che i parametri della proprietà della transazione non contengano una e commerciale o un punto interrogativo non codificati. Interrompono il formato URL. </p> <p> <p>Avviso: parametri di proprietà che contengono una e commerciale o un punto interrogativo non codificati (ad esempio: <span class="codeph"> ev_formComplete?=1</span> o <span class="codeph"> ev_formComplete&amp;Submit=1</span>), potrebbero causare una perdita di dati. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - ID transazione implementato correttamente</b> </p> <p>Peso: 1 </p> </td> 
   <td colname="col2"> <p> Il nome della proprietà <span class="codeph"> ev_transid=</span> non deve essere vuoto. </p> <p>Esempio: </p> <p> <span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Il nome della proprietà <span class="codeph"> ev_transid=</span> deve necessariamente contenere un valore (<span class="codeph"> ev_transid=</span>). Se lasciato senza valori, potrebbe verificarsi una perdita di dati della transazione. Assegna un valore a <span class="codeph"> ev_transid=</span> o rimuovi il parametro dal pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Istanziato in DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/home.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il codice Adobe Analytics non è installato o l’esecuzione non è riuscita. Restituisce 0 se non viene trovato alcun codice Analytics nella pagina web. </p> </td> 
   <td colname="col3"> <p>Verifica che il tag Analytics sia implementato nella pagina e non sia bloccato dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Istanziato una volta</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/home.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il codice Adobe Analytics è stato rilevato più di una volta nella pagina. Restituisce 0 se non viene trovato alcun codice Analytics nella pagina web. </p> </td> 
   <td colname="col3"> <p>Accertati che nella pagina sia presente un solo tag Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Ultima versione</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria di codici di Analytics. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. Restituisce 0 se non viene trovato alcun codice Analytics nella pagina web. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente della libreria Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - I tag di terze parti vengono caricati in modo asincrono dopo l’evento DOM ready</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/resources/load-order.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Per trovare un compromesso tra una buona esperienza utente e la raccolta di dati accurati, i tag di terze parti dovrebbero essere attivati durante l’evento DOM ready. In questo modo gli script di tracciamento verranno eseguiti senza influire sulle funzionalità del sito. </p> </td> 
   <td colname="col3"> <p>Per risolvere questo problema, modifica tutte le regole che eseguono pixel di terze parti in modo che vengano attivate in corrispondenza dell’evento DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servizio Experience Cloud ID - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/tools/macid.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria di codici del servizio Visitor ID, <span class="codeph"> visitorAPI.js</span>. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente della libreria del servizio Visitor ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Nelle pagine non è in esecuzione la versione più recente della libreria di codici di Platform Launch (Turbine). Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p> Aggiorna la libreria Platform Launch generando e pubblicando nuovamente la libreria Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/implementing/target/update-target-tool.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria di codici di Target. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente della libreria Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - mboxDefault precede mboxCreate </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/target/using/implement-target/client-side/mbox-implement/mbox-download.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>L’utilizzo corretto di <span class="codeph"> mboxCreate</span> è simile al seguente: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Accertati di includere un tag <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> prima di richiamare <span class="codeph"> mboxCreate()</span>. at.js non ne aggiungerà uno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - DOCTYPE valido</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/help/it-IT/target/using/implement-target/client-side/faq-at-js/target-atjs-faq.html#what-html-doctype-does-atjs-require" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> È stato rilevato un DOCTYPE non valido. In questo scenario non verrà attivata alcuna mbox. </p> <p>Per at.js, il DOCTYPE deve essere in modalità Standard oppure Target non funzionerà. </p> </td> 
   <td colname="col3"> <p>Aggiorna il DOCTYPE nella pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

