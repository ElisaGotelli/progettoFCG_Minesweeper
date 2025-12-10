# TAPPA 8 - REGOLE E TITOLO

## OBBIETTIVO DELLA TAPPA: 
Completare il gioco aggiungendo: 
- il titolo del gioco in cima alla schermata di gioco.
- le istruzioni, l'obiettivo, le regole e i dati della partita corrente (difficoltà e mine) all'interno del pannello di controllo.

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente: 
- è stata modificata la costante window_vertical_displacement riducendola per creare lo spazio necessario al titolo nella schermata di gioco.
- sono state definite nuove costanti nel codice e definiti/modificati parametri, costruttori e funzioni delle struct State e Control_Panel per la gestione del testo. Ad esempio, è stato aggiunto un oggetto Text in entrambe le struct.

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa8
```

## VERIFICA DEL RISULTATO: 
Nella schermata di gioco, dovrebbe comparire il titolo "MINESWEEPER" centrato sopra il Control Panel e il Game Panel. Mentre nel panello di controllo (Control Panel) dovrebbe essere presente sotto i tre pulsanti un testo contenente: la difficoltà di gioco scelta; il numero di mine nella griglia; l'obbiettivo e regole di gioco; <br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_otto_titolo](../risorse/risultati/tappa8.png)

## PROBLEMI RISCONTRATI E SOLUZIONI: 
Nessuno.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).