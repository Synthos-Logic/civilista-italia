---
name: civilista-archivio
description: >
  Conversione di documenti (PDF, sentenze, atti, dottrina) in Markdown indicizzato
  per la Knowledge Base civile, e governo dell'INDICE della giurisprudenza. ATTIVARE quando
  l'avvocato dice: 'converti questo PDF', 'metti questa sentenza in memoria',
  'aggiungi alla knowledge base', 'indicizza le rassegne', 'trasforma in markdown',
  'carica il documento nella KB', 'aggiorna l'indice della giurisprudenza',
  'prepara il documento per la consultazione', 'converti la rassegna',
  'aggiungi la rassegna annuale', 'indicizza gli atti del fascicolo'. Attivare anche
  quando un documento PDF va consultato ripetutamente e conviene convertirlo una volta
  per risparmiare token. È la skill che alimenta il protocollo quote-then-claim:
  produce il materiale ancorabile su cui si fonda ogni citazione verificata.
---

# civilista-archivio — Conversione e indicizzazione della Knowledge Base

## Cosa fa

Trasforma documenti (in primis PDF a testo nativo: Rassegne del Massimario, sentenze,
atti di causa, dottrina) in **Markdown pulito con marcatori di pagina** e genera un **indice a
due livelli** che rende la KB interrogabile a basso costo di token e — soprattutto —
**ancorabile**: ogni citazione potrà essere ricondotta a un file e a una pagina reali.

Due ragioni per cui esiste:

1. **Economia di contesto.** Un PDF viene letto come immagine, costoso a ogni
   interrogazione. Il Markdown è testo: leggibile, *grep*-abile, riusabile a costo minimo.
2. **Guardrail anti-allucinazione.** L'indice è il presupposto del protocollo
   *quote-then-claim*: non si cita ciò che non è nell'indice.

## I due livelli dell'indice

- **Strutturale** (concetto → fonte : pagina): PARTE / SEZIONE / CAPITOLO con il loro
  titolo-concetto e la pagina di inizio nel corpo. Serve a **navigare per argomento**
  (es. "CAPITOLO X — LE OBBLIGAZIONI IN GENERALE", "CAPITOLO VIII — COMUNIONE E CONDOMINIO").
- **Citazionale** (Rv → fonte : pagina → massima): ogni sentenza realmente presente,
  con numero Rv, pagina e citazione testuale. È il **backbone del grounding**.

Indice master e Markdown convertiti vivono in `KNOWLEDGE_BASE/_INDICE/`
(zona GLOBALE) oppure in `FASCICOLI/<caso>/_INDICE/` (zona di causa).

## Come si aggiorna una zona (uso normale)

```bash
# 1) metti i PDF nella zona, es. KNOWLEDGE_BASE/02_GIURISPRUDENZA/
# 2) converti + indicizza + rigenera indice e registro, in un colpo solo:
python3 skills/civilista-archivio/scripts/aggiorna_indice.py KNOWLEDGE_BASE

# stessa cosa per un fascicolo:
python3 skills/civilista-archivio/scripts/aggiorna_indice.py FASCICOLI/<caso>
```

Converte solo i PDF nuovi o modificati; gli altri li salta.

## Uso puntuale (un singolo documento)

```bash
python3 skills/civilista-archivio/scripts/converti_indicizza.py \
    <input.pdf> KNOWLEDGE_BASE/_INDICE/ --titolo "Etichetta leggibile della fonte"

python3 skills/civilista-archivio/scripts/genera_indice_master.py \
    KNOWLEDGE_BASE/_INDICE/ KNOWLEDGE_BASE/_INDICE/INDICE.md
```

Dipendenza: `pdfplumber` (`pip install pdfplumber`).

## Le fonti civili da cui partire

La KB del kit nasce da due serie ufficiali dell'Ufficio del Massimario:

- **Rassegne annuali — Gli orientamenti delle Sezioni Civili** (3 volumi per anno): l'orientamento
  consolidato, ma pubblicate con **12-18 mesi di ritardo**;
- **Rassegne mensili della giurisprudenza civile**: le massime del mese, con ~4-5 mesi di ritardo —
  sono ciò che copre il periodo per cui l'annuale non è ancora uscita.

Gli URL e le altre fonti civili aperte (pronunce segnalate, rinvii pregiudiziali ex art. 363-bis,
open data della Corte costituzionale) sono elencati con licenze e limiti in
`documentazione/FONTI_CIVILI.md`.

## Prima di pubblicare o condividere i Markdown: oscurare i difensori

Le **rassegne mensili** riportano sotto ogni massima la riga delle parti nella forma
`E. (COGNOME NOME) contro A. (COGNOME NOME)`: le parti sono già ridotte a iniziale dalla fonte,
i **difensori no**. Prima di pubblicare o inviare i `.md`:

```bash
python3 skills/civilista-archivio/scripts/oscura_difensori.py KNOWLEDGE_BASE/_INDICE
# --dry-run per contare senza scrivere
```

Sostituisce il nominativo con `[omissis]` e lascia intatti massima, estremi, classificazione,
presidente/estensore/relatore/P.M. (dati istituzionali della citazione) e l'ancoraggio alle pagine.
**Non usarlo sui documenti di causa di un fascicolo**: lì i nomi servono.

Quando l'avvocato porta materiale proprio (sentenze di merito, pareri, atti di causa),
va indicizzato **nella zona giusta**: la giurisprudenza generale in `KNOWLEDGE_BASE/`,
il materiale di una causa in `FASCICOLI/<caso>/` — lo scoping è per costruzione.

## Limiti — leggere con attenzione

- **NON fa OCR.** Se il PDF è una scansione (poco testo estraibile) lo script si ferma
  e lo segnala: va prima passato per un OCR. Non convertire mai una scansione "alla cieca".
- L'estrazione strutturale è tarata sulle Rassegne **annuali** (PARTE/SEZIONE/CAPITOLO).
  Nei volumi annuali il sommario di ciascuna parte viene talvolta indicizzato **due volte**
  (voce del sommario + voce del corpo, a pagine consecutive): è rumore noto, non un errore
  di ancoraggio. Le Rassegne **mensili** non hanno quella struttura: il loro indice strutturale
  è vuoto per costruzione e la ricerca per concetto si fa con `grep` sul `.md` o dal registro
  citazionale (che per le mensili è ricco: ogni massima porta la sua classificazione per materia).
- L'indice citazionale riconosce **tre forme reali**:
  annuale civile `Sez. 2, n. 13949/2024, Varrone, Rv. 671693-01`;
  mensile civile `Sez. U, Ordinanza interlocutoria n. 26471 del 01/10/2025 (Rv. 676180-01)`;
  penale `Sez. 3, n. 23006 del 22/06/2026, Rossi, Rv. …`.
  Più le varianti (`Sez. U.`, `S.U.`, `Sez. 6 - L`, relatore andato a capo, "n. … del 2024").
  Copertura misurata sulla Rassegna annuale 2024 vol. I: **1.178 su 1.207 occorrenze "Rv."**.
- **I richiami non sono citazioni.** Nelle mensili il blocco "*Massime precedenti Vedi: N. … del …
  Rv. …*" rimanda a precedenti che non stanno in quel documento: **non** vengono indicizzati, ed è
  voluto — il registro citazionale deve contenere solo massime realmente leggibili alla pagina
  indicata. Restano fuori, per la stessa ragione, i richiami *orfani* "*la medesima decisione (Rv. …)*".
- **Tutto il prodotto è materiale di lavoro**: la conversione non sostituisce la lettura
  della fonte ufficiale da parte dell'avvocato.

## PROTOCOLLO quote-then-claim (grounding obbligatorio)

Quando si cita giurisprudenza che dovrebbe essere nella KB, l'ordine è vincolante:

1. **Cerca prima nell'indice.** Per concetto → indice strutturale o `grep` sul `.md`.
   Per una sentenza → `grep` del numero Rv o della parte nel registro citazionale.
2. **Vai alla pagina e leggi.** Apri il `.md` al marcatore `<!-- pag. N -->` indicato.
3. **Incolla la massima testuale**, con l'indicazione `(fonte, p. N)`. Si afferma solo
   ciò che si è letto.
4. **Se non è nell'indice → si dichiara "non presente in KB".** NON si cita a memoria,
   NON si "ricostruisce" il numero. L'astensione è il comportamento corretto: meglio
   un buco dichiarato che una citazione inventata.

> Regola d'oro: **ciò che non è nell'indice non esiste**, ai fini della citazione.
> L'avvocato verifica comunque sulla banca dati ufficiale prima del deposito.
