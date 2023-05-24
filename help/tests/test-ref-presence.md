---
description: Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Adobe Experience Platform Auditor per la presenza di tag.
seo-description: This reference provides more information about the tests Adobe Experience Platform Auditor performs for tag presence.
seo-title: Tag presence
title: Presenza tag
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
exl-id: a6ac4d95-2f96-4abb-b39b-4dd0d8df5fe8
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 100%

---

# Presenza tag

Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Adobe Experience Platform Auditor per la presenza di tag.

Platform Auditor valuta se il tag esiste e se si trova nella posizione giusta nel codice della pagina.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Criteri </th> 
   <th colname="col3" class="entry"> Consiglio </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Presenza codice</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Il tag Advertising Cloud non è disponibile nel DOM. </p> </td> 
   <td colname="col3"> <p>Implementa il tag di Advertising Cloud utilizzando l’estensione di Advertising Cloud per Adobe Experience Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Pixel di segmento implementati</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Aggiorna i pixel del segmento di Advertising Cloud ai nuovi tag di sola immagine di Advertising Cloud. L’utilizzo di tag di segmento AMO obsoleti può causare la perdita di dati. </p> </td> 
   <td colname="col3"> <p>Implementa il pixel del segmento di Advertising Cloud utilizzando l’estensione di Advertising Cloud per Adobe Experience Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics - Caricato nel DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/home.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il tag Adobe Analytics non è stato rilevato. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente di Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Libreria caricata</b> </p> <p>Peso: 5 </p> <p>Informazioni aggiuntive: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Risoluzione dei problemi DTM</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aggiunta di codice intestazione e piè di pagina</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare un oggetto _satellite globale nel DOM. Dynamic Tag Management non installato o non eseguito. </p> </td> 
   <td colname="col3"> <p>Verifica che la libreria DTM sia implementata nella pagina e non sia bloccata dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Un codice incorporato</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> I siti di produzione devono caricare solo una libreria DTM. </p> </td> 
   <td colname="col3"> <p>Verifica che nella pagina venga caricata solo la libreria di produzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - Il callback pageBottom esiste in &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il callback <span class="codeph"> _satellite.pageBottom()</span> non è stato trovato all’interno del <span class="codeph"> &lt;body&gt;</span> della pagina, richiesto da Dynamic Tag Management. </p> <p>Il test ha esito negativo se la chiamata <span class="codeph"> pageBottom </span>non viene trovata nella pagina o se si trova nel tag <span class="codeph"> &lt;head&gt;</span> (o in un’altra posizione imprevista). Il test avrà esito positivo solo se <span class="codeph"> pageBottom</span> si troverà all’interno del tag <span class="codeph"> &lt;body&gt;</span>. Se non è presente nella pagina, non funzionerà e anche gli altri due test <span class="codeph"> pageBottom</span> non avranno esito positivo. </p> </td> 
   <td colname="col3"> <p>Aggiungi lo script in linea immediatamente prima del tag <span class="codeph"> &lt;/body&gt;</span> di chiusura per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - Tag pageBottom attivato</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il tag <code> pageBottom</code> DTM non è stato rilevato. </p> <p>Ciò potrebbe verificarsi se la chiamata si trova all’interno di un’istruzione <code> if</code> che restituisce un risultato simile a <code> if (false) {_satellite.pageBottom()}</code>. Quindi, anche se potrebbe esistere ed essere posizionato correttamente, il tag potrebbe non essere attivato. </p> </td> 
   <td colname="col3"> <p>Installa la chiamata <code> pageBottom</code> DTM su ogni pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servizio Experience Cloud ID - Presenza di codice</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/id-service/using/intro/overview.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Codice del servizio Experience Cloud ID non trovato. L’Experience Cloud ID (MCID) è vivamente consigliato per garantire il massimo valore dalle soluzioni Experience Cloud ed è fondamentale per la gestione ID nelle soluzioni Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Installa la versione più recente di MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servizio Experience Cloud ID - Presenza di cookie</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/tools/macid.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare il cookie <span class="codeph"> AMCV_</span>. Devi creare un’istanza di un oggetto visitatore dal codice <span class="codeph"> VisitorAPI.js</span>. </p> </td> 
   <td colname="col3"> <p> Se si tratta di un’implementazione DTM, verifica che l’ID AdobeOrg sia stato immesso correttamente nello strumento MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servizio Experience Cloud ID - Valore MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/id-service/using/intro/cookies.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il valore MID non è stato trovato nel cookie <span class="codeph"> AMCV_</span>. </p> </td> 
   <td colname="col3"> <p>Esegui di nuovo il test per verificare la presenza di eventuali latenze API MCID. Se la condizione persiste, contatta l’Assistenza clienti Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b> Launch - Libreria caricata</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare un oggetto _satellite globale nel DOM. Platform Launch non è installato o non può essere eseguito. </p> </td> 
   <td colname="col3"> <p>Verifica che la libreria Platform Launch sia implementata nella pagina e non sia bloccata dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - Non sono presenti più script incorporati</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Nella pagina non devono essere caricati più script incorporati. I siti di produzione devono caricare una sola libreria Platform Launch. </p> </td> 
   <td colname="col3"> <p>Verifica che nella pagina venga caricata solo la libreria di produzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - Il callback pageBottom esiste in &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il callback <span class="codeph"> _satellite.pageBottom()</span> non è stato trovato all’interno della sezione <span class="codeph"> &lt;body&gt;</span> della pagina, richiesto da Platform Launch. </p> <p>Il test ha esito negativo se la chiamata <span class="codeph"> pageBottom </span>non viene trovata nella pagina o se si trova nel tag <span class="codeph"> &lt;head&gt;</span> (o in un’altra posizione imprevista). Il test avrà esito positivo solo se <span class="codeph"> pageBottom</span> si troverà all’interno del tag <span class="codeph"> &lt;body&gt;</span>. Se non è presente nella pagina, non funzionerà e anche gli altri due test <span class="codeph"> pageBottom</span> non avranno esito positivo. </p> </td> 
   <td colname="col3"> <p>Aggiungi lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la funzionalità Platform Launch corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - Il callback pageBottom non deve esistere quando viene distribuito in modo asincrono</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Il callback <span class="codeph"> _satellite.pageBottom()</span> è stato trovato nella pagina. Ciò non dovrebbe accadere quando Platform Launch è implementato in modo asincrono. </p> </td> 
   <td colname="col3"> <p>Rimuovi lo script<span class="codeph"> _satellite.pageBottom()</span> per abilitare la funzionalità Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target - Presenza di codice</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Target deve essere definito nel DOM. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente di Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target - Libreria caricata in &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> La libreria Target deve essere caricata nel tag <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
   <td colname="col3"> <p> Verifica che la libreria Target sia caricata nel tag <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
