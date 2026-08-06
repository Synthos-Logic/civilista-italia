---
name: civilista-monitorio
description: >
  Workflow decisionale del procedimento monitorio italiano e della sua opposizione, dal recupero del credito fino all'esecuzione,
  dal lato del creditore e dal lato del debitore. ATTIVARE SEMPRE quando l'avvocato dice o chiede: 'decreto ingiuntivo', 'ricorso
  monitorio', 'facciamo un decreto ingiuntivo', 'conviene il decreto ingiuntivo o la causa ordinaria', 'recupero crediti', 'il
  cliente non paga', 'come recuperiamo questo credito', 'abbiamo prova scritta sufficiente', 'chiediamo la provvisoria esecuzione',
  'art. 642', 'quando devo notificare il decreto', 'il decreto è diventato inefficace', 'dichiarazione di esecutorietà', 'art. 647',
  'opposizione a decreto ingiuntivo', 'ho ricevuto un decreto ingiuntivo', 'ci hanno notificato un decreto ingiuntivo', 'quanto
  tempo ho per oppormi', 'conviene opporsi', 'sospensione della provvisoria esecuzione', 'art. 649', 'gravi motivi', 'ci hanno
  chiesto la provvisoria esecuzione', 'art. 648', 'opposizione tardiva', 'art. 650', 'chi deve fare la mediazione
  nell'opposizione', 'il decreto è stato revocato', 'possiamo procedere a precetto'. Attivare anche quando il cliente porta in
  studio un decreto appena notificato: la prima cosa è la check-list dei primi sette giorni contenuta in questa skill.
---

# civilista-monitorio — Procedimento d'ingiunzione e opposizione

Il monitorio è il procedimento in cui si vince o si perde **prima** di discutere il merito. Per il creditore tutto dipende dalla prova scritta e dalla tempestività
della notifica; per il debitore da **due date** (notifica del decreto, scadenza dei quaranta giorni) e da **due istanze** (artt. 648 e 649 c.p.c.). Questa skill è il
**workflow decisionale**: cosa fare, in che ordine, con quali rischi.

**Divisione del lavoro — rispettala, non duplicare:**

| Serve | Skill |
|---|---|
| Struttura e testo di ricorso monitorio, opposizione, precetto, diffida | `civilista-atti` (moduli 4, 5, 9, 10) |
| Qualificazione, onere della prova, valutazione economica | `civilista-caso` |
| Calcolo di ogni data, sospensione feriale, scadenziario | `civilista-scadenze` |
| Mediazione e negoziazione assistita in dettaglio | `civilista-adr` |
| Massime e orientamenti (quote-then-claim sulla KB) | `civilista-giurisprudenza` |
| Interessi, rivalutazione, nota spese | `civilista-quantificazione` |
| Quadro sostanziale | `KNOWLEDGE_BASE/06_SCHEDE_MATERIA/A_CONTRATTI_E_CREDITI/RECUPERO_CREDITI_E_DECRETO_INGIUNTIVO.md` |

**Regole vincolanti.** Nessun numero di sentenza: le massime si cercano con `civilista-giurisprudenza`. Nessun nome reale. Ogni dato numerico porta la data di
verifica. Ciò che si produce è una **bozza**.

*Norme verificate il 6 agosto 2026 sul testo vigente del c.p.c. e del D.Lgs. 28/2010; stato dei dati in fondo.*

---

# PARTE I — LATO CREDITORE

## MODULO 0 — La scelta della strada

Prima domanda, sempre: **il decreto ingiuntivo è davvero lo strumento giusto?** Un credito documentato male non diventa buono con un decreto: diventa un decreto
opposto, cioè la causa ordinaria che si sarebbe fatta comunque, più i costi del monitorio e un titolo che nel frattempo non produce pressione.

| Strada | Quando conviene | Rischio principale |
|---|---|---|
| **Diffida** (art. 1219 c.c.) | Credito modesto; debitore solvibile ma disorganizzato; rapporto da preservare; prescrizione da interrompere subito | Solo la perdita di tempo con chi non intende pagare |
| **Ricorso monitorio** (artt. 633 ss.) | Prova scritta forte; opposizione improbabile o debole; serve un titolo rapido | Con l'opposizione si finisce in cognizione piena e il creditore deve provare tutto |
| **Rito semplificato** (artt. 281-decies ss.) | Fatti non controversi o prova documentale ma opposizione certa; causa monocratica da portare subito a sentenza | Nessun titolo prima della sentenza, nessun effetto-pressione |
| **Citazione ordinaria** (art. 163) | Prova da costruire con testimoni o CTU; domande ulteriori (risoluzione, risarcimento, accertamento) | Costo, durata, rischio spese anticipato per intero |

**Sul rito semplificato.** Nelle sole cause in cui il tribunale giudica in composizione **monocratica** il giudizio **può sempre** essere introdotto nelle forme del
procedimento semplificato, anche se non ricorrono i presupposti del primo comma dell'art. 281-decies (fatti non controversi, prova documentale, pronta soluzione,
istruzione non complessa): è il secondo comma come modificato dal correttivo, e amplia la convenienza della via diretta quando l'opposizione è certa.

**I sei criteri, in ordine di peso.** (1) **Qualità della prova scritta**: regge da sola l'art. 634 c.p.c.? Una fattura non accettata contro un non imprenditore
ottiene il decreto ma non lo difende. (2) **Probabilità di opposizione**: contestazioni scritte già ricevute, contabilità in contenzioso, legale di controparte già
intervenuto rendono l'opposizione certa, e allora il monitorio serve solo se è ottenibile la provvisoria esecuzione ex art. 642 c.p.c. (3) **Valore**: sotto una
certa soglia il costo del recupero supera il beneficio — confronto **prima**, con `civilista-quantificazione`, messo per iscritto al cliente. (4) **Urgenza**: se il
patrimonio è in dismissione la domanda non è "monitorio o ordinario" ma **sequestro conservativo** (art. 671 c.p.c.). (5) **Solvibilità**: visura camerale e bilanci,
ipocatastale, protesti e pregiudizievoli, PRA — un titolo contro un incapiente è un costo con la copertina rigida. (6) **Filtro di procedibilità**: se la materia è a
mediazione obbligatoria il monitorio salta il filtro all'inizio ma lo reincontra dopo l'opposizione, con l'onere a proprio carico (Modulo 8). **Domanda di controllo,
sempre:** *se il debitore si oppone, con quali documenti proviamo il rapporto, la prestazione e l'importo?* Se non c'è risposta, non c'è ricorso.

---

## MODULO 1 — Requisiti del ricorso

**Il credito** deve essere **certo, liquido ed esigibile** e avere per oggetto una somma di denaro, una determinata quantità di cose fungibili o una cosa mobile
determinata (art. 633 c.p.c.). Esigibile significa termine di pagamento scaduto: un ricorso su fatture non ancora scadute è inammissibile.

**Prova scritta (art. 634 co. 1).** Polizze e promesse unilaterali per scrittura privata e telegrammi, anche se privi dei requisiti del codice civile.

**Prova privilegiata degli imprenditori — e oggi anche dei lavoratori autonomi (art. 634 co. 2).** Nel testo vigente, per i crediti relativi a somministrazioni di
merci e di danaro **nonché per prestazioni di servizi** fatte da imprenditori che esercitano attività commerciale **e da lavoratori autonomi**, anche a persone che
non esercitano tale attività, sono prove scritte idonee gli **estratti autentici delle scritture contabili** di cui agli artt. 2214 ss. c.c. e di quelle prescritte
dalle leggi tributarie, purché tenute **anche con strumenti informatici** con l'osservanza delle norme di legge. In pratica serve l'**estratto autentico** (libro
giornale, partitari), non un tabulato gestionale; le scritture devono risultare **regolarmente tenute**, ed è il primo punto che l'opponente attacca; la **fattura
elettronica via Sistema di Interscambio** come autonoma prova monitoria è materia di prassi non uniforme, da usare a corredo e non da sola.

**Professionisti (art. 636).** Nei casi dei nn. 2 e 3 dell'art. 633 la domanda deve essere accompagnata dalla **parcella** sottoscritta dal ricorrente e corredata
dal **parere della competente associazione professionale** — oggi il Consiglio dell'Ordine. Il parere non occorre se l'importo è determinato in base a **tariffe
obbligatorie**; poiché le tariffe professionali sono state abrogate nel 2012, quell'esenzione ha spazio residuale e il parere di congruità torna di regola
necessario. Il parere **vincola il giudice nella sola fase monitoria** entro il limite della somma richiesta: **nell'opposizione non prova nulla**, e il
professionista deve provare incarico ed effettività delle prestazioni. Per i compensi dell'avvocato verso il cliente esiste anche la via dell'art. 14 D.Lgs.
150/2011: **da verificare** quale convenga. Per i crediti dello Stato e degli enti pubblici valgono le prove privilegiate dell'art. 635: **verificare il testo
vigente**.

**Documenti e competenza (artt. 637-638, 640).** Il ricorso indica le prove e le deposita: un ricorso senza documenti è un ricorso rigettato, e il rigetto è
pronunciato con decreto non impugnabile, ma **la domanda è riproponibile** — non è una preclusione, è un costo. È competente il giudice che lo sarebbe per la domanda
ordinaria; attenzione al **foro del consumatore**, esclusivo, inderogabile e rilevabile d'ufficio, che è il vizio che uccide più decreti. Struttura e template del
ricorso → **`civilista-atti`, modulo 4**.

---

## MODULO 2 — La provvisoria esecuzione ex art. 642

**Non è mai concessa d'ufficio: va chiesta nel ricorso.** Ciò che cambia è il margine del giudice.

| Comma | Presupposto | Margine del giudice |
|---|---|---|
| **642 co. 1** | Credito fondato su **cambiale**, **assegno bancario o circolare**, **certificato di liquidazione di borsa**, **atto ricevuto da notaio o altro pubblico ufficiale autorizzato** | Su istanza del ricorrente ingiunge di pagare **senza dilazione** e autorizza l'esecuzione provvisoria: presupposti tipizzati, nessuna valutazione sul pericolo |
| **642 co. 2** | **Pericolo di grave pregiudizio nel ritardo**, ovvero **documentazione sottoscritta dal debitore** comprovante il diritto | Discrezionale; il giudice **può imporre cauzione** al ricorrente |
| **642 co. 3** | Negli stessi casi | Può autorizzare l'esecuzione **senza osservare il termine dell'art. 482** (i dieci giorni dal precetto) |

**Il pericolo va allegato con fatti:** protesti, esecuzioni di terzi in corso, iscrizioni pregiudizievoli, cessioni di azienda o immobili, bilanci in perdita, revoca
di affidamenti. Una frase di stile produce il rigetto dell'istanza.

**Conseguenze della scelta, da spiegare al cliente prima.** *Pro:* titolo esecutivo subito, si precetta e si pignora durante l'opposizione e molte opposizioni si
chiudono a stralcio. *Contro:* si apre il fronte dell'**art. 649** e la partita si concentra su quell'udienza; può essere imposta **cauzione**; l'esecuzione su un
decreto poi revocato espone a restituzioni e a responsabilità per esecuzione ingiusta. *Regola pratica:* con il presupposto del comma 1 chiederla sempre; con quello
del comma 2 solo se il pericolo è documentabile e si è pronti a difenderla in contraddittorio entro poche settimane.

---

## MODULO 3 — Notifica, termini, esecutorietà

**Notifica a pena di inefficacia (art. 644).** Il decreto diventa **inefficace** se la notificazione non è eseguita entro **60 giorni** dalla pronuncia se deve
avvenire nel territorio della Repubblica, **90 giorni** negli altri casi; la domanda **può essere riproposta**, con nuovo ricorso e nuovo contributo. Nella prassi si
computa dal deposito in cancelleria: verificare l'uso dell'ufficio e, nel dubbio, contare dalla data più sfavorevole. L'inefficacia non opera in automatico: va fatta
dichiarare.

**Termine per il debitore (art. 641).** Decreto emesso entro **30 giorni** dal deposito del ricorso; ingiunzione a pagare entro **40 giorni**, con l'espresso
avvertimento che nello stesso termine può essere proposta opposizione e che in mancanza si procederà a esecuzione forzata. Varianti: **10 giorni** se ridotto per
giusti motivi, **60 giorni** se aumentato per giusti motivi; **50 giorni** (riducibili fino a 20) se l'intimato risiede in altro Stato dell'Unione europea; **60
giorni**, non inferiori a 30 né superiori a 120, se risiede in altri Stati. Il termine scritto **nel singolo decreto prevale**: leggerlo, non presumerlo. Con il
decreto il giudice **liquida le spese**: vanno chieste e quantificate nel ricorso, con nota spese.

**Esecutorietà per mancata opposizione (art. 647).** Se l'opposizione non è proposta nel termine **oppure l'opponente non si è costituito**, il giudice che ha
pronunciato il decreto, su istanza **anche verbale** del ricorrente, lo dichiara esecutivo; nel primo caso ordina la rinnovazione della notificazione quando risulta
o appare probabile che l'intimato non abbia avuto conoscenza del decreto. Dichiarato esecutivo, **l'opposizione non può più essere proposta né proseguita**, salvo
l'art. 650, e la cauzione è liberata. Due avvertenze: l'esecutorietà **va chiesta**; e la **mancata costituzione dell'opponente** che pure ha notificato
l'opposizione è una causa di esecutorietà che quasi nessuno controlla.

**Esito dell'opposizione (art. 653).** Rigetto con sentenza passata in giudicato o provvisoriamente esecutiva, o estinzione: il decreto acquista efficacia esecutiva
se non l'aveva. Accoglimento **parziale**: il titolo è la **sentenza**, ma gli atti di esecuzione già compiuti conservano effetto nei limiti della somma ridotta.

---

## MODULO 4 — Dopo il decreto: precetto ed esecuzione

1. **Titolo.** Decreto esecutivo ex art. 642, o dichiarato esecutivo ex art. 647, o sentenza ex art. 653; si notifica **copia attestata conforme** (art. 475), non
   serve più la spedizione in forma esecutiva.
2. **Precetto** (artt. 480 ss.): per il decreto già notificato e divenuto esecutivo si indica il provvedimento che ne ha disposto l'esecutorietà (art. 654).
   Contenuto a pena di nullità, avvertimento sul sovraindebitamento, elezione di domicilio nel comune del giudice dell'esecuzione. Template → **`civilista-atti`,
   modulo 9**.
3. **Termini.** Dilatorio di **10 giorni** (art. 482), salvo autorizzazione ex art. 642 co. 3; il precetto **perde efficacia** se l'esecuzione non inizia entro **90
   giorni** dalla notificazione (art. 481). Istanza di vendita o assegnazione entro **45 giorni** dal pignoramento (art. 497); il termine di **iscrizione a ruolo**
   varia secondo la forma di espropriazione ed è breve e perentorio: verificarlo sulla norma applicabile.
4. **Limiti da dire al cliente prima di iniziare.** Impignorabilità e limiti su stipendi e pensioni, incapienza, concorso con altri creditori, sovraindebitamento e
   liquidazione. **La materia esecutiva e concorsuale non è coperta in profondità da questo kit**: dichiararlo e lavorare solo su ciò che è ancorabile.

---

# PARTE II — LATO DEBITORE (OPPOSIZIONE)

> Se il cliente è appena arrivato con il decreto in mano, vai al **Modulo 11**: prima la check-list dei sette giorni, poi il resto.

## MODULO 5 — Il termine di opposizione, e l'errore che costa la causa

**Quaranta giorni dalla notificazione del decreto** (artt. 641 e 645), salvo il diverso termine scritto nel decreto (varianti al Modulo 3). È **perentorio**:
scaduto, il decreto è dichiarabile esecutivo ex art. 647 e l'opposizione non è più proponibile, salvo l'art. 650. Soggetto alla **sospensione feriale** (1-31
agosto). Calcolo → `civilista-scadenze`.

### Avvertenza forte — la domanda di mediazione NON interrompe né sospende il termine

**Depositare una domanda di mediazione non ferma i quaranta giorni.** L'art. 8 D.Lgs. 28/2010 attribuisce alla domanda gli effetti della domanda giudiziale **sulla
prescrizione** e l'idoneità a **impedire la decadenza per una sola volta**: effetti che operano sulle decadenze **sostanziali**, non sui termini **processuali** come
quello dell'art. 641 c.p.c. La giurisprudenza di merito più recente lo afferma espressamente, anche per impedire un uso dilatorio della mediazione (verificato al 6
agosto 2026; massima → `civilista-giurisprudenza`). In passato **una parte della giurisprudenza di merito ha sostenuto la tesi opposta**: non è una ragione per
correre il rischio, è una ragione in più per opporsi nel termine.

**Regola operativa, senza eccezioni:** trattativa, saldo e stralcio, mediazione e piano di rientro si conducono **dopo** aver notificato l'opposizione, o con l'atto
già pronto. Mai al posto dell'opposizione.

---

## MODULO 6 — L'opposizione ex art. 645

**Forma e giudice.** Atto di citazione davanti **all'ufficio giudiziario al quale appartiene il giudice che ha emesso il decreto**, notificato all'opposto secondo le
norme ordinarie, con deposito di copia nel fascicolo; costituzione dell'opponente nel termine dell'art. 165.

**Rito.** Il giudizio si svolge secondo le norme del **procedimento ordinario di cognizione** davanti al giudice adito; seguendo il rito ordinario l'udienza di
comparizione è fissata **non oltre trenta giorni dalla scadenza del termine minimo a comparire**. Il **dimezzamento per legge dei termini di comparizione non è più
previsto**. Dopo il correttivo l'opposizione può essere introdotta anche nelle forme del **rito semplificato**, per il tramite dell'art. 281-decies co. 3, che
richiama espressamente le opposizioni a precetto (art. 615), agli atti esecutivi (art. 617) e a decreto ingiuntivo (art. 645); il giudice può **mutare il rito**.
Conviene all'opponente se la difesa è **documentale**, la contestazione del quantum è secca o il vizio di rito è evidente; **non** conviene se servono CTU, testimoni
o riconvenzionali complesse.

**Inversione sostanziale dei ruoli — il cuore di tutto.** L'opponente è **attore formale** ma **convenuto sostanziale**; l'opposto è convenuto formale ma **attore
sostanziale** e su di lui grava l'onere di provare i **fatti costitutivi del credito** (art. 2697 c.c.). Il monitorio non inverte l'onere della prova: lo
**posticipa**. Conseguenze:

- nell'atto di opposizione si svolgono **le difese del convenuto**: contestazione **specifica** dei fatti (quella generica equivale a non contestazione), eccezioni
  non rilevabili d'ufficio, riconvenzionali;
- **non basta** attaccare la prova monitoria: il difetto di prova ex art. 634 rende inammissibile il ricorso nella fase sommaria, ma nell'opposizione **non è
  insanabile**, perché l'opposto integra con i mezzi ordinari. Si attacca il **rapporto**, non solo il documento;
- **preclusioni:** eccezioni in senso stretto (prescrizione, compensazione giudiziale, incompetenza territoriale derogabile) e riconvenzionali vanno spese
  **nell'atto di opposizione**; le memorie dell'art. 171-ter servono a precisare, non a introdurre;
- lato **opposto**: produrre **tutta** la documentazione del rapporto, non contare sul decreto come prova, valutare riconvenzione o estensione della domanda per gli
  importi maturati dopo il ricorso. Struttura e template dell'atto → **`civilista-atti`, modulo 5**.

---

## MODULO 7 — Le due istanze che decidono l'esito pratico

Nei primi trenta-sessanta giorni si decide chi ha in mano il titolo.

**Art. 649 — sospensione della provvisoria esecuzione (istanza dell'opponente).** Testo vigente: il giudice istruttore, su istanza dell'opponente, quando ricorrono
**gravi motivi**, può, con **ordinanza non impugnabile**, sospendere l'esecuzione provvisoria del decreto concessa a norma dell'art. 642.

- **Presupposto unico: i gravi motivi**, che nella prassi si compongono di due elementi da allegare e documentare **entrambi**: **fondatezza apparente
  dell'opposizione** e **pregiudizio concreto** dell'esecuzione (blocco dell'attività, pignoramento del conto operativo, difficoltà di restituzione dell'opposto).
  **Non bastano** l'affermazione che il credito non è dovuto, le difficoltà economiche allegate genericamente, i documenti prodotti senza spiegare cosa provano.
- **Effetti:** ferma l'esecuzione, **non revoca** il decreto, che resta in vita fino alla sentenza. Ordinanza **non impugnabile**: non c'è un secondo grado, quindi
  la prima istanza è decisiva. Se il precetto è già arrivato, chiedere la sospensione **in via d'urgenza prima dell'udienza**, con istanza separata e ragioni
  indicate: **prassi degli uffici non uniforme**, verificarla presso il tribunale adito.

**Art. 648 — provvisoria esecuzione del decreto opposto (istanza dell'opposto).**

| Comma | Contenuto |
|---|---|
| **Co. 1** | Se l'opposizione **non è fondata su prova scritta o di pronta soluzione**, il giudice istruttore, su istanza dell'opposto, concede con **ordinanza non impugnabile** l'esecuzione provvisoria del decreto, se non già concessa, **alla prima udienza** |
| **Co. 2** | Concede in ogni caso l'esecuzione provvisoria **limitatamente alle somme non contestate**, salvo che l'opposizione riguardi vizi procedurali |
| **Co. 3** | L'esecuzione provvisoria **deve** essere concessa se chi la chiede offre **cauzione** per l'ammontare delle eventuali restituzioni, spese e danni |
| **Co. 4** (correttivo) | Se ricorrono **ragioni di urgenza specificamente indicate**, la parte costituita può chiedere che la decisione sia pronunciata **prima dell'udienza di comparizione**, con ordinanza non impugnabile |

Il comma 4 cambia i tempi reali: prima, tra i quaranta giorni per opporsi e il termine minimo a comparire, il creditore opposto poteva attendere mesi la prima
udienza; ora può chiederne l'anticipazione **motivando l'urgenza in modo specifico** — la genericità porta al rinvio.

**Come si imposta l'opposizione per resistere all'art. 648**, fin dall'atto introduttivo: (a) ancorarla a una **prova scritta** (contratto difforme, quietanza, nota
di credito, contestazione tempestiva, corrispondenza) o a una questione **di pronta soluzione** (prescrizione compiuta, difetto di legittimazione, foro del
consumatore); (b) **contestare voce per voce**, mai in blocco, perché ciò che non è specificamente contestato diventa "somma non contestata" ed è comunque esecutivo
ex co. 2; (c) presidiare la **cauzione** del co. 3, che rende dovuta la concessione.

**Sequenza tipica.** Notifica del decreto → opposizione nel termine → eventuali istanze anticipate (648 co. 4 dell'opposto, 649 dell'opponente) → verifiche
preliminari e prima udienza → **pronuncia su 648/649** → **da qui si riespande la condizione di procedibilità** (Modulo 8) → istruttoria → sentenza (art. 653).

---

## MODULO 8 — Mediazione: si riespande dopo le istanze, e l'onere è del creditore

**Esclusione iniziale, poi riespansione.** La condizione di procedibilità **non si applica** al procedimento per ingiunzione, **inclusa l'opposizione**, **fino alla
pronuncia sulle istanze di concessione e di sospensione della provvisoria esecuzione** (art. 5 co. 6 D.Lgs. 28/2010; esclusione corrispondente per la negoziazione
assistita, art. 3 D.L. 132/2014): è ciò che rende il monitorio la via più rapida quando la materia è comunque filtrata. Decise le istanze ex artt. 648-649, se la
materia rientra tra quelle dell'art. 5 co. 1 (contratti assicurativi, bancari e finanziari; locazione; comodato; affitto d'azienda; contratto d'opera;
somministrazione; franchising; subfornitura; condominio; società di persone; e le altre elencate), la **mediazione torna obbligatoria**.

**Chi deve attivarla — art. 5-bis D.Lgs. 28/2010.** Quando l'azione di cui all'art. 5 co. 1 è stata introdotta con ricorso per decreto ingiuntivo, nel procedimento
di opposizione l'onere di presentare la domanda di mediazione grava sulla **parte che ha proposto ricorso per decreto ingiuntivo**, cioè sul **creditore opposto**,
non sul debitore opponente (verificato al 6 agosto 2026). Il giudice, provveduto sulle istanze, verifica l'esperimento della mediazione; se manca, assegna il termine
per il deposito e fissa udienza dopo la scadenza del termine di durata. Se la mediazione non è comunque esperita, **dichiara l'improcedibilità della domanda e revoca
il decreto ingiuntivo**, provvedendo sulle spese.

**Durata: sei mesi**, prorogabile prima della scadenza per periodi non superiori a tre mesi ciascuno; nella mediazione demandata dal giudice, sei mesi prorogabili
una sola volta di ulteriori tre (art. 6 D.Lgs. 28/2010 nel testo modificato nel 2024). Primo incontro tra **20 e 40 giorni** dal deposito (art. 8). **Nessuna
sospensione feriale.** Dettaglio → `civilista-adr`.

**Le due letture.** *Creditore opposto:* il decreto si perde per **inerzia propria** — il giorno stesso dell'ordinanza, domanda in scadenziario e deposito.
*Opponente:* è una caduta del titolo che **non costa nulla** — se il termine passa a vuoto, eccepire l'improcedibilità e chiedere la revoca.

---

## MODULO 9 — Opposizione tardiva (art. 650)

Presupposti **stretti**, da provare e non da affermare: l'intimato può opporsi anche dopo la scadenza se **prova di non avere avuto tempestiva conoscenza** del
decreto per **irregolarità della notificazione**, **caso fortuito** o **forza maggiore**. Non basta non aver ritirato la raccomandata, né la disorganizzazione
propria: va ricostruita la vicenda notificatoria documento per documento (relata, avviso di ricevimento, compiuta giacenza, PEC e registri, residenza o sede
effettiva alla data).

**Termine: l'opposizione non è più ammessa decorsi dieci giorni dal primo atto di esecuzione**, tipicamente il pignoramento, non da quando il cliente se ne accorge.
Se nessun atto di esecuzione è stato compiuto, il *dies a quo* è **questione controversa**: agire in modo conservativo appena si ha conoscenza del decreto.
L'esecutorietà può essere sospesa a norma dell'art. 649 (art. 650 co. 2): istanza da proporre contestualmente.

---

## MODULO 10 — Difese tipiche dell'opponente

Da percorrere **tutte** in sede di analisi, poi selezionare: tre motivi solidi valgono più di dieci.

**Rito e vizi formali.** (1) **Vizi della notificazione** del decreto: incidono sulla decorrenza del termine e aprono l'art. 650. (2) **Inefficacia ex art. 644** per
notifica oltre i 60/90 giorni. (3) **Incompetenza** per valore, materia o territorio, con il **foro del consumatore** esclusivo, inderogabile e rilevabile d'ufficio.
(4) **Difetto di prova scritta ex artt. 634-636**: fatture non accettate contro non imprenditore, scritture contabili irregolari o prive di estratto autentico,
parcella priva del parere — arma utile per l'art. 649, non risolutiva nel merito. (5) **Vizi del decreto**: difetto di motivazione, ultrapetizione rispetto al
ricorso, spese liquidate male.

**Merito.** (6) **Contestazione dell'an**: inesistenza o diversa qualificazione del rapporto, difetto di legittimazione, credito ceduto senza prova della cessione e
della sua opponibilità. (7) **Contestazione del quantum, voce per voce**: acconti non scomputati, note di credito, sconti pattuiti, prezzi difformi dall'ordine,
interessi ultralegali privi di forma scritta (art. 1284 co. 3 c.c.). (8) **Eccezione di inadempimento** (art. 1460 c.c.): richiede contestazioni tempestive e
documentate e proporzionalità del rifiuto. (9) **Compensazione** (artt. 1241 ss.): legale se il controcredito è certo, liquido ed esigibile, altrimenti giudiziale ex
art. 1243 co. 2; **eccezione in senso stretto**. (10) **Prescrizione** (eccezione in senso stretto, art. 2938 c.c.): decennale ordinaria, quinquennale per canoni,
interessi e prestazioni periodiche, triennale per i compensi dei professionisti, annuale per mediatori e spedizionieri; ricostruire gli atti interruttivi. (11)
**Nullità e abusività rilevabili d'ufficio**: difetto di forma, clausole abusive verso il consumatore, nullità nei contratti bancari e finanziari. (12) **Rapporti
bancari**: contratto quadro non prodotto, anatocismo, tasso soglia, commissioni non pattuite, con **CTU contabile** e quesiti impostati fin dall'atto. (13) **Fatti
estintivi**: pagamento (quietanze e contabili riconducibili alle fatture), transazione, saldo e stralcio, remissione, novazione. (14) **Improcedibilità per mancata
mediazione dell'opposto** (Modulo 8), da monitorare per tutta la causa.

---

## MODULO 11 — Termini e check-list dei primi sette giorni

### Tabella dei termini — calcolo sempre con `civilista-scadenze`

| Adempimento | Termine | Norma | Note |
|---|---|---|---|
| Notifica del decreto | **60 giorni** dalla pronuncia (90 all'estero) | art. 644 | A pena di inefficacia; domanda riproponibile |
| Opposizione | **40 giorni** dalla notificazione | artt. 641, 645 | 10/60 per giusti motivi; 50 UE; 60 altri Stati |
| Costituzione dell'opponente | termine dell'art. 165 | art. 645 | La mancata costituzione apre l'art. 647 |
| Esecutorietà per mancata opposizione | su istanza, anche verbale | art. 647 | Non è automatica |
| Istanza ex art. 648 | prima udienza, o **prima** con urgenza specifica | art. 648 co. 1 e 4 | Ordinanza non impugnabile |
| Istanza ex art. 649 | con l'atto di opposizione o separatamente | art. 649 | Ordinanza non impugnabile |
| Domanda di mediazione in opposizione | termine assegnato dal giudice dopo le istanze | art. 5-bis D.Lgs. 28/2010 | Onere del creditore opposto |
| Durata della mediazione | 6 mesi prorogabili | art. 6 D.Lgs. 28/2010 | Nessuna sospensione feriale |
| Opposizione tardiva | **10 giorni** dal primo atto di esecuzione | art. 650 | Presupposti stretti |
| Termine dilatorio dopo il precetto | 10 giorni | art. 482 | Salvo autorizzazione ex art. 642 co. 3 |
| Efficacia del precetto | 90 giorni dalla notificazione | art. 481 | |

**Sospensione feriale (1-31 agosto):** si applica al termine di opposizione; sul termine dell'art. 644 la prassi non è pacifica, contare nel modo più sfavorevole.

### Check-list dei primi sette giorni dal ricevimento di un decreto ingiuntivo

**Giorno 1 — le tre date.** (1) Acquisire l'**originale notificato con relata e busta**, fotografare e numerare tutto. (2) Annotare **data di notifica**, **data di
pronuncia/deposito** e **termine scritto nel decreto**: prima di ogni altra cosa. (3) Verificare se il decreto è **provvisoriamente esecutivo ex art. 642** e su
quale comma: con la provvisoria esecuzione il cliente può essere pignorato durante l'opposizione. (4) Calcolare il termine con `civilista-scadenze` e iscriverlo in
[[SCADENZIARIO]] con due alert, a metà termine e a sette giorni dalla scadenza.

**Giorno 2 — i controlli che possono chiudere la partita subito.** (5) **Notifica regolare?** Indirizzo, PEC, sede da registri, compiuta giacenza: se è irregolare si
apre l'art. 650 e cambia il *dies a quo*. (6) **Art. 644**: la notifica è avvenuta entro 60 giorni dalla pronuncia? (7) **Competenza**, e in particolare: il cliente
è **consumatore**? (8) **Prescrizione**: scadenza e atti interruttivi.

**Giorno 3 — i documenti.** (9) Richiedere al cliente, in un'unica lista: contratto e ordini, DDT e verbali, fatture e note di credito, **contabili di pagamento**,
corrispondenza e contestazioni scritte, estratti conto. (10) Individuare i **fatti costitutivi** che l'opposto dovrà provare e i **documenti mancanti** al suo
fascicolo: è lì che si costruisce l'opposizione.

**Giorno 4 — la decisione, per iscritto.** (11) **Opporsi o no?** Se il credito è dovuto e la difesa pretestuosa, l'opposizione aggiunge spese e interessi: valutare
**piano di rientro o saldo e stralcio** prima della scadenza, con `civilista-quantificazione` per il conto reale. (12) Se si oppone: **rito ordinario o
semplificato** (Modulo 6) e **quali motivi** (Modulo 10). (13) **Parere scritto al cliente** con costi, tempi, rischio spese e alternative.

**Giorno 5 — le istanze.** (14) Impostare l'**istanza ex art. 649** se il decreto è esecutivo: gravi motivi = fumus + periculum, entrambi documentati; se il precetto
è già arrivato, valutare l'urgenza. (15) Impostare la difesa **contro l'art. 648**: ancoraggio a prova scritta o a questione di pronta soluzione, e contestazione
**voce per voce**.

**Giorni 6 e 7 — redazione e controllo.** (16) Bozza con **`civilista-atti`, modulo 5**, con eccezioni in senso stretto e riconvenzionali **tutte dentro**. (17)
Indice dei documenti, nota di iscrizione a ruolo, contributo unificato. (18) **`civilista-verifica`** prima del deposito. (19) Programmare la notifica con **almeno
cinque giorni** di margine: il malfunzionamento dei sistemi non sospende i termini. (20) Mettere già in scadenziario udienza, **termine per la mediazione
dell'opposto** (Modulo 8) e termini delle memorie integrative.

---

## MODULO 12 — Errori ricorrenti

1. **Trattare invece di opporre.** La domanda di mediazione non interrompe né sospende i quaranta giorni: è l'errore più costoso della materia e produce un titolo
   definitivo contro il cliente.
2. **Non notificare il decreto entro 60 giorni** dalla pronuncia (art. 644): decreto inefficace, ricorso da rifare, contributo da ripagare, credito più vecchio.
3. **Dimenticare la mediazione nell'opposizione.** L'onere è del **creditore opposto**: la sua inerzia porta all'improcedibilità e alla **revoca del decreto già
   ottenuto**.
4. **Contestare l'intero importo in blocco.** La provvisoria esecuzione è concessa comunque per le somme non specificamente contestate (648 co. 2).
5. **Fermarsi al vizio della prova monitoria.** Nell'opposizione l'opposto integra la prova con i mezzi ordinari: se non si attacca il rapporto sottostante, il
   decreto regge.
6. **Ingiunzione contro un consumatore davanti al foro del creditore**: foro esclusivo inderogabile, rilevabile d'ufficio.
7. **Non chiedere l'esecutorietà ex art. 647**, o non vedere che l'opponente ha notificato l'opposizione ma **non si è costituito**.
8. **Riservare le eccezioni "per le memorie".** Prescrizione, compensazione, incompetenza derogabile e riconvenzionali si spendono **nell'atto di opposizione**: dopo
   sono perse anche se fondate.
9. **Ottenere il titolo senza aver verificato la solvibilità**: la verifica va fatta prima del ricorso, non dopo il pignoramento negativo.

---

## Verifiche e stato dei dati

*Verifiche eseguite il 6 agosto 2026.*

- **Confermati** su banca dati aggiornata al 20 febbraio 2026 (riverificare su Normattiva prima del deposito): artt. 634, 636, 641, 642, 644, 647, 648, 649, 650, 653
  e 281-decies c.p.c.; **art. 648 co. 4** dal correttivo 2024; **opposizione con rito semplificato** tramite l'art. 281-decies co. 3.
- **Art. 645 co. 2**: rito ordinario, udienza non oltre trenta giorni dalla scadenza del termine minimo a comparire, **niente dimezzamento dei termini di
  comparizione**. Le fonti secondarie sono concordi ma non riportano il comma integrale: **da riverificare sul testo ufficiale**.
- **Art. 5-bis D.Lgs. 28/2010** (onere sul ricorrente, improcedibilità e revoca) e **art. 6** (durata **sei mesi** dopo la modifica del 2024): confermati. Prassi
  degli uffici non uniforme sul primo; molte fonti in rete riportano ancora tre mesi sul secondo.
- **Domanda di mediazione e termine di opposizione**: orientamento prevalente di merito nel senso che **non interrompe né sospende**; esiste un orientamento
  contrario più risalente. Massime → `civilista-giurisprudenza`.
- **Saggio legale 1,60% dal 1° gennaio 2026**: confermato, riverificare ogni gennaio. **Interessi ex D.Lgs. 231/2002**: tasso BCE 2,15% nel primo semestre 2026 e
  2,40% nel secondo, più otto punti (10,15% e 10,40%), oltre a € 40 forfettari — dato da tabella professionale, **da riverificare** sul comunicato ufficiale a
  gennaio e a luglio.
- **Da verificare:** art. 635 c.p.c.; via dell'art. 14 D.Lgs. 150/2011 per i compensi dell'avvocato; idoneità autonoma della fattura elettronica via Sistema di
  Interscambio; sospensione feriale sul termine dell'art. 644; *dies a quo* dell'opposizione tardiva senza atti di esecuzione; termini di iscrizione a ruolo delle
  forme di espropriazione.
- **Disallineamento interno da sanare:** `civilista-atti` (modulo 5) pone ancora l'onere della mediazione sulla **parte opponente**; l'art. 5-bis lo pone sul
  **ricorrente per decreto ingiuntivo**. Vale quanto scritto qui.

---

## Chiusura del lavoro

Ogni analisi si chiude con **le date** (notifica, scadenza, prossimo adempimento), **la decisione** con le sue alternative e **i documenti mancanti**. Aggiorna il
fascicolo in `FASCICOLI/<caso>/` con i wikilink e riporta ogni termine in [[SCADENZIARIO]] con `civilista-scadenze`: indici e collegamenti li mantieni tu. Per la
redazione passa a `civilista-atti`; prima del deposito proponi `civilista-verifica`. Italiano tecnico e asciutto, citazioni normative complete (articolo, comma,
codice), segnaposto tra parentesi quadre dove manca un dato. Nessun documento prodotto è depositabile così com'è: è una **bozza**, e la decisione resta del
difensore.
