**Data:** 24 ottobre 2026 · **Stato:** approvata da Mattia

<small>Decisione 0001</small>

# Un solo repository, con le cartelle che nascono fase per fase.

<small>Decisione</small>

## Un repository, cartelle per fase, licenze separate.

- Un solo repository, pubblico appena lo pubblichiamo, per documenti, contratti, archivio, server MCP, sito, agenti di prova e indicizzatore.
- I documenti pubblici stanno in `docs/`: pre-registrazione, minacce, privacy, stile, decisioni.
- Una cartella nasce solo quando parte la sua fase. Oggi esistono la radice, `LICENSES/` e `docs/`.
- I documenti sono in italiano. Il codice userà nomi inglesi.
- Fine riga LF e UTF-8 per tutti i file di testo, fissati in `.gitattributes` ed `.editorconfig`.
- Licenze: MIT per il codice, CC BY 4.0 per i documenti, CC0 1.0 per le esportazioni di dati aggregati.
- La protezione dei dati (`docs/privacy/`) entra nella Fase 0.

<small>Motivi</small>

## Tutto si verifica in un'unica storia.

- Un solo repository permette a terzi di verificare tutto in un'unica versione, con un'unica storia.
- Le cartelle vuote danno l'impressione di un lavoro che non c'è, e git non le conserva.
- L'impronta della pre-registrazione deve essere identica su ogni computer. Su Windows il fine riga CRLF la cambierebbe.
- MIT è pensata per il codice e CC BY per i testi. CC0 lascia i dati aggregati riusabili senza condizioni di diritto d'autore.
- La ricerca per la pre-registrazione ha mostrato che gli indirizzi dei proprietari possono essere dati personali (Linee guida EDPB 02/2025, versione 2.0). Va valutato prima del deploy.

<small>Alternative</small>

## Tre strade scartate.

- **Creare subito tutte le cartelle**, vuote: scartata per i motivi sopra.
- **Repository separati** per contratti, server e sito: più difficile da verificare per terzi.
- **Una sola licenza per tutto**: nessuna va bene sia per il codice sia per i testi.

<small>Conseguenze</small>

## Restano da scegliere strumenti e pubblicazione.

- Gli strumenti di sviluppo restano da scegliere: Hardhat o Foundry, sito statico, gestione dei pacchetti, controllo automatico dei segreti prima di ogni commit. Ognuno avrà una sua scheda nella Fase 1, e ogni cartella di codice avrà il suo `.gitignore` per i file generati.
- Le esportazioni per contributo e quelle dei contenuti non staranno in `data/`: la loro licenza si decide nella politica dei dati aperti.
- Il titolare del copyright nel file `LICENSE` è "The Blankchain authors". Si può sostituire con un nome.
- Il repository è solo locale. Prima di pubblicarlo su GitHub: attivare la segnalazione privata delle vulnerabilità, la scansione dei segreti con blocco del push e la protezione del ramo `main`; poi aggiornare il link in `SECURITY.md`.
