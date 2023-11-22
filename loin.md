Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# Level of Information Need (LOIN) Ontology

## Metadata
* **IRI**
  * `https://w3id.org/loin/v2`
* **Publisher(s)**
  * [Chair of Computing in Engineering, Ruhr University Bochum](https://www.inf.bi.rub.de)
* **Creators(s)**
  * [Liu Liu](https://orcid.org/0000-0001-5907-7609)
    [[ORCID]](https://orcid.org/0000-0001-5907-7609)
    (<liu.liu-m6r@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/liu_liu.html.en)
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
* **Created**
  * 2023-01-30
* **Version Information**
  * 2.0
* **Imports**
  * [http://inf.bi.rub.de/ontology/tmp](http://inf.bi.rub.de/ontology/tmp)
* **License &amp; Rights**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * &copy; 2023 by Chair of Computing in Engineering, Ruhr University Bochum
* **Source**
  * [https://github.com/RUB-Informatik-im-Bauwesen/loin-ontology](https://github.com/RUB-Informatik-im-Bauwesen/loin-ontology)
* **Ontology RDF**
  * RDF ([loin.ttl](turtle))
### Description
<p>The Level of Information Need (LOIN) Ontology is defined for specifying information requirements for delivery of data in a buildings' life cycle. The LOIN ontology is based on the standard BS EN 17412-1 (2020). Furthermore, it is extended with vocabulary for connecing Information Delivery Specifications (IDS) and Information containers for linked document delivery (ICDD) as per ISO 21597-1 (2020). </p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Properties](#properties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[Actor](#Actor),
[Alphanumerical information](#Alphanumericalinformation),
[Alphanumerical information content](#Alphanumericalinformationcontent),
[Appearance](#Appearance),
[Attribute name](#Attributename),
[Attribute of IDS](#AttributeofIDS),
[Breakdown structure](#Breakdownstructure),
[Breakdown structure type](#Breakdownstructuretype),
[Classification of IDS](#ClassificationofIDS),
[Detail](#Detail),
[Dimensionality](#Dimensionality),
[Document](#Document),
[Document content](#Documentcontent),
[Document format](#Documentformat),
[Document purpose](#Documentpurpose),
[Document specification](#Documentspecification),
[Documentation](#Documentation),
[Entity](#Entity),
[Entity name](#Entityname),
[Geometrical information](#Geometricalinformation),
[Geometrical information specification](#Geometricalinformationspecification),
[IDS data definition](#IDSdatadefinition),
[IDS facet definition](#IDSfacetdefinition),
[IDS facet parameter](#IDSfacetparameter),
[IDS requirement type](#IDSrequirementtype),
[IFC data type](#IFCdatatype),
[Identification](#Identification),
[Identifier](#Identifier),
[Identifier type](#Identifiertype),
[Information](#Information),
[Information delivery milestone](#Informationdeliverymilestone),
[Location](#Location),
[Material](#Material),
[Ontology data definition](#Ontologydatadefinition),
[Parametric behaviour](#Parametricbehaviour),
[Predefined type](#Predefinedtype),
[Property](#Property),
[Property name](#Propertyname),
[Property set name](#Propertysetname),
[Purpose](#Purpose),
[Receiving actor](#Receivingactor),
[Restriction type](#Restrictiontype),
[Sending actor](#Sendingactor),
[Specification per Object Type](#SpecificationperObjectType),
[Value](#Value),
### Actor
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Actor`
Description | <p>Actor is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:SendingActor](Sendingactor) (c)<br />[loin:ReceivingActor](Receivingactor) (c)<br />
In domain of |[loin:isRelatedToContainerParty](isrelatedtocontainerparty)<br />[loin:hasAgent](hasagent) (op)<br />
### Alphanumerical information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#AlphanumericalInformation`
Description | <p>Alphanumerical information is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:Information](Information) (c)<br />
Restrictions |[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp) **exactly** 1<br />
In domain of |[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp)<br />[loin:hasIdentification](hasidentification) (op)<br />[loin:hasInformationContent](hasalphanumericalinformatoncontent) (op)<br />
In range of |[loin:hasAlphanumericalInformation](hasalphanumericalinformation) (op)<br />
### Appearance
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Appearance`
Description | <p>Appearance as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
### Breakdown structure
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#BreakdownStructure`
Description | <p>Breakdown structure is a term for positioning the object in a structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasIdentifier](hasidentifier) (op) **exactly** 1<br />
In domain of |[loin:hasIdentifier](hasidentifier) (op)<br />[loin:hasBreakdownStructureType](hasbreakdownstructuretype) (op)<br />
In range of |[loin:hasBreakdownStructure](hasbreakdownstructure) (op)<br />
### Breakdown structure type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#BreakdownStructureType`
Description | <p>Breakdown structure type is a term to specify the structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[loin:hasBreakdownStructureType](hasbreakdownstructuretype) (op)<br />
### Detail
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Detail`
Description | <p>Detail as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
### Dimensionality
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Dimensionality`
Description | <p>Dimensionality as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
### Document
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Document`
Description | <p>Document is a term for specifying the documentation of information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[icdd4loin:isRelatedToContainerDocument](https://w3id.org/loin/v2/icdd#isRelatedToContainerDocument) (op) **max** 1<br />[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentContent](Documentcontent) (c)<br />[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentPurpose](Documentpurpose) (c)<br />[icdd4loin:isRelatedToContainerLinkset](https://w3id.org/loin/v2/icdd#isRelatedToContainerLinkset) (op) **max** 1<br />[loin:belongsToInformationContent](belongstoinformationcontent) (op) **max** 1<br />[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentFormat](Documentformat) (c)<br />
In domain of |[loin:hasDocumentSpecification](hasdocumentatonspecification) (op)<br />[icdd4loin:isRelatedToContainerLinkset](https://w3id.org/loin/v2/icdd#isRelatedToContainerLinkset) (op)<br />[loin:belongsToInformationContent](belongstoinformationcontent) (op)<br />[icdd4loin:isRelatedToContainerDocument](https://w3id.org/loin/v2/icdd#isRelatedToContainerDocument) (op)<br />
In range of |[loin:isRelatedToLoinDocument](isrelatedtoLoindocument) (op)<br />
### Document content
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#DocumentContent`
Description | <p>Document specification for content for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:DocumentSpecification](Documentspecification) (c)<br />
### Document format
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#DocumentFormat`
Description | <p>Document specification for format for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:DocumentSpecification](Documentspecification) (c)<br />
### Document purpose
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#DocumentPurpose`
Description | <p>Document purpose is a extension according to BS EN 17412-1 (2020) 6.4 Document - Example 1. It specifies the use of document</p>
Super-classes |[loin:DocumentSpecification](Documentspecification) (c)<br />
### Document specification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#DocumentSpecification`
Description | <p>Additional specification of document for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:DocumentPurpose](Documentpurpose) (c)<br />[loin:DocumentContent](Documentcontent) (c)<br />[loin:DocumentFormat](Documentformat) (c)<br />
In range of |[loin:hasDocumentSpecification](hasdocumentatonspecification) (op)<br />
### Documentation
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Documentation`
Description | <p>Documentation is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:Information](Information) (c)<br />
In domain of |[loin:hasDocument](hasdocument) (op)<br />
In range of |[loin:hasDocumentation](hasdocumentation) (op)<br />
### Geometrical information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#GeometricalInformation`
Description | <p>Geometrical information is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:Information](Information) (c)<br />
Restrictions |[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Appearance](Appearance) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:ParametricBehaviour](Parametricbehaviour) (c)<br />[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp) **exactly** 1<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Detail](Detail) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Dimensionality](Dimensionality) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Location](Location) (c)<br />
In domain of |[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op)<br />
In range of |[loin:hasGeometricalInformation](hasgeometricalinformation) (op)<br />
### Geometrical information specification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#GeometrySpecification`
Description | <p>Additional specification of geometrical information for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:ParametricBehaviour](Parametricbehaviour) (c)<br />[loin:Detail](Detail) (c)<br />[loin:Location](Location) (c)<br />[loin:Appearance](Appearance) (c)<br />[loin:Dimensionality](Dimensionality) (c)<br />
In domain of |[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp)<br />
In range of |[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op)<br />
### Identification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Identification`
Description | <p>Identification is a term for positioning the object in a breakdown structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasBreakdownStructure](hasbreakdownstructure) (op) **min** 1<br />
In domain of |[loin:hasBreakdownStructure](hasbreakdownstructure) (op)<br />
In range of |[loin:hasIdentification](hasidentification) (op)<br />
### Identifier
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Identifier`
Description | <p>Identifier is used to assiging a vaule for positioning the object in a breakdown structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasIdentifierType](hasidentifiertype) (op) **exactly** 1<br />[loin:value](value) (dp) **exactly** 1<br />[loin:hasBreakdownStructure](hasbreakdownstructure) (op) **exactly** 1<br />
In domain of |[loin:hasIdentifierType](hasidentifiertype) (op)<br />
In range of |[loin:specifiedByIdentifier](specifiedbyidentifier)<br />[loin:hasIdentifier](hasidentifier) (op)<br />
### Identifier type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#IdentifierType`
Description | <p>Identifier type is used to specify the identifier in a breakdown structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In domain of |[loin:isRelatedToLinksetIdentifier](isrelatedtolinksetidentifier)<br />
In range of |[loin:hasIdentifierType](hasidentifiertype) (op)<br />
### Information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Information`
Description | <p>Proxy class for the three information specifications Alphanumerical Information, Geometrical Information, and Documentation</p>
Sub-classes |[loin:AlphanumericalInformation](Alphanumericalinformation) (c)<br />[loin:GeometricalInformation](Geometricalinformation) (c)<br />[loin:Documentation](Documentation) (c)<br />
In range of |[loin:hasInformation](hasinformation) (op)<br />
### Alphanumerical information content
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#InformationContent`
Description | <p>Alphanumerical information content is a term for specifying the alphanumerical information according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:OntologyDataDefinition](Ontologydatadefinition) (c)<br />[ids4loin:DataDefinition](https://w3id.org/loin/v2/ids#DataDefinition) (c)<br />
In domain of |[loin:specifiedByIdentifier](specifiedbyidentifier)<br />[loin:isRelatedToLoinDocument](isrelatedtoLoindocument) (op)<br />
In range of |[loin:belongsToInformationContent](belongstoinformationcontent) (op)<br />[loin:hasInformationContent](hasalphanumericalinformatoncontent) (op)<br />
### Information delivery milestone
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#InformationDeliveryMilestone`
Description | <p>Information delivery milestone is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasReceivingActor](hasreceivingactor) (op) **exactly** 1<br />[loin:hasSpecificationPerObjectType](hasspecificationperobjecttype) (op) **min** 1<br />[loin:hasPurpose](haspurpose) (op) **exactly** 1<br />[loin:hasSendingActor](hashasSendingActor) (op) **exactly** 1<br />
In domain of |[loin:hasSendingActor](hashasSendingActor) (op)<br />[loin:hasReceivingActor](hasreceivingactor) (op)<br />[loin:hasSpecificationPerObjectType](hasspecificationperobjecttype) (op)<br />[loin:hasPurpose](haspurpose) (op)<br />[icdd4loin:isRelatedToContainerDescription](https://w3id.org/loin/v2/icdd#isRelatedToContainerDescription) (op)<br />
### Location
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Location`
Description | <p>Location as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
### Ontology data definition
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#OntologyDataDefinition`
Description | <p>Ontology data definition is an extension of BS EN 17412-1 (2020). It is used to specify the alphanumerical information according to a published or customized ontology</p>
Super-classes |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Restrictions |[loin:specifiedByIdentifier](specifiedbyidentifier) **min** 1<br />
### Parametric behaviour
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#ParametricBehaviour`
Description | <p>Parametric behaviour as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
### Purpose
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Purpose`
Description | <p>Purpose is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:description](description) (dp) **exactly** 1<br />
In domain of |[icdd4loin:isRelatedToContainerDescription](https://w3id.org/loin/v2/icdd#isRelatedToContainerDescription) (op)<br />
In range of |[loin:hasPurpose](haspurpose) (op)<br />
### Receiving actor
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#ReceivingActor`
Description | <p>Receiving actor is a party for information delivery according to ISO 19650-1 (2018)</p>
Super-classes |[loin:Actor](Actor) (c)<br />
In range of |[loin:hasReceivingActor](hasreceivingactor) (op)<br />
### Sending actor
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#SendingActor`
Description | <p>Sending actor is a party for information delivery according to ISO 19650-1 (2018)</p>
Super-classes |[loin:Actor](Actor) (c)<br />
In range of |[loin:hasSendingActor](hashasSendingActor) (op)<br />
### Specification per Object Type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#SpecificationPerObjectType`
Description | <p>SpecificationPerObjectType is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasDocumentation](hasdocumentation) (op) **exactly** 1<br />[loin:hasObjectType](hasobjecttype) (op) **exactly** 1<br />[loin:hasAlphanumericalInformation](hasalphanumericalinformation) (op) **max** 1<br />[loin:hasGeometricalInformation](hasgeometricalinformation) (op) **exactly** 1<br />
In domain of |[loin:hasAlphanumericalInformation](hasalphanumericalinformation) (op)<br />[loin:hasGeometricalInformation](hasgeometricalinformation) (op)<br />[loin:hasObjectType](hasobjecttype) (op)<br />[loin:hasInformation](hasinformation) (op)<br />[loin:hasDocumentation](hasdocumentation) (op)<br />
In range of |[loin:hasSpecificationPerObjectType](hasspecificationperobjecttype) (op)<br />
### Attribute of IDS
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#Attribute`
Description | <p>Attribute is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
Restrictions |[ids4loin:hasAttributeName](https://w3id.org/loin/v2/ids#hasAttributeName) (op) **exactly** 1<br />
In domain of |[ids4loin:hasValue](https://w3id.org/loin/v2/ids#hasValue) (op)<br />[ids4loin:hasAttributeName](https://w3id.org/loin/v2/ids#hasAttributeName) (op)<br />
### Attribute name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#AttributeName`
Description | <p>Attribute name must be a valid attribute name from the IFC schema according to the definition of IDS developed by buildingSMART International. Example AttributeName = "Description"</p>
Super-classes |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Restrictions |[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op) **exactly** 1<br />[ids4loin:restrictionFormulation](https://w3id.org/loin/v2/ids#restrictionFormulation) (dp) **exactly** 1<br />
In range of |[ids4loin:hasAttributeName](https://w3id.org/loin/v2/ids#hasAttributeName) (op)<br />
### Classification of IDS
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#Classification`
Description | <p>Classification is is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International. In this ontology, it is defined as an equivalent class of Indentification according to BS EN 17412-1</p>
Super-classes |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
### IDS data definition
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#DataDefinition`
Description | <p>IDS data definition is used to specify the alphanumerical information according to Information Delivery Specification (IDS) developed by buildingSMART International</p>
Super-classes |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Restrictions |[ids4loin:hasApplicability](https://w3id.org/loin/v2/ids#hasApplicability) (op) **min** 1<br />[ids4loin:hasRequirement](https://w3id.org/loin/v2/ids#hasRequirement) (op) **min** 1<br />[loin:description](description) (dp) **exactly** 1<br />[ids4loin:hasApplicability](https://w3id.org/loin/v2/ids#hasApplicability) (op) **some** [ids4loin:Entity](https://w3id.org/loin/v2/ids#Entity) (c)<br />
In domain of |[ids4loin:hasApplicability](https://w3id.org/loin/v2/ids#hasApplicability) (op)<br />[ids4loin:hasRequirement](https://w3id.org/loin/v2/ids#hasRequirement) (op)<br />
### Entity
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#Entity`
Description | <p>Entity is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
Restrictions |[ids4loin:hasEntityName](https://w3id.org/loin/v2/ids#hasEntityName) (op) **exactly** 1<br />
In domain of |[ids4loin:hasPredefinedType](https://w3id.org/loin/v2/ids#hasPredefinedType) (op)<br />[ids4loin:hasEntityName](https://w3id.org/loin/v2/ids#hasEntityName) (op)<br />
### Entity name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#EntityName`
Description | <p>Entity name must be a valid IFC class from the IFC schema according to IDS developed by buildingSMART International. Example EntityName = "IFCWALL"</p>
Super-classes |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Restrictions |[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op) **exactly** 1<br />[ids4loin:restrictionFormulation](https://w3id.org/loin/v2/ids#restrictionFormulation) (dp) **exactly** 1<br />
In range of |[ids4loin:hasEntityName](https://w3id.org/loin/v2/ids#hasEntityName) (op)<br />
### IDS facet definition
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#FacetDefinition`
Description | <p>IDS facet definition is used to define a facet to apply the requirement or to require the information according to IDS standard developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[ids4loin:Material](https://w3id.org/loin/v2/ids#Material) (c)<br />[ids4loin:Property](https://w3id.org/loin/v2/ids#Property) (c)<br />[ids4loin:Attribute](https://w3id.org/loin/v2/ids#Attribute) (c)<br />[ids4loin:Classification](https://w3id.org/loin/v2/ids#Classification) (c)<br />[ids4loin:Entity](https://w3id.org/loin/v2/ids#Entity) (c)<br />
In domain of |[loin:hasRequirementType](hasrequirementtype) (op)<br />
In range of |[ids4loin:hasApplicability](https://w3id.org/loin/v2/ids#hasApplicability) (op)<br />[ids4loin:hasRequirement](https://w3id.org/loin/v2/ids#hasRequirement) (op)<br />
### IDS facet parameter
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#FacetParameter`
Description | <p>IDS facet parameter is used to specify a facet definition according to IDS standard developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[ids4loin:AttributeName](https://w3id.org/loin/v2/ids#AttributeName) (c)<br />[ids4loin:PsetName](https://w3id.org/loin/v2/ids#PsetName) (c)<br />[ids4loin:PropertyName](https://w3id.org/loin/v2/ids#PropertyName) (c)<br />[ids4loin:IFCDataType](https://w3id.org/loin/v2/ids#IFCDataType) (c)<br />[ids4loin:PredefinedType](https://w3id.org/loin/v2/ids#PredefinedType) (c)<br />[ids4loin:Value](https://w3id.org/loin/v2/ids#Value) (c)<br />[ids4loin:EntityName](https://w3id.org/loin/v2/ids#EntityName) (c)<br />
In domain of |[ids4loin:restrictionFormulation](https://w3id.org/loin/v2/ids#restrictionFormulation) (dp)<br />[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op)<br />
### IFC data type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#IFCDataType`
Description | <p>IFC data type must be a valid predefined type from the IFC schema according to IDS standard developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Restrictions |[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op) **exactly** 1<br />[ids4loin:restrictionFormulation](https://w3id.org/loin/v2/ids#restrictionFormulation) (dp) **exactly** 1<br />
In range of |[ids4loin:hasIFCDataType](https://w3id.org/loin/v2/ids#hasIFCDataType) (op)<br />
### Material
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#Material`
Description | <p>Material is a facet of Information Delivery Specification(IDS), a standard developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
In domain of |[ids4loin:hasValue](https://w3id.org/loin/v2/ids#hasValue) (op)<br />
### Predefined type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#PredefinedType`
Description | <p>Predefined type must be a valid predefined type from the IFC schema, or any custom text value according to IDS standard developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Restrictions |[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op) **exactly** 1<br />[ids4loin:restrictionFormulation](https://w3id.org/loin/v2/ids#restrictionFormulation) (dp) **exactly** 1<br />
In range of |[ids4loin:hasPredefinedType](https://w3id.org/loin/v2/ids#hasPredefinedType) (op)<br />
### Property
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#Property`
Description | <p>Property is a facet of Information Delivery Specification(IDS), a standard developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
Restrictions |[ids4loin:belongsToPset](https://w3id.org/loin/v2/ids#belongsToPset) (op) **exactly** 1<br />[ids4loin:hasPropertyName](https://w3id.org/loin/v2/ids#hasPropertyName) (op) **exactly** 1<br />[ids4loin:hasIFCDataType](https://w3id.org/loin/v2/ids#hasIFCDataType) (op) **exactly** 1<br />
In domain of |[ids4loin:belongsToPset](https://w3id.org/loin/v2/ids#belongsToPset) (op)<br />[ids4loin:hasIFCDataType](https://w3id.org/loin/v2/ids#hasIFCDataType) (op)<br />[ids4loin:hasPropertyName](https://w3id.org/loin/v2/ids#hasPropertyName) (op)<br />[ids4loin:hasValue](https://w3id.org/loin/v2/ids#hasValue) (op)<br />
### Property name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#PropertyName`
Description | <p>Property name must be a valid name from the IFC schema, or any custom text value according to IDS stan developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Restrictions |[ids4loin:restrictionFormulation](https://w3id.org/loin/v2/ids#restrictionFormulation) (dp) **exactly** 1<br />[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op) **value** [loin:SimpleValue](https://w3id.org/loin/v2#SimpleValue) (c)<br />
In range of |[ids4loin:hasPropertyName](https://w3id.org/loin/v2/ids#hasPropertyName) (op)<br />
### Property set name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#PsetName`
Description | <p>Property set name must be a valid name from the IFC schema, or any custom text value according to IDS standard developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Restrictions |[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op) **exactly** 1<br />[ids4loin:restrictionFormulation](https://w3id.org/loin/v2/ids#restrictionFormulation) (dp) **exactly** 1<br />
In range of |[ids4loin:belongsToPset](https://w3id.org/loin/v2/ids#belongsToPset) (op)<br />
### IDS requirement type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#RequirementType`
Description | <p>IDS requirement type is used to specify a requirement, if it is optional or mandatory according to IDS standard developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[loin:hasRequirementType](hasrequirementtype) (op)<br />
### Restriction type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#RestrictionType`
Description | <p>Restriction type is used to specify the value of IDS facet parameter, that is defined in restriction formulation. The restriction types are based on IDS standard developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op)<br />
### Value
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#Value`
Description | <p>Value can be any custom value according to IDS standard developed by buildingSMART International</p>
Super-classes |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Restrictions |[ids4loin:restrictionFormulation](https://w3id.org/loin/v2/ids#restrictionFormulation) (dp) **exactly** 1<br />[ids4loin:hasRestrictionType](https://w3id.org/loin/v2/ids#hasRestrictionType) (op) **exactly** 1<br />
In range of |[ids4loin:hasValue](https://w3id.org/loin/v2/ids#hasValue) (op)<br />

## Object Properties
[belongs to information content](#belongstoinformationcontent),
[has agent](#hasagent),
[has alphanumerical information](#hasalphanumericalinformation),
[has breakdown structure](#hasbreakdownstructure),
[has breakdown structure type](#hasbreakdownstructuretype),
[has document](#hasdocument),
[has documentaton specification](#hasdocumentatonspecification),
[has documentation](#hasdocumentation),
[has geometrical information](#hasgeometricalinformation),
[has geometrical information specification](#hasgeometricalinformationspecification),
[has identification](#hasidentification),
[has identifier](#hasidentifier),
[has identifier type](#hasidentifiertype),
[has information](#hasinformation),
[has alphanumerical informaton content](#hasalphanumericalinformatoncontent),
[has object type](#hasobjecttype),
[has purpose](#haspurpose),
[has receiving actor](#hasreceivingactor),
[has reference source](#hasreferencesource),
[has requirement type](#hasrequirementtype),
[has has Sending Actor](#hashasSendingActor),
[has specification per object type](#hasspecificationperobjecttype),
[is related to Loin document](#isrelatedtoLoindocument),
[is related to container description](#isrelatedtocontainerdescription),
[is related to container document](#isrelatedtocontainerdocument),
[is related to container linkset](#isrelatedtocontainerlinkset),
[A property belongs to Property set](#ApropertybelongstoPropertyset),
[has applicability](#hasapplicability),
[has attribute name](#hasattributename),
[has entity name](#hasentityname),
[has IFC data type](#hasIFCdatatype),
[has predefined type](#haspredefinedtype),
[has property name](#haspropertyname),
[has requirement](#hasrequirement),
[has restriction type](#hasrestrictiontype),
[has value](#hasvalue),
[](belongstoinformationcontent)
### belongs to information content
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#belongsToInformationContent`
Description | Specification of document, that relates with a respective person
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
[](hasagent)
### has agent
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasAgent`
Description | Information of the information delivery actor defined by foaf ontology mit class foaf:Agent
Domain(s) |[loin:Actor](Actor) (c)<br />
[](hasalphanumericalinformation)
### has alphanumerical information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasAlphanumericalInformation`
Description | The object property relates an alphanumerical information with a LOIN object according to BS EN 17412-1 (2020)
Super-properties |[loin:hasInformation](hasinformation) (op)<br />
Domain(s) |[loin:SpecificationPerObjectType](SpecificationperObjectType) (c)<br />
Range(s) |[loin:AlphanumericalInformation](Alphanumericalinformation) (c)<br />
[](hasbreakdownstructure)
### has breakdown structure
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasBreakdownStructure`
Description | The object property relates the identification with a breakdown structure according to BS EN 17412-1 (2020)
Domain(s) |[loin:Identification](Identification) (c)<br />
Range(s) |[loin:BreakdownStructure](Breakdownstructure) (c)<br />
[](hasbreakdownstructuretype)
### has breakdown structure type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasBreakdownStructureType`
Description | The object property relates a specific type with the breakdown structure according to BS EN 17412-1 (2020)
Domain(s) |[loin:BreakdownStructure](Breakdownstructure) (c)<br />
Range(s) |[loin:BreakdownStructureType](Breakdownstructuretype) (c)<br />
[](hasdocument)
### has document
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasDocument`
Description | The object property relates a set of documents with documentation according to BS EN 17412-1 (2020)
Domain(s) |[loin:Documentation](Documentation) (c)<br />
[](hasdocumentatonspecification)
### has documentaton specification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasDocumentSpecification`
Description | The object property relates the document specifications with a document according to BS EN 17412-1 (2020)
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[loin:DocumentSpecification](Documentspecification) (c)<br />
[](hasdocumentation)
### has documentation
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasDocumentation`
Description | The object property relates the documentation with a LOIN object according to BS EN 17412-1 (2020)
Super-properties |[loin:hasInformation](hasinformation) (op)<br />
Domain(s) |[loin:SpecificationPerObjectType](SpecificationperObjectType) (c)<br />
Range(s) |[loin:Documentation](Documentation) (c)<br />
[](hasgeometricalinformation)
### has geometrical information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasGeometricalInformation`
Description | The object property relates the geometrical information with a LOIN object according to BS EN 17412-1 (2020)
Super-properties |[loin:hasInformation](hasinformation) (op)<br />
Domain(s) |[loin:SpecificationPerObjectType](SpecificationperObjectType) (c)<br />
Range(s) |[loin:GeometricalInformation](Geometricalinformation) (c)<br />
[](hasgeometricalinformationspecification)
### has geometrical information specification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasGeometrySpecification`
Description | The object property relates the specific aspects with geometrical information according to BS EN 17412-1 (2020)
Domain(s) |[loin:GeometricalInformation](Geometricalinformation) (c)<br />
Range(s) |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
[](hasidentification)
### has identification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasIdentification`
Description | The object property relates the identification of a breakdown structure with an alphanumerical information according to BS EN 17412-1 (2020)
Domain(s) |[loin:AlphanumericalInformation](Alphanumericalinformation) (c)<br />
Range(s) |[loin:Identification](Identification) (c)<br />
[](hasidentifier)
### has identifier
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasIdentifier`
Description | The object property relates a breakdown structure with its identifier according to BS EN 17412-1 (2020)
Domain(s) |[loin:BreakdownStructure](Breakdownstructure) (c)<br />
Range(s) |[loin:Identifier](Identifier) (c)<br />
[](hasidentifiertype)
### has identifier type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasIdentifierType`
Description | The object property relates an identifier of breakdown structure with a specific type according to BS EN 17412-1 (2020)
Domain(s) |[loin:Identifier](Identifier) (c)<br />
Range(s) |[loin:IdentifierType](Identifiertype) (c)<br />
[](hasinformation)
### has information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasInformation`
Description | Proxy property for the three information specification relationships
Domain(s) |[loin:SpecificationPerObjectType](SpecificationperObjectType) (c)<br />
Range(s) |[loin:Information](Information) (c)<br />
[](hasalphanumericalinformatoncontent)
### has alphanumerical informaton content
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasInformationContent`
Description | The object property relates the detailed content with alphanumerical information according to BS EN 17412-1 (2020)
Domain(s) |[loin:AlphanumericalInformation](Alphanumericalinformation) (c)<br />
Range(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
[](hasobjecttype)
### has object type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasObjectType`
Domain(s) |[loin:SpecificationPerObjectType](SpecificationperObjectType) (c)<br />
Range(s) |[dt:ConstructionObject](http://inf.bi.rub.de/ontology/dt#ConstructionObject) (c)<br />
[](haspurpose)
### has purpose
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasPurpose`
Description | The object property relates the purpose with the information delivery milestone according to BS EN 17412-1 (2020)
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:Purpose](Purpose) (c)<br />
[](hasreceivingactor)
### has receiving actor
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasReceivingActor`
Description | The object property relates the receiver actor with the information delivery milestone according to BS EN 17412-1 (2020)
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:ReceivingActor](Receivingactor) (c)<br />
[](hasreferencesource)
### has reference source
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasReferenceSource`
Domain(s) |([loin:BreakdownStructure](Breakdownstructure) (c) or [loin:OntologyDataDefinition](Ontologydatadefinition) (c))<br />
Range(s) |[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
[](hasrequirementtype)
### has requirement type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasRequirementType`
Description | relates the requirement type with the defined requirements in IDS data definition
Domain(s) |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
Range(s) |[ids4loin:RequirementType](https://w3id.org/loin/v2/ids#RequirementType) (c)<br />
[](hashasSendingActor)
### has has Sending Actor
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasSendingActor`
Description | The object property relates the sending actor with the information delivery milestone according to BS EN 17412-1 (2020)
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:SendingActor](Sendingactor) (c)<br />
[](hasspecificationperobjecttype)
### has specification per object type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasSpecificationPerObjectType`
Description | The specification per object type property relates the object type specifications with the information delivery milestone according to BS EN 17412-1 (2020)
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:SpecificationPerObjectType](SpecificationperObjectType) (c)<br />
[](isrelatedtoLoindocument)
### is related to Loin document
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#isRelatedToLoinDocument`
Description | The object property relates the alphanumerical information content with document according to BS EN 17412-1(2020)
Domain(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Range(s) |[loin:Document](Document) (c)<br />
[](isrelatedtocontainerdescription)
### is related to container description
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/icdd#isRelatedToContainerDescription`
Description | The object property is an extension with ICDD. It relates the information delivery milestone defined by BS EN 17412-1(2020) with container description
Domain(s) |[loin:Purpose](Purpose) (c)<br />[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[Container:ContainerDescription](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ContainerDescription) (c)<br />
[](isrelatedtocontainerdocument)
### is related to container document
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/icdd#isRelatedToContainerDocument`
Description | The object property is an extension with ICDD. It relates documents defined by BS EN 17412-1(2020) with container documents
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[Container:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](isrelatedtocontainerlinkset)
### is related to container linkset
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/icdd#isRelatedToContainerLinkset`
Description | The object property is an extension with ICDD. It relates ontological document defined by BS EN 17412-1(2020) with container linkset or data set
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[Container:Linkset](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Linkset) (c)<br />
[](ApropertybelongstoPropertyset)
### A property belongs to Property set
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#belongsToPset`
Description | Specification is used for facet property of IDS data definition.
Domain(s) |[ids4loin:Property](https://w3id.org/loin/v2/ids#Property) (c)<br />
Range(s) |[ids4loin:PsetName](https://w3id.org/loin/v2/ids#PsetName) (c)<br />
[](hasapplicability)
### has applicability
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasApplicability`
Description | The object property describes the applicability of a facet for the specification according to IDS definition
Domain(s) |[ids4loin:DataDefinition](https://w3id.org/loin/v2/ids#DataDefinition) (c)<br />
Range(s) |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
[](hasattributename)
### has attribute name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasAttributeName`
Description | The object property relates the attribute name with the facet attribute according to IDS definition
Domain(s) |[ids4loin:Attribute](https://w3id.org/loin/v2/ids#Attribute) (c)<br />
Range(s) |[ids4loin:AttributeName](https://w3id.org/loin/v2/ids#AttributeName) (c)<br />
[](hasentityname)
### has entity name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasEntityName`
Description | The object property relates the entity name with the facet entity according to IDS definition
Domain(s) |[ids4loin:Entity](https://w3id.org/loin/v2/ids#Entity) (c)<br />
Range(s) |[ids4loin:EntityName](https://w3id.org/loin/v2/ids#EntityName) (c)<br />
[](hasIFCdatatype)
### has IFC data type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasIFCDataType`
Description | The object property relates the IFC data type with the facet property according to IDS definition
Domain(s) |[ids4loin:Property](https://w3id.org/loin/v2/ids#Property) (c)<br />
Range(s) |[ids4loin:IFCDataType](https://w3id.org/loin/v2/ids#IFCDataType) (c)<br />
[](haspredefinedtype)
### has predefined type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasPredefinedType`
Description | The object property relates a predefined type with the facet entity according to IDS definition
Domain(s) |[ids4loin:Entity](https://w3id.org/loin/v2/ids#Entity) (c)<br />
Range(s) |[ids4loin:PredefinedType](https://w3id.org/loin/v2/ids#PredefinedType) (c)<br />
[](haspropertyname)
### has property name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasPropertyName`
Description | The object property relates a property name type with the facet property according to IDS definition
Domain(s) |[ids4loin:Property](https://w3id.org/loin/v2/ids#Property) (c)<br />
Range(s) |[ids4loin:PropertyName](https://w3id.org/loin/v2/ids#PropertyName) (c)<br />
[](hasrequirement)
### has requirement
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasRequirement`
Description | The object property relates the requirements with the IDS data definition
Domain(s) |[ids4loin:DataDefinition](https://w3id.org/loin/v2/ids#DataDefinition) (c)<br />
Range(s) |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
[](hasrestrictiontype)
### has restriction type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasRestrictionType`
Description | relates the restriction type with the facet parameter in IDS data definition
Domain(s) |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Range(s) |[ids4loin:RestrictionType](https://w3id.org/loin/v2/ids#RestrictionType) (c)<br />
[](hasvalue)
### has value
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#hasValue`
Description | relates the value with a facet in IDS data definition
Domain(s) |[ids4loin:Attribute](https://w3id.org/loin/v2/ids#Attribute) (c)<br />[ids4loin:Material](https://w3id.org/loin/v2/ids#Material) (c)<br />[ids4loin:Property](https://w3id.org/loin/v2/ids#Property) (c)<br />
Range(s) |[ids4loin:Value](https://w3id.org/loin/v2/ids#Value) (c)<br />

## Datatype Properties
[description](#description),
[requested as boolean, specifys if Geometrical information is needed according to BS EN 17412-1 (2020)](#requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)),
[value](#value),
[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters),
[](description)
### description
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#description`
Description | Description provide detail and extend of information derived by Information Delivery Specification (IDS)
Domain(s) |([loin:InformationContent](Alphanumericalinformationcontent) (c) or [loin:Purpose](Purpose) (c))<br />
[](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020))
### requested as boolean, specifys if Geometrical information is needed according to BS EN 17412-1 (2020)
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#requested`
Domain(s) |[loin:AlphanumericalInformation](Alphanumericalinformation) (c)<br />[loin:GeometricalInformation](Geometricalinformation) (c)<br />[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](value)
### value
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#value`
Description | value for general definition
[](Constrainttextformulatedforfacetparameters)
### Constraint text formulated for facet parameters
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2/ids#restrictionFormulation`
Description | Restriction formulation is for formulating facet parameter value, that is used by IDS definition.
Domain(s) |[ids4loin:FacetParameter](https://w3id.org/loin/v2/ids#FacetParameter) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Properties
[is related to container party](#isrelatedtocontainerparty),
[is related to linkset identifier](#isrelatedtolinksetidentifier),
[specified by identifier](#specifiedbyidentifier),
[](isrelatedtocontainerparty)
### is related to container party
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#isRelatedToContainerParty`
Description | The object property is an extension with ICDD. It relates the actors defined by BS EN 17412-1(2020) with container party
Domain(s) |[loin:Actor](Actor) (c)<br />
Range(s) |[Container:Party](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Party) (c)<br />
[](isrelatedtolinksetidentifier)
### is related to linkset identifier
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#isRelatedToLinksetIdentifier`
Description | The object property is an extension with ICDD. It relates the identifier type defined by BS EN 17412-1(2020) with linkset identifier
Domain(s) |[loin:IdentifierType](Identifiertype) (c)<br />
Range(s) |[Linkset:Identifier](https://standards.iso.org/iso/21597/-1/ed-1/en/Linkset#Identifier) (c)<br />
[](specifiedbyidentifier)
### specified by identifier
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#specifiedByIdentifier`
Domain(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Range(s) |[loin:Identifier](Identifier) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `https://w3id.org/loin/v2#`
* **Container**
  * `https://standards.iso.org/iso/21597/-1/ed-1/en/Container#`
* **Linkset**
  * `https://standards.iso.org/iso/21597/-1/ed-1/en/Linkset#`
* **dc**
  * `http://purl.org/dc/terms/`
* **dt**
  * `http://inf.bi.rub.de/ontology/dt#`
* **foaf**
  * `http://xmlns.com/foaf/0.1#`
* **icdd4loin**
  * `https://w3id.org/loin/v2/icdd#`
* **ids4loin**
  * `https://w3id.org/loin/v2/ids#`
* **loin**
  * `https://w3id.org/loin/v2#`
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
* **vann**
  * `http://purl.org/vocab/vann/`
* **vs**
  * `http://www.w3.org/2003/06/sw-vocab-status/ns#`
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