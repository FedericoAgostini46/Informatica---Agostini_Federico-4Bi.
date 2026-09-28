# MODULO M1 - ESERCIZI
## Esercizio 7 - Relazione di laboratorio con indice interno e note

#### Federico Agostini, 4BI 

## Indice

- [Obiettivo](#obiettivo)
- [Materiale](#materiale)
- [Procedimento](#procedimento)
- [Risultati](#risultati)
- [Conclusioni](#conclusioni)

## Obiettivo

Misurare il tempo di esecuzione, in millisecondi, dell'algoritmo di ordinamento Bubble Sort su array di dimensione crescente e verificare come il tempo cresce al crescere di *n*.

## Materiale

- Computer del laboratorio con JDK 17[^1]
- Un editor di testo o un IDE
- Classe Java `BubbleSort` con il metodo `ordina` e un `main` che misura il tempo

## Procedimento

1. Generare un array di `n` numeri interi casuali.
2. Salvare l'istante di inizio con `System.nanoTime()`.
3. Chiamare `ordina` sull'array.
4. Salvare l'istante di fine e calcolare la differenza in millisecondi.
5. Ripetere la misura per `n` = 100, 1000, 10000 e 100000.

Il codice usato per la misura è il seguente:

`````java
int[] a = new int[n];
Random r = new Random(42);
for (int i = 0; i < n; i++) {
    a[i] = r.nextInt(1_000_000);
}

long inizio = System.nanoTime();
ordina(a);
long fine = System.nanoTime();

System.out.println(n + " -> " + (fine - inizio) / 1_000_000 + " ms");
`````

## Risultati

| Dimensione *n* | Tempo (ms) | Rapporto col precedente |
|---------------:|-----------:|------------------------:|
| 100            | 1          | -                       |
| 1000           | 9          | 9,0                     |
| 10000          | 240        | 26,7                    |
| 100000         | 24800      | 103,3                   |

I tempi sono la media di cinque esecuzioni[^2].

## Conclusioni

Quando *n* diventa dieci volte più grande, il tempo cresce di circa cento volte (ultima riga della tabella). Questo è coerente con la complessità quadratica O(n²) del Bubble Sort. Per array piccoli la misura è dominata dal tempo di avvio e il rapporto è più basso.

[^1]: Versione verificata con il comando `java -version`.
[^2]: La prima esecuzione è più lenta perché la JVM deve ancora ottimizzare il codice; per questo si usa la media.