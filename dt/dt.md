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
<li>[dt:ConstructionObject](https://w3id.org/dt#ConstructionObject)</li>
<li>[dt:DataTemplate](https://w3id.org/dt#DataTemplate)</li>
<li>[dt:ExternalDictionaryReference](https://w3id.org/dt#ExternalDictionaryReference)</li>
<li>[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent)</li>
<li>[dt:PhysicalQuantity](https://w3id.org/dt#PhysicalQuantity)</li>
<li>[dt:PredefinedValueItem](https://w3id.org/dt#PredefinedValueItem)</li>
<li>[dt:PredefinedValuesList](https://w3id.org/dt#PredefinedValuesList)</li>
<li>[dt:Property](https://w3id.org/dt#Property)</li>
<li>[dt:ReferenceDocument](https://w3id.org/dt#ReferenceDocument)</li>
<li>[dt:SetOfProperties](https://w3id.org/dt#SetOfProperties)</li>
<li>[dt:Unit](https://w3id.org/dt#Unit)</li>
### Construction object
Property | Value
--- | ---
URI | `https://w3id.org/dt#ConstructionObject`
Description | object of interest in the context of a construction process
Super-classes |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
### Data template
Property | Value
--- | ---
URI | `https://w3id.org/dt#DataTemplate`
Description | data structure used to describe the characteristics of construction objects
Super-classes |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
Restrictions |[dt:hasProperty](https://w3id.org/dt#hasProperty) (op) **some** [isoprops:Property](https://w3id.org/isoprops#Property) (c)<br />[dt:hasSetOfProperties](https://w3id.org/dt#hasSetOfProperties) (op) **some** [dt:SetOfProperties](https://w3id.org/dt#SetOfProperties) (c)<br />[dt:isDataTemplateFor](https://w3id.org/dt#isDataTemplateFor) (op) **some** [loin:AlphanumericalInformation](https://w3id.org/loin#AlphanumericalInformation) (c)<br />
In domain of |[dt:hasProperty](https://w3id.org/dt#hasProperty) (op)<br />[dt:isDataTemplateFor](https://w3id.org/dt#isDataTemplateFor) (op)<br />[dt:hasSetOfProperties](https://w3id.org/dt#hasSetOfProperties) (op)<br />
### External dictionary
Property | Value
--- | ---
URI | `https://w3id.org/dt#ExternalDictionaryReference`
Description | reference to an external dictionary, which is a centralized repository of information about data such as meaning, relationships to other data, origin, usage and format
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[dt:hasExternalDictionaryProperty](https://w3id.org/dt#hasExternalDictionaryProperty) (op) **exactly** 1<br />[dt:hasExternalDictionary](https://w3id.org/dt#hasExternalDictionary) (op) **exactly** 1<br />
In domain of |[dt:hasExternalDictionaryProperty](https://w3id.org/dt#hasExternalDictionaryProperty) (op)<br />
In range of |[dt:hasExternalDictionaryReference](https://w3id.org/dt#hasExternalDictionaryReference) (op)<br />
### Library component
Property | Value
--- | ---
URI | `https://w3id.org/dt#LibraryComponent`
Description | named and individually scheduled physical item and feature that might require management, such as inspection, maintenance, servicing or replacement, during the in-use phase
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[dt:hasExternalDictionary](https://w3id.org/dt#hasExternalDictionary) (op) **some** [dt:ExternalDictionaryReference](https://w3id.org/dt#ExternalDictionaryReference) (c)<br />[dt:hasReferenceDocument](https://w3id.org/dt#hasReferenceDocument) (op) **some** [dt:ReferenceDocument](https://w3id.org/dt#ReferenceDocument) (c)<br />
Sub-classes |[dt:Property](https://w3id.org/dt#Property) (c)<br />[dt:DataTemplate](https://w3id.org/dt#DataTemplate) (c)<br />[dt:Unit](https://w3id.org/dt#Unit) (c)<br />[dt:ConstructionObject](https://w3id.org/dt#ConstructionObject) (c)<br />[dt:SetOfProperties](https://w3id.org/dt#SetOfProperties) (c)<br />[dt:ReferenceDocument](https://w3id.org/dt#ReferenceDocument) (c)<br />[dt:PhysicalQuantity](https://w3id.org/dt#PhysicalQuantity) (c)<br />
In domain of |[dt:hasExternalDictionaryReference](https://w3id.org/dt#hasExternalDictionaryReference) (op)<br />[dt:hasExternalDictionary](https://w3id.org/dt#hasExternalDictionary) (op)<br />[dt:hasReferenceDocument](https://w3id.org/dt#hasReferenceDocument) (op)<br />
### Physical quantity
Property | Value
--- | ---
URI | `https://w3id.org/dt#PhysicalQuantity`
Description | the physical quantity of a library component
Super-classes |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
### PredefinedValueItem
Property | Value
--- | ---
URI | `https://w3id.org/dt#PredefinedValueItem`
Description | the physical quantity of a library component
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[dt:hasIndex](https://w3id.org/dt#hasIndex) (dp) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />
### PredefinedValuesList
Property | Value
--- | ---
URI | `https://w3id.org/dt#PredefinedValuesList`
Description | list of predefined values
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:hasUnit](https://w3id.org/isoprops#hasUnit) **max** 1<br />[dt:hasPredefinedValueItem](https://w3id.org/dt#hasPredefinedValueItem) (op) **min** 1<br />[isoprops:hasUnit](https://w3id.org/isoprops#hasUnit) **min** 0<br />
### Property
Property | Value
--- | ---
URI | `https://w3id.org/dt#Property`
Description | inherent or acquired feature of an item
Super-classes |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
Restrictions |[dt:hasPredefinedValues](https://w3id.org/dt#hasPredefinedValues) (op) **min** 0<br />
### Reference document
Property | Value
--- | ---
URI | `https://w3id.org/dt#ReferenceDocument`
Description | publication that is consulted to find specific information, particularly in a technical or scientific domain
Super-classes |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
Restrictions |[dt:publisher](https://w3id.org/dt#publisher) (dp) **max** 1<br />[dt:uri](https://w3id.org/dt#uri) (dp) **max** 1<br />[dt:author](https://w3id.org/dt#author) (dp) **max** 1<br />[dt:dateOfPublication](https://w3id.org/dt#dateOfPublication) (dp) **max** 1<br />[dt:ISBN](https://w3id.org/dt#ISBN) (dp) **max** 1<br />
In range of |[dt:hasReferenceDocument](https://w3id.org/dt#hasReferenceDocument) (op)<br />
### Set of properties
Property | Value
--- | ---
URI | `https://w3id.org/dt#SetOfProperties`
Description | a set of properties that can be applied to a data template
Super-classes |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
Restrictions |[dt:hasProperty](https://w3id.org/dt#hasProperty) (op) **min** 0<br />[dt:hasProperty](https://w3id.org/dt#hasProperty) (op) **some** [isoprops:Property](https://w3id.org/isoprops#Property) (c)<br />[dt:hasSetOfProperties](https://w3id.org/dt#hasSetOfProperties) (op) **some** [dt:SetOfProperties](https://w3id.org/dt#SetOfProperties) (c)<br />[dt:hasSetOfProperties](https://w3id.org/dt#hasSetOfProperties) (op) **min** 0<br />
In domain of |[dt:hasSetOfProperties](https://w3id.org/dt#hasSetOfProperties) (op)<br />
In range of |[dt:hasSetOfProperties](https://w3id.org/dt#hasSetOfProperties) (op)<br />
### Unit
Property | Value
--- | ---
URI | `https://w3id.org/dt#Unit`
Description | real scalar quantity, defined and adopted by convention, with which any other quantity of the same kind can be compared to express the ratio of the second quantity to the first one as a number
Super-classes |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />

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
URI | `https://w3id.org/dt#hasExternalDictionary`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
[](hasexternalpropertyreference)
### has external property reference
Property | Value
--- | ---
URI | `https://w3id.org/dt#hasExternalDictionaryProperty`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:ExternalDictionaryReference](https://w3id.org/dt#ExternalDictionaryReference) (c)<br />
[](referencedexternaldictionary)
### referenced external dictionary
Property | Value
--- | ---
URI | `https://w3id.org/dt#hasExternalDictionaryReference`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
Range(s) |[dt:ExternalDictionaryReference](https://w3id.org/dt#ExternalDictionaryReference) (c)<br />
[](PredefindedValueItem@en-GB})
### Predefinded Value Item@en-GB}
Property | Value
--- | ---
URI | `https://w3id.org/dt#hasPredefinedValueItem`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasPredefinedValues)
### hasPredefinedValues
Property | Value
--- | ---
URI | `https://w3id.org/dt#hasPredefinedValues`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
URI | `https://w3id.org/dt#hasProperty`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:DataTemplate](https://w3id.org/dt#DataTemplate) (c)<br />
Range(s) |[isoprops:Property](https://w3id.org/isoprops#Property) (c)<br />
[](hasreferencedocument)
### has reference document
Property | Value
--- | ---
URI | `https://w3id.org/dt#hasReferenceDocument`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:LibraryComponent](https://w3id.org/dt#LibraryComponent) (c)<br />
Range(s) |[dt:ReferenceDocument](https://w3id.org/dt#ReferenceDocument) (c)<br />
[](hassetofproperties)
### has set of properties
Property | Value
--- | ---
URI | `https://w3id.org/dt#hasSetOfProperties`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:SetOfProperties](https://w3id.org/dt#SetOfProperties) (c)<br />[dt:DataTemplate](https://w3id.org/dt#DataTemplate) (c)<br />
Range(s) |[dt:SetOfProperties](https://w3id.org/dt#SetOfProperties) (c)<br />
[](isdatatemplatefor)
### is data template for
Property | Value
--- | ---
URI | `https://w3id.org/dt#isDataTemplateFor`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[dt:DataTemplate](https://w3id.org/dt#DataTemplate) (c)<br />
Range(s) |[loin:SpecificationPerObjectType](https://w3id.org/loin#SpecificationPerObjectType) (c)<br />

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
URI | `https://w3id.org/dt#ISBN`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](author)
### author
Property | Value
--- | ---
URI | `https://w3id.org/dt#author`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](dateofpublication)
### date of publication
Property | Value
--- | ---
URI | `https://w3id.org/dt#dateOfPublication`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Indexoftheelementintheenumeration)
### Index of the element in the enumeration
Property | Value
--- | ---
URI | `https://w3id.org/dt#hasIndex`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](publisher)
### publisher
Property | Value
--- | ---
URI | `https://w3id.org/dt#publisher`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](uri)
### uri
Property | Value
--- | ---
URI | `https://w3id.org/dt#uri`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `http://w3id.org/dt`
* **dc**
  * `http://purl.org/dc/terms/`
* **dt**
  * `https://w3id.org/dt#`
* **isoprops**
  * `https://w3id.org/isoprops#`
* **loin**
  * `https://w3id.org/loin#`
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