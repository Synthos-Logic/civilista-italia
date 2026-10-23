---
name: civilista-atti
description: >
  Redazione di atti del processo civile italiano dopo la riforma Cartabia, con struttura, formule
  e preclusioni corrette per ciascun atto. ATTIVARE SEMPRE quando l'avvocato chiede di scrivere,
  redigere, preparare o bozzare un atto civile, o dice: 'scrivi la citazione', 'prepara la
  comparsa di risposta', 'prepara la comparsa di costituzione', 'scrivi la riconvenzionale',
  'redigi le memorie 171-ter', 'memoria a -20', 'ricorso per decreto ingiuntivo', 'opposizione a
  decreto ingiuntivo', 'chiedi la sospensione ex 649', 'scrivi la comparsa conclusionale',
  'memoria di replica', 'atto di appello', 'imposta i motivi di appello', 'ricorso per
  cassazione', 'prepara il precetto', 'scrivi la diffida', 'messa in mora', 'bozza l'atto', 'usa i
  miei atti come modello', 'segui il mio stile', 'scrivi come scrivo io', 'ricava il mio stile dai
  modelli'. Attivare anche quando l'analisi svolta con civilista-caso deve tradursi in un
  documento da depositare.
---

# civilista-atti — Redazione degli atti civili

Questa skill produce **bozze di atti civili** con la struttura, le formule e il registro
tecnico corretti. Nel civile la forma dell'atto non è cerimonia: è il luogo dove maturano le
**decadenze**. Ciò che non è dedotto nell'atto giusto non si deduce più.

Prima di scrivere, se il merito non è ancora stato analizzato, passa da `civilista-caso`
(qualificazione, onere della prova, preclusioni, procedibilità). Per ogni data e ogni
termine passa da `civilista-scadenze`: qui si dice *quale* termine rileva, lì si calcola.

---

## Regole vincolanti per ogni atto prodotto

1. **Nessun numero di sentenza inventato.** Se serve giurisprudenza, si cerca con
   `civilista-giurisprudenza` nella Knowledge Base e vale il protocollo **quote-then-claim**:
   massima incollata testualmente con `(fonte, p. N)`. Se non è in KB, si scrive
   **"non presente in KB"** e si argomenta il principio senza attribuirlo ad alcuna pronuncia.
   Mai ricostruire a memoria numeri di sentenza, numeri Rv o date di deposito.
2. **Nessun nome reale nei modelli.** I template usano segnaposto tra parentesi quadre.
   I dati delle parti li inserisce il difensore.
3. **Prima di redigere, cerca l'impostazione dello studio.** Se esistono `STILE_STUDIO.md` o
   `MODELLI/`, seguili e **dichiara su cosa ti sei basato**. Procedura completa nel modulo
   *Lo stile dello studio*, più sotto. Un atto corretto ma scritto con un'impostazione estranea
   viene riscritto a mano: è lavoro buttato.
4. **Deposito telematico** obbligatorio ai sensi dell'**art. 196-quater disp. att. c.p.c.**
   Il malfunzionamento del sistema non sospende i termini: programma il deposito con almeno
   un giorno lavorativo pieno di margine.
5. **Conclusioni numerate**, graduate (principale, subordinata, istruttoria, spese) e
   **coerenti** con le domande svolte in atto. La domanda di spese non si omette mai e va
   formulata in modo completo: spese, compensi, rimborso forfettario, C.P.A. e I.V.A.
6. **Valore della causa** sempre dichiarato ai fini del contributo unificato, con il
   criterio di determinazione.
7. **Ogni atto è una bozza.** Chiusura obbligatoria di ogni modulo: bozza soggetta alla
   revisione del difensore, e proposta di eseguire `civilista-verifica` prima del deposito.
8. **Distingui fatto allegato e fatto provato**, e per ogni fatto costitutivo indica il
   documento o il mezzo di prova che lo sostiene.

---

## Prima di scrivere — una sola domanda

Se questi dati non risultano già dal fascicolo o dall'analisi svolta, chiedili **tutti
insieme, una volta sola**. Se il fascicolo esiste in `FASCICOLI/<caso>/`, leggilo prima:
gran parte delle risposte è già lì.

- **Autorità adita**: Tribunale / Giudice di pace / Corte di appello / Corte di cassazione,
  sede e sezione; se noto, il giudice designato.
- **Parti e lato**: chi agisce e chi resiste, con dati completi (denominazione o generalità,
  sede o residenza, codice fiscale o P.IVA); **da che parte stiamo** (attore/convenuto,
  ricorrente/resistente, opponente/opposto, appellante/appellato).
- **Valore della causa** e criterio di determinazione (importo, valore del bene,
  indeterminabile), ai fini di scaglione, competenza e contributo unificato.
- **Materia**: contratti e recupero crediti / responsabilità e danni / locazioni e condominio /
  famiglia e persone.
- **Rito**: ordinario, semplificato di cognizione (art. 281-decies ss.), monitorio,
  cautelare, esecutivo, locatizio, di appello.
- **Documenti disponibili**, numerati come saranno prodotti, con l'indicazione di quelli
  mancanti da recuperare.
- **Termine o udienza di riferimento**: data di notifica ricevuta, udienza fissata, decreto
  ex art. 171-bis, scadenza di impugnazione.
- **Condizione di procedibilità**: mediazione o negoziazione assistita **non dovuta / da
  avviare / in corso / già esperita** (con verbale e data).
- **Dati del difensore e procura**: nome, foro, C.F., PEC, domicilio digitale, e se la procura
  è già rilasciata e in quale forma.

Se manca un dato non decisivo, procedi lasciando il segnaposto e segnalandolo in calce come
**da completare**. Se manca un dato decisivo (data di notifica, autorità, lato), chiedilo:
senza quello l'atto non si scrive.

---

## 1. ATTO DI CITAZIONE (art. 163 c.p.c.)

### Struttura dell'atto

| Parte | Contenuto | Riferimento |
|---|---|---|
| Intestazione | Tribunale adito; parti con generalità, sede/residenza e codice fiscale; difensore, procura, domicilio digitale | art. 163 nn. 1-2 |
| Oggetto della domanda | *Petitum* determinato: che cosa si chiede | art. 163 n. 3 |
| Esposizione dei fatti | Fatti in ordine cronologico, in modo **chiaro e specifico**, ciascuno agganciato al documento che lo prova | art. 163 n. 4 |
| Ragioni di diritto | Elementi di diritto costituenti le ragioni della domanda; qualificazione, norma, sussunzione | art. 163 n. 4 |
| Mezzi di prova e documenti | Indicazione specifica dei mezzi di prova e dei documenti offerti in comunicazione | art. 163 n. 5 |
| Conclusioni | Numerate e graduate, coerenti con il *petitum* e con la domanda di spese | art. 163 n. 4 |
| Vocatio in ius | Giorno dell'udienza, invito a costituirsi nel termine di legge, avvertimenti | art. 163 n. 7 |
| Procura, valore, elenco documenti | Procura; dichiarazione di valore per il contributo unificato; indice dei documenti prodotti | art. 163 n. 6 |

**Termine a comparire** (art. 163-bis c.p.c.): l'udienza va fissata rispettando i giorni
liberi di legge dalla notificazione — di regola 120 giorni, elevati in caso di notificazione
all'estero. Il calcolo della data di udienza si fa con `civilista-scadenze`, che verifica
giorni liberi, festivi e sospensione feriale. **Non fissare mai un'udienza a occhio**:
il termine a comparire insufficiente è vizio della vocatio in ius.

### Template

```
TRIBUNALE ORDINARIO DI [Città] — Sezione [ ] Civile

ATTO DI CITAZIONE

Per: [Denominazione o Nome Cognome], [sede/residenza in ], C.F./P.IVA [ ],
rappresentata e difesa dall'Avv. [Nome Cognome] (C.F. [ ], PEC [ ], fax [ ]),
giusta procura [in calce / a margine / su foglio congiunto al presente atto],
presso il cui domicilio digitale elegge domicilio           — ATTRICE

Contro: [Denominazione o Nome Cognome], [sede/residenza in ], C.F./P.IVA [ ]
                                                             — CONVENUTA

OGGETTO: [es. accertamento dell'inadempimento e condanna al pagamento di € ]
VALORE: € [ ]

I. IN FATTO
1. [Fatto — doc. 1]
2. [Fatto — doc. 2-3]
3. [Fatto — doc. 4; testimone sig. [ ] sul capitolo n. [ ]]
[...]

II. IN DIRITTO
1. [Qualificazione giuridica del rapporto e norma applicabile]
2. [Fatti costitutivi della domanda e loro sussistenza nel caso]
3. [Onere della prova: che cosa grava sull'attore e che cosa sul convenuto]
4. [Quantificazione della pretesa, criteri di calcolo, interessi e rivalutazione]
[Se serve giurisprudenza: cercarla con `civilista-giurisprudenza` e incollare la massima
dalla KB con (fonte, p. N). Se non è in KB: "non presente in KB".]

III. CONDIZIONE DI PROCEDIBILITÀ
[Mediazione ex art. 5 D.Lgs. 28/2010 / negoziazione assistita ex art. 3 D.L. 132/2014:
esperita con verbale del [data], doc. [ ] / non dovuta perché [ ].]

IV. MEZZI DI PROVA E DOCUMENTI (art. 163 n. 5)
Si producono i documenti indicati nell'elenco in calce.
Si chiede ammettersi prova per testi sui seguenti capitoli:
1) "Vero che [ ]" — teste [Nome], [residenza];
2) "Vero che [ ]" — teste [Nome], [residenza].
[Eventuale: CTU contabile/medico-legale; interrogatorio formale di [ ] sui capitoli che
precedono; ordine di esibizione ex art. 210 c.p.c.]

V. CONCLUSIONI
Voglia l'Ill.mo Tribunale adito, disattesa ogni contraria istanza ed eccezione:
1) accertare e dichiarare [ ];
2) per l'effetto, condannare [parte convenuta] al pagamento della somma di € [ ],
   oltre interessi [legali/moratori ex D.Lgs. 231/2002] dal [data] al saldo
   [ed eventuale rivalutazione];
3) in via subordinata, [domanda gradata];
4) in ogni caso, condannare [parte convenuta] alla rifusione delle spese di lite,
   oltre rimborso forfettario, C.P.A. e I.V.A. come per legge.

VI. CITAZIONE (art. 163 n. 7)
Tutto ciò premesso, [parte attrice] cita [parte convenuta] a comparire innanzi al
Tribunale di [Città], Sezione [ ], all'udienza del [data], ore di rito, davanti al
giudice designato ai sensi dell'art. 168-bis c.p.c., con invito a costituirsi nel
termine di settanta giorni prima dell'udienza indicata, ai sensi e nelle forme
stabilite dall'art. 166 c.p.c., con l'AVVERTIMENTO che:
- la costituzione oltre il suddetto termine implica le decadenze di cui agli
  artt. 38 e 167 c.p.c., e in particolare la decadenza dalle domande riconvenzionali,
  dalle eccezioni processuali e di merito non rilevabili d'ufficio e dalla facoltà
  di chiedere l'autorizzazione a chiamare in causa un terzo;
- la difesa tecnica mediante avvocato è obbligatoria in tutti i giudizi davanti al
  Tribunale, fatta eccezione per i casi previsti dall'art. 86 c.p.c. o da leggi speciali;
- la parte, sussistendone i presupposti di legge, può presentare istanza per
  l'ammissione al patrocinio a spese dello Stato.

Ai fini del contributo unificato si dichiara che il valore della presente causa è di
€ [ ], corrispondente allo scaglione [ ].

[Città], [data]                                    Avv. [Nome Cognome]

PROCURA ALLE LITI
Io sottoscritto/a [ ], C.F. [ ], delego a rappresentarmi e difendermi nel presente
giudizio, in ogni sua fase e grado, l'Avv. [Nome Cognome], conferendogli ogni facoltà
di legge, ivi compresa quella di [transigere, conciliare, incassare, nominare
sostituti], ed eleggo domicilio presso il suo studio in [ ]. Dichiaro di essere
stato informato ai sensi del Reg. UE 2016/679 e degli obblighi informativi in materia
di mediazione e di negoziazione assistita.
[Luogo], [data]  Firma [ ]  —  È autentica: Avv. [Nome Cognome]

ELENCO DOCUMENTI
1. [ ]   2. [ ]   3. [ ]
```

**Chiusura.** Bozza soggetta a revisione del difensore. Prima del deposito telematico,
esegui `civilista-verifica`.

---

## 2. COMPARSA DI COSTITUZIONE E RISPOSTA (art. 167 c.p.c.)

**È l'atto più pericoloso del processo civile per il convenuto.** Quattro attività si
compiono qui **a pena di decadenza**, e solo con costituzione tempestiva:

| Attività | Regola |
|---|---|
| **Presa di posizione specifica sui fatti** | Ogni fatto avverso va contestato **puntualmente**. La contestazione generica equivale a non contestazione: il fatto non contestato non va provato (art. 115 c.p.c.) |
| **Eccezioni non rilevabili d'ufficio** | Prescrizione, compensazione, eccezione di inadempimento, decadenza convenzionale, transazione, novazione: se non sollevate qui, sono perse anche se fondate |
| **Domande riconvenzionali** | Vanno proposte con le relative conclusioni e con i mezzi di prova |
| **Chiamata del terzo** | Dichiarazione nella comparsa, a pena di decadenza, con istanza di spostamento dell'udienza; il giudice provvede nelle verifiche preliminari (artt. 167 co. 3 e 269 c.p.c.) |

**Termine di costituzione**: almeno **70 giorni prima dell'udienza** indicata in citazione
(art. 166 c.p.c.). È un termine **a ritroso**: se la scadenza cade di sabato o in giorno
festivo, il termine si **anticipa** al giorno precedente non festivo, non si proroga.
Calcolo con `civilista-scadenze`, che va eseguito **prima** di iniziare la stesura.

### Template

```
TRIBUNALE ORDINARIO DI [Città] — Sezione [ ] Civile
R.G. n. [ ] — Udienza del [data] — Giudice dott./dott.ssa [ ]

COMPARSA DI COSTITUZIONE E RISPOSTA
con domanda riconvenzionale [e istanza di chiamata del terzo]

Per: [Parte convenuta], C.F. [ ], rappresentata e difesa dall'Avv. [ ], giusta procura
[in calce], PEC [ ]                                          — CONVENUTA

Contro: [Parte attrice], C.F. [ ]                            — ATTRICE

I. PREMESSA
Con atto di citazione notificato il [data], [parte attrice] ha convenuto in giudizio
[parte convenuta] chiedendo [sintesi fedele della domanda avversaria].
La domanda è infondata in fatto e in diritto, per le ragioni che seguono.

II. PRESA DI POSIZIONE SUI FATTI (art. 167 co. 1 c.p.c.)
Si contestano specificamente i seguenti fatti avversari:
- punto [n.] della citazione: si contesta che [ ]; risulta invece che [ ] — doc. [ ];
- punto [n.]: si contesta che [ ]; il documento richiamato ex adverso attesta [ ];
- punto [n.]: si contesta [ ].
Si dà atto, per contro, che risulta non controverso [ ].

III. ECCEZIONI PROCESSUALI
[Incompetenza (art. 38 c.p.c., con indicazione del giudice competente); difetto di
legittimazione; litispendenza; nullità della citazione; improcedibilità per mancato
esperimento della condizione di procedibilità.]

IV. ECCEZIONI DI MERITO NON RILEVABILI D'UFFICIO (a pena di decadenza)
1. Prescrizione: il diritto azionato si è prescritto in data [ ], essendo decorso il
   termine [decennale/quinquennale/biennale] ex art. [ ] c.c. dal [ ]; non risultano
   atti interruttivi ex art. 2943 c.c.
2. Eccezione di inadempimento ex art. 1460 c.c.: [ ].
3. Compensazione ex artt. 1241 ss. c.c.: [ ].
[Precisare per ciascuna i fatti su cui si fonda e i documenti che li provano.]

V. DOMANDA RICONVENZIONALE
[Fatti costitutivi della riconvenzionale, norma applicabile, quantificazione, documenti.]

VI. ISTANZA DI CHIAMATA DEL TERZO [se del caso]
Si dichiara di voler chiamare in causa [Terzo], C.F. [ ], in quanto [garanzia propria/
impropria; comunanza di causa], e si chiede che il Giudice, ai sensi degli artt. 167 co. 3
e 269 c.p.c., autorizzi la chiamata e fissi nuova udienza per consentirne la citazione.

VII. MEZZI DI PROVA E DOCUMENTI
[Documenti prodotti; capitoli di prova per testi; interrogatorio formale; CTU.]

VIII. CONCLUSIONI
Voglia l'Ill.mo Tribunale adito, respinta ogni contraria istanza:
1) in via preliminare, [dichiarare la propria incompetenza / l'improcedibilità];
2) nel merito, rigettare integralmente la domanda attorea perché infondata in fatto
   e in diritto;
3) in via subordinata, [domanda gradata: riduzione, compensazione];
4) in via riconvenzionale, condannare [parte attrice] a [ ];
5) in ogni caso, condannare [parte attrice] alla rifusione delle spese di lite, oltre
   rimborso forfettario, C.P.A. e I.V.A. come per legge.

Ai fini del contributo unificato si dichiara che il valore della domanda riconvenzionale
è di € [ ].

[Città], [data]      Avv. [Nome Cognome]      PROCURA — ELENCO DOCUMENTI
```

**Chiusura.** Bozza soggetta a revisione del difensore. Prima del deposito telematico,
esegui `civilista-verifica`, con controllo specifico sul rispetto del termine dei 70 giorni.

---

## 3. MEMORIE INTEGRATIVE (art. 171-ter c.p.c.)

Tre memorie, tutte con termine **a ritroso** rispetto all'udienza ex art. 183 c.p.c. e tutte
**a pena di decadenza**. I termini decorrono dal decreto di verifiche preliminari ex art.
171-bis co. 3 c.p.c., ma si computano a ritroso dall'udienza confermata o differita: appena
arriva il decreto, **ricalcola tutte e tre le date** con `civilista-scadenze`.

| Memoria | Termine | Che cosa va scritto **qui e solo qui** |
|---|---|---|
| **Prima** | **-40 giorni** | Domande ed eccezioni conseguenti alla riconvenzionale o alle eccezioni del convenuto o del terzo; precisazione e modificazione di domande, eccezioni e conclusioni già proposte; istanza di chiamata del terzo se l'esigenza è sorta dalle difese del convenuto |
| **Seconda** | **-20 giorni** | Replica alle domande ed eccezioni nuove o modificate; eccezioni conseguenti; **indicazione dei mezzi di prova e produzioni documentali** |
| **Terza** | **-10 giorni** | Replica alle eccezioni nuove; indicazione della sola **prova contraria** |

> **La memoria a -20 è la scadenza più pericolosa del processo civile.** Chi non indica lì i
> mezzi di prova e non produce lì i documenti **decade**: non li recupera più, salvo la sola
> prova contraria nella terza memoria. Segnalala sempre come scadenza critica nello
> scadenziario, con margine operativo di almeno un giorno lavorativo pieno.

Errore ricorrente: applicare a queste scadenze la proroga in avanti. Sono termini **a
ritroso**: sabato e festivo **anticipano**.

### Template (adattabile alle tre memorie)

```
TRIBUNALE ORDINARIO DI [Città] — Sezione [ ] Civile
R.G. n. [ ] — Giudice dott./dott.ssa [ ] — Udienza ex art. 183 c.p.c. del [data]

[PRIMA / SECONDA / TERZA] MEMORIA INTEGRATIVA EX ART. 171-TER C.P.C.
depositata nel termine di [40/20/10] giorni anteriori all'udienza

Per: [Parte], rappresentata e difesa dall'Avv. [ ]

--- PRIMA MEMORIA (-40) ---
I. DOMANDE ED ECCEZIONI CONSEGUENTI ALLE DIFESE AVVERSARIE
[Indicare da quale difesa avversaria discende ciascuna domanda o eccezione nuova.]
II. PRECISAZIONE E MODIFICAZIONE DI DOMANDE, ECCEZIONI E CONCLUSIONI
[Testo delle conclusioni come precisate o modificate.]
III. [Eventuale] ISTANZA DI CHIAMATA DEL TERZO, sorta dalle difese del convenuto.

--- SECONDA MEMORIA (-20) ---
I. REPLICA ALLE DOMANDE ED ECCEZIONI NUOVE O MODIFICATE
II. ECCEZIONI CONSEGUENTI
III. INDICAZIONE DEI MEZZI DI PROVA (a pena di decadenza)
1) Prova per testi sui seguenti capitoli:
   a) "Vero che [ ]" — teste [Nome], [residenza];
   b) "Vero che [ ]" — teste [Nome], [residenza].
2) Interrogatorio formale di [ ] sui capitoli che precedono.
3) CTU [contabile / medico-legale / tecnica] sul seguente quesito: [ ].
4) Ordine di esibizione ex art. 210 c.p.c. di [ ], in quanto [ ].
IV. PRODUZIONI DOCUMENTALI (a pena di decadenza)
Si producono i documenti nn. [ ]-[ ] indicati nell'elenco in calce.

--- TERZA MEMORIA (-10) ---
I. REPLICA ALLE ECCEZIONI NUOVE
II. INDICAZIONE DELLA PROVA CONTRARIA
Prova contraria per testi sui capitoli avversari nn. [ ], con i testi [ ].
[Nella terza memoria non si producono documenti nuovi né si articolano prove dirette.]

[Città], [data]      Avv. [Nome Cognome]      ELENCO DOCUMENTI
```

**Chiusura.** Bozza soggetta a revisione del difensore. Prima del deposito telematico,
esegui `civilista-verifica`: sulla seconda memoria il controllo è sulla completezza dei
mezzi di prova, perché è l'ultima occasione utile.

---

## 4. RICORSO PER DECRETO INGIUNTIVO (artt. 633 ss. c.p.c.)

### Presupposti da verificare prima di scrivere

- **Credito certo, liquido ed esigibile** avente per oggetto una somma di denaro, una
  determinata quantità di cose fungibili o una cosa mobile determinata (art. 633 c.p.c.).
- **Prova scritta** del credito (art. 634 c.p.c.): polizze e promesse unilaterali per
  scrittura privata, telegrammi anche non sottoscritti; per i crediti relativi a
  somministrazioni di merci e di denaro fatte da imprenditori che esercitano un'attività
  commerciale, gli **estratti autentici delle scritture contabili** regolarmente tenute.
  Per i crediti di professionisti e per quelli dello Stato e degli enti pubblici valgono le
  regole speciali degli artt. 635 e 636 c.p.c.
- **Documenti allegati al ricorso** (art. 638 c.p.c.): il ricorso deve indicare le prove che
  si producono e depositarle. Un ricorso monitorio senza i documenti è un ricorso rigettato.
- **Fatture**: da sole non bastano; vanno accompagnate dal titolo (contratto, ordine, DDT,
  corrispondenza di conferma) e, per l'imprenditore commerciale, dall'estratto autentico
  delle scritture contabili.

**Provvisoria esecuzione ex art. 642 c.p.c.** — due presupposti alternativi:

| Presupposto | Contenuto |
|---|---|
| **Comma 1** | Il credito è fondato su cambiale, assegno bancario o circolare, certificato di liquidazione di borsa, o su atto ricevuto da notaio o da altro pubblico ufficiale autorizzato |
| **Comma 2** | Vi è **pericolo di grave pregiudizio nel ritardo**, ovvero il ricorrente produce **documentazione sottoscritta dal debitore** comprovante il diritto fatto valere. Il giudice può imporre **cauzione** |

Il pericolo di grave pregiudizio va **allegato con fatti concreti** (crisi di liquidità del
debitore, protesti, procedure esecutive in corso, dismissione di beni): l'affermazione
generica non basta.

**Spese**: il giudice, con il decreto, liquida le spese e ne ingiunge il pagamento
(art. 641 c.p.c.). Vanno quindi chieste e quantificate nel ricorso, con la nota spese.

### Template

```
TRIBUNALE ORDINARIO DI [Città] — Sezione [ ] Civile
[oppure: GIUDICE DI PACE DI [Città]]

RICORSO PER DECRETO INGIUNTIVO
ex artt. 633 ss. c.p.c., con istanza di provvisoria esecuzione ex art. 642 c.p.c.

Per: [Ricorrente], [sede/residenza], C.F./P.IVA [ ], rappresentata e difesa dall'Avv. [ ],
giusta procura in calce, PEC [ ]                              — RICORRENTE

Contro: [Ingiungendo], [sede/residenza], C.F./P.IVA [ ]       — INGIUNGENDO

VALORE: € [ ]

I. IL RAPPORTO E IL CREDITO
1. In data [ ] le parti hanno concluso [contratto/ordine] — doc. 1.
2. La ricorrente ha eseguito la prestazione [descrizione] — doc. 2-4 (DDT, verbali).
3. Sono state emesse le fatture nn. [ ] del [ ], per complessivi € [ ] — doc. 5-8.
4. Le fatture sono rimaste impagate alla scadenza del [ ]; la ricorrente ha sollecitato
   il pagamento con [PEC/raccomandata] del [ ] — doc. 9, rimasta senza riscontro.
5. Il credito residuo ammonta a € [ ] in linea capitale.

II. LA PROVA SCRITTA (artt. 634 ss. c.p.c.)
Il credito è provato per iscritto da: [contratto sottoscritto — doc. 1; conferma d'ordine
— doc. 2; estratto autentico delle scritture contabili ex art. 634 co. 2 c.p.c. — doc. 10;
riconoscimento di debito del [data] — doc. 11].

III. INTERESSI
Sulle somme sono dovuti gli interessi [moratori ex D.Lgs. 231/2002, in quanto transazione
commerciale / legali ex art. 1284 c.c.] dalla scadenza di ciascuna fattura al saldo.
[Indicare il saggio applicato e la data di riferimento; il valore va riverificato.]

IV. ISTANZA DI PROVVISORIA ESECUZIONE (art. 642 c.p.c.)
[Comma 1: il credito è fondato su [titolo], doc. [ ].]
[Comma 2: sussiste pericolo di grave pregiudizio nel ritardo, in quanto [fatti concreti,
doc. ]; in subordine, si produce documentazione sottoscritta dal debitore comprovante il
diritto fatto valere (doc. [ ]).]
Si chiede pertanto che il decreto sia dichiarato provvisoriamente esecutivo.

P.Q.M.
La ricorrente chiede che l'Ill.mo Giudice adito voglia:
1) ingiungere a [Ingiungendo] di pagare alla ricorrente la somma di € [ ], oltre
   interessi [ ] dalla scadenza di ciascuna fattura al saldo effettivo;
2) dichiarare il decreto provvisoriamente esecutivo ex art. 642 c.p.c.;
3) condannare l'ingiungendo al pagamento delle spese e dei compensi della presente
   procedura, come da nota che si allega, oltre rimborso forfettario, C.P.A. e I.V.A.,
   con ingiunzione di pagamento ex art. 641 c.p.c.;
il tutto con l'avvertimento che, nel termine di quaranta giorni dalla notificazione,
può essere proposta opposizione e che, in mancanza, si procederà a esecuzione forzata.

[Città], [data]   Avv. [ ]   PROCURA — ELENCO DOCUMENTI — NOTA SPESE
```

**Chiusura.** Bozza soggetta a revisione del difensore. Prima del deposito telematico,
esegui `civilista-verifica`, con controllo sulla completezza della prova scritta allegata.

---

## 5. ATTO DI OPPOSIZIONE A DECRETO INGIUNTIVO (art. 645 c.p.c.)

### Punti che governano l'atto

- **Termine: 40 giorni** dalla notificazione del decreto (artt. 641 e 645 c.p.c.), salvo i
  termini abbreviati o prolungati disposti dal giudice. È perentorio: scaduto, il decreto
  diventa esecutivo (art. 647 c.p.c.). Calcolo con `civilista-scadenze`.
- **Forma**: atto di citazione davanti all'ufficio giudiziario cui appartiene il giudice che
  ha emesso il decreto; il giudizio prosegue secondo le norme del procedimento ordinario.
  I termini di comparizione **non sono più dimezzati per legge**: verificare il testo vigente
  dell'art. 645 c.p.c. prima di fissare l'udienza. Costituzione dell'opponente nel termine
  dell'art. 165 c.p.c.
- **Inversione sostanziale dei ruoli**: l'opponente è **attore in senso formale** ma
  **convenuto in senso sostanziale**; l'opposto è convenuto formale ma **attore sostanziale**
  e su di lui grava l'onere di provare i fatti costitutivi del credito (art. 2697 c.c.).
  Conseguenza pratica: nell'atto di opposizione vanno svolte **le difese del convenuto** —
  contestazione specifica dei fatti, eccezioni non rilevabili d'ufficio, eventuali domande
  riconvenzionali — e non basta affermare che il credito "non è dovuto".
- **Sospensione della provvisoria esecuzione (art. 649 c.p.c.)**: su istanza dell'opponente,
  quando ricorrono **gravi motivi**, il giudice, sentite le parti, con ordinanza non
  impugnabile può sospendere l'esecuzione provvisoria. I gravi motivi vanno allegati con
  fatti: fondatezza *prima facie* dell'opposizione e pregiudizio concreto dall'esecuzione.
- **Rischio speculare**: l'opposto può chiedere la provvisoria esecuzione in corso di causa
  ex art. 648 c.p.c. se l'opposizione non è fondata su prova scritta o di pronta soluzione.
  Impostare l'opposizione in modo da resistere anche a quella istanza.
- **Mediazione**: nei procedimenti per ingiunzione la condizione di procedibilità si esperisce
  **dopo** la pronuncia sulle istanze di concessione e di sospensione della provvisoria
  esecuzione. L'**onere di attivare la mediazione grava sul ricorrente per decreto ingiuntivo**, non sull'opponente (art. 5-bis D.Lgs. 28/2010): verifica il
  testo vigente dell'art. 5 D.Lgs. 28/2010 e metti la scadenza in scadenziario il giorno
  stesso dell'ordinanza. È un punto su cui le opposizioni si perdono in rito.

### Template

```
TRIBUNALE ORDINARIO DI [Città] — Sezione [ ] Civile

ATTO DI CITAZIONE IN OPPOSIZIONE A DECRETO INGIUNTIVO
ex art. 645 c.p.c., con istanza di sospensione della provvisoria esecuzione
ex art. 649 c.p.c.

avverso il decreto ingiuntivo n. [ ]/[anno], emesso dal Tribunale di [Città] in data
[ ] nel proc. R.G. n. [ ], notificato in data [ ]

Per: [Opponente], C.F. [ ], rappresentata e difesa dall'Avv. [ ]   — OPPONENTE
Contro: [Opposto], C.F. [ ]                                        — OPPOSTA

I. IL DECRETO OPPOSTO
Con il decreto in epigrafe, notificato il [data], è stato ingiunto all'opponente il
pagamento di € [ ], oltre interessi e spese, sul presupposto di [ ].
Il decreto è [provvisoriamente esecutivo ex art. 642 c.p.c. / non provvisoriamente esecutivo].
La presente opposizione è proposta nel termine di quaranta giorni dalla notificazione.

II. ECCEZIONI PRELIMINARI E DI RITO
[Incompetenza; difetto dei presupposti del procedimento monitorio; carenza di prova
scritta ex art. 634 c.p.c.; nullità della notificazione; difetto di legittimazione.]

III. CONTESTAZIONE SPECIFICA DEI FATTI POSTI A FONDAMENTO DEL RICORSO
[Punto per punto, con i documenti. Ricordare che l'onere della prova dei fatti costitutivi
grava sull'opposto, attore in senso sostanziale.]

IV. ECCEZIONI DI MERITO NON RILEVABILI D'UFFICIO
[Prescrizione; pagamento; eccezione di inadempimento ex art. 1460 c.c.; compensazione;
transazione; nullità o annullabilità del titolo; contestazione del quantum e degli interessi.]

V. [Eventuale] DOMANDA RICONVENZIONALE
[Fatti, norma, quantificazione, documenti.]

VI. ISTANZA DI SOSPENSIONE DELL'ESECUZIONE PROVVISORIA (art. 649 c.p.c.)
Ricorrono gravi motivi, in quanto: (i) l'opposizione è fondata su [ ], come risulta da
doc. [ ]; (ii) l'esecuzione produrrebbe il seguente pregiudizio concreto: [ ] — doc. [ ].
Si chiede pertanto che il Giudice, sentite le parti, sospenda l'esecuzione provvisoria
del decreto opposto.

VII. MEZZI DI PROVA E DOCUMENTI
[Documenti; capitoli di prova; CTU.]

VIII. CONDIZIONE DI PROCEDIBILITÀ
Si dà atto che la materia [rientra / non rientra] tra quelle soggette a mediazione
obbligatoria e che, in caso affermativo, l'opponente provvederà a introdurre il
procedimento nel termine di legge, decorrente dalla pronuncia sulle istanze ex artt.
648 e 649 c.p.c.

IX. CONCLUSIONI
Voglia l'Ill.mo Tribunale adito, respinta ogni contraria istanza:
1) in via preliminare, sospendere l'esecuzione provvisoria del decreto opposto
   ex art. 649 c.p.c.;
2) revocare e dichiarare nullo e/o privo di effetto il decreto ingiuntivo n. [ ]/[anno];
3) accertare e dichiarare che nulla è dovuto dall'opponente [o che è dovuta la sola
   somma di € ];
4) in via riconvenzionale, condannare l'opposta a [ ];
5) in ogni caso, condannare l'opposta alla rifusione delle spese di lite, oltre
   rimborso forfettario, C.P.A. e I.V.A. come per legge.

CITAZIONE
Si cita l'opposta a comparire innanzi al Tribunale di [Città] all'udienza del [data],
con invito a costituirsi nel termine di legge e con gli avvertimenti di cui all'art.
163 n. 7 c.p.c.

Ai fini del contributo unificato il valore della causa è di € [ ].

[Città], [data]   Avv. [ ]   PROCURA — ELENCO DOCUMENTI
```

**Chiusura.** Bozza soggetta a revisione del difensore. Prima del deposito telematico,
esegui `civilista-verifica`: il primo controllo è sul rispetto dei 40 giorni.

---

## 6. COMPARSA CONCLUSIONALE E MEMORIA DI REPLICA (fase decisoria)

Termini **a ritroso** rispetto all'udienza di rimessione della causa in decisione
(art. 189 c.p.c.): note di precisazione delle conclusioni **-60**, comparse conclusionali
**-30**, memorie di replica **-15**. Se il giudice adotta un modello alternativo
(artt. 275-bis o 281-sexies c.p.c.), i termini li fissa il provvedimento: leggilo e calcola
su quello. Calcoli con `civilista-scadenze`.

**Regola di contenuto.** La comparsa conclusionale **non introduce nulla di nuovo**: non
domande, non eccezioni, non documenti, non mezzi di prova. Riordina il materiale già
acquisito e lo collega alle conclusioni precisate. La memoria di replica **replica soltanto**
alle argomentazioni della conclusionale avversaria: chi vi introduce argomenti nuovi espone
la parte a rilievi e non ottiene nulla.

### Template — comparsa conclusionale

```
TRIBUNALE ORDINARIO DI [Città] — Sezione [ ] Civile
R.G. n. [ ] — Giudice dott./dott.ssa [ ]
Udienza di rimessione in decisione del [data]

COMPARSA CONCLUSIONALE
per [Parte], rappresentata e difesa dall'Avv. [ ]

I. SVOLGIMENTO DEL PROCESSO
[Sintesi essenziale: atti introduttivi, memorie, istruttoria svolta, conclusioni precisate.]

II. LE RISULTANZE ISTRUTTORIE
[Prova per prova: documento o deposizione, contenuto rilevante, fatto che ne risulta
provato. Indicare verbale e pagina. Distinguere il fatto provato dal fatto allegato.]

III. LA DOMANDA È FONDATA / INFONDATA
1. [Fatto costitutivo n. 1: provato da [ ]]
2. [Fatto costitutivo n. 2: provato da [ ]]
3. [Fatti non contestati ex art. 115 c.p.c.: [ ]]
4. [Eccezioni avversarie e loro infondatezza: [ ]]

IV. QUANTIFICAZIONE
[Criteri di calcolo, interessi, rivalutazione, con la data di riferimento dei valori usati.]

V. SPESE DI LITE
Si chiede la condanna alle spese secondo soccombenza, come da nota che si deposita;
si segnala, ai fini dell'art. 91 c.p.c., la proposta transattiva formulata in data [ ]
(doc. [ ]) e rifiutata dalla controparte.

VI. CONCLUSIONI
Si insiste nelle conclusioni precisate all'udienza del [data], che qui si intendono
integralmente riportate e trascritte:
1) [ ];  2) [ ];  3) spese, compensi, rimborso forfettario, C.P.A. e I.V.A. come per legge.

[Città], [data]      Avv. [Nome Cognome]
```

### Template — memoria di replica

```
[Stessa intestazione]

MEMORIA DI REPLICA
per [Parte]

I. REPLICA ALLA COMPARSA CONCLUSIONALE AVVERSARIA
1. Sull'argomento di cui a pag. [ ]: [replica puntuale].
2. Sull'argomento di cui a pag. [ ]: [replica puntuale].
[Nessuna domanda nuova, nessuna eccezione nuova, nessuna produzione documentale.]

II. CONCLUSIONI
Si insiste integralmente nelle conclusioni già precisate.

[Città], [data]      Avv. [Nome Cognome]
```

**Chiusura.** Bozza soggetta a revisione del difensore. Prima del deposito telematico,
esegui `civilista-verifica`, con controllo sulla coerenza tra conclusioni precisate,
conclusionale e nota spese.

---

## 7. ATTO DI APPELLO (art. 342 c.p.c.)

**Leggi `references/atti-complessi.md`, sezione 1, prima di redigere.** Lì trovano posto il
template completo, il test motivo per motivo, i termini collegati e gli errori che producono
inammissibilità.

Nucleo da non perdere di vista: l'appello si propone con **citazione** contenente le
indicazioni dell'art. 163 c.p.c., **deve essere motivato**, e la motivazione deve contenere,
**a pena di inammissibilità**, in modo **chiaro, sintetico e specifico**, per **ciascun
motivo**:

1. l'indicazione del **capo della decisione** impugnato;
2. l'indicazione delle **censure alla ricostruzione dei fatti** compiuta dal giudice di
   primo grado;
3. l'indicazione delle **violazioni di legge** denunciate e della **loro rilevanza** ai fini
   della decisione impugnata.

Struttura obbligatoria a **motivi numerati e separati**, ciascuno autosufficiente e chiuso
dalla statuizione che si chiede in riforma. Conclusioni numerate, coerenti con i motivi
sviluppati, con domanda di spese estesa a entrambi i gradi. Eventuale istanza di sospensione
dell'efficacia esecutiva ex art. 283 c.p.c. Nuovi mezzi di prova e nuovi documenti solo alle
condizioni dell'art. 345 c.p.c. Termini con `civilista-scadenze`.

**Chiusura.** Bozza soggetta a revisione del difensore. Prima del deposito telematico,
esegui `civilista-verifica`.

---

## 8. RICORSO PER CASSAZIONE (art. 366 c.p.c.)

**Leggi `references/atti-complessi.md`, sezione 2, prima di redigere.** Lì trovano posto il
template completo, la tabella dei motivi ex art. 360 c.p.c., la disciplina della doppia
conforme e della proposta di definizione accelerata, e gli errori che producono
inammissibilità o improcedibilità.

Nucleo da non perdere di vista — il ricorso deve contenere, **a pena di inammissibilità**:
indicazione delle **parti** e del **provvedimento impugnato**; **esposizione sommaria dei
fatti della causa**; **motivi** con l'indicazione delle **norme di diritto** su cui si
fondano; indicazione della **procura**, se conferita con atto separato; **specifica
indicazione degli atti processuali, dei documenti e dei contratti o accordi collettivi sui
quali il ricorso si fonda** (**autosufficienza**). Serve **procura speciale** posteriore alla
pubblicazione del provvedimento impugnato e sottoscrizione di avvocato iscritto nell'albo
per le giurisdizioni superiori (artt. 83 e 365 c.p.c.).

Due verifiche preliminari, entrambe da fare **prima** di scrivere i motivi:

- **Doppia conforme (art. 360 co. 4 c.p.c.)**: non è impugnabile ai sensi del n. 5 la
  sentenza d'appello che conferma la decisione di primo grado in relazione alle **medesime
  questioni di fatto**. Se la doppia conforme sussiste, il motivo ex n. 5 va abbandonato o
  riportato, ricorrendone i presupposti, sul n. 4 o sul n. 3.
- **Proposta di definizione accelerata (art. 380-bis c.p.c.)**: se arriva, informa per
  iscritto il cliente del rischio — mancata richiesta di decisione nel termine di legge
  equivale a rinuncia con estinzione; definizione conforme alla proposta espone alla
  responsabilità aggravata ex art. 96 co. 3 e 4 c.p.c. La scelta è del cliente e va messa
  agli atti.

Ricorda il **deposito entro venti giorni** dall'ultima notificazione, a pena di
improcedibilità (art. 369 c.p.c.): mettilo in scadenziario il giorno stesso della
notificazione, con `civilista-scadenze`.

**Chiusura.** Bozza soggetta a revisione del difensore, unico abilitato a sottoscriverla ove
iscritto all'albo speciale. Prima del deposito telematico, esegui `civilista-verifica`.

---

## 9. ATTO DI PRECETTO (artt. 480 ss. c.p.c.)

### Requisiti

- **Titolo esecutivo** esistente e azionabile (art. 474 c.p.c.): sentenza, decreto ingiuntivo
  esecutivo, verbale di conciliazione, scrittura privata autenticata per obbligazioni di
  somme di denaro, atto pubblico, altri titoli previsti dalla legge. Dopo la riforma non
  occorre più la spedizione in forma esecutiva: si notifica **copia attestata conforme**
  (art. 475 c.p.c. come modificato dal D.Lgs. 149/2022).
- **Notificazione del titolo e del precetto** (art. 479 c.p.c.); per il decreto ingiuntivo
  già notificato ed esecutivo si indica nel precetto il provvedimento che ne ha disposto
  l'esecutorietà (art. 654 c.p.c.).
- **Contenuto a pena di nullità** (art. 480 c.p.c.): indicazione delle parti; data di
  notificazione del titolo esecutivo se avvenuta separatamente, ovvero trascrizione integrale
  del titolo quando è richiesta dalla legge; **intimazione ad adempiere** entro un termine
  **non minore di dieci giorni**, salva l'autorizzazione ex art. 482 c.p.c., con
  l'avvertimento che in mancanza si procederà a esecuzione forzata.
- **Dichiarazione di residenza o elezione di domicilio** della parte istante **nel comune in
  cui ha sede il giudice competente per l'esecuzione**, con indicazione dell'indirizzo PEC
  del difensore. In mancanza, le opposizioni al precetto si propongono davanti al giudice del
  luogo di notificazione e le notificazioni si eseguono presso la cancelleria.
- **Avvertimento sul sovraindebitamento** (art. 480 c.p.c.): il debitore può, con l'ausilio
  di un organismo di composizione della crisi o di un professionista nominato dal giudice,
  porre rimedio alla situazione di sovraindebitamento concludendo un accordo con i creditori
  o proponendo un piano.
- **Termini**: dilatorio di **10 giorni** prima di iniziare l'esecuzione (art. 482 c.p.c.);
  il precetto perde efficacia se l'esecuzione non inizia entro **90 giorni** dalla
  notificazione (art. 481 c.p.c.). Calcoli con `civilista-scadenze`.

### Template

```
ATTO DI PRECETTO

Per: [Creditore], [sede/residenza], C.F./P.IVA [ ], rappresentato e difeso dall'Avv. [ ],
C.F. [ ], PEC [ ], giusta procura [ ], che dichiara di voler ricevere le comunicazioni
al predetto indirizzo PEC ed elegge domicilio in [Comune in cui ha sede il giudice
competente per l'esecuzione], via [ ], presso [ ]

Contro: [Debitore], [sede/residenza], C.F./P.IVA [ ]

PREMESSO CHE
- in forza di [titolo esecutivo: sentenza n. [ ] del [ ] del Tribunale di [ ], resa nel
  proc. R.G. n. [ ], in copia attestata conforme / decreto ingiuntivo n. [ ]/[anno]
  dichiarato esecutivo con provvedimento del [ ]], [Debitore] è tenuto a pagare
  la somma di € [ ];
- il titolo esecutivo è stato notificato in data [ ] / viene notificato unitamente al
  presente atto;
- nulla è stato corrisposto.

CONTEGGIO
Sorte capitale                                            € [ ]
Interessi [legali/moratori] dal [ ] al [ ]                € [ ]
Spese e compensi liquidati in titolo                      € [ ]
Spese di notifica del titolo e registrazione              € [ ]
Compensi del presente precetto                            € [ ]
TOTALE                                                    € [ ]
oltre interessi dalla data del presente atto al saldo, oltre spese successive occorrende.

SI INTIMA E SI FA PRECETTO
a [Debitore] di pagare, entro il termine di dieci giorni dalla notificazione del presente
atto, la somma complessiva di € [ ] come sopra dettagliata, mediante bonifico su
IBAN [ ] intestato a [ ],
CON L'AVVERTIMENTO che, in difetto, si procederà a esecuzione forzata a norma di legge,
con ogni conseguente aggravio di spese.
SI AVVERTE ALTRESÌ il debitore che può, con l'ausilio di un organismo di composizione
della crisi o di un professionista nominato dal giudice, porre rimedio alla situazione
di sovraindebitamento concludendo con i creditori un accordo di composizione della crisi
o proponendo agli stessi un piano.
Giudice competente per l'esecuzione: Tribunale di [Città].

[Città], [data]                          Avv. [Nome Cognome]
```

**Chiusura.** Bozza soggetta a revisione del difensore. Prima della notificazione esegui
`civilista-verifica`, con controllo sul conteggio, sul termine dilatorio di dieci giorni e
sul termine di novanta giorni di efficacia del precetto.

---

## 10. DIFFIDA E MESSA IN MORA STRAGIUDIZIALE

### Che cosa fa e come si prova

- **Costituzione in mora** (art. 1219 c.c.): intimazione o richiesta fatta per iscritto.
- **Effetto interruttivo della prescrizione** (artt. 2943-2945 c.c.): ogni atto di
  costituzione in mora interrompe la prescrizione; **dall'interruzione decorre un nuovo
  periodo integrale**. È l'effetto che rende la diffida uno strumento di gestione del
  termine, non solo di pressione.
- **La decadenza non si interrompe** con una diffida: si impedisce solo compiendo l'atto
  previsto (artt. 2964 e 2966 c.c.).
- **Prova della ricezione**: PEC con ricevuta di consegna, o raccomandata a/r con avviso di
  ricevimento. Una diffida senza prova di consegna non interrompe nulla di dimostrabile:
  conserva la ricevuta e numerala come documento.
- **Diffida ad adempiere ex art. 1454 c.c.**: se si vuole la risoluzione di diritto, il
  termine assegnato **non può essere inferiore a quindici giorni**, salvo diversa pattuizione
  o salvo che, per la natura del contratto o per gli usi, un termine minore sia congruo; va
  dichiarato espressamente che, decorso il termine, il contratto si intenderà risolto di
  diritto. Se manca questa dichiarazione, non è una diffida ad adempiere: è un sollecito.
- **Condizione di procedibilità**: la diffida non sostituisce mediazione o negoziazione
  assistita. Se la materia le richiede, indicalo nella lettera e mettile in programma.

### Template

```
[Carta intestata dello studio]

Racc. a/r anticipata via PEC / PEC [indirizzo]

Spett.le [Destinatario]
[sede/residenza]
C.F./P.IVA [ ]

[Città], [data]

Oggetto: diffida e messa in mora ex art. 1219 c.c. — [rapporto] —
[eventuale: diffida ad adempiere ex art. 1454 c.c.]

Il/La sottoscritto/a Avv. [Nome Cognome], del Foro di [ ], in nome e per conto di
[Cliente], C.F./P.IVA [ ], con sede/residenza in [ ], che mi ha conferito mandato,

PREMESSO CHE
1. in data [ ] le parti hanno concluso [contratto/rapporto], come da [documento];
2. [descrizione dell'adempimento dovuto e del termine];
3. alla data odierna [descrizione dell'inadempimento: mancato pagamento delle fatture
   nn. [ ], per complessivi € [ ]; mancata consegna; vizi denunciati il [ ]];
4. i solleciti del [ ] sono rimasti senza riscontro,

DIFFIDA E COSTITUISCE IN MORA

la S.V. / codesta Spett.le Società a provvedere, entro e non oltre [numero] giorni dal
ricevimento della presente, a [pagare la somma di € [ ], oltre interessi
[legali/moratori ex D.Lgs. 231/2002] dal [ ] al saldo / adempiere all'obbligazione di ],
mediante [bonifico su IBAN [ ] intestato a [ ]].

[Se diffida ad adempiere ex art. 1454 c.c., termine non inferiore a 15 giorni:]
Si dichiara espressamente che, decorso inutilmente il predetto termine, il contratto
si intenderà risolto di diritto ai sensi e per gli effetti dell'art. 1454 c.c., salvo
il risarcimento del danno.

In difetto, si procederà senza ulteriore avviso nelle sedi giudiziarie competenti, con
ogni conseguenza in ordine a spese, competenze e interessi, e con riserva di ogni ulteriore
azione a tutela delle ragioni del mio assistito.

La presente vale a ogni effetto di legge quale atto interruttivo della prescrizione
ai sensi degli artt. 2943 e 2945 c.c.

[Eventuale: si comunica che la materia è soggetta a [mediazione obbligatoria ex art. 5
D.Lgs. 28/2010 / negoziazione assistita ex art. 3 D.L. 132/2014], che verrà attivata in
mancanza di riscontro.]

Distinti saluti.
                                                   Avv. [Nome Cognome]

Allegati: [documenti a supporto]
```

**Chiusura.** Bozza soggetta a revisione del difensore. Prima dell'invio esegui
`civilista-verifica`, con controllo su destinatario, termine assegnato, prova della
ricezione e coerenza con il termine di prescrizione calcolato.

---

## Lo stile dello studio — scrivere come scrive l'avvocato

Un atto tecnicamente corretto ma scritto con un'impostazione che non è la sua costringe
l'avvocato a riscriverlo. Il kit **non ricava da solo uno stile** osservando i fascicoli: lavora
su ciò che gli viene indicato. Questa è la procedura per indicarglielo.

### Dove stanno i riferimenti

```
Civile-Italia/
├── STILE_STUDIO.md        ← la scheda di stile: ha la precedenza su tutto
└── MODELLI/               ← atti dello studio già depositati
    ├── <materia>/         ← sottocartelle facoltative, per materia o per rito
    └── ...
```

Entrambi sono **esclusi dal versionamento**: contengono il lavoro dello studio.

### Regola operativa, vincolante

Prima di redigere qualsiasi atto, **in quest'ordine**:

1. se esiste `STILE_STUDIO.md`, leggilo: è la fonte prevalente, perché è stata rivista
   dall'avvocato;
2. altrimenti, se esiste `MODELLI/` con un atto pertinente per tipo o materia, aprilo e
   seguine l'impostazione;
3. in mancanza di entrambi, usa l'impostazione predefinita di questa skill e **dillo una
   volta sola**, senza insistere: *"Non ho modelli dello studio: ho usato l'impostazione
   standard. Se mi indica due o tre atti già depositati, le prossime bozze seguiranno la sua."*

**Dichiara sempre su cosa ti sei basato**, in chiusura e in una riga: *"Impostazione presa da
`MODELLI/monitorio/opposizione_2025.docx`"* oppure *"Impostazione da `STILE_STUDIO.md`"*. È la
stessa logica dell'ancoraggio delle massime: l'avvocato deve poter risalire alla fonte di ciò
che legge, anche quando la fonte è un suo atto.

Lo stile riguarda **la forma, mai il contenuto**: non si trasportano da un modello fatti,
importi, nomi, numeri di ruolo o argomenti di merito. Si prendono la struttura, l'ordine
dell'esposizione, il registro e le formule.

### Costruire la scheda di stile

Quando l'avvocato lo chiede — *"ricava il mio stile dai modelli"*, *"impara come scrivo"* — o
quando `MODELLI/` contiene almeno tre atti e la scheda non esiste ancora, proponilo tu una volta.

Leggi gli atti in `MODELLI/` e scrivi `STILE_STUDIO.md` con queste voci, **solo quelle che i
modelli documentano davvero**:

| Voce | Che cosa registrare |
|---|---|
| Intestazione ed epigrafe | Come si apre l'atto, come si indicano parti e difensore, dove vanno PEC e codice fiscale |
| Ordine delle parti | In che sequenza compaiono fatti, diritto, istanze istruttorie, conclusioni |
| Esposizione dei fatti | Numerati o discorsivi, con o senza titoletti, in che tempo verbale |
| Trattazione in diritto | Come si introducono le norme, come si innestano le massime, se si usano note |
| Conclusioni | Formula di apertura, ordine delle domande, come si gradua il subordine, come si chiedono le spese |
| Formule ricorrenti | Aperture e chiusure che tornano in più atti, riportate testualmente |
| Lessico | Termini che l'avvocato usa e termini che evita sistematicamente |
| Lunghezza tipica | Cartelle per tipo di atto, come indicazione e non come vincolo |

**Vincolo di riservatezza, non negoziabile.** La scheda registra **come** si scrive, mai **che
cosa** si è scritto: nessun nome di parte, nessun numero di causa, nessun importo, nessun fatto
tratto dai modelli. Le formule si riportano con segnaposto tra parentesi quadre. È la scheda che
più facilmente verrà condivisa fra colleghi dello stesso studio, e deve poter circolare.

Chiudi dicendo che il file è **modificabile a mano**: se l'avvocato corregge una voce, da quel
momento vale la sua. La scheda non si riscrive da sola a ogni atto — si rigenera solo su
richiesta, quando i modelli cambiano.

### Quando l'avvocato corregge la bozza

Se indica una differenza rispetto alla sua impostazione — un'intestazione diversa, le conclusioni
in altro ordine — applicala per il resto della sessione e **proponi di annotarla in
`STILE_STUDIO.md`**, così non va ripetuta la volta dopo. È il modo in cui la scheda migliora:
dalle correzioni, non dalle congetture.

---

## Stile e chiusura del lavoro

- Italiano tecnico e asciutto. Periodi brevi, niente enfasi, niente avverbi di rinforzo.
  Nessuna polemica personale verso la controparte o il giudice.
- **Citazioni normative complete**: articolo, comma, codice. "art. 167 co. 2 c.p.c.",
  mai "art. 167".
- **Numerazione**: fatti numerati, motivi numerati, conclusioni numerate. Un atto che si
  legge a salti è un atto che si perde.
- **Segnaposto tra parentesi quadre** ovunque manchi un dato: mai inventare importi, date,
  numeri di R.G. o generalità.
- **Dati personali**: solo quelli necessari all'atto (minimizzazione). Niente dati di terzi
  non pertinenti.
- Al termine della redazione: aggiorna il fascicolo in `FASCICOLI/<caso>/` con il documento
  prodotto e i wikilink, riporta le scadenze emerse in [[SCADENZIARIO]] con
  `civilista-scadenze`, e **proponi sempre `civilista-verifica` prima del deposito**.
- Nessun atto prodotto da questa skill è depositabile così com'è: è una **bozza**, e la
  decisione e la responsabilità restano del difensore.
