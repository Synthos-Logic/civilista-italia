---
description: Mostra la versione installata del Kit Civilista Italiano e verifica se su GitHub esiste una versione piu recente
---
La versione installata di questo plugin e la **0.8.4** (agosto 2026), con 12 skill: inizia, caso, scadenze, atti, monitorio, lavoro, famiglia, adr, quantificazione, giurisprudenza, verifica, archivio.

Esegui questi passi nell'ordine:

1. **Comunica la versione installata** (0.7.0) all'utente.

2. **Verifica la versione pubblicata su GitHub**: scarica `https://raw.githubusercontent.com/Synthos-Logic/civilista-italia/main/.claude-plugin/plugin.json` (con web fetch oppure `curl -s` da shell) e leggi il campo `version`.
   - Se il fetch fallisce (offline, restrizioni di rete): dillo esplicitamente e salta al punto 4. Non dedurre nulla sulla versione remota.

3. **Confronta le versioni** (confronto semantico: 0.10.0 > 0.9.0):
   - **Uguali** → conferma: "Sei aggiornato all'ultima versione."
   - **Remota piu recente** → AVVISA con chiarezza: il kit installato e rimasto indietro. Spiega che esiste un problema noto dell'app Claude per cui la sincronizzazione automatica del marketplace puo bloccarsi in silenzio (il client dice "aggiornato" anche quando non lo e), e fornisci la **procedura di sblocco garantita**:
     1. Personalizza → Plugin → **Personale**;
     2. sul chip del marketplace `civilista-italia` clicca **···** → **Rimuovi** (rimuove solo il catalogo: fascicoli e Knowledge Base nella cartella dello studio NON vengono toccati);
     3. clicca **+** e ri-aggiungi il marketplace con l'URL `Synthos-Logic/civilista-italia`;
     4. reinstalla il plugin Civilista Italia: arrivera l'ultima versione;
     5. riavvia l'app e apri una conversazione nuova.
     Suggerisci anche di consultare il CHANGELOG (`https://github.com/Synthos-Logic/civilista-italia/blob/main/CHANGELOG.md`).

4. **Verifica le skill attive**: controlla quali skill `civilista-*` risultano disponibili in questa sessione e segnala differenze rispetto all'elenco delle 12.

5. **Controlla anche la freschezza della banca dati**: leggi la data di generazione in testa a `KNOWLEDGE_BASE/_INDICE/INDICE.md`. Se e piu vecchia di 7 giorni, o se manca la cartella `02_GIURISPRUDENZA/SEGNALATE/`, proponi l'aggiornamento: la pipeline pubblica gira ogni lunedi, il kit va sincronizzato per riceverne i dati.
