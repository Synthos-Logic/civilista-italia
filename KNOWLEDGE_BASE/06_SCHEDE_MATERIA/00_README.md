# Schede di Materia — Guida all'uso
*Kit Civilista Italiano — versione 0.8.2 — Ultima verifica: 6 agosto 2026*

Le Schede di Materia sono l'equivalente civile delle "schede reato" del Kit Penalista. Sono il punto di ingresso operativo su una controversia: si aprono **prima** di studiare il fascicolo, per sapere cosa si deve provare, entro quando, davanti a chi e con quale filtro preventivo.

---

## A cosa servono

Una scheda risponde, per una singola materia, a cinque domande che nel civile decidono le cause:

1. **Cosa si fa valere** e su quale norma si fonda (inquadramento).
2. **Chi prova cosa** — la ripartizione dell'onere ex art. 2697 c.c. fra fatto costitutivo, impeditivo, modificativo ed estintivo, e con quale mezzo di prova. È la sezione centrale: una domanda ben fondata e mal ripartita si perde comunque.
3. **Entro quando** — prescrizione e decadenze sostanziali.
4. **Se la causa è procedibile** — mediazione obbligatoria, negoziazione assistita o nessun filtro.
5. **Davanti a chi e con quale rito**, e quanto si chiede.

Le sezioni finali (difese tipiche, quantificazione, errori ricorrenti) servono a impostare l'atto senza ripartire da zero.

---

## Come si usano

**In apertura di pratica.** Leggi la scheda della materia, poi il fascicolo. La tabella dell'onere della prova diventa la checklist documentale da chiedere al cliente al primo appuntamento: se un fatto costitutivo non ha un documento a supporto, o si trova o si cambia impostazione.

**Prima di scrivere l'atto.** La sezione "difese tipiche" va letta **dal lato opposto al proprio**: se stiamo dall'attivo, si legge la colonna del convenuto per anticipare le eccezioni e blindare le allegazioni già in citazione — dove le preclusioni sono più clementi.

**Prima del deposito.** La sezione "errori ricorrenti" è una lista di controllo. La sezione "condizione di procedibilità" è il primo controllo, non l'ultimo: una causa improcedibile è una causa persa a tavolino.

**Con le altre skill del kit:**
- calcoli di termini processuali, termini a ritroso, sospensione feriale → `civilista-scadenze` (le schede indicano il termine sostanziale, non fanno il calcolo);
- ricerca di massime e orientamenti → `civilista-giurisprudenza` con il protocollo quote-then-claim;
- redazione → `civilista-atti`; controllo pre-deposito → `civilista-verifica`;
- quantificazione analitica (tabelle, interessi, rivalutazione) → `civilista-quantificazione`.

---

## Avvertenza — materiale di lavoro, non fonte

Le schede **non sono una fonte** e non sostituiscono la verifica.

- Sono sintesi di lavoro redatte per orientare, non per essere citate in atti. Nessuna affermazione contenuta qui va riportata in un atto senza averla riscontrata sul testo normativo vigente e, per la giurisprudenza, sulla Knowledge Base.
- **Nelle schede non compaiono numeri di sentenza, per scelta.** La giurisprudenza del kit sta nella KB (Rassegne del Massimario civile) e si cerca lì, con la skill `civilista-giurisprudenza`, seguendo il PROTOCOLLO_GROUNDING: si apre la fonte, si incolla la massima testuale con l'indicazione del file e della pagina. Dove una scheda dice "orientamento consolidato" o "questione controversa", quella è un'indicazione di ricerca, non una citazione: va trasformata in una massima ancorata prima di finire in un atto. Meglio un rinvio che una citazione inventata.
- Le schede coprono il **perimetro dichiarato del kit** (contratti e crediti, responsabilità e danni, locazioni e condominio, famiglia e persone, lavoro). Fuori da lì non ci sono schede e non vanno improvvisate.
- **Attenzione ai termini nelle schede di lavoro:** le controversie dell'art. 409 c.p.c. non sono soggette alla sospensione feriale. La sezione "termini" delle schede `E_LAVORO/` va letta con questa avvertenza.

---

## Regola sui dati numerici — vincolante

**Ogni dato numerico riportato in una scheda porta la data di riferimento.**

Valgono per tutti i numeri del civile: saggio degli interessi legali, valori delle tabelle del danno, soglie di competenza per valore, soglie di procedibilità, parametri forensi, date di entrata in vigore e proroghe. Sono i dati che invecchiano più in fretta e che, se sbagliati, si vedono subito.

Formato: `valore (fonte, in vigore dal / edizione — verificato al gg/mm/aaaa)`.

Esempi in uso nelle schede:
- saggio legale **1,60% dal 1° gennaio 2026** (D.M. MEF pubblicato in G.U. nel dicembre 2025 — verificato al 5 agosto 2026);
- **TUN macrolesioni, D.P.R. 12/2025, in vigore dal 5 marzo 2025**, invalidità superiori al 10%;
- **Tabelle di Milano, edizione 2024**;
- competenza del giudice di pace: **beni mobili fino a € 10.000, danno da circolazione fino a € 25.000** (art. 7 c.p.c. come modificato dal D.Lgs. 149/2022);
- negoziazione assistita obbligatoria per pagamenti **fino a € 50.000** (art. 3 D.L. 132/2014).

Se un numero compare senza data di riferimento, va trattato come non verificato.

---

## Struttura delle cartelle

| Cartella | Materia | Schede |
|---|---|---|
| `A_CONTRATTI_E_CREDITI/` | Obbligazioni, contratti, recupero crediti | Inadempimento contrattuale; Recupero crediti e decreto ingiuntivo; Opposizione a decreto ingiuntivo |
| `B_RESPONSABILITA_E_DANNI/` | Responsabilità civile e quantificazione | Responsabilità extracontrattuale; Responsabilità sanitaria; Danno da circolazione stradale |
| `C_LOCAZIONI_E_CONDOMINIO/` | Immobili e beni comuni | Locazioni e sfratti; Condominio |
| `D_FAMIGLIA_E_PERSONE/` | Famiglia, minori, persone | Separazione, divorzio e figli; Mantenimento e affidamento |
| `E_LAVORO/` | Rapporto di lavoro subordinato | Licenziamento individuale; Crediti di lavoro |

---

## Struttura fissa di ogni scheda

1. Inquadramento
2. Fatti costitutivi e onere della prova (tabella — sezione più importante)
3. Termini (prescrizione e decadenze sostanziali)
4. Condizione di procedibilità
5. Rito e competenza
6. Difese tipiche (lato attivo / lato passivo)
7. Quantificazione
8. Errori ricorrenti
9. Da verificare (con data dell'ultima verifica)

L'ordine non cambia: serve a poter saltare direttamente alla sezione utile.

---

## Come si aggiornano

Dopo ogni causa chiusa, si aggiornano tre sezioni: "difese tipiche" (l'argomento usato e l'esito), "errori ricorrenti" (l'errore visto in concreto), "da verificare" (la novità normativa emersa e la nuova data di verifica). Una scheda con la data di verifica vecchia di più di sei mesi va riletta prima dell'uso, non dopo.
