---
description: 'null'
seo-description: 'null'
seo-title: Prova punto 1.0.1
title: Prova punto 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
translation-type: tm+mt
source-git-commit: 712d0768e5e5394372293bf8231c91489519bcd1

---


# Prova punto 1.0.1{#test-rubric}

## Prova punto 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## Avvisi {#alerts}

Questo riferimento fornisce ulteriori informazioni sugli avvisi visualizzati da Auditor per i test.

Gli avvisi mostrano problemi di cui dovreste essere a conoscenza, ma che non influiscono sulla valutazione. Si tratta di consigli sulle best practice che, in alcuni casi, potrebbero non essere applicabili all&#39;implementazione.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
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
    </draft-comment> <p><b>Advertising Cloud - Correggi tag di conversione implementato</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Verificare se viene utilizzato il tag di conversione corretto. </p> <p> <p>Avviso:  L'utilizzo di tag di conversione TubeMogul obsoleti può causare la perdita di dati. </p> </p> </td> 
   <td colname="col3"> <p>Aggiorna i pixel di conversione ai nuovi tag di conversione solo immagini di Advertising Cloud. </p> <p>Questa operazione può essere realizzata con la massima facilità con l'estensione Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Correggi il tag JS utilizzato</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud dovrebbe utilizzare i tag JavaScript più recenti. </p> </td> 
   <td colname="col3"> <p>Aggiorna il tuo JavaScript di Advertising Cloud alla versione più recente. L'utilizzo di versioni JavaScript obsolete può comportare la perdita di funzionalità. </p> <p>Questo può essere ottenuto più facilmente tramite l'utilizzo dell'estensione di lancio di Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Tag solo immagine</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Il formato pixel immagine di Advertising Cloud deve corrispondere a uno dei seguenti formati consigliati: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Aggiornate i pixel di Advertising Cloud ai nuovi tag di sola immagine di Advertising Cloud, in modo da poter sfruttare appieno la funzionalità di Advertising Cloud. </p> <p>Questa operazione può essere realizzata con la massima facilità con l'estensione Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Segmento Pixel Sincronizzazione DSP Abilitata</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Verificate se il pixel del segmento TubeMogul contiene un'impostazione di sincronizzazione DSP e consigliate di aggiungere l'impostazione al pixel. </p> <p>L'impostazione di sincronizzazione DSP è determinata dall'utilizzo di un parametro di stringa di query, in modo che </p> <p>SE il tag viene inviato<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>E il tag contiene il parametro URL <span class="codeph"> "sid=")</span> </p> <p>VERIFICATE QUINDI se esiste il parametro URL <span class="codeph"> "cs=0"</span> o<span class="codeph"> "cs=1"</span> e, in caso contrario, <span class="codeph"> "cs=1"</span> da aggiungere a tali pixel in modo che le percentuali di corrispondenza dell’audience possano migliorare. </p> </td> 
   <td colname="col3"> <p> Aggiungete il parametro URL <span class="codeph"> "cs=1"</span> ai pixel di Advertising Cloud in modo che possa verificarsi la sincronizzazione DSP, che aumenta le percentuali di corrispondenza del pubblico. </p> <p>Questo può essere facilmente realizzato con l'estensione Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - posizione callback pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Gestione tag dinamica richiede la funzione <span class="codeph"> _satellite.pageBottom()</span> . Aggiungete lo script in linea immediatamente prima del tag body di chiusura per garantire la funzionalità DTM corretta. </p> <p> <p>Nota: È consigliabile che il tag sia l' <i>ultimo</i> tag presente in <span class="codeph"> &lt;body&gt;</span>. Se si trova all'interno del tag <span class="codeph"> &lt;body&gt;</span> , ha la possibilità di funzionare, ma non è la migliore prassi, potrebbe funzionare in modo errato o con risultati indesiderati. </p> </p> </td> 
   <td colname="col3"> <p>Aggiungete lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Self-Hosted</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> La libreria DTM è in hosting sull'istanza di Adobe Akamai all'indirizzo <span class="filepath"> assets.adobedtm.com</span>. </p> <p> L'hosting autonomo è l'approccio consigliato per il caricamento di Gestione dinamica dei tag in quanto fornisce un maggiore controllo delle prestazioni del sito Web attraverso il controllo della cache, riducendo le dipendenze degli script di terze parti e un maggiore controllo del processo di pubblicazione. Le librerie DTM possono essere ospitate e gestite tramite il vostro hosting Web o CDN. </p> </td> 
   <td colname="col3"> <p>L'hosting autonomo è l'approccio consigliato per caricare Gestione dinamica dei tag su una pagina. Sebbene l'hosting di Gestione dinamica dei tag tramite la rete CDN Akamai funzioni nella maggior parte dei casi, l'hosting autonomo migliora le prestazioni della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Servizio Experience Cloud ID - Utilizza un solo AdobeOrg</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>In una normale implementazione MCID, deve essere utilizzato un solo AdobeOrg. </p> </td> 
   <td colname="col3"> <p>Verifica l’esistenza di più ID AdobeOrg per questa implementazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - pageBottom, posizionamento callback</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Se distribuita in modo sincrono, Launch deve avere una funzione di <span class="codeph"> callback </span>Bottom definita per ultima nel corpo della pagina </p> <p> <p>Nota: È consigliabile che il tag sia l' <i>ultimo</i> tag presente in <span class="codeph"> &lt;body&gt;</span>. Se si trova all'interno del tag <span class="codeph"> &lt;body&gt;</span> , ha la possibilità di funzionare, ma non è la migliore prassi, potrebbe funzionare in modo errato o con risultati indesiderati. </p> </p> </td> 
   <td colname="col3"> <p>Aggiungete lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - Self-Hosted</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>La libreria Launch è ospitata nell'istanza di Adobe Akamai all'indirizzo <span class="filepath"> assets.adobedtm.com</span>. </p> <p>L'hosting autonomo è l'approccio consigliato per il caricamento di Launch perché fornisce un maggiore controllo delle prestazioni del sito Web attraverso il controllo della cache, la riduzione delle dipendenze degli script di terze parti e un maggiore controllo del processo di pubblicazione. Le librerie Launch possono essere ospitate e gestite tramite il proprio hosting Web o CDN. </p> </td> 
   <td colname="col3"> <p>Sebbene l'hosting di Launch tramite la rete CDN di Akamai funzioni nella maggior parte dei casi, si consiglia di implementare l'hosting autonomo come primo passo per migliorare le prestazioni della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - Deve essere distribuito in modo asincrono</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Launch deve essere distribuito in modo asincrono per ottenere prestazioni ottimali. </p> </td> 
   <td colname="col3"> <p>Includere il parametro asincrono nello script in linea per garantire la funzionalità di avvio asincrono corretta </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Content in mboxDefault</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il contenuto dovrebbe essere presente in mboxDefault quando si utilizza at.js. </p> </td> 
   <td colname="col3"> <p>Verificate che il contenuto sia disponibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Configurazione {#configuration}

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
    </draft-comment> <p><b>Avvia - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
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

## Uniformità tag {#tag-consistency}

Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor per la coerenza dei tag.

I test di coerenza di Auditor rilevano incoerenze tra tutte le pagine digitalizzate. Si tratta di valori o configurazioni che devono essere identici in tutte le pagine del sito per garantire una raccolta accurata dei dati.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
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
    </draft-comment> <p><b>Analytics - Versione codice coerente </b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/choose-implementation-method.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> È stata trovata più di una versione del codice Analytics. </p> </td> 
   <td colname="col3"> <p>Sostituisci tutte le istanze di Analytics con la versione corrente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Presenza di tag {#tag-presence}

Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor per la presenza di tag.

Auditor valuta se il tag esiste e se si trova nella posizione giusta nel codice della pagina.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
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
    </draft-comment> <p><b>Advertising Cloud - Presenza codice</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Il tag Advertising Cloud non è disponibile nel DOM. </p> </td> 
   <td colname="col3"> <p>Implementate il tag Advertising Cloud utilizzando l'estensione Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Pixel di segmento implementati</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Aggiorna i pixel del segmento di Advertising Cloud ai nuovi tag di sola immagine di Advertising Cloud. L'utilizzo di tag di segmento AMO obsoleti può causare la perdita di dati. </p> </td> 
   <td colname="col3"> <p>Implementa il pixel del segmento di Advertising Cloud utilizzando l’estensione di lancio di Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Caricato nel DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il tag Adobe Analytics non è stato rilevato. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente di Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Libreria caricata</b> </p> <p>Peso: 5 </p> <p>Informazioni aggiuntive: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/c_Troubleshooting.html" format="html" scope="external"> Risoluzione dei problemi DTM</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Aggiunta di codice intestazione e piè di pagina</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare un oggetto _satellite globale nel DOM. Gestione tag dinamica non installata o non eseguita. </p> </td> 
   <td colname="col3"> <p>Verifica che la libreria DTM sia implementata sulla pagina e non sia bloccata dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Un codice da incorporare</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> I siti di produzione devono caricare solo una libreria DTM. </p> </td> 
   <td colname="col3"> <p>Verificate che sulla pagina venga caricata solo la libreria di produzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - il callback pageBottom esiste in &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il callback <span class="codeph"> _satellite.pageBottom()</span> non è stato trovato all'interno del <span class="codeph"> &lt;body&gt;</span> della pagina, richiesto da Gestione tag dinamica. </p> <p>Il test ha esito negativo se la <span class="codeph"> chiamata </span>pageBottom non viene trovata nella pagina o se si trova nel tag <span class="codeph"> &lt;head&gt;</span> (o in un'altra posizione imprevista). Passerà solo se <span class="codeph"> pageBottom</span> viene trovato in qualche punto all'interno del tag <span class="codeph"> &lt;body&gt;</span> . Se non è sulla pagina, non funzionerà e anche gli altri due test <span class="codeph"> PageBottom</span> non funzioneranno. </p> </td> 
   <td colname="col3"> <p>Aggiungete lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - tag pageBottom attivato</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il tag pageBottom <span class="codeph"></span> DTM non è stato rilevato. </p> <p>Ciò potrebbe verificarsi se la chiamata si trova all'interno di un'istruzione <span class="codeph"> if</span> che restituisce un risultato simile a <span class="codeph"> if (false) {_satellite.pageBottom()}</span>. Quindi, anche se potrebbe esistere e essere posizionato correttamente, l'etichetta potrebbe non essere attivata. </p> </td> 
   <td colname="col3"> <p>Installa la chiamata DTM <span class="codeph"> pageBottom</span> su ogni pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servizio Experience Cloud ID - Presenza del codice</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-overview.htmlimplementation-guides.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Codice del servizio Experience Cloud ID non trovato. L’Experience Cloud ID (MCID) è fortemente consigliato per consentirti di ottenere il massimo valore dalle soluzioni Experience Cloud ed è fondamentale per la gestione ID nelle soluzioni Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Installa la versione più recente di MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servizio Experience Cloud ID - Presenza dei cookie</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-implementation-guides.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare il cookie <span class="codeph"> AMCV_</span> . Devi creare un'istanza di un oggetto visitatore dal codice <span class="codeph"> VisitorAPI.js</span> . </p> </td> 
   <td colname="col3"> <p> Se si tratta di un’implementazione DTM, verifica che l’ID AdobeOrg sia stato immesso correttamente nello strumento MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servizio Experience Cloud ID - Valore MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_cookies.html#concept_37156268512445F287CD4BBB2839FFAA__section_C55AF54828DC4CCE89F6118655D694C8" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il valore MID non è stato trovato nel cookie <span class="codeph"> AMCV_</span> . </p> </td> 
   <td colname="col3"> <p>Eseguite di nuovo il test per verificare eventuali latenze API MCID. Se la condizione persiste, contatta l’Assistenza clienti Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Launch - Libreria caricata</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare un oggetto _satellite globale nel DOM. Launch non è installato o non è in grado di eseguire. </p> </td> 
   <td colname="col3"> <p>Verificare che la libreria Launch sia implementata sulla pagina e che non sia bloccata dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Avvio - Non sono presenti più script da incorporare</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Sulla pagina non devono essere caricati più script da incorporare. I siti di produzione devono caricare una sola libreria Launch. </p> </td> 
   <td colname="col3"> <p>Verificate che sulla pagina venga caricata solo la libreria di produzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - pageBottom callback esiste in &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il callback <span class="codeph"> _satellite.pageBottom()</span> non è stato trovato all'interno del <span class="codeph"> &lt;body&gt;</span> della pagina, richiesto da Launch. </p> <p>Il test ha esito negativo se la <span class="codeph"> chiamata </span>pageBottom non viene trovata nella pagina o se si trova nel tag <span class="codeph"> &lt;head&gt;</span> (o in un'altra posizione imprevista). Passerà solo se <span class="codeph"> pageBottom</span> viene trovato in qualche punto all'interno del tag <span class="codeph"> &lt;body&gt;</span> . Se non è sulla pagina, non funzionerà e anche gli altri due test <span class="codeph"> PageBottom</span> non funzioneranno. </p> </td> 
   <td colname="col3"> <p>Aggiungete lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la corretta funzionalità di Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - pageBottom il callback non deve esistere quando viene distribuito in modo asincrono</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Il callback <span class="codeph"> _satellite.pageBottom()</span> è stato trovato sulla pagina, il che non dovrebbe essere vero se Launch è distribuito in modo asincrono. </p> </td> 
   <td colname="col3"> <p>Rimuovete lo<span class="codeph"> script _satellite.pageBottom()</span> per abilitare la funzionalità Launch corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Presenza di codice</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Target deve essere definito nel DOM. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente di Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Libreria caricata in &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> 
    <draft-comment>
      TE61c380082a4b4706b28a84aa047599a7 
    </draft-comment> </td> 
   <td colname="col2"> <p> La libreria Target deve essere caricata nel tag <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
   <td colname="col3"> <p> Verificate che la libreria Target sia caricata nel tag <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

