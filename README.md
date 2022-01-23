Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4  

# Information Delivery Processes Ontology (IDPO) [![DOI](https://zenodo.org/badge/363266585.svg)](https://zenodo.org/badge/latestdoi/363266585)

## Metadata
* **IRI**
  * `https://w3id.org/idpo#`
* **Publisher(s)**
  * Chair of Computing in Engineering, Ruhr-University Bochum
* **Creators(s)**
  * Philipp Hagedorn, Ruhr-University Bochum
* **Created**
  * 2020-03-30
* **Version Information**
  * v0.1
* **Imports**
  * [http://www.w3.org/ns/prov-o#](http://www.w3.org/ns/prov-o#)
  * [sh:](http://www.w3.org/ns/shacl#)
* **License**
  * [https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/)
* **Source**
  * [https://git.inf.bi.ruhr-uni-bochum.de/semweb-ontology/idpo/](https://git.inf.bi.ruhr-uni-bochum.de/semweb-ontology/idpo/)
* **Ontology RDF**
  * RDF ([idpo.ttl](turtle))
### Description
<p>The Information Delivery Processes Ontology (IDPO) Ontology is defined for modeling information delivery in the construction planning based on BPMN processes and the PROV-Ontology. It provides SHACL templates for validating information requirements and delivery specifications.</p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview
![Ontology overview](https://icdd.vm.rub.de/ontology/idpo/idpo.svg "Ontology overview")
**Figure 1:** Ontology overview
## Classes
[Information](#Information),
[Information Delivery](#InformationDelivery),
[Information Delivery Specification](#InformationDeliverySpecification),
[Information Requirement](#InformationRequirement),
[Information Status](#InformationStatus),
[Information Usage](#InformationUsage),
[Project](#Project),
### Information
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#Information`
Description | <p>This class is used to represent a set of data summarized as information. Information can be generated and used. Instances of this class can be derived from bpmn2:DataObject individuals. This class is a subClass of prov:Entity which allows to associate additional provenance information.</p>
Super-classes |[prov:Entity](http://www.w3.org/ns/prov#Entity) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:hasRequirement](hasrequirement) (op)<br />[idpo:isUsedBy](isusedby) (op)<br />[idpo:derivedFromBPMN](derivedfromBPMNobject) (op)<br />[idpo:isGeneratedBy](isgeneratedby) (op)<br />[idpo:hasData](hasdata) (op)<br />[idpo:hasStatus](hasstatus) (op)<br />[idpo:hasSpecification](hasspecification) (op)<br />
In range of |[idpo:isStatusOf](isstatusof) (op)<br />[idpo:isSpecificationOf](isspecificationof) (op)<br />[idpo:generatesInformation](generatesInformation) (op)<br />[idpo:usesInformation](usesinformation) (op)<br />[idpo:isRequirementOf](isinformationrequirementof) (op)<br />
### Information Delivery
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#InformationDelivery`
Description | <p>This class is used to represent the activity of generation information regarding defined information requirements and delivery specifications. Instances of this class can be derived from bpmn2:Task individuals. This class is a subClass of prov:Activity which allows to associate additional provenance information.</p>
Super-classes |[prov:Activity](http://www.w3.org/ns/prov#Activity) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:deliversFor](deliversfor) (op)<br />[idpo:derivedFromBPMN](derivedfromBPMNobject) (op)<br />[idpo:hasSendingPerson](hassendingperson) (op)<br />[idpo:generatesInformation](generatesInformation) (op)<br />
In range of |[idpo:hasInformationDelivery](hasinformationdelivery) (op)<br />[idpo:isGeneratedBy](isgeneratedby) (op)<br />
### Information Delivery Specification
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#InformationDeliverySpecification`
Description | <p>This class contains a set of delivery specifications for an associated information individual.</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:deliverySpecification](deliveryspecification) (op)<br />[idpo:isSpecificationOf](isspecificationof) (op)<br />
In range of |[idpo:hasSpecification](hasspecification) (op)<br />
### Information Requirement
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#InformationRequirement`
Description | <p>This class contains the information requirements for an associated information individual.</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:dueDate](duedate) (dp)<br />[idpo:priority](priority) (dp)<br />[idpo:requires](requires) (op)<br />[idpo:isRequirementOf](isinformationrequirementof) (op)<br />[idpo:suitability](suitablity) (dp)<br />
In range of |[idpo:hasRequirement](hasrequirement) (op)<br />
### Information Status
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#InformationStatus`
Description | <p>This class represents the status of information.</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:isStatusOf](isstatusof) (op)<br />[idpo:status](status) (dp)<br />[idpo:statusSystem](statussystem) (dp)<br />
In range of |[idpo:hasStatus](hasstatus) (op)<br />
### Information Usage
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#InformationUsage`
Description | <p>This class is used to represent the activity of using information regarding defined information requirements and delivery specifications. Instances of this class can be derived from bpmn2:Task individuals. This class is a subClass of prov:Activity which allows to associate additional provenance information.</p>
Super-classes |[prov:Activity](http://www.w3.org/ns/prov#Activity) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:belongsTo](belongsto) (op)<br />[idpo:hasReceivingPerson](hasreceivingperson) (op)<br />[idpo:derivedFromBPMN](derivedfromBPMNobject) (op)<br />[idpo:usesInformation](usesinformation) (op)<br />
In range of |[idpo:hasInformationUsage](hasinformationusage) (op)<br />[idpo:isUsedBy](isusedby) (op)<br />
### Project
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#Project`
Description | <p>This class represents a project and hosts the activities for generating and using information and the related persons.</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:hasInformationUsage](hasinformationusage) (op)<br />[idpo:hasInformationDelivery](hasinformationdelivery) (op)<br />[idpo:hasMember](hasmember) (op)<br />
In range of |[idpo:isMemberOf](ismemberof) (op)<br />[idpo:deliversFor](deliversfor) (op)<br />[idpo:belongsTo](belongsto) (op)<br />

## Object Properties
[belongs to](#belongsto),
[delivers for](#deliversfor),
[delivery specification](#deliveryspecification),
[derived from BPMN object](#derivedfromBPMNobject),
[generates Information](#generatesInformation),
[has data](#hasdata),
[has information delivery](#hasinformationdelivery),
[has information usage](#hasinformationusage),
[has member](#hasmember),
[has receiving person](#hasreceivingperson),
[has requirement](#hasrequirement),
[has sending person](#hassendingperson),
[has specification](#hasspecification),
[has status](#hasstatus),
[is generated by](#isgeneratedby),
[is member of](#ismemberof),
[is information requirement of](#isinformationrequirementof),
[is specification of](#isspecificationof),
[is status of](#isstatusof),
[is used by](#isusedby),
[requires](#requires),
[uses information](#usesinformation),
[](belongsto)
### belongs to
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#belongsTo`
Description | Represents the usage of an information inside a project
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationUsage](InformationUsage) (c)<br />
Range(s) |[idpo:Project](Project) (c)<br />
[](deliversfor)
### delivers for
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#deliversFor`
Description | Represents the delivery of an information inside a project
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
Range(s) |[idpo:Project](Project) (c)<br />
[](deliveryspecification)
### delivery specification
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#deliverySpecification`
Description | Represents the concrete specification of delivered information as a sh:NodeShape oder any other rdfs:Resource
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationDeliverySpecification](InformationDeliverySpecification) (c)<br />
Range(s) |[sh:NodeShape](http://www.w3.org/ns/shacl#NodeShape) (c)<br />[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
[](derivedfromBPMNobject)
### derived from BPMN object
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#derivedFromBPMN`
Description | Associates the BPMN object from which this individual has been derived
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationUsage](InformationUsage) (c)<br />[idpo:InformationDelivery](InformationDelivery) (c)<br />[idpo:Information](Information) (c)<br />
Range(s) |[bpmn2:Task](http://www.omg.org/spec/BPMN/20100524/MODEL#Task) (c)<br />[bpmn2:DataObject](http://www.omg.org/spec/BPMN/20100524/MODEL#DataObject) (c)<br />
[](generatesInformation)
### generates Information
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#generatesInformation`
Description | Associates generated information to an information delivery
Super-properties |[prov:generated](http://www.w3.org/ns/prov#generated)<br />[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />
[](hasdata)
### has data
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasData`
Description | Associates any kind of data to an information
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
[](hasinformationdelivery)
### has information delivery
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasInformationDelivery`
Description | Associates an information delivery to a project
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Project](Project) (c)<br />
Range(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
[](hasinformationusage)
### has information usage
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasInformationUsage`
Description | Associates an information usage to a project
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Project](Project) (c)<br />
Range(s) |[idpo:InformationUsage](InformationUsage) (c)<br />
[](hasmember)
### has member
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasMember`
Description | Associates a prov:Person to a project
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Project](Project) (c)<br />
Range(s) |[prov:Person](http://www.w3.org/ns/prov#Person) (c)<br />
[](hasreceivingperson)
### has receiving person
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasReceivingPerson`
Description | Associates a prov:Person to a information usage
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationUsage](InformationUsage) (c)<br />
Range(s) |[prov:Person](http://www.w3.org/ns/prov#Person) (c)<br />
[](hasrequirement)
### has requirement
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasRequirement`
Description | Associates a requirement to an information
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
[](hassendingperson)
### has sending person
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasSendingPerson`
Description | Associates a prov:Person to a information delivery
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
Range(s) |[prov:Person](http://www.w3.org/ns/prov#Person) (c)<br />
[](hasspecification)
### has specification
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasSpecification`
Description | Associates a specification to an information
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationDeliverySpecification](InformationDeliverySpecification) (c)<br />
[](hasstatus)
### has status
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#hasStatus`
Description | Associates a status to an information
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationStatus](InformationStatus) (c)<br />
[](isgeneratedby)
### is generated by
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#isGeneratedBy`
Description | Associates the originating information delivery to an information
Super-properties |[prov:wasGeneratedBy](http://www.w3.org/ns/prov#wasGeneratedBy)<br />[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
[](ismemberof)
### is member of
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#isMemberOf`
Description | Associates a project to a prov:Person
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prov:Person](http://www.w3.org/ns/prov#Person) (c)<br />
Range(s) |[idpo:Project](Project) (c)<br />
[](isinformationrequirementof)
### is information requirement of
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#isRequirementOf`
Description | Associates the originating information to a requirement
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />
[](isspecificationof)
### is specification of
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#isSpecificationOf`
Description | Associates the originating information to a specification
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationDeliverySpecification](InformationDeliverySpecification) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />
[](isstatusof)
### is status of
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#isStatusOf`
Description | Associates the information that uses a status
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationStatus](InformationStatus) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />
[](isusedby)
### is used by
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#isUsedBy`
Description | Represents the usage of an information
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationUsage](InformationUsage) (c)<br />
[](requires)
### requires
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#requires`
Description | Represents the concrete requirement of delivered information as a sh:NodeShape oder any other rdfs:Resource on the dataset and/or document level
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[sh:Shape](http://www.w3.org/ns/shacl#Shape) (c)<br />
[](usesinformation)
### uses information
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#usesInformation`
Description | Associates used information to an information usage
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />[prov:used](http://www.w3.org/ns/prov#used)<br />
Domain(s) |[idpo:InformationUsage](InformationUsage) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />

## Datatype Properties
[due date](#duedate),
[priority](#priority),
[status](#status),
[status system](#statussystem),
[suitablity](#suitablity),
[](duedate)
### due date
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#dueDate`
Description | The due date of an information requirement
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](priority)
### priority
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#priority`
Description | Represents the priority of an information requirement, e. g. high, low, none
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](status)
### status
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#status`
Description | Represents the status string of a status individual, e. g. Work in Progess, Shared, Published, Archived
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationStatus](InformationStatus) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](statussystem)
### status system
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#statusSystem`
Description | Represents the status system string of a status individual, e. g. ISO19650 or an URI to the originating status system
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationStatus](InformationStatus) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI) (c)<br />
[](suitablity)
### suitablity
Property | Value
--- | ---
IRI | `http://w3id.org/idpo#suitability`
Description | Represents the suitability of information within an information requirement, e. g. regarding to ISO19650
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `http://w3id.org/idpo#`
* **bpmn2**
  * `http://www.omg.org/spec/BPMN/20100524/MODEL#`
* **dash**
  * `http://datashapes.org/dash#`
* **dc**
  * `http://purl.org/dc/elements/1.1/`
* **dcterms**
  * `http://purl.org/dc/terms/`
* **foaf**
  * `http://xmlns.com/foaf/0.1/`
* **idpo**
  * `http://w3id.org/idpo#`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **sh**
  * `http://www.w3.org/ns/shacl#`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **swa**
  * `http://topbraid.org/swa#`
* **tosh**
  * `http://topbraid.org/tosh#`
* **vann**
  * `http://purl.org/vocab/vann/`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni
