Markdown
# Navigazione e percorsi nel terminale

## Sequenza dei comandi eseguiti

```powershell
# 1. Spostamento nella cartella Documents
cd Documents

# 2. Creazione della cartella principale dell'esercizio e delle due sottocartelle
mkdir esercizio-percorsi
cd esercizio-percorsi
mkdir dati, risultati

# 3. Spostamento nella sottocartella 'dati'
cd dati

# 4. Spostamento nella sottocartella 'risultati' usando un percorso relativo
cd ..\risultati

# 5. Verifica della posizione finale
Get-Location