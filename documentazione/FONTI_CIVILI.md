# Fonti civili aperte — mappa verificata
*Verifica diretta: 5 agosto 2026. Ogni voce indica contenuto, licenza/limiti e automatizzabilità.*

Questo documento è il presupposto della Knowledge Base: elenca da dove viene il materiale citabile
e, soprattutto, **cosa NON è utilizzabile**.

---

## 1. Rassegne annuali delle Sezioni Civili — fonte principale della KB

*"Rassegna annuale della giurisprudenza di legittimità — Gli orientamenti delle Sezioni Civili"*,
Ufficio del Massimario della Corte di cassazione, 3 volumi per anno.

**Anno 2024** (base `https://www.cortedicassazione.it`):
- `/resources/cms/documents/Volume_I_2024_Massimario_Civilevolume_completocop.pdf`
- `/resources/cms/documents/Volume_II_2024_Massimario_Civilevolume_completocop.pdf`
- `/resources/cms/documents/Volume_III_2024_Massimario_Civilevolume_completocop.pdf`

**Anno 2023**:
- `/resources/cms/documents/VOLUME_I__RASSEGNA_ANNUALE_2023_rev.05_definitiva.pdf`
- `/resources/cms/documents/VOLUME_II__RASSEGNA_ANNUALE_2023_rev.06definitiva.pdf`
- `/resources/cms/documents/VOLUME_III__RASSEGNA_ANNUALE_2023.pdf`

Le annate anteriori al 2023 non sono nell'archivio del portale (che parte da luglio 2023); sono
verosimilmente sul Portale del Massimario IPZS — **da verificare**.

⏱️ **Latenza da conoscere**: la Rassegna annuale esce **12-18 mesi dopo la fine dell'anno**
(2023 → pubblicata il 19/06/2024; 2024 → 08/01/2026). Al 5 agosto 2026 la **Rassegna 2025 non
esiste ancora** (URL sul pattern del 2024: 404). Il periodo scoperto si copre con le mensili.

---

## 1-bis. Rassegne MENSILI della giurisprudenza civile — copertura del periodo recente

Stessa serie `RLC`, un PDF al mese (talvolta bimestrale), pubblicato con **~4-5 mesi di ritardo**.
Sono la fonte che tiene aggiornata la KB tra un'annuale e l'altra. Quelle usate nella KB (gen 2025 → feb 2026):

| Periodo | contentId | Nome file sul portale |
|---|---|---|
| gennaio 2025 | RLC41722 | `Rassegna_mensile_GENNAIO_2025__Settore_civile.pdf` |
| aprile-maggio 2025 | RLC47282 | `Rassegna_mensile_APRILEMAGGIO_2025__Settore_civile_rev.2.pdf` |
| giugno 2025 | RLC42932 | `Rassegna_mensile_GIUGNO_2025__settore_civile.pdf` |
| luglio-agosto 2025 | RLC48748 | `Rassegna_mensile_LUGLIOAGOSTO_2025__Settore_civile.pdf` |
| settembre 2025 | RLC49223 | `Rassegna_mensile_SETTEMBRE_2025__Settore_civile.pdf` |
| ottobre 2025 | RLC49748 | `Rassegna_mensile_OTTOBRE_2026__Settore_civile.pdf` ⚠️ |
| novembre 2025 | RLC50218 | `Rassegna_mensile_NOVEMBRE_2025__Settore_civile_rev02.pdf` |
| dicembre 2025 | RLC50588 | `Rassegna_mensile_DICEMBRE_2025__Settore_civile.pdf` |
| gennaio 2026 | RLC50740 | `Rassegna_mensile_GENNAIO_2026__Settore_civile.pdf` |
| febbraio 2026 | RLC51130 | `Rassegna_mensile_della_giurisprudenza_di_FEBBRAIO_2026__Settore_civile.pdf` |

⚠️ **La mensile di ottobre 2025 è pubblicata con "OTTOBRE_2026" nel nome del file**: refuso della
fonte, verificato sul contenuto (provvedimenti del 01/10/2025 e 14/10/2025). In KB è archiviata come
`2025_10`.

⚠️ **Come vanno rinominati i PDF prima di indicizzarli.** Lo schema in KB è
`AAAA_MM_Rassegna_Mensile_Civile.pdf`, dove `MM` è il **mese di apertura** del fascicolo anche
quando ne copre due: aprile-maggio 2025 è `2025_04`, luglio-agosto 2025 è `2025_07`. Non usare
`2025_04-05`: la pipeline settimanale pubblica i file con il mese di apertura, e un nome diverso
in locale farebbe convivere due copie della stessa rassegna, con la stessa massima citata da
"due fonti". Dalla v0.8.1 `sincronizza_giurisprudenza.py` rimuove da sé le copie con nome
superato, ma se indicizzi un PDF a mano il nome corretto lo devi dare tu.

**Lacune della fonte**: **febbraio e marzo 2025 non risultano pubblicati**. Da marzo 2026 in poi le
mensili non sono ancora uscite (al 5/8/2026 l'ultima è febbraio 2026).

**I nomi dei file non seguono uno schema stabile** (`rev.2`, `rev02`, `mnesile` con refuso,
`Rassegna_mensile_della_giurisprudenza_di_…`): i link vanno letti dalle pagine di dettaglio
`rlc_dettaglio.page?contentId=RLC…`, non costruiti a mano.

⚠️ **Dato personale da trattare**: a differenza delle annuali, le mensili riportano sotto ogni massima
la riga delle parti con il **nome del difensore**. Prima di pubblicare i Markdown va eseguito
`skills/civilista-archivio/scripts/oscura_difensori.py`.

---

## 2. Fonti civili periodiche del portale della Cassazione

| Fonte | Pattern | Contenuto | Automatizzabile |
|---|---|---|---|
| **Pronunce civili segnalate** | `civile_dettaglio.page?contentId=SZC…`, lista `giurisprudenza_civile.page`, paginazione `?frame3_item=N` | ~300 pronunce da luglio 2023, con massima, esito in sintesi e **PDF oscurato** allegato; nessun nome di parte | **Sì** |
| **Rassegne e documenti civili** | `rlc_dettaglio.page?contentId=RLC…`, lista `relazioni_documenti_civile.page` | ~105 PDF: rassegna mensile civile, raccolta mensile delle ordinanze interlocutorie, rassegne tematiche (protezione internazionale, tributario), relazioni | **Sì** |
| **Rinvii pregiudiziali ex art. 363-bis c.p.c.** | prefisso `RPC`, lista `rinvii_pregiudiziali_ex_art.page` (URL di dettaglio a slug) | ~130 voci; è l'analogo funzionale delle "questioni pendenti" del settore penale | **Sì** |
| **Corte cost. segnalate / sovranazionale** | `QUC` e `QCI` | trasversali civile-penale | **Sì** |

⚠️ **Non esiste** un equivalente civile delle questioni SU pendenti penali (`QSP`): il canale
funzionalmente corrispondente è il rinvio pregiudiziale (`RPC`).

---

## 3. Corte costituzionale — open data

`https://dati.cortecostituzionale.it` — pronunce e massime dal **1956**, formati CSV/JSON/XML più
endpoint SPARQL, aggiornamento settimanale. **Licenza CC BY-SA 3.0**: è la fonte italiana con la
licenza più aperta.

Nota di sistema: **il dataset non è segmentato per materia** — contiene già il civile. Per questo
l'archivio della Consulta è condiviso tra kit penale e kit civile e non va duplicato.

---

## 4. Fonti europee

- **EUR-Lex / CGUE** — endpoint SPARQL Cellar (`https://publications.europa.eu/webapi/rdf/sparql`).
  Contenuti in CC BY 4.0, metadati CC0: **riuso ampio, anche commerciale, con attribuzione**.
  Rilevanza civile alta: consumatori, clausole abusive, GDPR, trasporto aereo.
- **Corte EDU — HUDOC** — esiste un endpoint JSON funzionante ma **non documentato** (è l'API interna
  del front-end): utilizzabile con prudenza, condizioni d'uso da verificare.

---

## 5. Quello che NON si può usare

- **Italgiure / SentenzeWeb** — le condizioni d'uso vietano espressamente la diffusione anche
  gratuita, la riproduzione, "l'elaborazione ed il loro reimpiego, **anche con sistemi di
  Intelligenza Artificiale**", e gli "accessi massivi" con spider. **Escluso senza eccezioni.**
- **Banca Dati di Merito pubblica (BDP)** — ~3,5 milioni di provvedimenti civili dal 2016 (esclusi
  famiglia, minori e stato della persona). Accesso **solo con SPID/CIE/CNS**, nessuna API, nessun
  export, host che rifiuta client non-browser. **Non automatizzabile**: la giurisprudenza di merito
  resta consultabile dall'avvocato ma fuori dalla KB. Esiste un canale di riuso (convenzione
  Ministero della Giustizia–AIE, 30 gennaio 2025) riservato agli editori.

---

## 6. Note legali del portale della Cassazione — vincolo da rispettare

> "Il sito web e i dati ivi contenuti possono essere utilizzati solo per uso personale […].
> La riproduzione dei testi forniti nel formato elettronico è consentita purché venga menzionata
> la fonte. In ogni caso, l'utente non può utilizzare o far utilizzare a fini commerciali a terzi
> il sito web e i dati ivi contenuti."

Conseguenza operativa: **riproduzione lecita citando la fonte, uso commerciale escluso.** Un kit
gratuito è coerente con questo regime; qualunque forma di monetizzazione, anche indiretta, va
valutata prima, non dopo.

---

## 7. Radar riviste — candidati civili con RSS verificato

*Judicium* · *Il Diritto Processuale Civile* · *Diritto Bancario* · *Diritto.it* · *Ius in Itinere*.

Molte testate civilistiche non hanno feed o sono protette da anti-bot (Persona e Danno, Jus Civile,
Diritto Civile Contemporaneo, Cammino Diritto). In ogni caso il radar indicizza **solo titolo,
autore, data e link**: mai il testo degli articoli, che è opera protetta dei singoli autori. Le voci
del radar **non sono citabili negli atti**: servono a sapere che se ne parla, non a fondare un'argomentazione.
