Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# Information Delivery Processes Ontology (IDPO)

## Metadata
* **IRI**
  * `https://icdd.vm.rub.de/ontology/idpo`
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
[InformationDelivery](#InformationDelivery),
[InformationDeliverySpecification](#InformationDeliverySpecification),
[InformationRequirement](#InformationRequirement),
[InformationStatus](#InformationStatus),
[InformationUsage](#InformationUsage),
[Project](#Project),
### Information
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#Information`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[prov:Entity](http://www.w3.org/ns/prov#Entity) (c)<br />
In domain of |[idpo:hasSpecification](hasspecification) (op)<br />[idpo:isUsedBy](RepresentstheusageofanInformation) (op)<br />[idpo:hasData](hasdata) (op)<br />[idpo:hasRequirement](hasrequirement) (op)<br />[idpo:hasStatus](hasstatus) (op)<br />[idpo:isGeneratedBy](isgeneratedby) (op)<br />
In range of |[idpo:isStatusOf](isstatusof) (op)<br />[idpo:isRequirementOf](isinformationrequirementof) (op)<br />[idpo:generatesInformation](generatesInformation) (op)<br />[idpo:isSpecificationOf](isspecificationof) (op)<br />[idpo:usesInformation](usesInformation) (op)<br />
### InformationDelivery
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#InformationDelivery`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[prov:Activity](http://www.w3.org/ns/prov#Activity) (c)<br />
In domain of |[idpo:generatesInformation](generatesInformation) (op)<br />[idpo:deliversFor](deliversFor) (op)<br />
In range of |[idpo:hasInformationDelivery](hasnformationdelivery) (op)<br />[idpo:isGeneratedBy](isgeneratedby) (op)<br />
### InformationDeliverySpecification
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#InformationDeliverySpecification`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:isSpecificationOf](isspecificationof) (op)<br />[idpo:deliverySpecification](deliverySpecification) (op)<br />
In range of |[idpo:hasSpecification](hasspecification) (op)<br />
### InformationRequirement
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#InformationRequirement`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:priority](priority) (dp)<br />[idpo:requires](Requires) (op)<br />[idpo:isRequirementOf](isinformationrequirementof) (op)<br />[idpo:suitability](suitablity) (dp)<br />[idpo:dueDate](duedate) (dp)<br />
In range of |[idpo:hasRequirement](hasrequirement) (op)<br />
### InformationStatus
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#InformationStatus`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:status](status) (dp)<br />[idpo:isStatusOf](isstatusof) (op)<br />[idpo:statusSystem](statussystem) (dp)<br />
In range of |[idpo:hasStatus](hasstatus) (op)<br />
### InformationUsage
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#InformationUsage`
Super-classes |[prov:Activity](http://www.w3.org/ns/prov#Activity) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:belongsTo](RepresentstheusageofanInformationDelivery) (op)<br />[idpo:usesInformation](usesInformation) (op)<br />
In range of |[idpo:isUsedBy](RepresentstheusageofanInformation) (op)<br />[idpo:hasInformationUsage](hasInformationUsage) (op)<br />
### Project
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#Project`
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[idpo:hasInformationUsage](hasInformationUsage) (op)<br />[idpo:hasMember](hasMember) (op)<br />[idpo:hasInformationDelivery](hasnformationdelivery) (op)<br />
In range of |[idpo:isMemberOf](ismemberof) (op)<br />[idpo:belongsTo](RepresentstheusageofanInformationDelivery) (op)<br />[idpo:deliversFor](deliversFor) (op)<br />

## Object Properties
[Represents the usage of an InformationDelivery](#RepresentstheusageofanInformationDelivery),
[deliversFor](#deliversFor),
[deliverySpecification](#deliverySpecification),
[derived from BPMN object](#derivedfromBPMNobject),
[generatesInformation](#generatesInformation),
[has data](#hasdata),
[has nformation delivery](#hasnformationdelivery),
[hasInformationUsage](#hasInformationUsage),
[has Member](#hasMember),
[has requirement](#hasrequirement),
[has specification](#hasspecification),
[has status](#hasstatus),
[is generated by](#isgeneratedby),
[is member of](#ismemberof),
[is information requirement of](#isinformationrequirementof),
[is specification of](#isspecificationof),
[is status of](#isstatusof),
[Represents the usage of an Information](#RepresentstheusageofanInformation),
[Requires](#Requires),
[usesInformation](#usesInformation),
[](RepresentstheusageofanInformationDelivery)
### Represents the usage of an InformationDelivery
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#belongsTo`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationUsage](InformationUsage) (c)<br />
Range(s) |[idpo:Project](Project) (c)<br />
[](deliversFor)
### deliversFor
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#deliversFor`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
Range(s) |[idpo:Project](Project) (c)<br />
[](deliverySpecification)
### deliverySpecification
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#deliverySpecification`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationDeliverySpecification](InformationDeliverySpecification) (c)<br />
Range(s) |[sh:NodeShape](http://www.w3.org/ns/shacl#NodeShape) (c)<br />[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
[](derivedfromBPMNobject)
### derived from BPMN object
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#derivedFromBPMN`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |([idpo:Information](Information) (c) or [idpo:InformationUsage](InformationUsage) (c) or [idpo:InformationDelivery](InformationDelivery) (c))<br />
[](generatesInformation)
### generatesInformation
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#generatesInformation`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />[prov:generated](http://www.w3.org/ns/prov#generated)<br />
Domain(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />
[](hasdata)
### has data
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#hasData`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
[](hasnformationdelivery)
### has nformation delivery
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#hasInformationDelivery`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Project](Project) (c)<br />
Range(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
[](hasInformationUsage)
### hasInformationUsage
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#hasInformationUsage`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Project](Project) (c)<br />
Range(s) |[idpo:InformationUsage](InformationUsage) (c)<br />
[](hasMember)
### has Member
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#hasMember`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Project](Project) (c)<br />
Range(s) |[prov:Person](http://www.w3.org/ns/prov#Person) (c)<br />
[](hasrequirement)
### has requirement
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#hasRequirement`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
[](hasspecification)
### has specification
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#hasSpecification`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationDeliverySpecification](InformationDeliverySpecification) (c)<br />
[](hasstatus)
### has status
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#hasStatus`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationStatus](InformationStatus) (c)<br />
[](isgeneratedby)
### is generated by
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#isGeneratedBy`
Super-properties |[prov:wasGeneratedBy](http://www.w3.org/ns/prov#wasGeneratedBy)<br />[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationDelivery](InformationDelivery) (c)<br />
[](ismemberof)
### is member of
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#isMemberOf`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[prov:Person](http://www.w3.org/ns/prov#Person) (c)<br />
Range(s) |[idpo:Project](Project) (c)<br />
[](isinformationrequirementof)
### is information requirement of
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#isRequirementOf`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />
[](isspecificationof)
### is specification of
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#isSpecificationOf`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationDeliverySpecification](InformationDeliverySpecification) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />
[](isstatusof)
### is status of
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#isStatusOf`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationStatus](InformationStatus) (c)<br />
Range(s) |[idpo:Information](Information) (c)<br />
[](RepresentstheusageofanInformation)
### Represents the usage of an Information
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#isUsedBy`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:Information](Information) (c)<br />
Range(s) |[idpo:InformationUsage](InformationUsage) (c)<br />
[](Requires)
### Requires
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#requires`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[sh:Shape](http://www.w3.org/ns/shacl#Shape) (c)<br />
[](usesInformation)
### usesInformation
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#usesInformation`
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
IRI | `https://icdd.vm.rub.de/ontology/idpo#dueDate`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](priority)
### priority
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#priority`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](status)
### status
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#status`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationStatus](InformationStatus) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](statussystem)
### status system
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#statusSystem`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationStatus](InformationStatus) (c)<br />
[](suitablity)
### suitablity
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/idpo#suitability`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[idpo:InformationRequirement](InformationRequirement) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `https://icdd.vm.rub.de/ontology/idpo#`
* **bpmn2**
  * `http://www.omg.org/spec/BPMN/20100524/MODEL#`
* **cc**
  * `http://creativecommons.org/ns#`
* **dash**
  * `http://datashapes.org/dash#`
* **dce**
  * `http://purl.org/dc/elements/1.1/`
* **dcterms**
  * `http://purl.org/dc/terms/`
* **foaf**
  * `http://xmlns.com/foaf/0.1/`
* **idpo**
  * `https://icdd.vm.rub.de/ontology/idpo#`
* **list**
  * `https://w3id.org/list#`
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