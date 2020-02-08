---
description: Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor per la configurazione.
seo-description: Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor per la configurazione.
seo-title: Configurazione
title: Configurazione
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Configurazione

Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor per la configurazione.

I test di configurazione eseguono la ricerca di impostazioni, valori o potenziali conflitti specifici nell&#39;implementazione. Auditor valuta i tag rispetto ad altre regole e procedure ottimali consigliate.

<table id="table_A8A1FC360482447185C8460A18426638"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Prova </th> 
   <th colname="col2" class="entry"> Criteri </th> 
   <th colname="col3" class="entry"> Consiglio </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - I nomi di conversione utilizzano solo caratteri alfanumerici</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p>Il parametro <span class="codeph"> ev_conversion_property_name</span> deve contenere solo valori numerici e decimali EXCEPT per il parametro "<span class="codeph"> ev_transid</span>" (il valore <span class="codeph"> ev_transid</span> può contenere valori di testo o numerici) </p> <p>Cercate <span class="codeph"> everesttech.net</span> pixel che contengono un parametro URL a partire da <span class="codeph"> ev_</span>. </p> <p>Esempio: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Assicurarsi che i parametri delle proprietà della transazione contengano solo valori numerici e decimali. </p> <p> <p>Avviso:  Qualsiasi altro tipo di valore potrebbe causare la perdita di dati. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - I nomi di conversione usano caratteri URL-safe</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p> I nomi delle proprietà di conversione non devono contenere una e-mail o un punto interrogativo. </p> <p> Esempio: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Assicurati che i parametri della proprietà della transazione non contengano una e-mail o un punto interrogativo non codificati. Interrompono il formato URL. </p> <p> <p>Avviso: Parametri di proprietà contenenti una e-mail non codificata o un punto interrogativo (ad esempio: <span class="codeph"> ev_formComplete?=1</span> o <span class="codeph"> ev_formComplete&amp;Submit=1</span>), potrebbe causare una perdita di dati. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - ID transazione correttamente implementato</b> </p> <p>Peso: 1 </p> </td> 
   <td colname="col2"> <p> Il nome della proprietà <span class="codeph"> ev_transid=</span> non deve essere vuoto. </p> <p>Esempio: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Il nome della proprietà <span class="codeph"> ev_transid=</span> non deve essere lasciato senza un valore (<span class="codeph"> ev_transid=</span>). Se questo viene lasciato senza un valore, potrebbe verificarsi una perdita di dati della transazione. Assegnate un valore a <span class="codeph"> ev_transid=</span> o rimuovete il parametro dal pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Instanziata in DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il codice Adobe Analytics non è installato o non riesce a essere eseguito. Restituisce 0 se non viene trovato alcun codice di analisi sulla pagina Web. </p> </td> 
   <td colname="col3"> <p>Verifica che il tag Analytics sia implementato sulla pagina e non sia bloccato dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Crea un'istanza una volta</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il codice Adobe Analytics è stato rilevato più di una volta sulla pagina. . Restituisce 0 se non viene trovato alcun codice di analisi sulla pagina Web. </p> </td> 
   <td colname="col3"> <p>Accertatevi che sulla pagina sia presente un solo tag Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Ultima versione</b> </p> <p>Peso: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria dei codici di Analytics. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. Restituisce 0 se non viene trovato alcun codice di analisi sulla pagina Web. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente della libreria Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - I tag di terze parti vengono caricati in modo asincrono dopo la preparazione del DOM</b> </p> <p>Peso: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Per trovare un compromesso tra una buona esperienza utente e la raccolta di dati accurati, i tag di terze parti dovrebbero essere attivati a livello DOM. In questo modo gli script di tracciamento verranno eseguiti senza influire sulle funzionalità del sito. </p> </td> 
   <td colname="col3"> <p>Per risolvere questo problema, regolate tutte le regole che eseguono pixel di terze parti in modo che vengano attivate in corrispondenza di DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servizio Experience Cloud ID - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria del codice del servizio ID visitatori, <span class="codeph"> visitorAPI.js</span>. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente della libreria del servizio ID visitatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Avvia - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>In queste pagine non è in esecuzione la versione più recente della libreria dei codici Launch (turbina). Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p> Aggiornate la libreria Launch generando e pubblicando nuovamente la libreria Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria di codici di Target. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p>Installate la versione più recente della libreria Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - mboxDefault precede mboxCreate </b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>L'utilizzo corretto di <span class="codeph"> mboxCreate</span> è simile al seguente: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Contenuto cliente—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Accertatevi di includere un tag <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> prima di richiamare <span class="codeph"> mboxCreate()</span>. at.js non ne aggiungerà uno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - DOCTYPE valido</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> È stato rilevato un DOCTYPE non valido. In questo scenario non verrà attivata alcuna mbox. </p> <p>Per at.js, il DOCTYPE deve essere in modalità Standard oppure Target non funzionerà. </p> </td> 
   <td colname="col3"> <p>Aggiornare il DOCTYPE sulla pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

