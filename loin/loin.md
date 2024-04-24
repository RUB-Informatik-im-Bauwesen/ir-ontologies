Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.9.3

# Level of Information Need (LOIN) Ontology

## Metadata
* **URI**
  * `https://w3id.org/loin`
* **Publisher(s)**
  * [Chair of Computing in Engineering, Ruhr University Bochum](https://www.inf.bi.rub.de)
* **Creators(s)**
  * [Liu Liu](https://orcid.org/0000-0001-5907-7609)
    [[0000-0001-5907-7609](https://orcid.org/0000-0001-5907-7609)]
    [liu.liu-m6r@rub.de](liu.liu-m6r@rub.de) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/liu_liu.html.en)
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[0000-0002-6249-243X](https://orcid.org/0000-0002-6249-243X)]
    [philipp.hagedorn-n6v@rub.de](philipp.hagedorn-n6v@rub.de) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
* **Created**
  * 2023-01-30
* **Version Information**
  * 2.0
* **Imports**
  * [https://w3id.org/dt](https://w3id.org/dt)
* **License &amp; Rights**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * &copy; 2023 by Chair of Computing in Engineering, Ruhr University Bochum
* **Source**
  * [https://github.com/RUB-Informatik-im-Bauwesen/ir-ontologies/tree/main/loin](https://github.com/RUB-Informatik-im-Bauwesen/ir-ontologies/tree/main/loin)
* **Ontology RDF**
  * RDF ([loin.ttl](turtle))
### Description
The Level of Information Need (LOIN) Ontology is defined for specifying information requirements for delivery of data in a buildings' life cycle. The LOIN ontology is based on the standard BS EN 17412-1 (2020). Furthermore, it is extended with vocabulary for connecing Information Delivery Specifications (IDS) and Information containers for linked document delivery (ICDD) as per ISO 21597-1 (2020). 

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
<li>[Actor](#Actor)</li>
<li>[Alphanumerical information](#Alphanumericalinformation)</li>
<li>[Appearance](#Appearance)</li>
<li>[Breakdown structure](#Breakdownstructure)</li>
<li>[Breakdown structure type](#Breakdownstructuretype)</li>
<li>[Detail](#Detail)</li>
<li>[Dimensionality](#Dimensionality)</li>
<li>[Document content](#Documentcontent)</li>
<li>[Document format](#Documentformat)</li>
<li>[Document purpose](#Documentpurpose)</li>
<li>[Document specification](#Documentspecification)</li>
<li>[Documentation](#Documentation)</li>
<li>[Geometrical information](#Geometricalinformation)</li>
<li>[Geometrical information specification](#Geometricalinformationspecification)</li>
<li>[Identification](#Identification)</li>
<li>[Identifier](#Identifier)</li>
<li>[Identifier type](#Identifiertype)</li>
<li>[Information](#Information)</li>
<li>[Alphanumerical information content](#Alphanumericalinformationcontent)</li>
<li>[Information delivery milestone](#Informationdeliverymilestone)</li>
<li>[Location](#Location)</li>
<li>[Ontology data definition](#Ontologydatadefinition)</li>
<li>[Parametric behaviour](#Parametricbehaviour)</li>
<li>[Purpose](#Purpose)</li>
<li>[Receiving actor](#Receivingactor)</li>
<li>[Document](#Document)</li>
<li>[Sending actor](#Sendingactor)</li>
<li>[Specification per Object Type](#SpecificationperObjectType)</li>
<li>[Attribute of IDS](#AttributeofIDS)</li>
<li>[Attribute name](#Attributename)</li>
<li>[Classification of IDS](#ClassificationofIDS)</li>
<li>[IDS data definition](#IDSdatadefinition)</li>
<li>[Entity](#Entity)</li>
<li>[Entity name](#Entityname)</li>
<li>[IDS facet definition](#IDSfacetdefinition)</li>
<li>[IDS facet parameter](#IDSfacetparameter)</li>
<li>[IFC data type](#IFCdatatype)</li>
<li>[Material](#Material)</li>
<li>[Predefined type](#Predefinedtype)</li>
<li>[Property](#Property)</li>
<li>[Property name](#Propertyname)</li>
<li>[Property set name](#Propertysetname)</li>
<li>[IDS requirement type](#IDSrequirementtype)</li>
<li>[Restriction type](#Restrictiontype)</li>
<li>[Value](#Value)</li>
### Actor
Property | Value
--- | ---
URI | `https://w3id.org/loin#Actor`
Description | Actor is a contextual aspect according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Sub-classes |[Receiving actor](#Receivingactor) (c)<br />[Sending actor](#Sendingactor) (c)<br />
In domain of |[is related to container party](#isrelatedtocontainerparty) (op)<br />[has agent](#hasagent) (op)<br />
### Alphanumerical information
Property | Value
--- | ---
URI | `https://w3id.org/loin#AlphanumericalInformation`
Description | Alphanumerical information is a term for specifying the information need according to BS EN 17412-1 (2020)
Super-classes |[Information](#Information) (c)<br />
Restrictions |[requested](#requested) (dp) **exactly** 1<br />
In domain of |[has data template](#hasdatatemplate) (op)<br />[requested](#requested) (dp)<br />[has identification](#hasidentification) (op)<br />[has alphanumerical informaton content](#hasalphanumericalinformatoncontent) (op)<br />
In range of |[has alphanumerical information](#hasalphanumericalinformation) (op)<br />
### Appearance
Property | Value
--- | ---
URI | `https://w3id.org/loin#Appearance`
Description | Appearance as a geometrical information specification for information need according to BS EN 17412-1 (2020)
Super-classes |[Geometrical information specification](#Geometricalinformationspecification) (c)<br />
Has members |[https://w3id.org/loin#real-world](https://w3id.org/loin#real-world)<br />[https://w3id.org/loin#symbolic](https://w3id.org/loin#symbolic)<br />[https://w3id.org/loin#realistic](https://w3id.org/loin#realistic)<br />
### Breakdown structure
Property | Value
--- | ---
URI | `https://w3id.org/loin#BreakdownStructure`
Description | Breakdown structure is a term for positioning the object in a structure according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[has identifier](#hasidentifier) (op) **exactly** 1<br />
In domain of |[has identifier](#hasidentifier) (op)<br />[has breakdown structure type](#hasbreakdownstructuretype) (op)<br />
In range of |[has breakdown structure](#hasbreakdownstructure) (op)<br />
### Breakdown structure type
Property | Value
--- | ---
URI | `https://w3id.org/loin#BreakdownStructureType`
Description | Breakdown structure type is a term to specify the structure according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In range of |[has breakdown structure type](#hasbreakdownstructuretype) (op)<br />
Has members |[https://w3id.org/loin#Spatial](https://w3id.org/loin#Spatial)<br />[https://w3id.org/loin#EngineeringPrinciple](https://w3id.org/loin#EngineeringPrinciple)<br />[https://w3id.org/loin#ClassificationSystem](https://w3id.org/loin#ClassificationSystem)<br />[https://w3id.org/loin#Functional](https://w3id.org/loin#Functional)<br />[https://w3id.org/loin#FederationStrategy](https://w3id.org/loin#FederationStrategy)<br />[https://w3id.org/loin#Semantic](https://w3id.org/loin#Semantic)<br />
### Detail
Property | Value
--- | ---
URI | `https://w3id.org/loin#Detail`
Description | Detail as a geometrical information specification for information need according to BS EN 17412-1 (2020)
Super-classes |[Geometrical information specification](#Geometricalinformationspecification) (c)<br />
Has members |[https://w3id.org/loin#simplified](https://w3id.org/loin#simplified)<br />[https://w3id.org/loin#detailed](https://w3id.org/loin#detailed)<br />
### Dimensionality
Property | Value
--- | ---
URI | `https://w3id.org/loin#Dimensionality`
Description | Dimensionality as a geometrical information specification for information need according to BS EN 17412-1 (2020)
Super-classes |[Geometrical information specification](#Geometricalinformationspecification) (c)<br />
Has members |[https://w3id.org/loin#two-dimensional](https://w3id.org/loin#two-dimensional)<br />[https://w3id.org/loin#one-dimensional](https://w3id.org/loin#one-dimensional)<br />[https://w3id.org/loin#zero-dimensional](https://w3id.org/loin#zero-dimensional)<br />[https://w3id.org/loin#three-dimensional](https://w3id.org/loin#three-dimensional)<br />
### Document content
Property | Value
--- | ---
URI | `https://w3id.org/loin#DocumentContent`
Description | Document specification for content for information need according to BS EN 17412-1 (2020)
Super-classes |[Document specification](#Documentspecification) (c)<br />
Has members |[https://w3id.org/loin#Specification](https://w3id.org/loin#Specification)<br />[https://w3id.org/loin#Manual](https://w3id.org/loin#Manual)<br />[https://w3id.org/loin#Handdrawn_Sketches](https://w3id.org/loin#Handdrawn_Sketches)<br />[https://w3id.org/loin#Hard_Copy](https://w3id.org/loin#Hard_Copy)<br />[https://w3id.org/loin#Signed_Document](https://w3id.org/loin#Signed_Document)<br />[https://w3id.org/loin#Photograph](https://w3id.org/loin#Photograph)<br />[https://w3id.org/loin#Report](https://w3id.org/loin#Report)<br />
### Document format
Property | Value
--- | ---
URI | `https://w3id.org/loin#DocumentFormat`
Description | Document specification for format for information need according to BS EN 17412-1 (2020)
Super-classes |[Document specification](#Documentspecification) (c)<br />
### Document purpose
Property | Value
--- | ---
URI | `https://w3id.org/loin#DocumentPurpose`
Description | Document purpose is a extension according to BS EN 17412-1 (2020) 6.4 Document - Example 1. It specifies the use of document
Super-classes |[Document specification](#Documentspecification) (c)<br />
Has members |[https://w3id.org/loin#Required_with_Supplement](https://w3id.org/loin#Required_with_Supplement)<br />[https://w3id.org/loin#Used_As_Template](https://w3id.org/loin#Used_As_Template)<br />[https://w3id.org/loin#Required_For_Approval](https://w3id.org/loin#Required_For_Approval)<br />[https://w3id.org/loin#Provided_As_Information](https://w3id.org/loin#Provided_As_Information)<br />
### Document specification
Property | Value
--- | ---
URI | `https://w3id.org/loin#DocumentSpecification`
Description | Additional specification of document for information need according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Sub-classes |[Document purpose](#Documentpurpose) (c)<br />[Document content](#Documentcontent) (c)<br />[Document format](#Documentformat) (c)<br />
In range of |[has documentaton specification](#hasdocumentatonspecification) (op)<br />
### Documentation
Property | Value
--- | ---
URI | `https://w3id.org/loin#Documentation`
Description | Documentation is a term for specifying the information need according to BS EN 17412-1 (2020)
Super-classes |[Information](#Information) (c)<br />
Restrictions |[has document](#hasdocument) (op) **some** [Document](#Document) (c)<br />
In domain of |[has document](#hasdocument) (op)<br />
In range of |[has documentation](#hasdocumentation) (op)<br />
### Geometrical information
Property | Value
--- | ---
URI | `https://w3id.org/loin#GeometricalInformation`
Description | Geometrical information is a term for specifying the information need according to BS EN 17412-1 (2020)
Super-classes |[Information](#Information) (c)<br />
Restrictions |[has geometrical information specification](#hasgeometricalinformationspecification) (op) **some** [Detail](#Detail) (c)<br />[has geometrical information specification](#hasgeometricalinformationspecification) (op) **some** [Location](#Location) (c)<br />[has geometrical information specification](#hasgeometricalinformationspecification) (op) **some** [Parametric behaviour](#Parametricbehaviour) (c)<br />[has geometrical information specification](#hasgeometricalinformationspecification) (op) **some** [Appearance](#Appearance) (c)<br />[requested](#requested) (dp) **exactly** 1<br />[has geometrical information specification](#hasgeometricalinformationspecification) (op) **some** [Dimensionality](#Dimensionality) (c)<br />
In domain of |[has geometrical information specification](#hasgeometricalinformationspecification) (op)<br />[requested](#requested) (dp)<br />
In range of |[has geometrical information](#hasgeometricalinformation) (op)<br />
Has members |[https://w3id.org/loin#NotRequested](https://w3id.org/loin#NotRequested)<br />
### Geometrical information specification
Property | Value
--- | ---
URI | `https://w3id.org/loin#GeometrySpecification`
Description | Additional specification of geometrical information for information need according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Sub-classes |[Appearance](#Appearance) (c)<br />[Location](#Location) (c)<br />[Dimensionality](#Dimensionality) (c)<br />[Detail](#Detail) (c)<br />[Parametric behaviour](#Parametricbehaviour) (c)<br />
In domain of |[requested](#requested) (dp)<br />
In range of |[has geometrical information specification](#hasgeometricalinformationspecification) (op)<br />
### Identification
Property | Value
--- | ---
URI | `https://w3id.org/loin#Identification`
Description | Identification is a term for positioning the object in a breakdown structure according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[has breakdown structure](#hasbreakdownstructure) (op) **min** 1<br />
In domain of |[has breakdown structure](#hasbreakdownstructure) (op)<br />
In range of |[has identification](#hasidentification) (op)<br />
### Identifier
Property | Value
--- | ---
URI | `https://w3id.org/loin#Identifier`
Description | Identifier is used to assiging a vaule for positioning the object in a breakdown structure according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[has identifier type](#hasidentifiertype) (op) **exactly** 1<br />[has breakdown structure](#hasbreakdownstructure) (op) **exactly** 1<br />[value](#value) (dp) **exactly** 1<br />
In domain of |[has identifier type](#hasidentifiertype) (op)<br />
In range of |[has identifier](#hasidentifier) (op)<br />[specified by identifier](#specifiedbyidentifier) (op)<br />
### Identifier type
Property | Value
--- | ---
URI | `https://w3id.org/loin#IdentifierType`
Description | Identifier type is used to specify the identifier in a breakdown structure according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
In domain of |[is related to linkset identifier](#isrelatedtolinksetidentifier) (op)<br />
In range of |[has identifier type](#hasidentifiertype) (op)<br />
Has members |[https://w3id.org/loin#ReferenceOfStructure](https://w3id.org/loin#ReferenceOfStructure)<br />[https://w3id.org/loin#Index](https://w3id.org/loin#Index)<br />[https://w3id.org/loin#Codification](https://w3id.org/loin#Codification)<br />[https://w3id.org/loin#Name](https://w3id.org/loin#Name)<br />[https://w3id.org/loin#Numbering](https://w3id.org/loin#Numbering)<br />[https://w3id.org/loin#TypeName](https://w3id.org/loin#TypeName)<br />
### Information
Property | Value
--- | ---
URI | `https://w3id.org/loin#Information`
Description | Proxy class for the three information specifications Alphanumerical Information, Geometrical Information, and Documentation
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Sub-classes |[Documentation](#Documentation) (c)<br />[Geometrical information](#Geometricalinformation) (c)<br />[Alphanumerical information](#Alphanumericalinformation) (c)<br />
In range of |[has information](#hasinformation) (op)<br />
### Alphanumerical information content
Property | Value
--- | ---
URI | `https://w3id.org/loin#InformationContent`
Description | Alphanumerical information content is a term for specifying the alphanumerical information according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Sub-classes |[IDS data definition](#IDSdatadefinition) (c)<br />[Ontology data definition](#Ontologydatadefinition) (c)<br />
In domain of |[is related to Loin document](#isrelatedtoLoindocument) (op)<br />[specified by identifier](#specifiedbyidentifier) (op)<br />
In range of |[has alphanumerical informaton content](#hasalphanumericalinformatoncontent) (op)<br />[belongs to information content](#belongstoinformationcontent) (op)<br />
### Information delivery milestone
Property | Value
--- | ---
URI | `https://w3id.org/loin#InformationDeliveryMilestone`
Description | Information delivery milestone is a contextual aspect according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[has specification per object type](#hasspecificationperobjecttype) (op) **min** 1<br />[has receiving actor](#hasreceivingactor) (op) **exactly** 1<br />[has purpose](#haspurpose) (op) **exactly** 1<br />[has has Sending Actor](#hashasSendingActor) (op) **exactly** 1<br />
In domain of |[is related to container description](#isrelatedtocontainerdescription) (op)<br />[has receiving actor](#hasreceivingactor) (op)<br />[has has Sending Actor](#hashasSendingActor) (op)<br />[has purpose](#haspurpose) (op)<br />[has specification per object type](#hasspecificationperobjecttype) (op)<br />
Has members |[https://w3id.org/loin#detailedDesign](https://w3id.org/loin#detailedDesign)<br />[https://w3id.org/loin#preliminaryDesign](https://w3id.org/loin#preliminaryDesign)<br />[https://w3id.org/loin#finalDesign](https://w3id.org/loin#finalDesign)<br />
### Location
Property | Value
--- | ---
URI | `https://w3id.org/loin#Location`
Description | Location as a geometrical information specification for information need according to BS EN 17412-1 (2020)
Super-classes |[Geometrical information specification](#Geometricalinformationspecification) (c)<br />
Has members |[https://w3id.org/loin#relative](https://w3id.org/loin#relative)<br />[https://w3id.org/loin#absolute](https://w3id.org/loin#absolute)<br />
### Ontology data definition
Property | Value
--- | ---
URI | `https://w3id.org/loin#OntologyDataDefinition`
Description | Ontology data definition is an extension of BS EN 17412-1 (2020). It is used to specify the alphanumerical information according to a published or customized ontology
Super-classes |[Alphanumerical information content](#Alphanumericalinformationcontent) (c)<br />
Restrictions |[specified by identifier](#specifiedbyidentifier) (op) **min** 1<br />
### Parametric behaviour
Property | Value
--- | ---
URI | `https://w3id.org/loin#ParametricBehaviour`
Description | Parametric behaviour as a geometrical information specification for information need according to BS EN 17412-1 (2020)
Super-classes |[Geometrical information specification](#Geometricalinformationspecification) (c)<br />
Has members |[https://w3id.org/loin#explicit](https://w3id.org/loin#explicit)<br />[https://w3id.org/loin#parametric](https://w3id.org/loin#parametric)<br />[https://w3id.org/loin#constructive](https://w3id.org/loin#constructive)<br />
### Purpose
Property | Value
--- | ---
URI | `https://w3id.org/loin#Purpose`
Description | Purpose is a contextual aspect according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[description](#description) (dp) **exactly** 1<br />
In domain of |[is related to container description](#isrelatedtocontainerdescription) (op)<br />
In range of |[has purpose](#haspurpose) (op)<br />
Has members |[https://w3id.org/loin#costEstimation](https://w3id.org/loin#costEstimation)<br />[https://w3id.org/loin#coordination](https://w3id.org/loin#coordination)<br />[https://w3id.org/loin#structuralAnalysis](https://w3id.org/loin#structuralAnalysis)<br />[https://w3id.org/loin#visualization](https://w3id.org/loin#visualization)<br />[https://w3id.org/loin#fireSmokeSimulation](https://w3id.org/loin#fireSmokeSimulation)<br />
### Receiving actor
Property | Value
--- | ---
URI | `https://w3id.org/loin#ReceivingActor`
Description | Receiving actor is a party for information delivery according to ISO 19650-1 (2018)
Super-classes |[Actor](#Actor) (c)<br />
In range of |[has receiving actor](#hasreceivingactor) (op)<br />
### Document
Property | Value
--- | ---
URI | `https://w3id.org/loin#RequiredDocument`
Description | Document is a term for specifying the documentation of information need according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[has documentaton specification](#hasdocumentatonspecification) (op) **some** [Document content](#Documentcontent) (c)<br />[belongs to information content](#belongstoinformationcontent) (op) **max** 1<br />[is related to container linkset](#isrelatedtocontainerlinkset) (op) **max** 1<br />[has documentaton specification](#hasdocumentatonspecification) (op) **some** [Document format](#Documentformat) (c)<br />[has documentaton specification](#hasdocumentatonspecification) (op) **some** [Document purpose](#Documentpurpose) (c)<br />[is related to container document](#isrelatedtocontainerdocument) (op) **max** 1<br />
In domain of |[belongs to information content](#belongstoinformationcontent) (op)<br />[is related to container document](#isrelatedtocontainerdocument) (op)<br />[is related to container linkset](#isrelatedtocontainerlinkset) (op)<br />[has documentaton specification](#hasdocumentatonspecification) (op)<br />
In range of |[has document](#hasdocument) (op)<br />[is related to Loin document](#isrelatedtoLoindocument) (op)<br />
### Sending actor
Property | Value
--- | ---
URI | `https://w3id.org/loin#SendingActor`
Description | Sending actor is a party for information delivery according to ISO 19650-1 (2018)
Super-classes |[Actor](#Actor) (c)<br />
In range of |[has has Sending Actor](#hashasSendingActor) (op)<br />
### Specification per Object Type
Property | Value
--- | ---
URI | `https://w3id.org/loin#SpecificationPerObjectType`
Description | SpecificationPerObjectType is a contextual aspect according to BS EN 17412-1 (2020)
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[has geometrical information](#hasgeometricalinformation) (op) **exactly** 1<br />[has alphanumerical information](#hasalphanumericalinformation) (op) **max** 1<br />[has object type](#hasobjecttype) (op) **exactly** 1<br />[has documentation](#hasdocumentation) (op) **exactly** 1<br />
In domain of |[has object type](#hasobjecttype) (op)<br />[has documentation](#hasdocumentation) (op)<br />[has geometrical information](#hasgeometricalinformation) (op)<br />[has information](#hasinformation) (op)<br />[has alphanumerical information](#hasalphanumericalinformation) (op)<br />
In range of |[has specification per object type](#hasspecificationperobjecttype) (op)<br />
### Attribute of IDS
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#Attribute`
Description | Attribute is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International
Super-classes |[IDS facet definition](#IDSfacetdefinition) (c)<br />
Restrictions |[has attribute name](#hasattributename) (op) **exactly** 1<br />
In domain of |[has value](#hasvalue) (op)<br />[has attribute name](#hasattributename) (op)<br />
### Attribute name
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#AttributeName`
Description | Attribute name must be a valid attribute name from the IFC schema according to the definition of IDS developed by buildingSMART International. Example AttributeName = "Description"
Super-classes |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Restrictions |[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />[has restriction type](#hasrestrictiontype) (op) **exactly** 1<br />
In range of |[has attribute name](#hasattributename) (op)<br />
### Classification of IDS
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#Classification`
Description | Classification is is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International. In this ontology, it is defined as an equivalent class of Indentification according to BS EN 17412-1
Super-classes |[IDS facet definition](#IDSfacetdefinition) (c)<br />
### IDS data definition
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#DataDefinition`
Description | IDS data definition is used to specify the alphanumerical information according to Information Delivery Specification (IDS) developed by buildingSMART International
Super-classes |[Alphanumerical information content](#Alphanumericalinformationcontent) (c)<br />
Restrictions |[description](#description) (dp) **exactly** 1<br />[has requirement](#hasrequirement) (op) **min** 1<br />[has applicability](#hasapplicability) (op) **min** 1<br />[has applicability](#hasapplicability) (op) **some** [Entity](#Entity) (c)<br />
In domain of |[has applicability](#hasapplicability) (op)<br />[has requirement](#hasrequirement) (op)<br />
### Entity
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#Entity`
Description | Entity is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International
Super-classes |[IDS facet definition](#IDSfacetdefinition) (c)<br />
Restrictions |[has entity name](#hasentityname) (op) **exactly** 1<br />
In domain of |[has entity name](#hasentityname) (op)<br />[has predefined type](#haspredefinedtype) (op)<br />
### Entity name
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#EntityName`
Description | Entity name must be a valid IFC class from the IFC schema according to IDS developed by buildingSMART International. Example EntityName = "IFCWALL"
Super-classes |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Restrictions |[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />[has restriction type](#hasrestrictiontype) (op) **exactly** 1<br />
In range of |[has entity name](#hasentityname) (op)<br />
### IDS facet definition
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#FacetDefinition`
Description | IDS facet definition is used to define a facet to apply the requirement or to require the information according to IDS standard developed by buildingSMART International
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[Property](#Property) (c)<br />[Attribute of IDS](#AttributeofIDS) (c)<br />[Material](#Material) (c)<br />[Entity](#Entity) (c)<br />[Classification of IDS](#ClassificationofIDS) (c)<br />
In domain of |[has requirement type](#hasrequirementtype) (op)<br />
In range of |[has requirement](#hasrequirement) (op)<br />[has applicability](#hasapplicability) (op)<br />
### IDS facet parameter
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#FacetParameter`
Description | IDS facet parameter is used to specify a facet definition according to IDS standard developed by buildingSMART International
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[Property name](#Propertyname) (c)<br />[Property set name](#Propertysetname) (c)<br />[Predefined type](#Predefinedtype) (c)<br />[Entity name](#Entityname) (c)<br />[Value](#Value) (c)<br />[IFC data type](#IFCdatatype) (c)<br />[Attribute name](#Attributename) (c)<br />
In domain of |[has restriction type](#hasrestrictiontype) (op)<br />[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters) (dp)<br />
### IFC data type
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#IFCDataType`
Description | IFC data type must be a valid predefined type from the IFC schema according to IDS standard developed by buildingSMART International
Super-classes |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Restrictions |[has restriction type](#hasrestrictiontype) (op) **exactly** 1<br />[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />
In range of |[has IFC data type](#hasIFCdatatype) (op)<br />
### Material
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#Material`
Description | Material is a facet of Information Delivery Specification(IDS), a standard developed by buildingSMART International
Super-classes |[IDS facet definition](#IDSfacetdefinition) (c)<br />
In domain of |[has value](#hasvalue) (op)<br />
### Predefined type
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#PredefinedType`
Description | Predefined type must be a valid predefined type from the IFC schema, or any custom text value according to IDS standard developed by buildingSMART International
Super-classes |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Restrictions |[has restriction type](#hasrestrictiontype) (op) **exactly** 1<br />[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />
In range of |[has predefined type](#haspredefinedtype) (op)<br />
### Property
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#Property`
Description | Property is a facet of Information Delivery Specification(IDS), a standard developed by buildingSMART International
Super-classes |[IDS facet definition](#IDSfacetdefinition) (c)<br />
Restrictions |[A property belongs to Property set](#ApropertybelongstoPropertyset) (op) **exactly** 1<br />[has IFC data type](#hasIFCdatatype) (op) **exactly** 1<br />[has property name](#haspropertyname) (op) **exactly** 1<br />
In domain of |[has value](#hasvalue) (op)<br />[A property belongs to Property set](#ApropertybelongstoPropertyset) (op)<br />[has property name](#haspropertyname) (op)<br />[has IFC data type](#hasIFCdatatype) (op)<br />
### Property name
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#PropertyName`
Description | Property name must be a valid name from the IFC schema, or any custom text value according to IDS stan developed by buildingSMART International
Super-classes |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Restrictions |[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />[has restriction type](#hasrestrictiontype) (op) **value** [https://w3id.org/loin#SimpleValue](https://w3id.org/loin#SimpleValue) (c)<br />
In range of |[has property name](#haspropertyname) (op)<br />
### Property set name
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#PsetName`
Description | Property set name must be a valid name from the IFC schema, or any custom text value according to IDS standard developed by buildingSMART International
Super-classes |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Restrictions |[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />[has restriction type](#hasrestrictiontype) (op) **exactly** 1<br />
In range of |[A property belongs to Property set](#ApropertybelongstoPropertyset) (op)<br />
### IDS requirement type
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#RequirementType`
Description | IDS requirement type is used to specify a requirement, if it is optional or mandatory according to IDS standard developed by buildingSMART International
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[has requirement type](#hasrequirementtype) (op)<br />
### Restriction type
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#RestrictionType`
Description | Restriction type is used to specify the value of IDS facet parameter, that is defined in restriction formulation. The restriction types are based on IDS standard developed by buildingSMART International
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[has restriction type](#hasrestrictiontype) (op)<br />
Has members |[https://w3id.org/loin#SimpleValue](https://w3id.org/loin#SimpleValue)<br />[https://w3id.org/loin#Bounds](https://w3id.org/loin#Bounds)<br />[https://w3id.org/loin#Length](https://w3id.org/loin#Length)<br />[https://w3id.org/loin#Pattern](https://w3id.org/loin#Pattern)<br />[https://w3id.org/loin#Enumeration](https://w3id.org/loin#Enumeration)<br />
### Value
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#Value`
Description | Value can be any custom value according to IDS standard developed by buildingSMART International
Super-classes |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Restrictions |[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />[has restriction type](#hasrestrictiontype) (op) **exactly** 1<br />
In range of |[has value](#hasvalue) (op)<br />

## Object Properties
[belongs to information content](#belongstoinformationcontent),
[has agent](#hasagent),
[has alphanumerical information](#hasalphanumericalinformation),
[has breakdown structure](#hasbreakdownstructure),
[has breakdown structure type](#hasbreakdownstructuretype),
[has data template](#hasdatatemplate),
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
[specified by identifier](#specifiedbyidentifier),
[is related to container description](#isrelatedtocontainerdescription),
[is related to container document](#isrelatedtocontainerdocument),
[is related to container linkset](#isrelatedtocontainerlinkset),
[is related to container party](#isrelatedtocontainerparty),
[is related to linkset identifier](#isrelatedtolinksetidentifier),
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
URI | `https://w3id.org/loin#belongsToInformationContent`
Description | Specification of document, that relates with a respective person
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Document](#Document) (c)<br />
Range(s) |[https://w3id.org/loin#InformationContent](https://w3id.org/loin#InformationContent) (c)<br />
[](hasagent)
### has agent
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasAgent`
Description | Information of the information delivery actor defined by foaf ontology mit class foaf:Agent
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Actor](#Actor) (c)<br />
[](hasalphanumericalinformation)
### has alphanumerical information
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasAlphanumericalInformation`
Description | The object property relates an alphanumerical information with a LOIN object according to BS EN 17412-1 (2020)
Super-properties |[has information](#hasinformation) (op)<br />
Domain(s) |[Specification per Object Type](#SpecificationperObjectType) (c)<br />
Range(s) |[https://w3id.org/loin#AlphanumericalInformation](https://w3id.org/loin#AlphanumericalInformation) (c)<br />
[](hasbreakdownstructure)
### has breakdown structure
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasBreakdownStructure`
Description | The object property relates the identification with a breakdown structure according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Identification](#Identification) (c)<br />
Range(s) |[https://w3id.org/loin#BreakdownStructure](https://w3id.org/loin#BreakdownStructure) (c)<br />
[](hasbreakdownstructuretype)
### has breakdown structure type
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasBreakdownStructureType`
Description | The object property relates a specific type with the breakdown structure according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Breakdown structure](#Breakdownstructure) (c)<br />
Range(s) |[https://w3id.org/loin#BreakdownStructureType](https://w3id.org/loin#BreakdownStructureType) (c)<br />
[](hasdatatemplate)
### has data template
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasDataTemplate`
Super-properties |[has alphanumerical information](#hasalphanumericalinformation) (op)<br />
Domain(s) |[Alphanumerical information](#Alphanumericalinformation) (c)<br />
Range(s) |[dt:DataTemplate](https://w3id.org/dt#DataTemplate) (c)<br />
[](hasdocument)
### has document
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasDocument`
Description | The object property relates a set of documents with documentation according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Documentation](#Documentation) (c)<br />
Range(s) |[https://w3id.org/loin#RequiredDocument](https://w3id.org/loin#RequiredDocument) (c)<br />
[](hasdocumentatonspecification)
### has documentaton specification
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasDocumentSpecification`
Description | The object property relates the document specifications with a document according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Document](#Document) (c)<br />
Range(s) |[https://w3id.org/loin#DocumentSpecification](https://w3id.org/loin#DocumentSpecification) (c)<br />
[](hasdocumentation)
### has documentation
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasDocumentation`
Description | The object property relates the documentation with a LOIN object according to BS EN 17412-1 (2020)
Super-properties |[has information](#hasinformation) (op)<br />
Domain(s) |[Specification per Object Type](#SpecificationperObjectType) (c)<br />
Range(s) |[https://w3id.org/loin#Documentation](https://w3id.org/loin#Documentation) (c)<br />
[](hasgeometricalinformation)
### has geometrical information
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasGeometricalInformation`
Description | The object property relates the geometrical information with a LOIN object according to BS EN 17412-1 (2020)
Super-properties |[has information](#hasinformation) (op)<br />
Domain(s) |[Specification per Object Type](#SpecificationperObjectType) (c)<br />
Range(s) |[https://w3id.org/loin#GeometricalInformation](https://w3id.org/loin#GeometricalInformation) (c)<br />
[](hasgeometricalinformationspecification)
### has geometrical information specification
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasGeometrySpecification`
Description | The object property relates the specific aspects with geometrical information according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Geometrical information](#Geometricalinformation) (c)<br />
Range(s) |[https://w3id.org/loin#GeometrySpecification](https://w3id.org/loin#GeometrySpecification) (c)<br />
[](hasidentification)
### has identification
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasIdentification`
Description | The object property relates the identification of a breakdown structure with an alphanumerical information according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Alphanumerical information](#Alphanumericalinformation) (c)<br />
Range(s) |[https://w3id.org/loin#Identification](https://w3id.org/loin#Identification) (c)<br />
[](hasidentifier)
### has identifier
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasIdentifier`
Description | The object property relates a breakdown structure with its identifier according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Breakdown structure](#Breakdownstructure) (c)<br />
Range(s) |[https://w3id.org/loin#Identifier](https://w3id.org/loin#Identifier) (c)<br />
[](hasidentifiertype)
### has identifier type
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasIdentifierType`
Description | The object property relates an identifier of breakdown structure with a specific type according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Identifier](#Identifier) (c)<br />
Range(s) |[https://w3id.org/loin#IdentifierType](https://w3id.org/loin#IdentifierType) (c)<br />
[](hasinformation)
### has information
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasInformation`
Description | Proxy property for the three information specification relationships
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Specification per Object Type](#SpecificationperObjectType) (c)<br />
Range(s) |[https://w3id.org/loin#Information](https://w3id.org/loin#Information) (c)<br />
[](hasalphanumericalinformatoncontent)
### has alphanumerical informaton content
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasInformationContent`
Description | The object property relates the detailed content with alphanumerical information according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Alphanumerical information](#Alphanumericalinformation) (c)<br />
Range(s) |[https://w3id.org/loin#InformationContent](https://w3id.org/loin#InformationContent) (c)<br />
[](hasobjecttype)
### has object type
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasObjectType`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Specification per Object Type](#SpecificationperObjectType) (c)<br />
Range(s) |[dt:ConstructionObject](https://w3id.org/dt#ConstructionObject) (c)<br />
[](haspurpose)
### has purpose
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasPurpose`
Description | The object property relates the purpose with the information delivery milestone according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Information delivery milestone](#Informationdeliverymilestone) (c)<br />
Range(s) |[https://w3id.org/loin#Purpose](https://w3id.org/loin#Purpose) (c)<br />
[](hasreceivingactor)
### has receiving actor
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasReceivingActor`
Description | The object property relates the receiver actor with the information delivery milestone according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Information delivery milestone](#Informationdeliverymilestone) (c)<br />
Range(s) |[https://w3id.org/loin#ReceivingActor](https://w3id.org/loin#ReceivingActor) (c)<br />
[](hasreferencesource)
### has reference source
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasReferenceSource`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |([Breakdown structure](#Breakdownstructure) (c) or [Ontology data definition](#Ontologydatadefinition) (c))<br />
Range(s) |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI) (c)<br />
[](hasrequirementtype)
### has requirement type
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasRequirementType`
Description | relates the requirement type with the defined requirements in IDS data definition
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[IDS facet definition](#IDSfacetdefinition) (c)<br />
Range(s) |[ids4loin:RequirementType](https://w3id.org/loin/v2/ids#RequirementType) (c)<br />
[](hashasSendingActor)
### has has Sending Actor
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasSendingActor`
Description | The object property relates the sending actor with the information delivery milestone according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Information delivery milestone](#Informationdeliverymilestone) (c)<br />
Range(s) |[https://w3id.org/loin#SendingActor](https://w3id.org/loin#SendingActor) (c)<br />
[](hasspecificationperobjecttype)
### has specification per object type
Property | Value
--- | ---
URI | `https://w3id.org/loin#hasSpecificationPerObjectType`
Description | The specification per object type property relates the object type specifications with the information delivery milestone according to BS EN 17412-1 (2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Information delivery milestone](#Informationdeliverymilestone) (c)<br />
Range(s) |[https://w3id.org/loin#SpecificationPerObjectType](https://w3id.org/loin#SpecificationPerObjectType) (c)<br />
[](isrelatedtoLoindocument)
### is related to Loin document
Property | Value
--- | ---
URI | `https://w3id.org/loin#isRelatedToLoinDocument`
Description | The object property relates the alphanumerical information content with document according to BS EN 17412-1(2020)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Alphanumerical information content](#Alphanumericalinformationcontent) (c)<br />
Range(s) |[https://w3id.org/loin#RequiredDocument](https://w3id.org/loin#RequiredDocument) (c)<br />
[](specifiedbyidentifier)
### specified by identifier
Property | Value
--- | ---
URI | `https://w3id.org/loin#specifiedByIdentifier`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Alphanumerical information content](#Alphanumericalinformationcontent) (c)<br />
Range(s) |[https://w3id.org/loin#Identifier](https://w3id.org/loin#Identifier) (c)<br />
[](isrelatedtocontainerdescription)
### is related to container description
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/icdd#isRelatedToContainerDescription`
Description | The object property is an extension with ICDD. It relates the information delivery milestone defined by BS EN 17412-1(2020) with container description
Domain(s) |[Information delivery milestone](#Informationdeliverymilestone) (c)<br />[Purpose](#Purpose) (c)<br />
Range(s) |[Container:ContainerDescription](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ContainerDescription) (c)<br />
[](isrelatedtocontainerdocument)
### is related to container document
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/icdd#isRelatedToContainerDocument`
Description | The object property is an extension with ICDD. It relates documents defined by BS EN 17412-1(2020) with container documents
Domain(s) |[Document](#Document) (c)<br />
Range(s) |[Container:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](isrelatedtocontainerlinkset)
### is related to container linkset
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/icdd#isRelatedToContainerLinkset`
Description | The object property is an extension with ICDD. It relates ontological document defined by BS EN 17412-1(2020) with container linkset or data set
Domain(s) |[Document](#Document) (c)<br />
Range(s) |[Container:Linkset](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Linkset) (c)<br />
[](isrelatedtocontainerparty)
### is related to container party
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/icdd#isRelatedToContainerParty`
Description | The object property is an extension with ICDD. It relates the actors defined by BS EN 17412-1(2020) with container party
Domain(s) |[Actor](#Actor) (c)<br />
Range(s) |[Container:Party](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Party) (c)<br />
[](isrelatedtolinksetidentifier)
### is related to linkset identifier
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/icdd#isRelatedToLinksetIdentifier`
Description | The object property is an extension with ICDD. It relates the identifier type defined by BS EN 17412-1(2020) with linkset identifier
Domain(s) |[Identifier type](#Identifiertype) (c)<br />
Range(s) |[Linkset:Identifier](https://standards.iso.org/iso/21597/-1/ed-1/en/Linkset#Identifier) (c)<br />
[](ApropertybelongstoPropertyset)
### A property belongs to Property set
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#belongsToPset`
Description | Specification is used for facet property of IDS data definition.
Domain(s) |[Property](#Property) (c)<br />
Range(s) |[ids4loin:PsetName](https://w3id.org/loin/v2/ids#PsetName) (c)<br />
[](hasapplicability)
### has applicability
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasApplicability`
Description | The object property describes the applicability of a facet for the specification according to IDS definition
Domain(s) |[IDS data definition](#IDSdatadefinition) (c)<br />
Range(s) |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
[](hasattributename)
### has attribute name
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasAttributeName`
Description | The object property relates the attribute name with the facet attribute according to IDS definition
Domain(s) |[Attribute of IDS](#AttributeofIDS) (c)<br />
Range(s) |[ids4loin:AttributeName](https://w3id.org/loin/v2/ids#AttributeName) (c)<br />
[](hasentityname)
### has entity name
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasEntityName`
Description | The object property relates the entity name with the facet entity according to IDS definition
Domain(s) |[Entity](#Entity) (c)<br />
Range(s) |[ids4loin:EntityName](https://w3id.org/loin/v2/ids#EntityName) (c)<br />
[](hasIFCdatatype)
### has IFC data type
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasIFCDataType`
Description | The object property relates the IFC data type with the facet property according to IDS definition
Domain(s) |[Property](#Property) (c)<br />
Range(s) |[ids4loin:IFCDataType](https://w3id.org/loin/v2/ids#IFCDataType) (c)<br />
[](haspredefinedtype)
### has predefined type
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasPredefinedType`
Description | The object property relates a predefined type with the facet entity according to IDS definition
Domain(s) |[Entity](#Entity) (c)<br />
Range(s) |[ids4loin:PredefinedType](https://w3id.org/loin/v2/ids#PredefinedType) (c)<br />
[](haspropertyname)
### has property name
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasPropertyName`
Description | The object property relates a property name type with the facet property according to IDS definition
Domain(s) |[Property](#Property) (c)<br />
Range(s) |[ids4loin:PropertyName](https://w3id.org/loin/v2/ids#PropertyName) (c)<br />
[](hasrequirement)
### has requirement
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasRequirement`
Description | The object property relates the requirements with the IDS data definition
Domain(s) |[IDS data definition](#IDSdatadefinition) (c)<br />
Range(s) |[ids4loin:FacetDefinition](https://w3id.org/loin/v2/ids#FacetDefinition) (c)<br />
[](hasrestrictiontype)
### has restriction type
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasRestrictionType`
Description | relates the restriction type with the facet parameter in IDS data definition
Domain(s) |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Range(s) |[ids4loin:RestrictionType](https://w3id.org/loin/v2/ids#RestrictionType) (c)<br />
[](hasvalue)
### has value
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#hasValue`
Description | relates the value with a facet in IDS data definition
Domain(s) |[Property](#Property) (c)<br />[Attribute of IDS](#AttributeofIDS) (c)<br />[Material](#Material) (c)<br />
Range(s) |[ids4loin:Value](https://w3id.org/loin/v2/ids#Value) (c)<br />

## Datatype Properties
[description](#description),
[requested](#requested),
[value](#value),
[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters),
[](description)
### description
Property | Value
--- | ---
URI | `https://w3id.org/loin#description`
Description | Description provide detail and extend of information derived by Information Delivery Specification (IDS)
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |([Alphanumerical information content](#Alphanumericalinformationcontent) (c) or [Purpose](#Purpose) (c))<br />
[](requested)
### requested
Property | Value
--- | ---
URI | `https://w3id.org/loin#requested`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[Alphanumerical information](#Alphanumericalinformation) (c)<br />[Geometrical information](#Geometricalinformation) (c)<br />[Geometrical information specification](#Geometricalinformationspecification) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](value)
### value
Property | Value
--- | ---
URI | `https://w3id.org/loin#value`
Description | value for general definition
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](Constrainttextformulatedforfacetparameters)
### Constraint text formulated for facet parameters
Property | Value
--- | ---
URI | `https://w3id.org/loin/v2/ids#restrictionFormulation`
Description | Restriction formulation is for formulating facet parameter value, that is used by IDS definition.
Domain(s) |[IDS facet parameter](#IDSfacetparameter) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `https://w3id.org/loin`
* **Container**
  * `https://standards.iso.org/iso/21597/-1/ed-1/en/Container#`
* **Linkset**
  * `https://standards.iso.org/iso/21597/-1/ed-1/en/Linkset#`
* **dc**
  * `http://purl.org/dc/terms/`
* **dt**
  * `https://w3id.org/dt#`
* **foaf**
  * `http://xmlns.com/foaf/0.1#`
* **icdd4loin**
  * `https://w3id.org/loin/v2/icdd#`
* **ids4loin**
  * `https://w3id.org/loin/v2/ids#`
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