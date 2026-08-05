---
name: civilista-caso
description: >
  Analisi del caso civile e costruzione della strategia processuale, dal lato attivo e dal lato
  passivo. ATTIVARE SEMPRE quando l'avvocato porta una vicenda civile, un contratto, una diffida,
  un atto di citazione ricevuto, un decreto ingiuntivo, una richiesta risarcitoria, o dice:
  'analizza questa causa', 'che strategia adottiamo', 'conviene agire', 'conviene resistere',
  'ci hanno citato in giudizio', 'ci hanno notificato un decreto ingiuntivo', 'facciamo opposizione?',
  'abbiamo ragione?', 'chi deve provare cosa', 'come impostiamo la citazione', 'come impostiamo
  la comparsa', 'quali eccezioni possiamo sollevare', 'e ancora in tempo?', 'e prescritto?',
  'quanto ci costa questa causa', 'conviene transigere', 'quanto rischiamo di spese',
  'serve la mediazione prima di agire', 'valutazione del caso', 'parere sulla causa'.
  E la skill centrale del kit civile: usarla ogni volta che si entra nel merito di una vicenda,
  prima di scrivere qualsiasi atto.
---

# civilista-caso — Analisi del caso e strategia civile

Nel penale si smonta un'accusa. Nel civile no: si costruisce (o si smonta) una **pretesa**, e la
si costruisce con i fatti che si riesce a **provare**, entro le **finestre processuali** che sono
ancora aperte, a un **costo** che deve avere senso per il cliente.

Tre domande governano tutto e vanno tenute insieme per l'intera analisi:
1. **Chi deve provare cosa** (art. 2697 c.c.)?
2. **Entro quale atto** va fatto ciò che serve?
3. **Quanto costa avere ragione**, e in quanto tempo?

Vale il **PROTOCOLLO quote-then-claim**: ogni riferimento giurisprudenziale passa da
`civilista-giurisprudenza` e dalla KB. Ciò che non è in KB si dichiara "non presente in KB".

---

## Prima di iniziare — raccolta in un'unica domanda

Se l'avvocato non ha già dato queste informazioni, chiedile **tutte insieme, una volta sola**.
Non fare interrogatori a tappe.

- **Da che lato stiamo**: attore o convenuto (ricorrente/resistente; opponente/opposto se c'è un
  decreto ingiuntivo). È la prima cosa: cambia l'intera analisi.
- **I fatti**, in ordine cronologico, e **i documenti disponibili** (contratto, fatture, e-mail,
  PEC, perizie, referti, verbali, bonifici). Distinguere ciò che si ha in mano da ciò che si
  dovrebbe recuperare.
- **Il valore della causa** e come è determinato (importo richiesto, valore del bene, indeterminato).
- **La materia** (contratti e recupero crediti / responsabilità e danni / locazioni e condominio /
  famiglia e persone).
- **I rapporti già intercorsi**: diffide, solleciti, contestazioni, trattative, proposte
  transattive, riconoscimenti di debito, pagamenti parziali.
- **Termini o udienze già fissati**: notifiche ricevute, date d'udienza, termini di costituzione,
  scadenze di impugnazione.
- **Condizione di procedibilità**: mediazione o negoziazione assistita già esperita, in corso, o
  mai avviata.

Se il materiale basta, procedi senza chiedere. Se manca un elemento decisivo (es. la data di notifica)
procedi comunque, segnalando l'assunzione fatta e marcandola come **da confermare**.

---

## Struttura dell'analisi

Le otto sezioni che seguono vanno prodotte **sempre e in quest'ordine**. Nessuna si salta, anche
se breve. Dove il ragionamento cambia a seconda del lato, il cambio va **detto esplicitamente**.

---

### 1. QUALIFICAZIONE GIURIDICA E NORMA APPLICABILE

In poche righe: che vicenda è, quale norma la governa, quale diritto si fa valere (o quale pretesa
si contesta), quale sarebbe la domanda giudiziale (o l'eccezione).

**Segnala sempre le qualificazioni alternative.** Nel civile la qualificazione non è un'etichetta:
sposta la prescrizione e l'onere della prova. Casi ricorrenti:

| Qualificazione | Effetto su prescrizione | Effetto su onere della prova |
|---|---|---|
| **Responsabilità contrattuale** (art. 1218 c.c.) | Ordinaria decennale, salvo termini speciali | Il creditore prova il titolo e allega l'inadempimento; **il debitore prova** l'adempimento o l'impossibilità non imputabile |
| **Responsabilità extracontrattuale** (art. 2043 c.c.) | Quinquennale (art. 2947 c.c.); biennale per danno da circolazione di veicoli | **Il danneggiato prova** fatto, colpa, nesso e danno |
| **Contatto sociale / obblighi di protezione** | Regime contrattuale | Regime contrattuale, più favorevole al danneggiato |
| **Responsabilità da cose in custodia** (art. 2051 c.c.) | Quinquennale | Custode responsabile salvo prova del **caso fortuito**: si sposta su di lui |
| **Indebito / arricchimento senza causa** (artt. 2033, 2041 c.c.) | Decennale | Chi ripete prova il pagamento e la mancanza di causa |

Dal lato attivo: scegliere la qualificazione che dà il regime probatorio migliore, e **cumulare le
domande** dove è possibile (in via principale e in subordine). Dal lato passivo: attaccare la
qualificazione avversaria è spesso il primo colpo utile — riqualificare da contrattuale a
extracontrattuale può far cadere la pretesa per prescrizione o rovesciare l'onere della prova.

Se la qualificazione dipende da un orientamento giurisprudenziale, **cercalo in KB** con
`civilista-giurisprudenza` e cita la massima con la pagina. Non affermare orientamenti a memoria.

---

### 2. ONERE DELLA PROVA (art. 2697 c.c.) — il cuore dell'analisi

Questa sezione è il centro del lavoro civile: una causa si vince e si perde qui. Va prodotta
**sempre in forma di tabella**, e la colonna "lo abbiamo?" va compilata con onestà.

| Fatto | Tipo | Chi lo prova | Con quale mezzo | Lo abbiamo? |
|---|---|---|---|---|
| [es. conclusione del contratto] | costitutivo | attore | doc. 1 — contratto sottoscritto | Sì |
| [es. esecuzione della prestazione] | costitutivo | attore | doc. 3-5 — DDT, testi | Parziale — manca la ricezione |
| [es. pagamento] | estintivo | convenuto | quietanza, estratto conto | Non risulta |
| [es. eccezione di inadempimento] | impeditivo | convenuto | contestazioni via PEC, CTU | Da valutare |
| [es. transazione intervenuta] | modificativo | convenuto | accordo scritto | No |

Regole di compilazione:

- **Costitutivi** all'attore; **impeditivi, modificativi ed estintivi** al convenuto. La sequenza
  logica è questa e va rispettata anche quando è scomoda.
- Per ogni riga indicare il **mezzo di prova concreto**: documento (con numero di produzione),
  testimone (con il capitolo che dovrà provare), CTU, interrogatorio formale, confessione,
  presunzioni, giuramento. "Si proverà in giudizio" non è un mezzo di prova.
- **Fatti non contestati**: ciò che la controparte non contesta specificamente non va provato
  (art. 115 c.p.c.). Dal lato passivo questo impone una **contestazione specifica** di ogni fatto
  avverso: la contestazione generica equivale a non contestazione. È uno degli errori più costosi
  del convenuto.
- **Presunzioni e inversioni legali** vanno segnalate: art. 2051 (custodia), art. 2054 (circolazione),
  art. 1218 (inadempimento), art. 2050 (attività pericolose). Spostano il baricentro dell'intera causa.
- **Prova mancante = punto debole**, e va riportato nella sezione 6. Non arrotondare.

**Simmetria dei lati.** Dal lato attivo la tabella dice **cosa dobbiamo documentare prima di
agire**: se le righe costitutive non sono coperte, la causa non è pronta. Dal lato passivo dice
**dove attaccare**: il modo più economico di vincere è dimostrare che l'attore non ha provato un
fatto costitutivo, senza dover provare nulla di proprio.

---

### 3. PRECLUSIONI E FINESTRE PROCESSUALI

Nel civile un'eccezione fondata ma tardiva è un'eccezione persa. Questa sezione dice **cosa va
fatto entro quale atto** e **cosa è già precluso**.

Struttura la risposta su due colonne: *ancora possibile* / *già precluso*, con l'atto di riferimento.

Punti da verificare sempre (rito ordinario post-Cartabia):

- **Atto di citazione**: domande, *editio actionis*, indicazione dei mezzi di prova e dei documenti,
  avvertimenti di legge. Un vizio qui si paga per tutto il processo.
- **Comparsa di costituzione e risposta** (art. 167 c.p.c., a pena di decadenza entro il termine di
  costituzione): **domande riconvenzionali**, **eccezioni non rilevabili d'ufficio**, chiamata di
  terzo (istanza al giudice). Queste tre cose, se non fatte lì, non si fanno più.
- **Memorie integrative ex art. 171-ter c.p.c.** (le tre finestre a ritroso rispetto alla prima
  udienza): precisazioni e modifiche delle domande, nuove prove e documenti, prova contraria.
  Verificare quale finestra è ancora aperta.
- **Eccezioni rilevabili d'ufficio** (es. nullità del contratto) vs **eccezioni in senso stretto**
  (es. prescrizione, compensazione, eccezione di inadempimento): solo le prime sfuggono alla
  decadenza. La **prescrizione non è rilevabile d'ufficio**: se non eccepita nei termini, è persa.
- **Opposizione a decreto ingiuntivo**: i ruoli sostanziali sono invertiti (l'opponente è convenuto
  in senso sostanziale) e i termini sono stretti. Verificare subito la data di notifica del decreto
  e l'eventuale provvisoria esecutorietà.
- **Impugnazioni**: termine breve dalla notifica della sentenza, termine lungo dalla pubblicazione,
  sospensione feriale.

Per i **calcoli** rimanda sempre a `civilista-scadenze`: qui si dice *quale* termine rileva, lì si
calcola la data. Molti termini civili corrono **a ritroso** dall'udienza: in quel caso, se la
scadenza cade di sabato o in giorno festivo, il termine si **anticipa**, non si proroga.

---

### 4. CONDIZIONE DI PROCEDIBILITÀ

Primo controllo, non ultimo. Agire senza aver esperito la condizione significa vedersi assegnare
un termine e perdere mesi — o peggio.

- **Mediazione obbligatoria** (art. 5 D.Lgs. 28/2010): verificare se la materia rientra
  (tra le altre: condominio, diritti reali, divisione, successioni ereditarie, patti di famiglia,
  locazione, comodato, affitto d'azienda, risarcimento da responsabilità medica e sanitaria,
  diffamazione a mezzo stampa, contratti assicurativi, bancari e finanziari).
- **Negoziazione assistita** (art. 3 D.L. 132/2014): risarcimento da circolazione di veicoli e
  natanti, e domande di pagamento a qualsiasi titolo di somme **fino a € 50.000**, fuori dai casi
  di mediazione obbligatoria.
- **Effetti da valutare in strategia**, non solo in adempimento: i **tempi** del procedimento vanno
  conteggiati nel piano (e l'improcedibilità va eccepita nei termini); la domanda di mediazione
  **interrompe la prescrizione** e impedisce la decadenza; il **valore negoziale** è reale — è
  l'occasione per misurare la controparte e mettere agli atti una proposta ragionevole, che peserà
  sulle spese; la **mancata partecipazione senza giustificato motivo** ha conseguenze valutabili
  dal giudice.
- **Il decreto ingiuntivo**: la condizione di procedibilità va soddisfatta nella fase di
  opposizione. Verificare chi ha l'onere di attivarla e in quale termine — è un punto su cui le
  cause si perdono in rito.

Se la materia è dubbia, dirlo e indicare la verifica da fare. Se la condizione **non** è richiesta,
scriverlo comunque: è un controllo che deve risultare fatto.

---

### 5. PRESCRIZIONE E DECADENZA

Tre elementi, sempre tutti e tre:

1. **Termine applicabile**: ordinario decennale (art. 2946 c.c.); quinquennale per il fatto
   illecito (art. 2947 c.c.) e per le prestazioni periodiche (art. 2948 c.c.); biennale per il danno
   da circolazione; presunzioni di pagamento (artt. 2954 ss.); termini speciali della materia.
2. **Decorrenza**: dal giorno in cui il diritto **poteva essere fatto valere** (art. 2935 c.c.).
   Nel danno lungolatente conta il momento in cui il danno si è manifestato ed è stato
   ragionevolmente conoscibile. Precisare la data assunta e su cosa si fonda.
3. **Atti interruttivi già compiuti** (art. 2943 c.c.): diffide, PEC, raccomandate, domanda
   giudiziale, riconoscimento del debito (art. 2944 c.c.), pagamenti parziali. Per ciascuno servono
   **data e prova della ricezione**: una diffida senza prova di consegna non interrompe nulla di
   dimostrabile.

**Decadenze** (diverse dalla prescrizione, non interrompibili): denuncia dei vizi nella compravendita
e nell'appalto, impugnazione delle delibere condominiali e assembleari, termini di contestazione
contrattuali. Vanno verificate a parte: maturano prima e in silenzio.

**Simmetria dei lati.** Dal lato attivo: verificare che il diritto sia ancora azionabile e, se il
termine è prossimo, **interrompere subito** prima di ogni altra valutazione. Dal lato passivo: la
prescrizione è un'eccezione in senso stretto — va **sollevata nell'atto giusto** (§ 3), altrimenti
è persa anche se maturata.

---

### 6. PUNTI DEBOLI DELLA NOSTRA POSIZIONE

Sezione **obbligatoria**, esplicita, senza indulgenza. L'avvocato deve conoscere le crepe prima
della controparte e prima del giudice.

Ragiona almeno su:

- **Prove mancanti o fragili**: righe della tabella § 2 senza copertura documentale; testimoni
  legati alla parte; documenti non opponibili per data certa; e-mail senza valore di sottoscrizione.
- **Fatti sfavorevoli documentati**: pagamenti parziali che valgono riconoscimento, e-mail proprie
  che ammettono ritardi, comportamenti concludenti.
- **Rischio di riqualificazione** della vicenda in senso a noi sfavorevole.
- **Eccezioni prevedibili della controparte**, in ordine di pericolosità, e cosa abbiamo per ciascuna;
  **domande riconvenzionali probabili** e il loro valore.
- **Punti già preclusi** per attività già svolta o non svolta.
- **Elemento umano**: credibilità del cliente, coerenza della sua versione con i documenti.

Se la posizione è debole, **scriverlo in chiaro** e riportarlo nella valutazione economica (§ 7).
Un'analisi che non trova punti deboli non è un'analisi: è una brochure.

---

### 7. VALUTAZIONE ECONOMICA

Un civilista decide anche — spesso soprattutto — in base a quanto costa avere ragione. Sezione da
produrre in forma di prospetto.

| Voce | Contenuto | Nota |
|---|---|---|
| **Valore della causa** | Determinato o indeterminabile; criterio usato | Determina scaglione, competenza e spese |
| **Contributo unificato e anticipazioni** | CU, marca, notifiche, eventuale CTU | Verificare gli importi vigenti alla data |
| **Compensi di fase** (DM 55/2014 e s.m.i.) | Studio, introduttiva, istruttoria, decisoria per lo scaglione | **Parametro di riferimento, da riverificare**: gli importi sono soggetti ad aggiornamento |
| **Rischio soccombenza** | Spese di controparte se si perde; ipotesi di compensazione | Nel civile la soccombenza si paga: va quantificata, non evocata |
| **Soccombenza parziale / reciproca** | Scenario intermedio più probabile | Spesso è l'esito reale |
| **Tempi realistici** | Primo grado, eventuale appello, esecuzione | Includere ADR e tempi di CTU |
| **Recuperabilità** | La controparte è solvibile? Ci sono garanzie, beni, capienza? | Una sentenza contro un incapiente vale poco: verificarlo **prima** di agire |

Poi il confronto esplicito tra scenari:

- **Scenario giudiziale**: esito atteso, tempi, costo pieno, costo in caso di soccombenza.
- **Scenario transattivo**: cifra realisticamente ottenibile, tempi, certezza dell'incasso,
  risparmio di spese e di rischio.
- **Scenario di rinuncia** (lato attivo) o **di adempimento immediato** (lato passivo): quando è la
  scelta razionale, va detto. Anche questo è consiglio professionale.

Regole: ogni valore numerico porta **fonte e data di riferimento** e va segnalato come da
riverificare. Non presentare stime come certezze. La proposta transattiva formulata e rifiutata
pesa sulle spese: se ha senso, farla **e metterla agli atti**.

---

### 8. PROSSIME MOSSE

Elenco ordinato di azioni concrete, ciascuna con **chi la fa**, **entro quando** e **perché**.
Prima le mosse a termine, poi quelle istruttorie, poi quelle negoziali.

Esempi di formulazione corretta:

1. Interrompere la prescrizione con PEC di costituzione in mora — **prima di ogni altra attività**,
   se il termine è prossimo (§ 5).
2. Recuperare i documenti mancanti indicati nella tabella § 2 (elencarli uno per uno).
3. Avviare la mediazione obbligatoria in materia di [ ] (§ 4).
4. Costituirsi con comparsa contenente riconvenzionale ed eccezione di prescrizione — **a pena di
   decadenza** entro il termine di costituzione (§ 3).
5. Formulare proposta transattiva a € [ ], da mettere agli atti.
6. Ricercare in KB gli orientamenti su [ ] con `civilista-giurisprudenza`, prima di redigere l'atto.

**I calcoli dei termini si fanno con `civilista-scadenze`**, che ragiona su decorrenza, direzione
(in avanti / a ritroso), festivi e sospensione feriale, e aggiorna lo scadenziario del fascicolo.
Qui si indicano i termini rilevanti, non le date calcolate a mano.

---

## Integrazione con il fascicolo

Al termine dell'analisi:

- se il fascicolo esiste in `FASCICOLI/<caso>/`, aggiorna la scheda con la qualificazione scelta, la
  tabella dell'onere della prova e le scadenze emerse, e crea/aggiorna `SCADENZIARIO.md`; se non
  esiste, crealo con i wikilink già collegati — indici e collegamenti li mantieni tu, non l'avvocato;
- indicizza in `FASCICOLI/<caso>/_INDICE/` i documenti di causa con `civilista-archivio`: da lì in
  poi ogni affermazione sul fascicolo sarà ancorabile a un documento e a una pagina.

---

## Tono e stile

- Scrivi come un civilista che parla a un collega: tecnico, diretto, senza cautele di facciata.
- Usa l'imperativo: "verifica", "interrompi", "costituisciti", non "potrebbe essere opportuno".
- Distingui sempre **fatto allegato** da **fatto provato**: è la distinzione che decide le cause.
- Le sezioni 6 e 7 devono essere scomode: servono a quello.
- Ogni analisi è una **bozza di lavoro**: decisione e responsabilità restano del difensore.
