# TAPPA 2A - GRAFICA HEADER 

## OBBIETTIVO DELLA TAPPA: 
Implementare la grafica per un'intestazione per il pannello di gioco e dei suoi elementi, ovvero:
- un timer per la partita in corso;
- la faccina tipica del gioco stesso Minesweeper;
- un contatore per le bandierine ancora disponibili rispetto al numero totale di mine.

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente:
- sono state definite le struct (con le loro funzioni draw(), campi e i loro costruttori) per rappresentare: 
    * un singolo numero (Number); 
    * il contatore di bandierine (Flag_Counter) composto da tre Number; 
    * la faccina (Face);
    * il timer di gioco (Timer) composto da tre Number; 
    * la struttura contenente tutti gli elementi elencati precedentemente (Header).
- è stato aggiunto l'oggetto Header all'interno della struct Game_Panel;
- sono state definite delle nuove costanti globali contenenti le caratteristiche di colore e del bordo del nuovo oggetto Header;  
- è stata modificato in modo che venga preso in considerazione il nuovo oggetto Header il: 
    * calcolo del campo cell_size nel costruttore della struct Game_Panel;
    * calcolo del campo Grid_pos.y nel costruttore della struct Grid.

## VERIFICA DEL RISULTATO: 
- All'apertura della finestra, dovrebbe comparire esattamente al di sopra della griglia di gioco un rettangolo grigio con bordo nero (Header) contenente:
    * a sinistra tre numeri zero (corrispondenti al Timer);
    * al centro una faccina sorridente (corrispodnente a Face);
    * a destra tre numeri zero (corrispondenti al Flag Counter).
<br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_duea](../risorse/risultati/tappa2a.png)

## PROBLEMI RISCONTRATI E SOLUZIONI: 
Nessuno.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).