# TAPPA 7A - GRAFICA PULSANTE DI EXIT 

## OBBIETTIVO DELLA TAPPA: 
Creare la grafica per un nuovo pulsante EXIT per il ritorno dalla schermata di gioco alla schermata iniziale. <br>
Detto pulsante dovrà trovarsi: 
- nel pannello di controllo 
- nel pannello di pausa 
- nel pannello di vittoria/sconfitta 

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente sono state definite/modificate costanti globali, parametri, elementi e funzioni draw() delle struct Control_Panel e Stop_Panel per l'implementazione del nuovo pulsante. Ad esempio, è stata modificata la posizione del pulsante NUOVA PARTITA nella struct Stop_Panel per fare spazio al nuovo pulsante appena creato.

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa7a
```

## VERIFICA DEL RISULTATO: 
#### N.B: Le frecce nelle foto sono per indicare un particolare del risultato (tipo la cella considerata per quella verifica di risultato). Non devono comparire nel risultato
#### CONTROL PANEL: 
Nel Control Panel dovrebbe essere presente appena sotto i pulsanti PAUSA e NUOVA PARTITA e centrale orizzontalmente il nuovo pulsante ESCI. <br><br>
Allego uno screenshot del risultato da me ottenuto:  
![risultato_settea_control](../risorse/risultati/tappa7a_control.png)

#### STOP PANEL: 
Negli Stop Panel di tipo Pause, Win e Lose ora dovrebbe essere presente anche il pulsante ESCI a fianco al pulsante NUOVA PARTITA. <br><br>
Allego degli screenshot dei risultati da me ottenuti:  
![risultato_setteadue](../risorse/risultati/tappa7a_pausa.png)
![risultato_setteatre](../risorse/risultati/tappa7a_win.png)
![risultato_setteaquattro](../risorse/risultati/tappa7a_lose.png)

## PROBLEMI RISCONTRATI E SOLUZIONI: 
Nessuno.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).
