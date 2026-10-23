---
name: civilista-lavoro
description: >
  Diritto del lavoro e processo del lavoro italiano, dal lato del lavoratore e dal lato del
  datore. ATTIVARE SEMPRE su una vicenda lavoristica o quando l'avvocato dice: 'il mio cliente è
  stato licenziato', 'impugnare il licenziamento', licenziamento per giusta causa, giustificato
  motivo oggettivo, disciplinare, collettivo, orale, discriminatorio o ritorsivo; 'contestazione
  disciplinare', 'siamo ancora in tempo a impugnare', 'quando scadono i 60 giorni', 'i 180 giorni
  da quando decorrono', 'reintegra o indennità', 'tutele crescenti', 'jobs act', 'articolo 18',
  'differenze retributive', 'mansioni superiori', 'demansionamento', 'straordinari non pagati',
  'TFR', 'ferie non godute', 'rito del lavoro', 'ricorso ex art. 414', 'memoria ex art. 416',
  'conciliazione in sede protetta', 'contratto a termine illegittimo', 'somministrazione
  irregolare', 'infortunio sul lavoro', 'contenzioso INPS o INAIL'. Usare prima di scrivere
  qualsiasi atto in materia di lavoro.
---

# civilista-lavoro — Rapporto di lavoro, licenziamenti e processo del lavoro

Nel lavoro si perde per decadenza molto più spesso che nel merito. Due cose vanno controllate **prima di ogni altra**,
anche quando l'avvocato chiede altro: **la data di assunzione**, che decide il regime sanzionatorio del licenziamento,
e **il doppio termine di impugnazione**, che decide se la causa esiste ancora.

Rinvii vincolanti: i **calcoli** dei termini si fanno con `civilista-scadenze` (qui si dice *quale* termine rileva e da
*quale evento* decorre); le **massime** si cercano con `civilista-giurisprudenza` — in questa skill non compare alcun
numero di sentenza, e ciò che non è in KB si dichiara "non presente in KB". Il lavoro è fuori dal perimetro delle
schede di materia del kit: dillo all'avvocato.

Dati normativi **verificati online il 6 agosto 2026**, con fonte indicata; ciò che non è stato confermato è marcato **da verificare**.

## MODULO 0 — Inquadramento del rapporto

Sei risposte, chieste **tutte insieme**. Se un dato manca, procedi indicando l'assunzione fatta.

**0.1 Natura del rapporto.** Subordinato (art. 2094 c.c.); parasubordinato, comprese le collaborazioni
etero-organizzate cui si applica la disciplina del lavoro subordinato (art. 409 n. 3 c.p.c.; art. 2 D.Lgs. 81/2015);
autonomo (art. 2222 c.c.). Il rito del lavoro copre anche le controversie sulla qualificazione: l'art. 441-bis co. 1
c.p.c. lo dice espressamente per i licenziamenti (*ilcaso.it, verificato 6 agosto 2026*). Attenzione: l'azione diretta
ad accertare la subordinazione è soggetta alle decadenze estese dall'art. 32 L. 183/2010 (*medicoeleggi.com,
verificato 6 agosto 2026*) — non è libera nel tempo.

**0.2 Contratto e CCNL.** CCNL applicato e CCNL *applicabile* (non sempre coincidono), livello, mansioni effettive,
retribuzione lorda e sue voci, orario, unità produttiva. Senza il testo del contratto collettivo non si quantifica
nulla.

**0.3 Anzianità.** Data di assunzione, contratti a termine precedenti, passaggi societari, trasferimento d'azienda
(art. 2112 c.c.), cambi di appalto. Nelle tutele crescenti le frazioni di mese pari o superiori a 15 giorni valgono
come mese intero (art. 8 D.Lgs. 23/2015) e negli appalti si computa il periodo di impiego nell'attività appaltata
presso l'impresa subentrante (art. 7) (*lavoro.gov.it, verificato 6 agosto 2026*).

**0.4 Dimensioni del datore.** Soglie dell'art. 18 St. lav.: **più di 15** dipendenti nell'unità produttiva o nello
stesso comune, **più di 5** per l'imprenditore agricolo, **più di 60** complessivi sul territorio nazionale
(*wikilabour.it, verificato 6 agosto 2026*). Regola decisiva: **l'onere di provare l'inesistenza del requisito
dimensionale grava sul datore**, come fatto impeditivo della tutela reale (orientamento consolidato — *lexced.com,
verificato 6 agosto 2026*; massima da recuperare con `civilista-giurisprudenza`). Le regole di computo di part-time,
apprendisti e somministrati sono **da verificare** sul testo vigente.

**0.5 Data di assunzione — la domanda che decide tutto.** Il D.Lgs. 4 marzo 2015 n. 23 è in vigore dal **7 marzo
2015** (G.U. 6 marzo 2015 — *federmanager.it, verificato 6 agosto 2026*) e si applica ai lavoratori assunti a tempo
indeterminato **da quella data**. Tre raccordi (art. 1 D.Lgs. 23/2015 — *lavoro.gov.it, verificato 6 agosto 2026*):
assunti **dal 7 marzo 2015** → tutele crescenti; **conversione** di un contratto a termine o di apprendistato avvenuta
dopo quella data → tutele crescenti, anche se il rapporto originario è anteriore; **superamento della soglia**
dimensionale per effetto di assunzioni a tempo indeterminato successive → tutele crescenti per **tutti**, compresi gli
assunti prima. Sbagliare qui significa chiedere la reintegrazione dove spetta un'indennità, o viceversa.

**0.6 Che cosa è già successo, e da che lato stiamo.** Contestazione disciplinare e difese (art. 7 St. lav.), lettera
di licenziamento e data di **ricezione** (non di spedizione), comunicazione dei motivi se successiva, dimissioni,
verbali sindacali, diffide, richieste di conciliazione, procedure collettive. E soprattutto: siamo **lato lavoratore**, dove si
presidiano i termini di decadenza e la prova dei crediti, o **lato datore**, dove si presidiano la procedura, la
proporzionalità della sanzione e le eccezioni di decadenza e prescrizione?

## MODULO 1 — Licenziamenti

### 1.1 Le due fasi del termine di impugnazione

L'art. 6 L. 604/1966, nel testo sostituito dall'art. 32 L. 183/2010 e poi modificato dalla L. 92/2012, costruisce una
**decadenza a due fasi**, entrambe a pena di decadenza. La seconda non sana la prima e la prima non copre la seconda.

| Fase | Termine | Decorrenza | Atto idoneo |
|---|---|---|---|
| Prima | **60 giorni** | **ricezione** della comunicazione scritta del licenziamento, o dei motivi se successivi | qualsiasi **atto scritto**, anche stragiudiziale, anche tramite il sindacato |
| Seconda | **180 giorni** | dall'**impugnazione stragiudiziale** (per la legittimità, dalla **spedizione**) | deposito del ricorso, oppure comunicazione della richiesta di conciliazione o arbitrato |
| Coda | **60 giorni** | rifiuto della conciliazione o mancato accordo | deposito del ricorso |

(*brocardi.it — art. 6 L. 604/1966; lexced.com; studiolegalegulino.it, verificati 6 agosto 2026.* Il secondo termine
era di **270 giorni** nel testo del 2010, ridotto a **180** dalla riforma Fornero; la decorrenza esatta della
riduzione rispetto alla data del licenziamento è **da verificare** per i casi di confine.) La decorrenza **dalla
spedizione** risulta affermata in legittimità ma discussa nel merito: verificala con `civilista-giurisprudenza` e
comunque **calcola sull'ipotesi più sfavorevole**.

**Esempio 1 — calcolo corretto.** Licenziamento ricevuto il 10 aprile 2026; impugnazione stragiudiziale spedita via
PEC il 5 giugno 2026 (56° giorno, tempestiva). I 180 giorni decorrono dal 5 giugno, non dal 10 aprile: il ricorso va
depositato entro i primi giorni di dicembre. Data esatta con `civilista-scadenze`, **senza sospensione feriale** (§
3.4).

**Esempio 2 — l'errore che chiude il fascicolo.** Stesso caso: lo studio conta 180 giorni dal 10 aprile e il 20
novembre archivia la causa come decaduta. Era ancora in termini: il dies a quo è **l'impugnazione**, non il recesso.

**Esempio 3 — la conciliazione consuma il termine.** Impugnazione del 5 giugno 2026; richiesta di conciliazione
comunicata al datore il 20 novembre (entro i 180 giorni: decadenza impedita); rifiuto con PEC del 2 dicembre. Da lì
decorrono **60 giorni** per depositare il ricorso: chi crede di avere ancora i residui dei 180 decade.

Regole operative permanenti:

- Impugna **subito**, non al 59° giorno, con **prova della data**: PEC con ricevuta di accettazione e di consegna,
  raccomandata a/r, consegna a mani con firma. Conserva l'**accettazione**: prova la spedizione.
- Il termine di 60 giorni vale anche per i **dirigenti** (*dottrinalavoro.it, verificato 6 agosto 2026*).
- Risulta che il **ricorso cautelare** sia idoneo a impedire la decadenza della seconda fase, per un intervento della
  Corte costituzionale del 2020 (*ecnews.it, verificato 6 agosto 2026*); resta aperto il termine per introdurre il
  merito dopo il rigetto della cautelare, **da verificare**.
- Risulta un intervento della Corte costituzionale del 2025 sul primo termine in caso di **incapacità del lavoratore**
  di comprendere il significato dell'atto: in quell'ipotesi opera il termine complessivo di 240 giorni
  (*dottrinalavoro.it, verificato 6 agosto 2026*). Verificalo con `civilista-giurisprudenza`.
- **Licenziamento orale**: per la legittimità la decadenza dei 60 giorni **non si applica**, perché il recesso non
  scritto è nullo per difetto di forma, e opera la prescrizione ordinaria (*lavorosi.it, verificato 6 agosto 2026*).
  **Impugna comunque per iscritto entro 60 giorni**: la qualificazione come orale è contestabile e non va giocata come
  unica difesa.

### 1.2 I due regimi sanzionatori

**Assunti fino al 6 marzo 2015 — art. 18 St. lav.** (testo L. 92/2012; datori sopra soglia). Quattro tutele
(*wikilabour.it, verificato 6 agosto 2026*):

| Tutela | Quando | Contenuto |
|---|---|---|
| Reintegratoria piena | discriminatorio, nullo, orale, in periodo protetto | reintegrazione + risarcimento **non inferiore a 5 mensilità**; opzione per 15 mensilità |
| Reintegratoria attenuata | insussistenza del fatto contestato, o fatto punito dal CCNL con sanzione conservativa; manifesta insussistenza del fatto posto a base del GMO | reintegrazione + risarcimento **fino a 12 mensilità**, dedotto l'*aliunde perceptum* |
| Indennitaria forte | altri difetti di giusta causa o giustificato motivo | **12-24 mensilità** |
| Indennitaria debole | vizi formali e procedurali | **6-12 mensilità** |

**Assunti dal 7 marzo 2015 — D.Lgs. 23/2015**, impianto originario (*lavoro.gov.it, verificato 6 agosto 2026*): art. 2
discriminatorio, nullo od orale → reintegrazione; art. 3 co. 1 difetto di giusta causa o giustificato motivo →
estinzione e indennità (2 mensilità per anno, minimo 4, massimo 24; la procedura ex art. 7 L. 604/1966 non si
applica); art. 3 co. 2 insussistenza del fatto materiale → reintegrazione + indennità fino a 12 mensilità; art. 4 vizi
formali → indennità (1 mensilità per anno, 2-12); art. 9 piccole imprese → importi dimezzati; art. 10 licenziamento
collettivo.

**AVVERTENZA — l'impianto non è più quello del testo.** La Corte costituzionale è intervenuta più volte. Da quanto
risulta al 6 agosto 2026, e senza citare numeri di sentenza: sono cadute le **formule automatiche** che legavano
l'indennità alla sola anzianità (prima sull'art. 3, poi sull'art. 4), e il giudice **personalizza** l'importo entro
minimo e massimo valutando anzianità, dimensioni dell'impresa, comportamento delle parti e gravità del vizio; è caduto
l'avverbio che limitava la tutela reintegratoria alle nullità **espressamente** previste dalla legge, sicché rientrano
anche le nullità virtuali; la **reintegrazione attenuata** è stata estesa al licenziamento per **giustificato motivo
oggettivo** quando il fatto materiale posto a fondamento del recesso è insussistente; per le **piccole imprese** è
caduto il tetto delle 6 mensilità dell'art. 9, mentre resta il dimezzamento (*dirittobancario.it;
cortecostituzionale.it; avvocatomatteomoscioni.com; diritto-lavoro.com, verificati 6 agosto 2026*).

Materia **in movimento**: verifica lo stato aggiornato e recupera le pronunce con `civilista-giurisprudenza` prima di
indicare una forbice. Non riportare mai gli importi originari come diritto vigente: la quantificazione è oggi
**discrezionale e motivata**, non aritmetica.

### 1.3 Il rito: il rito Fornero è abrogato

Abrogato dal **D.Lgs. 149/2022** (riforma Cartabia), in vigore dal **28 febbraio 2023**; l'abrogazione opera per i
giudizi introdotti dopo quella data, le cause pendenti proseguono con la disciplina previgente (*giustiziainsieme.it,
verificato 6 agosto 2026*). Niente fase sommaria, niente opposizione. Oggi, dentro il rito del lavoro ordinario:

- **art. 441-bis c.p.c.** — le impugnazioni di licenziamento **in cui è proposta domanda di reintegrazione** hanno
  **carattere prioritario** sul ruolo del giudice, anche quando vanno risolte questioni di qualificazione del
  rapporto; il giudice può **ridurre i termini fino alla metà**, fermo un intervallo minimo di **20 giorni** tra
  notificazione e udienza; istruttoria e decisione sono concentrate; le domande connesse e riconvenzionali possono
  essere separate (*ilcaso.it, verificato 6 agosto 2026*);
- **art. 441-ter c.p.c.** — licenziamento del **socio di cooperativa**: il giudice del lavoro decide anche sulle
  questioni del rapporto associativo quando la cessazione dell'uno dipende dall'altro;
- **art. 441-quater c.p.c.** — licenziamento **discriminatorio**: l'azione di nullità si propone con ricorso ex art.
  414 c.p.c. o con i riti speciali antidiscriminatori, e la scelta preclude la successiva proposizione con rito
  diverso (*studiocataldi.it; giustiziainsieme.it, verificati 6 agosto 2026*).

Chiedere la **reintegrazione** non è solo scelta di merito: è ciò che attiva la priorità di trattazione.

### 1.4 Tipologie e cosa va provato

| Tipologia | Norma | Chi prova cosa | Punti di attacco |
|---|---|---|---|
| Giusta causa | art. 2119 c.c.; art. 7 St. lav. | il **datore** prova fatto e gravità | tempestività e specificità della contestazione, immutabilità dei fatti, proporzionalità, previsione conservativa del CCNL, recidiva |
| Giustificato motivo soggettivo | art. 3 L. 604/1966 | il **datore** | come sopra, con più peso alla proporzionalità |
| Giustificato motivo oggettivo | art. 3 L. 604/1966 | il **datore** prova ragione organizzativa, nesso con la posizione soppressa e impossibilità di ricollocazione | effettività della soppressione, *repêchage*, criteri di scelta fra posizioni fungibili, sostituzione successiva |
| Discriminatorio / ritorsivo | art. 15 St. lav.; D.Lgs. 215-216/2003; D.Lgs. 198/2006 | il lavoratore allega elementi precisi e concordanti; **onere agevolato**, con inversione sul datore | prossimità temporale con denunce, rivendicazioni, malattia, gravidanza, attività sindacale |
| Collettivo | L. 223/1991; art. 10 D.Lgs. 23/2015 | il **datore** prova procedura e criteri di scelta | comunicazione di avvio incompleta, comunicazione finale carente, criteri non verificabili, perimetro di comparazione |
| Orale | art. 2 L. 604/1966 | il **lavoratore** prova l'estromissione; il datore che eccepisce dimissioni le prova | v. § 1.1 sulla decadenza |
| In periodo protetto | art. 54 D.Lgs. 151/2001; art. 35 D.Lgs. 198/2006 | nullità, salvo deroghe di legge | maternità, paternità, causa di matrimonio: verificare le deroghe (colpa grave, cessazione dell'attività) |

Per il **collettivo**, soglie e scansioni della procedura sindacale e amministrativa (L. 223/1991) sono **da
verificare** sul testo vigente; il termine di impugnazione resta quello dell'art. 6 L. 604/1966. Lato datoriale,
l'**offerta di conciliazione** ex art. 6 D.Lgs. 23/2015 (importo non imponibile, una mensilità per anno entro 2-18,
contro rinuncia all'impugnazione) va valutata **subito dopo il recesso** (*lavoro.gov.it, verificato 6 agosto 2026*),
con importi da riverificare. **Dimissioni per fatti concludenti** (L. 203/2024): l'assenza ingiustificata oltre il
termine del CCNL o, in mancanza, oltre **15 giorni** consente al datore di far risolvere il rapporto previa
comunicazione all'Ispettorato, salvo che il lavoratore provi l'impossibilità di comunicare i motivi (*lavorosi.it,
verificato 6 agosto 2026*): lato lavoratore, va attaccata come un licenziamento mascherato.

## MODULO 2 — Crediti di lavoro

| Credito | Fonte | Onere della prova |
|---|---|---|
| Differenze retributive | CCNL; art. 36 Cost. | il **lavoratore** prova rapporto, inquadramento e prestazione; il **datore** prova il pagamento |
| Inquadramento superiore | art. 2103 c.c.; declaratorie CCNL | il **lavoratore** prova le mansioni effettive e la riconducibilità alla declaratoria |
| Mansioni superiori | art. 2103 c.c. | il **lavoratore**; assegnazione **definitiva dopo 6 mesi continuativi**, salvo diversa previsione del CCNL e salvo sostituzione di lavoratore con diritto alla conservazione del posto |
| Demansionamento | art. 2103 c.c. | il **lavoratore** prova inadempimento **e danno**, che non è *in re ipsa*; il **datore** prova le ragioni organizzative e la comunicazione scritta, richiesta a pena di nullità |
| Straordinari | CCNL; D.Lgs. 66/2003 | il **lavoratore** prova le ore eccedenti: la voce più fragile, serve prova documentale o testimoniale precisa |
| TFR | art. 2120 c.c. | il **lavoratore** prova rapporto e durata; il **datore** prova il pagamento |
| Ferie non godute | art. 10 D.Lgs. 66/2003 | il **datore** deve provare di aver **sollecitato** la fruizione e informato della perdita: senza quella prova l'indennità sostitutiva resta dovuta |

(*avvocato.it e leggeinchiaro.it per l'art. 2103 c.c.; azionesindacale.it per ferie e onere della prova — verificati 6
agosto 2026.*)

Ferie: minimo **quattro settimane** annue, due da fruire nell'anno e le restanti entro **18 mesi** dalla fine
dell'anno di maturazione; **monetizzazione vietata** in costanza di rapporto, ammessa alla cessazione. TFR: quota e
rivalutazione ex art. 2120 c.c., ancorate al testo vigente e ai coefficienti pubblicati, con fonte e data. Sui crediti
di lavoro il giudice riconosce **d'ufficio** interessi legali e **rivalutazione monetaria** dal giorno della
maturazione del diritto (art. 429 co. 3 c.p.c. — *brocardi.it, verificato 6 agosto 2026*): chiedili comunque nelle
conclusioni.

**Prescrizione.** Retribuzioni e prestazioni periodiche: **5 anni** (art. 2948 n. 4 c.c.). TFR e indennità di fine
rapporto: **5 anni** (art. 2948 n. 5 c.c.). Risarcimento da inadempimento contrattuale del datore: 10 anni (art. 2946
c.c.) (*codice-civile-online.it, verificato 6 agosto 2026*). Il punto delicato è la **decorrenza in costanza di
rapporto**: per l'orientamento formatosi in legittimità dal 2022, dopo la L. 92/2012 e il D.Lgs. 23/2015 è venuta meno
la "stabilità reale" che giustificava il decorso durante il rapporto, e la prescrizione **decorre dalla cessazione**,
a prescindere dalle dimensioni aziendali (*italpaghe.com; lavorosi.it, verificati 6 agosto 2026*). Cautele: recuperalo
in KB con `civilista-giurisprudenza` prima di fondarci una domanda; l'applicazione ai rapporti anteriori alle riforme
e al pubblico impiego è **da verificare**; con rapporto in corso e crediti risalenti **interrompi comunque**, con atto
scritto e prova della ricezione.

## MODULO 3 — Rito del lavoro (artt. 414 ss. c.p.c.)

**3.1 Il ricorso (art. 414).** Deve contenere: giudice adito; parti con codice fiscale e residenza o sede;
**determinazione dell'oggetto della domanda**; **esposizione dei fatti e degli elementi di diritto** con le
conclusioni; **indicazione specifica dei mezzi di prova** e dei documenti offerti in comunicazione (*brocardi.it,
verificato 6 agosto 2026*). La sanzione non è formale: nel rito del lavoro le **preclusioni scattano con l'atto
introduttivo**. Ciò che non è dedotto e capitolato nel ricorso non si recupera: capitoli numerati, testimoni con
generalità, documenti depositati.

**3.2 La memoria difensiva (art. 416).** Costituzione **almeno 10 giorni prima dell'udienza**. A pena di decadenza
(*brocardi.it, verificato 6 agosto 2026*): **domande riconvenzionali**; **eccezioni processuali e di merito non
rilevabili d'ufficio**, fra cui **prescrizione** e **decadenza dall'impugnazione**; **presa di posizione precisa e non
generica** sui fatti allegati (la contestazione generica equivale a non contestazione); **indicazione dei mezzi di
prova** e deposito dei documenti. Il sistema è **più rigido dell'ordinario**: non esistono memorie integrative ex art.
171-ter con cui ricostruire l'istruttoria. Chi arriva alla prima udienza con la difesa incompleta non ha una seconda
finestra.

**3.3 Sviluppo del giudizio** (*brocardi.it, verificato 6 agosto 2026*). Decreto di fissazione dell'udienza entro **5
giorni** dal deposito; udienza non oltre **60 giorni** dal deposito; notifica di ricorso e decreto entro **10 giorni**
dal decreto e comunque almeno **30 giorni** prima dell'udienza (40 se all'estero); costituzione del convenuto **10
giorni** prima dell'udienza (art. 415-416). All'esito della discussione il giudice **pronuncia sentenza dando lettura
del dispositivo**, che cristallizza la decisione, e può riservarsi fino a **60 giorni** per la motivazione (art. 429);
la sentenza è **provvisoriamente esecutiva** (art. 431).

**3.4 Sospensione feriale: NON si applica.** Le controversie di lavoro e quelle di previdenza e assistenza
obbligatorie sono **escluse** dalla sospensione feriale (art. 3 L. 742/1969, che rinvia all'art. 92 ord. giud. —
*avvocatoandreani.it; giuricivile.it, verificati 6 agosto 2026*). È la differenza che più spesso viene dimenticata da
chi fa civile ordinario. **Agosto è un mese pieno**: sui 60 e sui 180 giorni, sull'appello, sulla cassazione. Un
appello "rinviato a settembre" aggiungendo 31 giorni è inammissibile. In `civilista-scadenze` scrivi sempre:
"sospensione feriale NON applicata — controversia di lavoro".

**3.5 Appello** (*brocardi.it, verificato 6 agosto 2026*). Ricorso da depositare entro **30 giorni** dalla
notificazione della sentenza (40 se notificata all'estero); in mancanza di notificazione vale il termine lungo di **6
mesi** dalla pubblicazione (art. 434 co. 2; art. 327). Il presidente designa il relatore e fissa l'udienza entro **60
giorni**; la notifica di ricorso e decreto va fatta entro **10 giorni** dal deposito del decreto, con almeno **25
giorni** tra notificazione e udienza (60 se all'estero) (art. 435). Il ricorso va motivato **in modo chiaro, sintetico
e specifico**: per ciascun motivo, a **pena di inammissibilità**, vanno indicati il capo impugnato, le censure alla
ricostruzione dei fatti e le violazioni di legge con la loro rilevanza (art. 434).

**Art. 436-bis c.p.c. — sentenza a motivazione contestuale.** Nei casi di inammissibilità, improcedibilità e manifesta
fondatezza o infondatezza, il collegio, sentiti i difensori all'udienza, pronuncia sentenza dando lettura del
dispositivo e della motivazione **in forma sintetica**, anche con richiamo al solo punto risolutivo o a precedenti
conformi; nel rito del lavoro si passa direttamente alla discussione, senza nuova udienza né termine per note
(*brocardi.it; giustiziainsieme.it, verificati 6 agosto 2026*). Conseguenza pratica: **in appello lavoro si può uscire
dalla prima udienza con la causa decisa.**

## MODULO 4 — Prima della causa

**4.1 Tentativo di conciliazione (artt. 410-411 c.p.c.).** **Facoltativo** dopo la riforma del 2010, salvo i casi in
cui la legge lo impone (fra questi i contratti certificati, § 4.4). Si svolge davanti alla commissione presso
l'Ispettorato territoriale o nelle sedi previste dai contratti collettivi (*brocardi.it, verificato 6 agosto 2026*).
Effetti da usare in strategia: la comunicazione della richiesta **interrompe la prescrizione** e **sospende ogni
termine di decadenza** per la durata della procedura e per i **20 giorni** successivi; nel licenziamento, comunicata
entro i 180 giorni, impedisce la decadenza ma apre la coda di **60 giorni** dal rifiuto o dal mancato accordo (§ 1.1).
La controparte ha **20 giorni** per la memoria, la commissione fissa il tentativo entro **30 giorni**.

**4.2 Conciliazione in sede protetta e inoppugnabilità.** L'art. 2113 c.c. rende impugnabili entro sei mesi le rinunce
e transazioni su diritti derivanti da norme inderogabili; il **quarto comma** sottrae a quel regime le conciliazioni
concluse nelle sedi protette (giudiziale, commissione di conciliazione, sede sindacale, commissioni di
certificazione). Per questo una conciliazione lavoristica si fa **in sede protetta, non con scrittura privata**.
Operativamente: verifica l'effettiva assistenza del lavoratore da parte di chi la legge richiede; verbalizza in modo
che risulti la **consapevolezza dei diritti oggetto di rinuncia**; elenca le voci con importi, evitando rinunce
generiche a "ogni pretesa" prive di oggetto determinato. Una conciliazione mal verbalizzata è impugnabile: rischio
principale lato datore, via d'uscita lato lavoratore.

**4.3 Negoziazione assistita in materia di lavoro (art. 2-ter D.L. 132/2014).** Introdotta dal D.Lgs. 149/2022. Punto
fermo da dire sempre: **NON è condizione di procedibilità** — la norma prevede che le parti *possano* ricorrervi
"senza che ciò costituisca condizione di procedibilità della domanda giudiziale" (*wikilabour.it; giustiziainsieme.it,
verificati 6 agosto 2026*). Caratteristiche verificate: assistenza di **almeno un avvocato per parte**, con possibile
assistenza di un consulente del lavoro; accordo scritto sottoscritto da parti e difensori; trasmissione entro **10
giorni** agli organismi di cui all'art. 76 D.Lgs. 276/2003; l'accordo è titolo esecutivo e per l'iscrizione di ipoteca
giudiziale ed è sottratto al regime di impugnabilità dei primi tre commi dell'art. 2113 c.c. È uno strumento di
**chiusura transattiva stabile**, alternativo alla sede sindacale: non un adempimento da spuntare né un modo di
guadagnare tempo sulle decadenze, che si impediscono solo con la richiesta di conciliazione o arbitrato o col deposito
del ricorso.

**4.4 Certificazione dei contratti (artt. 75 ss. D.Lgs. 276/2003).** Procedura volontaria davanti a commissioni
abilitate (enti bilaterali, Ispettorato, università in albo, consigli provinciali dei consulenti del lavoro,
ministero). Gli effetti **permangono fino alla sentenza di merito** che accolga il ricorso; si impugna davanti al
giudice del lavoro per erronea qualificazione, difformità fra programma certificato ed esecuzione o vizi del consenso,
e davanti al giudice amministrativo per violazione del procedimento o eccesso di potere. Per i contratti certificati
il **tentativo di conciliazione davanti alla commissione è presupposto obbligatorio** del ricorso (*wikilabour.it,
verificato 6 agosto 2026*; termini di dettaglio **da verificare**). Certificare non rende inattaccabile il contratto
ma sposta il baricentro probatorio: è il primo documento da chiedere quando si contesta la qualificazione.

## MODULO 5 — Previdenza e assistenza obbligatorie

Rito del lavoro (artt. 442 ss. c.p.c.) e **nessuna sospensione feriale** (§ 3.4).

**INPS.** Il **ricorso amministrativo** ai comitati dell'Istituto è **condizione di procedibilità** ex art. 443
c.p.c.: se manca, il giudice non rigetta ma **sospende** assegnando un termine per proporlo (*studiolegalemondello.it,
verificato 6 agosto 2026*). Termine per il ricorso amministrativo: **90 giorni** dalla comunicazione del
provvedimento, con termini più brevi per alcune prestazioni; se l'Istituto non risponde alla domanda iniziale il
termine decorre dal decorso di **120 giorni**; trascorsi **90 giorni** dal ricorso senza decisione si può agire.
**Decadenza dall'azione giudiziaria** (art. 47 D.P.R. 639/1970): risulta **3 anni** per le prestazioni pensionistiche
e **1 anno** per quelle temporanee, con decorrenza dalla comunicazione della decisione o dalla scadenza del termine
per deciderla; un secondo ricorso amministrativo **non riapre** il termine (*lexced.com; studiolegalemondello.it,
verificati 6 agosto 2026*). La perimetrazione delle prestazioni assistenziali e i raccordi con l'art. 42 D.L. 269/2003
sono **da verificare**. **Spese**: la parte soccombente con reddito imponibile non superiore al doppio della soglia
del D.P.R. 115/2002 è esente da spese e onorari, e nelle conclusioni dell'atto introduttivo vanno inserite la
**dichiarazione sostitutiva** del reddito e la dichiarazione del valore della prestazione (art. 152 disp. att. c.p.c. —
*brocardi.it, verificato 6 agosto 2026*). Dimenticarla espone il cliente a spese evitabili.

**INAIL.** Risulta un'**opposizione amministrativa** entro **60 giorni** dalla comunicazione, di natura ordinatoria, e
una **prescrizione triennale** dell'azione per le prestazioni dal giorno dell'infortunio o dalla manifestazione della
malattia professionale, **sospesa durante il procedimento amministrativo** (formulazione corrente: tre anni più 150
giorni, con termine più ampio per le revisioni) (*studiobuccilli.com; lavorosi.it; judicium.it, verificati 6 agosto
2026*). Le durate esatte della sospensione sono **da verificare** con `civilista-giurisprudenza`. In materia
previdenziale **si agisce prima e si discute poi**: le decadenze sono di ordine pubblico.

## Tabella riassuntiva dei termini

Il calcolo si fa con `civilista-scadenze`. Qui c'è solo la mappa dei termini e delle decorrenze.

| Adempimento | Termine | Decorrenza | Norma |
|---|---|---|---|
| Impugnazione stragiudiziale del licenziamento | **60 giorni** | ricezione della comunicazione scritta, o dei motivi | art. 6 co. 1 L. 604/1966 |
| Deposito del ricorso o richiesta di conciliazione | **180 giorni** | impugnazione stragiudiziale (spedizione) | art. 6 co. 2 L. 604/1966 |
| Deposito del ricorso dopo conciliazione fallita | **60 giorni** | rifiuto o mancato accordo | art. 6 co. 2 L. 604/1966 |
| Impugnazione di trasferimento, termine, cessione di contratto, co.co.co. | 60 + 180 giorni | atto impugnato o scadenza del termine | art. 32 L. 183/2010 |
| Costituzione del convenuto | **10 giorni** prima dell'udienza | udienza (a ritroso) | art. 416 c.p.c. |
| Udienza di discussione | entro **60 giorni** dal deposito | deposito del ricorso | art. 415 c.p.c. |
| Notifica di ricorso e decreto | 10 giorni; almeno **30 giorni** prima dell'udienza | decreto / udienza | art. 415 c.p.c. |
| Deposito della motivazione | fino a **60 giorni** | udienza di discussione | art. 429 c.p.c. |
| Appello | **30 giorni** (40 dall'estero) | notificazione della sentenza | art. 434 co. 2 c.p.c. |
| Appello senza notificazione | **6 mesi** | pubblicazione della sentenza | art. 327 c.p.c. |
| Notifica dell'appello | 10 giorni; almeno **25 giorni** prima dell'udienza | decreto / udienza | art. 435 c.p.c. |
| Ricorso per cassazione | **60 giorni** / 6 mesi | notificazione / pubblicazione | artt. 325, 327 c.p.c. |
| Prescrizione retribuzioni e TFR | **5 anni** | cessazione del rapporto (orientamento dal 2022) | art. 2948 nn. 4 e 5 c.c. |
| Impugnazione di rinunce e transazioni | 6 mesi | cessazione del rapporto o data della rinuncia | art. 2113 c.c. |
| Ricorso amministrativo INPS | **90 giorni** | comunicazione del provvedimento | D.P.R. 639/1970 |
| Azione giudiziaria previdenziale | **3 anni / 1 anno** | decisione o scadenza del termine per deciderla | art. 47 D.P.R. 639/1970 |
| Prescrizione prestazioni INAIL | **3 anni**, con sospensione | infortunio o manifestazione della malattia | disciplina INAIL, **da verificare** |

**Su nessuno di questi termini si applica la sospensione feriale.**

## Errori ricorrenti

1. **Calcolare i 180 giorni dal licenziamento invece che dall'impugnazione stragiudiziale.** Contare dal recesso
   accorcia il termine reale di quasi due mesi e fa archiviare come decadute cause ancora vive.
2. **Applicare la sospensione feriale a una causa di lavoro.** Lavoro e previdenza sono escluse: agosto conta per
   intero, sui 60 giorni, sui 180 giorni, sull'appello, sulla cassazione.
3. **Sbagliare il regime sanzionatorio per la data di assunzione.** Assunto entro il 6 marzo 2015 o dal 7 marzo 2015?
   Il rapporto è stato convertito dopo quella data? La soglia è stata superata con assunzioni successive?
4. **Riportare le indennità del D.Lgs. 23/2015 come stanno nel testo originario.** Le formule automatiche sono cadute
   e la reintegrazione è stata estesa: verificalo con `civilista-giurisprudenza` prima di indicare una forbice.
5. **Impostare la causa con il rito Fornero.** È abrogato dal 28 febbraio 2023: ricorso ex art. 414 c.p.c., con la
   priorità di trattazione dell'art. 441-bis se si chiede la reintegrazione.
6. **Depositare un ricorso ex art. 414 senza capitoli di prova e documenti.** Le preclusioni scattano con l'atto
   introduttivo e non ci sono memorie integrative con cui rimediare. Lato passivo vale per la memoria ex art. 416:
   riconvenzionale, prescrizione e decadenza si propongono lì o non più.
7. **Contestare genericamente i fatti avversi.** La presa di posizione dev'essere precisa e analitica: la
   contestazione generica regala al ricorrente i fatti costitutivi.
8. **Trattare la negoziazione assistita in materia di lavoro come condizione di procedibilità.** Non lo è, ed è uno
   strumento di chiusura, non un modo di guadagnare tempo sulle decadenze.
9. **Chiudere una transazione lavoristica con scrittura privata.** Fuori dalle sedi protette resta impugnabile ex art.
   2113 c.c.: un accordo che il cliente crede definitivo e non lo è.
10. **Andare in appello lavoro senza aver preparato la discussione orale.** Con l'art. 436-bis la causa può essere
    decisa alla prima udienza con motivazione contestuale.

## Integrazione con il fascicolo e stile

Al termine di ogni analisi: scrivi nello **SCADENZIARIO** i due termini di impugnazione con le decorrenze **e la prova
documentale di ciascuna** (ricevuta di consegna del licenziamento, ricevuta di accettazione della PEC di impugnazione)
— un termine senza prova della data-evento è provvisorio; registra nella scheda del caso natura del rapporto, CCNL,
anzianità, dimensioni datoriali e **data di assunzione con il regime che ne discende**; indicizza con
`civilista-archivio` licenziamento, contestazione, giustificazioni, buste paga, CCNL e verbali sindacali. Wikilink e
indici li mantieni tu.

Scrivi come un giuslavorista che parla a un collega: tecnico, diretto, imperativo — "impugna", "eccepisci la
decadenza". **Ogni volta che compare un licenziamento, la prima frase riguarda i termini.** Distingui fatto allegato e
fatto provato e dichiara ciò che non hai verificato. Ogni atto è una **bozza**: la decisione resta del difensore.
