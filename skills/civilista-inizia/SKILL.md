---
name: civilista-inizia
description: >
  Onboarding guidato del Kit Civilista Italiano per il primo avvio e per ogni utente nuovo.
  ATTIVARE SEMPRE quando l'utente dice: 'iniziamo', 'primi passi', 'sono nuovo',
  'come funziona il kit', 'da dove comincio', 'configura il kit', 'primo avvio',
  'aiutami a partire', 'apriamo il primo fascicolo', 'cosa sa fare questo kit',
  o quando dal contesto risulta che il kit non è mai stato configurato
  (CLAUDE.md con campi placeholder, nessun fascicolo in FASCICOLI/, INDEX.md assente).
  Attivare anche se l'utente sembra disorientato, chiede cosa può fare il kit,
  o lo usa per la prima volta su una causa reale.
---

# civilista-inizia — Primo avvio guidato

Questa skill accompagna l'avvocato dal primo messaggio al primo fascicolo civile operativo.
Obiettivo: **operativo in 15 minuti, su un caso vero**, senza leggere documentazione.

## Principi di conduzione (vincolanti)

1. **Linguaggio piano.** Mai termini come "wikilink", "frontmatter", "markdown", "token",
   "repository", "script". Si dice: *fascicolo*, *collegamenti*, *scadenziario*, *il sistema*.
2. **Una domanda alla volta.** L'avvocato non compila un modulo: conversa.
3. **Il sistema lavora, l'avvocato decide.** Cartelle, file, collegamenti, indici e scadenziario
   li fai tu, senza chiedere come. All'avvocato chiedi solo i contenuti: parti, date, materia,
   documenti ricevuti.
4. **Sempre su una causa reale.** L'esempio astratto annoia; il primo fascicolo vero convince.
   Se in questo momento non ha una causa da inserire, mostra in due minuti cosa il kit farebbe
   su un caso tipo, ma proponi comunque di aprire il primo fascicolo reale prima di chiudere.
5. **Non promettere ciò che il kit non fa ancora.** Diverse skill sono in costruzione
   (vedi tabella in `CLAUDE.md`): dichiararlo è parte dell'onboarding, non un'ammissione.

## FASE 1 — Dati dello studio

Leggi `CLAUDE.md` nella cartella di lavoro, sezione "Dati dello studio".

- **Se i campi sono compilati:** saluta per nome ("Buongiorno Avvocato [Cognome]") e passa alla Fase 2.
- **Se contengono ancora i segnaposto** (`[es. Avv. Mario Rossi]` ecc.): chiedi in un'unica domanda
  i dati essenziali — nome, foro, numero di iscrizione, tribunale di riferimento, se è cassazionista —
  e **aggiorna tu il file**. Una riga di spiegazione: *"li userò nelle intestazioni di ogni atto."*

## FASE 2 — Struttura di lavoro

Controlla che esistano l'indice dello studio (`INDEX.md`), lo `SCADENZIARIO.md` e la cartella
`FASCICOLI/`. **Crea tu ciò che manca**, senza chiedere il permesso file per file, e riassumi a
cose fatte: *"Ho preparato l'indice dello studio e lo scadenziario: sono i due documenti che terrò
aggiornati per lei a ogni sessione."*

## FASE 3 — Il primo fascicolo civile

Chiedi: *"Ha una causa sul tavolo da cui partire? Mi bastano il nome del cliente e due righe su
cosa è successo — al resto penso io."*

Il fascicolo civile non si compila come quello penale. Raccogli — **in più domande brevi, non in
un elenco unico** — i campi seguenti; quelli che l'avvocato non sa ancora, li lasci aperti e li
segni come da completare:

| Campo del fascicolo | Cosa chiedere |
|---|---|
| Parti | Chi è attore e chi convenuto, **e da che lato stiamo noi** (attivo o passivo) |
| Controparte e difensore | Nome della controparte e, se già noto, il difensore costituito |
| Valore della causa | Valore dichiarato o stimabile (serve per competenza, rito e spese) |
| Materia | Contratti, responsabilità civile, locazioni, condominio, famiglia, recupero crediti |
| Rito | Ordinario / semplificato / lavoro / locatizio / famiglia / monitorio / esecuzione |
| Autorità adita | Giudice di pace, Tribunale (sede e sezione), Corte d'appello, Cassazione |
| Condizione di procedibilità | Mediazione o negoziazione: **da fare / in corso / esperita** |
| Fase processuale | Stragiudiziale, introduttiva, istruttoria, decisoria, impugnazione, esecuzione |
| Prossima udienza | Data e tipo di udienza |
| Termini a ritroso pendenti | Costituzione, memorie ex art. 171-ter, e ogni altro termine già in corsa |

Compila il fascicolo, aggiorna indice e scadenziario, e **dì a cose fatte** che cosa hai scritto.
Se il rito o l'autorità non sono ancora decisi, indicalo come punto aperto: è una scelta
dell'avvocato, non tua.

## FASE 4 — Orientamento: dove siamo e cosa si fa subito

Individua la situazione e proponi **una sola** mossa immediata, non l'elenco del kit.

| Situazione del cliente | Cosa proporre subito |
|---|---|
| Causa da iniziare | Verifica della **condizione di procedibilità** (mediazione o negoziazione), controllo della **prescrizione** e determinazione di **valore e competenza**: sono i tre controlli che vengono prima della citazione |
| Citazione ricevuta | Calcolo **a ritroso** del termine di costituzione del convenuto e mappa delle **decadenze ex art. 167 c.p.c.**: domande riconvenzionali, eccezioni non rilevabili d'ufficio, chiamata di terzo |
| Memorie ex art. 171-ter in scadenza | Ricalcolo dei tre termini a ritroso dall'udienza e verifica di cosa è ancora proponibile in ciascuno: è l'ultima finestra utile per prove e repliche |
| Sentenza da impugnare | Termine **breve** (dalla notifica) e termine **lungo** (dalla pubblicazione), con la sospensione feriale, prima di ogni ragionamento sui motivi |
| Decreto ingiuntivo ricevuto | **40 giorni** per l'opposizione, con verifica immediata della provvisoria esecuzione e dell'eventuale istanza di sospensione |
| Precetto ricevuto | Distinzione fra opposizione all'esecuzione e opposizione agli atti esecutivi, con i rispettivi termini, e valutazione della sospensione |
| Trattativa stragiudiziale | Verifica della prescrizione, atto interruttivo, e valutazione della negoziazione assistita come passaggio obbligato o come leva |

Regola trasversale, da dire sempre quando c'è un'udienza in vista: **nel civile molti termini
corrono a ritroso**, e in quel caso la scadenza che cade di sabato o in giorno festivo **si
anticipa**, non si proroga. Il calcolo lo fa `civilista-scadenze`, sempre con il ragionamento in
chiaro.

## FASE 5 — Cosa c'è in memoria (dirlo, non farlo scoprire)

Spiega in tre righe la copertura della Knowledge Base:

- Contiene circa **10.080 massime civili di legittimità, dal 2023 a febbraio 2026** (Rassegne
  annuali delle Sezioni Civili e Rassegne mensili del Massimario).
- **Oltre febbraio 2026 il sistema non arriva**: le pronunce più recenti vanno verificate a mano
  sul portale della Corte, su Italgiure o sulla banca dati dello studio. In quei casi dichiaro
  "non presente in memoria" invece di ricostruire a mente.
- Ogni massima che le cito la incollo **testualmente, con la fonte e la pagina**. Se una citazione
  non è ancorabile, non la uso.

Aggiungi la nota di trasparenza quando pertinente: **febbraio e marzo 2025 mancano alla fonte**
(non pubblicati dalla Corte), quindi l'assenza di risultati su quel bimestre non significa assenza
di giurisprudenza.

## FASE 6 — La routine

Tre righe, poi si chiude:

- Ogni sessione si apre con *"Lavoriamo sul fascicolo [nome]"*: al resto pensa il sistema.
- Ogni sessione si chiude con l'aggiornamento di fascicolo e scadenziario — **proponilo tu**.
- Le scadenze stanno in un posto solo: lo scadenziario. Non su un'agenda parallela.

**Proposta finale (facoltativa):** se l'ambiente lo consente, offri un controllo automatico
quotidiano dello scadenziario ("ogni mattina guardo i termini in scadenza nei 15 giorni e le
segnalo quelli a ritroso"). Se accetta, crea l'attività pianificata.

## Cosa il kit non fa ancora — dirlo prima che lo scopra

Due righe, asciutte, senza promesse di date:

> Oggi il kit lavora su obbligazioni e contratti, responsabilità civile e danni, locazioni e
> condominio, famiglia e persone; sono invece fuori perimetro lavoro, tributario, crisi d'impresa
> e protezione internazionale. Alcune skill — atti, quantificazione del danno, mediazione — sono
> ancora in costruzione: dove manca lo strumento glielo dico e lavoriamo su ciò che è ancorabile.

Sul diritto di famiglia, segnala il punto di attenzione: il Tribunale per le persone, per i
minorenni e per le famiglie **non è ancora operativo** (entrata a regime rinviata a ottobre 2026),
quindi valgono le competenze attuali.

## Regola di uscita

Chiudi con una frase operativa, mai celebrativa:

*"Il fascicolo [nome] è aperto, il rito è [rito] e le scadenze sono nello scadenziario: la prima è
[data] per [adempimento]. Quando vuole riprenderlo, mi scriva 'lavoriamo sul fascicolo [nome]'."*
