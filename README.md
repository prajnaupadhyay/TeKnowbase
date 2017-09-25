# Overview

TeKnowbase is a knowledge base of computer science concepts. It is organised in the form of triples in RDF form. TeKnowbase is constructed from technical websites such as Webopedia and Techtarget as well as online textbooks and Wikipedia. We first acquire entities from technical sources sources and then identify relationships between them using domain-specific heuristics. The owl:sameAs relation is used to link entities from TeKnowbase to DBpedia and Freebase entities. 

## There are 3 files here:

### 1) TeKnowbaseEntities.tsv: This file describes the entities in TeKnowbase. It consists of 3 columns:
	
	a) entity_id: This is a unique identifier assigned to each entity in TeKnowbase
	
	b) entity_name: Name of the entity
	
	c) entity_URI: A web-page dedicated to the description of this entity
	
### 2) TeKnowbaseRelations.tsv: This file describes the relations in TeKnowbase. It consists of 2 columns:
	
	a) relation_id: This is a unique identifier assigned to each relation in TeKnowbase
	
	b) relation_name: Name of the relation
	
### 3) TeKnowbase.tsv: Each line in this file states a technical fact. The first 3 columns of this file describe a triple of the following form:
	
	a) entity1: The head entity of the triple
	
	b) relation: The relation participating in the triple
	
	c) entity2: The tail entity of the triple
	
### The last 2 columns describe the following:
	
	d) source: The web-page from which the triple was extracted
	
	e) technique: The technique used to extract the triple


# TeKnowbase Statistics


Number of entities: 53,379 with 85,838 variations

Number of relations: 2574

Number of triples: 146,658

## Top 5 relations in decreasing order of frequencies

### Relation name	Frequency

synonymOf	35779

typeOf	27078

isTerminology(relatedTo)	26967

subTopicOf	2025

conceptIn	595


# Evaluation

Stratified sampling was used to sample 2% of triples participating in each of the 5-most frequest relations. These samples were evaluated by 2 experts. Triples extracted from unstructured sources were evaluated in a similiar fashion. The accuracies obtained were:

typeOf	99.03%

terminologyOf	98.9%

synonymOf	100%

subTopicOf	91.3%

conceptIn	95.4%

Unstructured sources	63.2%



# Contact:


1) prajna.upadhyay@cse.iitd.ac.in,
2) ramanath@cse.iitd.ac.in
