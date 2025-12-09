# TAPPA 3 - BORDO

## OBBIETTIVO DELLA TAPPA: 
Completare la grafica del Game_Panel implementando un bordo che racchiuda sia l'header che la griglia di gioco.  

## COSA È STATO IMPLEMENTATO: 
Rispetto alla tappa precedente: 
- sono state definite le struct (con le loro funzioni draw() e i loro costruttori) per rappresentare le celle che costituiscono il bordo (Border_Cell) e il bordo stesso (Border).
- è stato aggiunto il bordo all'interno della struct Game_Panel
- è stata modificato il costruttore della struct Grid per fare in modo che per la posizione y della griglia venga preso in considerazione anche il bordo

## ISTRUZIONI PER ESEGUIRE DA TERMINALE: 
Prima di poter scrivere questo comando su terminale, bisogna aver: 
- creato la cartella build 
- configurato tramite cmake 
- compilato con make 

```bash
cd build 
./Tappa3
```

## VERIFICA DEL RISULTATO: 
#### N.B: Le frecce nelle foto sono per indicare un particolare del risultato (tipo la cella considerata per quella verifica di risultato). Non devono comparire nel risultato
All'apertura della finestra dovrebbe vedersi un bordo grigio attorno alla griglia e all'header: <br>
- Il bordo non dovrebbe essere interagibile.
- Il bordo non dovrebbe andare a coprire l'illuminazione rossa (focus) delle celle esterne quando al passagio del mouse. <br><br>
Allego uno screenshot del risultato da me ottenuto:
![risultato_tre](../risorse/risultati/tappa3.png)

## PROBLEMI RISCONTRATI E SOLUZIONI: 
#### PROBLEMA: 
L'ordine di disegno iniziale (prima grid poi border) in Game_Panel.draw() causava che il bordo grafico (Border) andasse a coprire il gap tra le celle e il bordo e quindi l'effetto di focus (mouse_focus) delle celle esterne.

#### SOLUZIONE: 
È stato invertito l'ordine di disegno in Game_Panel: ora viene disegnato prima il bordo, poi l'header e infine la griglia, così che il focus delle celle rimanga sempre visibile in primo piano.

#### PROBLEMA: 
Inizialmente il bordo doveva essere rappresentato come una griglia di celle adiacenti simile alla struttura Grid. Tuttavia questo lavoro risultava molto complesso e con la creazione di diversi array di oggetti cella. Ciò andava a complicare di molto il codice, soprattutto se si considera con il bordo rimarrà sempre non interagibile.

#### SOLUZIONE: 
Si è optato per la creazione di soli 8 elementi fondamentali: 
- 4 Celle Angolari (angle_cells): Quadrati fissi che corrispondono ai vertici del bordo.
- 4 Celle Laterali (side_cells): Rettangoli che si adattano dinamicamente per coprire l'intera lunghezza/altezza tra gli angoli.<br>

Questa soluzione ha reso il bordo adattabile a diverse risoluzioni senza ricalcoli continui.

## FONTI DI RIFERIMENTO UTILIZZATE: 
Nessuna (oltre a quelle utilizzate nelle tappe precedenti).