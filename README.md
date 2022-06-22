# INCOSE Handbook Model
Data model of information from the International Council on Systems Engineering (INCOSE) Handbook.

This is based on the Fourth Edition of the [INCOSE Handbook](https://www.incose.org/products-and-publications/se-handbook), which is based on the [ISO/IEC/IEEE 15288 standard](https://www.iso.org/standard/63711.html). 
It is a personal project and not reviewed or endorsed by INCOSE.

Whilst I have made every effort to capture the data accurately there may be mistakes or omissions. If you identify any problems then please raise and issue or a pull request.

## About
For a discipline that is [pushing for a transformation into 'model-based' delivery](https://www.incose.org/about-incose/transformation), the INCOSE handbook is decidedly 'document-centric'. 
This is despite a careful reading of it revealing a reasonably well defined ontology and relatively strict set of definitions.

The purpose of this model is to capture the information from the handbook in a rigorous fashion, enabling the use of more sophisticated visualisation tools to review it.
The intent is not to replace the document in any sense, but simply to reframe select parts of it from a model-based perspective.

## Ontolology
Although it is not explicitly defined anywhere in the handbook, an ontology of the various concepts can be drawn out, based on the documented relationships between types of entity.
In particular Chapter 1 provides some key definitions and discussion in the form of [input-process-output (IPO) diagrams](https://en.wikipedia.org/wiki/IPO_model).
Based on this and other key text in the handbook the following ontology is understood to be used:

![Metamodel image](http://www.plantuml.com/plantuml/proxy?cache=no&fmt=svg&src=https://raw.githubusercontent.com/johnwelford/incoseHandbookModel/main/ontology.puml)

## Model
The model is entirely captured within the [incoseHandbookEntities.csv](https://github.com/johnwelford/incoseHandbookModel/blob/main/incoseHandbookEntities.csv) and [incoseHandbookRelationships.csv](https://github.com/johnwelford/incoseHandbookModel/blob/main/incoseHandbookRelationships.csv) files.
Each entity has a [universally unique identifier](https://en.wikipedia.org/wiki/Universally_unique_identifier), a type (from the ontology), a name, a description, and reference to where in the handbook it is defined (both page and section number).
The entity identifiers are then referenced in relationships between the entities.
Each relationship has its own identifier, a type (from the ontology), and the identifers of the entities it comes from and goes to.

## Use
The model is available to be presented using whatever tools you wish to use, simply by directly referencing the entities and relationships files as a data source.

## Examples
* [An interactive version of the handbook N² diagram](https://observablehq.com/@johnwelford/incose-handbook-n-diagram)

## To-do
- [x] Setup project
- [x] Document ontology
- [x] Include processes & definitions
- [x] Include inputs/outputs & definitions
- [x] Include enablers/controls & definitions
- [x] Fix missing/duplicated/unused inputs/outputs (e.g. 'Procedures')
- [ ] Include activities & definitions
