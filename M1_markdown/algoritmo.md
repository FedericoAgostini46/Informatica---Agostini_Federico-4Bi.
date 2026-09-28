# MODULO M1 - ESERCIZI
## Esercizio 9 - Diagramma di flusso di un algoritmo noto

# Ricerca sequenziale su un array

La ricerca sequenziale (o lineare) cerca un valore in un array confrontandolo con gli elementi uno alla volta, dal primo all'ultimo. Si ferma appena trova l'elemento e restituisce il suo indice. Non richiede che l'array sia ordinato.

## Implementazione in Java

`````java
public static int ricercaSequenziale(int[] a, int x) {
    for (int i = 0; i < a.length; i++) {
        if (a[i] == x) {
            return i;
        }
    }
    return -1;
}
`````

## Diagramma di flusso

`````mermaid
flowchart TD
    A(["Inizio: array a, valore x, n = lunghezza di a"]) --> B["i = 0"]
    B --> C{"i è minore di n?"}
    C -->|Sì| D{"a[i] è uguale a x?"}
    C -->|No| F(["Restituisci -1"])
    D -->|Sì| E(["Restituisci i"])
    D -->|No| G["i = i + 1"]
    G --> C
    E --> H(["Fine"])
    F --> H
`````

## Esempio

Con l'array di voti `{7, 6, 8, 5, 9}` e il valore cercato `8`, il ciclo confronta 7, poi 6, poi 8: il terzo confronto ha successo e il metodo restituisce l'indice atteso, cioè `2`.

## Elemento non presente

Se il valore cercato non è nell'array, la condizione `a[i] == x` non è mai vera e `i` arriva fino a `n`. A quel punto la condizione del ciclo diventa falsa, il ciclo termina e il metodo restituisce `-1`. Questo valore è scelto perché nessun indice valido è negativo, quindi chi chiama il metodo può riconoscere il caso "non trovato" con un semplice controllo. In questo caso vengono eseguiti tutti gli *n* confronti, che è il caso peggiore.