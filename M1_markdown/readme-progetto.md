# MODULO M1 - ESERCIZI
## Esercizio 6 - README di un progetto Java del terzo anno

MediaVoti è un programma Java da riga di comando che legge da un file CSV i voti degli studenti di una classe. Calcola la media generale, il voto più alto, il voto più basso e la media di ogni studente. Stampa il riepilogo direttamente a video.

## Requisiti

| Componente | Versione minima | Note                                         |
|------------|-----------------|----------------------------------------------|
| JDK        | 17              | Serve il compilatore `javac`, non solo la JRE |
| Git        | 2.30            | Per scaricare il progetto                    |
| Terminale  | qualsiasi       | Bash, PowerShell o il terminale del server   |

Per verificare di avere tutto, eseguire:

`````bash
javac -version
git --version
`````

## Installazione

1. Scaricare il progetto dal repository:

`````bash
   git clone https://github.com/nomeutente/mediavoti.git
`````

2. Entrare nella cartella del progetto:

`````bash
   cd mediavoti
`````

3. Compilare i sorgenti nella cartella `out`:

`````bash
   mkdir out
   javac -d out src/*.java
`````

4. Controllare che la compilazione sia riuscita: la cartella `out` deve contenere i file `.class`.

`````bash
   ls out
`````

## Uso

Il programma riceve come unico argomento il percorso del file CSV:

`````bash
java -cp out MediaVoti voti.csv
`````

### Formato del file di ingresso

Il file è di testo, con i campi separati da virgola. La prima riga è l'intestazione, ogni riga successiva contiene uno studente, una materia e un voto intero da 1 a 10.

`````csv
studente,materia,voto
Rossi,Matematica,7
Rossi,Informatica,8
Bianchi,Matematica,6
Bianchi,Informatica,9
Verdi,Matematica,5
Verdi,Informatica,7
`````

### Output atteso

Con il file qui sopra, salvato come `voti.csv`, il programma stampa:

`````text
Riepilogo voti - file: voti.csv
Studenti:        3
Voti letti:      6
Media generale:  7.00
Voto massimo:    9 (Bianchi, Informatica)
Voto minimo:     5 (Verdi, Matematica)

Media per studente:
  Bianchi   7.50
  Rossi     7.50
  Verdi     6.00
`````

## Struttura del progetto

`````text
mediavoti/
├── src/
│   ├── MediaVoti.java     # classe con il main
│   ├── LettoreCsv.java    # legge e valida il file CSV
│   └── Riepilogo.java     # calcola e stampa le statistiche
├── voti.csv               # file di esempio
├── README.md
└── LICENSE
`````

## Autore e licenza

Progetto realizzato da **Nome Cognome**, classe 4BI, Laboratorio di Informatica.

Distribuito con licenza [MIT](LICENSE).