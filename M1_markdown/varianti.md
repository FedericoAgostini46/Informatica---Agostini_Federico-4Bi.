# MODULO M1 - ESERCIZI
## Esercizio 4 - Le varianti di Markdown a confronto

La seguente tabella riassume il supporto ai principali costrutti nelle diverse varianti di Markdown.

| Costrutto | Markdown originale | CommonMark | GitHub Flavored Markdown |
| :--- | :---: | :---: | :---: |
| Blocchi di codice recintati | No | Sì | Sì |
| Tabelle | No | No | Sì |
| Caselle di spunta | No | No | Sì |
| Testo barrato | No | No | Sì |
| Collegamenti automatici | No | Sì | Sì |
| Note a piè di pagina | No | No | Sì |

## Esempi delle estensioni GitHub Flavored Markdown

### Checklist di laboratorio
- [x] Clonare il repository locale
- [x] Configurare l'utente Git
- [ ] Creare la struttura delle cartelle
- [ ] Scrivere il codice dei programmi
- [ ] Eseguire i test di verifica
- [ ] Effettuare push su GitHub

### Stato delle versioni
Per questo corso la versione Java ~11~ è considerata superata; utilizziamo unicamente Java 17 LTS.

### Autolink
In caso di problemi con i comandi è possibile consultare direttamente la guida su https://docs.github.com per trovare esempi utili.

## Scelta della variante per le consegne

Per le consegne di questo corso conviene utilizzare la variante GitHub Flavored Markdown (GFM) poiché offre funzionalità avanzate fondamentali come tabelle, checklist e blocchi di codice evidenziati, ideali per documentare progetti software direttamente su GitHub. 

Se questo stesso file viene aperto utilizzando uno strumento che supporta esclusivamente lo standard CommonMark puro, le tabelle non verranno formattate come griglie ma lette come testo semplice separato da barre, le caselle di spunta rimarranno testo grezzo con parentesi quadre e il testo barrato con tilde non evidenzierà la cancellatura. Durante l'analisi nell'anteprima di Visual Studio Code, l'estensione integrata supporta già la maggior parte delle estensioni GFM, mostrando quindi una resa pressoché identica a quella che si ottiene dopo aver caricato il file sulla piattaforma GitHub.