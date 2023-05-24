---
description: Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Adobe Experience Platform Auditor.
seo-description: This reference provides more information about the tests Adobe Experience Platform Auditor performs.
seo-title: Test reference
title: Riferimento test
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
exl-id: b368bf43-2007-4f98-a965-ed8fc07c0fdf
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 100%

---

# Riferimento test{#test-reference}

Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Adobe Experience Platform Auditor.

**Versione corrente per valutazione test:** 1.0.5

Ogni test è ponderato. Il punteggio del test è uguale al peso assegnato. Se superai un test con un peso di cinque, riceverai cinque punti.

* 0: segnala la presenza di problemi di cui dovresti essere a conoscenza, ma che non influiscono sul punteggio.
* 1: consiglia un’ottimizzazione. Nessun impatto sulla precisione dei dati.
* 2: se il test non viene superato, non potrai accedere alle funzioni e alle correzioni più recenti in Experience Cloud.
* 3: test di efficienza e verifica se l’implementazione rispetta le best practice.
* 4: in caso di errore, è possibile che si raccolgano dati non affidabili.
* 5: in caso di errore, è possibile che si verifichi una perdita di dati.

I test vengono superati/non superati. Essi verificano la conformità o la non conformità alle condizioni di prova, pertanto non vi sono punteggi parziali per la conformità parziale. Ad esempio, se il test verifica la versione più recente di una soluzione Adobe e si è in ritardo di una sola versione, si ottiene la stessa valutazione come se si fosse in ritardo di cinque versioni. Le versioni più recenti includono miglioramenti delle prestazioni e correzioni di bug, per cui si consiglia di utilizzare la versione più recente.

È **vivamente consigliato** correggere i risultati di livello 4 o 5.

È **consigliato** correggere i risultati di livello da 1 a 3.

## Quali tecnologie Adobe sono valutate da Platform Auditor? {#section-52833b71c05448aaae508e6070a387f5}

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
* Adobe Experience Platform Launch
