# Kit Civilista Italiano

**Assistente operativo per avvocati civilisti italiani, con giurisprudenza ancorata e verificabile.**
Kit gemello del [Kit Penalista Italiano](https://github.com/Synthos-Logic/penalista-italia), da cui eredita l'impianto anti-allucinazione.

> **Versione 0.1 — kit in costruzione.** Contiene la Knowledge Base civile e la skill di archivio. Le skill operative (scadenze, atti, analisi del caso, giurisprudenza, verifica) sono in lavorazione e vengono rilasciate dopo la validazione sul campo.

---

## Cosa c'è già, e perché conta

**6.122 massime civili indicizzate e citabili con riscontro testuale.**
La KB è costruita sulle *Rassegne annuali della giurisprudenza di legittimità — Gli orientamenti delle Sezioni Civili* dell'Ufficio del Massimario della Corte di cassazione, anni **2023** e **2024** (3 volumi ciascuna, fonte ufficiale e pubblica).

Ogni massima è raggiungibile così:

```
numero Rv  →  file .md  →  pagina  →  testo della massima
```

Esempio reale dalla KB:

> `Rv 671693-01` (p. 201) — Sez. 2, n. 13949/2024, Varrone
> *"Per quanto attiene alla compensazione volontaria, […] essa non richiede la certezza, liquidità ed esigibilità dei contrapposti crediti, come risulta dall'art. 1252 c.c., ma si fonda sull'accordo delle parti […]"*
> (2024 Massimario Civile Volume I, p. 201)

**Il principio è: ancora o astieniti.** Se una massima non è nella KB, il kit dichiara *"non presente in KB"* invece di ricostruirla a memoria. È la regola che distingue uno strumento professionale da un generatore di citazioni plausibili — un problema reale, sanzionato dalla stessa Cassazione.

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
