# Simulatore di DNA - pAequor

Questo progetto simula una popolazione di organismi che possiedono un filamento casuale di DNA. Ogni organismo ha la capacità di mutare, confrontare il proprio DNA con quello di altri e determinare la probabilità di sopravvivenza in base a specifici criteri genetici. Questo progetto è stato realizzato come parte del percorso di studi su Codecademy.

## Funzionalità del Progetto

Il codice include le seguenti funzionalità principali:

- **returnRandBase**: genera una base di DNA casuale tra 'A', 'T', 'C', 'G'.
- **mockUpStrand**: crea un filamento di DNA casuale lungo 15 basi, utilizzando `returnRandBase` per ogni base.
- **pAequorFactory**: una funzione fabbrica che crea oggetti `pAequor` con proprietà e metodi specifici.

### Metodi della Fabbrica `pAequor`

1. **mutate**: modifica una base casuale del filamento DNA con una nuova base, diversa da quella iniziale.
2. **compareDNA**: confronta il DNA di due oggetti `pAequor` e calcola la percentuale di somiglianza.
3. **willLikelySurvive**: determina se l'organismo ha una probabilità alta di sopravvivere, basandosi sulla percentuale di basi 'C' e 'G' nel DNA (almeno 60%).

### Generazione di un Array di Organismi

Al termine del codice, viene creato un array di 30 organismi `pAequor`, ciascuno con un filamento di DNA generato casualmente.

## Come Eseguire il Progetto

1. **Clonazione del Repository**: Clona il repository nella tua macchina locale.
2. **Esecuzione del Codice**: Esegui il codice JavaScript in un ambiente compatibile (come Node.js o un browser).
   
   ```
   let dnaArray = [];
   for(let i = 1; i <= 30; i++) {
     dnaArray.push(pAequorFactory(i, mockUpStrand()));
   }
   ```
Utilizzo dei Metodi: Dopo aver creato gli oggetti pAequor, puoi chiamare i metodi mutate, compareDNA, e willLikelySurvive sugli organismi per simulare mutazioni, confrontare filamenti, e valutare la probabilità di sopravvivenza.

## Struttura del Codice
- returnRandBase: Genera una base casuale ('A', 'T', 'C', o 'G').
- mockUpStrand: Crea un filamento casuale di 15 basi.
- pAequorFactory: Funzione fabbrica che genera organismi pAequor con proprietà e metodi specifici per la simulazione.

## Esempi di Utilizzo
Ecco alcuni esempi di cosa puoi fare con gli organismi pAequor:

- Mutazione di una base:
```
dnaArray[0].mutate(); // Cambia una base casuale del primo filamento
```
- Confronto del DNA di due organismi:
```
dnaArray[0].compareDNA(dnaArray[1]); // Confronta il primo e il secondo filamento
```
- Determinare la probabilità di sopravvivenza:
```
dnaArray[0].willLikelySurvive(); // Ritorna true se il DNA del primo organismo ha almeno il 60% di basi 'C' e 'G'
```
## Note
Questo progetto è stato creato per esercitare l'uso di array, funzioni di generazione casuale, e oggetti in JavaScript.
