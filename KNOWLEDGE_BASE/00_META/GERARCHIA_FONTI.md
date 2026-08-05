# Gerarchia delle Fonti — Regole per l'AI (settore civile)

Questo file definisce come Claude deve pesare le fonti presenti nella Knowledge Base.
**Va letto prima di qualsiasi ragionamento giuridico.**

---

## Regola fondamentale

Non tutte le fonti hanno lo stesso valore. Una sentenza del Tribunale di Roma non vale quanto una
pronuncia delle Sezioni Unite. L'AI deve sempre indicare la fonte usata e il suo livello
gerarchico, e segnalare quando fonti di livello diverso sono in contrasto.

---

## Gerarchia in ordine decrescente di autorità

### LIVELLO 1 — Massima autorità nomofilattica

**Sezioni Unite Civili della Cassazione**
- Risolvono i contrasti tra sezioni semplici e le questioni di massima di particolare importanza
  (art. 374 c.p.c.); la sezione semplice che non condivide il principio non decide, ma rimette
  alle Sezioni Unite con ordinanza motivata (art. 374 co. 3 c.p.c.).
- In caso di contrasto con sezioni semplici, prevalgono sempre.

**Principio di diritto su rinvio pregiudiziale (art. 363-bis c.p.c.)**
- Il principio enunciato è **vincolante nel procedimento** in cui la questione è sorta e, se il
  processo si estingue, in ogni successivo processo tra le stesse parti sulla medesima domanda.
- È l'istituto civile che più si avvicina, per funzione, alle questioni rimesse alle SU: quando
  una questione è **pendente** in rinvio pregiudiziale, NON è un precedente — è la segnalazione
  che il punto è controverso (utile per istanze di sospensione, motivi in subordine, strategia).

**Corte costituzionale — sentenze ablative**
- Una norma dichiarata illegittima cessa di esistere nell'ordinamento: ogni ragionamento su quella
  norma deve tenerne conto, e va segnalato immediatamente all'avvocato.

### LIVELLO 2 — Alta autorità (orientamento dominante)

**Cassazione civile — sezioni semplici**
- Orientamento tendenzialmente seguito dai giudici di merito.
- In presenza di contrasto tra sezioni, indicare **entrambi** gli orientamenti senza sceglierne uno,
  e segnalare se il contrasto è già stato rimesso alle SU o è oggetto di rinvio pregiudiziale.
- Se l'orientamento è superato da pronuncia successiva, indicare la più recente.

**Rassegne annuali dell'Ufficio del Massimario — sezioni civili** ← *fonte principale di questa KB*
- Sintesi ufficiale degli orientamenti delle sezioni civili, anno per anno, già organizzata per tema.
- Non sostituiscono le sentenze originali, ma le rappresentano fedelmente.
- Citare come: "Rassegna Massimario Civile [anno], vol. [I/II/III], p. [pagina]", riportando gli
  estremi della pronuncia e il numero **Rv**.

**Pronunce civili segnalate dall'Ufficio del Massimario** (tipo `massimario-segnalate`)
- Massime ufficiali delle pronunce di rilievo nomofilattico pubblicate dalla Corte sul proprio portale.
- Se la pronuncia è delle **Sezioni Unite** → pesa come LIVELLO 1.
- Non hanno ancora numero Rv: si citano per numero/anno con riferimento alla scheda e al PDF
  ufficiale. Quando la stessa pronuncia compare nella Rassegna annuale con Rv, **si preferisce
  la citazione con Rv**.

**Corte costituzionale — sentenze interpretative / additive**
- Non abrogano la norma ma ne fissano l'interpretazione costituzionalmente orientata.

### LIVELLO 3 — Autorità sovranazionale (rilievo diretto)

**Corte di giustizia UE**
- Nel civile ha peso crescente e spesso decisivo: clausole abusive e tutela del consumatore,
  privacy e GDPR, trasporto aereo, appalti, concorrenza, non discriminazione.
- L'interpretazione del diritto UE data dalla CGUE vincola il giudice nazionale, che deve
  disapplicare la norma interna incompatibile.

**Corte EDU (Strasburgo)**
- Rilevanti nel civile: art. 6 CEDU (equo processo e durata ragionevole), art. 8 (vita privata e
  familiare), art. 1 Prot. 1 (protezione della proprietà).
- Le sentenze contro l'Italia hanno forza diretta; quelle contro altri Stati valgono come precedente.
- Rimedio interno collegato: revocazione ex art. 391-quater c.p.c. (termine 60 giorni), che la
  Cassazione tratta come *extrema ratio*.

### LIVELLO 4 — Autorità persuasiva

**Dottrina** (tipo `dottrina`)
- Non vincola. Utile per inquadrare, per argomentare l'interpretazione, per segnalare contrasti.
- Va sempre citata come dottrina, mai come giurisprudenza.

**Giurisprudenza di merito** (tipo `sentenza`, gradi di merito)
- Non vincola, ma orienta: particolarmente utile la prassi del **foro competente** in concreto.
- ⚠️ La Banca Dati di Merito pubblica del Ministero (BDP) è consultabile dall'avvocato con SPID/CIE/CNS,
  ma **non è integrata in questa KB** e non è automatizzabile: quando serve la prassi di merito,
  il kit lo dichiara e rimanda alla consultazione diretta.

**Note e prassi dello studio** (tipo `nota-studio`)
- Materiale interno. Consultabile, mai citabile come autorità: "secondo la nota interna dello
  studio…" non è "secondo la Cassazione…".

---

## Regole di ingaggio per l'AI

1. **Ogni citazione porta il suo tipo e il suo livello.** Consultabile ≠ autorevole.
2. **Contrasto tra livelli** → prevale il livello più alto, ma il contrasto va segnalato.
3. **Contrasto nello stesso livello** (sezioni semplici) → esporre entrambi gli orientamenti.
4. **Fonte non in KB** → dichiarare "non presente in KB" (PROTOCOLLO_GROUNDING), mai citare a memoria.
5. **Valori numerici** (tabelle del danno, saggio legale, parametri forensi) → indicare sempre
   fonte e data di riferimento: nel civile scadono in fretta.
