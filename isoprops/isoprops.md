Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# ISO 23386 Property Ontology (ISOProps)

## Metadata
* **IRI**
  * `https://w3id.org/isoprops`
* **Publisher(s)**
  * [Chair of Computing in Engineering, Ruhr University Bochum](https://www.inf.bi.rub.de)
* **Creators(s)**
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
  * [Sven Zentgraf](https://orcid.org/0000-0001-6058-7614)
    [[ORCID]](https://orcid.org/0000-0001-6058-7614)
    (<sven.zentgraf@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/sven_zentgraf.html.en)
* **Created**
  * 2019-01-01
* **Modified**
  * 2024-04-24
* **Issued**
  * 2021-12-06
* **Version Information**
  * v2.1
* **Version IRI**
  * [https://w3id.org/isoprops](https://w3id.org/isoprops)
* **Imports**
  * [http://inf.bi.rub.de/ontology/dt](http://inf.bi.rub.de/ontology/dt)
* **License**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
* **Ontology RDF**
  * RDF ([isoprops.ttl](turtle))
* **Code Repository**
  * [https://github.com/RUB-Informatik-im-Bauwesen/ir-ontologies/tree/main/isoprops](https://github.com/RUB-Informatik-im-Bauwesen/ir-ontologies/tree/main/isoprops)
### Description
<p>The ISO Property (ISOProps) ontology maps the data model of the ISO 23386 for the describing, creating, and maintenance of properties in interconnected data dictionaries.</p>
<p>The namespace for ISOProps terms is <a href="https://w3id.org/isoprops">https://w3id.org/isoprops</a></p>
<p>The preferred prefix for the ISOProps namespace is <code>isoprops</code>.</p>
<h2>Ontology Overview</h2>
<p><img alt="IDDO Ontology" src="Ontology_Overview.png" title="Ontology" /></p>
<h2>Assigning an ISOProps Property to a Feature of Interest</h2>
<p><img alt="Property_Assignment" src="Property_Assignment.png" title="Property_Assignment" /></p>
<h2>Relation between DCAT vocabulary and the ISOProps ontology</h2>
<p><img alt="DataCatalog_Overview" src="DataCatalog_Overview.png" title="DataCatalog_Overview" /></p>
* **History Note:** <p>v2.1: renamed from IDDO to ISOProps
  v2.0: update</p>
<p>v0.3: dcat usage update </p>
<p>v0.2: ontology update </p>
<p>v0.1: initial ontology for BIMSTRUCT project </p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Annotation Properties](#annotationproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[Assigned property](#Assignedproperty),
[Datenkatalog](#Datenkatalog),
[Defining value item](#Definingvalueitem),
[Digital format item](#Digitalformatitem),
[External Dictionary Reference](#ExternalDictionaryReference),
[Grenzwertliste](#Grenzwertliste),
[Group of properties](#Groupofproperties),
[Liste definierender Werte](#ListedefinierenderWerte),
[Maximum Boundary Limit](#MaximumBoundaryLimit),
[Minimum Boundary Limit](#MinimumBoundaryLimit),
[Physikalische Groesse](#PhysicalQuantity),
[Possible value in language N](#PossiblevalueinlanguageN),
[Property](#Property),
[Referenzdokument](#Referenzdokument),
[Symbol des Merkmals in einer gegebenen Merkmalsgruppe](#SymboldesMerkmalsineinergegebenenMerkmalsgruppe),
[Teilmenge des Datenkatalogs](#TeilmengedesDatenkatalogs),
[Text format item](#Textformatitem),
### Assigned property
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#AssignedProperty`
Description | <p>Repraesentiert die Zweisung eines Merkmals und einer Merkmalszustandes an ein Feature of Interest (FOI)</p>
Super-classes |[http://www.w3id.org/opm#Property](http://www.w3id.org/opm#Property) (c)<br />
Restrictions |[isoprops:hasPropertyReference](hatMerkmalreferenz) (op) **exactly** 1<br />[http://www.w3id.org/opm#hasPropertyState](http://www.w3id.org/opm#hasPropertyState) **min** 1<br />
In domain of |[isoprops:hasPropertyReference](hatMerkmalreferenz) (op)<br />
In range of |[isoprops:hasProperty](hasproperty) (op)<br />
### Maximum Boundary Limit
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#BoundaryLimitMax`
Description | <p>Boundary limit  interval consisting of the the upper (maxValue) interval boundary</p>
Usage Note | PA040
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:hasUnit](hasunit) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />[isoprops:Inclusive](inclusive) (dp) **exactly** 1<br />
In domain of |[isoprops:hasUnit](hasunit) (op)<br />[isoprops:Inclusive](inclusive) (dp)<br />
### Minimum Boundary Limit
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#BoundaryLimitMin`
Description | <p>Grenzwertintervall bestehend aus der unteren(minValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />[isoprops:Inclusive](inclusive) (dp) **exactly** 1<br />[isoprops:hasUnit](hasunit) (op) **exactly** 1<br />
In domain of |[isoprops:hasUnit](hasunit) (op)<br />[isoprops:Inclusive](inclusive) (dp)<br />
In range of |[isoprops:hasBoundaryLimit](Boundaryvalue) (op)<br />
### Grenzwertliste
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#BoundaryValue`
Description | <p>Pair  (List of boundary intervals of possible values for the property, unit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:hasBoundaryLimit](Boundaryvalue) (op) **max** 1 [isoprops:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />[isoprops:hasBoundaryLimit](Boundaryvalue) (op) **max** 1 [isoprops:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />
In domain of |[isoprops:hasBoundaryLimit](Boundaryvalue) (op)<br />
In range of |[isoprops:hasBoundary](Grenzwerte) (op)<br />
### Defining value item
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DefiningValueItem`
Description | <p>Enthaelt einen definierenden Wert eines Arrays in Form eines Literals</p>
Usage Note | PA035
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[isoprops:hasDefiningValueItem](Definingvalue) (op)<br />
### Liste definierender Werte
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DefiningValuesList`
Description | <p>Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:DefiningValueItem](Definingvalueitem) **min** 1<br />
In domain of |[isoprops:hasDefiningValueItem](Definingvalue) (op)<br />
In range of |[isoprops:hasDefiningValue](Definingvalues) (op)<br />
### Datenkatalog
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Dictionary`
Description | <p>Centralized repository of information about data such as meaning, relationships to other data, origin, usage and format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[isoprops:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op) **min** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />
In domain of |[isoprops:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Referenzdokument
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DictionaryReferenceDocument`
Description | <p>Publication that is consulted to find specific information, particularly in a technical or scientific domain</p>
Super-classes |[dcat:Distribution](http://www.w3.org/ns/dcat#Distribution) (c)<br />
Restrictions |[isoprops:hasPropertyGroupReference](haspropertygroupreference) (op) **exactly** 1<br />
In range of |[isoprops:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op)<br />
### Teilmenge des Datenkatalogs
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DictionarySubset`
Description | <p>Defines a subset or subgrouping of a data catalog</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />[isoprops:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />
In domain of |[isoprops:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op)<br />
In range of |[isoprops:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Digital format item
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DigitalFormatItem`
Description | <p>Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:Precision](Tolerance) (dp) **exactly** 1<br />[isoprops:hasUnit](hasunit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
In domain of |[isoprops:Precision](Tolerance) (dp)<br />
In range of |[isoprops:hasDigitalFormat](DigitalesFormat) (op)<br />
### External Dictionary Reference
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#ExternalDictionaryReference`
Description | <p>Pair (property internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing properties</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[http://inf.bi.rub.de/ontology/dt#hasExternalDictionary](http://inf.bi.rub.de/ontology/dt#hasExternalDictionary) **exactly** 1<br />[http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty](http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty) **exactly** 1<br />
In range of |[isoprops:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />
### Group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#GroupOfProperties`
Description | <p>Sammlung, die es ermoeglicht, die Merkmale vorauszuplanen oder zu organisieren</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[isoprops:CountryOfUse](Countryofuse) (dp) **min** 1<br />[isoprops:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op) **min** 0 [isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:Tolerance](Tolerance1) (dp) **min** 0<br />[isoprops:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[isoprops:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op) **min** 0 [isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:DeprecationExplanation](ErlaeuterungfuerdieAblehnung) (dp) **max** 1<br />[isoprops:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[isoprops:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[isoprops:Status](Status) (dp) **exactly** 1<br />[isoprops:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[isoprops:CountryOfOrigin](Ursprungsland) (dp) **exactly** 1<br />[isoprops:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[isoprops:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[isoprops:RevisionNumber](Revisionnumber) (dp) **exactly** 1<br />[isoprops:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[isoprops:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[isoprops:hasParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **min** 0 [isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp) **exactly** 1<br />[isoprops:DeprecationExplanation](ErlaeuterungfuerdieAblehnung) (dp) **min** 0<br />[isoprops:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[isoprops:hasExternalDictionaryReference](hasExternalDictionaryReference) (op) **min** 0 [isoprops:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[isoprops:VisualRepresentation](BildlicheDarstellung) (dp) **min** 1<br />[isoprops:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />[isoprops:DateOfVersion](Dateofversion) (dp) **exactly** 1<br />[isoprops:hasParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **max** 1 [isoprops:GroupOfProperties](Groupofproperties) (c)<br />
In domain of |[isoprops:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[isoprops:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[isoprops:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[isoprops:CountryOfUse](Countryofuse) (dp)<br />[isoprops:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[isoprops:Status](Status) (dp)<br />[isoprops:DateOfDeactivation](Dateofdeactivation) (dp)<br />[isoprops:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp)<br />[isoprops:VisualRepresentation](BildlicheDarstellung) (dp)<br />[isoprops:DateOfVersion](Dateofversion) (dp)<br />[isoprops:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />[isoprops:DateOfCreation](DatumderErstellung) (dp)<br />[isoprops:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp)<br />[isoprops:hasRelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op)<br />[isoprops:RevisionNumber](Revisionnumber) (dp)<br />[isoprops:CreatorsLanguage](Creator'slanguage) (dp)<br />[isoprops:CountryOfOrigin](Ursprungsland) (dp)<br />[isoprops:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[isoprops:hasParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[isoprops:DeprecationExplanation](ErlaeuterungfuerdieAblehnung) (dp)<br />[isoprops:DateOfActivation](DatumderAktivierung) (dp)<br />[isoprops:NameInLanguage](NameinlanguageN) (dp)<br />[isoprops:DateOfLastChange](Dateoflastchange) (dp)<br />[isoprops:VersionNumber](Versionsnummer) (dp)<br />
In range of |[isoprops:hasPropertyGroupReference](haspropertygroupreference) (op)<br />[isoprops:hasGivenGroupOfProperties](Givengroupofproperties) (op)<br />[isoprops:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[isoprops:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[isoprops:hasGroupOfProperties](Group(s)ofproperties) (op)<br />[isoprops:hasParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />
### Physikalische Groesse
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#PhysicalQuantity`
Description | <p>List of pairs (physical quantity | language) Physical quantities are expressed in International System (SI) units Non-physical quantities such as text are expressed with the value "without" This is equivalent to a measure in ISO 16739-1 and ISO 10303 Only one physical quantity can be attached to a property. This attribute is used to provide the quantity in plain text with all the needed translations</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
### Possible value in language N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#PossibleValues`
Description | <p>Possible value for the property and language Values can be string or numbers</p>
Usage Note | PA039
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[isoprops:hasPossibleValues](ListofpossiblevaluesinlanguageN) (op)<br />
### Property
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Property`
Description | <p>Inherent or acquired feature of an item</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[isoprops:DeprecationExplanation](ErlaeuterungfuerdieAblehnung) (dp) **min** 0<br />[isoprops:DataType](Datatype) (dp) **exactly** 1<br />[isoprops:MethodOfMeasurement](Methodofmeasurement) (dp) **min** 0<br />[isoprops:CountryOfOrigin](Ursprungsland) (dp) **max** 1<br />[isoprops:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[isoprops:replacesProperties](ListeersetzterMerkmale) (op) **min** 0 [isoprops:Property](Property) (c)<br />[isoprops:DeprecationExplanation](ErlaeuterungfuerdieAblehnung) (dp) **max** 1<br />[isoprops:hasDefiningValue](Definingvalues) (op) **min** 0 [isoprops:DefiningValuesList](ListedefinierenderWerte) (c)<br />[isoprops:Tolerance](Tolerance1) (dp) **min** 0<br />[isoprops:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />[isoprops:hasPhysicalQuantity](PhysikalischeGroesse) (op) **min** 1<br />[isoprops:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[isoprops:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[isoprops:hasConnectedProperty](Connectedproperties) (op) **min** 0 [isoprops:Property](Property) (c)<br />[isoprops:DescriptionInLanguage](BeschreibunginSpracheN) (dp) **min** 0<br />[isoprops:isReplacedByProperty](ListeersetzenderMerkmale) (op) **min** 0 [isoprops:Property](Property) (c)<br />[isoprops:CountryOfOrigin](Ursprungsland) (dp) **min** 0<br />[isoprops:NameOfTheDefiningValues](Namesofthedefiningvalues) (dp) **min** 0<br />[isoprops:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[isoprops:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[isoprops:ExampleInLanguage](BeispielinSpracheN) (dp) **min** 0<br />[isoprops:hasSymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op) **min** 0 [isoprops:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />[isoprops:hasPossibleValues](ListofpossiblevaluesinlanguageN) (op) **min** 0 [isoprops:PossibleValues](PossiblevalueinlanguageN) (c)<br />[isoprops:hasPossibleValues](ListofpossiblevaluesinlanguageN) (op) **min** 0<br />[isoprops:hasBoundary](Grenzwerte) (op) **exactly** 1 [isoprops:BoundaryValue](Grenzwertliste) (c)<br />[isoprops:hasTextFormat](Textformat) (op) **min** 0 [isoprops:TextFormatItem](Textformatitem) (c)<br />[isoprops:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[isoprops:CountryOfUse](Countryofuse) (dp) **min** 1<br />[isoprops:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[isoprops:hasGroupOfProperties](Group(s)ofproperties) (op) **min** 1 [isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:DynamicProperty](DynamicProperty) (dp) **exactly** 1<br />[isoprops:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[isoprops:VisualRepresentation](BildlicheDarstellung) (dp) **min** 0<br />[isoprops:DateOfVersion](Dateofversion) (dp) **exactly** 1<br />[isoprops:hasUnit](hasunit) (op) **min** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[isoprops:Status](Status) (dp) **exactly** 1<br />[isoprops:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[isoprops:hasDigitalFormat](DigitalesFormat) (op) **min** 0 [isoprops:DigitalFormatItem](Digitalformatitem) (c)<br />[isoprops:hasExternalDictionaryReference](hasExternalDictionaryReference) (op) **min** 0 [isoprops:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[isoprops:RevisionNumber](Revisionnumber) (dp) **exactly** 1<br />[isoprops:hasParameterOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op) **min** 0 [isoprops:Property](Property) (c)<br />[isoprops:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />
In domain of |[isoprops:Status](Status) (dp)<br />[isoprops:DateOfVersion](Dateofversion) (dp)<br />[isoprops:ExampleInLanguage](BeispielinSpracheN) (dp)<br />[isoprops:VisualRepresentation](BildlicheDarstellung) (dp)<br />[isoprops:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />[isoprops:hasDefiningValue](Definingvalues) (op)<br />[isoprops:hasGroupOfProperties](Group(s)ofproperties) (op)<br />[isoprops:hasDigitalFormat](DigitalesFormat) (op)<br />[isoprops:DateOfCreation](DatumderErstellung) (dp)<br />[isoprops:hasBoundary](Grenzwerte) (op)<br />[isoprops:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp)<br />[isoprops:hasPhysicalQuantity](PhysikalischeGroesse) (op)<br />[isoprops:DataType](Datatype) (dp)<br />[isoprops:hasParameterOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[isoprops:MethodOfMeasurement](Methodofmeasurement) (dp)<br />[isoprops:RevisionNumber](Revisionnumber) (dp)<br />[isoprops:CountryOfOrigin](Ursprungsland) (dp)<br />[isoprops:hasTextFormat](Textformat) (op)<br />[isoprops:CreatorsLanguage](Creator'slanguage) (dp)<br />[isoprops:hasSymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />[isoprops:hasGivenGroupOfProperties](Givengroupofproperties) (op)<br />[isoprops:hasPossibleValues](ListofpossiblevaluesinlanguageN) (op)<br />[isoprops:DeprecationExplanation](ErlaeuterungfuerdieAblehnung) (dp)<br />[isoprops:Tolerance](Tolerance1) (dp)<br />[isoprops:DateOfActivation](DatumderAktivierung) (dp)<br />[isoprops:NameInLanguage](NameinlanguageN) (dp)<br />[isoprops:hasUnit](hasunit) (op)<br />[isoprops:VersionNumber](Versionsnummer) (dp)<br />[isoprops:DateOfLastChange](Dateoflastchange) (dp)<br />[isoprops:hasConnectedProperty](Connectedproperties) (op)<br />[isoprops:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[isoprops:replacesProperties](ListeersetzterMerkmale) (op)<br />[isoprops:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[isoprops:CountryOfUse](Countryofuse) (dp)<br />[isoprops:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[isoprops:DescriptionInLanguage](BeschreibunginSpracheN) (dp)<br />[isoprops:isReplacedByProperty](ListeersetzenderMerkmale) (op)<br />[isoprops:DateOfDeactivation](Dateofdeactivation) (dp)<br />
In range of |[isoprops:hasConnectedProperty](Connectedproperties) (op)<br />[isoprops:hasPropertyReference](hatMerkmalreferenz) (op)<br />[isoprops:isReplacedByProperty](ListeersetzenderMerkmale) (op)<br />[isoprops:replacesProperties](ListeersetzterMerkmale) (op)<br />[isoprops:hasParameterOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />
### Symbol des Merkmals in einer gegebenen Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#SymbolOfTheProperty`
Description | <p>Pair (symbol of the property, globally unique identifier of the group of properties (attribute GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:hasGivenGroupOfProperties](Givengroupofproperties) (op) **exactly** 1 [isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:Symbol](Symbol) (dp) **exactly** 1<br />
In domain of |[isoprops:Symbol](Symbol) (dp)<br />
In range of |[isoprops:hasSymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />
### Text format item
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#TextFormatItem`
Description | <p>Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:Encoding](Encoding) (dp) **exactly** 1<br />[isoprops:NumberOfCharacters](NumberofCharacters) (dp) **exactly** 1<br />
In domain of |[isoprops:NumberOfCharacters](NumberofCharacters) (dp)<br />[isoprops:Encoding](Encoding) (dp)<br />
In range of |[isoprops:hasTextFormat](Textformat) (op)<br />

## Object Properties
[Grenzwerte](#Grenzwerte),
[Boundary value](#Boundaryvalue),
[Connected properties](#Connectedproperties),
[Defining values](#Definingvalues),
[Defining value](#Definingvalue),
[hat den Verweis auf ein Referenzdokument](#hatdenVerweisaufeinReferenzdokument),
[hat Teilmenge eines Katalogs](#hatTeilmengeeinesKatalogs),
[Digitales Format](#DigitalesFormat),
[has external dictionary](#hasexternaldictionary),
[has external dictionary property](#hasexternaldictionaryproperty),
[has External Dictionary Reference](#hasExternalDictionaryReference),
[Given group of properties](#Givengroupofproperties),
[Group(s) of properties](#Group(s)ofproperties),
[Parameter des dynamischen Merkmals](#ParameterdesdynamischenMerkmals),
[uebergeordnete Merkmalsgruppe](#uebergeordneteMerkmalsgruppe),
[Physikalische Groesse](#PhysikalischeGroesse),
[List of possible values in language N](#ListofpossiblevaluesinlanguageN),
[has property](#hasproperty),
[has property group reference](#haspropertygroupreference),
[hat Merkmalreferenz](#hatMerkmalreferenz),
[Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen](#BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen),
[Symbols of the property in a given property group](#Symbolsofthepropertyinagivenpropertygroup),
[Textformat](#Textformat),
[has unit](#hasunit),
[Liste ersetzender Merkmalsgruppen](#ListeersetzenderMerkmalsgruppen),
[Liste ersetzender Merkmale](#ListeersetzenderMerkmale),
[Liste ersetzter Merkmalsgruppen](#ListeersetzterMerkmalsgruppen),
[Liste ersetzter Merkmale](#ListeersetzterMerkmale),
[](Grenzwerte)
### Grenzwerte
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasBoundary`
Description | Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:BoundaryValue](Grenzwertliste) (c)<br />
[](Boundaryvalue)
### Boundary value
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasBoundaryLimit`
Description | Einzelnes Grenzwertintervall
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:BoundaryValue](Grenzwertliste) (c)<br />
Range(s) |[isoprops:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
[](Connectedproperties)
### Connected properties
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasConnectedProperty`
Description | Liste der global eindeutigen Bezeichner der verbundenen Merkmale (Attribut PA001); der Wert eines Merkmals steht zu den Werten der anderen in einer Beziehung. Beispielsweise ist ein Schallabsorptionsgrad fuer eine bestimmte Frequenz gegeben, in diesem Fall sind Schallabsorp-tionsgrad und Frequenz ver-bundene Merkmale.
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:Property](Property) (c)<br />
[](Definingvalues)
### Defining values
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDefiningValue`
Description | Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:DefiningValuesList](ListedefinierenderWerte) (c)<br />
[](Definingvalue)
### Defining value
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDefiningValueItem`
Description | Contains a defining value of an array
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:DefiningValuesList](ListedefinierenderWerte) (c)<br />
Range(s) |[isoprops:DefiningValueItem](Definingvalueitem) (c)<br />
[](hatdenVerweisaufeinReferenzdokument)
### hat den Verweis auf ein Referenzdokument
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDictionaryReferenceDocument`
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[isoprops:DictionarySubset](TeilmengedesDatenkatalogs) (c)<br />
Range(s) |[isoprops:DictionaryReferenceDocument](Referenzdokument) (c)<br />
[](hatTeilmengeeinesKatalogs)
### hat Teilmenge eines Katalogs
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDictionarySubset`
Super-properties |[dcat:dataset](http://www.w3.org/ns/dcat#dataset)<br />
Domain(s) |[isoprops:Dictionary](Datenkatalog) (c)<br />
Range(s) |[isoprops:DictionarySubset](TeilmengedesDatenkatalogs) (c)<br />
[](DigitalesFormat)
### Digitales Format
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDigitalFormat`
Description | Pair for digital text type (precision, unit) Precision is the number of significant digits
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:DigitalFormatItem](Digitalformatitem) (c)<br />
[](hasexternaldictionary)
### has external dictionary
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasExternalDictionary`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasexternaldictionaryproperty)
### has external dictionary property
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasExternalDictionaryProperty`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasExternalDictionaryReference)
### has External Dictionary Reference
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasExternalDictionaryReference`
Description | Liste von Paaren (interner Merk-malsbezeichner, entsprechender Datenkatalog-Bezeichner) dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden
Usage Note | PA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[isoprops:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />
[](Givengroupofproperties)
### Given group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasGivenGroupOfProperties`
Description | Globally unique identifier of a group of properties (attribute GA001) for the symbol assigned to the property.
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](Group(s)ofproperties)
### Group(s) of properties
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasGroupOfProperties`
Description | Liste von global eindeutigen Bezeichnern von Merkmalsgruppen (Attribut GA001), denen das Merkmal angehoert
Usage Note | PA021
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](ParameterdesdynamischenMerkmals)
### Parameter des dynamischen Merkmals
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasParameterOfTheDynamicProperty`
Description | Liste von GUIDs von Merkmalen, welche Parameter der Funktion fuer ein dynamisches Merkmal sind
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:Property](Property) (c)<br />
[](uebergeordneteMerkmalsgruppe)
### uebergeordnete Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasParentGroupOfProperties`
Description | Ermoeglicht die Ver-knuepfung einer Unter-gruppe mit einer ueber-geordneten Gruppe ueber ihre global ein-deutigen Bezeichner (Attribut GA001) jedes einer Gruppe zugehoerige Merkmal wird von der/den Untergruppe(n) uebernommen
Usage Note | GA023
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](PhysikalischeGroesse)
### Physikalische Groesse
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasPhysicalQuantity`
Description | Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben --> http://qudt.org/vocab/quantitykind/Dimensionless dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.
Usage Note | PA027
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[qudt:QuantityKind](http://qudt.org/schema/qudt/QuantityKind) (c)<br />
[](ListofpossiblevaluesinlanguageN)
### List of possible values in language N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasPossibleValues`
Description | Liste von Paaren (moeglicher Wert fuer das Merkmal und Sprache) Werte koennen String oder Zahlen sein
Usage Note | PA039
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:PossibleValues](PossiblevalueinlanguageN) (c)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasProperty`
Description | Fuegt ein Merkmal zu einem Feature of Interest (FOI) hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[isoprops:AssignedProperty](Assignedproperty) (c)<br />
[](haspropertygroupreference)
### has property group reference
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasPropertyGroupReference`
Description | Attaches a property group reference to a isoprops:ReferenceDocument
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[isoprops:ReferenceDocument](https://w3id.org/isoprops#ReferenceDocument) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](hatMerkmalreferenz)
### hat Merkmalreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasPropertyReference`
Description | Attaches a property reference to a property assignment
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:AssignedProperty](Assignedproperty) (c)<br />
Range(s) |[isoprops:Property](Property) (c)<br />
[](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen)
### Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasRelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | List of pairs (group of properties internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing groups of properties
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](Symbolsofthepropertyinagivenpropertygroup)
### Symbols of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasSymbolsOfTheProperty`
Description | Liste von Paaren (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />
[](Textformat)
### Textformat
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasTextFormat`
Description | Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:TextFormatItem](Textformatitem) (c)<br />
[](hasunit)
### has unit
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasUnit`
Description | A unit to represent a scale that enables a value to be measured It is possible to use this attribute to explain there is no unit attached to the property by using unitless --> http://qudt.org/vocab/unit/UNITLESS
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />[isoprops:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />[isoprops:Property](Property) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](ListeersetzenderMerkmalsgruppen)
### Liste ersetzender Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#isReplacedByGroupOfProperties`
Description | List of globally unique identifiers of the replacing groups of properties
Usage Note | GA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](ListeersetzenderMerkmale)
### Liste ersetzender Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#isReplacedByProperty`
Description | Globally unique identifier (attribute PA001) of the replacing property (or properties)
Usage Note | PA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:Property](Property) (c)<br />
[](ListeersetzterMerkmalsgruppen)
### Liste ersetzter Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#replacesGroupOfProperties`
Description | List of globally unique identifiers of the replaced groups of properties
Usage Note | GA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](ListeersetzterMerkmale)
### Liste ersetzter Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#replacesProperties`
Description | Globally unique identifier of the replaced property (or properties)
Usage Note | PA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[isoprops:Property](Property) (c)<br />

## Datatype Properties
[Kategorie der Merkmalsgruppe](#KategoriederMerkmalsgruppe),
[Ursprungsland](#Ursprungsland),
[Country of use](#Countryofuse),
[Creator's language](#Creator'slanguage),
[Data type](#Datatype),
[Datum der Aktivierung](#DatumderAktivierung),
[Datum der Erstellung](#DatumderErstellung),
[Date of deactivation](#Dateofdeactivation),
[Date of last change](#Dateoflastchange),
[Datum der Ueberarbeitung](#DatumderUeberarbeitung),
[Date of version](#Dateofversion),
[Definition of in language N](#DefinitionofinlanguageN),
[Erlaeuterung fuer die Ablehnung](#ErlaeuterungfuerdieAblehnung),
[Beschreibung in Sprache N](#BeschreibunginSpracheN),
[Dynamic Property](#DynamicProperty),
[Encoding](#Encoding),
[Beispiel in Sprache N](#BeispielinSpracheN),
[Globally Unique Identifier (GUID)](#GloballyUniqueIdentifier(GUID)),
[inclusive](#inclusive),
[Method of measurement](#Methodofmeasurement),
[Name in language N](#NameinlanguageN),
[Names of the defining values](#Namesofthedefiningvalues),
[Number of Characters](#NumberofCharacters),
[Tolerance](#Tolerance),
[Revision number](#Revisionnumber),
[Status](#Status),
[Subdivision of use](#Subdivisionofuse),
[Symbol](#Symbol),
[Tolerance](#Tolerance1),
[Versionsnummer](#Versionsnummer),
[Bildliche Darstellung](#BildlicheDarstellung),
[](KategoriederMerkmalsgruppe)
### Kategorie der Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#CategoryOfGroupOfProperties`
Description | Gibt die Kategorie der erstellten Merkmalsgruppe an
Usage Note | GA022
Example | ````Reference document`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](Ursprungsland)
### Ursprungsland
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#CountryOfOrigin`
Description | Land, aus dem die Anforderung an dieses Merkmal/dieser Merkmalsgruppe stammt
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Countryofuse)
### Country of use
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#CountryOfUse`
Description | Country (group of countries, continent) in which the property is relevant for the market the stakeholders operate in
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Creator'slanguage)
### Creator's language
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#CreatorsLanguage`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property; this explanation has to be written in international English (EN)
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Datatype)
### Data type
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DataType`
Description | Format fuer die Angabe des Wertes des Merkmals dies kann aus einer Soft-ware-Perspektive als Speiche-rungsart verstanden werden im Falle eines dynamischen Merkmals ist der Wert dieses Attributs der Datentyp des Er-gebnisses der Berechnung mit der Gleichung
Usage Note | PA030
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](DatumderAktivierung)
### Datum der Aktivierung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfActivation`
Description | Datum, nach dem das Merkmal verwendet werden kann
Usage Note | PA04/GA04
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderErstellung)
### Datum der Erstellung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfCreation`
Description | Datum der Validierung der An-frage zur Erstellung des Merkmals durch Sachverstaendige
Usage Note | PA003/GA003
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofdeactivation)
### Date of deactivation
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfDeactivation`
Description | Date of deactivation
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateoflastchange)
### Date of last change
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfLastChange`
Description | Datum der Validierung der letzten Aenderungsanfrage durch Sachverstaendige
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderUeberarbeitung)
### Datum der Ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfRevision`
Description | Datum der Ueberarbeitung
Usage Note | PA006/GA006
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofversion)
### Date of version
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfVersion`
Description | Date of version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DefinitionofinlanguageN)
### Definition of in language N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DefinitionInLanguage`
Description | List of pairs (definition of the property/group of properties, language)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Groupofproperties) (c)<br />[isoprops:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](ErlaeuterungfuerdieAblehnung)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DeprecationExplanation`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property/group of properties; this explanation has to be written in international English (EN)
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](BeschreibunginSpracheN)
### Beschreibung in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DescriptionInLanguage`
Description | List of pairs (Description of the property, language)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DynamicProperty)
### Dynamic Property
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DynamicProperty`
Description | If this is a dynamic property, the value is dependent on the parameters provided in the attribute PA032
Usage Note | PA031
Example | ````yes`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](Encoding)
### Encoding
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Encoding`
Description | The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](BeispielinSpracheN)
### Beispiel in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#ExampleInLanguage`
Description | Liste von Paaren (Beispiel des Merkmals, Sprache)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](GloballyUniqueIdentifier(GUID))
### Globally Unique Identifier (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#GloballyUniqueIdentifier`
Description | Eindeutiger Bezeichner, der mit dem in RFC 4122 beschriebenen Algorithmus erzeugt wird
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](inclusive)
### inclusive
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Inclusive`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />[isoprops:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](Methodofmeasurement)
### Method of measurement
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#MethodOfMeasurement`
Description | Evaluation of construction products to ensure their fitness according to requirements in harmonised technical specifications
Usage Note | PA029
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](NameinlanguageN)
### Name in language N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#NameInLanguage`
Description | Liste von Paaren (Name des Merkmals und Sprache) Dieses Attribut kann verwendet werden, um Synonyme fuer verschiedene Domaenen hinzuzufuegen
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Namesofthedefiningvalues)
### Names of the defining values
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#NameOfTheDefiningValues`
Description | Im Falle eines Feldes liefert dieses Attribut die Namen der Spaltenkoepfe, festgelegt als Liste von Paaren (Name, Sprache)
Usage Note | PA034
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](NumberofCharacters)
### Number of Characters
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#NumberOfCharacters`
Description | Die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Tolerance)
### Tolerance
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Precision`
Description | Precision is the number of significant digits
Usage Note | PA037
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:DigitalFormatItem](Digitalformatitem) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Revisionnumber)
### Revision number
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#RevisionNumber`
Description | Diese Nummer der ueberarbeitung ermoeglicht die Verfolgung kleinerer aenderungen, z. B. neue uebersetzung, Korrekturen von Tippfehlern: wenn sich die Versionsnummer aendert, beginnt die Nummer der ueberarbeitung wieder bei 1. Sachverstaendige entscheiden, ob eine neue Nummer der ueberarbeitung angewendet werden kann oder ob eine neue ueberarbeitung erforderlich ist.
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Status)
### Status
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Status`
Description | Status of the property during its life cycle
Usage Note | PA002/GA002
Example | ````active`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
[](Subdivisionofuse)
### Subdivision of use
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#SubdivisionOfUse`
Description | Documented geographical region of use of the group of properties
Usage Note | PA025/GA020
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Symbol)
### Symbol
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Symbol`
Usage Note | PA022
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Tolerance1)
### Tolerance
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Tolerance`
Description | Fuer numerische Werte; der Gesamtbetrag, um den eine be-stimmte Einheit schwanken darf; sie ist die Differenz zwischen dem Hoechstwert und dem Mindestwert fuer die Einheit
Usage Note | PA036
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Versionsnummer)
### Versionsnummer
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#VersionNumber`
Description | This version number allows tracking of major changes. Experts decide if a new version number must be applied
Usage Note | PA009/GA009
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](BildlicheDarstellung)
### Bildliche Darstellung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#VisualRepresentation`
Description | Bildliche Darstellung des Merkmals durch Skizzen, Fotos, Videos oder sonstige Multimedia-Objekte
Usage Note | PA023/GA018
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Property) (c)<br />[isoprops:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Annotation Properties
[accessURL](#accessURL),
[Code](#Code),
[](accessURL)
### accessURL
Property | Value
--- | ---
IRI | `http://www.w3.org/ns/dcat#accessURL`
[](Code)
### Code
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#code`
Is Defined By | http://www.w3.org/2000/01/rdf-schema#
Description | Code, der zur Identifizierung des Attributs verwendet werden kann
Domain(s) |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Range(s) |[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#Literal) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `https://w3id.org/isoprops#`
* **dc**
  * `http://purl.org/dc/terms/`
* **dcat**
  * `http://www.w3.org/ns/dcat#`
* **ex**
  * `http://www.example.com/property#`
* **isoprops**
  * `https://w3id.org/isoprops#`
* **opm**
  * `https://w3id.org/opm#`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **qudt**
  * `http://qudt.org/schema/qudt/`
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
* **unit**
  * `http://qudt.org/vocab/unit/`
* **vann**
  * `http://purl.org/vocab/vann/`
* **voaf**
  * `http://purl.org/vocommons/voaf#`
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