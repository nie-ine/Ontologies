# Ontologies
In the [NIE-INE](http://www.fee.unibas.ch/nie_ine.html) project an infrastructure is developed to ensure long-term storage of data of scientific edition projects in the Humanities at the Swiss Universities of Basel, Bern and Zürich.  
For this purpose the existing platform [Knora-SALSAH](https://github.com/dhlab-basel/Knora) of the [Digital Humanities Lab](https://github.com/dhlab-basel) is used.  
The essence of the infrastructure is that data, stored in e.g. a MySQL relational database, are converted to a different i.e. machine-readable format by making the semantics of the data explicit.  
To enable data expression in this new format, a series of vocabularies or ontologies are created, representing [Semantic Web technology](https://github.com/nie-ine/Ontologies/wiki/Introduction-to-Semantic-Web-technology), introduced on the wiki.  
These semantic models adhere to the [model theory of W3C RDF, RDFS](https://www.w3.org/TR/2002/WD-rdf-mt-20020429/), and [OWL Full](https://www.w3.org/TR/owl-semantics/), and are declared in [Turtle syntax](https://www.w3.org/TR/turtle/). At the same time the ontologies are compliant to the semantic restrictions of Knora. They are directly accessable in the [nie-ontologies](https://github.com/nie-ine/Ontologies/tree/master/nie-ontologies) folder.  
Whenever possible [ontologies developed by others (external)](https://github.com/nie-ine/Ontologies/wiki/Introduction-to-Semantic-Web-technology#other-ontologies-used-in-humanities-and-publishing) are used to base on. Local copies of such ontologies, when not available in Turtle or RDF-XML, are in the [other-ontologies](https://github.com/nie-ine/Ontologies/tree/master/other-ontologies) folder.  
NIE-ontologies are highly interdependent and represent a network-like collection of namespaces, rather than a strongly hierarchical pyramidal structure. The granularity and specificity of the formalized terminology differs strongly among the vocabularies. A basic approach is to create a namespace that can be extended easily. Rarely ontological elements will be deprecated.  
All the used ontologies are referenced in a prefix header in the Turtle files.  

Figure 1 shows a graphical representation of triples from different ontologies concerning 'literature', created with [EasyRDF ](http://www.easyrdf.org/converter) in GraphViz DOT language. Also two external ontologies [CIDOC](http://www.cidoc-crm.org/) and [FRBROO](http://iflastandards.info/ns/fr/frbr/frbroo/) are mentioned.  

![figure](https://github.com/nie-ine/Ontologies/blob/master/NIE_literature_basis.svg)

##### Figure 1: Graphic representing classes and properties from different ontologies concerning 'literature'

Figure 2 shows a reduced graphical representation of the classes and properties from the external ['WGS84 Geo Positioning' ontology](https://github.com/nie-ine/Ontologies/blob/master/geo.ttl).

![figure](https://github.com/nie-ine/Ontologies/blob/master/geo_reduced.svg)

##### Figure 2: Graphic representing the classes and properties from the 'WGS84 Geo Positioning' ontology
