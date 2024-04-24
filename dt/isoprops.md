Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.9.3

# Data Template (DT) Ontology

## Metadata
* **URI**
  * `http://w3id.org/dt`
* **Creators(s)**
  * [Liu Liu](https://orcid.org/0000-0001-5907-7609)
    [[0000-0001-5907-7609](https://orcid.org/0000-0001-5907-7609)]
    [liu.liu-m6r@rub.de](liu.liu-m6r@rub.de) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/liu_liu.html.en)
  * [Marthina Mellenthin-Filardo](https://orcid.org/0000-0001-7759-7579)
    [[0000-0001-7759-7579](https://orcid.org/0000-0001-7759-7579)]
    [martina.mellenthin.filardo@uni-weimar.de](martina.mellenthin.filardo@uni-weimar.de) of [Bauhaus-Universitaet Weimar](https://www.uni-weimar.de/en/civil-engineering/chairs/construction-engineering-and-management/people/martina-mellenthin-filardo-msc/)
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[0000-0002-6249-243X](https://orcid.org/0000-0002-6249-243X)]
    [philipp.hagedorn-n6v@rub.de](philipp.hagedorn-n6v@rub.de) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
  * [Sven Zentgraf](https://orcid.org/0000-0001-6058-7614)
    [[0000-0001-6058-7614](https://orcid.org/0000-0001-6058-7614)]
    [sven.zentgraf@rub.de](sven.zentgraf@rub.de) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/sven_zentgraf.html.en)
* **Created**
  * 2023-12-23
* **Version Information**
  * Created with TopBraid Composer
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
The Data Template (DT) Ontology is based on concepts and principles for creating templates from ISO 23387 and the associated XML data schema, which is currently under development. 

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
<li>[Construction object](#Constructionobject)</li>
<li>[Data template](#Datatemplate)</li>
<li>[External dictionary](#Externaldictionary)</li>
<li>[Library component](#Librarycomponent)</li>
<li>[Physical quantity](#Physicalquantity)</li>
<li>[PredefinedValueItem](#PredefinedValueItem)</li>
<li>[PredefinedValuesList](#PredefinedValuesList)</li>
<li>[Property](#Property)</li>
<li>[Reference document](#Referencedocument)</li>
<li>[Set of properties](#Setofproperties)</li>
<li>[Unit](#Unit)</li>
### Construction object
Property | Value
--- | ---
URI | `http://w3id.org/dt#ConstructionObject`
Description | object of interest in the context of a construction process
Super-classes |[Library component](#Librarycomponent) (c)<br />
### Data template
Property | Value
--- | ---
URI | `http://w3id.org/dt#DataTemplate`
Description | data structure used to describe the characteristics of construction objects
Super-classes |[Library component](#Librarycomponent) (c)<br />
Restrictions |[has set of properties](#hassetofproperties) (op) **some** [Set of properties](#Setofproperties) (c)<br />[has property](#hasproperty) (op) **some** [https://w3id.org/isoprops#Property](https://w3id.org/isoprops#Property) (c)<br />[is data template for](#isdatatemplatefor) (op) **some** [https://w3id.org/loin#AlphanumericalInformation](https://w3id.org/loin#AlphanumericalInformation) (c)<br />
In domain of |[is data template for](#isdatatemplatefor) (op)<br />[has property](#hasproperty) (op)<br />[has set of properties](#hassetofproperties) (op)<br />
### External dictionary
Property | Value
--- | ---
URI | `http://w3id.org/dt#ExternalDictionaryReference`
Description | reference to an external dictionary, which is a centralized repository of information about data such as meaning, relationships to other data, origin, usage and format
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[has external dictionary](#hasexternaldictionary) (op) **exactly** 1<br />[has external property reference](#hasexternalpropertyreference) (op) **exactly** 1<br />
In domain of |[has external property reference](#hasexternalpropertyreference) (op)<br />
In range of |[referenced external dictionary](#referencedexternaldictionary) (op)<br />
### Library component
Property | Value
--- | ---
URI | `http://w3id.org/dt#LibraryComponent`
Description | named and individually scheduled physical item and feature that might require management, such as inspection, maintenance, servicing or replacement, during the in-use phase
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[has reference document](#hasreferencedocument) (op) **some** [Reference document](#Referencedocument) (c)<br />[has external dictionary](#hasexternaldictionary) (op) **some** [External dictionary](#Externaldictionary) (c)<br />
Sub-classes |[Physical quantity](#Physicalquantity) (c)<br />[Data template](#Datatemplate) (c)<br />[Construction object](#Constructionobject) (c)<br />[Unit](#Unit) (c)<br />[Property](#Property) (c)<br />[Reference document](#Referencedocument) (c)<br />[Set of properties](#Setofproperties) (c)<br />
In domain of |[has reference document](#hasreferencedocument) (op)<br />[referenced external dictionary](#referencedexternaldictionary) (op)<br />[has external dictionary](#hasexternaldictionary) (op)<br />
### Physical quantity
Property | Value
--- | ---
URI | `http://w3id.org/dt#PhysicalQuantity`
Description | the physical quantity of a library component
Super-classes |[Library component](#Librarycomponent) (c)<br />
### PredefinedValueItem
Property | Value
--- | ---
URI | `http://w3id.org/dt#PredefinedValueItem`
Description | the physical quantity of a library component
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[Index of the element in the enumeration](#Indexoftheelementintheenumeration) (dp) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />
### PredefinedValuesList
Property | Value
--- | ---
URI | `http://w3id.org/dt#PredefinedValuesList`
Description | list of predefined values
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[https://w3id.org/isoprops#hasUnit](https://w3id.org/isoprops#hasUnit) **max** 1<br />[https://w3id.org/isoprops#hasUnit](https://w3id.org/isoprops#hasUnit) **min** 0<br />[Predefinded Value Item@en-GB}](#PredefindedValueItem@en-GB}) (op) **min** 1<br />
### Property
Property | Value
--- | ---
URI | `http://w3id.org/dt#Property`
Description | inherent or acquired feature of an item
Super-classes |[Library component](#Librarycomponent) (c)<br />
Restrictions |[hasPredefinedValues](#hasPredefinedValues) (op) **min** 0<br />
### Reference document
Property | Value
--- | ---
URI | `http://w3id.org/dt#ReferenceDocument`
Description | publication that is consulted to find specific information, particularly in a technical or scientific domain
Super-classes |[Library component](#Librarycomponent) (c)<br />
Restrictions |[uri](#uri) (dp) **max** 1<br />[publisher](#publisher) (dp) **max** 1<br />[author](#author) (dp) **max** 1<br />[date of publication](#dateofpublication) (dp) **max** 1<br />[ISBN](#ISBN) (dp) **max** 1<br />
In range of |[has reference document](#hasreferencedocument) (op)<br />
### Set of properties
Property | Value
--- | ---
URI | `http://w3id.org/dt#SetOfProperties`
Description | a set of properties that can be applied to a data template
Super-classes |[Library component](#Librarycomponent) (c)<br />
Restrictions |[has property](#hasproperty) (op) **some** [https://w3id.org/isoprops#Property](https://w3id.org/isoprops#Property) (c)<br />[has set of properties](#hassetofproperties) (op) **some** [Set of properties](#Setofproperties) (c)<br />[has property](#hasproperty) (op) **min** 0<br />[has set of properties](#hassetofproperties) (op) **min** 0<br />
In domain of |[has set of properties](#hassetofproperties) (op)<br />
In range of |[has set of properties](#hassetofproperties) (op)<br />
### Unit
Property | Value
--- | ---
URI | `http://w3id.org/dt#Unit`
Description | real scalar quantity, defined and adopted by convention, with which any other quantity of the same kind can be compared to express the ratio of the second quantity to the first one as a number
Super-classes |[Library component](#Librarycomponent) (c)<br />

## Object Properties
[has external dictionary](#hasexternaldictionary),
[has external property reference](#hasexternalpropertyreference),
[referenced external dictionary](#referencedexternaldictionary),
[Predefinded Value Item@en-GB}](#PredefindedValueItem@en-GB}),
[hasPredefinedValues](#hasPredefinedValues),
[has property](#hasproperty),
[has reference document](#hasreferencedocument),
[has set of properties](#hassetofproperties),
[is data template for](#isdatatemplatefor),
[](hasexternaldictionary)
### has external dictionary
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasExternalDictionary`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Library component](#Librarycomponent) (c)<br />
[](hasexternalpropertyreference)
### has external property reference
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasExternalDictionaryProperty`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[External dictionary](#Externaldictionary) (c)<br />
[](referencedexternaldictionary)
### referenced external dictionary
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasExternalDictionaryReference`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Library component](#Librarycomponent) (c)<br />
Range(s) |[http://w3id.org/dt#ExternalDictionaryReference](http://w3id.org/dt#ExternalDictionaryReference) (c)<br />
[](PredefindedValueItem@en-GB})
### Predefinded Value Item@en-GB}
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasPredefinedValueItem`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasPredefinedValues)
### hasPredefinedValues
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasPredefinedValues`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasProperty`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Data template](#Datatemplate) (c)<br />
Range(s) |[https://w3id.org/isoprops#Property](https://w3id.org/isoprops#Property) (c)<br />
[](hasreferencedocument)
### has reference document
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasReferenceDocument`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Library component](#Librarycomponent) (c)<br />
Range(s) |[http://w3id.org/dt#ReferenceDocument](http://w3id.org/dt#ReferenceDocument) (c)<br />
[](hassetofproperties)
### has set of properties
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasSetOfProperties`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Set of properties](#Setofproperties) (c)<br />[Data template](#Datatemplate) (c)<br />
Range(s) |[http://w3id.org/dt#SetOfProperties](http://w3id.org/dt#SetOfProperties) (c)<br />
[](isdatatemplatefor)
### is data template for
Property | Value
--- | ---
URI | `http://w3id.org/dt#isDataTemplateFor`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[Data template](#Datatemplate) (c)<br />
Range(s) |[https://w3id.org/loin#SpecificationPerObjectType](https://w3id.org/loin#SpecificationPerObjectType) (c)<br />

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
URI | `http://w3id.org/dt#ISBN`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](author)
### author
Property | Value
--- | ---
URI | `http://w3id.org/dt#author`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](dateofpublication)
### date of publication
Property | Value
--- | ---
URI | `http://w3id.org/dt#dateOfPublication`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Indexoftheelementintheenumeration)
### Index of the element in the enumeration
Property | Value
--- | ---
URI | `http://w3id.org/dt#hasIndex`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](publisher)
### publisher
Property | Value
--- | ---
URI | `http://w3id.org/dt#publisher`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](uri)
### uri
Property | Value
--- | ---
URI | `http://w3id.org/dt#uri`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `http://w3id.org/dt`
* **dc**
  * `http://purl.org/dc/terms/`
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