# Ontologies
In the [NIE-INE](http://www.fee.unibas.ch/nie_ine.html) project an infrastructure is developed to ensure long-term storage of data of scientific edition projects in the Humanities at the University of Basel.  
For this purpose the existing platform [Knora-SALSAH](https://github.com/dhlab-basel/Knora) of the [Digital Humanities Lab](https://github.com/dhlab-basel) is used.  
The essence of the infrastructure is that data, stored in e.g. a MySQL relational database, are converted to a different machine-readable format, i.e. one that makes the semantics of the data explicit.  
To enable data expression in this new format a series of vocabularies or ontologies are created, representing Semantic Web technology. These semantic models adhere to the [model theory of W3C RDF, RDFS](https://www.w3.org/TR/2002/WD-rdf-mt-20020429/), and [OWL Full](https://www.w3.org/TR/owl-semantics/), and are declared in [Turtle syntax](https://www.w3.org/TR/turtle/).  
Whenever possible existing ontologies are used to base on. NIE-ontologies are interdependent.  
All the used or referenced ontologies are prefixed in a header in the Turtle files.  
The ontologies, with 'ontology-knora.ttl' in the name', are currently [here](https://github.com/nie-ine/Knora/tree/develop/webapi/_test_data/ontologies).  
An introduction to [Semantic Web technology](https://github.com/nie-ine/Ontologies/wiki/Introduction-to-Semantic-Web-technology) is on the wiki.

## Importing an ontology in Knora, currently as 'project':

1. install Docker, managed e.g. in WebStorm

2. check Docker in command line, e.g.:
	docker images

3. extract compressed installation script InstallKnoraSalsahSipi.zip in the desired folder

4. install Knora, SALSAH, Sipi in the desired folder, in command line:
	chmod 755 SetUpKnoraSalsahSipi.sh
	. SetUpKnoraSalsahSipi.sh

5. outcomment the 3 lines for (lengthy) cloning at beginning in SetUpKnoraSalsahSipi.sh

6. create a new project in ../Knora/webapi/_test_data/all_data/admin-data.ttl by copy-pasting a previous one and adapt data accordingly  
Note: a project short name cannot contain white space, since it used as part of a generated IRI in Knora.

7. restart Knora and Salsah to reload the test data in command line:
	. DualRestartKnoraSalsah.sh

8. in ../Knora/webapi/scripts/fuseki-load-test-data.sh create link between working ontology and the 'project' ontology as declared in ../admin-data.ttl, by copy-pasting previous one and adapt data accordingly

9. restart Knora and Salsah to reload the test data:
	. DualRestartKnoraSalsah.sh

10. set permissions in ../Knora/webapi/_test_data/all_data/permissions-data.ttl by copy-pasting a previous one and adapt data accordingly

11. restart Knora and Salsah to reload the test data:
	. DualRestartKnoraSalsah.sh

12. put Knora-compliant ontologies as Turtle file in ../Knora/webapi/_test_data/ontologies

13. restart Knora and Salsah to reload the test data:
	. DualRestartKnoraSalsah.sh

14. check import in http://localhost:4200 in Salsah 2.0: information under ontology (project) name, 'Team' and 'Ressources' should be visible

15. update changes from/to Knora on GitHUb
