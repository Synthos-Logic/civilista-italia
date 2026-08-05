# Changelog — Kit Civilista Italiano

## [0.4.0] — 2026-08-05
Il set di skill e' completo: si passa dall'analisi alla produzione dell'atto.

### Aggiunto
- **`civilista-atti`** — redazione degli atti civili con struttura e template compilabile per dieci
  atti: citazione (art. 163, avvertimenti n. 7), comparsa di risposta (art. 167, quattro decadenze),
  memorie ex art. 171-ter (con la memoria a ‑20 marcata come scadenza critica per mezzi di prova e
  produzioni), ricorso per decreto ingiuntivo e opposizione ex art. 645, conclusionale e replica,
  appello (art. 342) e ricorso per cassazione (art. 366, autosufficienza, doppia conforme, art. 380-bis)
  — questi ultimi due con i modelli estesi in `references/atti-complessi.md` —, precetto, diffida e
  messa in mora. Ogni atto rimanda a `civilista-scadenze` per i termini e si chiude proponendo
  `civilista-verifica` prima del deposito.
- **`civilista-adr`** — condizioni di procedibilita': matrice materia → mediazione / negoziazione /
  nessuna, con esclusioni e regola dell'art. 5-bis sull'onere nell'opposizione a decreto ingiuntivo;
  effetti su prescrizione e decadenza; conseguenze della mancata partecipazione (art. 12-bis);
  conduzione del procedimento; rilievo tardivo. Checklist "prima di iniziare la causa".
- **`civilista-quantificazione`** — quanto si chiede e quanto costa: tabelle di Milano (ed. 2024) e
  Roma, Tabella Unica Nazionale macrolesioni (D.P.R. 12/2025, in vigore dal 5 marzo 2025) e
  micropermanenti; interessi e rivalutazione sui debiti di valore col metodo delle Sezioni Unite del
  1995; parametri forensi DM 55/2014 come modificato dal DM 147/2022; stima del rischio economico
  della causa e confronto con l'ipotesi transattiva.

### Regola mantenuta
Nessuna delle skill e delle schede contiene numeri di sentenza (unica eccezione: il richiamo
metodologico alle Sezioni Unite del 1995 sul calcolo di interessi e rivalutazione). Le massime si
prendono dalla Knowledge Base con `civilista-giurisprudenza`, sotto protocollo quote-then-claim.
Ogni valore numerico volatile porta fonte e data di verifica: nel civile questi numeri scadono.

## [0.3.0] — 2026-08-05
Il kit smette di essere un archivio e diventa operativo: cinque skill nuove e otto schede di materia.

### Aggiunto — skill
- **`civilista-inizia`** — avvio guidato su un caso reale. Il fascicolo civile ha campi propri: lato in
  cui stiamo (attore/convenuto), controparte e suo difensore, valore, materia, rito, autorita' adita,
  stato della condizione di procedibilita', prossima udienza e termini a ritroso pendenti.
- **`civilista-caso`** — analisi e strategia. Il cuore non e' smontare un'accusa ma la **tabella
  dell'onere della prova** (art. 2697 c.c.: fatto costitutivo / impeditivo / modificativo / estintivo,
  chi lo prova, con quale mezzo, "lo abbiamo?"), le preclusioni per atto, la condizione di
  procedibilita', prescrizione e decadenza, i punti deboli della NOSTRA posizione e la valutazione
  economica (spese di lite, rischio soccombenza, alternativa transattiva). Funziona da entrambi i lati.
- **`civilista-scadenze`** — riscritta da zero, non adattata dal penale. MODULO 0 vincolante: prima di
  ogni calcolo si stabilisce se il termine corre **in avanti o a ritroso**, se la materia e' esclusa
  dalla sospensione feriale e qual e' la data-evento con la sua prova. Regola cardine: nei termini a
  ritroso la scadenza che cade di sabato o festivo si **ANTICIPA**, non si proroga. Tre esempi svolti
  con date 2026, di cui uno che attraversa agosto e uno a ritroso che cade di sabato.
- **`civilista-giurisprudenza`** — ricerca ancorata sulla KB, con MODULO 0 sulla copertura reale
  (2023 - febbraio 2026, buco febbraio-marzo 2025) e formato di citazione distinto per rassegne
  annuali e mensili. La giurisprudenza di merito non e' in KB e il kit lo dichiara.
- **`civilista-verifica`** — controllo pre-deposito a 10 punti: citazioni con riscontro testuale,
  ricalcolo dei termini da zero, **decadenze e preclusioni**, condizione di procedibilita' documentata,
  conclusioni e domanda di spese, onere della prova, minimizzazione dei dati personali, requisiti
  formali di appello (art. 342) e cassazione (art. 366). Un solo esito bloccante ferma il deposito.

### Aggiunto — schede di materia
`KNOWLEDGE_BASE/06_SCHEDE_MATERIA/`, otto schede sul perimetro dichiarato: inadempimento contrattuale,
recupero crediti e decreto ingiuntivo, responsabilita' extracontrattuale, responsabilita' sanitaria,
danno da circolazione stradale, locazioni e sfratti, condominio, separazione-divorzio-figli.
Ognuna con fatti costitutivi e onere della prova, termini, condizione di procedibilita', rito e
competenza, difese tipiche dai due lati, quantificazione ed errori ricorrenti.
**Per scelta non contengono numeri di sentenza**: le massime stanno in KB e si citano da li'.

### Nota di metodo
Durante la revisione e' stata rimossa da `civilista-scadenze` una citazione ripresa da un commento
online e non riscontrabile in KB. Il kit chiede agli altri di non citare cio' che non puo' verificare:
vale prima di tutto per se stesso.

## [0.2.0] — 2026-08-05
La KB non si ferma piu' al 2024: copertura estesa fino a **febbraio 2026**.

### Aggiunto
- **10 Rassegne mensili della giurisprudenza civile** (gennaio 2025 → febbraio 2026),
  2.985 pagine convertite e indicizzate: **+3.958 massime**, per un totale di **10.080**
  massime citabili in KB (erano 6.122).
- `oscura_difensori.py` in `civilista-archivio`: le rassegne MENSILI riportano, sotto ogni
  massima, la riga delle parti con il **nome del difensore** ("E. (COGNOME NOME) contro E.").
  Lo script lo sostituisce con `[omissis]` prima della pubblicazione — **8.813 nominativi
  oscurati** — senza toccare massima, estremi, classificazione, presidente/estensore/relatore
  (dati istituzionali della citazione) ne' l'ancoraggio alle pagine.

### Corretto
- Regex del registro citazionale estesa alle **ordinanze interlocutorie** e ai decreti:
  le mensili citano `Sez. U, Ordinanza interlocutoria n. 26471 del 01/10/2025 (Rv. 676180-01)`,
  forma che il pattern precedente non riconosceva.
- I richiami "Massime precedenti Vedi: N. … del … Rv. …" delle mensili **non** vengono
  indicizzati come citazioni: sono rimandi, non massime presenti nel documento. E' voluto.

### Noto — copertura reale delle fonti
- La **Rassegna annuale 2025 non esiste ancora**: il Massimario consolida l'annata con
  12-18 mesi di ritardo (la 2023 e' uscita il 19/06/2024, la 2024 l'08/01/2026). Fino ad
  allora il 2025-2026 e' coperto dalle mensili.
- **Febbraio e marzo 2025 mancano alla fonte**: non risultano pubblicate sul portale.
- La mensile di ottobre 2025 e' pubblicata dalla Corte con il nome file "OTTOBRE_2026":
  refuso della fonte, verificato sul contenuto (provvedimenti del 01/10/2025 e 14/10/2025)
  e archiviata come `2025_10`.
- Le mensili non hanno struttura PARTE/CAPITOLO: il loro indice strutturale e' vuoto per
  costruzione, la ricerca per concetto si fa con `grep` sul `.md` o dal registro citazionale.

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
