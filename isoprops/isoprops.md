Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# The ISO Property Ontology (ISOProps)

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
[Boundary values list](#Boundaryvalueslist),
[Datenkatalog](#Datenkatalog),
[Definierender Wert-Item](#DefinierenderWert-Item),
[Dictionary subset](#Dictionarysubset),
[Digital format item](#Digitalformatitem),
[External Dictionary Reference](#ExternalDictionaryReference),
[Liste definierender Werte](#ListedefinierenderWerte),
[Maximum Boundary Limit](#MaximumBoundaryLimit),
[Merkmal](#Merkmal),
[Merkmalsgruppe](#Merkmalsgruppe),
[Minimum Boundary Limit](#MinimumBoundaryLimit),
[Physical quantity](#PhysicalQuantity),
[Possible value in language N](#PossiblevalueinlanguageN),
[Reference document](#Referencedocument),
[Symbol des Merkmals in einer gegebenen Merkmalsgruppe](#SymboldesMerkmalsineinergegebenenMerkmalsgruppe),
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
Restrictions |[isoprops:hasUnit](hatEinheit) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />[isoprops:Inclusive](inclusive) (dp) **exactly** 1<br />
In domain of |[isoprops:Inclusive](inclusive) (dp)<br />[isoprops:hasUnit](hatEinheit) (op)<br />
### Minimum Boundary Limit
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#BoundaryLimitMin`
Description | <p>Grenzwertintervall bestehend aus der unteren(minValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:Inclusive](inclusive) (dp) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />[isoprops:hasUnit](hatEinheit) (op) **exactly** 1<br />
In domain of |[isoprops:Inclusive](inclusive) (dp)<br />[isoprops:hasUnit](hatEinheit) (op)<br />
In range of |[isoprops:hasBoundaryLimit](Boundaryvalue) (op)<br />
### Boundary values list
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#BoundaryValue`
Description | <p>Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:hasBoundaryLimit](Boundaryvalue) (op) **max** 1 [isoprops:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />[isoprops:hasBoundaryLimit](Boundaryvalue) (op) **max** 1 [isoprops:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
In domain of |[isoprops:hasBoundaryLimit](Boundaryvalue) (op)<br />
In range of |[isoprops:hasBoundary](Grenzwerte) (op)<br />
### Definierender Wert-Item
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
Description | <p>In case of an array, this attribute provides the defining values when applicable, the datatype is given by the attribute PA030</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:DefiningValueItem](DefinierenderWert-Item) **min** 1<br />
In domain of |[isoprops:hasDefiningValueItem](Definingvalue) (op)<br />
In range of |[isoprops:hasDefiningValue](DefinierendeWerte) (op)<br />
### Datenkatalog
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Dictionary`
Description | <p>Zentralisiertes Repository von Informationen ueber Daten, wie z. B. Bedeutung, Beziehungen zu anderen Daten, Ursprung, Verwendung und Format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[isoprops:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op) **min** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />
In domain of |[isoprops:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Reference document
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DictionaryReferenceDocument`
Description | <p>Publikation, die hinzugezogen wird, um bestimmte Informationen zu finden, insbesondere in einer technischen oder wissenschaftlichen Domaene</p>
Super-classes |[dcat:Distribution](http://www.w3.org/ns/dcat#Distribution) (c)<br />
Restrictions |[isoprops:hasPropertyGroupReference](hatMerkmalsgruppenreferenz) (op) **exactly** 1<br />
In range of |[isoprops:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
### Dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DictionarySubset`
Description | <p>Defines a subset or subgrouping of a data catalog</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[isoprops:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op) **exactly** 1<br />[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />
In domain of |[isoprops:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
In range of |[isoprops:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Digital format item
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DigitalFormatItem`
Description | <p>Pair for digital text type (precision, unit) Precision is the number of significant digits</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:Precision](Toleranz) (dp) **exactly** 1<br />[isoprops:hasUnit](hatEinheit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
In domain of |[isoprops:Precision](Toleranz) (dp)<br />
In range of |[isoprops:hasDigitalFormat](Digitalformat) (op)<br />
### External Dictionary Reference
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#ExternalDictionaryReference`
Description | <p>Paar (interner Merkmalsbezeichner, entsprechender Datenkatalog-Bezeichner) Dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[http://inf.bi.rub.de/ontology/dt#hasExternalDictionary](http://inf.bi.rub.de/ontology/dt#hasExternalDictionary) **exactly** 1<br />[http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty](http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty) **exactly** 1<br />
In range of |[isoprops:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />
### Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#GroupOfProperties`
Description | <p>Sammlung, die es ermoeglicht, die Merkmale vorauszuplanen oder zu organisieren</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[isoprops:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[isoprops:hasParentGroupOfProperties](Parentgroupofproperties) (op) **min** 0 [isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[isoprops:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[isoprops:CountryOfUse](LandderVerwendung) (dp) **min** 1<br />[isoprops:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[isoprops:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[isoprops:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />[isoprops:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op) **min** 0 [isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:DeprecationExplanation](DeprecationExplanation) (dp) **max** 1<br />[isoprops:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[isoprops:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[isoprops:Tolerance](Tolerance) (dp) **min** 0<br />[isoprops:CountryOfOrigin](Countryoforigin) (dp) **exactly** 1<br />[isoprops:VisualRepresentation](Visualrepresentation) (dp) **min** 1<br />[isoprops:DateOfLastChange](DatumderletztenAenderung) (dp) **min** 0<br />[isoprops:Status](Status) (dp) **exactly** 1<br />[isoprops:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[isoprops:SubdivisionOfUse](UnterteilungderVerwendung) (dp) **min** 0<br />[isoprops:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op) **min** 0 [isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op) **min** 0 [isoprops:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[isoprops:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[isoprops:DeprecationExplanation](DeprecationExplanation) (dp) **min** 0<br />[isoprops:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[isoprops:hasParentGroupOfProperties](Parentgroupofproperties) (op) **max** 1 [isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp) **exactly** 1<br />
In domain of |[isoprops:DateOfDeactivation](Dateofdeactivation) (dp)<br />[isoprops:VisualRepresentation](Visualrepresentation) (dp)<br />[isoprops:VersionNumber](Versionsnummer) (dp)<br />[isoprops:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp)<br />[isoprops:SubdivisionOfUse](UnterteilungderVerwendung) (dp)<br />[isoprops:Status](Status) (dp)<br />[isoprops:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[isoprops:DeprecationExplanation](DeprecationExplanation) (dp)<br />[isoprops:hasRelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries) (op)<br />[isoprops:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[isoprops:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[isoprops:DateOfActivation](Dateofactivation) (dp)<br />[isoprops:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[isoprops:NameInLanguage](NameinSpracheN) (dp)<br />[isoprops:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />[isoprops:DateOfLastChange](DatumderletztenAenderung) (dp)<br />[isoprops:DateOfCreation](Dateofcreation) (dp)<br />[isoprops:hasParentGroupOfProperties](Parentgroupofproperties) (op)<br />[isoprops:DateOfVersion](DatumderVersion) (dp)<br />[isoprops:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[isoprops:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[isoprops:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[isoprops:CountryOfOrigin](Countryoforigin) (dp)<br />[isoprops:CountryOfUse](LandderVerwendung) (dp)<br />
In range of |[isoprops:hasParentGroupOfProperties](Parentgroupofproperties) (op)<br />[isoprops:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[isoprops:hasPropertyGroupReference](hatMerkmalsgruppenreferenz) (op)<br />[isoprops:hasGroupOfProperties](Group(s)ofproperties) (op)<br />[isoprops:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[isoprops:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op)<br />
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#PhysicalQuantity`
Description | <p>Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
### Possible value in language N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#PossibleValues`
Description | <p>Moeglicher Wert fuer das Merkmal und Sprache Werte koennen String oder Zahlen sein</p>
Usage Note | PA039
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[isoprops:hasPossibleValues](ListofpossiblevaluesinlanguageN) (op)<br />
### Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Property`
Description | <p>Inherent or acquired feature of an item</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[isoprops:hasGroupOfProperties](Group(s)ofproperties) (op) **min** 1 [isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:hasPossibleValues](ListofpossiblevaluesinlanguageN) (op) **min** 0<br />[isoprops:DescriptionInLanguage](BeschreibunginSpracheN) (dp) **min** 0<br />[isoprops:hasParameterOfTheDynamicProperty](Parametersofthedynamicproperty) (op) **min** 0 [isoprops:Property](Merkmal) (c)<br />[isoprops:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[isoprops:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[isoprops:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[isoprops:SubdivisionOfUse](UnterteilungderVerwendung) (dp) **min** 0<br />[isoprops:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[isoprops:ExampleInLanguage](ExampleinlanguageN) (dp) **min** 0<br />[isoprops:CountryOfOrigin](Countryoforigin) (dp) **max** 1<br />[isoprops:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op) **min** 0 [isoprops:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />[isoprops:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[isoprops:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[isoprops:Status](Status) (dp) **exactly** 1<br />[isoprops:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[isoprops:NameOfTheDefiningValues](NamederdefinierendenWerte) (dp) **min** 0<br />[isoprops:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[isoprops:VisualRepresentation](Visualrepresentation) (dp) **min** 0<br />[isoprops:hasDigitalFormat](Digitalformat) (op) **min** 0 [isoprops:DigitalFormatItem](Digitalformatitem) (c)<br />[isoprops:hasUnit](hatEinheit) (op) **min** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[isoprops:CountryOfOrigin](Countryoforigin) (dp) **min** 0<br />[isoprops:DeprecationExplanation](DeprecationExplanation) (dp) **min** 0<br />[isoprops:hasBoundary](Grenzwerte) (op) **exactly** 1 [isoprops:BoundaryValue](Boundaryvalueslist) (c)<br />[isoprops:DeprecationExplanation](DeprecationExplanation) (dp) **max** 1<br />[isoprops:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op) **min** 0 [isoprops:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[isoprops:hasPossibleValues](ListofpossiblevaluesinlanguageN) (op) **min** 0 [isoprops:PossibleValues](PossiblevalueinlanguageN) (c)<br />[isoprops:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[isoprops:hasTextFormat](Textformat) (op) **min** 0 [isoprops:TextFormatItem](Textformatitem) (c)<br />[isoprops:DateOfLastChange](DatumderletztenAenderung) (dp) **min** 0<br />[isoprops:hasDefiningValue](DefinierendeWerte) (op) **min** 0 [isoprops:DefiningValuesList](ListedefinierenderWerte) (c)<br />[isoprops:isReplacedByProperty](ListeersetzenderMerkmale) (op) **min** 0 [isoprops:Property](Merkmal) (c)<br />[isoprops:hasPhysicalQuantity](Physicalquantity) (op) **min** 1<br />[isoprops:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[isoprops:replacesProperties](Listofreplacedproperties) (op) **min** 0 [isoprops:Property](Merkmal) (c)<br />[isoprops:Tolerance](Tolerance) (dp) **min** 0<br />[isoprops:DynamicProperty](DynamicProperty) (dp) **exactly** 1<br />[isoprops:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />[isoprops:MethodOfMeasurement](Messverfahren) (dp) **min** 0<br />[isoprops:DataType](Datentyp(GUID)) (dp) **exactly** 1<br />[isoprops:CountryOfUse](LandderVerwendung) (dp) **min** 1<br />[isoprops:hasConnectedProperty](Connectedproperties) (op) **min** 0 [isoprops:Property](Merkmal) (c)<br />
In domain of |[isoprops:DeprecationExplanation](DeprecationExplanation) (dp)<br />[isoprops:hasUnit](hatEinheit) (op)<br />[isoprops:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />[isoprops:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[isoprops:Status](Status) (dp)<br />[isoprops:isReplacedByProperty](ListeersetzenderMerkmale) (op)<br />[isoprops:DateOfActivation](Dateofactivation) (dp)<br />[isoprops:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />[isoprops:NameInLanguage](NameinSpracheN) (dp)<br />[isoprops:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[isoprops:DateOfLastChange](DatumderletztenAenderung) (dp)<br />[isoprops:DateOfCreation](Dateofcreation) (dp)<br />[isoprops:DateOfVersion](DatumderVersion) (dp)<br />[isoprops:hasDigitalFormat](Digitalformat) (op)<br />[isoprops:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[isoprops:hasPhysicalQuantity](Physicalquantity) (op)<br />[isoprops:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[isoprops:hasParameterOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />[isoprops:replacesProperties](Listofreplacedproperties) (op)<br />[isoprops:CountryOfOrigin](Countryoforigin) (dp)<br />[isoprops:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op)<br />[isoprops:ExampleInLanguage](ExampleinlanguageN) (dp)<br />[isoprops:CountryOfUse](LandderVerwendung) (dp)<br />[isoprops:DateOfDeactivation](Dateofdeactivation) (dp)<br />[isoprops:VisualRepresentation](Visualrepresentation) (dp)<br />[isoprops:hasConnectedProperty](Connectedproperties) (op)<br />[isoprops:VersionNumber](Versionsnummer) (dp)<br />[isoprops:hasGroupOfProperties](Group(s)ofproperties) (op)<br />[isoprops:Tolerance](Tolerance) (dp)<br />[isoprops:hasPossibleValues](ListofpossiblevaluesinlanguageN) (op)<br />[isoprops:SubdivisionOfUse](UnterteilungderVerwendung) (dp)<br />[isoprops:hasDefiningValue](DefinierendeWerte) (op)<br />[isoprops:DataType](Datentyp(GUID)) (dp)<br />[isoprops:hasTextFormat](Textformat) (op)<br />[isoprops:DescriptionInLanguage](BeschreibunginSpracheN) (dp)<br />[isoprops:hasBoundary](Grenzwerte) (op)<br />[isoprops:MethodOfMeasurement](Messverfahren) (dp)<br />[isoprops:DateOfRevision](DatumderUeberarbeitung) (dp)<br />
In range of |[isoprops:isReplacedByProperty](ListeersetzenderMerkmale) (op)<br />[isoprops:hasParameterOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />[isoprops:hasPropertyReference](hatMerkmalreferenz) (op)<br />[isoprops:hasConnectedProperty](Connectedproperties) (op)<br />[isoprops:replacesProperties](Listofreplacedproperties) (op)<br />
### Symbol des Merkmals in einer gegebenen Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#SymbolOfTheProperty`
Description | <p>Paar (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:Symbol](Symbol) (dp) **exactly** 1<br />[isoprops:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op) **exactly** 1 [isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
In domain of |[isoprops:Symbol](Symbol) (dp)<br />
In range of |[isoprops:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />
### Text format item
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#TextFormatItem`
Description | <p>Paar fuer den Texttyp (Verschluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[isoprops:Encoding](Kodierung) (dp) **exactly** 1<br />[isoprops:NumberOfCharacters](AnzahlderZeichen) (dp) **exactly** 1<br />
In domain of |[isoprops:Encoding](Kodierung) (dp)<br />[isoprops:NumberOfCharacters](AnzahlderZeichen) (dp)<br />
In range of |[isoprops:hasTextFormat](Textformat) (op)<br />

## Object Properties
[Grenzwerte](#Grenzwerte),
[Boundary value](#Boundaryvalue),
[Connected properties](#Connectedproperties),
[Definierende Werte](#DefinierendeWerte),
[Defining value](#Definingvalue),
[has relation to a reference document](#hasrelationtoareferencedocument),
[hat Teilmenge eines Katalogs](#hatTeilmengeeinesKatalogs),
[Digital format](#Digitalformat),
[has external dictionary](#hasexternaldictionary),
[has external dictionary property](#hasexternaldictionaryproperty),
[hat externe Dictionary Referenz](#hatexterneDictionaryReferenz),
[Gegebene Merkmalsgruppe](#GegebeneMerkmalsgruppe),
[Group(s) of properties](#Group(s)ofproperties),
[Parameters of the dynamic property](#Parametersofthedynamicproperty),
[Parent group of properties](#Parentgroupofproperties),
[Physical quantity](#Physicalquantity),
[List of possible values in language N](#ListofpossiblevaluesinlanguageN),
[has property](#hasproperty),
[hat Merkmalsgruppenreferenz](#hatMerkmalsgruppenreferenz),
[hat Merkmalreferenz](#hatMerkmalreferenz),
[Relations of the group of properties identifiers in the interconnected data dictionaries](#Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries),
[Symbole des Merkmals in einer gegebenen Merk-malsgruppe](#SymboledesMerkmalsineinergegebenenMerk-malsgruppe),
[Textformat](#Textformat),
[hat Einheit](#hatEinheit),
[Liste ersetzender Merkmalsgruppen](#ListeersetzenderMerkmalsgruppen),
[Liste ersetzender Merkmale](#ListeersetzenderMerkmale),
[Liste ersetzter Merkmalsgruppen](#ListeersetzterMerkmalsgruppen),
[List of replaced properties](#Listofreplacedproperties),
[](Grenzwerte)
### Grenzwerte
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasBoundary`
Description | Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:BoundaryValue](Boundaryvalueslist) (c)<br />
[](Boundaryvalue)
### Boundary value
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasBoundaryLimit`
Description | Einzelnes Grenzwertintervall
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:BoundaryValue](Boundaryvalueslist) (c)<br />
Range(s) |[isoprops:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
[](Connectedproperties)
### Connected properties
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasConnectedProperty`
Description | List of the globally unique identifier of the connected properties (attribute PA001); the value of one property is related to the values of the other ones. For example, a sound absorption coefficient is given for a specific frequency, in this case sound absorption and frequency are connected properties
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:Property](Merkmal) (c)<br />
[](DefinierendeWerte)
### Definierende Werte
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDefiningValue`
Description | Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
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
Range(s) |[isoprops:DefiningValueItem](DefinierenderWert-Item) (c)<br />
[](hasrelationtoareferencedocument)
### has relation to a reference document
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDictionaryReferenceDocument`
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[isoprops:DictionarySubset](Dictionarysubset) (c)<br />
Range(s) |[isoprops:DictionaryReferenceDocument](Referencedocument) (c)<br />
[](hatTeilmengeeinesKatalogs)
### hat Teilmenge eines Katalogs
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDictionarySubset`
Super-properties |[dcat:dataset](http://www.w3.org/ns/dcat#dataset)<br />
Domain(s) |[isoprops:Dictionary](Datenkatalog) (c)<br />
Range(s) |[isoprops:DictionarySubset](Dictionarysubset) (c)<br />
[](Digitalformat)
### Digital format
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasDigitalFormat`
Description | Pair for digital text type (precision, unit) Precision is the number of significant digits
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
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
[](hatexterneDictionaryReferenz)
### hat externe Dictionary Referenz
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasExternalDictionaryReference`
Description | Liste von Paaren (interner Merk-malsbezeichner, entsprechender Datenkatalog-Bezeichner) dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden
Usage Note | PA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />
[](GegebeneMerkmalsgruppe)
### Gegebene Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasGivenGroupOfProperties`
Description | Global eindeutiger Bezeichner einer Merkmalsgruppe (Attribut GA001) fuer das dem Merkmal zugeordnetem Symbol
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Group(s)ofproperties)
### Group(s) of properties
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasGroupOfProperties`
Description | Liste von global eindeutigen Bezeichnern von Merkmalsgruppen (Attribut GA001), denen das Merkmal angehoert
Usage Note | PA021
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Parametersofthedynamicproperty)
### Parameters of the dynamic property
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasParameterOfTheDynamicProperty`
Description | List of GUIDS of properties which are parameters of the function for a dynamic property
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:Property](Merkmal) (c)<br />
[](Parentgroupofproperties)
### Parent group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasParentGroupOfProperties`
Description | Enables a sub-group to be linked to a parent group via their globally unique identifiers (attribute GA001) Any property attached to a group is inherited by the sub-group(s)
Usage Note | GA023
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Physicalquantity)
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasPhysicalQuantity`
Description | List of pairs (physical quantity | language) Physical quantities are expressed in International System (SI) units Non-physical quantities such as text are expressed with the value "without" --> http://qudt.org/vocab/quantitykind/Dimensionless This is equivalent to a measure in ISO 16739-1 and ISO 10303 Only one physical quantity can be attached to a property. This attribute is used to provide the quantity in plain text with all the needed translations
Usage Note | PA027
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[qudt:QuantityKind](http://qudt.org/schema/qudt/QuantityKind) (c)<br />
[](ListofpossiblevaluesinlanguageN)
### List of possible values in language N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasPossibleValues`
Description | Liste von Paaren (moeglicher Wert fuer das Merkmal und Sprache) Werte koennen String oder Zahlen sein
Usage Note | PA039
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:PossibleValues](PossiblevalueinlanguageN) (c)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasProperty`
Description | Attaches a property to a feature of interest (FOI)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[isoprops:AssignedProperty](Assignedproperty) (c)<br />
[](hatMerkmalsgruppenreferenz)
### hat Merkmalsgruppenreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasPropertyGroupReference`
Description | Fuegt eine Merkmalsgruppe (oberstes in der Hierarchie) zu einer isoprops:ReferenceDocument hinzu
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:ReferenceDocument](https://w3id.org/isoprops#ReferenceDocument) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](hatMerkmalreferenz)
### hat Merkmalreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasPropertyReference`
Description | Fuegt ein Merkmal zu einer Merkmalszuweisung hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:AssignedProperty](Assignedproperty) (c)<br />
Range(s) |[isoprops:Property](Merkmal) (c)<br />
[](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries)
### Relations of the group of properties identifiers in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasRelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | Liste von Paaren (inter-ner Bezeichner der Merkmalsgruppe, ent-sprechender Daten-katalog-Bezeichner) dieses Attribut sollte fuer die Kompatibilitaet zwischen bereits vorhandenen Merk-malsgruppen verwen-det werden
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](SymboledesMerkmalsineinergegebenenMerk-malsgruppe)
### Symbole des Merkmals in einer gegebenen Merk-malsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasSymbolsOfTheProperty`
Description | Liste von Paaren (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />
[](Textformat)
### Textformat
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasTextFormat`
Description | Paar fuer den Texttyp (Verschluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:TextFormatItem](Textformatitem) (c)<br />
[](hatEinheit)
### hat Einheit
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#hasUnit`
Description | Eine Einheit zur Darstellung einer Skala, die es ermoeglicht, einen Wert zu messen es ist moeglich, dieses Attribut zu verwenden, um zu erlaeutern, dass dem Merkmal keine Einheit zugeordnet ist, indem einheitslos verwendet wird --> http://qudt.org/vocab/unit/UNITLESS
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />[isoprops:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](ListeersetzenderMerkmalsgruppen)
### Liste ersetzender Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#isReplacedByGroupOfProperties`
Description | Liste von globalen Bezeichnern fuer die ersetzenden Merkmalsgruppen
Usage Note | GA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](ListeersetzenderMerkmale)
### Liste ersetzender Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#isReplacedByProperty`
Description | global eindeutiger Bezeichner (Attribut PA001) des ersetzenden Merkmals (oder der Merkmale)
Usage Note | PA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:Property](Merkmal) (c)<br />
[](ListeersetzterMerkmalsgruppen)
### Liste ersetzter Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#replacesGroupOfProperties`
Description | List of globally unique identifiers of the replaced groups of properties
Usage Note | GA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Listofreplacedproperties)
### List of replaced properties
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#replacesProperties`
Description | Globally unique identifier of the replaced property (or properties)
Usage Note | PA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[isoprops:Property](Merkmal) (c)<br />

## Datatype Properties
[Kategorie der Merkmalsgruppe](#KategoriederMerkmalsgruppe),
[Country of origin](#Countryoforigin),
[Land der Verwendung](#LandderVerwendung),
[Erlaeuterung fuer die Ablehnung](#ErlaeuterungfuerdieAblehnung),
[Datentyp (GUID)](#Datentyp(GUID)),
[Date of activation](#Dateofactivation),
[Date of creation](#Dateofcreation),
[Date of deactivation](#Dateofdeactivation),
[Datum der letzten Aenderung](#DatumderletztenAenderung),
[Datum der Ueberarbeitung](#DatumderUeberarbeitung),
[Datum der Version](#DatumderVersion),
[Definition of in language N](#DefinitionofinlanguageN),
[Erlaeuterung fuer die Ablehnung](#DeprecationExplanation),
[Beschreibung in Sprache N](#BeschreibunginSpracheN),
[Dynamic Property](#DynamicProperty),
[Kodierung](#Kodierung),
[Example in language N](#ExampleinlanguageN),
[Global eindeutiger Bezeichner (GUID)](#GlobaleindeutigerBezeichner(GUID)),
[inclusive](#inclusive),
[Messverfahren](#Messverfahren),
[Name in Sprache N](#NameinSpracheN),
[Name der definierenden Werte](#NamederdefinierendenWerte),
[Anzahl der Zeichen](#AnzahlderZeichen),
[Toleranz](#Toleranz),
[Nummer der ueberarbeitung](#Nummerderueberarbeitung),
[Status](#Status),
[Unterteilung der Verwendung](#UnterteilungderVerwendung),
[Symbol](#Symbol),
[Tolerance](#Tolerance),
[Versionsnummer](#Versionsnummer),
[Visual representation](#Visualrepresentation),
[](KategoriederMerkmalsgruppe)
### Kategorie der Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#CategoryOfGroupOfProperties`
Description | Specifies the category of the created property group
Usage Note | GA022
Example | ````Reference document`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Countryoforigin)
### Country of origin
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#CountryOfOrigin`
Description | Land, aus dem die Anforderung an dieses Merkmal/dieser Merkmalsgruppe stammt
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](LandderVerwendung)
### Land der Verwendung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#CountryOfUse`
Description | Land (Gruppe von Laendern, Kon-tinent), in dem das Merkmal/die Merkmalsgruppe fuer den Markt, auf dem die Beteiligten arbeiten, relevant ist
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ErlaeuterungfuerdieAblehnung)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#CreatorsLanguage`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property; this explanation has to be written in international English (EN)
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Datentyp(GUID))
### Datentyp (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DataType`
Description | Format fuer die Angabe des Wertes des Merkmals dies kann aus einer Soft-ware-Perspektive als Speiche-rungsart verstanden werden im Falle eines dynamischen Merkmals ist der Wert dieses Attributs der Datentyp des Er-gebnisses der Berechnung mit der Gleichung
Usage Note | PA030
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Dateofactivation)
### Date of activation
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfActivation`
Description | Date after when the property can be used
Usage Note | PA04/GA04
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofcreation)
### Date of creation
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfCreation`
Description | Date of validation of the property creation request by experts
Usage Note | PA003/GA003
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofdeactivation)
### Date of deactivation
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfDeactivation`
Description | Date of deactivation
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderletztenAenderung)
### Datum der letzten Aenderung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfLastChange`
Description | Date of validation of the last change request by experts
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderUeberarbeitung)
### Datum der Ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfRevision`
Description | Datum der Ueberarbeitung
Usage Note | PA006/GA006
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderVersion)
### Datum der Version
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DateOfVersion`
Description | Date of version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DefinitionofinlanguageN)
### Definition of in language N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DefinitionInLanguage`
Description | List of pairs (definition of the property/group of properties, language)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DeprecationExplanation)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DeprecationExplanation`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property/group of properties; this explanation has to be written in international English (EN)
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](BeschreibunginSpracheN)
### Beschreibung in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#DescriptionInLanguage`
Description | List of pairs (Description of the property, language)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
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
[](Kodierung)
### Kodierung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Encoding`
Description | Die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ExampleinlanguageN)
### Example in language N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#ExampleInLanguage`
Description | Liste von Paaren (Beispiel des Merkmals, Sprache)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](GlobaleindeutigerBezeichner(GUID))
### Global eindeutiger Bezeichner (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#GloballyUniqueIdentifier`
Description | Unique identifier generated using the algorithm denoted in RFC 4122
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](inclusive)
### inclusive
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Inclusive`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />[isoprops:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](Messverfahren)
### Messverfahren
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#MethodOfMeasurement`
Description | Evaluation of construction products to ensure their fitness according to requirements in harmonised technical specifications
Usage Note | PA029
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](NameinSpracheN)
### Name in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#NameInLanguage`
Description | Liste von Paaren (Name des Merkmals und Sprache) Dieses Attribut kann verwendet werden, um Synonyme fuer verschiedene Domaenen hinzuzufuegen
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](NamederdefinierendenWerte)
### Name der definierenden Werte
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#NameOfTheDefiningValues`
Description | Im Falle eines Feldes liefert dieses Attribut die Namen der Spaltenkoepfe, festgelegt als Liste von Paaren (Name, Sprache)
Usage Note | PA034
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](AnzahlderZeichen)
### Anzahl der Zeichen
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#NumberOfCharacters`
Description | The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Toleranz)
### Toleranz
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Precision`
Description | Praezision ist die Anzahl signifi-kanter Stellen
Usage Note | PA037
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:DigitalFormatItem](Digitalformatitem) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Nummerderueberarbeitung)
### Nummer der ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#RevisionNumber`
Description | This revision number allows tracking of minor changes e.g. new translation, changes of typos: if the version number changes, the revision number starts again at 1 Experts decide if a new revision number can be applied or if a new revision is needed
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Status)
### Status
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Status`
Description | Status des Merkmals waehrend seines Lebenszyklus
Usage Note | PA002/GA002
Example | ````active`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](UnterteilungderVerwendung)
### Unterteilung der Verwendung
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#SubdivisionOfUse`
Description | Documented geographical region of use of the group of properties
Usage Note | PA025/GA020
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />[isoprops:Property](Merkmal) (c)<br />
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
[](Tolerance)
### Tolerance
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#Tolerance`
Description | Fuer numerische Werte; der Gesamtbetrag, um den eine be-stimmte Einheit schwanken darf; sie ist die Differenz zwischen dem Hoechstwert und dem Mindestwert fuer die Einheit
Usage Note | PA036
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Versionsnummer)
### Versionsnummer
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#VersionNumber`
Description | This version number allows tracking of major changes. Experts decide if a new version number must be applied
Usage Note | PA009/GA009
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Visualrepresentation)
### Visual representation
Property | Value
--- | ---
IRI | `https://w3id.org/isoprops#VisualRepresentation`
Description | Bildliche Darstellung des Merkmals durch Skizzen, Fotos, Videos oder sonstige Multimedia-Objekte
Usage Note | PA023/GA018
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[isoprops:Property](Merkmal) (c)<br />[isoprops:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Description | Code that can be used to identify the attribute
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