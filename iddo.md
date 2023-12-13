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
[Boundary values list](#Boundaryvalueslist),
[Datenkatalog](#Datenkatalog),
[Definierender Wert-Item](#DefinierenderWert-Item),
[Dictionary subset](#Dictionarysubset),
[Digital format item](#Digitalformatitem),
[External Dictionary Reference](#ExternalDictionaryReference),
[Liste definierender Werte](#ListedefinierenderWerte),
[Maximum Boundary Limit](#MaximumBoundaryLimit),
[Merkmalsgruppe](#Merkmalsgruppe),
[Physikalische Groesse](#PhysikalischeGroesse),
[Possible value in language N](#PossiblevalueinlanguageN),
[Property](#Property),
[Referenzdokument](#Referenzdokument),
[Symbol of the property in a given property group](#Symbolofthepropertyinagivenpropertygroup),
[Text format item](#Textformatitem),
[Unterer Grenzwert](#UntererGrenzwert),
[Zugewiesenes Merkmal](#ZugewiesenesMerkmal),
### Zugewiesenes Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#AssignedProperty`
Description | <p>Repraesentiert die Zweisung eines Merkmals und einer Merkmalszustandes an ein Feature of Interest (FOI)</p>
Super-classes |[http://www.w3id.org/opm#Property](http://www.w3id.org/opm#Property) (c)<br />
Restrictions |[http://www.w3id.org/opm#hasPropertyState](http://www.w3id.org/opm#hasPropertyState) **min** 1<br />[iddo:hasPropertyReference](hasPropertyReference) (op) **exactly** 1<br />
In domain of |[iddo:hasPropertyReference](hasPropertyReference) (op)<br />
In range of |[iddo:hasProperty](hasproperty) (op)<br />
### Maximum Boundary Limit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMax`
Description | <p>Grenzwertintervall bestehend aus der oberen(maxValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Inclusive](inclusive) (dp) **exactly** 1<br />[iddo:hasUnit](hasunit) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />
In domain of |[iddo:Inclusive](inclusive) (dp)<br />[iddo:hasUnit](hasunit) (op)<br />
### Unterer Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMin`
Description | <p>Boundary limit interval consisting of the lower(minValue) interval boundary</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[iddo:hasUnit](hasunit) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />[iddo:Inclusive](inclusive) (dp) **exactly** 1<br />
In domain of |[iddo:Inclusive](inclusive) (dp)<br />[iddo:hasUnit](hasunit) (op)<br />
In range of |[iddo:hasBoundaryLimit](Grenzwert) (op)<br />
### Boundary values list
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValue`
Description | <p>Pair  (List of boundary intervals of possible values for the property, unit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasBoundaryLimit](Grenzwert) (op) **max** 1 [iddo:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />[iddo:hasBoundaryLimit](Grenzwert) (op) **max** 1 [iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />
In domain of |[iddo:hasBoundaryLimit](Grenzwert) (op)<br />
In range of |[iddo:hasBoundary](Boundaryvalues) (op)<br />
### Definierender Wert-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValueItem`
Description | <p>Contains a defining value of an array in the form of a literal</p>
Usage Note | PA035
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:hasDefiningValueItem](DefinierenderWert) (op)<br />
### Liste definierender Werte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValuesList`
Description | <p>In case of an array, this attribute provides the defining values when applicable, the datatype is given by the attribute PA030</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DefiningValueItem](DefinierenderWert-Item) **min** 1<br />
In domain of |[iddo:hasDefiningValueItem](DefinierenderWert) (op)<br />
In range of |[iddo:hasDefiningValue](Definingvalues) (op)<br />
### Datenkatalog
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dictionary`
Description | <p>Centralized repository of information about data such as meaning, relationships to other data, origin, usage and format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op) **min** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />
In domain of |[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Referenzdokument
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionaryReferenceDocument`
Description | <p>Publication that is consulted to find specific information, particularly in a technical or scientific domain</p>
Super-classes |[dcat:Distribution](http://www.w3.org/ns/dcat#Distribution) (c)<br />
Restrictions |[iddo:hasPropertyGroupReference](haspropertygroupreference) (op) **exactly** 1<br />
In range of |[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
### Dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionarySubset`
Description | <p>Definiert eine Teilmenge oder Untergruppierung eines Datenkatalogs</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />
In domain of |[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
In range of |[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Digital format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormatItem`
Description | <p>Pair for digital text type (precision, unit) Precision is the number of significant digits</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasUnit](hasunit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[iddo:Precision](Tolerance) (dp) **exactly** 1<br />
In domain of |[iddo:Precision](Tolerance) (dp)<br />
In range of |[iddo:hasDigitalFormat](Digitalformat) (op)<br />
### External Dictionary Reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExternalDictionaryReference`
Description | <p>Pair (property internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing properties</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[http://inf.bi.rub.de/ontology/dt#hasExternalDictionary](http://inf.bi.rub.de/ontology/dt#hasExternalDictionary) **exactly** 1<br />[http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty](http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty) **exactly** 1<br />
In range of |[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />
### Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupOfProperties`
Description | <p>Sammlung, die es ermoeglicht, die Merkmale vorauszuplanen oder zu organisieren</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:hasDimension](Dimension) (op) **min** 0<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **exactly** 1<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:CountryOfUse](LandderVerwendung) (dp) **min** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:CategoryOfGroupOfProperties](Categoryofgroupofproperties) (dp) **exactly** 1<br />[iddo:hasParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **max** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 1<br />[iddo:Tolerance](Tolerance1) (dp) **min** 0<br />[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />[iddo:hasParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp) **min** 0<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[iddo:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />
In domain of |[iddo:VersionNumber](Versionsnummer) (dp)<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp)<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:hasParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:Status](Status) (dp)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:hasRelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:CountryOfUse](LandderVerwendung) (dp)<br />[iddo:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:CategoryOfGroupOfProperties](Categoryofgroupofproperties) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />
In range of |[iddo:hasPropertyGroupReference](haspropertygroupreference) (op)<br />[iddo:replacesGroupOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:hasGroupOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:isReplacedByGroupOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:hasParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />
### Physikalische Groesse
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PhysicalQuantity`
Description | <p>List of pairs (physical quantity | language) Physical quantities are expressed in International System (SI) units Non-physical quantities such as text are expressed with the value "without" This is equivalent to a measure in ISO 16739-1 and ISO 10303 Only one physical quantity can be attached to a property. This attribute is used to provide the quantity in plain text with all the needed translations</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
### Possible value in language N
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
Description | <p>Inherent or acquired feature of an item</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **min** 0<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:MethodOfMeasurement](Messverfahren) (dp) **min** 0<br />[iddo:CountryOfUse](LandderVerwendung) (dp) **min** 1<br />[iddo:DataType](Datentyp(GUID)) (dp) **exactly** 1<br />[iddo:ExampleInLanguage](BeispielinSpracheN) (dp) **min** 0<br />[iddo:hasPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0<br />[iddo:hasBoundary](Boundaryvalues) (op) **exactly** 1 [iddo:BoundaryValue](Boundaryvalueslist) (c)<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:NameOfTheDefiningValues](Namesofthedefiningvalues) (dp) **min** 0<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op) **min** 0 [iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />[iddo:hasParameterOfTheDynamicProperty](Parametersofthedynamicproperty) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[iddo:replacesProperties](Listofreplacedproperties) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 0<br />[iddo:hasPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />[iddo:hasGroupOfProperties](Merkmalsgruppe(n)) (op) **min** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:hasTextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](Textformatitem) (c)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:hasUnit](hasunit) (op) **min** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[iddo:hasDefiningValue](Definingvalues) (op) **min** 0 [iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />[iddo:isReplacedByProperty](Listofreplacingproperties) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:Tolerance](Tolerance1) (dp) **min** 0<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp) **min** 0<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />[iddo:DynamicProperty](DynamischesMerkmal) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:hasPhysicalQuantity](Physicalquantity) (op) **min** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **max** 1<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp) **min** 0<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:hasDigitalFormat](Digitalformat) (op) **min** 0 [iddo:DigitalFormatItem](Digitalformatitem) (c)<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />
In domain of |[iddo:Tolerance](Tolerance1) (dp)<br />[iddo:VersionNumber](Versionsnummer) (dp)<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp)<br />[iddo:hasDefiningValue](Definingvalues) (op)<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op)<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp)<br />[iddo:ExampleInLanguage](BeispielinSpracheN) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:MethodOfMeasurement](Messverfahren) (dp)<br />[iddo:hasTextFormat](Textformat) (op)<br />[iddo:hasGroupOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:hasDimension](Dimension) (op)<br />[iddo:hasParameterOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />[iddo:hasDigitalFormat](Digitalformat) (op)<br />[iddo:hasBoundary](Boundaryvalues) (op)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />[iddo:hasPhysicalQuantity](Physicalquantity) (op)<br />[iddo:replacesProperties](Listofreplacedproperties) (op)<br />[iddo:DataType](Datentyp(GUID)) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:CountryOfUse](LandderVerwendung) (dp)<br />[iddo:hasUnit](hasunit) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:isReplacedByProperty](Listofreplacingproperties) (op)<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp)<br />[iddo:hasPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />
In range of |[iddo:hasPropertyReference](hasPropertyReference) (op)<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op)<br />[iddo:hasParameterOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />[iddo:isReplacedByProperty](Listofreplacingproperties) (op)<br />[iddo:replacesProperties](Listofreplacedproperties) (op)<br />
### Symbol of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolOfTheProperty`
Description | <p>Paar (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Symbol](Symbol) (dp) **exactly** 1<br />[iddo:hasGivenGroupOfProperties](GegebeneMerkmalsgruppe) (op) **exactly** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
In domain of |[iddo:Symbol](Symbol) (dp)<br />
In range of |[iddo:hasSymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />
### Text format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormatItem`
Description | <p>Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:NumberOfCharacters](NumberofCharacters) (dp) **exactly** 1<br />[iddo:Encoding](Kodierung) (dp) **exactly** 1<br />
In domain of |[iddo:Encoding](Kodierung) (dp)<br />[iddo:NumberOfCharacters](NumberofCharacters) (dp)<br />
In range of |[iddo:hasTextFormat](Textformat) (op)<br />

## Object Properties
[Boundary values](#Boundaryvalues),
[Grenzwert](#Grenzwert),
[Verbundene Merkmale](#VerbundeneMerkmale),
[Defining values](#Definingvalues),
[Definierender Wert](#DefinierenderWert),
[has relation to a reference document](#hasrelationtoareferencedocument),
[hat Teilmenge eines Katalogs](#hatTeilmengeeinesKatalogs),
[Digital format](#Digitalformat),
[Dimension](#Dimension),
[has external dictionary](#hasexternaldictionary),
[has external dictionary property](#hasexternaldictionaryproperty),
[has External Dictionary Reference](#hasExternalDictionaryReference),
[Gegebene Merkmalsgruppe](#GegebeneMerkmalsgruppe),
[Merkmalsgruppe(n)](#Merkmalsgruppe(n)),
[Parameters of the dynamic property](#Parametersofthedynamicproperty),
[uebergeordnete Merkmalsgruppe](#uebergeordneteMerkmalsgruppe),
[Physical quantity](#Physicalquantity),
[Liste moeglicher Werte in Sprache N](#ListemoeglicherWerteinSpracheN),
[has property](#hasproperty),
[has property group reference](#haspropertygroupreference),
[has Property Reference](#hasPropertyReference),
[Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen](#BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen),
[Symbole des Merkmals in einer gegebenen Merk-malsgruppe](#SymboledesMerkmalsineinergegebenenMerk-malsgruppe),
[Textformat](#Textformat),
[has unit](#hasunit),
[Liste ersetzender Merkmalsgruppen](#ListeersetzenderMerkmalsgruppen),
[List of replacing properties](#Listofreplacingproperties),
[Liste ersetzter Merkmalsgruppen](#ListeersetzterMerkmalsgruppen),
[List of replaced properties](#Listofreplacedproperties),
[](Boundaryvalues)
### Boundary values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundary`
Description | Pair (list of boundary intervals of possible values for the property, unit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:BoundaryValue](Boundaryvalueslist) (c)<br />
[](Grenzwert)
### Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundaryLimit`
Description | Single Boundary value interval
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryValue](Boundaryvalueslist) (c)<br />
Range(s) |[iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />
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
[](Definingvalues)
### Defining values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDefiningValue`
Description | Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />
[](DefinierenderWert)
### Definierender Wert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDefiningValueItem`
Description | Enthaelt einen definierenden Wert eines Arrays
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />
Range(s) |[iddo:DefiningValueItem](DefinierenderWert-Item) (c)<br />
[](hasrelationtoareferencedocument)
### has relation to a reference document
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDictionaryReferenceDocument`
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
Range(s) |[iddo:DictionaryReferenceDocument](Referenzdokument) (c)<br />
[](hatTeilmengeeinesKatalogs)
### hat Teilmenge eines Katalogs
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
Description | Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
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
[](hasExternalDictionaryReference)
### has External Dictionary Reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasExternalDictionaryReference`
Description | Liste von Paaren (interner Merk-malsbezeichner, entsprechender Datenkatalog-Bezeichner) dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden
Usage Note | PA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Merkmalsgruppe(n))
### Merkmalsgruppe(n)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasGroupOfProperties`
Description | List of globally unique identifiers of groups of properties (attribute GA001) to which the property is attached
Usage Note | PA021
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Parametersofthedynamicproperty)
### Parameters of the dynamic property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasParameterOfTheDynamicProperty`
Description | Liste von GUIDs von Merkmalen, welche Parameter der Funktion fuer ein dynamisches Merkmal sind
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](uebergeordneteMerkmalsgruppe)
### uebergeordnete Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasParentGroupOfProperties`
Description | Ermoeglicht die Ver-knuepfung einer Unter-gruppe mit einer ueber-geordneten Gruppe ueber ihre global ein-deutigen Bezeichner (Attribut GA001) jedes einer Gruppe zugehoerige Merkmal wird von der/den Untergruppe(n) uebernommen
Usage Note | GA023
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Physicalquantity)
### Physical quantity
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
Range(s) |[iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasProperty`
Description | Attaches a property to a feature of interest (FOI)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
[](haspropertygroupreference)
### has property group reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyGroupReference`
Description | Fuegt eine Merkmalsgruppe (oberstes in der Hierarchie) zu einer iddo:ReferenceDocument hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[iddo:ReferenceDocument](https://w3id.org/iddo/v2#ReferenceDocument) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](hasPropertyReference)
### has Property Reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyReference`
Description | Attaches a property reference to a property assignment
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen)
### Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasRelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | Liste von Paaren (inter-ner Bezeichner der Merkmalsgruppe, ent-sprechender Daten-katalog-Bezeichner) dieses Attribut sollte fuer die Kompatibilitaet zwischen bereits vorhandenen Merk-malsgruppen verwen-det werden
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Description | Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
[](hasunit)
### has unit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasUnit`
Description | A unit to represent a scale that enables a value to be measured It is possible to use this attribute to explain there is no unit attached to the property by using unitless --> http://qudt.org/vocab/unit/UNITLESS
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />[iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](ListeersetzenderMerkmalsgruppen)
### Liste ersetzender Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#isReplacedByGroupOfProperties`
Description | List of globally unique identifiers of the replacing groups of properties
Usage Note | GA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Description | List of globally unique identifiers of the replaced groups of properties
Usage Note | GA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Listofreplacedproperties)
### List of replaced properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#replacesProperties`
Description | Global eindeutiger Bezeichner des ersetzten Merkmals (oder der Merkmale)
Usage Note | PA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />

## Datatype Properties
[Category of group of properties](#Categoryofgroupofproperties),
[Ursprungsland](#Ursprungsland),
[Land der Verwendung](#LandderVerwendung),
[Erlaeuterung fuer die Ablehnung](#ErlaeuterungfuerdieAblehnung),
[Datentyp (GUID)](#Datentyp(GUID)),
[Datum der Aktivierung](#DatumderAktivierung),
[Datum der Erstellung](#DatumderErstellung),
[Date of deactivation](#Dateofdeactivation),
[Datum der letzten Aenderung](#DatumderletztenAenderung),
[Datum der Ueberarbeitung](#DatumderUeberarbeitung),
[Datum der Version](#DatumderVersion),
[Definition of in language N](#DefinitionofinlanguageN),
[Deprecation explanation](#Deprecationexplanation),
[Description in language N](#DescriptioninlanguageN),
[Dynamisches Merkmal](#DynamischesMerkmal),
[Kodierung](#Kodierung),
[Beispiel in Sprache N](#BeispielinSpracheN),
[Global eindeutiger Bezeichner (GUID)](#GlobaleindeutigerBezeichner(GUID)),
[inclusive](#inclusive),
[Messverfahren](#Messverfahren),
[Name in Sprache N](#NameinSpracheN),
[Names of the defining values](#Namesofthedefiningvalues),
[Number of Characters](#NumberofCharacters),
[Tolerance](#Tolerance),
[Nummer der ueberarbeitung](#Nummerderueberarbeitung),
[Status](#Status),
[Subdivision of use](#Subdivisionofuse),
[Symbol](#Symbol),
[Tolerance](#Tolerance1),
[Versionsnummer](#Versionsnummer),
[Bildliche Darstellung](#BildlicheDarstellung),
[](Categoryofgroupofproperties)
### Category of group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CategoryOfGroupOfProperties`
Description | Gibt die Kategorie der erstellten Merkmalsgruppe an
Usage Note | GA022
Example | ````Domain`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Ursprungsland)
### Ursprungsland
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfOrigin`
Description | Land, aus dem die Anforderung an dieses Merkmal/dieser Merkmalsgruppe stammt
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](LandderVerwendung)
### Land der Verwendung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfUse`
Description | Land (Gruppe von Laendern, Kon-tinent), in dem das Merkmal/die Merkmalsgruppe fuer den Markt, auf dem die Beteiligten arbeiten, relevant ist
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ErlaeuterungfuerdieAblehnung)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CreatorsLanguage`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property; this explanation has to be written in international English (EN)
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
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
[](DatumderAktivierung)
### Datum der Aktivierung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfActivation`
Description | Date after when the property can be used
Usage Note | PA04/GA04
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderErstellung)
### Datum der Erstellung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfCreation`
Description | Date of validation of the property creation request by experts
Usage Note | PA003/GA003
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofdeactivation)
### Date of deactivation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfDeactivation`
Description | Date of deactivation
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderletztenAenderung)
### Datum der letzten Aenderung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfLastChange`
Description | Date of validation of the last change request by experts
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderUeberarbeitung)
### Datum der Ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfRevision`
Description | Date of revision
Usage Note | PA006/GA006
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderVersion)
### Datum der Version
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfVersion`
Description | Date of version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DefinitionofinlanguageN)
### Definition of in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefinitionInLanguage`
Description | List of pairs (definition of the property/group of properties, language)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Deprecationexplanation)
### Deprecation explanation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DeprecationExplanation`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property/group of properties; this explanation has to be written in international English (EN)
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DescriptioninlanguageN)
### Description in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DescriptionInLanguage`
Description | List of pairs (Description of the property, language)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DynamischesMerkmal)
### Dynamisches Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DynamicProperty`
Description | If this is a dynamic property, the value is dependent on the parameters provided in the attribute PA032
Usage Note | PA031
Example | ````no`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](Kodierung)
### Kodierung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Encoding`
Description | The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](BeispielinSpracheN)
### Beispiel in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExampleInLanguage`
Description | List of pairs (example of the property, language)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](GlobaleindeutigerBezeichner(GUID))
### Global eindeutiger Bezeichner (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GloballyUniqueIdentifier`
Description | Eindeutiger Bezeichner, der mit dem in RFC 4122 beschriebenen Algorithmus erzeugt wird
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](inclusive)
### inclusive
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Inclusive`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />[iddo:BoundaryLimitMax](MaximumBoundaryLimit) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](Messverfahren)
### Messverfahren
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#MethodOfMeasurement`
Description | Beurteilung von Bauprodukten, um ihre Tauglichkeit entsprechend den Anforderungen in harmonisierten technischen Spezifikationen sicherzustellen
Usage Note | PA029
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](NameinSpracheN)
### Name in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NameInLanguage`
Description | List of pairs (property name and language) This attribute can be used to add synonyms for different domains
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Namesofthedefiningvalues)
### Names of the defining values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NameOfTheDefiningValues`
Description | Im Falle eines Feldes liefert dieses Attribut die Namen der Spaltenkoepfe, festgelegt als Liste von Paaren (Name, Sprache)
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
[](Tolerance)
### Tolerance
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Precision`
Description | Precision is the number of significant digits
Usage Note | PA037
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Nummerderueberarbeitung)
### Nummer der ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RevisionNumber`
Description | Diese Nummer der ueberarbeitung ermoeglicht die Verfolgung kleinerer aenderungen, z. B. neue uebersetzung, Korrekturen von Tippfehlern: wenn sich die Versionsnummer aendert, beginnt die Nummer der ueberarbeitung wieder bei 1. Sachverstaendige entscheiden, ob eine neue Nummer der ueberarbeitung angewendet werden kann oder ob eine neue ueberarbeitung erforderlich ist.
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Status)
### Status
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Status`
Description | Status des Merkmals waehrend seines Lebenszyklus
Usage Note | PA002/GA002
Example | ````inactive`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Subdivisionofuse)
### Subdivision of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SubdivisionOfUse`
Description | Dokumentierte geographische Region, in der das Merkmal/ die Merkmalsgruppe verwendet wird
Usage Note | PA025/GA020
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
[](Tolerance1)
### Tolerance
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Tolerance`
Description | For numerical values; the total amount that a specific unit is permitted to vary; it is the difference between the maximum and the minimum limits for the unit
Usage Note | PA036
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Versionsnummer)
### Versionsnummer
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VersionNumber`
Description | Diese Versionsnummer ermoeglicht die Verfolgung groesserer aenderungen. Sachverstaendige entscheiden, ob eine neue Ver-sionsnummer angewendet werden muss.
Usage Note | PA009/GA009
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](BildlicheDarstellung)
### Bildliche Darstellung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VisualRepresentation`
Description | Visual representation of the group of properties through sketches, photos, videos or other multimedia objects
Usage Note | PA023/GA018
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
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