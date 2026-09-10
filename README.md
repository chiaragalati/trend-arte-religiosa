# _Sola fide, sola scriptura, sola data_: principali generi pittorici e analisi del trend dell'arte religiosa

## DOI
[![DOI](https://zenodo.org/badge/1363229389.svg)](https://doi.org/10.5281/zenodo.22684741)


## Descrizione
Lo scopo del progetto è l'analisi (esplorativa ed esplicativa) di un dataset storico-artistico, che comprende una serie di opere la cui realizzazione si colloca tra l'XI e il XXI secolo. Ci si focalizzerà in seguito sull'andamento dell'arte religiosa in generale nel corso del periodo preso in esame, e successivamente nel XVI secolo.

Dall'elaborazione dei dati emerge quale genere prevalente del dataset l'arte religiosa, nettamente più presente rispetto agli altri. Si può notare un picco nel Cinquecento, dovuto alla produzione artistica rinascimentale del Quattrocento, mentre successivamente si registra una serie di fluttuazioni e picchi ricorrenti, dovuti agli scontri religiosi che hanno segnato l'epoca, in particolare la Controriforma cattolica, e che hanno impattato la produzione del genere artistico.

## Fonti
I dati utilizzati per l'analisi sono costituiti da un file CSV di 229.3+ KB. 

Link al dataset: https://raw.githubusercontent.com/dhdmch/2025-2026/refs/heads/main/data/vapod/data.csv

| Variabile | Tipo |	Definizione | Esempio |
| :------- | :--- | :--------- | :------ |
|    id    |	str |  ID dell'opera| 	http://www.wikidata.org/entity/Q16549203 |
|    titolo    |	str | Titolo dell'opera | Deposizione della croce	 |
|    artisti    |	str |  Autore dell'opera| 	Federico Barocci (maschio) |
|    data_creazione    |	str |  Data| 	1568 |
|    generi    |	str | Genere | 	arte religiosa |
|    luoghi    |	str | Luogo, collocazione | cattedrale di San Lorenzo	 |
|    collezioni    |	str | Collezione | cattedrale di San Lorenzo	 |
|    contenuti    |	str | Contenuto, descrizione dell'opera | 	Gesù; deposizione di Gesù |
|    movimenti    |	str | Corrente artistica | NaN	 |
|    soggetti    |	str | Soggetto | 	deposizione di Gesù	 |
|    altezza    |	float | Altezza dell'opera in cm| 412.0	 |
|    larghezza    |	float |  Larghezza dell'opera in cm| 232.0	 |

## Metodi e strumenti
Il progetto, sviluppato su Google Colab utilizzando il linguaggio di programmazione Python, e lo strumento Pandas per le operazioni di analisi dei dati, è strutturato nel seguente modo:

caricamento e ispezione dei dati (pd.read_csv, df, df.shape, df.info());
processamentodei dati (df.duplicated(), df.isnull().sum());
exploratory data analysis (df["colonna"].str.split("; ").explode().value_counts() per spezzettare i generi, una funzione per aggrupparli, e visualizzazione tramite grafico a barre (plot.bar()), creazione di un secondo dataframe per l'arte religiosa e definizione di una funzione per ottenere i secoli, visualizzazione tramite grafico a linee (plot.line());
explanatory data analysis (creazione di un altro dataframe per il XVI secolo e visualizzazione tramite grafico a linee (plot.line()).

## Credits
Galati Chiara 
## Licenza
I dati sono rilasciati sotto licenza [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).
