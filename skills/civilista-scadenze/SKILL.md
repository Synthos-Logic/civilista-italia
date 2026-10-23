---
name: civilista-scadenze
description: >
  Calcolo dei termini processuali civili con ragionamento esplicito, termini a ritroso e
  sospensione feriale, e aggiornamento dello scadenziario del fascicolo. ATTIVARE SEMPRE quando
  l'avvocato chiede un termine o dice: 'quando scade', 'entro quando devo depositare', 'calcola i
  termini', 'che termini ho', 'termine a ritroso', 'quando devo costituirmi', 'entro quando la
  comparsa di risposta', 'quando scadono le memorie', 'memorie 171-ter', 'termine per l'appello',
  'quanto tempo ho per il ricorso in Cassazione', 'termine breve o termine lungo', 'reclamo
  cautelare', 'quando devo iniziare il merito dopo la cautelare', 'sospensione feriale', 'ad
  agosto si sospende?', 'quando si prescrive', 'è ancora in termini?', 'abbiamo perso il
  termine?', 'quando scade il precetto', 'termine per l'opposizione a decreto ingiuntivo',
  'opposizione agli atti esecutivi'. Attivare anche per riverificare un termine già calcolato in
  studio.
---

# civilista-scadenze — Calcolo dei termini nel processo civile

Un errore su un termine civile non si recupera: produce decadenza, improcedibilità o
inammissibilità. Ogni calcolo va svolto per iscritto, passo per passo, mostrando il
ragionamento. Non si risponde mai "circa", "più o meno", "intorno al".

Se manca un dato indispensabile (data di notifica, materia, tipo di rito, data udienza),
chiedilo prima di calcolare. Non stimare mai una data-evento.

---

## MODULO 0 — Le tre domande obbligatorie (vincolante)

Nessun calcolo può iniziare prima di aver risposto, per iscritto, a queste tre domande.

### 0.1 — Il termine corre IN AVANTI o A RITROSO?

| Direzione | Come funziona | Se la scadenza cade di sabato o festivo |
|---|---|---|
| **In avanti** (dall'evento verso il futuro) | Si conta dal giorno successivo all'evento | **PROROGA** al primo giorno successivo non festivo |
| **A ritroso** (dall'udienza verso il passato) | Si conta all'indietro dal giorno dell'udienza, escluso | **ANTICIPAZIONE** al primo giorno precedente non festivo |

La regola a ritroso è invertita perché il termine è posto a garanzia dell'intervallo
minimo di difesa della controparte: prorogare in avanti eroderebbe quell'intervallo.
È l'errore più frequente in assoluto. Orientamento consolidato di legittimità; la massima
va verificata con `civilista-giurisprudenza` prima di usarla in un atto.

**Termini a ritroso tipici:** costituzione del convenuto (70 gg), memorie ex art. 171-ter
(40/20/10 gg), costituzione dell'appellato e appello incidentale (20 gg ex art. 343),
note di precisazione delle conclusioni (60 gg), comparse conclusionali (30 gg),
repliche (15 gg), termini a comparire (120/150/90 gg).

### 0.2 — La materia è ESCLUSA dalla sospensione feriale?

Sospensione dal **1 al 31 agosto** (L. 742/1969, ridotta da 45 a 31 giorni dal D.L. 132/2014).

**Cause escluse — i termini corrono anche ad agosto:** procedimenti cautelari; alimenti;
convalida di sfratto; opposizioni all'esecuzione; controversie di lavoro; previdenza e
assistenza obbligatoria; amministrazione di sostegno, interdizione e inabilitazione;
ordini di protezione contro gli abusi familiari; procedure concorsuali; ogni causa in cui
la ritardata trattazione produce grave pregiudizio alle parti (previa dichiarazione
d'urgenza del giudice).

Se la materia è esclusa, scriverlo espressamente nel calcolo: "sospensione feriale NON
applicata perché [materia]". Se è dubbio, calcolare **entrambe le ipotesi** e assumere
come operativa la più breve.

### 0.3 — Qual è la data-evento e come si prova?

| Evento di decorrenza | Prova documentale da avere in fascicolo |
|---|---|
| Notificazione della sentenza | Relata / ricevuta PEC di consegna (RdAC) |
| Pubblicazione della sentenza | Attestazione di deposito, numero e data di pubblicazione |
| Comunicazione di cancelleria | Biglietto di cancelleria via PEC, data di consegna |
| Notificazione di atto di parte | Relata o ricevuta di accettazione + consegna |
| Pronuncia in udienza | Verbale d'udienza |

Se la prova non è in fascicolo, il termine è **provvisorio**: segnalarlo e chiedere il documento.

---

## Regole di computo (art. 155 c.p.c.)

1. Si esclude il giorno iniziale (*dies a quo non computatur*); si computa quello finale.
2. I giorni festivi intermedi si contano; incidono solo sul giorno di scadenza.
3. Se il termine scade in giorno festivo, la scadenza è prorogata di diritto al primo
   giorno seguente non festivo.
4. La proroga vale anche per il **sabato**, per gli atti processuali compiuti fuori
   dell'udienza. Le **udienze del sabato restano valide**.
5. Termini a mesi o ad anni: si computano *ex nominatione dierum* (dal giorno al giorno
   corrispondente), senza contare il numero dei giorni.
6. Sospensione feriale: i 31 giorni di agosto non si contano; il termine riprende il
   1 settembre per i giorni residui. Per i termini a mesi/anni, si aggiungono 31 giorni
   alla scadenza naturale.
7. Termini a ritroso che attraversano agosto: i 31 giorni si aggiungono **all'indietro**,
   anticipando ulteriormente la scadenza.

---

## MODULO 1 — Fase introduttiva (rito ordinario)

| Adempimento | Termine | Norma | Direzione |
|---|---|---|---|
| Termine a comparire | **120 giorni liberi** dalla notificazione | art. 163-bis | avanti (dilatorio) |
| Termine a comparire, notifica all'estero | **150 giorni liberi** | art. 163-bis | avanti (dilatorio) |
| Costituzione del convenuto | almeno **70 giorni** prima dell'udienza | art. 166 | **ritroso** |
| Verifiche preliminari del giudice | entro **15 giorni** dalla scadenza del termine ex art. 166 | art. 171-bis | avanti |
| Differimento dell'udienza da parte del giudice | fino a **45 giorni** | art. 171-bis co. 3 | avanti |

**Decadenze della comparsa di risposta (art. 167):** solo con la costituzione tempestiva
si propongono domande riconvenzionali, eccezioni processuali e di merito non rilevabili
d'ufficio, e si chiede l'autorizzazione alla chiamata del terzo. Costituirsi anche un solo
giorno oltre il settantesimo significa perdere queste facoltà, non solo "costituirsi tardi".

I 120 giorni sono un termine dilatorio minimo; "liberi" significa che non si computano né
il giorno della notificazione né quello dell'udienza.

---

## MODULO 2 — Memorie integrative (art. 171-ter)

Tre termini, tutti **a ritroso** dall'udienza ex art. 183 e tutti **a pena di decadenza**:

| Memoria | Termine | Contenuto ammesso |
|---|---|---|
| Prima | **-40 giorni** | domande ed eccezioni conseguenti alla riconvenzionale o alle eccezioni del convenuto o del terzo; precisazione e modificazione di domande, eccezioni e conclusioni; istanza di chiamata del terzo se l'esigenza è sorta dalle difese del convenuto |
| Seconda | **-20 giorni** | replica alle domande ed eccezioni nuove o modificate; eccezioni conseguenti; **indicazione dei mezzi di prova e produzioni documentali** |
| Terza | **-10 giorni** | replica alle eccezioni nuove; indicazione della **prova contraria** |

**Decorrenza dopo il correttivo (D.Lgs. 164/2024):** i termini iniziano a decorrere
quando è pronunciato il decreto ex art. 171-bis co. 3, ma **si computano a ritroso
rispetto all'udienza** fissata in citazione o a quella diversa fissata dal giudice.
Regola operativa: appena arriva il decreto, ricalcolare le tre date sull'udienza
confermata o differita e riscrivere lo scadenziario.

**La seconda memoria è la più pericolosa del processo civile**: chi non indica lì i mezzi
di prova e non produce i documenti, decade. Segnalarla sempre come scadenza critica.

---

## MODULO 3 — Fase decisoria

| Atto | Termine (a ritroso dall'udienza di rimessione in decisione) | Norma |
|---|---|---|
| Note di precisazione delle conclusioni | **-60 giorni** | art. 189 |
| Comparse conclusionali | **-30 giorni** | art. 189 |
| Memorie di replica | **-15 giorni** | art. 189 |

**Deposito della sentenza:** 60 giorni (collegiale) / 30 giorni (monocratico) dalla
scadenza del termine per le repliche.

**Modelli alternativi:** decisione a seguito di trattazione mista o orale
(artt. 275-bis e 281-sexies): il giudice fissa termini propri, spesso più brevi.
Quando il giudice adotta uno di questi modelli, i termini ordinari non si applicano:
leggere il provvedimento e calcolare su quello.

**Note scritte in luogo dell'udienza (art. 127-ter):** il giudice assegna un termine
perentorio **non inferiore a 15 giorni**; le parti costituite possono opporsi entro
**5 giorni** dalla comunicazione.

---

## MODULO 4 — Impugnazioni

### Termine breve (art. 325) — decorre dalla NOTIFICAZIONE della sentenza

| Impugnazione | Termine |
|---|---|
| Appello | **30 giorni** |
| Revocazione ordinaria (art. 395 nn. 4 e 5) | **30 giorni** |
| Opposizione di terzo revocatoria | **30 giorni** |
| Ricorso per Cassazione | **60 giorni** |

### Termine lungo (art. 327) — decorre dalla PUBBLICAZIONE della sentenza

**6 mesi**, salvo il caso di contumacia incolpevole. Soggetto a sospensione feriale
(+31 giorni se il semestre attraversa agosto).

I due termini non si sommano e non si scelgono: se la sentenza è stata notificata vale il
breve. Verificare sempre a chi e in quale forma è stata notificata: il termine breve
decorre per chi ha ricevuto la notificazione.

### Giudizio di appello

| Adempimento | Termine | Norma |
|---|---|---|
| Termine a comparire | **90 giorni liberi** (150 se notifica all'estero) | art. 342 ss. |
| Costituzione dell'appellante | 10 giorni dalla notificazione dell'atto di appello | art. 347 |
| Costituzione dell'appellato | almeno **70 giorni** prima dell'udienza | art. 343 |
| Appello incidentale | almeno **20 giorni** prima dell'udienza | art. 343 |

### Giudizio di cassazione

| Adempimento | Termine | Norma |
|---|---|---|
| Deposito del ricorso | **20 giorni** dall'ultima notificazione | art. 369 |
| Controricorso | **40 giorni** dalla notificazione del ricorso | art. 370 |
| Istanza di decisione dopo proposta di definizione accelerata | **40 giorni** | art. 380-bis |
| Revocazione per contrarietà a decisione della Corte EDU | **60 giorni** | art. 391-quater |

Il mancato deposito nei 20 giorni ex art. 369 produce improcedibilità: è un termine
che si perde per disorganizzazione, non per errore di calcolo. Metterlo in scadenziario
il giorno stesso della notificazione del ricorso.

---

## MODULO 5 — Cautelare e reclamo

| Adempimento | Termine | Norma |
|---|---|---|
| Reclamo contro il provvedimento cautelare | **15 giorni** dalla pronuncia in udienza, ovvero dalla comunicazione o notificazione | art. 669-terdecies |
| Inizio del giudizio di merito dopo la cautelare | **60 giorni** (perentorio) dalla pronuncia in udienza o dalla comunicazione | art. 669-octies |

**Attenzione all'art. 669-octies:** l'onere di iniziare il merito nei 60 giorni **non**
opera per i provvedimenti d'urgenza ex art. 700 e per gli altri provvedimenti anticipatori
degli effetti della sentenza di merito (nonché per nuova opera, danno temuto e sospensione
di delibere assembleari): lì ciascuna parte *può* iniziare il merito, ma non deve. Prima
di calcolare, qualificare il provvedimento come conservativo o anticipatorio: se è
conservativo e i 60 giorni scadono a vuoto, la misura perde efficacia (art. 669-novies).

**Sospensione feriale: NON si applica** ai procedimenti cautelari. Un reclamo notificato
il 5 agosto scade il 20 agosto, non a settembre.

---

## MODULO 6 — Esecuzione

| Adempimento | Termine | Norma |
|---|---|---|
| Termine dilatorio dopo la notifica del precetto | **10 giorni** prima di iniziare l'esecuzione | art. 482 |
| Efficacia del precetto | perde efficacia se l'esecuzione non inizia entro **90 giorni** dalla notificazione | art. 481 |
| Istanza di vendita o assegnazione | **45 giorni** dal pignoramento, a pena di inefficacia | art. 497 |
| Opposizione a decreto ingiuntivo | **40 giorni** dalla notificazione | artt. 641 e 645 |
| Opposizione agli atti esecutivi | **20 giorni** dall'atto o dalla sua conoscenza legale | art. 617 |
| Opposizione all'esecuzione | prima dell'inizio: davanti al giudice competente; dopo: con ricorso al giudice dell'esecuzione | artt. 615-616 |

Le **opposizioni all'esecuzione** rientrano tra le materie escluse dalla sospensione
feriale: non contare agosto a favore del cliente. Il termine di iscrizione a ruolo del
pignoramento varia secondo il tipo (mobiliare, immobiliare, presso terzi): verificarlo
sulla norma applicabile prima di indicarlo.

---

## MODULO 7 — ADR e mediazione

- La domanda di mediazione, dal momento della comunicazione alle altre parti, produce
  sulla **prescrizione** gli effetti della domanda giudiziale e **impedisce la decadenza
  per una sola volta** (art. 8 D.Lgs. 28/2010). "Una sola volta" è letterale: la seconda
  domanda sullo stesso diritto non impedisce più nulla.
- **Primo incontro:** non prima di **20** e non oltre **40 giorni** dal deposito della domanda.
- **Durata del procedimento:** **6 mesi**, prorogabili prima della scadenza con accordo
  scritto delle parti allegato al verbale; nella mediazione demandata dal giudice la
  proroga è una sola, di ulteriori 3 mesi (art. 6 D.Lgs. 28/2010, testo coordinato al
  correttivo D.Lgs. 216/2024). La durata incide sulla procedibilità della domanda giudiziale.
- I termini della mediazione non seguono la sospensione feriale: agosto è un mese pieno.
- Quando la mediazione è condizione di procedibilità, presidiare anche il **termine
  giudiziale** assegnato per avviarla.

---

## MODULO 8 — Prescrizione e decadenza

| Fattispecie | Termine | Norma |
|---|---|---|
| Prescrizione ordinaria | **10 anni** | art. 2946 |
| Canoni, interessi, prestazioni periodiche | **5 anni** | art. 2948 |
| Risarcimento da fatto illecito | **5 anni** | art. 2947 co. 1 |
| Danno da circolazione di veicoli (RCA) | **2 anni** | art. 2947 co. 2 |
| Fatto illecito costituente reato con prescrizione più lunga | termine del reato | art. 2947 co. 3 |

**Interruzione (artt. 2943-2945):** la notificazione dell'atto introduttivo del giudizio e
ogni atto di costituzione in mora interrompono la prescrizione; dall'interruzione decorre
un **nuovo periodo integrale**. Se l'interruzione avviene con domanda giudiziale l'effetto
è permanente: la prescrizione non corre fino al passaggio in giudicato.

**Decadenza:** non soggetta a interruzione né, salvo diversa disposizione, a sospensione
(art. 2964); si impedisce solo compiendo l'atto previsto (art. 2966).

Servono sempre due dati provati: **data di decorrenza** (quando il diritto poteva essere
fatto valere) e **elenco degli atti interruttivi con le relative prove**. In mancanza, il
calcolo è un'ipotesi e va dichiarato tale.

---

## Formato obbligatorio di ogni calcolo

Ogni termine va esposto in questa sequenza, senza saltare passaggi:

```
TIPO DI TERMINE:      [descrizione]
NORMA:                [articolo]
EVENTO:               [fatto storico + data + prova in fascicolo]
DIES A QUO:           [data — non computato]
DIREZIONE:            [in avanti / a ritroso]
SOSPENSIONE FERIALE:  [SI / NO — perché]
CONTEGGIO:            [passaggi aritmetici, giorno per giorno o mese per mese]
FESTIVI / SABATO:     [scadenza naturale + giorno della settimana + correzione applicata]
DIES AD QUEM:         [data]
```

**>> SCADENZA: [giorno della settimana] [data]. Deposito operativo entro [data - 1]. <<**

---

## Esempi svolti (2026)

### Esempio 1 — Appello, termine breve che attraversa agosto e scade di sabato

Sentenza di primo grado notificata a mezzo PEC il **lunedì 20 luglio 2026**
(RdAC in fascicolo). Materia: responsabilità contrattuale, non esclusa.

- Evento: notificazione della sentenza, 20 luglio 2026.
- Dies a quo: 20 luglio, non computato. Il termine decorre dal 21 luglio.
- Direzione: in avanti. Termine: 30 giorni (art. 325).
- Sospensione feriale: SI, materia ordinaria. Dal 21 al 31 luglio si consumano
  **11 giorni**. Dal 1 al 31 agosto il termine è sospeso.
- Ripresa: 1 settembre 2026, con **19 giorni residui** (30 - 11).
  1 settembre + 18 giorni = **19 settembre 2026**.
- Festivi/sabato: il 19 settembre 2026 è un **sabato** → proroga di diritto al primo
  giorno seguente non festivo, **lunedì 21 settembre 2026**.

**>> SCADENZA: lunedì 21 settembre 2026. Notifica dell'appello entro venerdì 18 settembre. <<**

### Esempio 2 — Memorie ex art. 171-ter, termine a ritroso che cade di sabato

Udienza ex art. 183 confermata con decreto ex art. 171-bis per **venerdì 16 ottobre 2026**.

- Direzione: **a ritroso** dall'udienza, giorno dell'udienza non computato.
- Sospensione feriale: irrilevante, nessuno dei tre intervalli attraversa agosto.

| Memoria | Scadenza naturale | Giorno | Correzione a ritroso | Scadenza operativa |
|---|---|---|---|---|
| Prima (-40) | 6 settembre 2026 | domenica | anticipa; il 5 è sabato | **venerdì 4 settembre 2026** |
| Seconda (-20) | 26 settembre 2026 | **sabato** | anticipa | **venerdì 25 settembre 2026** |
| Terza (-10) | 6 ottobre 2026 | martedì | nessuna | **martedì 6 ottobre 2026** |

Chi avesse applicato la proroga in avanti avrebbe depositato la seconda memoria lunedì
28 settembre, **decadendo dai mezzi di prova e dalle produzioni documentali**.

**>> SCADENZA CRITICA: seconda memoria (mezzi di prova) venerdì 25 settembre 2026.
Deposito entro giovedì 24 settembre. <<**

### Esempio 3 — Termine lungo a mesi con sospensione feriale

Sentenza pubblicata il **10 marzo 2026**, mai notificata. Materia ordinaria.

- Evento: pubblicazione (attestazione di deposito in fascicolo), 10 marzo 2026.
- Direzione: in avanti. Termine: 6 mesi (art. 327).
- Computo a mesi: dal 10 marzo al **10 settembre 2026** (giovedì).
- Sospensione feriale: SI → si aggiungono **31 giorni**: 10 settembre + 31 =
  **11 ottobre 2026**.
- Festivi: l'11 ottobre 2026 è **domenica** → proroga a **lunedì 12 ottobre 2026**.

**>> SCADENZA: lunedì 12 ottobre 2026. Impugnazione da notificare entro venerdì 9 ottobre. <<**

---

## Errori da non fare mai

1. **Applicare la proroga in avanti a un termine a ritroso.** Il sabato e il festivo
   anticipano, non prorogano. È l'errore che costa più decadenze: memorie 171-ter,
   costituzione del convenuto, appello incidentale.
2. **Sospendere ad agosto un termine in materia esclusa.** Cautelari, lavoro, sfratti,
   alimenti, opposizioni esecutive, concorsuali, protezione dagli abusi familiari:
   agosto è un mese pieno. Un reclamo cautelare "rinviato a settembre" è un reclamo perso.
3. **Confondere termine breve e termine lungo.** Se la sentenza è stata notificata, il
   semestre non esiste più. Verificare sempre l'esistenza e la data della notificazione
   prima di ragionare sui 6 mesi.
4. **Fidarsi di un calcolo già fatto in redazione.** Ogni termine riportato da altri
   (collega, praticante, gestionale, calcolatore online, questa stessa skill in una
   sessione precedente) va **rifatto da zero** prima del deposito. Il ricalcolo indipendente
   è obbligatorio, non facoltativo.
5. **Calcolare su una data-evento non provata.** "Credo sia stata notificata a fine luglio"
   non è una data. Senza relata, ricevuta PEC o attestazione, il termine è provvisorio.
6. **Dimenticare di ricalcolare dopo il decreto ex art. 171-bis.** Se il giudice differisce
   l'udienza, tutte le scadenze a ritroso cambiano.
7. **Trattare la decadenza come la prescrizione.** La decadenza non si interrompe con una
   raccomandata: si impedisce solo compiendo l'atto.
8. **Contare il dies a quo.** Il giorno dell'evento non si conta mai; il giorno finale sì.

---

## Regola di chiusura

Ogni termine calcolato va **scritto nello SCADENZIARIO del fascicolo**, con: fascicolo,
tipo di termine, norma, evento e data di decorrenza, dies ad quem e stato della prova
documentale. Un termine calcolato in chat e non trascritto è un termine non calcolato.

Ogni scadenza va comunicata con almeno **un giorno lavorativo pieno di margine operativo**
rispetto al dies ad quem, indicando la data di deposito consigliata: il margine copre i
disservizi del deposito telematico, che non sospendono i termini.

Aggiornare [[SCADENZIARIO]] al termine di ogni calcolo.
