# Kit Civilista Italiano

**Assistente operativo per avvocati civilisti italiani, con giurisprudenza ancorata e verificabile.**
Kit gemello del [Kit Penalista Italiano](https://github.com/Synthos-Logic/penalista-italia), da cui eredita l'impianto anti-allucinazione.

> **Versione 0.4.** Nove skill, otto schede di materia e la Knowledge Base civile. Il set operativo è completo: dall'avvio del fascicolo alla verifica dell'atto prima del deposito.

## Le skill

| Skill | A cosa serve |
|---|---|
| `civilista-inizia` | Avvio guidato: dal primo messaggio al primo fascicolo operativo, su un caso vero |
| `civilista-caso` | Analisi e strategia: onere della prova, preclusioni, procedibilità, punti deboli, convenienza economica |
| `civilista-scadenze` | Termini civili con ragionamento esplicito — inclusi i termini **a ritroso**, dove la scadenza di sabato si anticipa invece di prorogarsi |
| `civilista-giurisprudenza` | Ricerca in KB con citazioni verificabili e copertura dichiarata |
| `civilista-verifica` | Controllo pre-deposito a 10 punti: citazioni, termini, decadenze, procedibilità, forma dell'atto |
| `civilista-atti` | Redazione degli atti: citazione, comparsa, memorie 171-ter, monitorio e opposizione, appello, cassazione, precetto, diffida |
| `civilista-adr` | Condizione di procedibilità: mediazione o negoziazione, effetti su prescrizione e decadenza, conduzione |
| `civilista-quantificazione` | Quanto si chiede e quanto costa: danno, interessi e rivalutazione, nota spese, rischio economico |
| `civilista-archivio` | Conversione e indicizzazione di nuove fonti nella KB |

**Otto schede di materia** in `KNOWLEDGE_BASE/06_SCHEDE_MATERIA/` (inadempimento, recupero crediti e decreto ingiuntivo, responsabilità extracontrattuale e sanitaria, danno da circolazione, locazioni e sfratti, condominio, famiglia): fatti costitutivi e onere della prova, termini, condizione di procedibilità, rito e competenza, difese dai due lati, quantificazione, errori ricorrenti. Senza numeri di sentenza — quelli si prendono dalla KB.

---

## Cosa c'è già, e perché conta

**10.080 massime civili indicizzate e citabili con riscontro testuale**, dal 2023 a **febbraio 2026**. Due fonti ufficiali e pubbliche dell'Ufficio del Massimario:

| Fonte | Periodo | Massime |
|---|---|---|
| *Rassegne annuali — Gli orientamenti delle Sezioni Civili* (3 volumi per anno) | 2023 e 2024 | 6.122 |
| *Rassegne mensili della giurisprudenza civile* | gennaio 2025 → febbraio 2026 | 3.958 |

Le due fonti si integrano perché il Massimario lavora su tempi diversi: **la Rassegna annuale consolida l'anno e arriva con 12-18 mesi di ritardo** (quella del 2024 è uscita l'8 gennaio 2026; la 2025 non esiste ancora), mentre le mensili escono a circa 4-5 mesi. Nella KB il periodo recente è quindi coperto dalle mensili, in attesa del consolidato.

Due lacune dichiarate, per onestà: **febbraio e marzo 2025 non risultano pubblicati** sul portale della Corte, e da marzo 2026 in poi le mensili non sono ancora uscite.

Ogni massima è raggiungibile così:

```
numero Rv  →  file .md  →  pagina  →  testo della massima
```

Esempio reale dalla KB:

> `Rv 671693-01` (p. 201) — Sez. 2, n. 13949/2024, Varrone
> *"Per quanto attiene alla compensazione volontaria, […] essa non richiede la certezza, liquidità ed esigibilità dei contrapposti crediti, come risulta dall'art. 1252 c.c., ma si fonda sull'accordo delle parti […]"*
> (2024 Massimario Civile Volume I, p. 201)

**Il principio è: ancora o astieniti.** Se una massima non è nella KB, il kit dichiara *"non presente in KB"* invece di ricostruirla a memoria. È la regola che distingue uno strumento professionale da un generatore di citazioni plausibili — un problema reale, sanzionato dalla stessa Cassazione.

**Nota sui dati personali.** Le Rassegne mensili riportano, sotto ogni massima, la riga delle parti (già ridotte a iniziali dalla fonte) con il **nome del difensore**. Nei Markdown pubblicati questi nominativi sono sostituiti con `[omissis]` — 8.813 occorrenze — tramite `oscura_difensori.py`. Restano i dati istituzionali della citazione (presidente, estensore, relatore, P.M.) e resta intatto tutto il resto: massima, estremi, classificazione, ancoraggio alle pagine.

---

## Perimetro dichiarato

Il kit lavora, in ordine di profondità: **obbligazioni, contratti e recupero crediti** · **responsabilità civile e danni** · **locazioni e condominio** · **famiglia e persone** (con l'avvertenza che il Tribunale unico per le persone, i minorenni e le famiglie non è ancora operativo).

Fuori perimetro, per ora: lavoro, tributario, crisi d'impresa, protezione internazionale.

---

## Installazione

Il kit si installa come plugin Cowork dal marketplace:

```
/plugin marketplace add Synthos-Logic/civilista-italia
```

Poi si copia la cartella di lavoro (`KNOWLEDGE_BASE/`, `FASCICOLI/`, `CLAUDE.md`) nella cartella dello studio e si compilano i dati in `CLAUDE.md`.

**I PDF delle Rassegne non sono versionati** (troppo grandi): la KB contiene i Markdown convertiti e gli indici, che è ciò che serve per citare. Per riscaricare i PDF originali, vedi `documentazione/FONTI_CIVILI.md`.

---

## Come si aggiunge una fonte

```bash
# metti il PDF in KNOWLEDGE_BASE/02_GIURISPRUDENZA/ e poi:
python3 skills/civilista-archivio/scripts/aggiorna_indice.py KNOWLEDGE_BASE
```

Conversione in Markdown, indice strutturale (concetto → pagina), registro citazionale (Rv → pagina → massima), registro fonti. Il tutto senza OCR: i PDF scansionati vengono segnalati e saltati.

---

## Documentazione

- `CLAUDE.md` — istruzioni operative e regole vincolanti
- `KNOWLEDGE_BASE/00_META/PROTOCOLLO_GROUNDING.md` — il protocollo quote-then-claim
- `KNOWLEDGE_BASE/00_META/GERARCHIA_FONTI.md` — come si pesano le fonti nel civile
- `documentazione/FONTI_CIVILI.md` — mappa verificata delle fonti civili aperte, con licenze e limiti

---

## Licenza e note d'uso

Codice e struttura: **MIT**.
I contenuti delle Rassegne sono documenti ufficiali della Corte di cassazione: riprodotti **citando la fonte** e **senza finalità commerciali**, come prescritto dalle note legali del portale della Corte. Il kit non redistribuisce banche dati soggette a restrizioni (Italgiure/SentenzeWeb è espressamente escluso).

*Di Synthos Logic. Gli atti prodotti dal kit sono sempre bozze soggette alla revisione del difensore.*
