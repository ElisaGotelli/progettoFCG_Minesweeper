# TAPPA 2B - HEADER INTERATTIVO 

## OBBIETTIVO DELLA TAPPA: 
Rendere l'header interattivo: 
- al piazzamento/rimozione di una bandierina nella griglia, il contatore di bandierine deve variare di conseguenza
- la texture della faccina deve cambiare in base agli eventi che avvengono durante la partita (click, vittoria, sconfitta)
- il timer deve scorrere calcolando i secondi reali di gioco e il tempo totale della partita deve essere mostrato nel pannello di fine partita

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente: 
- è stato implementato un Clock interno a SFML per il calcolo del tempo reale trascorso per il timer 
- sono stati definiti e modificati diversi parametri e funzioni all'interno di diverse struct per gestire le nuove funzionalità. Ad esempio è stata definita la funzione set_number nella struct Flag_Counter per l'aggiornamento grafico del contatore.
- è stata aggiunta l'indicazione del tempo totale (formattato in ore, minuti e secondi) nel pannello di fine partita (Stop_Panel).
- è stata definita una nuova funzione handle per gestire il rilascio del pulsante sinistro del mouse (per far tornare la faccina allo stato normale dopo il click).
- sono state modificate le funzioni handle per la perdita e ripresa del focus, in modo da bloccare o far ripartire il timer di gioco, e la gestione del click del mouse per aggiornare correttamente la texture della faccina (Face).

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa2b
```

## VERIFICA DEL RISULTATO: 
#### N.B: Le frecce nelle foto sono per indicare un particolare del risultato (tipo la cella considerata per quella verifica di risultato). Non devono comparire nel risultato
#### INIZIO PARTITA: 
Appena aperta (o appena prima dell'inizio di una nuova partita) la finestra l'header dovrebbe presentare: 
- tre zeri per il timer 
- la faccina con la texture di default (smile_face_texture)
- la rappresentazione con Number del numeri 15 per il contatore (cioè il numero di mine nella griglia) <br>
Non dovrebbe essere possibile incrementare/decrementare il contatore bandierine o far partire il timer prima della prima mossa. <br><br>
Allego uno screenshot del risultato da me ottenuto:
![risultato_dueb_inizio](../risorse/risultati/tappa2b_inizio.png)

#### TIMER:
- Dopo la prima mossa, il timer dovrebbe partire in automatico aggiornandosi ogni secondo. <br><br>
Allego uno screenshot del risultato da me ottenuto:
![risultato_dueb_timer](../risorse/risultati/tappa2b_timer.png)

- In caso di perdita del focus della finestra, il timer dovrebbe fermarsi e ripartire solo quando la finestra riprende il focus.

#### FLAG COUNTER:
- Al piazzamento di una bandierina il contatore delle bandierine dovrebbe diminuire di uno, a parte quando arriva a zero (il contatore non ammette numeri negativi). <br><br>
Allego uno screenshot del risultato da me ottenuto:
![risultato_dueb_flagDecr](../risorse/risultati/tappa2b_flagDecr.png)
- Al togliere una bandierina, il contatore delle bandierine dovrebbe aumentare di uno. Tuttavia, se anche dopo la rimozione il numero di bandierine presenti supera ancora quello delle mine (ad esempio passando da 17 a 16 bandierine su 15 mine totali), il contatore deve rimanere fisso a zero. <br><br>
Allego uno screenshot del risultato da me ottenuto:
![risultato_dueb_flagInc](../risorse/risultati/tappa2b_flagInc.png)

#### FACE:  
- Alla rivelazione di una cella coperta tramite click sinistro del mouse, la faccina dovrebbe cambiare texture in quella sorpresa, per poi tornare nella texture di default al rilascio del pulsante.
 <br><br>
Allego uno screenshot del risultato da me ottenuto:
![risultato_dueb_face](../risorse/risultati/tappa2b_face.png)

## PROBLEMI RISCONTRATI E SOLUZIONI: 
Nessuno.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).