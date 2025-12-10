# TAPPA 7B - PULSANTE DI USCITA INTERATTIVO

## OBBIETTIVO DELLA TAPPA: 
Rendere interattivo il pulsante ESCI nei vari pannelli, permettendo all'utente di abbandonare la partita in corso e tornare alla schermata iniziale del menu principale.

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente: 
- è stata implementata la funzione State::exit() che si occupa di resettare lo stato della partita e rendere nuovamente visibile lo Start_Panel.
- sono state modificate le funzioni per la gestione degli eventi di: click di un pulsante e movimento del mouse in modo che gestiscano anche il nuovo pulsante creato.

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa7b
```

## VERIFICA DEL RISULTATO: 
#### N.B: Le frecce nelle foto sono per indicare un particolare del risultato (tipo la cella considerata per quella verifica di risultato). Non devono comparire nel risultato
- Al passaggio del mouse sopra al pulsante ESCI (sia nel Control Panel che negli Stop Panel di tipo Pause, Win e Lose), si dovrebbe azionare lo stesso effetto di focus presente anche per il gli altri pulsanti. <br><br>
Allego gli screenshot dei risultati da me ottenuti:  
![risultato_setteb_control](../risorse/risultati/tappa7b_control.png)
![risultato_setteb_pausa](../risorse/risultati/tappa7b_pausa.png)
![risultato_setteb_lose](../risorse/risultati/tappa7b_lose.png)
![risultato_setteb_win](../risorse/risultati/tappa7b_win.png)

- Cliccando il pulsante ESCI sia nel Control Panel che negli Stop Panel di tipo Pause, Win e Lose la schermata di gioco dovrebbe chiudersi e dovrebbe ricomparire la schermata iniziale (Start Panel). <br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_setteb_return](../risorse/risultati/tappa7b_return.png)


## PROBLEMI RISCONTRATI E SOLUZIONI: 
Nessuno.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).