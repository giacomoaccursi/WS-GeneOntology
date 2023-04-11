# Gene Ontology

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

La missione del Consorzio GO è quella di sviluppare un modello computazionale aggiornato e completo dei sistemi biologici, a partire dal livello molecolare fino ad arrivare a percorsi più ampi, sistemi cellulari e a livello di organismo.

La gene ontology fornisce una rappresentazione delle attuali conoscenze scientifiche sulle funzioni dei geni (più precisamente delle molecole prteiche e di RNA non codificanti prodotte dai geni) di molti orgianismi, dall'essere umano fino ad arrivare ai batteri. È ampiamente utlizzata a supporto della ricerca scientifica e conta decine di migliaia di citazioni nelle pubblicazioni. Capire la funzione dei geni è uno degli obiettivi principali della ricerca biomedica. Inoltre, le conoscenze ottenute su un organismo sono spesso applicabili ad altri organismi, soprattutto se questi condividono i geni in questione perchè li hanno ereditati entrambi da un antenato comune.

La gene ontology come consorzio è nata nel 1998 quando i ricercatori che studiavano il genoma di 3 organismi modello - Drosophila melanogaster (moscerino della frutta), Mus musculus (topo) e Saccharomyces cerevisiae (lievito di birra) - hanno deciso di lavorare in collaborazione su uno schema di classificazione comune per la funzione dei geni. Oggi la gene ontology vanta migliaia di organismi rappresentati. 

L'ontologia consente, in modo flessibile e dinamico, di fornire descrizioni comparabili di sequenze di geni e proteine omologhe in tutto lo spettro filogenetico.
È collegata a molte altre ontologie biomediche e costituisce una base per la ricerca che applica l'informatica alla biologia e alla medicina.



