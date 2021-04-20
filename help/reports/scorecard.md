---
description: Dopo aver eseguito un test, la scheda di valutazione mostra le informazioni su un controllo di audit.
seo-description: Dopo aver eseguito un test, la scheda di valutazione mostra le informazioni su un controllo di audit.
seo-title: Scheda di valutazione
title: Scheda di valutazione
uuid: a765cd6a-d3d6-4438-9621-d7899385a518
exl-id: a2ccaf7d-744f-42f0-8193-1c6a93f7a09a
translation-type: ht
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: ht
source-wordcount: '432'
ht-degree: 100%

---

# Scheda di valutazione {#scorecard}

Dopo aver eseguito un test, la scheda di valutazione mostra le informazioni su un controllo di audit.

Fai clic sul nome del controllo di audit nella pagina Adobe Experience Platform Auditor per visualizzare i risultati del test.

![](assets/report.png)

Utilizza la scheda di valutazione per visualizzare il punteggio del controllo di audit nelle seguenti categorie:

* Punteggio complessivo
* Presenza tag

   Valuta se il tag esiste e se si trova nella posizione giusta nel codice della pagina.
* Coerenza tag

   Valuta se i tag sono coerenti tra gli URL.
* Configurazione

   Valuta i tag rispetto ad altre regole e best practice consigliate.
* Avviso

   Gli avvisi mostrano problemi di cui dovresti essere a conoscenza, ma che non influiscono sul punteggio.

Il punteggio dipende dal peso di ciascun test e dal suo superamento. Se il test viene superato, la valutazione aumenta di un numero di punti pari al peso del test.

* 0: segnala la presenza di problemi di cui dovresti essere a conoscenza, ma che non influiscono sul punteggio.
* 1: consiglia un’ottimizzazione. Nessun impatto sulla precisione dei dati.
* 2: se il test non viene superato, non potrai accedere alle funzioni e alle correzioni più recenti in Adobe Experience Cloud.
* 3: test di efficienza e verifica se l’implementazione è conforme alle best practice fortemente consigliate.
* 4: in caso di errore, è possibile che si raccolgano dati non affidabili.
* 5: in caso di errore, è possibile che si verifichi una perdita di dati.

La scheda di valutazione elenca eventuali problemi di livello 4 o 5 che si **consiglia fortemente** di risolvere.

La scheda di valutazione elenca eventuali problemi di livello da 1 a 3 che si **consiglia** di risolvere.

Fai clic su **[!UICONTROL Scarica il rapporto]** per scaricare un file [!DNL Excel] o PDF contenente le informazioni segnalate dal controllo di audit.

Oltre al punteggio per ciascuna categoria, la scheda di valutazione elenca tutte le correzioni consigliate o fortemente consigliate, nonché gli elementi che hanno superato il test. Fai clic su ogni problema per visualizzare ulteriori dettagli nel riquadro a destra. Fai di nuovo clic per approfondire e visualizzare le raccomandazioni su come risolvere il problema. Di seguito sono riportati i dettagli di un problema consigliato nella scheda di valutazione mostrata sopra:

![](assets/report-issue-details.png)

Fai clic sulle categorie nella parte superiore dello schermo per visualizzare i problemi rilevati in ciascuna categoria.

## Quali pagine facevano parte del test? {#section-fd38ffeb868648e89c34c5772fa65f46}

Puoi visualizzare gli elenchi degli URL che hanno superato o non superato il test.

Dalla scheda di valutazione, fai clic sul nome di un test o sul link **[!UICONTROL See All]** (Vedi tutto) sotto ogni intestazione di categoria. In questo modo si viene indirizzati ai dettagli dei test. Per ogni test, puoi visualizzare la descrizione del test e un elenco degli URL i cui test hanno avuto esito positivo o negativo. Queste informazioni sono incluse anche nei rapporti scaricati.
