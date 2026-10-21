# Come si lavora col kit — il metodo

*Installare il kit richiede dieci minuti. Usarlo bene richiede di aver capito tre cose, e sono queste.*

L'installazione è un'altra guida: [`INSTALLAZIONE.md`](INSTALLAZIONE.md). Questa comincia dove quella finisce — dal secondo giorno in poi.

---

## 1. Tre posti che sembrano uno

È l'equivoco da cui nascono quasi tutti i problemi dei primi giorni. L'interfaccia mette vicine tre cose che si assomigliano e si comportano in modo opposto.

| | Che cos'è | Quanto dura |
|---|---|---|
| **La conversazione** | Quello che trascini dentro una chat | Vive lì e muore lì: la conversazione dopo non ne sa nulla |
| **La cartella di lavoro** | `Civile-Italia`, quella che hai scaricato e **collegato** | È il disco dello studio: quello che finisce qui resta |
| **Il Progetto** | Un contenitore di istruzioni e appunti condivisi fra conversazioni | Permanente, ma **non è lì che vivono i fascicoli** |

L'incidente tipico è questo: si trascina la cartella di un fascicolo *dentro la chat* invece di lavorare nella cartella collegata. Il lavoro viene fatto, ma finisce in un posto che alla conversazione successiva non esiste più — e lo si rifà da capo.

Il consiglio che circola — *«devi creare un progetto»* — coglie la cosa giusta, cioè smettere di lavorare in chat sciolta. La parola però porta fuori strada, perché «Progetto» designa il terzo meccanismo mentre quello che serve è il secondo: la **cartella di lavoro collegata**.

---

## 2. Dove va cosa

Una regola sola: **tutto il lavoro vive dentro `Civile-Italia`**. Niente sul desktop, niente in Download, niente trascinato in chat se non per una domanda usa e getta.

```
Civile-Italia/
├── CLAUDE.md                  ← i dati dello studio: nome, foro, tribunale
├── INDEX.md                   ← l'indice dello studio, lo tiene aggiornato il kit
├── SCADENZIARIO.md            ← tutte le scadenze, in un posto solo
├── FASCICOLI/
│   ├── ROSSI_c_BANCA_XY/      ← un fascicolo = una cartella
│   │   ├── FASCICOLO.md       ← la scheda: parti, rito, valore, fase
│   │   ├── atti/              ← atti e documenti della causa
│   │   └── bozze/             ← quello che producete insieme
│   └── CONDOMINIO_VIA_ROMA/
├── MODELLI/                   ← i tuoi atti già depositati (§ 5)
└── KNOWLEDGE_BASE/            ← la giurisprudenza: si aggiorna da sola ogni lunedì
```

Le cartelle dei fascicoli **non le crei tu**: basta dire che fascicolo si apre e le prepara il kit, con la scheda e le scadenze già dentro.

> **Quando arrivano le carte di una causa**, copiale nel Finder dentro `FASCICOLI/<caso>/atti/` e *poi* aprine la conversazione. Trascinarle nella chat significa perderle alla sessione successiva.

La separazione sembra pedanteria con un fascicolo solo. Con dieci è l'unica difesa contro la risposta giusta sul fascicolo sbagliato.

**I dati dei clienti restano sul tuo computer.** `FASCICOLI/`, `MODELLI/` e la scheda di stile sono esclusi dal versionamento: non finiscono su GitHub nemmeno se aggiorni il kit.

---

## 3. Aprire e chiudere una sessione

**Una conversazione per fascicolo.** Non riusare la stessa chat per cause diverse: il contesto si sporca e le risposte si mescolano. Quando una conversazione si allunga troppo, chiudila e aprine una nuova sullo stesso fascicolo — la memoria sta nella cartella, non nella chat, quindi non si perde niente.

**La prima volta in assoluto**, una volta sola:

```
/civilista-italia:civilista-inizia
```

Configura lo studio — nome, foro, tribunale — e apre il primo fascicolo.

> ⚠️ **È la procedura di primo avvio, non un rituale di apertura.** Rilanciarla a ogni sessione ripropone le domande di configurazione e riparte da capo. Capita di sentirselo consigliare: non va fatto.

**Tutte le volte dopo:**

```
Lavoriamo sul fascicolo Rossi contro Banca XY
```

Rilegge la scheda, le scadenze e il lavoro dell'ultima volta, e riparte da lì.

**Prima di chiudere:**

```
Aggiorna il fascicolo e lo scadenziario
```

Dovrebbe proporlo da solo. È il momento in cui il lavoro passa dalla conversazione al disco: saltarlo significa ritrovarsi la settimana dopo senza traccia di quello che si era deciso.

---

## 4. Come si verifica che il kit sia stato davvero usato

Un punto da sapere subito: **alla domanda «stai usando il kit?» l'assistente risponde di sì anche quando non è vero.** Non è malafede — non dispone di un modo affidabile di osservare il proprio lavoro. La domanda è quindi inutile, e va sostituita.

**Prima mossa: imporlo invece di sperarlo.** Apri la richiesta con il comando esplicito. Con la barra `/` compare l'elenco; scrivendo `civ` si filtra.

| Se devi | Apri con |
|---|---|
| Capire se conviene agire o resistere | `/civilista-italia:civilista-caso` |
| Calcolare un termine | `/civilista-italia:civilista-scadenze` |
| Scrivere un atto | `/civilista-italia:civilista-atti` |
| Decreto ingiuntivo, da una parte o dall'altra | `/civilista-italia:civilista-monitorio` |
| Cercare giurisprudenza | `/civilista-italia:civilista-giurisprudenza` |
| Rileggere prima del deposito | `/civilista-italia:civilista-verifica` |

**Seconda mossa: riconoscere le impronte.** Una risposta che viene davvero dal kit ne ha tre, e sono difficili da falsificare.

- **Le massime hanno numero Rv, fonte e pagina**, e il testo è incollato, non riassunto. «Cassazione 2024» senza numero e senza pagina significa che la banca dati non è stata aperta.
- **I termini sono calcolati a vista**, con la sospensione feriale e la direzione dichiarata. Una data secca senza il conto non è passata dal calcolo.
- **Lo scadenziario e il fascicolo risultano modificati sul disco.** È la prova più dura: se la cartella non è cambiata, il lavoro è rimasto nella chat.

**Se hai altri strumenti installati** può prendere la strada sbagliata. Due accorgimenti: apri sempre col comando `/civilista-italia:…`, che non lascia margine; e quando vuoi l'altro, dillo esplicitamente. Se ti risponde di aver usato qualcos'altro, non discutere: rilancia con il comando davanti.

---

## 5. Lo stile dello studio

Il kit **non ricava da solo uno stile** osservando i fascicoli: non esiste un apprendimento automatico della scrittura. Lavora però su ciò che gli si indica, e la documentazione dello studio è lo strumento per farlo.

**Come si imposta.** Nella cartella `MODELLI/` metti da tre a cinque atti **già depositati**, di tipo diverso: una citazione, una comparsa di risposta, una memoria. La selezione conta più della quantità. Se l'impostazione cambia per materia, usa sottocartelle — `MODELLI/monitorio/`, `MODELLI/lavoro/`.

**Come si usa.** Prima di redigere, il kit cerca da solo un modello pertinente e ne segue l'impostazione — struttura, ordine dell'esposizione, registro, formule — e **dichiara su quale si è basato**, come fa con le massime. Dai modelli prende la forma, mai i fatti: niente importi, nomi o argomenti di merito trasportati da una causa all'altra.

**La scheda di stile.** Quando i modelli sono almeno tre, si può chiedere:

```
Ricava il mio stile dai modelli
```

Il kit li legge una volta sola e ne scrive `STILE_STUDIO.md`: come si intesta l'atto, in che ordine vanno le parti, come si introducono le norme, come si graduano le conclusioni, quali formule ricorrono, quali termini si evitano. Da lì in poi legge quella scheda invece degli atti interi.

Tre vantaggi: è **correggibile** — si apre e si scrive *«no, le conclusioni le metto prima dei fatti»*, e la correzione resta; è **economica**, una pagina invece di cinque atti a ogni stesura; ed è **verificabile**, perché lo stile smette di essere un'impressione e diventa un documento che si può leggere e discutere.

La scheda registra **come** si scrive, mai **che cosa** si è scritto: nessun nome di parte, nessun numero di causa, nessun importo. È il file che più facilmente verrà condiviso fra colleghi dello stesso studio, e deve poter circolare.

---

## 6. Gli errori ricorrenti

| Cosa si vede | Perché | Cosa fare |
|---|---|---|
| Ha lavorato sul fascicolo ma il file non si trova | La cartella era allegata alla conversazione, non collegata: fuori da `Civile-Italia` non ha un posto dove scrivere | Sposta tutto in `FASCICOLI/` e ricollega la cartella |
| Stessa conversazione, risposte che si confondono | Una sola chat con dentro due fascicoli | Una conversazione per fascicolo; quando si allunga, aprine una nuova |
| Dice di aver usato il kit ma non sembra | Non ha un modo affidabile di verificarlo da sé | Controlla le impronte (§ 4) e rilancia col comando esplicito |
| Il kit compare «bloccato» nel pannello | Difetto noto dell'app: il catalogo si pianta in silenzio | Procedura di sblocco in [`INSTALLAZIONE.md`](INSTALLAZIONE.md). **Non cancellare la cartella di lavoro** |
| Le bozze non somigliano ai tuoi atti | Mancano i modelli, o non sono stati indicati | Popola `MODELLI/` e chiedi la scheda di stile (§ 5) |

---

## 7. Il promemoria

| Momento | Cosa fare |
|---|---|
| Arrivano le carte | Copiale nel Finder in `FASCICOLI/<caso>/atti/`. Mai trascinarle in chat |
| Apro una sessione | Conversazione nuova, cartella `Civile-Italia` collegata, «lavoriamo sul fascicolo X» |
| Chiedo una cosa seria | Apro con `/civilista-italia:…`, non a voce libera |
| Devo scrivere un atto | Il kit usa i modelli da solo; se non li ha, glieli indico |
| Ricevo una risposta | Controllo le impronte: Rv e pagina, conto dei termini, scadenziario aggiornato |
| Chiudo | «Aggiorna il fascicolo e lo scadenziario» |
| Cambio causa | Conversazione nuova. Sempre |

---

**Se qualcosa non torna**, [apri una segnalazione](https://github.com/Synthos-Logic/civilista-italia/issues). Il kit gemello per il penale è arrivato dov'è perché chi lo usava su casi veri ha indicato dove sbagliava: una segnalazione precisa vale più di un complimento.
