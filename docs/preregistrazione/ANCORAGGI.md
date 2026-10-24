Aggiornato il 24 ottobre 2026

<small>Pre-registrazione · Ancoraggi</small>

# Nessuna versione è ancora ancorata.

Questo è il registro delle versioni citato nella [pre-registrazione](preregistrazione.md) (sezione 14) e nei suoi [allegati](allegati.md). Per ogni versione ancorata qui si registrano l'impronta SHA-256 di ogni file e le prove della sua data:

- il blocco Bitcoin della prova OpenTimestamps;
- le marche temporali RFC 3161, con accanto il certificato pubblico dell'autorità che le ha emesse, perché si possano verificare anche quando quel certificato verrà sostituito;
- il tag firmato e la release immutabile su GitHub;
- se ci sono, il DOI e la transazione sulla testnet.

Le copie congelate andranno in `docs/preregistrazione/versioni/`, gli emendamenti in `docs/preregistrazione/emendamenti/`.

<small>Regola</small>

## L'impronta si calcola sui byte che git conserva.

Non si calcola sulla copia del file sul proprio computer, che un editor può aver salvato con un altro fine riga. Il file è in UTF-8 senza BOM, con fine riga LF. Il comando, al commit che introduce la versione:

```bash
git show <commit>:docs/preregistrazione/versioni/v1.0/preregistrazione.md | sha256sum
```

Va eseguito in Git Bash, su Linux o su macOS. In Windows PowerShell 5.1 i simboli `|` e `>` ricodificano il testo e cambiano l'impronta. Con OpenTimestamps e RFC 3161 si marca lo stesso file, estratto con `git cat-file blob <commit>:<percorso>`.

| Versione | Data | File | SHA-256 | Prove |
|---|---|---|---|---|
| nessuna | | | | |
