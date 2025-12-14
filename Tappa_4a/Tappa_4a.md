# TAPPA 4A - GRAFICA PANNELLO DI CONTROLLO 

## OBBIETTIVO DELLA TAPPA: 
Implementare la grafica per un pannello di controllo che: 
- dovrà essere posizionato alla sinistra della griglia di gioco; 
-dovrà per ora contenere solo due pulsanti:
    * un pulsante per mettere in pausa la partita; 
    * un pulsante per iniziare una nuova partita.

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente: 
- sono state definite le struct (con le loro funzioni draw(), campi e i loro costruttori) per rappresentare: 
    * dei pulsanti per i vari pannelli del gioco che in futuro consentiranno quando cliccati l'esecuzione automatica di diverse azioni(Control_Button);
    * il pannello di controllo contenente detti pulsanti (Control_Panel):
- sono state definite delle nuove costanti globali contenenti le caratteristiche di colore, testo, posizionamento, tipo, spessore e la dimensione dei nuovi oggetti Control_Button e Control_Panel;
- sono stati ridotti i valori delle costanti 'window_horizontal_displacement' e 'window_vertical_displacement' per avere una migliore visibilità del Game_Panel e Control_Panel;
- è stato modificato calcolo del campo cell_size nel costruttore della struct Game_Panel in modo che consideri ora la larghezza della finestra invece dell'altezza.

## VERIFICA DEL RISULTATO: 
#### N.B: Le frecce nelle foto sono per indicare un particolare del risultato (tipo la cella considerata per quella verifica di risultato). Non devono comparire nel risultato
All'apertura della finestra, precisamente a sinistra del Game Panel, dovrebbe essere visibile il Control Panel con dimensioni uguali a quella del Game Panel e con all'interno i due Control Button 'Pausa' e 'nuova Partita' in alto. <br><br>
Allego uno screenshot del risultato da me ottenuto:
![risultato_quattroa](../risorse/risultati/tappa4a.png)

## PROBLEMI RISCONTRATI E SOLUZIONI: 
#### PROBLEMA: 
Con l'aggiunta del Control Panel, lo spazio orizzontale nella finestra disponibile per il Game Panel si è ridotto. <br> 
Poiché la cell_size nelle tappe precedenti era calcolata basandosi sull'altezza della finestra e il Control Panel veniva creato delle stesse dimensioni del Game Panel, i due si andavano a sovrappore.

#### SOLUZIONE: 
Il calcolo del campo cell_size nel costruttore della struct Game_Panel è stato modificato in modo che si vada totalmente a basare sulla larghezza della finestra anzichè sull'altezza.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).