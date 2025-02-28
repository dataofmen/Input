
## 6 Steps
1. IO: reading and parsing
1. Enrichment: by named entity recognition and tagging, semantic information is added
1. Preprocessing: filtering and manipulation
1. Frequencies: word counting and keyword extraction
1. Transformation: creating vector representation for each term or document
1. Visualization: tag cloud



### IO

* Parsing and reading the data into KNIME is the first step which has to be accomplished. 
* The output of all parser nodes is a data table consisting of one column with DocumentCells. 
* Each DocumentCell contains one document. 
* This list of documents can then be used as input by all nodes of the enrichment category. 


### Enrichemnt

* The Enrichment category contains nodes, which assign part of speech tags, recognize standard named entities, such as names of persons, organization, or locations; biomedical name entities, such as names of genes or proteins; or chemical structures. Each recognized named entity is assigned a tag value e.g. “Person” and a tag type e.g. “NE” for named entity. 
* The tag type represents the domain, or type of a tagger e.g. biomedical named entities or chemical named entities and the value represents a particular characteristic in that domain, e.g. gene in the biomedical field. 
* Each tagger usually assigns tags of its own domain and thus uses its own tag type and set of values.
* Based on these tag types and values filtering can be applied afterwards, the named entities can be extracted and visualized.



#### Unmodifiable
Named entities can be set to “unmodifiable” in order to prevent them from being separated, manipulated or filtered by subsequent nodes of the preprocessing category in the workflow (e.g. Stemmer).

#### Tagger conflicts
If two named entity recognizer are applied one after the other, the latter will overwrite the tagging of the former in case of conflicts. For example if first the ABNER Tagger node recognized “interleukin 7” as a named entity, and second the Dictionary Tagger node recognizes “interleukin” as a named entity (based on a specified dictionary), then the previously recognized term “interleukin 7” is split up and “interleukin” (without 7) is tagged as a named entity.


### Preprocessing
In the preprocessing step terms are filtered and manipulated in order to get rid of terms that do not contain content, such as stop words, numbers, punctuation marks, or very small words, or to remove endings based on declination or conjugation by applying stemming.


For each tag type (tagger) there is a corresponding filter node that filters terms with certain tag values assigned.  This combination of tagging and filtering allows for a powerful identification and extraction for named entities of different types. It is for example easily possible to identify and extract gene names from PubMed articles and visualize them in a tag cloud.

#### bow (bag of words data table)
* 모든 preprocessing node는 bag of words data table 타입의 데이터만 처리할 수 있다. 따라서 preprocessing 전에 bow transformation이 필요하다.
* bow table은 term column과 document column으로 구성된다.
* The Bow creator node, which transforms a list of documents into a bag of words is available in the Transformation node category as well. 


#### preprocessing nodes
* Stop word filtering
* RegEx filter and Replacer 
* Snowball Stemmer
* Dict Replacer


#### "Dialog" tab in preprocessing nodes
The dialogs of all preprocessing nodes contain a “Preprocessing” tab, in which three settings can be specified:

* Deep preprocessing: the preprocessing of a term, e.g. stemming is on the one hand applied on each term contained in the term column of the bag of words data table. On the other hand it can be applied on the terms contained in the documents of the document column, which is called “deep preprocessing”. This is useful if e.g. after preprocessing frequencies have to be computed. If the terms are only preprocessed in the term column but not in the corresponding document itself, the preprocessed term cannot be found in document afterwards and thus not be counted. Deep preprocessing is applied by default.


* Appending: if deep preprocessing is applied, terms in the documents are preprocessed, i.e. filtered and manipulated as well. Sometimes it is useful to keep additionally the original document. Therefore this option can be selected, which is set by default as well. The original, unchanged documents are appended as additional column in the bag of words data table.


* Unmodifiable policy: By default all preprocessing nodes do not apply preprocessing on terms that have been set unmodifiable beforehand by a certain tagger node. This unmodifiable flag can be ignored.


### Frequencies
* 'terms in documents'와 'complete corpus'의 빈도를 계산한다.
* Based on the computed frequencies filtering can be applied by the Frequency Filter node in order to keep e.g. the high frequent terms.


#### Famous frequency measures
* TF: term frequency
* IDF: inverse document frequency
* inverse category frequency



### Transformation
Before 'regular KNIME nodes' can be applied on the texts the data has to be transformed into numerical data. 

#### Transformation nodes
* Document vector
* Term vector 
* Term to structure
* Bow creator
* String to Documents



