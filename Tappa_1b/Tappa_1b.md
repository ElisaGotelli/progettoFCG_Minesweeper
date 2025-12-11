# TAPPA 1B - CELLE INTERATTIVE 

## OBBIETTIVO DELLA TAPPA: 
Rendere le celle interattive:
- sviluppare un meccanismo di focus per le celle al passaggio del mouse
- sviluppare i meccanismi di rivelazione di una cella, di rivelazione a cascata (flood reveal) e che la prima mossa porti sempre ad una rivelazione a cascata
- sviluppare i meccanismi di posizionamento/rimozione di una bandierina

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente:
- è stato sviluppato un file [textures_fonts.hpp](../risorse/textures_fonts.hpp) per la gestione di tutte le texture e font che verranno utilizzati nel progetto;
- sono stati definiti/modificati diversi parametri, costruttori e funzioni (all'interno delle varie struct) e costanti globali per gestire correttamente le nuove funzionalità e grafiche di gioco. Ad esempio è stata definita la funzione reveal nella struct State per l'implementazione della rivelazione automatica di una cella con texture Covered;
- sono state implementate diverse funzioni handle per la gestione degli eventi di: 
    * click di un pulsante del mouse (click sinistro: rivelazione cella o rivelazione a catena; destro: posizionamento/rimozione bandierina);
    * movimento del mouse (nel caso il mouse sia sopra ad una cella, il bordo di detta cella diventi rosso);
    * perdita/presa focus della finestra; 
    * eventi non programmati; 

 ##### CASO PARTICOLARE PRIMA MOSSA:
Come da regole di gioco è stato fatto in modo che la prima cella rivelata della partita sia sempre di tipo cell_type Empty e che le celle adiacenti non abbiano cell_type Mine. In questo modo, la prima mossa porterà sempre all'esecuzione di flood_reveal (rivelazione a catena). <br>
Le mine vengono posizionate casualmente e i vari cell_type vengono assegnati solo dopo il primo click del tasto sinistro del mouse nella griglia, tramite la chiamata alle funzioni place_mines e place_numbers.

## VERIFICA DEL RISULTATO:
#### N.B: Le frecce nelle foto sono per indicare un particolare del risultato (tipo la cella con focus del mouse al momento dello screenshot). Non devono comparire nel risultato
#### FOCUS: 
- Al passaggio del mouse su una cella, questa dovrebbe avere il bordo illuminato di rosso. <br> <br> Allego uno screenshot del risultato da me ottenuto:
![risultato_1b_focus](../risorse/risultati/tappa1b_focus.png)

#### PRIMA MOSSA:
- Al primo click del tasto sinistro del mouse su una cella coperta qualsiasi, dovrebbe partire sempre una rivelazione a catena. <br> <br> Allego uno screenshot del risultato da me ottenuto:
![risultato_1b_primoClick](../risorse/risultati/tappa1b_primoClick.png)

#### RIVELAZIONE CELLA:
- Dopo la prima mossa, ogni click del tasto sinistro del mouse su una cella coperta dovrebbe portare alla rivelazione di detta cella: 
    * se detta cella fosse cell_type Number, detto numero dovrebbe corrispondere al numero di mine adiacenti alla cella; 
    * se detta cella fosse cell_type Empty dovrebbe partire una rivelazione a cascata;
    * se detta cella fosse cell_type Mine, la cella dovrebbe cambiare texture in Exploded_Mine_texture; <br> <br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_1b_reveal](../risorse/risultati/tappa1b_reveal.png)

#### BANDIERINA: 
- Al click del tasto destro del mouse su una cella coperta dovrebbe apparire una bandierina.
- Al click del atsto destro del mouse su una cella con bandierina, la bandierina dovrebbe sparire. <br> <br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_1b_flag](../risorse/risultati/tappa1b_flag.png)

## PROBLEMI RISCONTRATI E SOLUZIONI:
#### PROBLEMA:
Il bordo rosso rappresentante il focus su una cella veniva parzialmente coperto dalle celle adiacenti.
#### SOLUZIONE: 
Si è aggiunto un leggero gap tra le celle, ridimensionandole leggermente affinché il bordo fosse ben visibile senza sovrapposizioni.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).

