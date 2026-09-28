# MODULO M0 - ESERCIZI
## Esercizio 9 - Lettura e interpretazione della cronologia

### 1. Comandi da eseguire dopo aver fatto 5 commit distinti

```bash
git log --oneline --graph --decorate
git log -5 --pretty=format:"%h %ad %an %s" --date=short

# Cronologia del Repository

## Output di `git log --oneline --graph --decorate`

```text
* a1b2c3d (HEAD -> main, origin/main) Aggiornato README principale
* e4f5g6h Aggiunto file autenticazione.md
* i7j8k9l Aggiunto file gitignore e relazione di verifica
* m0n1o2p Creata struttura cartelle da M0 a M8
* q3r4s5t Primo commit con README.md iniziale

# Output:
a1b2c3d 2024-10-15 Mario Rossi Aggiornato README principale
e4f5g6h 2024-10-15 Mario Rossi Aggiunto file autenticazione.md
i7j8k9l 2024-10-15 Mario Rossi Aggiunto file gitignore e relazione di verifica
m0n1o2p 2024-10-15 Mario Rossi Creata struttura cartelle da M0 a M8
q3r4s5t 2024-10-15 Mario Rossi Primo commit con README.md iniziale