# TAPPA 1A - SFONDO E CELLA 9X9

## OBIETTIVO DELLA TAPPA: 
Impostazione della grafica base (sfondo e bordo) della finestra e definizione delle strutture fondamentali (come griglia e cella) per la griglia di gioco 9x9.

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente:
- è stato impostato un nuovo colore di sfondo per la finestra (verde chiaro)
- è stato aggiunto un bordo alla finestra tramite la creazione di una RectangleShape
- sono state definite le struct (con le loro funzioni draw() e i loro costruttori) per rappresentare la griglia (Grid); le celle (Cell); il pannello di gioco (Game Panel); lo stato complessivo della finestra (State).

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa1a
```

## VERIFICA DEL RISULTATO: 
All'apertura la finestra dovrebbe mostrare uno sfondo verde chiaro, un bordo verde scuro e una griglia 9x9 di celle grigie, con texture 'Covered', posizionata nella parte destra orizzontamente e centrale verticalmente della finestra.
<br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_unoa](../risorse/risultati/tappa1a.png)

## PROBLEMI RISCONTRATI E SOLUZIONI: 
#### PROBLEMA: 
Creare il bordo per la finestra in quanto in SFML non esiste un comando che va ad impostare un bordo interno alla finestra stessa. 
#### SOLUZIONE: 
Creare un rettangolo di dimensioni leggermente ridotte rispetto alla finestra, posizione di orgine leggermente spostata rispetto alla finestra, di colore trasparente e bordo spesso quanto la differenza di dimensione tra finestra e il rettangolo appena creato (cioè 15 pixel) e colore verde scuro.

## FONTI DI RIFERIMENTO UTILIZZATE:  
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).



