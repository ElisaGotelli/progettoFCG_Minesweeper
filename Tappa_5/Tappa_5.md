# TAPPA 5 - SCHERMATA INIZIALE

## OBBIETTIVO DELLA TAPPA: 
Creare e rendere interattiva una schermata iniziale per il gioco.

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente: 
- è stata definita una nuova struct (con la sua funzione draw() e costruttore) che rappresenta la schermata iniziale di gioco (Start_Panel).
- è stato definito l'oggetto Start_Panel all'interno della struct State
- sono state definite delle nuove costanti globali per le caratteristiche di dimensione, posizione, gap e testo del nuovo Start Panel.
- è stata modificata la funzione draw() della struct State in modo che, all'apertura della finestra, venga inizialmente reso visibile solo lo Start Panel.
- sono state modificate le funzione per la gestione degli eventi di: perdita di focus in modo che la schermata di pausa (Stop Panel di tipo pause) non diventi visibile se lo Start Panel risulta ancora visibile; di click di un pulsante sulla tastiera per rendere visibile la schermata di gioco; di click e movimento del mouse in modo che non venga eseguita nessuna azione quando la schermata iniziale è visibile; 

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa5
```

## VERIFICA DEL RISULTATO: 
All'apertura della finestra non dovrebbe più apparire la schermata di gioco ma la schermata iniziale (Start_Panel). <br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_cinque](../risorse/risultati/tappa5.png)

Al click del pulsante SPACE su tastiera quando la schermata iniziale è ancora visibile, la schermata iniziale dovrebbe essere sostituita da quella di gioco di default.

## PROBLEMI RISCONTRATI E SOLUZIONI: 
Nessuno.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).