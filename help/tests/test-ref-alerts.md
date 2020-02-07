---
description: Questo riferimento fornisce ulteriori informazioni sugli avvisi visualizzati da Auditor per i test.
seo-description: Questo riferimento fornisce ulteriori informazioni sugli avvisi visualizzati da Auditor per i test.
seo-title: Avvisi
title: Avvisi
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 762ff31ca4d5ed69d1b813589e419c51a40d5920

---


# Avvisi{#alerts}

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
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM - posizione callback pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Gestione tag dinamica richiede la funzione <span class="codeph"> _satellite.pageBottom()</span> . Aggiungete lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la funzionalità DTM corretta. </p> <p> <p>Nota: È consigliabile che il tag sia l' <i>ultimo</i> tag presente in <span class="codeph"> &lt;body&gt;</span>. Se si trova all'interno del tag <span class="codeph"> &lt;body&gt;</span> , ha la possibilità di funzionare, ma non è la migliore prassi, potrebbe funzionare in modo errato o con risultati indesiderati. </p> </p> </td> 
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
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom, posizionamento callback</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Informazioni aggiuntive</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>La funzione di <span class="codeph"> callback </span>Bottom di Launch deve essere definita per ultima nel corpo della pagina, se distribuita in modo sincrono. </p> <p> <p>Nota: È consigliabile che il tag sia l' <i>ultimo</i> tag presente in <span class="codeph"> &lt;body&gt;</span>. Se si trova all'interno del tag <span class="codeph"> &lt;body&gt;</span> , ha la possibilità di funzionare, ma non è la migliore prassi, potrebbe funzionare in modo errato o con risultati indesiderati. </p> </p> </td> 
   <td colname="col3"> <p>Launch richiede la funzione <span class="codeph"> _satellite.pageBottom()</span> per le distribuzioni sincrone. Aggiungete lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la corretta funzionalità di Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - Self-Hosted</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Guida introduttiva di Launch</a> </p> <p><a href="https://docs.adobelaunch.com/client-side-information/asynchronous-deployment" format="https" scope="external"> Avvia distribuzione asincrona</a> </p> </td> 
   <td colname="col2"> <p>La libreria Launch è ospitata nell'istanza di Adobe Akamai all'indirizzo <span class="filepath"> assets.adobedtm.com</span>. </p> <p>L'hosting autonomo è l'approccio consigliato per il caricamento di Launch perché fornisce un maggiore controllo delle prestazioni del sito Web attraverso il controllo della cache, la riduzione delle dipendenze degli script di terze parti e un maggiore controllo del processo di pubblicazione. Le librerie Launch possono essere ospitate e gestite tramite il proprio hosting Web o CDN. </p> </td> 
   <td colname="col3"> <p>Sebbene l'hosting di Launch tramite la rete CDN di Akamai funzioni nella maggior parte dei casi, si consiglia di implementare l'hosting autonomo come primo passo per migliorare le prestazioni della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - Deve essere distribuito in modo asincrono</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
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

