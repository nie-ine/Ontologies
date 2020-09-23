Dear visitor, we are in the process of transferring information from this repository to the [e-editiones.ch website](http://e-editiones.ch), to bring all the SWT parts (and more) together.  
There will be the authoritative publication of our ontologies, and rules for machine reasoning.  
The development of domain ontologies and rules for machine reasoning will remain in this GitHub project.
<!---
and also the functional parts (microservices) for SPARQL1.1 (Jena-Fuseki-TDB2) and N3-rule-machine reasoning (EYE) on the RDF-graphs of a few edition projects.

NIE-ontologies are highly interdependent and represent a networked collection of namespaces, rather than a strongly hierarchical pyramidal structure. They differ quite in size, granularity and specificity. A basic approach is to create a namespace that can be extended easily. Rarely ontological elements will be deprecated.  
All the used ontologies are referenced in a prefix header in the Turtle files.  
A series of [basic modeling patterns](https://github.com/nie-ine/Ontologies/wiki/2.-Basic-modeling-patterns) are also published on the wiki.

There are 2 series: more general and project ontologies. The former are grosso modo further divided into four levels: 1) general domain, 2) general Humanities, 3) specific Humanities, and 4) external terminology systems ontologies (see figure 1). This division is somehow arbitrary, meaning that it isn’t formalized, but it is convenient to illustrate the articulation of ontologies and their interrelations. Table 1 shows the status of the modeling at the end of September 2019. The most populated ontologies are ‘human’, ‘information carrier’, ‘document’, ‘text’, ‘text-expression’, ‘text-structure’, ‘scholarly-editing’, ‘publishing’, ‘literature’, and ‘linguistic-morphology’. The ‘time’-ontology contains properties mainly for N3-rule declarations.

<div align="center">

![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE-ontologies-network.png)

##### Figure 1: A simplified representation of the NIE-INE web of ontologies
&nbsp;  

![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE-ontologies_numbers.png)

##### Table 1: NIE ontologies in numbers at end of September 2019
&nbsp;  
</div>

## General domain ontologies
Although all ontological classes are instantiable, the more general ones will often function as “glue” to search in an RDF-database with SPARQL queries, and to enhance machine reasoning, e.g. for subsumption (subclassing). For example, if a scholar wants to search for all translations of a certain text, the property ‘is translated into’ can be used without specifying the language. In another case, one would like to find all information carriers (e.g. manuscripts and prints) bearing creations from of a certain author, but crossing more than one project: one project refers to prints existing in an archive and having a signature, and another project uses manuscripts preserved in a library with a manuscript identifier; both the manuscripts and prints can be found with a super-property ‘is on carrier’.
As a general domain ontology, the concept-ontology (see figure 7 in 'Graphics') describes for example concepts created by a person as abstract ideas, e.g. symbolic and propositional, basing on CIDOC-CRM and FRBROO. It contains entities such as ‘information’, ‘identifier’, and ‘thought-method’, and their relations to each other and to other entities, e.g. persons. The document-ontology (see also figures 1, 8, 9, and 13 in 'Graphics') describes documents, document structures, e.g. tables, identifiers and references, such as footnotes. It also contains the abstract document expression as based on FRBROO, and different relations between document structures.

## General Humanities Ontologies
The “general Humanities ontologies” comprise the core concepts for scholarly editions, as well as the bulk of entities modeled so far in agreement with the edition projects. The following is a description of five core vocabularies for scientific editing in Humanities.

### Text
This ontology describes text as a human natural language expression serialized in writeable form (see figure 11 in 'Graphics'). It contains all kinds of text forms (e.g. written, typewritten, transcribed, and printed) and roles of persons processing text (e.g. editor, annotator, and citer). It serves as basis for all text-related ontologies: text-expression, text-structure, text-editing, and literature ontology.

### Text expression
The eponymous core concept bases (via the document-ontology) on FRBROO, as text abstracted from its carrier (see Figure 9 in 'Graphics'). The ontology declares further related roles (e.g. author and commentator) and general expression types (e.g. draft and commentary). It provides the basis for the literature- and scholarly-editing-ontology.

### Text structure
This ontology describes all kinds of textual structures (see figure 13 in 'Graphics'), e.g. syntactic, compositional, content, scientific, readability. They form an upper layer to enable more flexible and extensive search, as well as machine reasoning. More specific entities are: word, sentence, paragraph, section, line, and text column. Extensions of this ontology are the note-structure- (see figure 14 in 'Graphics') and the prosodic-structure-ontology (see figure 15 in 'Graphics'), containing entities such as marginal note and gloss, and verse and strophe respectively. An important relation between structures is ‘part of’, which, by its transitive nature, enables searching and machine reasoning in a way that do not require to explicitly state all possible relations between structures in the data, since they can be inferred via transitivity.

### Text editing and Scholarly editing
Both describe the necessary semantics for editing, the latter extending the former with specific scholarly entities, e.g. diplomatic transcription, critical edition, different types of apparatus, lemma, variant, editorial comment, witness, siglum and more alike. Also related roles are declared, e.g. editor, glossator, and critical text editor. An extensive set of properties relates these entities to each other, as well as to text, text structure and expression elements (see figures 1, 9, 16, and 17 in 'Graphics').

### Publishing
This ontology describes classes and properties related to publishing, e.g. publication and its subclasses, e.g. printed and web publication, serial like newspaper, periodical, or magazine. There is a substantial set of properties relating expressions and other entities to elements in this ontology.

### Literature
This ontology describes literary genres such as narrative and different kinds of poetry, and further different types of literary expressions (e.g. poem, hymn, novel) and their subclasses. It also contains related roles, e.g. poet and novelist. Different types of literary structures are declared, e.g. foreword, preface, prologue, and epilogue, and related properties (see figures 1, 9, 21, and 22 in 'Graphics').

## Specific Humanities ontologies
This series comprises more specific entities as used in different specialized domains in the Humanities, e.g. about scholasticism. Some ontologies are an onset (e.g. ‘indology’, ‘catholic organization’ and ‘philosophy’), providing the more general concepts as needed for the current projects, but they will be extended. ‘Catholic orders’ and ‘philosophies’ describe subclasses of classes in aforementioned ontologies, also to be extended.
Although the scope of these ontologies is narrower, i.e. more project-oriented, the entities can be reused in another context, if applicable, meaning that they do not need to be restricted to a specific project.

## External terminology systems ontology
This ontology contains formal descriptions of datatypes, functioning as link between terminology or coding systems, and OWL ontologies. Such coding systems in the Humanities are general ISO1 standards (e.g. for languages), more specific ISO standards such as OAIS2, and GND3 for the DACH countries. It is also planned to use SKOS schemes and properties for this purpose in the near future.

## Project ontologies
These ontologies contain entities linked to the specific subjects of the projects, but they are still usable outside the respective projects, if applicable. For example, another national or international project about a same author could reuse some elements in order to be linkable with one of the projects supported by NIE-INE. It then would be possible to query the two different SPARQL endpoints simultaneously, which is essential for research since the triple stores can contain complementary information on the same subject. This is actually the case for the DRCS project, a project dealing with the commentaries on the Sentences of Peter Lombard, which is linked to another project of the University of Baltimore, U.S.. This case demonstrates the added value of semantic interoperability between disparate databases, facilitated by the use of the same external ontologies CIDOC-CRM and FRBROO.

Note: until 28 November 2019 a similar library of reduced and adapted ontologies was maintained for the [Knora server application](https://www.knora.org/), developed by the [DHLab (DHL)](https://dhlab.philhist.unibas.ch/en/home/) at the University of Basel and the [Data and Service Center for humanities (DaSCH)](https://dasch.swiss/) (see also on the [wiki](https://github.com/nie-ine/Ontologies/wiki/Note:-DHL-Knora-ontologies)).

# Graphics
Note:
The graphics are being updated to the current status of the ontologies.  

Four kinds of graphics are used to illustrate the ontologies, to show classes, properties, and instances in different ways.  

A first manually created graphic type (Figures 1, 2, and 12) shows different core domain ontological elements in a simplified way, offering a broad overview to explain the dependencies between the ontologies, but allowing to focus on certain semantics, e.g. on text and critical editing (Figure 1) and page (Figure 2), while providing also the more general semantics.  

A second type of graphic centers 1 entity (Figures 3, 11, and 17), e.g. ‘event’, relating it to elements from different domain ontologies, and adhering (in a reduced way) to the RDF structure, e.g. mentioning prefixes and full property names. Classes are represented by discs, properties by rectangles. Classes from external ontologies are colored orange in the upper part. These graphics are created with [Grafo](https://app.gra.fo/). The subclass property is represented by a dotted arrow.  
 
A third type of graphic (Figure 7) focuses on (a part of) an ontology, also representing properties as nodes. It is created with the open source [SPARQL-visualizer](https://github.com/MadsHolten/sparql-visualizer), by filtering some ontological elements out (labels, comments and blank nodes) to enhance readability. It is particularly suitable for terminology discussion with domain specialists.  

Similar graphics are created with [EasyRDF ](http://www.easyrdf.org/converter) (Figures 4, 5, 6, 10, 18, 19, 21-25).   
RDF/S and OWL classes and properties, and xsd datatypes are represented by brown ellipses and arrows resp., except subclass and subproperty properties, which are represented by green arrows.  
External ontology classes and properties are represented by purple ellipses and arrows resp.  
NIE classes and properties are represented by blue ellipses and arrows resp.  

A fourth type (Figures 8, 9, 13, 14, and 15), created with [Protégé](https://protege.stanford.edu/), depicts a subsumption tree of a merged group of ontologies. It is very useful to get a quick and broad hierarchical overview during the modeling. In the example, four ontologies are merged and linked to CIDOC-CRM.

Following external ontologies are used:  
[CIDOC-CRM](http://www.cidoc-crm.org/)  
[Dublin Core Terms](http://purl.org/dc/terms/)  
[FOAF](http://xmlns.com/foaf/0.1/)  
[FRBROO](http://iflastandards.info/ns/fr/frbr/frbroo/)  
[SWEET Space](http://sweetontology.net/reprSpace)  
[SWEET Time](http://sweetontology.net/propTime)  
[SWEET Space Distance](http://sweetontology.net/propSpaceDistance)  

<div align="center">

![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_core-concepts_graphic.png)

##### Figure 1: Graphic representing core classes and properties from different ontologies
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_page_graphic.png)

##### Figure 2: Graphic representing classes and properties from different ontologies concerning 'page'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_event.png)

##### Figure 3: Graphic representing classes and properties from different ontologies concerning 'event'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_agent.svg)

##### Figure 4: Graphic representing classes and properties from different ontologies concerning 'agent'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_creation.svg)

##### Figure 5: Graphic representing classes and properties from different ontologies concerning 'creation'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_language.svg)

##### Figure 6: Graphic representing classes and properties from different ontologies concerning 'language'
&nbsp;  
&nbsp;  
Figure 7 shows the concept-ontology, created with [SPARQL-visualizer | Intro-viz](https://github.com/MadsHolten/sparql-visualizer)  

![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/sparql-viz-graph_concept.svg)

##### Figure 7: Graphic representing classes and properties from the concept-ontology
&nbsp;  
&nbsp;  
Figure 8 shows the subsumption tree of the class concept:Information, from the concept, document, text and text structure ontologies.  

![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_information.png)

##### Figure 8: Tree representing classes from different ontologies concerning 'information'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_expression.png)

##### Figure 9: Tree representing classes from different ontologies concerning 'expression'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_expression.svg)

##### Figure 10: Graphic representing classes and properties from different ontologies concerning 'expression'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_text.png)

##### Figure 11: Graphic representing classes and properties from different ontologies concerning 'text'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_reference.png)

##### Figure 12: Graphic representing classes and properties from different ontologies concerning 'text referencing'
See also: [Basic modeling pattern for text referencing](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_basic-modeling-patterns/BMP_reference.png)
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_text-structure.png)

##### Figure 13: Tree representing classes concerning 'text structure'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_text-structure_note.png)

##### Figure 14: Tree representing classes concerning 'note structure'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_text-structure_prosodicStructure.png)

##### Figure 15: Tree representing classes concerning 'prosodic structure'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_scientific-structure.png)

##### Figure 16: Graphic representing classes and properties from different ontologies concerning 'scientific structure'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_apparatus.png)

##### Figure 17: Graphic representing classes and properties from different ontologies concerning scientific edition and apparatus
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_information-carrier.svg)

##### Figure 18: Graphic representing classes and properties from different ontologies concerning 'information carrier'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_print.svg)

##### Figure 19: Graphic representing classes and properties from different ontologies concerning 'print'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_letter.svg)

##### Figure 20: Graphic representing classes and properties from different ontologies concerning 'letter'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_literature_basis.svg)

##### Figure 21: Graphic representing classes and properties from different ontologies providing a conceptual basis for 'literature'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_literature.svg)

##### Figure 22: Graphic representing classes and properties from different ontologies concerning 'literature'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_text-structure_poem.svg)

##### Figure 23: Graphic representing classes and properties from different ontologies concerning 'text-structure' and 'poem'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_publication.svg)

##### Figure 24: Graphic representing classes and properties from different ontologies concerning 'publication'
</div>

Figure 25 shows a graphical representation of the classes and properties from the external ontology [WGS84 Geo Positioning](http://www.w3.org/2003/01/geo/wgs84_pos#).  

<div align="center">

![figure](https://github.com/nie-ine/Ontologies/blob/master/Other-ontologies/geo_reduced.svg)

##### Figure 25: Graphic representing the classes and properties from the 'WGS84 Geo Positioning' ontology
</div>
--->