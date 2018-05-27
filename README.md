# Ontologies
In the [NIE-INE](http://www.fee.unibas.ch/nie_ine.html) project an infrastructure is developed to ensure long-term storage of data of scientific edition projects in the Humanities at the Swiss Universities of Basel, Bern and Zürich.  
For this purpose the existing platform [Knora-SALSAH](https://github.com/dhlab-basel/Knora) of the [Digital Humanities Lab](https://github.com/dhlab-basel) is used.  
The essence of the infrastructure is that data, stored in e.g. a MySQL relational database, are converted to a different i.e. machine-readable format by making the semantics of the data explicit.  
To enable data expression in this new format, a series of vocabularies or ontologies are created, representing [Semantic Web technology](https://github.com/nie-ine/Ontologies/wiki/Introduction-to-Semantic-Web-technology), introduced on the wiki.  
These semantic models adhere to the [model theory of W3C RDF, RDFS](https://www.w3.org/TR/2002/WD-rdf-mt-20020429/), and [OWL Full](https://www.w3.org/TR/owl-semantics/), and are declared in [Turtle syntax](https://www.w3.org/TR/turtle/). At the same time the ontologies are compliant to the semantic restrictions of Knora. They are directly accessable in the [nie-ontologies](https://github.com/nie-ine/Ontologies/tree/master/nie-ontologies) folder.  
Whenever possible [ontologies developed by others (external)](https://github.com/nie-ine/Ontologies/wiki/Introduction-to-Semantic-Web-technology#other-ontologies-used-in-humanities-and-publishing) are used to base on. Local copies of such ontologies, when not available in Turtle or RDF-XML, are in the [other-ontologies](https://github.com/nie-ine/Ontologies/tree/master/other-ontologies) folder.  
NIE-ontologies are highly interdependent and represent a network-like collection of namespaces, rather than a strongly hierarchical pyramidal structure. The granularity and specificity of the formalized terminology differs strongly among the vocabularies. A basic approach is to create a namespace that can be extended easily. Rarely ontological elements will be deprecated.  
All the used ontologies are referenced in a prefix header in the Turtle files.  

# Graphics
These are created with [EasyRDF ](http://www.easyrdf.org/converter) in SVG format.  
They contain reduced representations of class and property declarations from external and NIE-ontologies.  
RDF/S and OWL classes and properties, and xsd datatypes are represented by brown ellipses and arrows resp., except subclass and subproperty properties, which are represented by green arrows.  
External ontology classes and properties are represented by purple ellipses and arrows resp.
NIE classes and properties are represented by blue ellipses and arrows resp.  

Following external ontologies are used:  
[CIDOC](http://www.cidoc-crm.org/)  
[Dublin Core Terms](http://purl.org/dc/terms/)  
[FOAF](http://xmlns.com/foaf/0.1/)  
[FRBROO](http://iflastandards.info/ns/fr/frbr/frbroo/)  

Following figures show graphical representations of triples from different ontologies concerning indicated domains with related classes and properties.  
&nbsp;  
&nbsp;  

<div align="center">

![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_event.svg)

##### Figure 1: Graphic representing classes and properties from different ontologies concerning 'event'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_agent.svg)

##### Figure 2: Graphic representing classes and properties from different ontologies concerning 'agent'
&nbsp;  
&nbsp;  
![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_creation.svg)

##### Figure 3: Graphic representing classes and properties from different ontologies concerning 'creation'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_language.svg)

##### Figure 4: Graphic representing classes and properties from different ontologies concerning 'language'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_expression.svg)

##### Figure 5: Graphic representing classes and properties from different ontologies concerning 'expression'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_text.svg)

##### Figure 6: Graphic representing classes and properties from different ontologies concerning 'text'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_text-structure.svg)

##### Figure 7: Graphic representing classes and properties from different ontologies concerning 'text structure'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_information-carrier.svg)

##### Figure 8: Graphic representing classes and properties from different ontologies concerning 'information carrier'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_print.svg)

##### Figure 9: Graphic representing classes and properties from different ontologies concerning 'print'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_letter_DUO.svg)

##### Figure 10: Graphic representing classes and properties from different ontologies concerning 'letter'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_edition.svg)

##### Figure 11: Graphic representing classes and properties from different ontologies concerning 'edition'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_literature_basis.svg)

##### Figure 12: Graphic representing classes and properties from different ontologies providing a conceptual basis for 'literature'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_literature.svg)

##### Figure 13: Graphic representing classes and properties from different ontologies concerning 'literature'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_text-structure_poem.svg)

##### Figure 14: Graphic representing classes and properties from different ontologies concerning 'text-structure' and 'poem'


![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_ontology_graphics/NIE_publication.svg)

##### Figure 15: Graphic representing classes and properties from different ontologies concerning 'publication'
</div>

Figure 16 shows a graphical representation of the classes and properties from the external ['WGS84 Geo Positioning' ontology](https://github.com/nie-ine/Ontologies/blob/master/geo.ttl).  

![figure](https://github.com/nie-ine/Ontologies/tree/master/other-ontologies/geo_reduced.svg)

##### Figure 3: Graphic representing the classes and properties from the 'WGS84 Geo Positioning' ontology
