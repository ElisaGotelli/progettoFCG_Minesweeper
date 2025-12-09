# TAPPA 4B - PANNELLO DI CONTROLLO INTERATTIVO

## OBBIETTIVO DELLA TAPPA: 
- Rendere interattivo il Control Panel: 
    * quando viene cliccato il pulsante 'Nuova Partita' la schermata di gioco deve tornare allo stato di default. 
    * quando viene cliccato il pulsante 'Pausa' la partita in corso deve essere messa in pausa.
    * i pulsanti devono avere lo stesso effetto di focus visivo (bordo rosso) delle celle.
- Gestire la grafica e logica per la pausa del gioco.
- Inserire nello Stop Panel il pulsante di 'Nuova Partita' al posto del testo 'premere ENTER per cominciare una nuova partita'.

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente: 
- sono stati definiti e modificati diversi nuovi parametri e funzioni a tutte le struct e costanti globali nel codice per gestire correttamente le nuove funzionalità e grafiche di gioco. Ad esempio è stato aggiunto un nuovo tipo possibile di Stop_Panel nell'enum class stop_type per la rappresentazione del pannello di Pausa.
- è stato aggiunto un nuovo oggetto Control_Button di tipo new_game nello Stop Panel per il reset della partita.
- sono state modificate le funzione per la gestione degli eventi: di perdita di focus per fare in modo che il gico venga automaticamente messo in pausa; di click e rilascio di un pulsante e movimento del mouse per gestire i vari Control_Button; di click del pulsante SPACE su tastiera in modo che permetta di far ripartire la partita se essa è in pausa.

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa4b
```

## VERIFICA DEL RISULTATO: 
#### N.B: Le frecce nelle foto sono per indicare un particolare del risultato (tipo la cella considerata per quella verifica di risultato). Non devono comparire nel risultato
#### FOCUS: 
Al passaggio del mouse sopra un pulsante, il pulsante dovrebbe avere lo stesso effetto di focus delle celle (bordo rosso).<br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_quattrob_focus](../risorse/risultati/tappa4b_focus.png)

#### CONTROL PANEL: 
Al cliccare con il pulsante sinistro del mouse il pulsante PAUSA nel Control Panel dovrebbe comparire lo Stop Panel di tipo Pause e il gioco dovrebbe stopparsi. <br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_quattrob_pausa](../risorse/risultati/tappa4b_pausa.png)

Al cliccare con il pulsante sinistro del mouse il pulsante NUOVA PARTITA nel Control Panel la schermata di gioco dovrebbe tornare a quella di default. <br><br>


#### STOP PANEL: 
Negli Stop Panel di tipo Win e Lose non dovrebbe più essere presente la scritta 'premere ENTER per cominciare una nuova PARTITA' ma vi dovrebbe essere il pulsante di NUOVA PARTITA. <br><br>
Allego degli screenshots dei risultati da me ottenuti:  
![risultato_quattrob_lose](../risorse/risultati/tappa4b_lose.png)  
![risultato_quattrob_win](../risorse/risultati/tappa4b_win.png) 

Al cliccare il pulsante ENTER nello Stop Panel di tipo Pause la partita dovrebbe ripartire dall'esatto momento in cui era stata fermata (stesso valore del timer). <br><br>

Al cliccare con il pulsante sinistro del mouse il pulsante NUOVA PARTITA nello Stop Panel la schermata di gioco dovrebbe tornare a quella di default (quindi con lo Stop Panel non visibile) <br><br>

## PROBLEMI RISCONTRATI E SOLUZIONI: 
Nessuno.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).