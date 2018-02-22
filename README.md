# Ontologies
In the [NIE-INE](http://www.fee.unibas.ch/nie_ine.html) project an infrastructure is developed to ensure long-term storage of data of scientific edition projects in the Humanities at the Universities of Basel, Bern and Zürich.  
For this purpose the existing platform [Knora-SALSAH](https://github.com/dhlab-basel/Knora) of the [Digital Humanities Lab](https://github.com/dhlab-basel) is used.  
The essence of the infrastructure is that data, stored in e.g. a MySQL relational database, are converted to a different i.e. machine-readable format by making the semantics of the data explicit.  
To enable data expression in this new format, a series of vocabularies or ontologies are created, representing Semantic Web technology. These semantic models adhere to the [model theory of W3C RDF, RDFS](https://www.w3.org/TR/2002/WD-rdf-mt-20020429/), and [OWL Full](https://www.w3.org/TR/owl-semantics/), and are declared in [Turtle syntax](https://www.w3.org/TR/turtle/). At the same time the ontologies are compliant to the semantic restrictions of Knora.  
The ontologies developed in NIE are in the [nie-ontologies](https://github.com/nie-ine/Ontologies/tree/master/nie-ontologies) folder.
Whenever possible ontologies developed by others are used to base on.  
Local copies of others' ontologies, when not available in Turtle or RDF-XML, are in the [other-ontologies](https://github.com/nie-ine/Ontologies/tree/master/other-ontologies) folder.
NIE-ontologies are interdependent.  
All the used or referenced ontologies are prefixed in a header in the Turtle files.  
An introduction to [Semantic Web technology](https://github.com/nie-ine/Ontologies/wiki/Introduction-to-Semantic-Web-technology) is on the wiki.
