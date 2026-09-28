# MODULO M1 - ESERCIZI
## Esercizio 8 - Guida ai recinti annidati

Questa guida spiega come mostrare un blocco di codice dentro un altro blocco di codice. Un recinto (in inglese *fence*) è la riga di apertura e di chiusura di un blocco: si scrive con tre o più backtick.

## Esempio 1: un blocco java normale

Qui vedrai un normale blocco di codice Java, con i colori della sintassi. I backtick di apertura e chiusura non compaiono: sono già stati interpretati.

`````java
public class Saluto {
    public static void main(String[] args) {
        System.out.println("Ciao");
    }
}
`````

## Esempio 2: lo stesso blocco mostrato come sorgente

Qui vedrai il sorgente Markdown dell'esempio precedente, comprese le righe con i tre backtick e la parola java. Per ottenerlo il recinto esterno usa quattro backtick, cioè uno più di quello interno.

`````markdown
````java
public class Saluto {
    public static void main(String[] args) {
        System.out.println("Ciao");
    }
}
````
`````

## Esempio 3: un terzo livello di annidamento

Qui vedrai il sorgente dell'esempio 2, quindi un blocco a quattro backtick che contiene un blocco a tre backtick. Il recinto più esterno usa cinque backtick.

`````markdown
````markdown
```java
public class Saluto {
    public static void main(String[] args) {
        System.out.println("Ciao");
    }
}
```
````
`````

## Regola da ricordare

Il recinto esterno deve essere sempre più lungo di qualsiasi recinto scritto al suo interno: se dentro ci sono tre backtick, fuori ne servono almeno quattro. In alternativa si può usare la tilde per il recinto esterno, che non si confonde con i backtick. Se il recinto è sbagliato, tutto il resto del documento viene reso come codice.