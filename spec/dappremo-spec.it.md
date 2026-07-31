# Specifica DAPPREMO

**Data Protection and Privacy Relationships Model**

Versione: 1.0.1
Stato: Rilasciata
Autore: Nicola Fabiano
Licenza: CC BY 4.0 (si vedano [`../LICENSE`](../LICENSE) e [`../NOTICE.md`](../NOTICE.md))

> Questa è la traduzione italiana della specifica. Il testo canonico è quello
> inglese: [`dappremo-spec.en.md`](dappremo-spec.en.md). In caso di divergenza
> prevale la versione inglese.

---

## 0. Stato del documento

*(Questa sezione non è normativa.)*

Questo documento è la specifica canonica del Data Protection and Privacy
Relationships Model (DAPPREMO). Riformula in termini normativi un modello che è
stato descritto in forma discorsiva in una serie di pubblicazioni, registrate in
[`../PUBLICATIONS.md`](../PUBLICATIONS.md).

**Espansione canonica dell'acronimo.** DAPPREMO sta per *Data Protection and
Privacy Relationships Model*. Alcuni passaggi delle pubblicazioni di origine lo
rendono come *Data Protection Relationships Model*; quella forma abbreviata è
superata e non deve essere usata.

**Base testuale e autorevolezza.** Sono due cose distinte. La *base testuale* di
questa specifica è la versione JSCI del 2021, che è quella il cui regime di
diritti ne consente la rielaborazione. La *versione più recente sottoposta a
revisione paritaria* è il capitolo pubblicato nel 2024 negli atti dell'11°
Annual Privacy Forum. Dove le due divergano su un punto sostanziale, prevale la
pubblicazione successiva, e questa specifica la segue, enunciandone con parole
proprie il contenuto. `PUBLICATIONS.md` registra il regime dei diritti di
ciascuna fonte.

**Originalità.** Questa specifica è opera originale. Non riproduce il testo di
alcuna delle pubblicazioni elencate, che restano soggette ai termini dei
rispettivi editori.

**Sezioni normative e non normative.** Le sezioni da 3 a 6 sono normative:
stabiliscono che cosa il modello *è*, e un'implementazione o un'estensione che
dichiari conformità a DAPPREMO va valutata rispetto ad esse. Le sezioni 0, 1, 7,
8 e 9 sono informative. La sezione 2 fissa le convenzioni notazionali usate
dalle sezioni normative.

**Questioni aperte.** Due elementi presenti nelle pubblicazioni di origine sono
deliberatamente *non* enunciati come normativi, perché l'autore li dichiara in
corso di sviluppo e non sono formalmente stabiliti: la caratterizzazione del
modello attraverso relazioni di equivalenza e l'analogia con il fibrato. Sono
esposti nella sezione 8, insieme al programma di lavoro dichiarato dall'autore.

---

## 1. Introduzione

*(Questa sezione non è normativa.)*

La conformità alle norme in materia di protezione dei dati e privacy è
comunemente affrontata come la verifica di una lista di controllo rispetto a un
corpo normativo. Quell'approccio tratta le norme come un oggetto autosufficiente
e l'attività da valutare come qualcosa *a cui* le norme si applicano.

DAPPREMO propone una lettura diversa. Ogni area di attività — un settore della
pubblica amministrazione, il core business di un'impresa, un ecosistema Internet
of Things, un singolo progetto di sviluppo software — può essere descritta come
un insieme i cui oggetti sono le sue regole, attività e processi. Anche la
protezione dei dati personali e la privacy costituiscono un insieme di questo
tipo. Ciò che rileva non è allora l'applicazione dell'uno all'altro, ma le
**relazioni** fra essi: relazioni dinamiche anziché statiche, che possono
collegare interi domini oppure singoli oggetti al loro interno, e che si leggono
propriamente su più dimensioni anziché su un unico piano.

Lo scopo del modello è duplice. In primo luogo, ottenere una visione più ampia e
più precisa di un dato scenario di quanto consenta una lettura bidimensionale
delle norme. In secondo luogo — ed è l'aspetto che l'autore sottolinea nella
versione del 2024 — portare alla luce oggetti rilevanti per lo scenario ma
abitualmente trascurati, per scelta o per inavvertenza. Il valore del modello sta
tanto in ciò che fa emergere quanto nel modo in cui organizza ciò che è già noto.

I destinatari sono le autorità di controllo, i titolari e i responsabili del
trattamento, i responsabili della protezione dei dati e i consulenti, gli
interessati, e i ricercatori che lavorano alla rappresentazione formale dei
concetti di protezione dei dati e privacy.

---

## 2. Convenzioni notazionali

Le sezioni normative usano la notazione insiemistica standard:

| Notazione | Significato |
|---|---|
| `{a, b, c, …}` | l'insieme i cui elementi sono a, b, c, … |
| `a ∈ A` | a è un elemento di A |
| `A ⊂ B` | A è un sottoinsieme di B |
| `A ∪ B` | unione di A e B |
| `A ∩ B` | intersezione di A e B |
| `A × B` | prodotto cartesiano di A e B |
| `R` | una relazione |
| `a R b` | a è in relazione con b tramite R |
| `Sᵢ ∼ Sⱼ` | Sᵢ e Sⱼ sono connessi (si veda R2) |
| `∃` | esiste |
| `⟺` | se e solo se |
| `∅` | l'insieme vuoto |

Le definizioni sono numerate da `D1` a `D7`, i tipi di relazione da `R1` a `R5`,
le assunzioni da `A1` ad `A5`. I riferimenti nella forma "si veda D3" rinviano a
questi identificatori, che sono i medesimi della versione inglese e non vanno
rinumerati né rinominati.

---

## 3. Definizioni

*(Questa sezione è normativa.)*

**D1 — Dominio.**
Un *dominio* è un insieme che rappresenta un'area delimitata di attività. Sono
esempi di dominio un settore della pubblica amministrazione, il core business di
un'impresa privata, un ecosistema Internet of Things, un progetto di sviluppo
software, e la stessa area della protezione dei dati personali e della privacy.
I domini sono indicati con `S₁, S₂, S₃, …` oppure, dove conveniente, con `A`,
`B`, `C`.

**D2 — Oggetto.**
Un *oggetto* è un elemento di un dominio. Gli oggetti possono essere statici o
dinamici: norme giuridiche, principi etici, attività, e i processi che tali
attività costituiscono sono tutti oggetti. Un dominio è compiutamente descritto
dai suoi oggetti insieme alle relazioni in cui essi stanno (si veda la sezione 4).

**D3 — Proprietà caratteristica.**
Una *proprietà caratteristica* è la proprietà che accomuna tutti e soli gli
oggetti di un dato dominio. Per il dominio della protezione dei dati personali e
della privacy, la proprietà caratteristica è l'**effetto applicativo** dei suoi
oggetti, cioè l'effetto che essi producono quando sono applicati a uno scenario
concreto.

Da D3 discende che un dominio può contenere oggetti di natura eterogenea. Un
principio etico non è enunciato in alcuna legge sulla protezione dei dati,
eppure è un oggetto del dominio della protezione dei dati personali, perché
condivide con le norme giuridiche la proprietà caratteristica di quel dominio:
produce lo stesso tipo di effetto applicativo. L'appartenenza a un dominio è
determinata dalla proprietà caratteristica, non dalla fonte formale dell'oggetto.

**D4 — Insieme delle regole sulla privacy (P).**
`P` indica l'insieme i cui oggetti sono le norme giuridiche che disciplinano la
privacy e la protezione delle persone fisiche con riguardo al trattamento dei
dati personali, entro un dato ordinamento. Dove l'ordinamento è quello
dell'Unione europea, `P` comprende in particolare il Regolamento (UE) 2016/679.

**D5 — Insieme dei principi etici (E).**
`E` indica l'insieme i cui oggetti sono i principi etici che rilevano per il
trattamento dei dati personali e per la privacy. `E` non è un sottoinsieme di
`P`: i suoi oggetti non sono enunciati in norme giuridiche. È nondimeno un
insieme di oggetti che condividono la proprietà caratteristica descritta in D3.

**D6 — Insieme di riferimento (B).**
L'*insieme di riferimento* `B` (in inglese *reference set*) è definito come:

> `B = P ∪ E`

`B` è il dominio rispetto al quale gli altri domini sono valutati secondo questo
modello. L'uso di `B` anziché del solo `P` è una scelta sostanziale: rende
esplicito che la valutazione di uno scenario non è riducibile alle norme
giuridiche vigenti.

**D7 — Agente.**
Un *agente* è una persona o un ente che opera entro un dominio e trae
conseguenze dalle relazioni in cui quel dominio si trova. Sono agenti le
autorità di controllo, i titolari e i responsabili del trattamento, i
responsabili della protezione dei dati e i consulenti, e gli interessati. Gli
agenti possono essere persone fisiche o organizzazioni. Gli agenti non sono
oggetti di un dominio: agiscono sui domini e sulle loro relazioni.

---

## 4. Tipi di relazione

*(Questa sezione è normativa.)*

**R1 — Relazione.**
Dati due insiemi non vuoti `A` e `B`, una *relazione* `R` fra `A` e `B` è un
qualsiasi sottoinsieme del loro prodotto cartesiano:

> `R ⊆ A × B`

Quando la coppia ordinata `(a, b)` appartiene a `R`, gli elementi `a ∈ A` e
`b ∈ B` si dicono in relazione tramite `R`, e si scrive `a R b`.

Da R1 discende che una relazione non deve necessariamente coinvolgere tutti gli
elementi di ciascun insieme. Un elemento di `A` che non sia in relazione con
alcun elemento di `B` è *non collegato* secondo `R`; tali elementi sono ammessi e
non costituiscono un difetto del modello. Ne discende inoltre che un singolo
elemento di `A` può essere in relazione con più elementi di `B`.

![Due insiemi A e B, con frecce che indicano le coppie ordinate di una relazione R](../figures/fig-01-relation.svg)

*Figura 1 — Una relazione come sottoinsieme del prodotto cartesiano. Gli
elementi 2 e 4 di A non sono in relazione con nulla secondo R.*

**R2 — Connessione fra domini.**
Data una famiglia di domini `(S₁, S₂, S₃, …, Sₙ)`, due di essi sono *connessi*
quando fra loro sussiste una relazione:

> `Sᵢ ∼ Sⱼ ⟺ ∃R tale che Sᵢ R Sⱼ`

Un dominio può essere connesso a più domini contemporaneamente, e in tal caso la
configurazione è *uno-a-molti*; dove sia connesso a un solo dominio, la
configurazione è *uno-a-uno*.

![Quattro domini connessi da relazioni, in configurazione uno-a-molti](../figures/fig-02-connected-domains.svg)

*Figura 2 — Connessioni entro una famiglia di domini. S₁ è connesso sia a S₂ sia
a S₃: una configurazione uno-a-molti.*

**R3 — Inclusione forte.**
Quando ogni oggetto di un dominio `A` è anche oggetto dell'insieme di
riferimento `B`:

> `A ⊂ B`

L'inclusione forte afferma che tutte le regole dell'area descritta da `A` sono
anche regole di privacy o principi etici. È un'affermazione impegnativa e
raramente si verificherà. R3 è enunciata perché è il caso limite, non perché sia
quello atteso; dove uno scenario non la soddisfi, si usa invece R4.

![L'insieme A interamente contenuto nell'insieme B](../figures/fig-03-inclusion.svg)

*Figura 3 — Inclusione forte: ogni oggetto di A è anche oggetto di B.*

**R4 — Relazione debole.**
Qualunque sia il dominio `A` delle regole che disciplinano una determinata area,
esiste un opportuno sottoinsieme dell'insieme di riferimento al quale `A` è
correlato:

> `∃ A′ ⊂ B tale che A R A′`

R4 è il caso generale del modello ed è da preferire a R3 nella valutazione di
scenari concreti. Stabilisce che gli oggetti di `A` non devono essere essi stessi
norme di protezione dei dati, privacy o etica: essi sono *in relazione con* quelle
norme, e le norme così correlate costituiscono il sottoinsieme `A′` dell'insieme
di riferimento che `A` chiama in causa.

L'individuazione di `A′` per un dato `A` è l'operazione analitica centrale
secondo questo modello: determina quali norme e principi siano effettivamente
chiamati in causa dall'area sottoposta a valutazione.

**R5 — Intersezione.**
Due o più domini possono condividere oggetti. Dove ciò accade, gli oggetti
condivisi costituiscono la loro intersezione:

> `A ∩ B`, e per tre domini `A ∩ B ∩ C`, `A ∩ C`, `B ∩ C`

L'intersezione di un dominio con l'insieme di riferimento individua gli oggetti
che appartengono a entrambi, e dunque l'area in cui la valutazione del dominio e
la valutazione in materia di protezione dei dati e privacy coincidono.

![Tre insiemi sovrapposti con le loro intersezioni a due e a tre](../figures/fig-04-intersection.svg)

*Figura 4 — Intersezioni fra tre domini. Dove A sia il dominio della protezione
dei dati personali, le regioni evidenziate individuano gli oggetti che esso
condivide con gli altri.*

---

## 5. Assunzioni

*(Questa sezione è normativa.)*

**A1 — Non autonomia dell'insieme di riferimento.**
L'insieme di riferimento `B` non genera autonomamente attività. Un corpo di
norme, per quanto completo, non determina di per sé il compimento di alcuna
attività; opera attraverso la condotta concreta degli agenti individuati in D7.
L'esistenza di `B` è necessaria e funzionale ad altri domini, con i quali deve
porsi in relazione.

**A2 — Eterogeneità degli oggetti.**
Un dominio può contenere oggetti di natura diversa, purché condividano la sua
proprietà caratteristica (D3). Su questa base l'insieme di riferimento contiene
sia norme giuridiche sia principi etici.

**A3 — Dinamicità delle relazioni.**
Le relazioni fra domini sono dinamiche, non statiche. Variano nel tempo e con lo
scenario. Una valutazione condotta secondo questo modello è pertanto valida
rispetto a uno scenario dichiarato e a un momento dichiarato, e va ripetuta
quando l'uno o l'altro mutino.

**A4 — Numero non predeterminato di domini.**
Il numero di domini che possono essere considerati non è predeterminato ed è
potenzialmente illimitato. La complessità di una valutazione cresce con il numero
di domini che vi sono ammessi. La selezione dei domini rilevanti per uno scenario
è una decisione analitica che va dichiarata esplicitamente.

**A5 — Presenza dell'insieme di riferimento.**
In qualsiasi valutazione delle relazioni fra domini condotta secondo questo
modello, l'insieme di riferimento `B` è presente. Nessuna area di attività è
esente dalle norme sulla protezione delle persone fisiche con riguardo al
trattamento dei dati personali, salvo che uno specifico ordinamento disponga
diversamente.

---

## 6. Multidimensionalità

*(Questa sezione è normativa.)*

Le relazioni descritte nella sezione 4 non vanno lette su un unico piano. Una
rappresentazione bidimensionale, come un diagramma di Venn, è una proiezione:
adeguata a illustrare una singola relazione, inadeguata a rappresentare il quadro
nel suo complesso.

Il quadro va letto come una rete distribuita multidimensionale, in cui ogni nodo
è un dominio e ogni arco una relazione fra domini. Piani distinti della
rappresentazione sono strati di un unico sistema, non sistemi separati.

![Una rete distribuita di nodi collegati da archi](../figures/fig-05-network.svg)

*Figura 5 — Il quadro letto come rete distribuita. Ogni nodo è un dominio, ogni
arco una relazione. La figura è essa stessa una proiezione bidimensionale di una
struttura da leggere su più piani.*

La conseguenza pratica è una regola di metodo. Dove la valutazione di uno
scenario appaia completa su un singolo piano, essa va considerata incompleta
finché non siano state considerate le relazioni sussistenti sugli altri piani. La
posizione dell'osservatore determina ciò che è visibile; mutare quella posizione
— allargando il campo visivo fino a comprendere i diversi soggetti e processi
coinvolti — porta in evidenza relazioni che prima non erano osservabili.

---

## 7. Applicazione per agente

*(Questa sezione è informativa.)*

**Autorità di controllo.** In un'istruttoria preliminare, una questione che
appare autosufficiente è regolarmente in relazione con altri domini.
L'applicazione del modello restituisce l'insieme completo delle relazioni
chiamate in causa: per un'applicazione sottoposta a esame, ciò può comprendere
lo sviluppo software, i dispositivi connessi e i trasferimenti di dati. Nella
decisione su un reclamo, restituisce una visione d'insieme delle relazioni che
rilevano per il caso.

**Titolari e responsabili del trattamento.** Il modello sostiene l'analisi delle
relazioni fra il core business e ogni altro dominio con cui sussista un
collegamento. Individuare `A′` (R4) in fase di analisi determina quali principi
attuare e quali misure ne conseguano, in luogo di un generico adempimento di
conformità.

**Responsabili della protezione dei dati e consulenti.** Il modello sostiene una
valutazione che individua gli oggetti effettivamente pertinenti al caso, compresi
quelli che un'analisi convenzionale lascia da parte. È qui che lo scopo enunciato
nella sezione 1 — far emergere ciò che è abitualmente trascurato — incide più
direttamente sulla pratica professionale.

**Interessati.** Conoscere le relazioni che sussistono riguardo ai propri dati
personali consente un esercizio dei propri diritti più consapevole e più
corretto della sola consultazione delle norme giuridiche.

---

## 8. Direzioni di ricerca aperte

*(Questa sezione non è normativa e non enuncia alcun requisito.)*

Gli elementi che seguono sono registrati perché l'autore li ha dichiarati, nelle
pubblicazioni di origine, come lavoro in corso. Non fanno parte del modello come
sopra specificato, e nulla in questa specifica dipende da essi.

**Relazioni di equivalenza.** Le pubblicazioni di origine indicano che il modello
può essere espresso attraverso il concetto di relazione di equivalenza. Ciò non è
qui enunciato come normativo. Una relazione nel senso di R1 sussiste fra due
insiemi distinti ed è un sottoinsieme del loro prodotto cartesiano; una relazione
di equivalenza, per contro, è definita su un unico insieme e richiede
riflessività, simmetria e transitività, che non sono stabilite per le relazioni
descritte nella sezione 4. Determinare le condizioni alle quali un dominio ammetta
una partizione in classi di equivalenza, e che cosa tale partizione
rappresenterebbe in termini giuridici, resta aperto.

**Fibrato.** Le pubblicazioni di origine tracciano un'analogia con la struttura
matematica nota come fibrato, in cui la base corrisponderebbe all'insieme di
riferimento e le fibre alle relazioni fra insiemi e oggetti. L'analogia è
illustrativa; il suo sviluppo formale — l'individuazione di spazio base, fibra e
proiezione — è dichiarato dall'autore in corso di sviluppo.

**Ontologia del modello.** Nella versione del 2024 l'autore riferisce di un
lavoro volto a un'ontologia di DAPPREMO, avviato concentrandosi anzitutto sulle
relazioni fra individui, pubblica amministrazione e istituzioni, e riferisce che
una prima analisi ha fatto emergere oggetti non precedentemente individuati.
Questa specifica non enuncia tale ontologia; registrarne qui la direzione serve a
collegare i due lavori, non a duplicarli.

**Modellazione e intelligenza artificiale.** L'autore ha inoltre dichiarato un
programma di lavoro comprendente la costruzione di modelli UML che descrivano
contesti specifici secondo il modello, la raccolta di dataset, e lo sviluppo di
un sistema di intelligenza artificiale basato su tecniche di machine learning e
deep learning, con l'obiettivo di analizzare uno scenario e produrre risultati
utili ad affrontare questioni di protezione dei dati e privacy. Per il
riferimento si veda [`../PUBLICATIONS.md`](../PUBLICATIONS.md).

**Allineamento a vocabolari esistenti.** *(Non fa parte del programma dichiarato
dall'autore; è qui registrato come osservazione.)* DAPPREMO è uno strato
relazionale, non un vocabolario di concetti di protezione dei dati. Vocabolari
machine-readable sviluppati altrove forniscono concetti che potrebbero popolare i
domini di questo modello. Un'espressione di DAPPREMO in una serializzazione
semantic-web, che riusi tali vocabolari per gli oggetti e vi sovrapponga lo strato
relazionale, sarebbe una via per rendere il modello elaborabile
automaticamente, e lo collegherebbe al lavoro sull'ontologia sopra richiamato.

---

## 9. Riferimenti

La storia editoriale di DAPPREMO, con il regime dei diritti di ciascuna fonte, è
registrata in [`../PUBLICATIONS.md`](../PUBLICATIONS.md); le voci in formato
citabile sono in [`../references.bib`](../references.bib). La versione più
recente del modello sottoposta a revisione paritaria è:

- N. Fabiano, *A Singular Approach to Address Privacy Issues by the Data
  Protection and Privacy Relationships Model (DAPPREMO)*, in K. Rannenberg,
  P. Drogkaris, C. Lauradoux (a cura di), *Privacy Technologies and Policy*,
  11th Annual Privacy Forum (APF 2023), Lecture Notes in Computer Science
  vol. 13888, pp. 166–181, Springer, Cham, 2024.
  DOI: 10.1007/978-3-031-61089-9_8

Atti normativi richiamati:

- Regolamento (UE) 2016/679 (regolamento generale sulla protezione dei dati).
- Consiglio d'Europa, Convenzione sulla protezione delle persone rispetto al
  trattamento automatizzato di dati a carattere personale (STE n. 108), come
  emendata dal Protocollo CETS n. 223.
