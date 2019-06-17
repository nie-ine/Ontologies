# Ontologies

The current ontology development is in the [Ontologies-shared repository](https://github.com/nie-ine/Ontologies-shared), concerning the ontology turtle files and their dependencies on DHL's Knora.
The rest of the information here remains relevant.

In the [NIE-INE](http://www.nie-ine.ch) project an infrastructure is developed to ensure long-term storage of data of scientific edition projects in the Humanities at the Swiss Universities of Basel, Bern and Zürich.  
For this purpose the platform [Knora](https://github.com/dhlab-basel/Knora) of the [Digital Humanities Lab](https://github.com/dhlab-basel) is used.  
The essence of the infrastructure is that data, stored in e.g. a MySQL relational database, are converted to a different i.e. machine-readable format by making the semantics of the data explicit.  
To enable data expression in this new format, a series of vocabularies or ontologies are created, representing [Semantic Web technology](https://github.com/nie-ine/Ontologies/wiki/1.-Introduction-to-Semantic-Web-technology), introduced on the wiki.  
These semantic models adhere to the [model theory of W3C RDF, RDFS](https://www.w3.org/TR/2002/WD-rdf-mt-20020429/), and [OWL Full](https://www.w3.org/TR/owl-semantics/), and are declared in [Turtle syntax](https://www.w3.org/TR/turtle/). At the same time the ontologies are compliant to the semantic restrictions of Knora. They are directly accessable in the [nie-ontologies](https://github.com/nie-ine/Ontologies/tree/master/nie-ontologies) folder.  
Whenever possible [ontologies developed by others (external)](https://github.com/nie-ine/Ontologies/wiki/1.-Introduction-to-Semantic-Web-technology#other-ontologies-used-in-humanities-and-publishing) are used to base on. Local copies of such ontologies, when not available in Turtle or RDF-XML, are in the [other-ontologies](https://github.com/nie-ine/Ontologies/tree/master/other-ontologies) folder.  
NIE-ontologies are highly interdependent and represent a networked collection of namespaces, rather than a strongly hierarchical pyramidal structure. The granularity and specificity of the formalized terminology differs strongly among the vocabularies. A basic approach is to create a namespace that can be extended easily. Rarely ontological elements will be deprecated.  
All the used ontologies are referenced in a prefix header in the Turtle files.  
A series of [basic modeling patterns](https://github.com/nie-ine/Ontologies/wiki/2.-Basic-modeling-patterns) are also published on the wiki.

# Graphics
Note: the graphics are being updated to the current status of the ontologies, and in this process the ones created with [EasyRDF ](http://www.easyrdf.org/converter) (class ovals), will be replaced by graphics created with https://app.gra.fo/ (class circles).  
They contain reduced representations of class and property declarations from external and NIE-ontologies and are meant to show dependencies between domain ontologies.  
Old: RDF/S and OWL classes and properties, and xsd datatypes are represented by brown ellipses and arrows resp., except subclass and subproperty properties, which are represented by green arrows.  
External ontology classes and properties are represented by purple ellipses and arrows resp.  
NIE classes and properties are represented by blue ellipses and arrows resp.  
New: ontologies have an own color. External elements are/will be in light green. The subclass property is represented by a dotted arrow.

Besides these graphics there are tree structures created with [Protégé](https://protege.stanford.edu/) to give a subsumption-based overview of 1 or more ontologies.

Following external ontologies are used:  
[CIDOC](http://www.cidoc-crm.org/)  
[Dublin Core Terms](http://purl.org/dc/terms/)  
[FOAF](http://xmlns.com/foaf/0.1/)  
[FRBROO](http://iflastandards.info/ns/fr/frbr/frbroo/)  
[NASA Space](http://sweet.jpl.nasa.gov/2.3/reprSpace.owl#)  
[NASA Time](http://sweet.jpl.nasa.gov/2.3/propTime.owl#)  
[NASA Space Distance](http://sweet.jpl.nasa.gov/2.3/propSpaceDistance.owl#)  

Following figures show graphical representations of triples from different ontologies concerning indicated concepts with related classes and properties.  
&nbsp;  
&nbsp;  

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
Figure 7 shows the subsumption tree of the class concept:Information, from the concept, document, text and text structure ontologies.  

![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_information.png)

##### Figure 7: Tree representing classes from different ontologies concerning 'information'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_expression.png)

##### Figure 8: Tree representing classes from different ontologies concerning 'expression'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_expression.svg)

##### Figure 9: Graphic representing classes and properties from different ontologies concerning 'expression'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_text.png)

##### Figure 10: Graphic representing classes and properties from different ontologies concerning 'text'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_reference.png)

##### Figure 11: Graphic representing classes and properties from different ontologies concerning 'text referencing'
See also: [Basic modeling pattern for text referencing](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_basic-modeling-patterns/BMP_reference.png)
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_text-structure.png)

##### Figure 12: Tree representing classes concerning 'text structure'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_text-structure_note.png)

##### Figure 13: Tree representing classes concerning 'note structure'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_Protege-hierarchy_text-structure_prosodicStructure.png)

##### Figure 14: Tree representing classes concerning 'prosodic structure'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_edition.svg)

##### Figure 15: Graphic representing classes and properties from different ontologies concerning 'edition'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_apparatus.png)

##### Figure 16: Graphic representing classes and properties from different ontologies concerning scientific edition and apparatus
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_information-carrier.svg)

##### Figure 17: Graphic representing classes and properties from different ontologies concerning 'information carrier'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_print.svg)

##### Figure 18: Graphic representing classes and properties from different ontologies concerning 'print'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_letter_DUO.svg)

##### Figure 19: Graphic representing classes and properties from different ontologies concerning 'letter'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_literature_basis.svg)

##### Figure 20: Graphic representing classes and properties from different ontologies providing a conceptual basis for 'literature'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_literature.svg)

##### Figure 21: Graphic representing classes and properties from different ontologies concerning 'literature'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_text-structure_poem.svg)

##### Figure 22: Graphic representing classes and properties from different ontologies concerning 'text-structure' and 'poem'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_publication.svg)

##### Figure 23: Graphic representing classes and properties from different ontologies concerning 'publication'
</div>

Figure 24 shows a graphical representation of the classes and properties from the external ontology [WGS84 Geo Positioning](http://www.w3.org/2003/01/geo/wgs84_pos#).  

<div align="center">

![figure](https://github.com/nie-ine/Ontologies/blob/master/other-ontologies/geo_reduced.svg)

##### Figure 24: Graphic representing the classes and properties from the 'WGS84 Geo Positioning' ontology
</div>

