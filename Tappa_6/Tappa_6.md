# TAPPA 6 - LIVELLI DI DIFFICOLTÀ

## OBBIETTIVO DELLA TAPPA: 
Implementare i restanti due livelli di difficoltà del gioco. <br>
Le modalità saranno:
- FACILE: 
    * dimensione griglia: 9x9 celle
    * numero mine: 15 
- MEDIO: 
    * dimensione griglia: 16x16 celle
    * numero mine: 40
- DIFFICILE: 
    * dimensione griglia: 30X16 celle
    * numero mine: 99 
Rendere possibile, inoltre, la scelta della difficoltà di gioco già dalla schermata iniziale.

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente: 
- sono state definite/modificate diverse costanti globali, parametri, costruttori e funzioni per diverse struct per gestire correttamente le nuove funzionalità e grafiche di gioco. Ad esempio, è stato modificato l'header in modo che abbia un'altezza fissa (basata sulla modalità Easy) indipendente dalla dimensione delle celle correnti, per garantirne la leggibilità. Oppure è stato aggiunto un nuovo possibile tipo (new_game) per lo Stop_Panel nella enum stop_type per gestire la scelta della difficoltà della prossima partita al click del pulsante 'Nuova Partita'. 
- sono state modificate le funzioni per la gestione degli eventi di: click di un pulsante e movimento del mouse (gestione nuovi pulsanti creati); click di un pulsante sulla tastiera (rimosso l'avvio tramite tasto SPACE dalla schermata iniziale).

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa6
```

## VERIFICA DEL RISULTATO: 
#### N.B: Le frecce nelle foto sono per indicare un particolare del risultato (tipo la cella considerata per quella verifica di risultato). Non devono comparire nel risultato
#### START PANEL
All'apertura della finestra, nello Start Panel, dovrebbero apparire i tre pulsanti di difficoltà al posto del testo 'Premere ENTER per cominciare una nuova partita'. <br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_sei_start](../risorse/risultati/tappa6_start.png)

Cliccando sui rispettivi pulsanti, la griglia deve adattarsi alle dimensioni specificate per la difficoltà scelta: 
- FACILE: griglia 9x9 e 15 mine. 
- MEDIO: griglia 16x16 e 40 mine. 
- DIFFICILE: griglia 30x16 e 99 mine. <br><br>
Allego degli screenshot dei risultati da me ottenuti:  
![risultato_sei_facile](../risorse/risultati/tappa6_facile.png)
![risultato_sei_medio](../risorse/risultati/tappa6_medio.png)
![risultato_sei_difficile](../risorse/risultati/tappa6_difficile.png)

#### PANNELLI:
Cliccando il pulsante NUOVA PARTITA (dal Control Panel o dagli Stop Panel), dovrebbe comparire il menu di scelta difficoltà (Stop Panel tipo New_Game) che permette di cambiare difficoltà di gioco.<br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_sei_pannelli](../risorse/risultati/tappa6_pannelli.png)


## PROBLEMI RISCONTRATI E SOLUZIONI: 
#### PROBLEMA 
Con l'introduzione delle difficoltà MEDIO e DIFFICILE, il numero di celle aumenta drasticamente e, per quanto riguarda la modalità DIFFICILE, va a modificare anche l'aspetto della griglia da quadrata a rettangolare. 
Per queste due nuove modalità la griglia e il panel (essendo che era stato impostato che avessere sempre le stesse dimensioni) andavano a coprirsi l'uno con l'altro.

#### SOLUZIONE 
È stata implementata la funzione set_difficulty in modo che in base alla difficoltà scelta La dimensione del Game Panel venga variata per essere totalmente contenuta nello spazio tra Control Panel e bordo finestra. <br>
Essendo che la funzione reset non va a ricosturire ogni volta un nuovo Control Panel, il Control Panel rimarrà sempre delle stesse dimensioni e non adrà a coprire il Game Panel. 

#### PROBLEMA: 
Con il cambiamento delle dimensioni del Game Panel si andava a variare anche la dimensione dell'Header e dei suoi elementi rendendoli in alcuni casi illeggibili. 

#### SOLUZIONE: 
Si è optato per lasciare sempre uguale (cioè come sarebbero rappresentati nella modalità EASY di gioco) l'altezza dell'Header e le dimensioni dei suoi elementi tramite l'utilizzo delle costanti starting_cell_size e header_grid_proportion. 

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).