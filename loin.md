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
[Attribut of IDS](#AttributofIDS),
[Attribute name](#Attributename),
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
[Information delivery milestone](#Informationdeliverymilestone),
[Location](#Location),
[Material](#Material),
[Object](#Object),
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
[Value](#Value),
### Actor
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Actor`
Description | <p>Actor is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:SendingActor](Sendingactor) (c)<br />[loin:ReceivingActor](Receivingactor) (c)<br />
In domain of |[loin:isRelatedToContainerParty](isrelatedtocontainerparty)<br />[loin:hasAgent](hasagent) (op)<br />
### Appearance
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Appearance`
Description | <p>Appearance as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
### Attribut of IDS
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Attribute`
Description | <p>Attribut is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetdefinition) (c)<br />
Restrictions |[loin:hasAttributeName](hasattributename) (op) **exactly** 1<br />
In domain of |[loin:hasAttributeName](hasattributename) (op)<br />[loin:hasValue](hasvalue) (op)<br />
### Attribute name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#AttributeName`
Description | <p>Attribute name must be a valid attribute name from the IFC schema according to the definition of IDS developed by buildingSMART International. Example AttributeName = "Description"</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />[loin:restrictionFormulation](Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />
In range of |[loin:hasAttributeName](hasattributename) (op)<br />
### Breakdown structure
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#BreakdownStructure`
Description | <p>Breakdown structure is a term for positioning the object in a structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasIdentifier](hasidentifier) (op) **exactly** 1<br />
In domain of |[loin:hasBreakdownStructureType](hasbreakdownstructuretype) (op)<br />[loin:hasIdentifier](hasidentifier) (op)<br />
In range of |[loin:hasBreakdownStructure](hasbreakdownstructure) (op)<br />
### Breakdown structure type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#BreakdownStructureType`
Description | <p>Breakdown structure type is a term to specify the structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[loin:hasBreakdownStructureType](hasbreakdownstructuretype) (op)<br />
### Classification of IDS
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Classification`
Description | <p>Classification is is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International. In this ontology, it is defined as an equivalent class of Indentification according to BS EN 17412-1</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetdefinition) (c)<br />
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
Restrictions |[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentPurpose](Documentpurpose) (c)<br />[loin:belongsToInformationContent](belongstoinformationcontent) (op) **max** 1<br />[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentFormat](Documentformat) (c)<br />[loin:isRelatedToContainerDocument](isrelatedtocontainerdocument) (op) **max** 1<br />[loin:isRelatedToContainerLinkset](isrelatedtocontainerlinkset) (op) **max** 1<br />[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentContent](Documentcontent) (c)<br />
In domain of |[loin:hasDocumentSpecification](hasdocumentatonspecification) (op)<br />[loin:isRelatedToContainerLinkset](isrelatedtocontainerlinkset) (op)<br />[loin:belongsToInformationContent](belongstoinformationcontent) (op)<br />[loin:isRelatedToContainerDocument](isrelatedtocontainerdocument) (op)<br />
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
Sub-classes |[loin:DocumentFormat](Documentformat) (c)<br />[loin:DocumentContent](Documentcontent) (c)<br />[loin:DocumentPurpose](Documentpurpose) (c)<br />
In range of |[loin:hasDocumentSpecification](hasdocumentatonspecification) (op)<br />
### Documentation
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Documentation`
Description | <p>Documentation is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In domain of |[loin:hasDocument](hasdocument) (op)<br />
In range of |[loin:hasDocumentation](hasdocumentation) (op)<br />
### Entity
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Entity`
Description | <p>Entity is a facet of Information Delivery Specification (IDS), a standard developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetdefinition) (c)<br />
Restrictions |[loin:hasEntityName](hasentityname) (op) **exactly** 1<br />
In domain of |[loin:hasEntityName](hasentityname) (op)<br />[loin:hasPredefinedType](haspredefinedtype) (op)<br />
### Entity name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#EntityName`
Description | <p>Entity name must be a valid IFC class from the IFC schema according to IDS developed by buildingSMART International. Example EntityName = "IFCWALL"</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />[loin:restrictionFormulation](Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />
In range of |[loin:hasEntityName](hasentityname) (op)<br />
### Geometrical information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Geometry`
Description | <p>Geometrical information is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:ParametricBehaviour](Parametricbehaviour) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Location](Location) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Dimensionality](Dimensionality) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Appearance](Appearance) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Detail](Detail) (c)<br />[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp) **exactly** 1<br />
In domain of |[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op)<br />[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp)<br />
In range of |[loin:hasGeometry](hasgeometricalinformation) (op)<br />
### Geometrical information specification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#GeometrySpecification`
Description | <p>Additional specification of geometrical information for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:Appearance](Appearance) (c)<br />[loin:ParametricBehaviour](Parametricbehaviour) (c)<br />[loin:Detail](Detail) (c)<br />[loin:Dimensionality](Dimensionality) (c)<br />[loin:Location](Location) (c)<br />
In domain of |[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp)<br />
In range of |[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op)<br />
### IDS data definition
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#IDSDataDefinition`
Description | <p>IDS data definition is used to specify the alphanumerical information according to Information Delivery Specification (IDS) developed by buildingSMART International</p>
Super-classes |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Restrictions |[loin:description](description) (dp) **exactly** 1<br />[loin:hasRequirement](hasrequirement) (op) **min** 1<br />[loin:hasApplicability](hasapplicability) (op) **min** 1<br />[loin:hasApplicability](hasapplicability) (op) **some** [loin:Entity](Entity) (c)<br />
In domain of |[loin:hasRequirement](hasrequirement) (op)<br />[loin:hasApplicability](hasapplicability) (op)<br />
### IDS facet definition
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#IDSFacetDefinition`
Description | <p>IDS facet definition is used to define a facet to apply the requirement or to require the information according to IDS standard developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:Material](Material) (c)<br />[loin:Classification](ClassificationofIDS) (c)<br />[loin:Property](Property) (c)<br />[loin:Entity](Entity) (c)<br />[loin:Attribute](AttributofIDS) (c)<br />
In domain of |[loin:hasRequirementType](hasrequirementtype) (op)<br />
In range of |[loin:hasRequirement](hasrequirement) (op)<br />[loin:hasApplicability](hasapplicability) (op)<br />
### IDS facet parameter
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#IDSFacetParameter`
Description | <p>IDS facet parameter is used to specify a facet definition according to IDS standard developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:PropertyName](Propertyname) (c)<br />[loin:AttributeName](Attributename) (c)<br />[loin:PsetName](Propertysetname) (c)<br />[loin:IFCDataType](IFCdatatype) (c)<br />[loin:EntityName](Entityname) (c)<br />[loin:PredefinedType](Predefinedtype) (c)<br />[loin:Value](Value) (c)<br />
In domain of |[loin:hasRestrictionType](hasrestrictiontype) (op)<br />[loin:restrictionFormulation](Constrainttextformulatedforfacetparameters) (dp)<br />
### IDS requirement type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#IDSRequirementType`
Description | <p>IDS requirement type is used to specify a requirement, if it is optional or mandatory according to IDS standard developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[loin:hasRequirementType](hasrequirementtype) (op)<br />
### Restriction type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#IDSRestrictionType`
Description | <p>Restriction type is used to specify the value of IDS facet parameter, that is defined in restriction formulation. The restriction types are based on IDS standard developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[loin:hasRestrictionType](hasrestrictiontype) (op)<br />
### IFC data type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#IFCDataType`
Description | <p>IFC data type must be a valid predefined type from the IFC schema according to IDS standard developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />[loin:restrictionFormulation](Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />
In range of |[loin:hasIFCDataType](hasIFCdatatype) (op)<br />
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
Restrictions |[loin:value](value) (dp) **exactly** 1<br />[loin:hasBreakdownStructure](hasbreakdownstructure) (op) **exactly** 1<br />[loin:hasIdentifierType](hasidentifiertype) (op) **exactly** 1<br />
In domain of |[loin:hasIdentifierType](hasidentifiertype) (op)<br />
In range of |[loin:hasIdentifier](hasidentifier) (op)<br />[loin:specifiedByIdentifier](specifiedbyidentifier)<br />
### Identifier type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#IdentifierType`
Description | <p>Identifier type is used to specify the identifier in a breakdown structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In domain of |[loin:isRelatedToLinksetIdentifier](isrelatedtolinksetidentifier)<br />
In range of |[loin:hasIdentifierType](hasidentifiertype) (op)<br />
### Alphanumerical information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Information`
Description | <p>Alphanumerical information is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp) **exactly** 1<br />
In domain of |[loin:hasInformationContent](hasalphanumericalinformatoncontent) (op)<br />[loin:hasIdentification](hasidentification) (op)<br />[loin:requested](requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)) (dp)<br />
In range of |[loin:hasInformation](hasalphanumericalinformation) (op)<br />
### Alphanumerical information content
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#InformationContent`
Description | <p>Alphanumerical information content is a term for specifying the alphanumerical information according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:IDSDataDefinition](IDSdatadefinition) (c)<br />[loin:OntologyDataDefinition](Ontologydatadefinition) (c)<br />
In domain of |[loin:isRelatedToLoinDocument](isrelatedtoLoindocument) (op)<br />[loin:specifiedByIdentifier](specifiedbyidentifier)<br />
In range of |[loin:hasInformationContent](hasalphanumericalinformatoncontent) (op)<br />[loin:belongsToInformationContent](belongstoinformationcontent) (op)<br />
### Information delivery milestone
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#InformationDeliveryMilestone`
Description | <p>Information delivery milestone is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasPurpose](haspurpose) (op) **exactly** 1<br />[loin:hasProvider](hasprovider) (op) **exactly** 1<br />[loin:hasObject](hasobject) (op) **min** 1<br />[loin:hasReceiver](hasinformationreceiver) (op) **exactly** 1<br />
In domain of |[loin:hasObject](hasobject) (op)<br />[loin:isRelatedToContainerDescription](isrelatedtocontainerdescription) (op)<br />[loin:hasReceiver](hasinformationreceiver) (op)<br />[loin:hasProvider](hasprovider) (op)<br />[loin:hasPurpose](haspurpose) (op)<br />
### Location
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Location`
Description | <p>Location as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
### Material
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Material`
Description | <p>Material is a facet of Information Delivery Specification(IDS), a standard developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetdefinition) (c)<br />
In domain of |[loin:hasValue](hasvalue) (op)<br />
### Object
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Object`
Description | <p>Object is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasGeometry](hasgeometricalinformation) (op) **max** 1<br />[loin:hasInformation](hasalphanumericalinformation) (op) **max** 1<br />[loin:hasDocumentation](hasdocumentation) (op) **max** 1<br />
In domain of |[loin:hasDocumentation](hasdocumentation) (op)<br />[loin:hasInformation](hasalphanumericalinformation) (op)<br />[loin:hasGeometry](hasgeometricalinformation) (op)<br />
In range of |[loin:hasObject](hasobject) (op)<br />
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
### Predefined type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#PredefinedType`
Description | <p>Predefined type must be a valid predefined type from the IFC schema, or any custom text value according to IDS standard developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:restrictionFormulation](Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />
In range of |[loin:hasPredefinedType](haspredefinedtype) (op)<br />
### Property
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Property`
Description | <p>Property is a facet of Information Delivery Specification(IDS), a standard developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetdefinition) (c)<br />
Restrictions |[loin:belongsToPset](ApropertybelongstoPropertyset) (op) **exactly** 1<br />[loin:hasPropertyName](haspropertyname) (op) **exactly** 1<br />[loin:hasIFCDataType](hasIFCdatatype) (op) **exactly** 1<br />
In domain of |[loin:belongsToPset](ApropertybelongstoPropertyset) (op)<br />[loin:hasPropertyName](haspropertyname) (op)<br />[loin:hasValue](hasvalue) (op)<br />[loin:hasIFCDataType](hasIFCdatatype) (op)<br />
### Property name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#PropertyName`
Description | <p>Property name must be a valid name from the IFC schema, or any custom text value according to IDS stan developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **value** [loin:SimpleValue](https://w3id.org/loin/v2#SimpleValue) (c)<br />[loin:restrictionFormulation](Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />
In range of |[loin:hasPropertyName](haspropertyname) (op)<br />
### Property set name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#PsetName`
Description | <p>Property set name must be a valid name from the IFC schema, or any custom text value according to IDS standard developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />[loin:restrictionFormulation](Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />
In range of |[loin:belongsToPset](ApropertybelongstoPropertyset) (op)<br />
### Purpose
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Purpose`
Description | <p>Purpose is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:description](description) (dp) **exactly** 1<br />
In domain of |[loin:isRelatedToContainerDescription](isrelatedtocontainerdescription) (op)<br />
In range of |[loin:hasPurpose](haspurpose) (op)<br />
### Receiving actor
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#ReceivingActor`
Description | <p>Receiving actor is a party for information delivery according to ISO 19650-1 (2018)</p>
Super-classes |[loin:Actor](Actor) (c)<br />
In range of |[loin:hasReceiver](hasinformationreceiver) (op)<br />
### Sending actor
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#SendingActor`
Description | <p>Sending actor is a party for information delivery according to ISO 19650-1 (2018)</p>
Super-classes |[loin:Actor](Actor) (c)<br />
In range of |[loin:hasProvider](hasprovider) (op)<br />
### Value
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#Value`
Description | <p>Value can be any custom value according to IDS standard developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:restrictionFormulation](Constrainttextformulatedforfacetparameters) (dp) **exactly** 1<br />[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />
In range of |[loin:hasValue](hasvalue) (op)<br />

## Object Properties
[belongs to information content](#belongstoinformationcontent),
[A property belongs to Property set](#ApropertybelongstoPropertyset),
[has agent](#hasagent),
[has applicability](#hasapplicability),
[has attribute name](#hasattributename),
[has breakdown structure](#hasbreakdownstructure),
[has breakdown structure type](#hasbreakdownstructuretype),
[has document](#hasdocument),
[has documentaton specification](#hasdocumentatonspecification),
[has documentation](#hasdocumentation),
[has entity name](#hasentityname),
[has geometrical information](#hasgeometricalinformation),
[has geometrical information specification](#hasgeometricalinformationspecification),
[has IFC data type](#hasIFCdatatype),
[has identification](#hasidentification),
[has identifier](#hasidentifier),
[has identifier type](#hasidentifiertype),
[has alphanumerical information](#hasalphanumericalinformation),
[has alphanumerical informaton content](#hasalphanumericalinformatoncontent),
[has object](#hasobject),
[has predefined type](#haspredefinedtype),
[has property name](#haspropertyname),
[has provider](#hasprovider),
[has purpose](#haspurpose),
[has information receiver](#hasinformationreceiver),
[has reference source](#hasreferencesource),
[has requirement](#hasrequirement),
[has requirement type](#hasrequirementtype),
[has restriction type](#hasrestrictiontype),
[has value](#hasvalue),
[is related to container description](#isrelatedtocontainerdescription),
[is related to container document](#isrelatedtocontainerdocument),
[is related to container linkset](#isrelatedtocontainerlinkset),
[is related to Loin document](#isrelatedtoLoindocument),
[](belongstoinformationcontent)
### belongs to information content
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#belongsToInformationContent`
Description | Specification of document, that relates with a respective person
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
[](ApropertybelongstoPropertyset)
### A property belongs to Property set
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#belongsToPset`
Description | Specification is used for facet property of IDS data definition.
Domain(s) |[loin:Property](Property) (c)<br />
Range(s) |[loin:PsetName](Propertysetname) (c)<br />
[](hasagent)
### has agent
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasAgent`
Description | Information of the information delivery actor defined by foaf ontology mit class foaf:Agent
Domain(s) |[loin:Actor](Actor) (c)<br />
[](hasapplicability)
### has applicability
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasApplicability`
Description | The object property describes the applicability of a facet for the specification according to IDS definition
Domain(s) |[loin:IDSDataDefinition](IDSdatadefinition) (c)<br />
Range(s) |[loin:IDSFacetDefinition](IDSfacetdefinition) (c)<br />
[](hasattributename)
### has attribute name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasAttributeName`
Description | The object property relates the attribute name with the facet attribute according to IDS definition
Domain(s) |[loin:Attribute](AttributofIDS) (c)<br />
Range(s) |[loin:AttributeName](Attributename) (c)<br />
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
Domain(s) |[loin:Object](Object) (c)<br />
Range(s) |[loin:Documentation](Documentation) (c)<br />
[](hasentityname)
### has entity name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasEntityName`
Description | The object property relates the entity name with the facet entity according to IDS definition
Domain(s) |[loin:Entity](Entity) (c)<br />
Range(s) |[loin:EntityName](Entityname) (c)<br />
[](hasgeometricalinformation)
### has geometrical information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasGeometry`
Description | The object property relates the geometrical information with a LOIN object according to BS EN 17412-1 (2020)
Domain(s) |[loin:Object](Object) (c)<br />
Range(s) |[loin:Geometry](Geometricalinformation) (c)<br />
[](hasgeometricalinformationspecification)
### has geometrical information specification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasGeometrySpecification`
Description | ["Appearance", "Detail", "Dimensionality", "Location", "ParametricBehaviour"]
Domain(s) |[loin:Geometry](Geometricalinformation) (c)<br />
Range(s) |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
[](hasIFCdatatype)
### has IFC data type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasIFCDataType`
Description | The object property relates the IFC data type with the facet property according to IDS definition
Domain(s) |[loin:Property](Property) (c)<br />
Range(s) |[loin:IFCDataType](IFCdatatype) (c)<br />
[](hasidentification)
### has identification
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasIdentification`
Description | The object property relates the identification of a breakdown structure with an alphanumerical information according to BS EN 17412-1 (2020)
Domain(s) |[loin:Information](Alphanumericalinformation) (c)<br />
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
[](hasalphanumericalinformation)
### has alphanumerical information
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasInformation`
Description | The object property relates an alphanumerical information with a LOIN object according to BS EN 17412-1 (2020)
Domain(s) |[loin:Object](Object) (c)<br />
Range(s) |[loin:Information](Alphanumericalinformation) (c)<br />
[](hasalphanumericalinformatoncontent)
### has alphanumerical informaton content
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasInformationContent`
Description | The object property relates the detailed content with alphanumerical information according to BS EN 17412-1 (2020)
Domain(s) |[loin:Information](Alphanumericalinformation) (c)<br />
Range(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
[](hasobject)
### has object
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasObject`
Description | The object property relates the objects with the information delivery milestone according to BS EN 17412-1 (2020)
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:Object](Object) (c)<br />
[](haspredefinedtype)
### has predefined type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasPredefinedType`
Description | The object property relates a predefined type with the facet entity according to IDS definition
Domain(s) |[loin:Entity](Entity) (c)<br />
Range(s) |[loin:PredefinedType](Predefinedtype) (c)<br />
[](haspropertyname)
### has property name
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasPropertyName`
Description | The object property relates a property name type with the facet property according to IDS definition
Domain(s) |[loin:Property](Property) (c)<br />
Range(s) |[loin:PropertyName](Propertyname) (c)<br />
[](hasprovider)
### has provider
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasProvider`
Description | The object property relates the information provider with the information delivery milestone according to BS EN 17412-1 (2020)
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:SendingActor](Sendingactor) (c)<br />
[](haspurpose)
### has purpose
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasPurpose`
Description | The object property relates the purpose with the information delivery milestone according to BS EN 17412-1 (2020)
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:Purpose](Purpose) (c)<br />
[](hasinformationreceiver)
### has information receiver
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasReceiver`
Description | The object property relates the information receiver with the information delivery milestone according to BS EN 17412-1 (2020)
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:ReceivingActor](Receivingactor) (c)<br />
[](hasreferencesource)
### has reference source
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasReferenceSource`
Domain(s) |([loin:BreakdownStructure](Breakdownstructure) (c) or [loin:OntologyDataDefinition](Ontologydatadefinition) (c))<br />
Range(s) |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI) (c)<br />
[](hasrequirement)
### has requirement
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasRequirement`
Description | The object property relates the requirements with the IDS data definition
Domain(s) |[loin:IDSDataDefinition](IDSdatadefinition) (c)<br />
Range(s) |[loin:IDSFacetDefinition](IDSfacetdefinition) (c)<br />
[](hasrequirementtype)
### has requirement type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasRequirementType`
Description | relates the requirement type with the defined requirements in IDS data definition
Domain(s) |[loin:IDSFacetDefinition](IDSfacetdefinition) (c)<br />
Range(s) |[loin:IDSRequirementType](IDSrequirementtype) (c)<br />
[](hasrestrictiontype)
### has restriction type
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasRestrictionType`
Description | relates the restriction type with the facet parameter in IDS data definition
Domain(s) |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Range(s) |[loin:IDSRestrictionType](Restrictiontype) (c)<br />
[](hasvalue)
### has value
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#hasValue`
Description | relates the value with a facet in IDS data definition
Domain(s) |[loin:Material](Material) (c)<br />[loin:Property](Property) (c)<br />[loin:Attribute](AttributofIDS) (c)<br />
Range(s) |[loin:Value](Value) (c)<br />
[](isrelatedtocontainerdescription)
### is related to container description
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#isRelatedToContainerDescription`
Description | The object property is an extension with ICDD. It relates the information delivery milestone defined by BS EN 17412-1(2020) with container description
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />[loin:Purpose](Purpose) (c)<br />
Range(s) |[Container:ContainerDescription](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ContainerDescription) (c)<br />
[](isrelatedtocontainerdocument)
### is related to container document
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#isRelatedToContainerDocument`
Description | The object property is an extension with ICDD. It relates documents defined by BS EN 17412-1(2020) with container documents
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[Container:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](isrelatedtocontainerlinkset)
### is related to container linkset
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#isRelatedToContainerLinkset`
Description | The object property is an extension with ICDD. It relates ontological document defined by BS EN 17412-1(2020) with container linkset or data set
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[Container:Linkset](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Linkset) (c)<br />
[](isrelatedtoLoindocument)
### is related to Loin document
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#isRelatedToLoinDocument`
Description | The object property relates the alphanumerical information content with document according to BS EN 17412-1(2020)
Domain(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Range(s) |[loin:Document](Document) (c)<br />

## Datatype Properties
[description](#description),
[requested as boolean, specifys if Geometrical information is needed according to BS EN 17412-1 (2020)](#requestedasboolean,specifysifGeometricalinformationisneededaccordingtoBSEN17412-1(2020)),
[Constraint text formulated for facet parameters](#Constrainttextformulatedforfacetparameters),
[value](#value),
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
Domain(s) |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />[loin:Information](Alphanumericalinformation) (c)<br />[loin:Geometry](Geometricalinformation) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](Constrainttextformulatedforfacetparameters)
### Constraint text formulated for facet parameters
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#restrictionFormulation`
Description | Restriction formulation is for formulating facet parameter value, that is used by IDS definition.
Domain(s) |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](value)
### value
Property | Value
--- | ---
IRI | `https://w3id.org/loin/v2#value`
Description | value for general definition

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
* **foaf**
  * `http://xmlns.com/foaf/0.1#`
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