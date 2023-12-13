Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# The Interconnected Data Dictionary Ontology (IDDO)

## Metadata
* **IRI**
  * `https://w3id.org/iddo/v2`
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
  * 2022-10-18
* **Issued**
  * 2021-12-06
* **Version Information**
  * v2.0
* **Version IRI**
  * [https://w3id.org/iddo/v2](https://w3id.org/iddo/v2)
* **Imports**
  * [http://inf.bi.rub.de/ontology/dt](http://inf.bi.rub.de/ontology/dt)
* **License**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
* **Ontology RDF**
  * RDF ([iddo.ttl](turtle))
* **Code Repository**
  * [https://github.com/RUB-Informatik-im-Bauwesen/iddo](https://github.com/RUB-Informatik-im-Bauwesen/iddo)
### Description
<p>The interconnected data dictionary ontology maps the data model of the ISO 23386 for the describing, creating, and maintenance of properties in interconnected data dictionaries.</p>
<p>The namespace for IDDO terms is <a href="https://w3id.org/iddo">https://w3id.org/iddo</a></p>
<p>The preferred prefix for the IDDO namespace is <code>iddo</code>.</p>
<h2>Ontology Overview</h2>
<p><img alt="IDDO Ontology" src="Ontology_Overview.png" title="Ontology" /></p>
<h2>Assigning an IDDO Property to a Feature of Interest</h2>
<p><img alt="Property_Assignment" src="Property_Assignment.png" title="Property_Assignment" /></p>
<h2>Relation between DCAT vocabulary and the IDDO ontology</h2>
<p><img alt="DataCatalog_Overview" src="DataCatalog_Overview.png" title="DataCatalog_Overview" /></p>
* **History Note:** <p>v2.0: update</p>
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
[Datenkatalog](#Datenkatalog),
[Defining value item](#Definingvalueitem),
[Defining values list](#Definingvalueslist),
[Dictionary subset](#Dictionarysubset),
[Digitales Format-Item](#DigitalesFormat-Item),
[External Dictionary Reference ](#ExternalDictionaryReference),
[Grenzwertliste](#Grenzwertliste),
[Group of properties](#Groupofproperties),
[Liste moeglicher Werte in Sprache N](#PossibleValueInLanguageN),
[Maximum Boundary Limit](#MaximumBoundaryLimit),
[Minimum Boundary Limit](#MinimumBoundaryLimit),
[Physical quantity](#Physicalquantity),
[Property](#Property),
[Referenzdokument](#Referenzdokument),
[Symbol of the property in a given property group](#Symbolofthepropertyinagivenpropertygroup),
[Text format item](#Textformatitem),
[Zugewiesenes Merkmal](#ZugewiesenesMerkmal),
### Zugewiesenes Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#AssignedProperty`
Description | <p>Represents the assignment of a property and a property state to a feature of interest (FOI).</p>
Super-classes |[http://www.w3id.org/opm#Property](http://www.w3id.org/opm#Property) (c)<br />
Restrictions |[iddo:hasPropertyReference](hatMerkmalreferenz) (op) **exactly** 1<br />[http://www.w3id.org/opm#hasPropertyState](http://www.w3id.org/opm#hasPropertyState) **min** 1<br />
In domain of |[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />
In range of |[iddo:hasProperty](hasproperty) (op)<br />
### Maximum Boundary Limit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMax`
Description | <p>Boundary limit  interval consisting of the the upper (maxValue) interval boundary</p>
Usage Note | PA040
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Inclusive](inclusive) (dp) **exactly** 1<br />[iddo:hasUnit](hatEinheit) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />
In domain of |[iddo:Inclusive](inclusive) (dp)<br />[iddo:hasUnit](hatEinheit) (op)<br />
### Minimum Boundary Limit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMin`
Description | <p>Grenzwertintervall bestehend aus der unteren(minValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasUnit](hatEinheit) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />[iddo:Inclusive](inclusive) (dp) **exactly** 1<br />
In domain of |[iddo:hasUnit](hatEinheit) (op)<br />[iddo:Inclusive](inclusive) (dp)<br />
In range of |[iddo:hasBoundaryLimit](Grenzwert) (op)<br />
### Grenzwertliste
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValue`
Description | <p>Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasBoundaryLimit](Grenzwert) (op) **max** 1 [iddo:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />[iddo:hasBoundaryLimit](Grenzwert) (op) **max** 1 [iddo:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
In domain of |[iddo:hasBoundaryLimit](Grenzwert) (op)<br />
In range of |[iddo:hasBoundary](Boundaryvalues) (op)<br />
### Defining value item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValueItem`
Description | <p>Enthaelt einen definierenden Wert eines Arrays in Form eines Literals</p>
Usage Note | PA035
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:hasDefiningValueItem](DefinierenderWert) (op)<br />
### Defining values list
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValuesList`
Description | <p>Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DefiningValueItem](Definingvalueitem) **min** 1<br />
In domain of |[iddo:hasDefiningValueItem](DefinierenderWert) (op)<br />
In range of |[iddo:hasDefiningValue](DefinierendeWerte) (op)<br />
### Datenkatalog
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dictionary`
Description | <p>Zentralisiertes Repository von Informationen ueber Daten, wie z. B. Bedeutung, Beziehungen zu anderen Daten, Ursprung, Verwendung und Format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />[iddo:hasDictionarySubset](hasdictionarysubset) (op) **min** 1<br />[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />
In domain of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Referenzdokument
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionaryReferenceDocument`
Description | <p>Publikation, die hinzugezogen wird, um bestimmte Informationen zu finden, insbesondere in einer technischen oder wissenschaftlichen Domaene</p>
Super-classes |[dcat:Distribution](http://www.w3.org/ns/dcat#Distribution) (c)<br />
Restrictions |[iddo:hasPropertyGroupReference](hatMerkmalsgruppenreferenz) (op) **exactly** 1<br />
In range of |[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op)<br />
### Dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionarySubset`
Description | <p>Defines a subset or subgrouping of a data catalog</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op) **exactly** 1<br />
In domain of |[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op)<br />
In range of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Digitales Format-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormatItem`
Description | <p>Pair for digital text type (precision, unit) Precision is the number of significant digits</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasUnit](hatEinheit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[iddo:Precision](Toleranz) (dp) **exactly** 1<br />
In domain of |[iddo:Precision](Toleranz) (dp)<br />
In range of |[iddo:hasDigitalFormat](Digitalformat) (op)<br />
### External Dictionary Reference 
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExternalDictionaryReference`
Description | <p>Paar (interner Merkmalsbezeichner, entsprechender Datenkatalog-Bezeichner) Dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty](http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty) **exactly** 1<br />[http://inf.bi.rub.de/ontology/dt#hasExternalDictionary](http://inf.bi.rub.de/ontology/dt#hasExternalDictionary) **exactly** 1<br />
In range of |[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />
### Group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupOfProperties`
Description | <p>Collection enabling the properties to be prearranged or organized</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp) **exactly** 1<br />[iddo:VisualRepresentation](Visualrepresentation) (dp) **min** 1<br />[iddo:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />[iddo:hasDimension](Dimension) (op) **min** 0<br />[iddo:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **exactly** 1<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[iddo:hasParentGroupOfProperties](Parentgroupofproperties) (op) **min** 0 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[iddo:hasParentGroupOfProperties](Parentgroupofproperties) (op) **max** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />
In domain of |[iddo:hasParentGroupOfProperties](Parentgroupofproperties) (op)<br />[iddo:NameInLanguage](NameinlanguageN) (dp)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:hasRelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp)<br />[iddo:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:DateOfCreation](Dateofcreation) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:DateOfActivation](Dateofactivation) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp)<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />
In range of |[iddo:hasPropertyGroupReference](hatMerkmalsgruppenreferenz) (op)<br />[iddo:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:hasGroupOfProperties](Group(s)ofproperties) (op)<br />[iddo:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:hasParentGroupOfProperties](Parentgroupofproperties) (op)<br />
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PhysicalQuantity`
Description | <p>Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
### Liste moeglicher Werte in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PossibleValueInLanguageN`
Description | <p>Possible value for the property and language Values can be string or numbers</p>
Usage Note | PA039
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:hasPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />
### Property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Property`
Description | <p>Inhaerente oder erworbene Eigenschaft eines Datenelements</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp) **min** 0<br />[iddo:ExampleInLanguage](ExampleinlanguageN) (dp) **min** 0<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:hasPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossibleValueInLanguageN) (c)<br />[iddo:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **max** 1<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:hasDefiningValue](DefinierendeWerte) (op) **min** 0 [iddo:DefiningValuesList](Definingvalueslist) (c)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp) **min** 0<br />[iddo:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[iddo:hasBoundary](Boundaryvalues) (op) **exactly** 1 [iddo:BoundaryValue](Grenzwertliste) (c)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:hasUnit](hatEinheit) (op) **min** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **min** 0<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:hasPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0<br />[iddo:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[iddo:replacesProperties](ListeersetzterMerkmale) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:NameOfTheDefiningValues](NamederdefinierendenWerte) (dp) **min** 0<br />[iddo:hasGroupOfProperties](Group(s)ofproperties) (op) **min** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:DynamicProperty](DynamicProperty) (dp) **exactly** 1<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[iddo:DataType](Datentyp(GUID)) (dp) **exactly** 1<br />[iddo:hasDigitalFormat](Digitalformat) (op) **min** 0 [iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />[iddo:hasParameterOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:hasTextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](Textformatitem) (c)<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp) **min** 0<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op) **min** 0 [iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:hasPhysicalQuantity](PhysikalischeGroesse) (op) **min** 1<br />[iddo:isReplacedByProperty](Listofreplacingproperties) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />
In domain of |[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:hasPhysicalQuantity](PhysikalischeGroesse) (op)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp)<br />[iddo:hasBoundary](Boundaryvalues) (op)<br />[iddo:replacesProperties](ListeersetzterMerkmale) (op)<br />[iddo:hasTextFormat](Textformat) (op)<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp)<br />[iddo:NameInLanguage](NameinlanguageN) (dp)<br />[iddo:hasGroupOfProperties](Group(s)ofproperties) (op)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp)<br />[iddo:DataType](Datentyp(GUID)) (dp)<br />[iddo:hasDigitalFormat](Digitalformat) (op)<br />[iddo:ExampleInLanguage](ExampleinlanguageN) (dp)<br />[iddo:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />[iddo:hasPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />[iddo:hasDefiningValue](DefinierendeWerte) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:hasDimension](Dimension) (op)<br />[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:isReplacedByProperty](Listofreplacingproperties) (op)<br />[iddo:hasParameterOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:hasUnit](hatEinheit) (op)<br />[iddo:DateOfCreation](Dateofcreation) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:DateOfActivation](Dateofactivation) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:Tolerance](Tolerance) (dp)<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />
In range of |[iddo:hasParameterOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />[iddo:isReplacedByProperty](Listofreplacingproperties) (op)<br />[iddo:replacesProperties](ListeersetzterMerkmale) (op)<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op)<br />
### Symbol of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolOfTheProperty`
Description | <p>Pair (symbol of the property, globally unique identifier of the group of properties (attribute GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Symbol](Symbol) (dp) **exactly** 1<br />[iddo:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op) **exactly** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />
In domain of |[iddo:Symbol](Symbol) (dp)<br />
In range of |[iddo:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />
### Text format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormatItem`
Description | <p>Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Encoding](Kodierung) (dp) **exactly** 1<br />[iddo:NumberOfCharacters](NumberofCharacters) (dp) **exactly** 1<br />
In domain of |[iddo:NumberOfCharacters](NumberofCharacters) (dp)<br />[iddo:Encoding](Kodierung) (dp)<br />
In range of |[iddo:hasTextFormat](Textformat) (op)<br />

## Object Properties
[Boundary values](#Boundaryvalues),
[Grenzwert](#Grenzwert),
[Verbundene Merkmale](#VerbundeneMerkmale),
[Definierende Werte](#DefinierendeWerte),
[Definierender Wert](#DefinierenderWert),
[hat den Verweis auf ein Referenzdokument](#hatdenVerweisaufeinReferenzdokument),
[has dictionary subset](#hasdictionarysubset),
[Digital format](#Digitalformat),
[Dimension](#Dimension),
[has external dictionary](#hasexternaldictionary),
[has external dictionary property](#hasexternaldictionaryproperty),
[hat externe Dictionary Referenz](#hatexterneDictionaryReferenz),
[Gegebene Merkmalsgruppe](#GegebeneMerkmalsgruppe),
[Group(s) of properties](#Group(s)ofproperties),
[Parameter des dynamischen Merkmals](#ParameterdesdynamischenMerkmals),
[Parent group of properties](#Parentgroupofproperties),
[Physikalische Groesse](#PhysikalischeGroesse),
[Liste moeglicher Werte in Sprache N](#ListemoeglicherWerteinSpracheN),
[has property](#hasproperty),
[hat Merkmalsgruppenreferenz](#hatMerkmalsgruppenreferenz),
[hat Merkmalreferenz](#hatMerkmalreferenz),
[Relations of the group of properties identifiers in the interconnected data dictionaries](#Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries),
[Symbole des Merkmals in einer gegebenen Merk-malsgruppe](#SymboledesMerkmalsineinergegebenenMerk-malsgruppe),
[Textformat](#Textformat),
[hat Einheit](#hatEinheit),
[Liste ersetzender Merkmalsgruppen](#ListeersetzenderMerkmalsgruppen),
[List of replacing properties](#Listofreplacingproperties),
[Liste ersetzter Merkmalsgruppen](#ListeersetzterMerkmalsgruppen),
[Liste ersetzter Merkmale](#ListeersetzterMerkmale),
[](Boundaryvalues)
### Boundary values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundary`
Description | Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:BoundaryValue](Grenzwertliste) (c)<br />
[](Grenzwert)
### Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundaryLimit`
Description | Single Boundary value interval
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryValue](Grenzwertliste) (c)<br />
Range(s) |[iddo:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
[](VerbundeneMerkmale)
### Verbundene Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasConnectedProperty`
Description | List of the globally unique identifier of the connected properties (attribute PA001); the value of one property is related to the values of the other ones. For example, a sound absorption coefficient is given for a specific frequency, in this case sound absorption and frequency are connected properties
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](DefinierendeWerte)
### Definierende Werte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDefiningValue`
Description | Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:DefiningValuesList](Definingvalueslist) (c)<br />
[](DefinierenderWert)
### Definierender Wert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDefiningValueItem`
Description | Contains a defining value of an array
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DefiningValuesList](Definingvalueslist) (c)<br />
Range(s) |[iddo:DefiningValueItem](Definingvalueitem) (c)<br />
[](hatdenVerweisaufeinReferenzdokument)
### hat den Verweis auf ein Referenzdokument
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDictionaryReferenceDocument`
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
Range(s) |[iddo:DictionaryReferenceDocument](Referenzdokument) (c)<br />
[](hasdictionarysubset)
### has dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDictionarySubset`
Super-properties |[dcat:dataset](http://www.w3.org/ns/dcat#dataset)<br />
Domain(s) |[iddo:Dictionary](Datenkatalog) (c)<br />
Range(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
[](Digitalformat)
### Digital format
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDigitalFormat`
Description | Pair for digital text type (precision, unit) Precision is the number of significant digits
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
[](Dimension)
### Dimension
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDimension`
Description | In case of a physical quantity, dimension according to ISO 80000 (all parts) This attribute allows the dimension to be machine readable; as all physical quantities are derived from 7 base quantities, it is provided with the power (as a rational number) attached to a basic dimension in the following order and with one space between each
Usage Note | PA028
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
[](hasexternaldictionary)
### has external dictionary
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasExternalDictionary`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hasexternaldictionaryproperty)
### has external dictionary property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasExternalDictionaryProperty`
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
[](hatexterneDictionaryReferenz)
### hat externe Dictionary Referenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasExternalDictionaryReference`
Description | Liste von Paaren (interner Merk-malsbezeichner, entsprechender Datenkatalog-Bezeichner) dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />
[](GegebeneMerkmalsgruppe)
### Gegebene Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasGivenGroupOfProperties`
Description | Globally unique identifier of a group of properties (attribute GA001) for the symbol assigned to the property.
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Group(s)ofproperties)
### Group(s) of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasGroupOfProperties`
Description | List of globally unique identifiers of groups of properties (attribute GA001) to which the property is attached
Usage Note | PA021
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](ParameterdesdynamischenMerkmals)
### Parameter des dynamischen Merkmals
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasParameterOfTheDynamicProperty`
Description | Liste von GUIDs von Merkmalen, welche Parameter der Funktion fuer ein dynamisches Merkmal sind
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](Parentgroupofproperties)
### Parent group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasParentGroupOfProperties`
Description | Enables a sub-group to be linked to a parent group via their globally unique identifiers (attribute GA001) Any property attached to a group is inherited by the sub-group(s)
Usage Note | GA023
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](PhysikalischeGroesse)
### Physikalische Groesse
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPhysicalQuantity`
Description | Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben --> http://qudt.org/vocab/quantitykind/Dimensionless dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.
Usage Note | PA027
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[qudt:QuantityKind](http://qudt.org/schema/qudt/QuantityKind) (c)<br />
[](ListemoeglicherWerteinSpracheN)
### Liste moeglicher Werte in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPossibleValuesInLanguageN`
Description | Liste von Paaren (moeglicher Wert fuer das Merkmal und Sprache) Werte koennen String oder Zahlen sein
Usage Note | PA039
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:PossibleValueInLanguageN](PossibleValueInLanguageN) (c)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasProperty`
Description | Attaches a property to a feature of interest (FOI)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
[](hatMerkmalsgruppenreferenz)
### hat Merkmalsgruppenreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyGroupReference`
Description | Attaches a property group reference to a iddo:ReferenceDocument
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:ReferenceDocument](https://w3id.org/iddo/v2#ReferenceDocument) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](hatMerkmalreferenz)
### hat Merkmalreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyReference`
Description | Fuegt ein Merkmal zu einer Merkmalszuweisung hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries)
### Relations of the group of properties identifiers in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasRelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | Liste von Paaren (inter-ner Bezeichner der Merkmalsgruppe, ent-sprechender Daten-katalog-Bezeichner) dieses Attribut sollte fuer die Kompatibilitaet zwischen bereits vorhandenen Merk-malsgruppen verwen-det werden
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](SymboledesMerkmalsineinergegebenenMerk-malsgruppe)
### Symbole des Merkmals in einer gegebenen Merk-malsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasSymbolsOfTheProperty`
Description | List of pairs (symbol of the property, globally unique identifier of the group of properties (attribute GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />
[](Textformat)
### Textformat
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasTextFormat`
Description | Paar fuer den Texttyp (Verschluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
[](hatEinheit)
### hat Einheit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasUnit`
Description | A unit to represent a scale that enables a value to be measured It is possible to use this attribute to explain there is no unit attached to the property by using unitless --> http://qudt.org/vocab/unit/UNITLESS
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />[iddo:Property](Property) (c)<br />[iddo:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](ListeersetzenderMerkmalsgruppen)
### Liste ersetzender Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#isReplacedByGroupOfProperties`
Description | Liste von globalen Bezeichnern fuer die ersetzenden Merkmalsgruppen
Usage Note | GA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Listofreplacingproperties)
### List of replacing properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#isReplacedByProperty`
Description | global eindeutiger Bezeichner (Attribut PA001) des ersetzenden Merkmals (oder der Merkmale)
Usage Note | PA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](ListeersetzterMerkmalsgruppen)
### Liste ersetzter Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#replacesGroupOfProperties`
Description | Liste von globalen Bezeichnern fuer die ersetzten Merk-malsgruppen
Usage Note | GA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](ListeersetzterMerkmale)
### Liste ersetzter Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#replacesProperties`
Description | Global eindeutiger Bezeichner des ersetzten Merkmals (oder der Merkmale)
Usage Note | PA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />

## Datatype Properties
[Kategorie der Merkmalsgruppe](#KategoriederMerkmalsgruppe),
[Ursprungsland](#Ursprungsland),
[Country of use](#Countryofuse),
[Creator's language](#Creator'slanguage),
[Datentyp (GUID)](#Datentyp(GUID)),
[Date of activation](#Dateofactivation),
[Date of creation](#Dateofcreation),
[Date of deactivation](#Dateofdeactivation),
[Date of last change](#Dateoflastchange),
[Datum der Ueberarbeitung](#DatumderUeberarbeitung),
[Datum der Version](#DatumderVersion),
[Definition of in language N](#DefinitionofinlanguageN),
[Deprecation explanation](#Deprecationexplanation),
[Description in language N](#DescriptioninlanguageN),
[Dynamic Property](#DynamicProperty),
[Kodierung](#Kodierung),
[Example in language N](#ExampleinlanguageN),
[Global eindeutiger Bezeichner (GUID)](#GlobaleindeutigerBezeichner(GUID)),
[inclusive](#inclusive),
[Method of measurement](#Methodofmeasurement),
[Name in language N](#NameinlanguageN),
[Name der definierenden Werte](#NamederdefinierendenWerte),
[Number of Characters](#NumberofCharacters),
[Toleranz](#Toleranz),
[Nummer der ueberarbeitung](#Nummerderueberarbeitung),
[Status](#Status),
[Subdivision of use](#Subdivisionofuse),
[Symbol](#Symbol),
[Toleranz](#Tolerance),
[Version number](#Versionnumber),
[Visual representation](#Visualrepresentation),
[](KategoriederMerkmalsgruppe)
### Kategorie der Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CategoryOfGroupOfProperties`
Description | Gibt die Kategorie der erstellten Merkmalsgruppe an
Usage Note | GA022
Example | ````Domain`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Ursprungsland)
### Ursprungsland
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfOrigin`
Description | Land, aus dem die Anforderung an dieses Merkmal/dieser Merkmalsgruppe stammt
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Countryofuse)
### Country of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfUse`
Description | Land (Gruppe von Laendern, Kon-tinent), in dem das Merkmal/die Merkmalsgruppe fuer den Markt, auf dem die Beteiligten arbeiten, relevant ist
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Creator'slanguage)
### Creator's language
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CreatorsLanguage`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property; this explanation has to be written in international English (EN)
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Datentyp(GUID))
### Datentyp (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DataType`
Description | Format fuer die Angabe des Wertes des Merkmals dies kann aus einer Soft-ware-Perspektive als Speiche-rungsart verstanden werden im Falle eines dynamischen Merkmals ist der Wert dieses Attributs der Datentyp des Er-gebnisses der Berechnung mit der Gleichung
Usage Note | PA030
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Dateofactivation)
### Date of activation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfActivation`
Description | Datum, nach dem das Merkmal verwendet werden kann
Usage Note | PA04/GA04
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofcreation)
### Date of creation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfCreation`
Description | Datum der Validierung der An-frage zur Erstellung des Merkmals durch Sachverstaendige
Usage Note | PA003/GA003
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofdeactivation)
### Date of deactivation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfDeactivation`
Description | Date of deactivation
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateoflastchange)
### Date of last change
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfLastChange`
Description | Datum der Validierung der letzten Aenderungsanfrage durch Sachverstaendige
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderUeberarbeitung)
### Datum der Ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfRevision`
Description | Datum der Ueberarbeitung
Usage Note | PA006/GA006
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderVersion)
### Datum der Version
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfVersion`
Description | Datum der Version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DefinitionofinlanguageN)
### Definition of in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefinitionInLanguage`
Description | Liste von Paaren (Definition des Merkmals/der Merkmalsgruppe, Sprache)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Deprecationexplanation)
### Deprecation explanation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DeprecationExplanation`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property/group of properties; this explanation has to be written in international English (EN)
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DescriptioninlanguageN)
### Description in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DescriptionInLanguage`
Description | Liste von Paaren (Beschreibung des Merkmals, Sprache)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DynamicProperty)
### Dynamic Property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DynamicProperty`
Description | Wenn es sich um ein dynamisches Merkmal handelt, haengt der Wert von den im Attribut PA032 bereitgestellten Parametern ab
Usage Note | PA031
Example | ````yes`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](Kodierung)
### Kodierung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Encoding`
Description | Die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ExampleinlanguageN)
### Example in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExampleInLanguage`
Description | Liste von Paaren (Beispiel des Merkmals, Sprache)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](GlobaleindeutigerBezeichner(GUID))
### Global eindeutiger Bezeichner (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GloballyUniqueIdentifier`
Description | Unique identifier generated using the algorithm denoted in RFC 4122
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](inclusive)
### inclusive
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Inclusive`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />[iddo:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](Methodofmeasurement)
### Method of measurement
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#MethodOfMeasurement`
Description | Evaluation of construction products to ensure their fitness according to requirements in harmonised technical specifications
Usage Note | PA029
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](NameinlanguageN)
### Name in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NameInLanguage`
Description | List of pairs (property name and language) This attribute can be used to add synonyms for different domains
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](NamederdefinierendenWerte)
### Name der definierenden Werte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NameOfTheDefiningValues`
Description | In case of an array, this attribute provides the names of the column headers defined as a list of pairs (name, language)
Usage Note | PA034
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](NumberofCharacters)
### Number of Characters
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NumberOfCharacters`
Description | The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Toleranz)
### Toleranz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Precision`
Description | Precision is the number of significant digits
Usage Note | PA037
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Nummerderueberarbeitung)
### Nummer der ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RevisionNumber`
Description | Diese Nummer der ueberarbeitung ermoeglicht die Verfolgung kleinerer aenderungen, z. B. neue uebersetzung, Korrekturen von Tippfehlern: wenn sich die Versionsnummer aendert, beginnt die Nummer der ueberarbeitung wieder bei 1. Sachverstaendige entscheiden, ob eine neue Nummer der ueberarbeitung angewendet werden kann oder ob eine neue ueberarbeitung erforderlich ist.
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Status)
### Status
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Status`
Description | Status des Merkmals waehrend seines Lebenszyklus
Usage Note | PA002/GA002
Example | ````active`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
[](Subdivisionofuse)
### Subdivision of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SubdivisionOfUse`
Description | Dokumentierte geographische Region, in der das Merkmal/ die Merkmalsgruppe verwendet wird
Usage Note | PA025/GA020
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Symbol)
### Symbol
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Symbol`
Usage Note | PA022
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Tolerance)
### Toleranz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Tolerance`
Description | Fuer numerische Werte; der Gesamtbetrag, um den eine be-stimmte Einheit schwanken darf; sie ist die Differenz zwischen dem Hoechstwert und dem Mindestwert fuer die Einheit
Usage Note | PA036
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Versionnumber)
### Version number
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VersionNumber`
Description | This version number allows tracking of major changes. Experts decide if a new version number must be applied
Usage Note | PA009/GA009
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Visualrepresentation)
### Visual representation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VisualRepresentation`
Description | Visual representation of the group of properties through sketches, photos, videos or other multimedia objects
Usage Note | PA023/GA018
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Property) (c)<br />
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
IRI | `https://w3id.org/iddo/v2#code`
Is Defined By | http://www.w3.org/2000/01/rdf-schema#
Description | Code that can be used to identify the attribute
Domain(s) |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Range(s) |[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#Literal) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `https://w3id.org/iddo/v2#`
* **dc**
  * `http://purl.org/dc/terms/`
* **dcat**
  * `http://www.w3.org/ns/dcat#`
* **ex**
  * `http://www.example.com/property#`
* **iddo**
  * `https://w3id.org/iddo/v2#`
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