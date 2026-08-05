---
name: civilista-verifica
description: >
  Controllo qualità pre-deposito di un atto civile. ATTIVARE SEMPRE quando l'avvocato dice:
  'verifica l'atto', 'controlla prima del deposito', 'è pronto per il deposito?',
  'ricontrolla le citazioni', 'verifica i termini', 'controllo finale', 'check finale',
  'revisiona la comparsa', 'rileggi la citazione', 'controlla le conclusioni',
  'siamo in decadenza?', 'ho dimenticato qualcosa prima di depositare',
  o quando un atto destinato al deposito (citazione, comparsa di risposta, memorie ex art. 171-ter,
  ricorso, opposizione a decreto ingiuntivo, atto di appello, ricorso per cassazione)
  sta per essere consegnato. Attivare anche d'ufficio: proporre la verifica al termine
  della redazione di qualsiasi atto destinato al deposito.
---

# civilista-verifica — Verifica pre-deposito

Controllo qualità dello studio: un riesame **indipendente e sistematico** dell'atto prima che esca.
Principio: *l'atto regge solo se ogni affermazione, ogni termine e ogni domanda superano la
verifica*. Nel civile la verifica ha un bersaglio in più rispetto al penale: **le preclusioni**.
Un'eccezione fondata ma tardiva è un'eccezione persa, e il momento per accorgersene è adesso.

## Quando attivarla

- Su richiesta esplicita dell'avvocato.
- **D'ufficio**, al termine della redazione di ogni atto destinato al deposito:
  *"Vuole che esegua la verifica pre-deposito? Controllo citazioni, termini a ritroso, decadenze,
  procedibilità e conclusioni."*

## Metodo: verifica indipendente

Se l'ambiente consente di lanciare un agente di verifica separato (subagente), **usarlo**:
il verificatore non deve essere influenzato dal contesto di chi ha scritto l'atto. Istruirlo a
leggere SOLO l'atto, il fascicolo, lo scadenziario e la Knowledge Base — non la conversazione di
redazione. Se il subagente non è disponibile, eseguire la checklist direttamente **dichiarandolo**
nel report.

La checklist si esegue **tutta e nell'ordine**. Nessun punto si salta perché "sembra a posto":
si esegue e si scrive l'esito.

## CHECKLIST DI VERIFICA

### 1. Citazioni giurisprudenziali — la verifica più importante

Per OGNI pronuncia citata nell'atto:

| Esito | Criterio | Azione |
|---|---|---|
| ✅ VERIFICATA | Presente nel registro citazionale della KB (`KNOWLEDGE_BASE/_INDICE/INDICE.md` o `FASCICOLI/<caso>/_INDICE/`) **con riscontro testuale della massima** alla pagina indicata | Nessuna |
| ⚠️ NON IN KB | Non presente nei registri (o successiva a febbraio 2026, limite di copertura) | Rendere la citazione testuale dall'indice, oppure dichiararla "non presente in KB"; verifica su Italgiure / portale della Corte / banca dati dello studio |
| ❌ SOSPETTA | Estremi incoerenti (sezione, anno, numero, Rv non plausibili) o massima che non corrisponde alla fonte | Segnalare: NON depositare senza verifica umana |

**Mai declassare una citazione a "verificata" per somiglianza.** La verifica richiede il riscontro
**testuale** della massima, non la sola corrispondenza degli estremi. Verificare anche che la
massima citata dica davvero ciò che l'atto le fa dire, e che sia pertinente alla domanda svolta:
una massima esatta ma fuori tema è un errore di merito.

Controllare infine la **gerarchia**: se sul punto esistono Sezioni Unite in senso contrario,
l'atto deve farci i conti.

### 2. Termini e date — ricalcolo da zero

- **Ricalcolare da zero** ogni termine menzionato nell'atto con `civilista-scadenze`: non fidarsi
  del calcolo fatto in redazione.
- **Attenzione ai termini a ritroso** (costituzione ex artt. 166 e 171-ter, comparizione ex art.
  163-bis): se la scadenza cade di sabato o in giorno festivo, il termine **si anticipa** al giorno
  precedente non festivo. La proroga in avanti (art. 155 co. 4-5 c.p.c.) vale solo per i termini
  che corrono in avanti. È l'errore più frequente e il più costoso.
- Sospensione feriale: applicata o esclusa correttamente secondo la materia.
- Confronto con lo SCADENZIARIO del fascicolo: coincidono? Se no, la divergenza è un errore in uno
  dei due posti e va risolta prima del deposito.
- Coerenza interna delle date citate nell'atto: notifica, decorrenza, udienza, deposito.

### 3. Decadenze e preclusioni

Domanda guida: **l'atto contiene qualcosa che doveva essere proposto prima?**

- Domande nuove, riconvenzionali, eccezioni non rilevabili d'ufficio, chiamata di terzo: erano
  soggette al termine di costituzione del convenuto (art. 167 c.p.c.)? Sono nei tempi?
- Mezzi di prova e produzioni documentali: rispettano la scansione delle memorie ex art. 171-ter
  (precisazione delle domande, prove costituende e documenti, prova contraria)?
- In appello: divieto di domande ed eccezioni nuove (art. 345 c.p.c.) e limiti alle prove nuove.
- Se una richiesta è **tardiva**, dirlo con chiarezza e indicare l'alternativa (rilevabilità
  d'ufficio, richiesta di rimessione in termini, rinuncia consapevole).

### 4. Condizione di procedibilità

- La materia rientra nella **mediazione obbligatoria** (art. 5 D.Lgs. 28/2010) o nella
  **negoziazione assistita** (art. 3 D.L. 132/2014: risarcimento da circolazione e pagamenti fino
  a € 50.000)?
- Se sì: il tentativo è stato **esperito** prima del deposito, e l'atto lo **allega e lo documenta**
  (verbale di mancato accordo o mancata partecipazione, invito rifiutato o non riscontrato)?
- Il documento è nell'indice del fascicolo di parte ed è richiamato nell'atto?
- Nell'opposizione a decreto ingiuntivo: verificare su chi grava l'onere di attivare la procedura
  e con quali conseguenze in caso di inerzia.

### 5. Coerenza di parti, valore, rito e autorità

- Parti indicate correttamente e per esteso: denominazione, codice fiscale o partita IVA, sede o
  residenza, legale rappresentante; nostro cliente dal lato giusto (attore/convenuto,
  appellante/appellato, opponente/opposto).
- Difensore di controparte e domicilio digitale, dove rilevanti per la notifica.
- **Valore della causa**: dichiarato, coerente con le domande svolte, e coerente con competenza,
  rito e contributo unificato.
- **Rito**: quello indicato è quello effettivamente seguito nella struttura dell'atto (ordinario,
  semplificato, lavoro, locatizio, famiglia, monitorio, esecuzione)?
- **Autorità adita**: corretta per competenza per materia, valore e territorio; sezione indicata.

### 6. Conclusioni

- Sono **numerate** e distinte fra loro.
- Ogni conclusione corrisponde a una domanda effettivamente svolta e argomentata nel corpo
  dell'atto; e ogni domanda argomentata trova la sua conclusione (nessuna domanda "persa per strada").
- Domande subordinate e in via istruttoria collocate e qualificate correttamente.
- **Domanda di spese** presente, con distrazione ex art. 93 c.p.c. se richiesta, e coerente con il
  valore dichiarato e con i parametri forensi applicabili.
- Richieste accessorie (interessi, rivalutazione, provvisoria esecuzione) presenti se dovute.

### 7. Allegazione e onere della prova (art. 2697 c.c.)

- Per ciascun **fatto costitutivo** allegato: è indicata la prova che lo sorregge (documento,
  capitolo di prova orale, richiesta di CTU, presunzione)?
- Per i fatti impeditivi, modificativi ed estintivi: l'onere è correttamente collocato in capo a
  chi li invoca?
- Nessun salto fra **fatto allegato** e **fatto provato**: l'atto non deve affermare come provato
  ciò che è solo dedotto.
- Capitoli di prova: specifici, circostanziati, non valutativi, con testi indicati e generalità.

### 8. Documenti e fascicolo di parte

- L'indice del fascicolo di parte esiste ed è **numerato progressivamente**.
- Ogni documento richiamato nell'atto (doc. n. X) esiste nell'indice, con la stessa numerazione.
- Nessun documento presente in indice ma mai richiamato, e nessun richiamo a documento assente.
- Documenti già prodotti in altra fase o nel monitorio: indicati come tali.

### 9. Dati personali — minimizzazione

- L'atto contiene dati **eccedenti** rispetto a quanto necessario a sostenere le domande?
  In particolare: dati sulla salute, dati di terzi estranei, dati di minori, dati economici non
  pertinenti.
- Se un dato particolare è necessario, è **strettamente funzionale** alla domanda e non replicato
  senza ragione in più punti.
- Valutare l'oscuramento delle generalità nei documenti allegati che ritraggono terzi.

### 10. Requisiti formali delle impugnazioni

**Appello (art. 342 c.p.c.):** per ciascun motivo devono risultare (a) il **capo della sentenza
impugnato**, indicato in modo puntuale; (b) le **censure alla ricostruzione dei fatti** operata dal
primo giudice; (c) le **violazioni di legge** dedotte e la loro rilevanza sulla decisione.
Verificare che nessun motivo si risolva in una generica riproposizione delle difese di primo grado
e che le domande non accolte siano state **espressamente riproposte** (art. 346 c.p.c.).

**Cassazione (art. 366 c.p.c.):** esposizione sommaria dei fatti di causa; motivi con l'indicazione
delle norme e del vizio dedotto ai sensi dell'art. 360; **specifica indicazione degli atti e dei
documenti** su cui il motivo si fonda e della loro collocazione nel fascicolo (autosufficienza);
indicazione del provvedimento impugnato e della procura. Verificare inoltre la sottoscrizione del
difensore cassazionista.

Per gli atti di primo grado, controllare in ogni caso: intestazione con i dati dello studio
(da `CLAUDE.md`), procura richiamata, sottoscrizione, dichiarazione di valore, indicazione del
domicilio digitale.

## FORMATO DEL REPORT

```
# VERIFICA PRE-DEPOSITO — [tipo di atto] — [fascicolo] — [data]

## Esito complessivo: 🟢 PRONTO / 🟡 DEPOSITABILE CON RISERVE / 🔴 NON DEPOSITARE

## Tabella per esito
| # | Controllo | Esito | Nota |
|---|---|---|---|
| 1 | Citazioni giurisprudenziali | ✅ n / ⚠️ n / ❌ n | ... |
| 2 | Termini e date (ricalcolo) | ✅ / ⚠️ / ❌ | ... |
| 3 | Decadenze e preclusioni | ✅ / ⚠️ / ❌ | ... |
| 4 | Condizione di procedibilità | ✅ / ⚠️ / ❌ | ... |
| 5 | Parti, valore, rito, autorità | ✅ / ⚠️ / ❌ | ... |
| 6 | Conclusioni e domanda di spese | ✅ / ⚠️ / ❌ | ... |
| 7 | Allegazione e onere della prova | ✅ / ⚠️ / ❌ | ... |
| 8 | Documenti e indice di parte | ✅ / ⚠️ / ❌ | ... |
| 9 | Dati personali | ✅ / ⚠️ / ❌ | ... |
| 10 | Requisiti formali / impugnazione | ✅ / ⚠️ / ❌ | ... |

## Dettaglio citazioni
[elenco per esito, con la massima testuale e (fonte, p. N) per le verificate]

## Correzioni da fare prima del deposito
1. [azione concreta, in ordine di gravità, con il punto della checklist da cui deriva]
```

Salvare il report nel fascicolo come `verifica-[atto]-[data].md` e collegarlo al fascicolo.

## Regole finali

- **Un solo ❌ blocca il deposito.** L'esito complessivo non può essere 🟢 se anche un solo
  controllo è ❌, qualunque sia il numero dei ✅.
- Un ❌ su decadenze o su condizione di procedibilità va segnalato **per primo**: sono i vizi che
  non si sanano dopo.
- **L'esito 🟢 non sostituisce la revisione del difensore.** Ogni atto resta una bozza fino alla
  revisione personale dell'avvocato.
- La verifica è un fatto di metodo, non di sfiducia: proporla sempre, anche per gli atti semplici.
