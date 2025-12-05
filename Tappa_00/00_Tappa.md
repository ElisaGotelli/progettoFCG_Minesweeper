# TAPPA 00 - SETUP BASE DELLA FINESTRA 

## OBIETTIVO DELLA TAPPA:
Creazione della finestra di rendering principale e implementazione del Game Loop per la gestione degli eventi base (chiusura e ridimensionamento).

## COSA È STATO IMPLEMENTATO: 
- La finestra è stata configurata con:
    * Titolo: Base Window 
    * Proporzioni: 800x600 
    * Limite di frame: 60 FPS
    * Sfondo: nero
- Gli eventi sono stati gestiti tramite funzioni callback (window.handleEvents). 
- In caso di ridimensionamento della finestra da parte dell'utente è stato implementato che la finestra rimanga sempre di dimensioni con rapporto 4:3 in modo da evitare distorsioni grafiche. 

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa00
```

## VERIFICA DEL RISULTATO: 
All'avvio dell'esecuzione, dovrebbe essere mostrata su schermo una finestra nera 800x600 con il titolo "Base Window".
- Provando a ridimensionare la finestra, il contenuto dovrebbe adattarsi mantenendo le proporzioni 4:3.
- Cliccando il pulsante di uscita dalla finestra ("X" in alto a sinistra) il programma dovrebbe terminare correttamente senza errori in console. <br><br>

Allego uno screenshot del risultato da me ottenuto:  
![risultato_zero](../risorse/risultati/tappa00.png)

## PROBLEMI RISCONTRATI E SOLUZIONI: 
Nessuno (per motivazione spiegata nel punto sottostante).

## FONTI DI RIFERIMENTO UTILIZZATE: 
Per questa tappa è stato utilizzato il codice sviluppato durante le lezioni insieme al professor Puppo per lo svolgimento del laboratorio 3. <br>
Sono solo stati aggiunti dei commenti e cambiato il titolo della finestra.  
