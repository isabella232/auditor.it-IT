---
description: Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor per la presenza di tag.
seo-description: Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor per la presenza di tag.
seo-title: Presenza di tag
title: Presenza di tag
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Presenza di tag

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
   <td colname="col1"> <p><b>Advertising Cloud - Presenza codice</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Il tag Advertising Cloud non è disponibile nel DOM. </p> </td> 
   <td colname="col3"> <p>Implementate il tag Advertising Cloud utilizzando l'estensione Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Pixel di segmento implementati</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Aggiorna i pixel del segmento di Advertising Cloud ai nuovi tag di sola immagine di Advertising Cloud. L'utilizzo di tag di segmento AMO obsoleti può causare la perdita di dati. </p> </td> 
   <td colname="col3"> <p>Implementa il pixel del segmento di Advertising Cloud utilizzando l’estensione di lancio di Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics - Caricato nel DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il tag Adobe Analytics non è stato rilevato. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente di Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Libreria caricata</b> </p> <p>Peso: 5 </p> <p>Informazioni aggiuntive: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Risoluzione dei problemi DTM</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aggiunta di codice intestazione e piè di pagina</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare un oggetto _satellite globale nel DOM. Gestione tag dinamica non installata o non eseguita. </p> </td> 
   <td colname="col3"> <p>Verifica che la libreria DTM sia implementata sulla pagina e non sia bloccata dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Un codice da incorporare</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> I siti di produzione devono caricare solo una libreria DTM. </p> </td> 
   <td colname="col3"> <p>Verificate che sulla pagina venga caricata solo la libreria di produzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - il callback pageBottom esiste in &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il callback <span class="codeph"> _satellite.pageBottom()</span> non è stato trovato all'interno del <span class="codeph"> &lt;body&gt;</span> della pagina, richiesto da Gestione tag dinamica. </p> <p>Il test ha esito negativo se la <span class="codeph"> chiamata </span>pageBottom non viene trovata nella pagina o se si trova nel tag <span class="codeph"> &lt;head&gt;</span> (o in un'altra posizione imprevista). Passerà solo se <span class="codeph"> pageBottom</span> viene trovato in qualche punto all'interno del tag <span class="codeph"> &lt;body&gt;</span> . Se non è sulla pagina, non funzionerà e anche gli altri due test <span class="codeph"> PageBottom</span> non funzioneranno. </p> </td> 
   <td colname="col3"> <p>Aggiungete lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - tag pageBottom attivato</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il tag DTM <code> pageBottom</code> non è stato rilevato. </p> <p>Ciò potrebbe verificarsi se la chiamata si trova all'interno di un' <code> if</code> istruzione che restituisce un risultato simile a <code> if (false) {_satellite.pageBottom()}</code>. Quindi, anche se potrebbe esistere e essere posizionato correttamente, l'etichetta potrebbe non essere attivata. </p> </td> 
   <td colname="col3"> <p>Installa la chiamata DTM <code> pageBottom</code> su ogni pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servizio Experience Cloud ID - Presenza del codice</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Codice del servizio Experience Cloud ID non trovato. L’Experience Cloud ID (MCID) è fortemente consigliato per consentirti di ottenere il massimo valore dalle soluzioni Experience Cloud ed è fondamentale per la gestione ID nelle soluzioni Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Installa la versione più recente di MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servizio Experience Cloud ID - Presenza dei cookie</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare il cookie <span class="codeph"> AMCV_</span> . Devi creare un'istanza di un oggetto visitatore dal codice <span class="codeph"> VisitorAPI.js</span> . </p> </td> 
   <td colname="col3"> <p> Se si tratta di un’implementazione DTM, verifica che l’ID AdobeOrg sia stato immesso correttamente nello strumento MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servizio Experience Cloud ID - Valore MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il valore MID non è stato trovato nel cookie <span class="codeph"> AMCV_</span> . </p> </td> 
   <td colname="col3"> <p>Eseguite di nuovo il test per verificare eventuali latenze API MCID. Se la condizione persiste, contatta l’Assistenza clienti Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Launch - Libreria caricata</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare un oggetto _satellite globale nel DOM. Launch non è installato o non è in grado di eseguire. </p> </td> 
   <td colname="col3"> <p>Verificare che la libreria Launch sia implementata sulla pagina e che non sia bloccata dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Avvio - Non sono presenti più script da incorporare</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Sulla pagina non devono essere caricati più script da incorporare. I siti di produzione devono caricare una sola libreria Launch. </p> </td> 
   <td colname="col3"> <p>Verificate che sulla pagina venga caricata solo la libreria di produzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom callback esiste in &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il callback <span class="codeph"> _satellite.pageBottom()</span> non è stato trovato all'interno del <span class="codeph"> &lt;body&gt;</span> della pagina, richiesto da Launch. </p> <p>Il test ha esito negativo se la <span class="codeph"> chiamata </span>pageBottom non viene trovata nella pagina o se si trova nel tag <span class="codeph"> &lt;head&gt;</span> (o in un'altra posizione imprevista). Passerà solo se <span class="codeph"> pageBottom</span> viene trovato in qualche punto all'interno del tag <span class="codeph"> &lt;body&gt;</span> . Se non è sulla pagina, non funzionerà e anche gli altri due test <span class="codeph"> PageBottom</span> non funzioneranno. </p> </td> 
   <td colname="col3"> <p>Aggiungete lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la corretta funzionalità di Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom il callback non deve esistere quando viene distribuito in modo asincrono</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
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
   <td colname="col1"> <p><b> Target - Libreria caricata in &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> La libreria Target deve essere caricata nel tag <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
   <td colname="col3"> <p> Verificate che la libreria Target sia caricata nel tag <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>
