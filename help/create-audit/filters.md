---
description: L'inclusione di filtri limita i collegamenti che un controllo può visualizzare per indicizzazione dall'URL iniziale. Escludere i filtri impedisce a un controllo di eseguire il crawling dei collegamenti.
seo-description: L'inclusione di filtri limita i collegamenti che un controllo può visualizzare per indicizzazione dall'URL iniziale. Escludere i filtri impedisce a un controllo di eseguire il crawling dei collegamenti.
seo-title: Includi ed Escludi filtri
title: Includi ed Escludi filtri
uuid: 477fc38c-7351-42dd-8209-2fb7549ee34c
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Includi ed Escludi filtri{#include-and-exclude-filters}

L&#39;inclusione di filtri limita i collegamenti che un controllo può visualizzare per indicizzazione dall&#39;URL iniziale. Escludere i filtri impedisce a un controllo di eseguire il crawling dei collegamenti.

<!--
Content from ObservePoint (https://help.observepoint.com/articles/2872121-include-and-exclude-filters) with their permission. Modified slightly for style and Auditor emphasis.
-->

L&#39;inclusione di filtri ed Escludi filtri fornisce linee guida per i controlli. Lasciando vuoti i filtri Includi ed Escludi, un controllo può eseguire la ricerca per indicizzazione dei collegamenti che si trovano, a partire dai collegamenti nell&#39;URL iniziale.

![](assets/filter.png)

Applicando l’opzione Includi filtri, Escludi filtri o una combinazione di entrambe le istruzioni, è possibile specificare i collegamenti che è possibile fornire a un controllo per indicizzazione.

Qualsiasi elemento nel campo Includi filtri limita la scansione solo alle pagine che corrispondono a tale elemento. Qualsiasi elemento in un campo Exclude Filters impedisce la scansione di pagine corrispondenti a tale elemento.

I filtri Includi ed Escludi possono essere URL completi, URL parziali o espressioni regolari che corrispondono a una pagina valida.

## Ordine di precedenza {#section-e9d42419dd3f459bb20e7a33c6104f12}

1. **L&#39;URL** iniziale ha la precedenza su tutto il resto e sarà sempre visualizzato durante un controllo, anche se un URL corrisponde a un elemento nei filtri Escludi. L’URL iniziale viene sempre visitato prima di qualsiasi altro URL.

   ![](assets/startingpage.png)

   Nell&#39;immagine qui sopra, un controllo rileva i collegamenti dalla `document.links` proprietà della pagina iniziale. Tali collegamenti possono essere analizzati dall&#39;audit.

1. **Gli URL** da includere devono essere collegati da una pagina iniziale, altrimenti non possono essere scoperti e non verranno visitati.

   ![](assets/includefilter.png)

   Nell&#39;immagine precedente, l&#39;aggiunta di un filtro Includi limita gli URL idonei a quelli corrispondenti al filtro. Ora solo cinque collegamenti possono essere analizzati dall&#39;audit.

1. **Escludete gli URL** per eliminare i collegamenti dall&#39;idoneità.

   ![](assets/excludefilter.png)

   Nell&#39;immagine precedente, l&#39;aggiunta di un filtro Exclude impedisce agli URL di accedere ai collegamenti idonei. Ora solo tre collegamenti possono essere analizzati dall&#39;audit.

## URL iniziale {#section-ccb46abcd96f4a8ab171245015d2b724}

Auditor richiede una singola pagina per l’URL iniziale. L’URL iniziale viene sempre visitato prima di qualsiasi altro URL. Eventuali collegamenti scoperti dalla pagina iniziale possono essere visitati, fatti salvi i filtri Includi ed Escludi. Se un elemento Exclude corrisponde a un URL iniziale, verrà ignorato.

## Includi filtri {#section-7626060a56a24b658f8c05f031ac3f5f}

I filtri Includi limitano i collegamenti idonei per la scansione durante un controllo. I filtri possono essere:

* URL completi
* URL parziale
* Espressioni regolari corrispondenti agli URL completi o parziali
* Qualsiasi combinazione di quanto sopra

L&#39;aggiunta di URL o espressioni regolari al filtro Includi non garantisce che tali URL specifici vengano analizzati nel controllo. Il controllo esamina i collegamenti nell&#39;URL iniziale, quindi esplora i collegamenti idonei. L&#39;audit prosegue questo processo di ispezione e navigazione fino al raggiungimento del limite di 500 URL scansionati o fino al raggiungimento di nessun altro collegamento idoneo.

>[!NOTE]
>
>In alcuni casi, potrebbero essere necessarie fino a 48 ore per completare una scansione di 500 pagine.

Per impostazione predefinita, un controllo eseguirà la scansione di tutti i sottodomini dell’URL iniziale. A meno che non venga esplicitamente ignorato fornendo un filtro di inclusione, la scansione utilizzerà il filtro di inclusione regex seguente:

`^https?://([^/:\?]*\.)?mysite.com`

In questo modo, qualsiasi collegamento presente nella pagina dell’URL iniziale può essere visitato. Corrisponde a qualsiasi pagina in qualsiasi sottodominio dall&#39;URL iniziale.

L&#39;utilizzo del filtro Include predefinito offre un ampio intervallo di controlli per la ricerca per indicizzazione di un controllo. Per eseguire il controllo in alcune sezioni o pagine, fornire indicazioni specifiche aggiungendo filtri in questa casella. In tal caso, sostituire il valore predefinito con le directory che si desidera che vengano analizzate dal controllo. È inoltre possibile utilizzare i filtri di inclusione per eseguire il controllo tra più domini in cui è necessario avviare il controllo su un dominio e terminare su un altro. A tal fine, digitare i domini che si desidera attraversare. In ogni caso, per trovare eventuali URL Includi filtro, questi devono essere rilevati in una pagina sottoposta a controllo.

I filtri Includi possono contenere URL esatti, URL parziali o espressioni regolari. Ad esempio, se l’URL iniziale è [!DNL http://mysite.com]l’URL iniziale, le pagine seguenti potrebbero essere sottoposte a scansione per impostazione predefinita (note i caratteri grassetti):

```
http://mysite.com
http
<b>s</b>://mysite.com
http://
<b>www</b>.mysite.com/home
http://
<b>dev</b>.mysite.com/home
http://
<b>my</b>.mysite.com/products/products_and_services.html
```

Per i pattern URL complessi, utilizzate il tester delle espressioni regolari di [ObservePoint](http://regex.observepoint.com/).

Consultare anche il documento [Common Regular Expressions for ObservePoint](https://help.observepoint.com/articles/2872116-common-regular-expressions-for-observepoint) per i casi di utilizzo comuni di corrispondenza dei pattern.

## Escludi filtri {#section-00aa5e10c878473b91ba0844bebe7ca9}

I filtri Exclude impediscono l&#39;audit degli URL. Potete usare URL esatti, URL parziali o espressioni regolari. Eventuali URL che corrispondono a un elemento nei filtri Exclude non vengono visualizzati. Se l&#39;URL iniziale è incluso nei filtri Escludi, non viene escluso. L&#39;URL iniziale viene sempre analizzato da un controllo.

## Verifica di filtri e URL {#section-3cfa125b1756411395a64701e128efa0}

Potete verificare i filtri e gli URL in Auditor.

Durante la creazione del controllo, fare clic su **[!UICONTROL Test Advanced Filters]**. Inserite i filtri e gli URL, quindi fate clic su **[!UICONTROL Applica]**.

![](assets/test-advanced-filters.png)

## Documentazione di ObservePoint {#section-79cdc8e850d047969b6d2badf6bbd6f9}

Questo articolo è stato sviluppato in collaborazione con ObservePoint. Per informazioni aggiornate, consulta la documentazione [](https://help.observepoint.com/articles/2872121-include-and-exclude-filters)ObservePoint.
