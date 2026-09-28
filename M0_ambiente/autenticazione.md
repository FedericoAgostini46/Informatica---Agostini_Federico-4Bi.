# MODULO M0 - ESERCIZI
## Esercizio 8 - Autenticazione verso GitHub e sua verifica

### File `M0_ambiente/autenticazione.md`

```markdown
# Autenticazione verso GitHub

## Metodo Scelto
**Chiave SSH**

## Motivazione della Scelta
Ho scelto l'autenticazione tramite chiave SSH perché utilizzo una mia postazione di lavoro. SSH permette di inviare i file a GitHub senza dover inserire ogni volta la password o il token personale, rendendo il lavoro più veloce e sicuro. Inoltre, la chiave privata rimane memorizzata sul computer locale e non viene mai condivisa.

## Verifica del Funzionamento

### Comando eseguito
```bash
ssh -T git@github.com
