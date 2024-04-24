Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# Data Template (DT) Ontology

## Metadata
* **IRI**
  * `http://w3id.org/dt`
* **Creators(s)**
  * [Liu Liu](https://orcid.org/0000-0001-5907-7609)
    [[ORCID]](https://orcid.org/0000-0001-5907-7609)
    (<liu.liu-m6r@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/liu_liu.html.en)
  * [Marthina Mellenthin-Filardo](https://orcid.org/0000-0001-7759-7579)
    [[ORCID]](https://orcid.org/0000-0001-7759-7579)
    (<martina.mellenthin.filardo@uni-weimar.de></a>) of [Bauhaus-Universitaet Weimar](https://www.uni-weimar.de/en/civil-engineering/chairs/construction-engineering-and-management/people/martina-mellenthin-filardo-msc/)
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
  * [Sven Zentgraf](https://orcid.org/0000-0001-6058-7614)
    [[ORCID]](https://orcid.org/0000-0001-6058-7614)
    (<sven.zentgraf@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/sven_zentgraf.html.en)
* **Created**
  * 2023-12-23
* **Version Information**
  * 1.0
* **Imports**
  * [https://w3id.org/isoprops](https://w3id.org/isoprops)
  * [https://w3id.org/loin](https://w3id.org/loin)
* **License &amp; Rights**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * &copy; 2024 by Chair of Computing in Engineering, Ruhr University Bochum and Chair of Construction Management, Bauhaus Universitaet Weimar
* **Source**
  * [https://github.com/RUB-Informatik-im-Bauwesen/ir-ontologies/tree/main/dt](https://github.com/RUB-Informatik-im-Bauwesen/ir-ontologies/tree/main/dt)
* **Ontology RDF**
  * RDF ([dt.ttl](turtle))
### Description
<p>The Data Template (DT) Ontology is based on concepts and principles for creating templates from ISO 23387 and the associated XML data schema, which is currently under development. </p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[Construction object](#Constructionobject),
[Data template](#Datatemplate),
[External dictionary](#Externaldictionary),
[Library component](#Librarycomponent),
[Physical quantity](#Physicalquantity),
[Predefined value item](#Predefinedvalueitem),
[Predefined value list](#Predefinedvaluelist),
[Property](#Property),
[Reference document](#Referencedocument),
[Set of properties](#Setofproperties),
[Unit](#Unit),
### Construction object
Property | Value
--- | ---
IRI | `http://w3id.org/dt#ConstructionObject`
Description | <p>object of interest in the context of a construction process</p>
Super-classes |[dt:LibraryComponent](Librarycomponent) (c)<br />
### Data template
Property | Value
--- | ---
IRI | `http://w3id.org/dt#DataTemplate`
Description | <p>data structure used to describe the characteristics of construction objects</p>
Super-classes |[dt:LibraryComponent](Librarycomponent) (c)<br />
Restrictions |[dt:isDataTemplateFor](isdatatemplatefor) (op) **some** [https://w3id.org/loin/v2#AlphanumericalInformation](https://w3id.org/loin/v2#AlphanumericalInformation) (c)<br />[dt:hasProperty](hasproperty) (op) **some** [https://w3id.org/isoprops#Property](https://w3id.org/isoprops#Property) (c)<br />[dt:hasSetOfProperties](hassetofproperties) (op) **some** [dt:SetOfProperties](Setofproperties) (c)<br />
In domain of |[dt:hasProperty](hasproperty) (op)<br />[dt:hasSetOfProperties](hassetofproperties) (op)<br />[dt:isDataTemplateFor](isdatatemplatefor) (op)<br />
### External dictionary
Property | Value
--- | ---
IRI | `http://w3id.org/dt#ExternalDictionaryReference`
Description | <p>reference to an external dictionary, which is a centralized repository of information about data such as meaning, relationships to other data, origin, usage and format</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[dt:hasExternalDictionary](hasexternaldictionary) (op) **exactly** 1<br />[dt:hasExternalDictionaryProperty](hasexternalpropertyreference) (op) **exactly** 1<br />
In domain of |[dt:hasExternalDictionaryProperty](hasexternalpropertyreference) (op)<br />
In range of |[dt:hasExternalDictionaryReference](referencedexternaldictionary) (op)<br />
### Library component
Property | Value
--- | ---
IRI | `http://w3id.org/dt#LibraryComponent`
Description | <p>named and individually scheduled physical item and feature that might require management, such as inspection, maintenance, servicing or replacement, during the in-use phase</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[dt:hasExternalDictionary](hasexternaldictionary) (op) **some** [dt:ExternalDictionaryReference](Externaldictionary) (c)<br />[dt:hasReferenceDocument](hasreferencedocument) (op) **some** [dt:ReferenceDocument](Referencedocument) (c)<br />
Sub-classes |[dt:Property](Property) (c)<br />[dt:DataTemplate](Datatemplate) (c)<br />[dt:SetOfProperties](Setofproperties) (c)<br />[dt:Unit](Unit) (c)<br />[dt:PhysicalQuantity](Physicalquantity) (c)<br />[dt:ReferenceDocument](Referencedocument) (c)<br />[dt:ConstructionObject](Constructionobject) (c)<br />
In domain of |[dt:hasExternalDictionaryReference](referencedexternaldictionary) (op)<br />[dt:hasExternalDictionary](hasexternaldictionary) (op)<br />[dt:hasReferenceDocument](hasreferencedocument) (op)<br />
### Physical quantity
Property | Value
--- | ---
IRI | `http://w3id.org/dt#PhysicalQuantity`
Description | <p>the physical quantity of a library component</p>
Super-classes |[dt:LibraryComponent](Librarycomponent) (c)<br />
### Predefined value item
Property | Value
--- | ---
IRI | `http://w3id.org/dt#PredefinedValueItem`
Description | <p>the physical quantity of a library component</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[dt:hasIndex](Indexoftheelementintheenumeration) (dp) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />
### Predefined value list
Property | Value
--- | ---
IRI | `http://w3id.org/dt#PredefinedValuesList`
Description | <p>list of predefined values</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[dt:hasPredefinedValueItem](PredefindedValueItem@en-GB}) (op) **min** 1<br />[https://w3id.org/isoprops#hasUnit](https://w3id.org/isoprops#hasUnit) **max** 1<br />[https://w3id.org/isoprops#hasUnit](https://w3id.org/isoprops#hasUnit) **min** 0<br />
### Property
Property | Value
--- | ---
IRI | `http://w3id.org/dt#Property`
Description | <p>inherent or acquired feature of an item</p>
Super-classes |[dt:LibraryComponent](Librarycomponent) (c)<br />
Restrictions |[dt:hasPredefinedValues](PredefinedValues) (op) **min** 0<br />
### Reference document
Property | Value
--- | ---
IRI | `http://w3id.org/dt#ReferenceDocument`
Description | <p>publication that is consulted to find specific information, particularly in a technical or scientific domain</p>
Super-classes |[dt:LibraryComponent](Librarycomponent) (c)<br />
Restrictions |[dt:dateOfPublication](dateofpublication) (dp) **max** 1<br />[dt:uri](uri) (dp) **max** 1<br />[dt:author](author) (dp) **max** 1<br />[dt:ISBN](ISBN) (dp) **max** 1<br />[dt:publisher](publisher) (dp) **max** 1<br />
In range of |[dt:hasReferenceDocument](hasreferencedocument) (op)<br />
### Set of properties
Property | Value
--- | ---
IRI | `http://w3id.org/dt#SetOfProperties`
Description | <p>a set of properties that can be applied to a data template</p>
Super-classes |[dt:LibraryComponent](Librarycomponent) (c)<br />
Restrictions |[dt:hasProperty](hasproperty) (op) **min** 0<br />[dt:hasProperty](hasproperty) (op) **some** [https://w3id.org/isoprops#Property](https://w3id.org/isoprops#Property) (c)<br />[dt:hasSetOfProperties](hassetofproperties) (op) **min** 0<br />[dt:hasSetOfProperties](hassetofproperties) (op) **some** [dt:SetOfProperties](Setofproperties) (c)<br />
In domain of |[dt:hasSetOfProperties](hassetofproperties) (op)<br />
In range of |[dt:hasSetOfProperties](hassetofproperties) (op)<br />
### Unit
Property | Value
--- | ---
IRI | `http://w3id.org/dt#Unit`
Description | <p>real scalar quantity, defined and adopted by convention, with which any other quantity of the same kind can be compared to express the ratio of the second quantity to the first one as a number</p>
Super-classes |[dt:LibraryComponent](Librarycomponent) (c)<br />

## Object Properties
[has external dictionary](#hasexternaldictionary),
[has external property reference](#hasexternalpropertyreference),
[referenced external dictionary](#referencedexternaldictionary),
[Predefinded Value Item@en-GB}](#PredefindedValueItem@en-GB}),
[Predefined Values](#PredefinedValues),
[has property](#hasproperty),
[has reference document](#hasreferencedocument),
[has set of properties](#hassetofproperties),
[is data template for](#isdatatemplatefor),
[](hasexternaldictionary)
### has external dictionary
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasExternalDictionary`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:LibraryComponent](Librarycomponent) (c)<br />
[](hasexternalpropertyreference)
### has external property reference
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasExternalDictionaryProperty`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:ExternalDictionaryReference](Externaldictionary) (c)<br />
[](referencedexternaldictionary)
### referenced external dictionary
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasExternalDictionaryReference`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:LibraryComponent](Librarycomponent) (c)<br />
Range(s) |[dt:ExternalDictionaryReference](Externaldictionary) (c)<br />
[](PredefindedValueItem@en-GB})
### Predefinded Value Item@en-GB}
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasPredefinedValueItem`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](PredefinedValues)
### Predefined Values
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasPredefinedValues`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasProperty`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:DataTemplate](Datatemplate) (c)<br />
Range(s) |[https://w3id.org/isoprops#Property](https://w3id.org/isoprops#Property) (c)<br />
[](hasreferencedocument)
### has reference document
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasReferenceDocument`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:LibraryComponent](Librarycomponent) (c)<br />
Range(s) |[dt:ReferenceDocument](Referencedocument) (c)<br />
[](hassetofproperties)
### has set of properties
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasSetOfProperties`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:SetOfProperties](Setofproperties) (c)<br />[dt:DataTemplate](Datatemplate) (c)<br />
Range(s) |[dt:SetOfProperties](Setofproperties) (c)<br />
[](isdatatemplatefor)
### is data template for
Property | Value
--- | ---
IRI | `http://w3id.org/dt#isDataTemplateFor`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:DataTemplate](Datatemplate) (c)<br />
Range(s) |[https://w3id.org/loin/v2#SpecificationPerObjectType](https://w3id.org/loin/v2#SpecificationPerObjectType) (c)<br />

## Datatype Properties
[ISBN](#ISBN),
[author](#author),
[date of publication](#dateofpublication),
[Index of the element in the enumeration](#Indexoftheelementintheenumeration),
[publisher](#publisher),
[uri](#uri),
[](ISBN)
### ISBN
Property | Value
--- | ---
IRI | `http://w3id.org/dt#ISBN`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](author)
### author
Property | Value
--- | ---
IRI | `http://w3id.org/dt#author`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](dateofpublication)
### date of publication
Property | Value
--- | ---
IRI | `http://w3id.org/dt#dateOfPublication`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Indexoftheelementintheenumeration)
### Index of the element in the enumeration
Property | Value
--- | ---
IRI | `http://w3id.org/dt#hasIndex`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](publisher)
### publisher
Property | Value
--- | ---
IRI | `http://w3id.org/dt#publisher`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](uri)
### uri
Property | Value
--- | ---
IRI | `http://w3id.org/dt#uri`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `http://w3id.org/dt#`
* **dc**
  * `http://purl.org/dc/terms/`
* **dt**
  * `http://w3id.org/dt#`
* **isoprops**
  * `http://w3id.org/isoprops#`
* **loin**
  * `http://w3id.org/loin#`
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