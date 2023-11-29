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
[Data dictionary](#Datadictionary),
[Definierender Wert-Item](#DefinierenderWert-Item),
[Dictionary subset](#Dictionarysubset),
[Digitales Format-Item](#DigitalesFormat-Item),
[External Dictionary Reference](#ExternalDictionaryReference),
[Grenzwerte](#BoundaryValueItem),
[Grenzwertliste](#Grenzwertliste),
[Liste definierender Werte](#ListedefinierenderWerte),
[Merkmal](#Merkmal),
[Merkmalsgruppe](#Merkmalsgruppe),
[Possible value in language N](#PossiblevalueinlanguageN),
[Reference document](#Referencedocument),
[Symbol des Merkmals in einer gegebenen Merkmalsgruppe](#SymboldesMerkmalsineinergegebenenMerkmalsgruppe),
[Textformat-Item](#Textformat-Item),
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
### Grenzwerte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValueItem`
Description | <p>Boundary value interval consisting of the lower(minValue) and the upper(maxValue) interval boundary</p>
Usage Note | PA040
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:maxValue](https://schema.org/maxValue) **exactly** 1<br />[sdo:minValue](https://schema.org/minValue) **exactly** 1<br />
In range of |[iddo:BoundaryValue](Boundaryvalue) (op)<br />
### Grenzwertliste
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValuesList`
Description | <p>Pair  (List of boundary intervals of possible values for the property, unit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:BoundaryValue](Boundaryvalue) (op) **min** 1 [iddo:BoundaryValueItem](BoundaryValueItem) (c)<br />[iddo:Unit](Unit) (op) **exactly** 1<br />
In domain of |[iddo:BoundaryValue](Boundaryvalue) (op)<br />
In range of |[iddo:BoundaryValues](Grenzwerte) (op)<br />
### Definierender Wert-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValueItem`
Description | <p>Enthaelt einen definierenden Wert eines Arrays in Form eines Literals</p>
Usage Note | PA035
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:DefiningValue](DefinierenderWert) (op)<br />
### Liste definierender Werte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValuesList`
Description | <p>Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DefiningValueItem](DefinierenderWert-Item) **min** 1<br />
In domain of |[iddo:DefiningValue](DefinierenderWert) (op)<br />
In range of |[iddo:DefiningValues](Definingvalues) (op)<br />
### Data dictionary
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dictionary`
Description | <p>Zentralisiertes Repository von Informationen ueber Daten, wie z. B. Bedeutung, Beziehungen zu anderen Daten, Ursprung, Verwendung und Format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[iddo:hasDictionarySubset](hasdictionarysubset) (op) **min** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />
In domain of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Reference document
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionaryReferenceDocument`
Description | <p>Publication that is consulted to find specific information, particularly in a technical or scientific domain</p>
Super-classes |[dcat:Distribution](http://www.w3.org/ns/dcat#Distribution) (c)<br />
Restrictions |[iddo:hasPropertyGroupReference](hatMerkmalsgruppenreferenz) (op) **exactly** 1<br />
In range of |[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
### Dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionarySubset`
Description | <p>Defines a subset or subgrouping of a data catalog</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />
In domain of |[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
In range of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Digitales Format-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormatItem`
Description | <p>Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Precision](Tolerance) (dp) **exactly** 1<br />[iddo:Unit](Unit) (op) **exactly** 1<br />
In domain of |[iddo:Precision](Tolerance) (dp)<br />[iddo:Unit](Unit) (op)<br />
In range of |[iddo:DigitalFormat](Digitalformat) (op)<br />
### External Dictionary Reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExternalDictionaryReference`
Description | <p>Pair (property internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing properties</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[http://inf.bi.rub.de/ontology/dt#hasExternalDictionary](http://inf.bi.rub.de/ontology/dt#hasExternalDictionary) **exactly** 1<br />[http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty](http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty) **exactly** 1<br />
In range of |[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />
### Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupOfProperties`
Description | <p>Sammlung, die es ermoeglicht, die Merkmale vorauszuplanen oder zu organisieren</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DateOfRevision](Dateofrevision) (dp) **exactly** 1<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp) **min** 0<br />[iddo:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Tolerance](Toleranz) (dp) **min** 0<br />[iddo:Dimension](Dimension) (dp) **min** 0<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **max** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:CountryOfUse](LandderVerwendung) (dp) **min** 1<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp) **min** 0<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 1<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp) **exactly** 1<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />
In domain of |[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp)<br />[iddo:CountryOfUse](LandderVerwendung) (dp)<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp)<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:DateOfRevision](Dateofrevision) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp)<br />[iddo:DateOfCreation](Dateofcreation) (dp)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp)<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />
In range of |[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:hasPropertyGroupReference](hatMerkmalsgruppenreferenz) (op)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op)<br />
### Possible value in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PossibleValueInLanguageN`
Description | <p>Moeglicher Wert fuer das Merkmal und Sprache Werte koennen String oder Zahlen sein</p>
Usage Note | PA039
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />
### Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Property`
Description | <p>Inherent or acquired feature of an item</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:TextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](Textformat-Item) (c)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:DateOfRevision](Dateofrevision) (dp) **exactly** 1<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0<br />[iddo:CountryOfUse](LandderVerwendung) (dp) **min** 1<br />[iddo:NameOfTheDefiningValues](NamederdefinierendenWerte) (dp) **min** 0<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op) **min** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp) **min** 0<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 0<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op) **min** 0 [iddo:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />[iddo:Dimension](Dimension) (dp) **min** 0<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:PhysicalQuantity](Physicalquantity) (dp) **min** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:DataType](Datatype) (dp) **exactly** 1<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp) **min** 0<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp) **min** 0<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp) **min** 0<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **min** 0<br />[iddo:DefiningValues](Definingvalues) (op) **min** 0 [iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />[iddo:ConnectedProperties](VerbundeneMerkmale) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:DynamicProperty](DynamischesMerkmal) (dp) **exactly** 1<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp) **min** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **max** 1<br />[iddo:DigitalFormat](Digitalformat) (op) **min** 0 [iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />[iddo:BoundaryValues](Grenzwerte) (op) **exactly** 1 [iddo:BoundaryValuesList](Grenzwertliste) (c)<br />[iddo:Dimension](Dimension) (dp) **max** 1<br />[iddo:Tolerance](Toleranz) (dp) **min** 0<br />[iddo:ExampleInLanguage](ExampleinlanguageN) (dp) **min** 0<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:Units](Units) (op) **min** 0<br />
In domain of |[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp)<br />[iddo:DataType](Datatype) (dp)<br />[iddo:DateOfCreation](Dateofcreation) (dp)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp)<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp)<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />[iddo:PhysicalQuantity](Physicalquantity) (dp)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:DefinitionInLanguage](DefinitionofinlanguageN) (dp)<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:TextFormat](Textformat) (op)<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:DefiningValues](Definingvalues) (op)<br />[iddo:BoundaryValues](Grenzwerte) (op)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:DigitalFormat](Digitalformat) (op)<br />[iddo:Status](Status) (dp)<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp)<br />[iddo:CountryOfUse](LandderVerwendung) (dp)<br />[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:Tolerance](Toleranz) (dp)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:Units](Units) (op)<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp)<br />[iddo:Dimension](Dimension) (dp)<br />[iddo:ExampleInLanguage](ExampleinlanguageN) (dp)<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:DateOfRevision](Dateofrevision) (dp)<br />[iddo:ConnectedProperties](VerbundeneMerkmale) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />
In range of |[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />[iddo:ConnectedProperties](VerbundeneMerkmale) (op)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />
### Symbol des Merkmals in einer gegebenen Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolOfTheProperty`
Description | <p>Pair (symbol of the property, globally unique identifier of the group of properties (attribute GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op) **exactly** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Symbol](Symbol) (dp) **exactly** 1<br />
In domain of |[iddo:Symbol](Symbol) (dp)<br />
In range of |[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />
### Textformat-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormatItem`
Description | <p>Paar fuer den Texttyp (Verschluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:NumberOfCharacters](AnzahlderZeichen) (dp) **exactly** 1<br />[iddo:Encoding](Encoding) (dp) **exactly** 1<br />
In domain of |[iddo:NumberOfCharacters](AnzahlderZeichen) (dp)<br />[iddo:Encoding](Encoding) (dp)<br />
In range of |[iddo:TextFormat](Textformat) (op)<br />

## Object Properties
[Boundary value](#Boundaryvalue),
[Grenzwerte](#Grenzwerte),
[Verbundene Merkmale](#VerbundeneMerkmale),
[Definierender Wert](#DefinierenderWert),
[Defining values](#Definingvalues),
[Digital format](#Digitalformat),
[Gegebene Merkmalsgruppe](#GegebeneMerkmalsgruppe),
[Merkmalsgruppe(n)](#Merkmalsgruppe(n)),
[Liste moeglicher Werte in Sprache N](#ListemoeglicherWerteinSpracheN),
[Liste ersetzter Merkmalsgruppen](#ListeersetzterMerkmalsgruppen),
[List of replaced properties](#Listofreplacedproperties),
[List of replacing groups of properties](#Listofreplacinggroupsofproperties),
[Liste ersetzender Merkmale](#ListeersetzenderMerkmale),
[Parameter des dynamischen Merkmals](#ParameterdesdynamischenMerkmals),
[uebergeordnete Merkmalsgruppe](#uebergeordneteMerkmalsgruppe),
[Relations of the group of properties identifiers in the interconnected data dictionaries](#Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries),
[Symbols of the property in a given property group](#Symbolsofthepropertyinagivenpropertygroup),
[Text format](#Textformat),
[Unit](#Unit),
[Units](#Units),
[has relation to a reference document](#hasrelationtoareferencedocument),
[has dictionary subset](#hasdictionarysubset),
[has external dictionary](#hasexternaldictionary),
[has external dictionary property](#hasexternaldictionaryproperty),
[hat externe Dictionary Referenz](#hatexterneDictionaryReferenz),
[has property](#hasproperty),
[hat Merkmalsgruppenreferenz](#hatMerkmalsgruppenreferenz),
[hat Merkmalreferenz](#hatMerkmalreferenz),
[](Boundaryvalue)
### Boundary value
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValue`
Description | Single Boundary value interval
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryValuesList](Grenzwertliste) (c)<br />
Range(s) |[iddo:BoundaryValueItem](BoundaryValueItem) (c)<br />
[](Grenzwerte)
### Grenzwerte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValues`
Description | Pair (list of boundary intervals of possible values for the property, unit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:BoundaryValuesList](Grenzwertliste) (c)<br />
[](VerbundeneMerkmale)
### Verbundene Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ConnectedProperties`
Description | Liste der global eindeutigen Bezeichner der verbundenen Merkmale (Attribut PA001); der Wert eines Merkmals steht zu den Werten der anderen in einer Beziehung. Beispielsweise ist ein Schallabsorptionsgrad fuer eine bestimmte Frequenz gegeben, in diesem Fall sind Schallabsorp-tionsgrad und Frequenz ver-bundene Merkmale.
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](DefinierenderWert)
### Definierender Wert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValue`
Description | Contains a defining value of an array
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />
Range(s) |[iddo:DefiningValueItem](DefinierenderWert-Item) (c)<br />
[](Definingvalues)
### Defining values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValues`
Description | In case of an array, this attribute provides the defining values when applicable, the datatype is given by the attribute PA030
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />
[](Digitalformat)
### Digital format
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormat`
Description | Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
[](GegebeneMerkmalsgruppe)
### Gegebene Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GivenGroupsOfProperties`
Description | Global eindeutiger Bezeichner einer Merkmalsgruppe (Attribut GA001) fuer das dem Merkmal zugeordnetem Symbol
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Merkmalsgruppe(n))
### Merkmalsgruppe(n)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupsOfProperties`
Description | Liste von global eindeutigen Bezeichnern von Merkmalsgruppen (Attribut GA001), denen das Merkmal angehoert
Usage Note | PA021
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](ListemoeglicherWerteinSpracheN)
### Liste moeglicher Werte in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfPossibleValuesInLanguageN`
Description | List of pairs (possible value for the property and language) Values can be string or numbers
Usage Note | PA039
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />
[](ListeersetzterMerkmalsgruppen)
### Liste ersetzter Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacedGroupsOfProperties`
Description | Liste von globalen Bezeichnern fuer die ersetzten Merk-malsgruppen
Usage Note | GA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Listofreplacedproperties)
### List of replaced properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacedProperties`
Description | Globally unique identifier of the replaced property (or properties)
Usage Note | PA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](Listofreplacinggroupsofproperties)
### List of replacing groups of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacingGroupsOfProperties`
Description | List of globally unique identifiers of the replacing groups of properties
Usage Note | GA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](ListeersetzenderMerkmale)
### Liste ersetzender Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacingProperties`
Description | Globally unique identifier (attribute PA001) of the replacing property (or properties)
Usage Note | PA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](ParameterdesdynamischenMerkmals)
### Parameter des dynamischen Merkmals
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ParametersOfTheDynamicProperty`
Description | Liste von GUIDs von Merkmalen, welche Parameter der Funktion fuer ein dynamisches Merkmal sind
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](uebergeordneteMerkmalsgruppe)
### uebergeordnete Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ParentGroupOfProperties`
Description | Enables a sub-group to be linked to a parent group via their globally unique identifiers (attribute GA001) Any property attached to a group is inherited by the sub-group(s)
Usage Note | GA023
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries)
### Relations of the group of properties identifiers in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | List of pairs (group of properties internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing groups of properties
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Symbolsofthepropertyinagivenpropertygroup)
### Symbols of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolsOfTheProperty`
Description | List of pairs (symbol of the property, globally unique identifier of the group of properties (attribute GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />
[](Textformat)
### Text format
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormat`
Description | Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:TextFormatItem](Textformat-Item) (c)<br />
[](Unit)
### Unit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Unit`
Description | Unit of measurement for the digital text type
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](Units)
### Units
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Units`
Description | Eine Einheit zur Darstellung einer Skala, die es ermoeglicht, einen Wert zu messen es ist moeglich, dieses Attribut zu verwenden, um zu erlaeutern, dass dem Merkmal keine Einheit zugeordnet ist, indem einheitslos verwendet wird
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](hasrelationtoareferencedocument)
### has relation to a reference document
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDictionaryReferenceDocument`
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
Range(s) |[iddo:DictionaryReferenceDocument](Referencedocument) (c)<br />
[](hasdictionarysubset)
### has dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDictionarySubset`
Super-properties |[dcat:dataset](http://www.w3.org/ns/dcat#dataset)<br />
Domain(s) |[iddo:Dictionary](Datadictionary) (c)<br />
Range(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
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
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasProperty`
Description | Fuegt ein Merkmal zu einem Feature of Interest (FOI) hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
[](hatMerkmalsgruppenreferenz)
### hat Merkmalsgruppenreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyGroupReference`
Description | Fuegt eine Merkmalsgruppe (oberstes in der Hierarchie) zu einer iddo:ReferenceDocument hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[iddo:ReferenceDocument](https://w3id.org/iddo/v2#ReferenceDocument) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](hatMerkmalreferenz)
### hat Merkmalreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyReference`
Description | Fuegt ein Merkmal zu einer Merkmalszuweisung hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />

## Datatype Properties
[Kategorie der Merkmalsgruppe](#KategoriederMerkmalsgruppe),
[Ursprungsland](#Ursprungsland),
[Land der Verwendung](#LandderVerwendung),
[Creator's language](#Creator'slanguage),
[Data type](#Datatype),
[Datum der Aktivierung](#DatumderAktivierung),
[Date of creation](#Dateofcreation),
[Datum der Deaktivierung](#DatumderDeaktivierung),
[Datum der letzten Aenderung](#DatumderletztenAenderung),
[Date of revision](#Dateofrevision),
[Datum der Version](#DatumderVersion),
[Definition of in language N](#DefinitionofinlanguageN),
[Deprecation explanation](#Deprecationexplanation),
[Description in language N](#DescriptioninlanguageN),
[Dimension](#Dimension),
[Dynamisches Merkmal](#DynamischesMerkmal),
[Encoding](#Encoding),
[Example in language N](#ExampleinlanguageN),
[Globally Unique Identifier (GUID)](#GloballyUniqueIdentifier(GUID)),
[Method of measurement](#Methodofmeasurement),
[Name in Sprache N](#NameinSpracheN),
[Name der definierenden Werte](#NamederdefinierendenWerte),
[Anzahl der Zeichen](#AnzahlderZeichen),
[Physical quantity](#Physicalquantity),
[Tolerance](#Tolerance),
[Nummer der ueberarbeitung](#Nummerderueberarbeitung),
[Status](#Status),
[Unterteilung der Verwendung](#UnterteilungderVerwendung),
[Symbol](#Symbol),
[Toleranz](#Toleranz),
[Version number](#Versionnumber),
[Bildliche Darstellung](#BildlicheDarstellung),
[](KategoriederMerkmalsgruppe)
### Kategorie der Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CategoryOfGroupOfProperties`
Description | Specifies the category of the created property group
Usage Note | GA022
Example | ````Domain`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Ursprungsland)
### Ursprungsland
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfOrigin`
Description | Country from where the requirement for this property/group of properties originated
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](LandderVerwendung)
### Land der Verwendung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfUse`
Description | Country (group of countries, continent) in which the property is relevant for the market the stakeholders operate in
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Creator'slanguage)
### Creator's language
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CreatorsLanguage`
Description | Satz, der den Grund fuer die Ab-lehnung erlaeutert, der erklaeren kann, wie Werte umzurechnen sind, damit sie dem neuen Merkmal entsprechen; diese Er-laeuterung muss in internatio-nalem Englisch (EN) geschrieben werden
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Datatype)
### Data type
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DataType`
Description | Format for expressing the value of the property This can be understood as the storage type from a software perspective In case of a dynamic property the value of this attribute is the datatype of the result of the calculation by the formula
Usage Note | PA030
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](DatumderAktivierung)
### Datum der Aktivierung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfActivation`
Description | Date after when the property can be used
Usage Note | PA04/GA04
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofcreation)
### Date of creation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfCreation`
Description | Datum der Validierung der An-frage zur Erstellung des Merkmals durch Sachverstaendige
Usage Note | PA003/GA003
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderDeaktivierung)
### Datum der Deaktivierung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfDeactivation`
Description | Date of deactivation
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderletztenAenderung)
### Datum der letzten Aenderung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfLastChange`
Description | Date of validation of the last change request by experts
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofrevision)
### Date of revision
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfRevision`
Description | Datum der Ueberarbeitung
Usage Note | PA006/GA006
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderVersion)
### Datum der Version
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfVersion`
Description | Datum der Version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DefinitionofinlanguageN)
### Definition of in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefinitionInLanguage`
Description | Liste von Paaren (Definition des Merkmals/der Merkmalsgruppe, Sprache)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Deprecationexplanation)
### Deprecation explanation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DeprecationExplanation`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property/group of properties; this explanation has to be written in international English (EN)
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DescriptioninlanguageN)
### Description in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DescriptionInLanguage`
Description | List of pairs (Description of the property, language)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Dimension)
### Dimension
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dimension`
Description | Im Falle einer physikalischen Groesse, Dimension nach ISO 80000 (alle Teile) dieses Attribut ermoeglicht, dass die Dimension maschinenlesbar ist; da alle physikalischen Groessen von 7 Basisgroessen abgeleitet sind, wird es durch Angabe der Basisdimensionen mit zugehoeriger Potenz (als rationale Zahl) in der folgenden Reihenfolge und mit jeweils einem Leerzeichen dazwischen angegeben
Usage Note | PA028
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](DynamischesMerkmal)
### Dynamisches Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DynamicProperty`
Description | Wenn es sich um ein dynamisches Merkmal handelt, haengt der Wert von den im Attribut PA032 bereitgestellten Parametern ab
Usage Note | PA031
Example | ````yes`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](Encoding)
### Encoding
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Encoding`
Description | The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](Textformat-Item) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ExampleinlanguageN)
### Example in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExampleInLanguage`
Description | Liste von Paaren (Beispiel des Merkmals, Sprache)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](GloballyUniqueIdentifier(GUID))
### Globally Unique Identifier (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GloballyUniqueIdentifier`
Description | Unique identifier generated using the algorithm denoted in RFC 4122
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Methodofmeasurement)
### Method of measurement
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#MethodOfMeasurement`
Description | Beurteilung von Bauprodukten, um ihre Tauglichkeit entsprechend den Anforderungen in harmonisierten technischen Spezifikationen sicherzustellen
Usage Note | PA029
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](NameinSpracheN)
### Name in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NameInLanguage`
Description | List of pairs (property name and language) This attribute can be used to add synonyms for different domains
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](NamederdefinierendenWerte)
### Name der definierenden Werte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NameOfTheDefiningValues`
Description | Im Falle eines Feldes liefert dieses Attribut die Namen der Spaltenkoepfe, festgelegt als Liste von Paaren (Name, Sprache)
Usage Note | PA034
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](AnzahlderZeichen)
### Anzahl der Zeichen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NumberOfCharacters`
Description | The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](Textformat-Item) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Physicalquantity)
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PhysicalQuantity`
Description | Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.
Usage Note | PA027
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Tolerance)
### Tolerance
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Precision`
Description | Praezision ist die Anzahl signifi-kanter Stellen
Usage Note | PA037
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Nummerderueberarbeitung)
### Nummer der ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RevisionNumber`
Description | This revision number allows tracking of minor changes e.g. new translation, changes of typos: if the version number changes, the revision number starts again at 1 Experts decide if a new revision number can be applied or if a new revision is needed
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Status)
### Status
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Status`
Description | Status of the property during its life cycle
Usage Note | PA002/GA002
Example | ````inactive`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](UnterteilungderVerwendung)
### Unterteilung der Verwendung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SubdivisionOfUse`
Description | Documented geographical region of use of the group of properties
Usage Note | PA025/GA020
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Symbol)
### Symbol
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Symbol`
Usage Note | PA022
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Toleranz)
### Toleranz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Tolerance`
Description | For numerical values; the total amount that a specific unit is permitted to vary; it is the difference between the maximum and the minimum limits for the unit
Usage Note | PA036
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Versionnumber)
### Version number
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VersionNumber`
Description | Diese Versionsnummer ermoeglicht die Verfolgung groesserer aenderungen. Sachverstaendige entscheiden, ob eine neue Ver-sionsnummer angewendet werden muss.
Usage Note | PA009/GA009
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](BildlicheDarstellung)
### Bildliche Darstellung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VisualRepresentation`
Description | Visual representation of the group of properties through sketches, photos, videos or other multimedia objects
Usage Note | PA023/GA018
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Description | Code, der zur Identifizierung des Attributs verwendet werden kann
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