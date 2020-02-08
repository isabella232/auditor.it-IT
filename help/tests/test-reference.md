---
description: Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor.
seo-description: Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor.
seo-title: Riferimento test
title: Riferimento test
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 0c116f699b697ad010ee074ac67159a49ec09ccd

---


# Riferimento test{#test-reference}

Questo riferimento fornisce ulteriori informazioni sui test eseguiti da Auditor.

**Versione corrente per valutazione test:** 1.0.5

Ogni prova è ponderata. La valutazione del test è uguale allo spessore assegnato. Se superate un test con un peso di cinque, riceverete cinque punti.

* 0: Avvisi di problemi di cui dovresti essere a conoscenza, ma che non influiscono sulla valutazione.
* 1: Consiglia un&#39;ottimizzazione. Nessun impatto sulla precisione dei dati.
* 2: Se il test non viene superato, non potrai accedere alle funzioni e alle correzioni più recenti in Experience Cloud.
* 3: Prove di efficienza e verifica se l’implementazione rispetta le best practice.
* 4: In caso di errore, è possibile che si raccolgano dati non affidabili.
* 5: Se si verifica un errore, è possibile che si verifichi una perdita di dati.

I test vengono superati/non superato. Essi verificano la conformità o la non conformità alle condizioni di prova, pertanto non vi sono punteggi parziali per la conformità parziale. Ad esempio, se il test verifica la versione più recente di una soluzione Adobe e si è in ritardo di una sola versione, si ottiene la stessa valutazione di cinque versioni precedenti. Le versioni più recenti includono miglioramenti delle prestazioni e correzioni di bug, per cui si consiglia di utilizzare la versione più recente.

È **vivamente consigliato** correggere i risultati di livello 4 o 5.

È **consigliato** correggere i risultati di livello da 1 a 3.

## Quali tecnologie Adobe sono state definite da Auditor? {#section-52833b71c05448aaae508e6070a387f5}

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

## Categorie di test {#section-630181db21ef4eec9ce6a13a0482bb55}

Il presente riferimento di prova suddivide le prove nelle seguenti categorie:
