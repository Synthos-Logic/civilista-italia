---
name: civilista-giurisprudenza
description: >
  Ricerca e organizzazione della giurisprudenza civile italiana, ancorata alla Knowledge Base del
  kit (Rassegne del Massimario, Sezioni Civili). ATTIVARE SEMPRE quando l'avvocato dice: 'cerca
  giurisprudenza su', 'cosa dice la Cassazione civile su', 'ci sono massime su', 'trova precedenti
  su', 'orientamento della Cassazione in tema di', 'esiste un contrasto tra sezioni su', 'le
  Sezioni Unite si sono pronunciate su', 'c'è un rinvio pregiudiziale ex 363-bis su', 'cerca la
  massima Rv', 'quale sezione decide di', 'cosa dice la CGUE su clausole abusive', 'la Corte
  costituzionale si è pronunciata su', 'ultime massime in tema di'. Attivare anche per costruire
  la sezione giurisprudenziale di un atto, verificare se un principio è consolidato o superato, e
  controllare la copertura della KB prima di affermare che non risulta giurisprudenza.
---

# civilista-giurisprudenza — Ricerca giurisprudenziale civile ancorata

Nel civile la giurisprudenza non decora l'atto: lo regge. Il giudice civile ragiona per orientamenti
consolidati, e una massima citata male — o inventata — costa più di una massima assente.
Questa skill fa una cosa sola e la fa bene: **trova nella KB ciò che c'è davvero, lo cita con
la sua pagina, e dichiara con chiarezza ciò che non c'è.**

Vincolo assoluto: vale il **PROTOCOLLO quote-then-claim**
(`KNOWLEDGE_BASE/00_META/PROTOCOLLO_GROUNDING.md`). Si afferma solo ciò che si è letto.

---

## Prima di iniziare

Se la richiesta non è già precisa, chiedi **in un'unica domanda**:

- **La questione giuridica specifica** — non "responsabilità medica" ma "onere della prova del nesso
  causale nella responsabilità sanitaria contrattuale"
- **Da che lato stiamo** (attore/convenuto): quale orientamento ci giova e quale ci verrà opposto
- **A cosa serve la ricerca** (fondare una domanda / resistere a un'eccezione / verificare se un
  principio è consolidato / preparare un motivo di ricorso per Cassazione)
- **Il periodo rilevante**, se la questione è recente o normativamente mossa

---

## MODULO 0 — COPERTURA DELLA KB (obbligatorio, prima di ogni ricerca)

**Non si cerca senza aver detto all'avvocato fin dove arriva la KB.** Questo modulo non è
opzionale e non si salta neanche quando la ricerca sembra facile.

La Knowledge Base civile contiene **10.080 massime**, su due binari:

| Binario | Contenuto | Copertura | Numero Rv |
|---|---|---|---|
| **Rassegne annuali — Gli orientamenti delle Sezioni Civili** | Orientamento assestato e organizzato per materia, 3 volumi per anno | **2023 e 2024** | Sì |
| **Rassegne mensili della giurisprudenza civile** | Massime del mese, per sezione, con classificazione per materia | **gennaio 2025 → febbraio 2026** | Sì |

Buchi e limiti da dichiarare, sempre, senza aspettare che l'avvocato li scopra:

1. **Febbraio e marzo 2025 non esistono in KB perché non sono stati pubblicati dalla fonte.**
   Se la ricerca cade in quel bimestre, dillo esplicitamente: *l'assenza di risultati non è
   assenza di giurisprudenza*. Le mensili disponibili del 2025 sono: 01, 04-05 (fascicolo unico),
   06, 07-08 (fascicolo unico), 09, 10, 11, 12.
2. **Sopra febbraio 2026 la KB non arriva.** Qualsiasi pronuncia successiva è fuori copertura:
   si dichiara "non presente in KB" e si indica dove verificarla.
3. **La Rassegna annuale 2025 non esiste ancora** (esce con 12-18 mesi di ritardo). Per il 2025
   e il 2026 la KB ha solo le mensili: riportano la massima ufficiale ma non l'assestamento per
   materia tipico dell'annuale. Dirlo quando si presenta un orientamento recente come "consolidato":
   sulle mensili si può dire cosa ha deciso la Corte, non che l'indirizzo sia stabilizzato.
4. **La giurisprudenza di merito NON è in KB.** La Banca Dati di Merito del Ministero è
   consultabile solo dall'avvocato con SPID/CIE/CNS e non è automatizzabile. Quando serve la prassi
   del foro competente — e nel civile serve spesso — il kit lo dichiara e rimanda alla consultazione
   diretta dell'avvocato.

**Formula da usare quando la ricerca cade fuori copertura** (adattarla, non ometterla):

> Non presente in KB: la copertura arriva a febbraio 2026 [oppure: il bimestre febbraio-marzo 2025
> non è stato pubblicato dalla fonte]. Il principio va verificato prima del deposito sul portale
> della Corte di cassazione, su **Italgiure** (ricerca per Rv e per estremi) o su **DeJure**.
> Non ricostruisco a memoria numeri di sentenza.

Verifica rapida della copertura effettiva prima di rispondere:

```bash
cat KNOWLEDGE_BASE/_INDICE/REGISTRO_FONTI.md      # tutte e sole le fonti consultabili
head -5 KNOWLEDGE_BASE/_INDICE/INDICE.md          # data di generazione e numero di massime
```

Ciò che non compare nel REGISTRO_FONTI non è nella KB. Punto.

---

## MODULO 1 — COME SI CERCA

Due modi di entrare nella KB, a seconda che si parta dal **concetto** o dalla **sentenza**.

### A. Ricerca per concetto

**A1 — Indice strutturale (solo annuali).** In `INDICE.md`, sezione 1, le Rassegne annuali sono
mappate PARTE → CAPITOLO con la pagina di inizio: è la via più rapida per posizionarsi su una
materia. Esempi reali di voci presenti: `CAPITOLO VIII — COMUNIONE E CONDOMINIO`,
`CAPITOLO X — LE OBBLIGAZIONI IN GENERALE`, `CAPITOLO XI — IL CONTRATTO IN GENERALE`,
`CAPITOLO XIV — LA RESPONSABILITÀ EXTRACONTRATTUALE`, `CAPITOLO XV — LE RESPONSABILITÀ PROFESSIONALI`.

*Rumore noto*: nei volumi annuali ogni voce compare spesso **due volte** a pagine consecutive
(voce del sommario + voce del corpo). Non è un errore di ancoraggio: si sceglie la pagina del corpo.
*Le Rassegne mensili hanno indice strutturale vuoto per costruzione* (non hanno PARTE/CAPITOLO):
per le mensili si usa il grep (A2) o il registro citazionale (B).

**A2 — grep sul `.md`.** Metodo principale. I file convertiti stanno tutti in `KNOWLEDGE_BASE/_INDICE/`:

```bash
# concetto su tutto lo stock consolidato (annuali 2023-2024)
grep -n -i "compensazione volontaria" KNOWLEDGE_BASE/_INDICE/202[34]_Massimario_Civile_Volume*.md

# stesso concetto sul flusso recente (mensili 2025-2026)
grep -n -i "clausol[ae] abusiv" KNOWLEDGE_BASE/_INDICE/2025_*.md KNOWLEDGE_BASE/_INDICE/2026_*.md

# ricerca per norma: le massime citano gli articoli testualmente
grep -n "art. 2051" KNOWLEDGE_BASE/_INDICE/2024_Massimario_Civile_VolumeIII.md
grep -n "Cod. Civ. art. 1218" KNOWLEDGE_BASE/_INDICE/2025_12_Rassegna_Mensile_Civile.md
```

Usa più formulazioni: la Corte scrive "danno da cose in custodia" dove l'avvocato dice "art. 2051".
Se il primo grep è muto, il problema quasi sempre è il lemma, non la KB.

**A3 — Classificazione per materia (mensili).** Nelle mensili ogni massima porta, sopra il testo,
un **codice numerico a sei cifre + la voce di materia** dello schema di classificazione del
Massimario, seguito dall'abstract analitico. Esempio reale (ottobre 2025, p. 4):

```
111017 NEGOZI GIURIDICI - FIDUCIARI Trust - Opponibilità nei confronti dei creditori - ...
```

Da qui si ricava:
- si cerca **per voce**: `grep -n "NEGOZI GIURIDICI" KNOWLEDGE_BASE/_INDICE/2025_*.md`
- si cerca **per codice**, per trovare tutte le massime della stessa materia in mesi diversi:
  `grep -rn "^111017" KNOWLEDGE_BASE/_INDICE/2025_*.md KNOWLEDGE_BASE/_INDICE/2026_*.md`
- le mensili sono ordinate **per sezione** (Sezioni Unite, Prima, Seconda, Terza, Lavoro,
  Tributaria, Questioni processuali e comuni alle sezioni, più eventuali rassegne tematiche):
  il sommario di p. 2 dà le pagine di inizio di ciascuna sezione. Serve a capire subito **chi**
  ha deciso, e quindi quanto pesa.

### B. Ricerca per sentenza (numero Rv)

Il **registro citazionale** è la sezione 2 di `INDICE.md`: una riga per ogni massima realmente
presente, con Rv, pagina e file.

```bash
grep -n "Rv 671693" KNOWLEDGE_BASE/_INDICE/INDICE.md
# → - `Rv 671693-01` (p.201) — Sez. 2, n. 13949/2024, Var- rone, Rv. 671693-01
#   nel blocco della fonte: 2024_Massimario_Civile_VolumeI.md

grep -n "Rv 676180" KNOWLEDGE_BASE/_INDICE/INDICE.md
# → - `Rv 676180-01` (p.4) — Sez. U, Ordinanza interlocutoria n. 26471 del 01/10/2025 (Rv. 676180-01
#   nel blocco della fonte: 2025_10_Rassegna_Mensile_Civile.md
```

Note operative:
- Il registro è **raggruppato per fonte**: il file si legge dall'intestazione `###` sopra la riga
  trovata (`grep -n "^### " INDICE.md` e confronto dei numeri di riga).
- Una massima può comparire a **più pagine** (`(p.15,p.172,p.199)`): la prima è la trattazione, le
  altre sono richiami trasversali. Si cita la pagina che si è letta.
- I sub-numeri contano: `Rv. 671693-01` e `Rv. 671693-02` sono due massime diverse della stessa
  sentenza, a pagine diverse (vol. I p. 201 e vol. III p. 242).
- **I richiami non sono citazioni.** I blocchi "*Massime precedenti Vedi: N. … del … Rv. …*" in coda
  alle massime mensili rimandano a pronunce che **non** stanno in quel documento: sono piste di
  ricerca, non fonti citabili. Se serve quel precedente, va cercato con il suo Rv nel registro; se
  non c'è, è fuori KB.

### C. Dalla massima alla pagina

Trovata la riga, si apre il `.md` al marcatore `<!-- pag. N -->` e si legge il testo.

```bash
# leggere l'intorno della pagina 201 del volume I 2024
grep -n "<!-- pag. 201 -->" KNOWLEDGE_BASE/_INDICE/2024_Massimario_Civile_VolumeI.md

# operazione inversa: da un numero di riga trovato col grep, risalire alla pagina
awk -v L=8890 'NR<=L && /^<!-- pag\./ {p=$0} NR==L {print p}' \
    KNOWLEDGE_BASE/_INDICE/2024_Massimario_Civile_VolumeI.md
# → <!-- pag. 201 -->
```

Solo dopo aver letto si scrive. Attenzione ai **ritorni a capo della conversione**: nei volumi
annuali un cognome può risultare spezzato (`Var- rone`) e una parola può andare a capo a metà; nella
citazione si ricompone il testo, senza alterarne il contenuto.

---

## MODULO 2 — COME SI CITA

Due formati, uno per binario. Vanno usati per intero: estremi + Rv + **collocazione in KB**.

**Rassegna annuale** (stock 2023-2024):

```
Cass. civ., Sez. 2, n. 13949/2024, Rv. 671693-01 — Rassegna Massimario Civile 2024, vol. I, p. 201
```

**Rassegna mensile** (2025 - febbraio 2026):

```
Cass. civ., Sez. U, ord. interlocutoria n. 26471 del 01/10/2025, Rv. 676180-01 — Rassegna mensile
ottobre 2025, p. 4
```

Regole di citazione:
- **Il tipo di provvedimento va indicato** quando la fonte lo indica (sentenza / ordinanza /
  ordinanza interlocutoria / regolamento di giurisdizione). Un'**ordinanza interlocutoria** non
  decide: rimette. Citarla come precedente è un errore che l'avversario userà.
- **Mai citare senza pagina**: la collocazione rende la citazione verificabile in dieci secondi.
- **Mai dedurre un Rv.** Se manca, si citano gli estremi che ci sono e si dichiara che il numero
  Rv non risulta dalla fonte in KB.
- Per una pronuncia presente sia in mensile sia in annuale, **si preferisce la citazione annuale
  con Rv**: è la forma assestata e la più agevolmente verificabile su Italgiure.

**Formato con segnaposto**, da usare quando il principio è noto ma la fonte non è in KB — mai
riempirlo a memoria:

```
Cass. civ., Sez. [ ], [sent./ord.] n. [ ] del [data], Rv. [ ] — NON PRESENTE IN KB:
da verificare su Italgiure/DeJure prima del deposito
```

---

## MODULO 3 — GERARCHIA DELLE FONTI CIVILI

Dettaglio in `KNOWLEDGE_BASE/00_META/GERARCHIA_FONTI.md`. Sintesi operativa: **consultabile ≠
autorevole**. Ogni citazione porta con sé il suo livello.

| Livello | Fonte | Come si usa |
|---|---|---|
| **1** | **Sezioni Unite civili** (art. 374 c.p.c.) | Prevalgono sempre sulle sezioni semplici. Se esiste una SU sul punto, si apre con quella. |
| **1** | **Principio di diritto su rinvio pregiudiziale (art. 363-bis c.p.c.)** | Vincolante nel procedimento in cui la questione è sorta e, se il processo si estingue, in ogni successivo processo tra le stesse parti sulla medesima domanda. |
| **1** | **Corte costituzionale — pronunce ablative** | La norma dichiarata illegittima non esiste più: va segnalato immediatamente all'avvocato, prima di ogni altro ragionamento. |
| **2** | **Cassazione, sezioni semplici** | Orientamento seguito dal merito. In caso di contrasto si espongono **entrambi** gli indirizzi. |
| **2** | **Corte cost. interpretative/additive** | Non abrogano: fissano l'interpretazione costituzionalmente orientata. |
| **3** | **CGUE** | Peso **alto e spesso decisivo** in materia di tutela del consumatore e clausole abusive, GDPR e protezione dei dati, trasporto aereo, appalti, concorrenza, non discriminazione. L'interpretazione della CGUE vincola il giudice nazionale, che deve disapplicare la norma interna incompatibile: è un argomento più forte di una massima di sezione semplice. |
| **3** | **Corte EDU** | Art. 6 (equo processo e durata ragionevole), art. 8 (vita privata e familiare), art. 1 Prot. 1 (proprietà). Rimedio interno collegato: revocazione ex art. 391-quater c.p.c. |
| **4** | **Dottrina** | Persuasiva. Va citata **come dottrina**, mai come giurisprudenza. |
| **4** | **Giurisprudenza di merito** | Persuasiva, ma la prassi del foro competente conta molto in concreto. **Non è in KB**: la cerca l'avvocato sulla Banca Dati di Merito (accesso con SPID/CIE/CNS). |

**Contrasti e questioni pendenti.** Quando due sezioni semplici divergono: **(1)** esporre entrambi
gli orientamenti con le rispettive massime testuali; **(2)** verificare se il contrasto è **già stato
rimesso** alle Sezioni Unite o è oggetto di rinvio pregiudiziale ex art. 363-bis — le ordinanze
interlocutorie nelle mensili lo segnalano espressamente; **(3)** ricordare che una **questione
pendente non è un precedente**: si usa per chiedere la rimessione, per un motivo in subordine, per
valutare se attendere. Mai citarla come autorità.

---

## MODULO 4 — COSTRUIRE LA SEZIONE GIURISPRUDENZIALE DI UN ATTO

Un atto civile regge se il giudice, leggendo, può verificare tutto senza uscire dal foglio.
Schema per ogni principio che si vuole affermare:

1. **Enunciato del principio**, in una frase, con la conseguenza sul nostro caso.
2. **Massima testuale** — virgolettata, non parafrasata, presa dalla pagina letta.
3. **Estremi completi + collocazione** nel formato del MODULO 2.
4. **Applicazione al fatto**: perché quella massima decide *questo* punto. Senza questo passaggio
   la citazione è arredamento.

Esempio di blocco corretto (fonte reale in KB, testo da incollare dalla pagina):

> In tema di compensazione volontaria, **Cass. civ., Sez. 2, n. 13949/2024, Rv. 671693-01**
> (Rassegna Massimario Civile 2024, vol. I, p. 201) ha chiarito che essa «non richiede la certezza,
> liquidità ed esigibilità dei contrapposti crediti […] ma si fonda sull'accordo delle parti, la cui
> dimostrazione non richiede l'osservanza di forme particolari». Nel nostro caso ne discende che [...].

**Obblighi non negoziabili in questa sezione:**

- **L'orientamento contrario si dichiara.** Se esiste un indirizzo sfavorevole, va scritto e
  affrontato — l'avversario lo citerà comunque, e il giudice se ne accorgerà. Formula tipica:
  "*non ignora la difesa l'orientamento secondo cui […] (estremi); esso tuttavia non si attaglia
  al caso di specie perché […]*".
- **Distinguere consolidato da isolato.** SU o indirizzo uniforme pluriennale = consolidato.
  Una singola massima mensile del 2025 = pronuncia recente, non indirizzo. Dirlo.
- **Segnalare il superamento.** Se una massima più recente in KB contraddice quella più antica,
  si cita la più recente e si dà conto della precedente.
- **Divieto assoluto di citare ciò che non è in KB.** Nessun numero di sentenza a memoria, nessuna
  ricostruzione "plausibile", nessun Rv dedotto per analogia. Se il principio serve ma la fonte
  manca, si scrive il principio e si marca il punto con la formula del MODULO 0: sarà l'avvocato
  a chiudere la citazione dalla banca dati prima del deposito.
- **I numeri scadono.** Tabelle del danno, saggio legale, parametri forensi: quando compaiono in
  una massima, indicare l'anno di riferimento e segnalare che vanno riverificati.

---

## Output tipico e avvertenze

Struttura della risposta: **(1)** copertura della KB per questa domanda (MODULO 0); **(2)** massime
trovate, raggruppate per livello gerarchico, ciascuna con testo, estremi e pagina; **(3)**
orientamento contrario, se esiste in KB; **(4)** stato dell'indirizzo (consolidato / recente /
controverso / pendente in SU o 363-bis); **(5)** buchi dichiarati, con l'indicazione di dove
verificarli; **(6)** blocco pronto per l'atto, se richiesto, nel formato del MODULO 4.

- Asciutto e verificabile: la forza dell'argomento sta nella massima, non nell'aggettivo.
- Se la ricerca non produce nulla, dirlo in una riga e indicare dove cercare — non riempire.
- Non presentare mai come "orientamento della Cassazione" ciò che è una singola pronuncia.
- Tutto ciò che esce da questa skill è materiale di lavoro: l'avvocato verifica sulla banca dati
  ufficiale prima del deposito.
