CONSEGNA PROGETTO PER L'ESAME DI DATA MINING

STUDENTE: Lxxxxxxxx Txxxxxxxx

MATRICOLA: xxxxxx

DOCENTE: Dxxxxx Mxxxxxx

CORSO DI LAUREA: Data Science

DATASET: https://archive.ics.uci.edu/ml/datasets/online+retail


La cartella inviata contiene 6 file in formato PDF, che rappresentano la versione stampata dei notebook utilizzati per lo svolgimento dell'analisi. 

Le analisi sono state svolte utilizzando python attraverso l'uso di Jupyter Notebooks, con l'ausilio di WEKA per testare i vari algoritmi di clustering e di Frequent Pattern e Association Rules Mining, al fine di scoprire le soluzioni migliori. 

I notebook sono di seguito sintetizzati:

1) Analisi del dataset al fine di effettuare una pulizia generale, eliminando le informazioni corrotte o non utili ai fini della ricerca. Inoltre è stato impostato un obiettivo di business verosimile, cioè effettuare una segmentazione degli utenti al fine di attuare una strategia di marketing pubblicitario mirata. In fine attraverso statistiche e grafici è possibile ottenere una descrizione completa del dataset e dei suoi attributi principali.

2) Attraverso l'utilizzo della tecnica di segmentazione/analisi RFM(Recency, Frequency, Monetary) e dell'algoritmo di clustering K-MEANS i clienti sono stati suddivisi in diverse categorie. Dopo aver individuato e descritto le categorie più interessanti ai fini della nostra indagine, abbiamo deciso di concentrare l'analisi di marketing sulla categoria Best Customers. 

3) Dalla categoria dei best customers sono stati individuati innanzitutto i top client (o Whales), intesi come coloro che hanno un valore di monetary più elevato, e da questi, sono stati selezionati i 100 clienti con il più alto numero di prodotti acquistati a prezzo scontato (almeno 20 pezzi con una percentuale di sconto del 15% rispetto alla media del prezzo).

4) Utilizzando l'algoritmo APRIORI e le metriche di supporto e lift, sono state individuati i pattern frequenti e successivamente le regole di associazione con correlazione positiva. Tali regole sono state estratte da un sottoinsieme del dataset che comprende esclusivamente le transazioni effettuate dai clienti target precedentemente selezionati (basandomi sull'idea che le previsioni effettuate su un sottoinsieme di clienti con alto livello di similarità sono più affidabili).

5) Intersecando gli antecedent delle regole di associazione individuate con l'insieme dei prodotti contenuti nell'ultimo acquisto effettuato dai clienti target, sono stati riscontrati 6 casi in cui 6 clienti diversi avevano nel carrello uno o più prodotti presenti negli antecedent delle regole. Di conseguenza i prodotti contenuti nel consequent di tali regole sono stati selezionati come consigliati per tali clienti. La società potrebbe quindi scegliere di inviare un campione omaggio di tali prodotti ai clienti selezionati (christmas gift), proponendo uno sconto speciale nel caso di acquisto di uno stock di almeno X pezzi.

6) L'analisi effettuata per il notebook 4 è stata ripetuta per il dataset completo, rivelando l'alta presenza di pattern contenenti stessi prodotti che differiscono solo per il colore o la quantità. Per motivi computazionali, non è stato possibile ovviare a questo problema aggregando le descrizioni di stessi prodotti con colore o numero differente. Sono state scoperte 138 diverse regole dai 352 frequent pattern scovati, utilizzando una soglia di supporto pari a 0.02 ed un valore di lift > 1 per le regole di associazione
