Gene Ontology

Link utili: http://geneontology.org/docs/literature/ 



Data la mole di dati in costante crescita che ruota attorno alla biologia molecolare, le ontologie sono emerse come strumento computazionale essenziale per aiutare l'organizzazione, la descrizione e l'analisi dei dati.

Le ontologie descrivono e classificano le entità di interesse in uno specifico dominio scentifico in maniera accessibile in modo tale da poter sviluppare algoritmi e strumenti su di ese. La tecnologia alla base delle ontologie ha le sue radici nell'intelligenza artificiale basata sulla logica, consentendo una sofisticata inferenza automatizzata e il rilevamento degli errori. 

Le ontologie sono costituite da diversi elementi distinti, fra cui classi, metadati, relazioni formati e assiomi. 

**Classi**: la classe è l'unità base di una ontologia e rappresenta un tipo di uno cosa in un dominio di interesse. Esempio: l'acido carbossilico, il cuore, il melanoma e l'apoptosi. Solitamente le classi sono associate ad un identificatore univoco, per esempio (rispettivamente) CHEBI:33575, FMA:7088, DOID:1909 e GO:0006915. Tali identificatori sono privi di semantica, non contengono riverimento al nome o alla definizione della classe, questo per promuovere stabilità anche nel momento in cui la conoscenza scientifica e la relativa rappresentazione evolvono.

**Metadata**: I metadati associati alle classi possono includere qualsiasi identificativo secondario associato e indicatori per indicare se la classe è stata contrassegnata come obsoleta. Possono anche incudere uno o più sinonimi o riferimenti incrociati a quella classe in database alternativi e risorse web.

**Relazioni**: le classi sono disposte in una gerarchia che va dal generale allo specifica. Nonostante la classificazione gerarchica, la maggior parte delle ontologie non sono semplici alberi, piuttosto sono strutturate come grafi aciclici diretti. Questo perchè è possibile che le classi abbiano più genitori nella gerarchia di classificazione e inoltre le ontologie comprendono altri tipi di relazioni tra entità diverse dalla classificazione gerarchica. Tutte le relazioni sono dirette e i redattori dell'ontologia devono fare attenzione a gareantire che la struttura complessiva non contenga cicli.

![image-20230411154732816](/home/giacomo/.config/Typora/typora-user-images/image-20230411154732816.png)

(a) A simple hierarchical tree, (b) a directed, acyclic graph, (c) a graph that contains a cycle, indicated in red

Un tipo di relazione comune usato in più ontologie è **part_of** o **has_part**, che rappresenta la composizione o la costituzione. La specifica di un tipo di relazione in un'ontologia include un identitificatore univoco, un nome e una gerarchia di classificazione. Gli stessi metadati che sono associati alle classi possono essere associati anche ai tipi di relazione. 

**Formati**: In genere le ontologie vengono memorizzate in file conformi a un formato specifico, anche se esistono eccezioni che vengono memorizzate in infrastrutture personalizzate. Le ontologie possono essere rapprsentate in diversi linguaggi ontologici e storicamente si è assistito a un'evoluzione delle capacità dei linguaggi ontologici verso una maggiore espressività e complessità logica, che è stata rispecchiata dai proressi della capacità computazionale e degli strumenti. Le ontologie biologiche come GO sono state storicamente rappresentate nel linguaggio OBO (Open Biomedical Ontologies), progettato specificamente per la struttura e il contenuto dei metadati associati alle bio-ontologie, ma col tempo ci si è spostati verso lo standard del web semantico, il Web Ontology Language (OWL). 

**Assiomi**: Nei linguaggi logic-based come OWL, le affermazioni nelle ontologie hanno un significato logico definite all'interno di una teori logica basati su insiemi. Le classi hanno istanze come membri, e gli assiomi logici definiscono vincoli sulle definizioni di classe che si applicano a tutti i membri della classe. I linguaggi logici alla base della tecnologia ontologica sono chiamati collettivamente Logiche di Descrizione. Alcuni degli assiomi logici disponibili nel linguaggio OWL: quantificazione, cardinalità, connettivi logici e negazione, disgiunzione ed equivalenza di classi, ecc...

---

**Funzione**: la nozione di funzione in biologia ha ricevuto una grande attenzione. Esistono due scuole di pensiero su come dovrebbero essere definite le funzioni: "funzione di ruolo causale" e "funzione di effetto selezionato". La funzione di ruolo causale è stata proposta per la prima volta da Cummins [1] e si concentra sulla descrizione della funzione in termini di come una parte contribuisce a una capacità complessiva del sistema che la contiene. In questa formulazione, la funzione di un'entità è relativa a un sistema a cui contribuisce. Per esempio l'affermazione "la funzione del cuore è quella di pompare sangue" ha significato solo nel contesto della capacità del sistema circolatorio più ampio di fornire nutrienti e rimuovere prodotti di scarto dai tessuti corporei. Tuttavia una delle principali obiezioni alla definizione di ruolo causale è che non esiste un modo sistematico di identificare quale debba essere il sistema più ampio e la relativa capacità di tale sistema. La funzione di "effetto selezionato", invece, deriva dalla definizione "eziologica" di funzione proposta per la prima volta da Wright [2]. In questa formulazione, la funzione di un'entità è la risposta alla domanda sul perchè l'entità esiste, ovvero equivale a chiedersi "per quale dei suoi effetti è stata selezionata durante l'evoluzione?". Un vantaggio evidente di questa formulazione è che incorpora esplicitamente considerazioni evolutive e richiede che una funzione derivi in ultima analisi dalla sua storia di selezione naturale. Ritornando all'esempio fatto in precedenza, un effetto del cuore è quello di produrre un suono, ma non sarebbe corretto dire che la funzione del cuore è quella di produrre un suono. La definizione di funzione con effetto selezionato distinguerebbe una funzione propria (pompare sangue) da un effetto accidentale (ad esempio produrre un suono) sulla base del fatto che la selezione naturale ha più probabilmente operato sull'effetto di pompare il sangue. 

**Funzioni in GeneOntology**: per comprendere come le funzioni dei geni siano rappresentate in GO, sono necessarie alcune conoscenze di base di biologia molecolare: 

+ Un gene è una regione contigua di DNA che codifica le istruzioni per la produzione di una grande molecola da parte della cellula (o potenzialmente più macromolecole diverse). 
+ Una macromolecola è chiamata prodotto genico (in quanto viene prodotta secondo le istruzioni di un gene) e può essere di due tipi: una proteina o un RNA non codificante. 
+ Un prodotto genico può agire come una macchina molecolare, cioè può eseguire un'azione chimica che chiamiamo attività.
+ Prodotto genici di geni diversi possono combinarsi in macchine molecolari più grandi, chiamati complessi macromolecolari. 

Ogni concetto della Gene Ontology si riferisce all'attività di un prodotto o di un complesso genito, in quanto si tratta di entità che svolgono processi cellulari. Un gene codifica un prodotto genico, quindi può ovviamente esere considerato la funte ultima di queste attività e processi. Ma in senso stretto, un gene non svolge un'attività in sè. Pertanto quando la Gene Ontology si riferisce alla "funzione genica" in realtà è un'abbreviazione di "funzione del prodotto genico". 

La Gene Ontology definisce l'universo delle possibili funzioni che un gene può avere, ma non fa alcuna affermazione sulle funzioni di nessun gene in particolare. Tali affermazioni sono invece catturate come "annotazioni GO". Un'annotazione GO è una affermazione sulla funzione di un particolare gene. Ma la nostra conoscenza biologica è altamente incompleta, di conseguenza, il formato idi annotazione GO è stato progettato per catturare dichiarazioni parziali e incomplete sulla funzione del gene. un'annotazione GO solitamente associa solo un singolo concetto GO a un singolo gene. Insieme, queste affermazioni costituiscono un' istantanea delle attuali conoscenze biologiche. Le diverse conoscenze sulla funzione dei geni possono essere stabilite in misura diversa, per questo ogni annotazione Go fa sempre riferimento alle prove su cui si basa.  

La Gene Ontology considera 3 aspetti distinti di come possono essere descritte le funzioni dei geni: funzione molecolare, componente cellulare e processo biologico. Per comprendere il significato di questi aspetti e il loro rapporto, può essere utile considerare il modello biologico assunto nelle annotazioni GO. Go segue quello che potrebbe essere definito il "paradigma della biologia molecolare", in questa rappresentazione, un gene codifica un prodotto genico, che svolge un processo o un'attività a livello molecolare (funzione molecolare) in una posizione specifica rispetto alla cellula (componente molecolare) e questo processo molecolare contribuisce a un obiettivo biologico più ampio (processo biologico) costituito da più processi a livello molecolare.  

![](file:///home/giacomo/Pictures/Screenshot_20230502_122825.png)

Replicazione del DNA (nel lievito) come modellata utilizzando GO. I prodotti/complessi genici (bianco) eseguono processi molecolari (funzione molecolare, rosso) in luoghi specifici (componente cellulare, giallo), come parte di obiettivi biologici pi ampi (processo biologico, in particolare la replicazione del DNA). 

Nella Gene Ontology, una funzione molecolare è un processo che può essere svolto dall'azione di una singola macchina macromolecolare, attraverso interazioni fisiche dirette con altre entità molecolari. In questo senso, la funzione denota un'azione o un'attività che un prodotto genico svolge. Queste azioni sono descritte da due prospettive distinte ma correlate, comunemente usate dai biologi: 

1. Attività biochimica.
2. Ruolo di componente in un sistema/processo più ampio.

Le attività biochimiche includono attività di legame e catalitiche e sono sol funzioni in senso lato per esempio come qualcosa funziona o il meccanimo molecolare di funzionamento.
le descrizioni di dei ruoli dei componenti, invece, si riferiscono a ruoli in processi più ampi e sono talvolta descritte per analogia con un sistema meccanico o elettrico. Per esempio, i biologi possono riferirsi a una proteina che funziona (agisce) come recettore. Questo perchè l'attività viene interpretata come la ricezione di un segnale e la ua conversione in un'altra forma fisico-chimica. A differenza delle attività biochimiche, questi ruoli richiedono un certo grado di interpretazione che include la conoscenza del contesto nel quale il prodotto genico agisce.

Una componente cellulare è una posizione, rispetto ai compartimenti e alle strutture cellulari, occupata da un macchinario macromolecolare quando svolge una funzione molecolare. Esistono due modi in cui i biologi descrivono la localizzazione dei prodotti genici: 

1. Rispetto a strutture cellulari (per esempio, il lato citoplasmatico della membrana plastica) o a compartimenti (per esempio, la membrana plasmatica).
2. I complessi macromolecolari (ad esempio, il ribosoma).

A differenza degli altri aspetti di GO, i concetti di componente cellulare non si riferiscono a processi, ma piuttosto a un'anatomia cellulare. Ciononostante sono stati concepiti per essere applicati alle azioni di prodotti o complessi genici: un annotazione GO a un componente cellulare fornisce informazioni sul punto in cui un processo molecolare può verificarsi durante un processo più ampio.

Nella GO, un processo biologico rappresenta un obiettivo specifico che l'organismo è geneticamente "programmato" per raggiungere. Ogni processo biologico è spesso descritto dal suo risutlato o stato finale, ad esempio il processo biologico della divisione cellulare porta alla creazione di due cellule figlie da una singola cellula madre. Un processo biologico è realizzato da un particolare insieme di processi molecolari eseguiti da specifici prodotto genici, spesso in modo altamente regolato e in una particolare sequenza temporale. 
L'annotazione di un particolare prodotto genico a un concetto di processo biologico GO dovrebbe quindi avere una chiara interpretazione: il prodotto genico svolge un processo molecolare che ha un ruolo integrale in quel programma biologico. Ma un prodotto genico può influire su un obiettivo biologico anche se non agisce strettamente all'interno del processo, e in questi casi un'annotazione GO mira a specificare questa relazione nella misura in cui è nota. In primo luogo, un prodotto genico può controllare quando e dove viene eseguito il programma; in altre parole, può regolare il programma. In questo caso, il prodotto genico agisce al di fuori del programma, e controlla (direttamente o indirettamente) l'attività di uno o più prodotti genici che agiscono all'interno del programma. In secondo luogo, il prodotto genico potrebbe agire in un altro programma biologico separato, necessario per lo svolgimento del programma in questione. Per esempio, l'embriogenesi animale richiede la traduzione, anche se la traduzione non è generalmente considerata parte del programma di embriogenesi. Pertanto, attualmente, l'annotazione di un determinato processo biologico può avere uno di questi tre significati (in particolare, un'attività genica può far parte di un processo biologico, regolarlo o essere a monte di un processo biologico, ma comunque necessaria per esso). Il Consorzio GO sta attualmente esplorando modi per rappresentare computazionalmente questi diversi significati in modo da poterli distinguere.

---

La Gene Ontology è un vocabolario controllato di termini per rappresentare la biologia in modo strutturato. I termini sono suddivisi in tre ontologie distinte che rappresentano tre diversi aspetti biologici: 

+ Funzioni Molecolari (MF)
+ Processi Biologici (BP) 
+ Componenti Cellulari (CC)

Queste tre ontologie sono non ridontanti e condividono uno spazio comune di identificatori e una sintassi ben specificata.
I termini sono collegati fra di loro da relazioni per formare un vocabolario gerarchico. Questo è spesso modellato come un grafo nel quale le relazioni formano archi diretti e i termini sono i nodi. 
Dato che ogni termine può avere relazioni multiple sia verso termini padre, sia verso termini figlio, la struttura permette una maggiore espressività rispetto a una semplice gerarchia. 

![Screenshot_20230508_095513](/home/giacomo/Pictures/Screenshot_20230508_095513.png)

La struttura dell'ontologia è illustrata su un sottoinsieme dei percorsi del termine "reolazione dell'assemblaggio della proiezione cellulare", al suo termine radice. Le relazioni in GO sono "is_a", "part_of", "has_part" o "regulates". Nella sua rappresentazione di base non dovrebbero esserci cicli nel grafo, potendo così stabilire genitori e figli. 

Ad Ottobre 2015 l'ontologia contava 43835 termini, 73776 relazioni "is_a", 7436 relazioni "part_of" e 8263 relazioni "regulates". 
Per mantentere aggiornare lo stato di conoscenza, l'onologia viene revisionata costantemente, ma i termini non vengono mai eliminati, il loro stato viene cambiato in "obsoleto", tutte le relazioni con esso vengono eliminate e al nome viene aggiunto il prefisso "obsolete". Un esempio di termine obsoleto è GO:0000005, "obsolete ribosomal chaperone activity". È stata classificata come obsoleta "perchè si riferisce a una classe di prodotti genici e processi biologici piuttosto che a una funzione molecare".
I cambiamenti alle relazioni non impattano le annotazioni perché le annotazioni sono associate a un dato termine GO indipendentemente dalle sue relazioni con altri termini all'interno del GO.
Tuttavia il rendere obsoleti i termini ha un impatto sulle annotazioni associate ad essi. In alcuni casi i vecchi termini possono essere automaticamente sostituiti dai nuovi o da un parente, in altri i cambiamenti sono così importanti che le annotazioni devono essere riviste manualmente. 
Questi cambiamenti possono influenzare le analisi effettuate usando l'ontologia. Per questo motivo nelle relazioni o negli articoli è buona norma fornire la versione del file utilizzato per una determinata analisi.
In GO il numero di versione è la data in cui il file è stato ottenuto dal sito di GO (i file di GO sono aggiornati quotidianamente)

**Perchè usare GO?** Perchè mette a disposizione un vocabolario standardizzato per descrivere geni e le funzioni e localizzazioni dei prodotti genici. La struttura gerarchica di GO permette di comparare proteine annotate a termini diversi dell'ontologia, purchè i termini abbiano relazioni tra loro. 
GO viene spesso utilizzata per analizzare i risultati di esperimenti ad alto rendimento. Un uso comune è quello di dedurre le comunanze nella posizione o nella funzione dei geni che sono sovra o sottoespressi. Nel profiling funzionale, GO viene usata per determinare quali processi sono diversi tra gli insiemi di geni. A tal fine si utilizza un test di verosomiglianza per determinare se i termini GO sono rappresentati in modo diverso tra i due gruppi di geni. Un'altra applicazione di GO è la deduzione di funzioni di geni non annotati. Le predizioni geniche con una somuglianza significativa con i geni annotati possono essere assegnate a uno o più funzioni dei geni caratterizzati . Anche la altri metodi, come la presenza di domini proteici specifici, possono essere utilizzati per assegnare termini GO. Sono stati sviluppati numerosi strumenti per applicare GO a vari task. Sebbene le risorse dell'ontologia genia facilitino le inferenze e le analisi, i ricercatori che utlizzano GO devono familiarizzare con la struttura dell'ontologia e anche con i metodi e le ipotesi alla base degli strumenti che utilizzano per garantire la validità dei risultati. 

---

La missione del Consorzio GO è quella di sviluppare un modello computazionale aggiornato e completo dei sistemi biologici, a partire dal livello molecolare fino ad arrivare a percorsi più ampi, sistemi cellulari e a livello di organismo.

La gene ontology fornisce una rappresentazione delle attuali conoscenze scientifiche sulle funzioni dei geni (più precisamente delle molecole prteiche e di RNA non codificanti prodotte dai geni) di molti orgianismi, dall'essere umano fino ad arrivare ai batteri. È ampiamente utlizzata a supporto della ricerca scientifica e conta decine di migliaia di citazioni nelle pubblicazioni. Capire la funzione dei geni è uno degli obiettivi principali della ricerca biomedica. Inoltre, le conoscenze ottenute su un organismo sono spesso applicabili ad altri organismi, soprattutto se questi condividono i geni in questione perchè li hanno ereditati entrambi da un antenato comune.

La gene ontology come consorzio è nata nel 1998 quando i ricercatori che studiavano il genoma di 3 organismi modello - Drosophila melanogaster (moscerino della frutta), Mus musculus (topo) e Saccharomyces cerevisiae (lievito di birra) - hanno deciso di lavorare in collaborazione su uno schema di classificazione comune per la funzione dei geni. Oggi la gene ontology vanta migliaia di organismi rappresentati. 

L'ontologia consente, in modo flessibile e dinamico, di fornire descrizioni comparabili di sequenze di geni e proteine omologhe in tutto lo spettro filogenetico.
È collegata a molte altre ontologie biomediche e costituisce una base per la ricerca che applica l'informatica alla biologia e alla medicina. 

---

chapter 13

L'analisi delle categorie geniche è un importante approccio di integrazione della conoscenza nelle scienze biomediche che combina basi di conoscenza come la Gene Ontology con elenchi di geni o di loro prodotti, che spesso sono il risultato di esperimenti high-throughput, ottenuti da esperimenti di laboratorio o di sintesi.
Il risultato dei metodi biologici high-throughput è spesso un elenco composto da diverse centinaia di entità biologiche, che nel caso degli esperimenti di profilazione dell'espressione genica sono identificatori di geni o dei loro prodotti. Poichè un'entità biologica può avere diverse funzioni specifiche per il contesto, è difficile per l'uomo interpretare il risultato di un esperimento sulla base di questi elenchi. Gli approcci computazionali per accedeere alle conoscenze sulle caratteristiche biologiche giocano quindi un ruolo importante nella realizzazione di ricerche basate su esperimenti high-thoughput. Un mood pratico per rispondere alla domanda "cosa sta succedendo?" è quello di eseguire un'analisi per categorie di geni, cioè chiedere se questi geni di risposta condividono alcune caratteristiche biologiche che li distinguono dall'insieme di tutti i geni testati nell'esperimento. 
