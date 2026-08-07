# Changelog — Kit Civilista Italiano

## [0.8.3] — 2026-08-07

### Aggiunto — la pagina del progetto smette di sembrare un repository di codice
Il pubblico del kit sono avvocati, e la prima cosa che vedono aprendo GitHub non e' il README:
e' la lista dei file, il pulsante Code, i commit. Due interventi:

- **Pagina di presentazione** (`docs/index.html`, servita da GitHub Pages su
  `synthos-logic.github.io/civilista-italia`): una pagina vera, senza arredamento da
  programmatori, con il problema, un esempio di lavoro, il perimetro e l'installazione.
  **Non contiene numeri volatili** — niente conteggi di massime, niente numero di versione —
  perche' una pagina che invecchia in silenzio e' peggio di una pagina che non c'e';
- **Quattro immagini nel README** (`docs/img/`): intestazione, schema dell'installazione,
  catena della citazione `Rv → file → pagina → testo`, e uno **screenshot di lavoro reale**
  con l'apertura di un fascicolo per decreto ingiuntivo. Sono PNG e non SVG: GitHub sanifica
  gli SVG serviti dal repository e ne perde colori e stili.

Aggiunti anche quattro badge (versione, licenza, cadenza di aggiornamento, tempo di
installazione), presi da dati vivi dove possibile: quello della versione legge l'ultima release.


## [0.8.2] — 2026-08-06

### Aggiunto — pagina iniziale del progetto piu' utile a chi arriva per la prima volta
Il README descriveva il kit; ora lo **mostra**. Due aggiunte:
- **un caso di lavoro reale** — un decreto ingiuntivo appena notificato — con quello che il kit
  fa davvero: le tre date, il termine, la trappola della mediazione che non sospende, le istanze
  ex artt. 648 e 649, e una massima **presa dalla Knowledge Base con numero Rv e pagina**, non
  parafrasata;
- **l'installazione sulla pagina**, in tre passi numerati con quello che deve comparire a ogni
  passo, invece del solo rimando a `docs/INSTALLAZIONE.md` (che resta, per il dettaglio).

### Aggiunto — tolleranza al percorso nella sincronizzazione
`sincronizza_giurisprudenza.py` risolve i percorsi del repository dati attraverso un elenco di
candidati invece di un percorso fisso. Serve perche' GitHub reindirizza le rinomine di
*repository* ma **non i percorsi interni**: il giorno in cui la banca dati riorganizzasse le
cartelle (per esempio dando al penale il prefisso `PENALE/`, oggi assente, per simmetria con
`CIVILE/`), le installazioni gia' aggiornate non se ne accorgerebbero.

Il ripiego e' vincolato alla **stessa materia**, e per il civile c'e' di proposito un solo
candidato: se `CIVILE/SEGNALATE/` non esistesse, lo script si ferma con un errore esplicito
invece di ripiegare su `SEGNALATE/` di radice, che e' il penale. Riempire di sentenze penali
la Knowledge Base di un civilista, in silenzio, sarebbe molto peggio di un errore.

### Nota
La 0.8.1 e' stata pubblicata senza la tolleranza al percorso: arriva con questa versione.


## [0.8.1] — 2026-08-06
Correzioni emerse dalla verifica sul repository pubblicato.

### Corretto — conteggio doppio delle rassegne mensili dopo la sincronizzazione
Un fascicolo del Massimario puo' coprire due mesi (aprile-maggio, luglio-agosto). La pipeline
lo nomina con il mese di apertura (`2025_04`), il seed del kit lo nominava con il periodo intero
(`2025_04-05`). Alla prima sincronizzazione i due nomi convivevano: **stessa rassegna presente
due volte**, KB dichiarata a 11.647 massime invece di 10.080 e ogni ricerca che restituiva la
stessa massima da "due fonti" diverse. `sincronizza_giurisprudenza.py` ora elimina le versioni
locali con lo stesso prefisso `AAAA_MM` prima di copiare: la pipeline e' proprietaria di quei file.
Verificato su zona pulita.

### Corretto — testi disallineati
- `CLAUDE.md` dichiarava ancora "versione 0.4: nove skill, otto schede": ora dichiara la 0.8.1
  con dodici skill e dodici schede, **e l'elenco esplicito di cio' che resta fuori copertura**
  (sfratti passo passo, successioni e divisioni, esecuzione forzata oltre i fondamentali,
  licenziamenti collettivi, contratti tipici);
- il README delle schede di materia era fermo alla "versione 0.1";
- tre file citavano ancora `cassazione-penale-db`, nome del repository dati prima della rinomina
  (`PROTOCOLLO_GROUNDING.md`, `aggiorna_indice.py`, `indicizza_schede.py`).


## [0.8.0] — 2026-08-06
Il kit entra nelle tre materie che fanno la giornata di uno studio civile.

### Aggiunto — tre skill verticali
- **`civilista-monitorio`** — il ciclo completo del decreto ingiuntivo: quando conviene rispetto al
  rito semplificato o all'ordinario, prova scritta, provvisoria esecuzione ex art. 642, notifica e
  inefficacia, esecutorieta'. Dal lato del debitore: i 40 giorni (che **la domanda di mediazione non
  sospende**), l'inversione sostanziale dell'onere della prova, le istanze ex artt. 648 e 649 su cui
  si decide la partita nei primi trenta giorni, l'opposizione tardiva, e una **check-list dei primi
  sette giorni** dal ricevimento di un decreto.
- **`civilista-lavoro`** — licenziamenti con le **due fasi del termine** (60 giorni per l'impugnazione
  stragiudiziale, 180 per il deposito del ricorso: e' li' che si perdono le cause), regimi
  sanzionatori distinti per data di assunzione, rito lavoro dopo l'abrogazione del rito Fornero
  (artt. 441-bis ss.), crediti retributivi e mansioni, conciliazione in sede protetta, cenni al
  contenzioso previdenziale. **Le cause di lavoro non si sospendono nel periodo feriale**: e' scritto
  in tre punti diversi perche' e' l'errore piu' frequente.
- **`civilista-famiglia`** — la mappa delle strade (consensuale, giudiziale, negoziazione assistita,
  ufficiale di stato civile) con presupposti, tempi e quando conviene davvero; rito unificato
  473-bis con l'obbligo di deposito della documentazione economica; affidamento, mantenimento,
  ascolto del minore e curatore speciale; casa familiare e ordini di protezione. Include una regola
  di condotta: se emergono elementi di violenza domestica o rischio per minori, **si segnala
  all'avvocato e non si tratta come un contenzioso ordinario**.

### Aggiunto — quattro schede di materia
`E_LAVORO/LICENZIAMENTO.md`, `E_LAVORO/CREDITI_DI_LAVORO.md`,
`D_FAMIGLIA_E_PERSONE/MANTENIMENTO_E_AFFIDAMENTO.md`,
`A_CONTRATTI_E_CREDITI/OPPOSIZIONE_A_DECRETO_INGIUNTIVO.md`. Dodici schede in tutto.

### Corretto — audit di coerenza sui dati critici
Costruendo le nuove skill sono emerse due discordanze fra fonti secondarie, risolte sul testo
coordinato:
- **onere di attivare la mediazione nell'opposizione a decreto ingiuntivo**: `civilista-atti` lo
  attribuiva all'opponente; l'art. 5-bis D.Lgs. 28/2010 lo pone sul **ricorrente monitorio**. Corretto;
- **durata della mediazione**: e' di **sei mesi** (art. 6 modificato dal D.Lgs. 216/2024), non tre.
  Molte fonti online riportano ancora il testo previgente. Allineate tutte le occorrenze;
- confermato che nell'opposizione a decreto ingiuntivo i **termini di comparizione non sono piu'
  dimezzati per legge** (soppressione operata dalla L. 218/2011).

### Cambiato
- **Perimetro riscritto in ordine di frequenza reale**: monitorio, lavoro, famiglia, contratti,
  responsabilita' civile, locazioni e condominio. Il lavoro non e' piu' fuori perimetro.
- `/civilista-italia:versione` e `/civilista-italia:aiuto` aggiornati alle 12 skill.

## [0.7.0] — 2026-08-06
Documentazione d'installazione e comandi rapidi: il kit si puo' consegnare a un collega.

### Aggiunto
- **`docs/INSTALLAZIONE.md`** — guida passo passo scritta a parole, senza schermate: dove si trova
  ogni comando nell'app, cosa deve comparire a ogni passaggio, cosa fare quando non compare.
  Tre passi: plugin, cartella di lavoro, banca dati che si aggiorna da sola. Include la procedura
  di sblocco quando il catalogo del marketplace si congela, la sezione problemi comuni e la nota
  sulla convivenza con il Kit Penalista.
- **Comandi rapidi**: `/civilista-italia:versione` (confronta la versione installata con quella
  pubblicata, propone lo sblocco se il client e' rimasto indietro e **controlla anche la freschezza
  della banca dati**) e `/civilista-italia:aiuto` (guida rapida alle 9 skill in italiano piano).

## [0.6.0] — 2026-08-06
Arrivano i rinvii pregiudiziali: il kit sa anche cosa sta per essere deciso.

### Aggiunto
- **Rinvii pregiudiziali ex art. 363-bis c.p.c.** nella banca dati sincronizzata
  (`02_GIURISPRUDENZA/RINVII_PREGIUDIZIALI/`, 103 schede dal 2023): questioni rimesse alla Corte da
  giudici di merito — e anche da TAR, Corte dei conti e Corti di giustizia tributaria — con data
  dell'ordinanza, ufficio remittente, R.G. del giudizio a quo, materia e PDF ufficiale.
  Sono l'analogo civile delle questioni SU pendenti del kit penale.
- `sincronizza_giurisprudenza.py` scarica anche questa cartella.

### Regola d'uso (nella skill `civilista-archivio`)
Un rinvio **pendente non e' un precedente**: non si cita come autorita'. Serve a sapere che il punto
e' controverso e che la Corte si pronuncera'. Il quesito integrale sta nel PDF dell'ordinanza di
rimessione, non sulla pagina della Corte: si legge li', non si riassume.

## [0.5.0] — 2026-08-05
La Knowledge Base civile smette di essere statica: arriva il flusso settimanale.

### Aggiunto
- **`sincronizza_giurisprudenza.py`** in `civilista-archivio`: scarica le **pronunce civili
  segnalate** dal repo pubblico `Synthos-Logic/giurisprudenza-db` (aggiornato ogni lunedì da una
  GitHub Action) e l'archivio della Corte costituzionale, poi reindicizza la zona. Nessun account
  GitHub richiesto; cache git locale con aggiornamenti incrementali.
- Sezione dedicata nella skill `civilista-archivio`, con le avvertenze d'uso: la cartella
  `SEGNALATE/` e' della pipeline (le modifiche locali vengono sovrascritte), le segnalate non hanno
  ancora numero Rv, alcune schede portano piu' numeri (pronunce gemelle).

### Nota
Il seed della banca dati civile e' di **296 schede** (2023-2026). Da questo momento la KB ha due
binari: le Rassegne (stock consolidato, con Rv) e le segnalate (flusso settimanale, con PDF
ufficiale). La gerarchia delle fonti resta quella di `GERARCHIA_FONTI.md`: le Sezioni Unite
segnalate pesano come livello 1.

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
