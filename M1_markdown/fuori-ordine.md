# MODULO M1 - ESERCIZI
## Esercizio 11 - Che cosa stampa un notebook eseguito fuori ordine

# Che cosa stampa un notebook eseguito fuori ordine

Le quattro celle di codice, dall'alto in basso come appaiono sullo schermo, sono queste (fra parentesi il numero di esecuzione salvato):

| Posizione | N. esecuzione | Contenuto                                            |
|----------:|--------------:|------------------------------------------------------|
| 1ª        | `[2]`         | `aula = "Laboratorio 3"` e `posti = 24`              |
| 2ª        | `[4]`         | `posti = posti - 2` e stampa dei posti disponibili   |
| 3ª        | `[3]`         | stampa di `aula` e di `posti - iscritti`             |
| 4ª        | `[1]`         | `iscritti = 22` e stampa degli iscritti              |

## 1. Ordine reale di esecuzione

Le celle sono state eseguite nell'ordine `[1]`, `[2]`, `[3]`, `[4]`, cioè: prima la quarta cella dello schermo, poi la prima, poi la terza, infine la seconda. Lo si deduce dai numeri fra parentesi quadre: il kernel li assegna in ordine crescente, uno per ogni esecuzione, quindi il numero indica quando la cella è stata eseguita, non dove si trova sullo schermo.

## 2. Perché `[4]` mostra 22 mentre `[3]` ha usato 24

Il kernel conserva le variabili in memoria e ogni cella vede il loro valore *nel momento in cui viene eseguita*. Quando è stata eseguita `[3]`, l'unica cella che aveva toccato `posti` era `[2]`, che l'ha posta a 24. La cella `[4]` è stata eseguita dopo, ha calcolato 24 - 2 = 22 e ha stampato 22. Il fatto che `[4]` sia scritta sopra `[3]` non conta: conta l'ordine di esecuzione. L'output di `[3]` (`liberi: 2`, cioè 24 - 22) è rimasto salvato com'era e non viene ricalcolato dopo `[4]`.

## 3. Output dopo Restart Kernel and Run All Cells

Con un kernel nuovo le celle vengono eseguite nell'ordine in cui sono scritte, dall'alto in basso. La quarta cella non viene eseguita affatto, perché l'esecuzione si ferma alla prima cella che dà errore.

`````text
1ª cella (aula, posti)       -> nessun output
2ª cella (ex [4])            -> Posti disponibili: 22
3ª cella (ex [3])            -> NameError: name 'iscritti' is not defined
4ª cella (ex [1])            -> non eseguita
`````

## 4. Quale cella produce un errore

Produce un errore la terza cella dello schermo, quella con numero di esecuzione `[3]`. Il messaggio esatto è:

`````text
NameError: name 'iscritti' is not defined
`````

Il motivo è che `iscritti` viene definita solo nella quarta cella, che dall'alto in basso viene dopo la cella che la usa. Nel notebook consegnato tutto "funzionava" solo perché la cella `[1]` era stata eseguita per prima.

## 5. Correzione del notebook

Va spostata in cima la cella che contiene `iscritti = 22`, così che ogni variabile sia definita prima di essere usata. Con le celle nell'ordine (iscritti, aula e posti, posti - 2, stampa dei liberi), l'esecuzione dall'alto in basso da un kernel vuoto arriva in fondo senza errori e stampa:

`````text
Iscritti: 22
Posti disponibili: 22
Laboratorio 3 - liberi: 0
`````

Al posto di `liberi: 2` comparirà `liberi: 0`. Il valore 2 nasceva dall'ordine casuale in cui erano state eseguite le celle: nell'ordine corretto la cella dei posti disponibili viene prima e `posti` vale già 22 quando si calcola 22 - 22.

## 6. Verifica sul server

Le previsioni vanno confrontate con l'esecuzione reale. Spuntare le voci dopo averle controllate:

- [ ] Ricostruito il notebook con le quattro celle nell'ordine originale
- [ ] Eseguito Restart Kernel and Run All Cells e ottenuto `NameError` alla terza cella
- [ ] Spostata la cella di `iscritti` in cima e rieseguito tutto
- [ ] Confrontato l'output con quello scritto sopra