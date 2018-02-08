[Direct link to ontologies in Knora](https://github.com/nie-ine/Knora/tree/develop/webapi/_test_data/ontologies)

# Ontologies
In the [NIE-INE](http://www.fee.unibas.ch/nie_ine.html) project an infrastructure is developed to ensure long-term storage of data of scientific edition projects in the Humanities at the University of Basel.  
For this purpose the existing platform [Knora-SALSAH](https://github.com/dhlab-basel/Knora) of the [Digital Humanities Lab](https://github.com/dhlab-basel) is used.  
The essence of the infrastructure is that data, stored in e.g. a MySQL relational database, are converted to a different i.e. machine-readable format by making the semantics of the data explicit.  
To enable data expression in this new format a series of vocabularies or ontologies are created, representing Semantic Web technology. These semantic models adhere to the [model theory of W3C RDF, RDFS](https://www.w3.org/TR/2002/WD-rdf-mt-20020429/), and [OWL Full](https://www.w3.org/TR/owl-semantics/), and are declared in [Turtle syntax](https://www.w3.org/TR/turtle/).  
Whenever possible ontologies developed by others are used to base on.  
Local copies of others' ontologies when not available in Turtle or RDF-XML:
- [WGS84 Geo Positioning: an RDF vocabulary](https://github.com/nie-ine/Ontologies/blob/master/geo.ttl)  

NIE-ontologies are interdependent.  
All the used or referenced ontologies are prefixed in a header in the Turtle files.  
The [ontologies developed in NIE-INE](https://github.com/nie-ine/Knora/tree/develop/webapi/_test_data/ontologies), with 'ontology-knora.ttl' in the name', are currently in Knora defined as projects.  
An introduction to [Semantic Web technology](https://github.com/nie-ine/Ontologies/wiki/Introduction-to-Semantic-Web-technology) is on the wiki.