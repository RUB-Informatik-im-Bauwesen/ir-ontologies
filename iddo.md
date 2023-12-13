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
[Definierender Wert-Item](#DefinierenderWert-Item),
[Dictionary subset](#Dictionarysubset),
[Digital format item](#Digitalformatitem),
[External Dictionary Reference ](#ExternalDictionaryReference),
[Grenzwertliste](#Grenzwertliste),
[Liste definierender Werte](#ListedefinierenderWerte),
[Merkmal](#Merkmal),
[Merkmalsgruppe](#Merkmalsgruppe),
[Minimum Boundary Limit](#MinimumBoundaryLimit),
[Oberer Grenzwert](#ObererGrenzwert),
[Physical quantity](#PhysicalQuantity),
[Possible value in language N](#PossiblevalueinlanguageN),
[Reference document](#Referencedocument),
[Symbol of the property in a given property group](#Symbolofthepropertyinagivenpropertygroup),
[Text format item](#Textformatitem),
[Zugewiesenes Merkmal](#ZugewiesenesMerkmal),
### Zugewiesenes Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#AssignedProperty`
Description | <p>Repraesentiert die Zweisung eines Merkmals und einer Merkmalszustandes an ein Feature of Interest (FOI)</p>
Super-classes |[http://www.w3id.org/opm#Property](http://www.w3id.org/opm#Property) (c)<br />
Restrictions |[http://www.w3id.org/opm#hasPropertyState](http://www.w3id.org/opm#hasPropertyState) **min** 1<br />[iddo:hasPropertyReference](hatMerkmalreferenz) (op) **exactly** 1<br />
In domain of |[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />
In range of |[iddo:hasProperty](hatMerkmal) (op)<br />
### Oberer Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMax`
Description | <p>Grenzwertintervall bestehend aus der oberen(maxValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />[iddo:Inclusive](inclusive) (dp) **exactly** 1<br />[iddo:hasUnit](hasunit) (op) **exactly** 1<br />
In domain of |[iddo:Inclusive](inclusive) (dp)<br />[iddo:hasUnit](hasunit) (op)<br />
### Minimum Boundary Limit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMin`
Description | <p>Grenzwertintervall bestehend aus der unteren(minValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[iddo:hasUnit](hasunit) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />
In domain of |[iddo:Inclusive](inclusive) (dp)<br />[iddo:hasUnit](hasunit) (op)<br />
In range of |[iddo:hasBoundaryLimit](Grenzwert) (op)<br />
### Grenzwertliste
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValue`
Description | <p>Pair  (List of boundary intervals of possible values for the property, unit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasBoundaryLimit](Grenzwert) (op) **max** 1 [iddo:BoundaryLimitMax](ObererGrenzwert) (c)<br />[iddo:hasBoundaryLimit](Grenzwert) (op) **max** 1 [iddo:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
In domain of |[iddo:hasBoundaryLimit](Grenzwert) (op)<br />
In range of |[iddo:hasBoundary](Boundaryvalues) (op)<br />
### Definierender Wert-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValueItem`
Description | <p>Contains a defining value of an array in the form of a literal</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:DefiningValue](Definingvalue) (op)<br />
### Liste definierender Werte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValuesList`
Description | <p>Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DefiningValueItem](DefinierenderWert-Item) **min** 1<br />
In domain of |[iddo:DefiningValue](Definingvalue) (op)<br />
In range of |[iddo:DefiningValues](DefinierendeWerte) (op)<br />
### Datenkatalog
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dictionary`
Description | <p>Zentralisiertes Repository von Informationen ueber Daten, wie z. B. Bedeutung, Beziehungen zu anderen Daten, Ursprung, Verwendung und Format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[iddo:hasDictionarySubset](hasdictionarysubset) (op) **min** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />
In domain of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Reference document
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionaryReferenceDocument`
Description | <p>Publication that is consulted to find specific information, particularly in a technical or scientific domain</p>
Super-classes |[dcat:Distribution](http://www.w3.org/ns/dcat#Distribution) (c)<br />
Restrictions |[iddo:hasPropertyGroupReference](haspropertygroupreference) (op) **exactly** 1<br />
In range of |[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op)<br />
### Dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionarySubset`
Description | <p>Defines a subset or subgrouping of a data catalog</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />
In domain of |[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op)<br />
In range of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Digital format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormatItem`
Description | <p>Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasUnit](hasunit) (op) **exactly** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[iddo:Precision](Toleranz) (dp) **exactly** 1<br />
In domain of |[iddo:Precision](Toleranz) (dp)<br />
In range of |[iddo:DigitalFormat](DigitalesFormat) (op)<br />
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
Restrictions |[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:CategoryOfGroupOfProperties](Categoryofgroupofproperties) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[iddo:DateOfRevision](Dateofrevision) (dp) **exactly** 1<br />[iddo:CountryOfUse](LandderVerwendung) (dp) **min** 1<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp) **min** 0<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:hasDimension](Dimension) (op) **min** 0<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:VisualRepresentation](Visualrepresentation) (dp) **min** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **exactly** 1<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **max** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
In domain of |[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:CategoryOfGroupOfProperties](Categoryofgroupofproperties) (dp)<br />[iddo:CountryOfUse](LandderVerwendung) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:NameInLanguage](NameinlanguageN) (dp)<br />[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:DateOfRevision](Dateofrevision) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp)<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />[iddo:DateOfActivation](Dateofactivation) (dp)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />
In range of |[iddo:hasPropertyGroupReference](haspropertygroupreference) (op)<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op)<br />
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PhysicalQuantity`
Description | <p>Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
### Possible value in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PossibleValueInLanguageN`
Description | <p>Moeglicher Wert fuer das Merkmal und Sprache Werte koennen String oder Zahlen sein</p>
Usage Note | PA039
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />
### Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Property`
Description | <p>Inherent or acquired feature of an item</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:ExampleInLanguage](BeispielinSpracheN) (dp) **min** 0<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:DateOfRevision](Dateofrevision) (dp) **exactly** 1<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:DescriptionInLanguage](BeschreibunginSpracheN) (dp) **min** 0<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp) **min** 0<br />[iddo:VisualRepresentation](Visualrepresentation) (dp) **min** 0<br />[iddo:hasBoundary](Boundaryvalues) (op) **exactly** 1 [iddo:BoundaryValue](Grenzwertliste) (c)<br />[iddo:DynamicProperty](DynamicProperty) (dp) **exactly** 1<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[iddo:hasTextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](Textformatitem) (c)<br />[iddo:SymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op) **min** 0 [iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op) **min** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:CountryOfUse](LandderVerwendung) (dp) **min** 1<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **max** 1<br />[iddo:NameOfTheDefiningValues](Namesofthedefiningvalues) (dp) **min** 0<br />[iddo:ListOfReplacingProperties](Listofreplacingproperties) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:DefiningValues](DefinierendeWerte) (op) **min** 0 [iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />[iddo:hasPhysicalQuantity](Physicalquantity) (op) **min** 1<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:DataType](Datentyp(GUID)) (dp) **exactly** 1<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **min** 0<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0<br />[iddo:MethodOfMeasurement](Messverfahren) (dp) **min** 0<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:hasUnit](hasunit) (op) **min** 1 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[iddo:DigitalFormat](DigitalesFormat) (op) **min** 0 [iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
In domain of |[iddo:ListOfReplacingProperties](Listofreplacingproperties) (op)<br />[iddo:DefiningValues](DefinierendeWerte) (op)<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op)<br />[iddo:Tolerance](Tolerance) (dp)<br />[iddo:hasPhysicalQuantity](Physicalquantity) (op)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:hasBoundary](Boundaryvalues) (op)<br />[iddo:ExampleInLanguage](BeispielinSpracheN) (dp)<br />[iddo:SymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />[iddo:CountryOfUse](LandderVerwendung) (dp)<br />[iddo:NameInLanguage](NameinlanguageN) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:DateOfRevision](Dateofrevision) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:DescriptionInLanguage](BeschreibunginSpracheN) (dp)<br />[iddo:DigitalFormat](DigitalesFormat) (op)<br />[iddo:hasUnit](hasunit) (op)<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op)<br />[iddo:hasDimension](Dimension) (op)<br />[iddo:DateOfLastChange](DatumderletztenAenderung) (dp)<br />[iddo:DataType](Datentyp(GUID)) (dp)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:MethodOfMeasurement](Messverfahren) (dp)<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:DateOfActivation](Dateofactivation) (dp)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:hasTextFormat](Textformat) (op)<br />
In range of |[iddo:hasConnectedProperty](VerbundeneMerkmale) (op)<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:ListOfReplacingProperties](Listofreplacingproperties) (op)<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op)<br />[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />
### Symbol of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolOfTheProperty`
Description | <p>Pair (symbol of the property, globally unique identifier of the group of properties (attribute GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op) **exactly** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Symbol](Symbol) (dp) **exactly** 1<br />
In domain of |[iddo:Symbol](Symbol) (dp)<br />
In range of |[iddo:SymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />
### Text format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormatItem`
Description | <p>Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Encoding](Encoding) (dp) **exactly** 1<br />[iddo:NumberOfCharacters](AnzahlderZeichen) (dp) **exactly** 1<br />
In domain of |[iddo:Encoding](Encoding) (dp)<br />[iddo:NumberOfCharacters](AnzahlderZeichen) (dp)<br />
In range of |[iddo:hasTextFormat](Textformat) (op)<br />

## Object Properties
[Defining value](#Definingvalue),
[Definierende Werte](#DefinierendeWerte),
[Digitales Format](#DigitalesFormat),
[Gegebene Merkmalsgruppe](#GegebeneMerkmalsgruppe),
[Merkmalsgruppe(n)](#Merkmalsgruppe(n)),
[Liste moeglicher Werte in Sprache N](#ListemoeglicherWerteinSpracheN),
[Liste ersetzter Merkmalsgruppen](#ListeersetzterMerkmalsgruppen),
[Liste ersetzter Merkmale](#ListeersetzterMerkmale),
[Liste ersetzender Merkmalsgruppen](#ListeersetzenderMerkmalsgruppen),
[List of replacing properties](#Listofreplacingproperties),
[Parameter des dynamischen Merkmals](#ParameterdesdynamischenMerkmals),
[uebergeordnete Merkmalsgruppe](#uebergeordneteMerkmalsgruppe),
[Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen](#BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen),
[Symbole des Merkmals in einer gegebenen Merk-malsgruppe](#SymboledesMerkmalsineinergegebenenMerk-malsgruppe),
[Boundary values](#Boundaryvalues),
[Grenzwert](#Grenzwert),
[Verbundene Merkmale](#VerbundeneMerkmale),
[hat den Verweis auf ein Referenzdokument](#hatdenVerweisaufeinReferenzdokument),
[has dictionary subset](#hasdictionarysubset),
[Dimension](#Dimension),
[has external dictionary](#hasexternaldictionary),
[has external dictionary property](#hasexternaldictionaryproperty),
[has External Dictionary Reference](#hasExternalDictionaryReference),
[Physical quantity](#Physicalquantity),
[hat Merkmal](#hatMerkmal),
[has property group reference](#haspropertygroupreference),
[hat Merkmalreferenz](#hatMerkmalreferenz),
[Textformat](#Textformat),
[has unit](#hasunit),
[](Definingvalue)
### Defining value
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValue`
Description | Enthaelt einen definierenden Wert eines Arrays
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />
Range(s) |[iddo:DefiningValueItem](DefinierenderWert-Item) (c)<br />
[](DefinierendeWerte)
### Definierende Werte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValues`
Description | Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />
[](DigitalesFormat)
### Digitales Format
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormat`
Description | Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
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
Description | Liste von Paaren (moeglicher Wert fuer das Merkmal und Sprache) Werte koennen String oder Zahlen sein
Usage Note | PA039
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />
[](ListeersetzterMerkmalsgruppen)
### Liste ersetzter Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacedGroupsOfProperties`
Description | List of globally unique identifiers of the replaced groups of properties
Usage Note | GA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](ListeersetzterMerkmale)
### Liste ersetzter Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacedProperties`
Description | Global eindeutiger Bezeichner des ersetzten Merkmals (oder der Merkmale)
Usage Note | PA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](ListeersetzenderMerkmalsgruppen)
### Liste ersetzender Merkmalsgruppen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacingGroupsOfProperties`
Description | Liste von globalen Bezeichnern fuer die ersetzenden Merkmalsgruppen
Usage Note | GA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Listofreplacingproperties)
### List of replacing properties
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
Description | List of GUIDS of properties which are parameters of the function for a dynamic property
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
[](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen)
### Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | List of pairs (group of properties internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing groups of properties
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](SymboledesMerkmalsineinergegebenenMerk-malsgruppe)
### Symbole des Merkmals in einer gegebenen Merk-malsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolsOfTheProperty`
Description | List of pairs (symbol of the property, globally unique identifier of the group of properties (attribute GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />
[](Boundaryvalues)
### Boundary values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundary`
Description | Pair (list of boundary intervals of possible values for the property, unit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:BoundaryValue](Grenzwertliste) (c)<br />
[](Grenzwert)
### Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundaryLimit`
Description | Einzelnes Grenzwertintervall
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryValue](Grenzwertliste) (c)<br />
Range(s) |[iddo:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
[](VerbundeneMerkmale)
### Verbundene Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasConnectedProperty`
Description | Liste der global eindeutigen Bezeichner der verbundenen Merkmale (Attribut PA001); der Wert eines Merkmals steht zu den Werten der anderen in einer Beziehung. Beispielsweise ist ein Schallabsorptionsgrad fuer eine bestimmte Frequenz gegeben, in diesem Fall sind Schallabsorp-tionsgrad und Frequenz ver-bundene Merkmale.
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](hatdenVerweisaufeinReferenzdokument)
### hat den Verweis auf ein Referenzdokument
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
Domain(s) |[iddo:Dictionary](Datenkatalog) (c)<br />
Range(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
[](Dimension)
### Dimension
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDimension`
Description | In case of a physical quantity, dimension according to ISO 80000 (all parts) This attribute allows the dimension to be machine readable; as all physical quantities are derived from 7 base quantities, it is provided with the power (as a rational number) attached to a basic dimension in the following order and with one space between each
Usage Note | PA028
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
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
Description | List of pairs (property internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing properties
Usage Note | PA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />
[](Physicalquantity)
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPhysicalQuantity`
Description | Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben --> http://qudt.org/vocab/quantitykind/Dimensionless dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.
Usage Note | PA027
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[qudt:QuantityKind](http://qudt.org/schema/qudt/QuantityKind) (c)<br />
[](hatMerkmal)
### hat Merkmal
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
[](hatMerkmalreferenz)
### hat Merkmalreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyReference`
Description | Fuegt ein Merkmal zu einer Merkmalszuweisung hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](Textformat)
### Textformat
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasTextFormat`
Description | Paar fuer den Texttyp (Verschluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
[](hasunit)
### has unit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasUnit`
Description | A unit to represent a scale that enables a value to be measured It is possible to use this attribute to explain there is no unit attached to the property by using unitless --> http://qudt.org/vocab/unit/UNITLESS
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:BoundaryLimitMax](ObererGrenzwert) (c)<br />[iddo:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />

## Datatype Properties
[Category of group of properties](#Categoryofgroupofproperties),
[Ursprungsland](#Ursprungsland),
[Land der Verwendung](#LandderVerwendung),
[Erlaeuterung fuer die Ablehnung](#ErlaeuterungfuerdieAblehnung),
[Datentyp (GUID)](#Datentyp(GUID)),
[Date of activation](#Dateofactivation),
[Datum der Erstellung](#DatumderErstellung),
[Datum der Deaktivierung](#DatumderDeaktivierung),
[Datum der letzten Aenderung](#DatumderletztenAenderung),
[Date of revision](#Dateofrevision),
[Datum der Version](#DatumderVersion),
[Definition in Sprache N](#DefinitioninSpracheN),
[Deprecation explanation](#Deprecationexplanation),
[Beschreibung in Sprache N](#BeschreibunginSpracheN),
[Dynamic Property](#DynamicProperty),
[Encoding](#Encoding),
[Beispiel in Sprache N](#BeispielinSpracheN),
[Global eindeutiger Bezeichner (GUID)](#GlobaleindeutigerBezeichner(GUID)),
[inclusive](#inclusive),
[Messverfahren](#Messverfahren),
[Name in language N](#NameinlanguageN),
[Names of the defining values](#Namesofthedefiningvalues),
[Anzahl der Zeichen](#AnzahlderZeichen),
[Toleranz](#Toleranz),
[Nummer der ueberarbeitung](#Nummerderueberarbeitung),
[Status](#Status),
[Subdivision of use](#Subdivisionofuse),
[Symbol](#Symbol),
[Toleranz](#Tolerance),
[Version number](#Versionnumber),
[Visual representation](#Visualrepresentation),
[](Categoryofgroupofproperties)
### Category of group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CategoryOfGroupOfProperties`
Description | Gibt die Kategorie der erstellten Merkmalsgruppe an
Usage Note | GA022
Example | ````Alternative use`<br />```
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
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](LandderVerwendung)
### Land der Verwendung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfUse`
Description | Land (Gruppe von Laendern, Kon-tinent), in dem das Merkmal/die Merkmalsgruppe fuer den Markt, auf dem die Beteiligten arbeiten, relevant ist
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ErlaeuterungfuerdieAblehnung)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CreatorsLanguage`
Description | Satz, der den Grund fuer die Ab-lehnung erlaeutert, der erklaeren kann, wie Werte umzurechnen sind, damit sie dem neuen Merkmal entsprechen; diese Er-laeuterung muss in internatio-nalem Englisch (EN) geschrieben werden
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Datentyp(GUID))
### Datentyp (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DataType`
Description | Format fuer die Angabe des Wertes des Merkmals dies kann aus einer Soft-ware-Perspektive als Speiche-rungsart verstanden werden im Falle eines dynamischen Merkmals ist der Wert dieses Attributs der Datentyp des Er-gebnisses der Berechnung mit der Gleichung
Usage Note | PA030
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Dateofactivation)
### Date of activation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfActivation`
Description | Date after when the property can be used
Usage Note | PA04/GA04
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderErstellung)
### Datum der Erstellung
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
Description | Datum der Deaktivierung
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
Description | Date of revision
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
[](DefinitioninSpracheN)
### Definition in Sprache N
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
Description | Satz, der den Grund fuer die Ablehnung erlaeutert, der erklaeren kann, wie Werte umzurechnen sind, damit sie dem neuen Merkmal/der neuen Merkmalsgruppe entsprechen; diese Erlaeuterung muss in internationalem Englisch (EN) geschrieben werden
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](BeschreibunginSpracheN)
### Beschreibung in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DescriptionInLanguage`
Description | List of pairs (Description of the property, language)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DynamicProperty)
### Dynamic Property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DynamicProperty`
Description | If this is a dynamic property, the value is dependent on the parameters provided in the attribute PA032
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
Domain(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](BeispielinSpracheN)
### Beispiel in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExampleInLanguage`
Description | Liste von Paaren (Beispiel des Merkmals, Sprache)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](GlobaleindeutigerBezeichner(GUID))
### Global eindeutiger Bezeichner (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GloballyUniqueIdentifier`
Description | Unique identifier generated using the algorithm denoted in RFC 4122
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](inclusive)
### inclusive
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Inclusive`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:BoundaryLimitMax](ObererGrenzwert) (c)<br />[iddo:BoundaryLimitMin](MinimumBoundaryLimit) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](Messverfahren)
### Messverfahren
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#MethodOfMeasurement`
Description | Beurteilung von Bauprodukten, um ihre Tauglichkeit entsprechend den Anforderungen in harmonisierten technischen Spezifikationen sicherzustellen
Usage Note | PA029
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](NameinlanguageN)
### Name in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NameInLanguage`
Description | List of pairs (property name and language) This attribute can be used to add synonyms for different domains
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Namesofthedefiningvalues)
### Names of the defining values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NameOfTheDefiningValues`
Description | In case of an array, this attribute provides the names of the column headers defined as a list of pairs (name, language)
Usage Note | PA034
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](AnzahlderZeichen)
### Anzahl der Zeichen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NumberOfCharacters`
Description | Die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Toleranz)
### Toleranz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Precision`
Description | Praezision ist die Anzahl signifi-kanter Stellen
Usage Note | PA037
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Nummerderueberarbeitung)
### Nummer der ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RevisionNumber`
Description | This revision number allows tracking of minor changes e.g. new translation, changes of typos: if the version number changes, the revision number starts again at 1 Experts decide if a new revision number can be applied or if a new revision is needed
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Status)
### Status
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Status`
Description | Status of the property during its life cycle
Usage Note | PA002/GA002
Example | ````active`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Subdivisionofuse)
### Subdivision of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SubdivisionOfUse`
Description | Documented geographical region of use of the group of properties
Usage Note | PA025/GA020
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
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
[](Visualrepresentation)
### Visual representation
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