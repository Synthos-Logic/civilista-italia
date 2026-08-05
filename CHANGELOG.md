# Changelog — Kit Civilista Italiano

## [0.1.0] — 2026-08-05
Prima pubblicazione. Kit in costruzione.

### Aggiunto
- **Knowledge Base civile seed**: Rassegne annuali della giurisprudenza di legittimita' —
  Sezioni Civili, anni **2023 e 2024** (6 volumi), convertite in Markdown con marcatori di pagina.
  **6.122 massime** indicizzate nel registro citazionale (Rv → file → pagina → massima),
  269 voci strutturali nell'indice per concetto. Ancoraggio verificato a campione.
- **Skill `civilista-archivio`**: conversione e indicizzazione di PDF, gestione dell'indice a due
  livelli e del registro fonti, per la zona globale e per i singoli fascicoli.
- `CLAUDE.md` con le regole operative civili: onere della prova e preclusioni, termini a ritroso
  (anticipazione, non proroga), condizioni di procedibilita' (mediazione/negoziazione), doppio
  lato attore-convenuto, volatilita' dei valori numerici.
- `KNOWLEDGE_BASE/00_META/GERARCHIA_FONTI.md` riscritta per il civile: SU civili, principio di
  diritto su rinvio pregiudiziale ex art. 363-bis, CGUE, limiti della giurisprudenza di merito.
- `documentazione/FONTI_CIVILI.md`: mappa verificata delle fonti civili aperte (SZC, RLC, RPC,
  open data Consulta, EUR-Lex), con licenze, limiti e cio' che NON e' utilizzabile
  (Italgiure/SentenzeWeb, Banca Dati di Merito).

### Adattato dal kit penale
- Regex del registro citazionale estesa al formato civile `Sez. 2, n. 13949/2024, Varrone, Rv. …`
  (il penale usa `n. … del gg/mm/aaaa`), con le varianti reali dei volumi: copertura 97,6%
  sulle occorrenze "Rv." misurate sulla Rassegna 2024 vol. I.

### Noto / in coda
- Doppia indicizzazione strutturale delle voci di sommario nei volumi civili (rumore, non errore).
- Richiami "orfani" del tipo "la medesima decisione (Rv. …)" non collegati alla citazione precedente.
- Skill operative (inizia, scadenze, atti, analisi del caso, giurisprudenza, verifica, ADR,
  quantificazione): in lavorazione.
