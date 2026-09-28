# MODULO M0 - ESERCIZI
## Esercizio 6 - Struttura delle cartelle per l'intero anno

# 1. Creazione delle 9 cartelle dei moduli
mkdir M0_ambiente
mkdir M1_markdown_jupyter
mkdir M2_programmazione_python
mkdir M3_strutture_dati
mkdir M4_oop
mkdir M5_eccezioni_files
mkdir M6_interfacce_grafiche
mkdir M7_database
mkdir M8_concorrenza_rete

# 2. Creazione dei file segnaposto (.gitkeep) per permettere a Git di tracciare le cartelle
touch M0_ambiente/.gitkeep
touch M1_markdown_jupyter/.gitkeep
touch M2_programmazione_python/.gitkeep
touch M3_strutture_dati/.gitkeep
touch M4_oop/.gitkeep
touch M5_eccezioni_files/.gitkeep
touch M6_interfacce_grafiche/.gitkeep
touch M7_database/.gitkeep
touch M8_concorrenza_rete/.gitkeep

# 3. Creazione dei file README.md in ciascuna cartella
echo "# Modulo M0 - Ambiente" > M0_ambiente/README.md
echo "# Modulo M1 - Markdown e Jupyter" > M1_markdown_jupyter/README.md
echo "# Modulo M2 - Programmazione Python" > M2_programmazione_python/README.md
echo "# Modulo M3 - Strutture Dati" > M3_strutture_dati/README.md
echo "# Modulo M4 - OOP" > M4_oop/README.md
echo "# Modulo M5 - Eccezioni e Files" > M5_eccezioni_files/README.md
echo "# Modulo M6 - Interfacce Grafiche" > M6_interfacce_grafiche/README.md
echo "# Modulo M7 - Database" > M7_database/README.md
echo "# Modulo M8 - Concorrenza e Rete" > M8_concorrenza_rete/README.md

# 4. Salvataggio ed invio con un unico commit
git add .
git commit -m "Aggiunta struttura cartelle M0-M8 con README e .gitkeep"
git push

# 5. Verifica dei file tracciati
git ls-files
