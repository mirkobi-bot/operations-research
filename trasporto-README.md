Questo script risolve un problema di ottimizzazione del trasporto tra impianti di produzione e ristoranti. 
Il problema si presenta come una variante del classico problema del trasporto e viene impostato come un problema di programmazione lineare
con l'obiettivo di minimizzare il costo complessivo di trasporto dell'acqua in bottiglie dagli impianti di produzione ai ristoranti.

Descrizione del problema
In una rete di distribuzione, abbiamo:
-4 impianti di produzione di bottiglie d'acqua, ognuno con una capacità produttiva massima espressa in unità di bottiglie.
-3 ristoranti, ognuno con una domanda specifica di bottiglie d'acqua che deve essere soddisfatta.
-Un costo di trasporto unitario tra ciascun impianto e ciascun ristorante.

Obiettivo
L'obiettivo è minimizzare il costo totale di trasporto necessario per soddisfare la domanda dei ristoranti senza superare le capacità produttive degli impianti.

Variabili
Le variabili di decisione sono rappresentate dalle quantità 𝑥𝑖,𝑗 di bottiglie d'acqua da trasportare dall’impianto 𝑖 al ristorante 𝑗. Queste variabili sono continue e non negative.

Vincoli
Vincolo di capacità produttiva: La somma delle bottiglie trasportate da un impianto ai ristoranti non può superare la capacità produttiva dell'impianto.
Vincolo di domanda: La somma delle bottiglie ricevute da ciascun ristorante deve essere almeno pari alla domanda specificata per quel ristorante.

Funzione obiettivo
La funzione obiettivo è il costo totale di trasporto, calcolato come la somma del prodotto tra quantità trasportate e costo di trasporto unitario per ogni coppia impianto-ristorante:
Costo totale= ∑∑ xi,j ×costoi,j

​Vincoli commentati
Nel codice, sono presenti due vincoli commentati che aggiungerebbero ulteriori condizioni:
-Vincolo sul costo dell'impianto 1: Limita il costo di trasporto dell'impianto 1 a non superare il 25% del costo totale.
-Vincolo di equilibrio tra impianti: Richiede che ciascun impianto copra almeno il 15% del totale delle spedizioni.

Risultato
Se il problema ha una soluzione, lo script visualizza:
-I valori ottimali delle quantità trasportate per ogni coppia impianto-ristorante.
-Il costo minimo totale del trasporto.
-La produzione totale di ciascun impianto.
In caso contrario, stampa che non esiste una soluzione ammissibile.
