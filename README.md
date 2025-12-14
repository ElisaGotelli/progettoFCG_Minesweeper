# MINESWEEPER THE GAME 
## OBBIETTIVO DEL PROGETTO: 
Questo progetto presenta come obbiettivo quello di creare una versione personalizzata del gioco Minesweeper (in italiano: Prato Fiorito/Campo Minato).<br>
Per le regole e caratteristiche base del gioco si è preso spunto principalmente dai siti: 
- [tictactoefree.com](https://tictactoefree.com/it/prato-fiorito/regole)
- [wikipedia](https://it.wikipedia.org/wiki/Campo_minato_(videogioco))

Invece, per lo sviluppo del progetto completo, ci si è focalizzati in particolare sulla:
- possibilità di scegliere tra diverse difficoltà di gioco (FACILE; MEDIO; DIFFICILE) che si differenziano per il numero di mine e la dimensione della griglia;
- creazione di una schermata iniziale contenente un benvenuto al gioco e la possibilità di scegliere la difficoltà della partita che si andrà a giocare;
- creazione della schermata di gioco principale contenente: 
    * il titolo del gioco;
    * un pannello di gioco costituito dalla griglia (che varia in dimensione in base alla difficoltà), dall'intestazione (con timer, la tipica faccina del classico Minesweeper e il contatore di bandierine) e dal bordo;
    * un pannello di controllo che include un testo (contenente regole, obiettivo, difficoltà e numero mine nella griglia della partita corrente) e dei pulsanti per:
        * mettere in pausa la partita;
        * iniziare una nuova partita;
        * l'uscita dalla schermata di gioco;
- creazione di un pannello nella schermata di gioco visibile solo a fine/pausa di una partita che va ad indicare lo stato della partita in corso (pausa, vittoria, sconfitta) e permette di iniziare una nuova partita o uscire dalla schermata di gioco. <br>
Detto pannello, inoltre, permette, se è stato indicato che si vuole iniziare una nuova partita, di selezionarne direttamente la nuova difficoltà;

## TAPPE CREATE: 
Per il progetto sono state sviluppate 14, in cui: 
- ogni numero di tappa rappresenta l'introduzione di una nuova macro-funzionalità (ad esempio le tappe 1a,1b,1c insieme sono i vari passi per l'implementazione della prima versione giocabile del progetto);
- le tappe con il suffisso 'graphic' nel nome del file .cpp implementano solo della nuova grafica rispetto alla tappa precedente;
- le tappe con il suffisso 'interactive' nel nome del file .cpp contiene la parola 'interactive' rendono interattiva la grafica implementata nella tappa precedente;
- ogni tappa, come richiesto, presenta, oltre al file di codice, un file di documentazione che spiega nel dettaglio la tappa in analisi. <br>
In particolare, nella sezione 'Problemi riscontrati e soluzioni' di dette documentazioni sono stati riportati i problemi riscontrati (segnati nei vari file di documentazione), essi sono solo i problemi che hanno richiesto maggior tempo per essere risolti. Per i problemi minori, risolti velocemente tramite piccole modifiche, sono stati utilizzati dei commenti nel codice con la scritta 'MODIFICATO';

## RISORSE CODICE UTILIZZATE: 
Come risorse esterne di codice sono stati utilizzati solamente i laboratori e i file di codice sviluppati in classe insieme al professore Puppo (in particolare il codice del Laboratorio 3).
