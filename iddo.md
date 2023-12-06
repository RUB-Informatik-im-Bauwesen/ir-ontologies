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
[Defining value item](#Definingvalueitem),
[Defining values list](#Definingvalueslist),
[Dictionary subset](#Dictionarysubset),
[Digitales Format-Item](#DigitalesFormat-Item),
[Dimension](#Dimension1),
[External Dictionary Reference](#ExternalDictionaryReference),
[Grenzwertliste](#Grenzwertliste),
[Group of properties](#Groupofproperties),
[Merkmal](#Merkmal),
[Oberer Grenzwert](#ObererGrenzwert),
[Physical quantity](#PhysicalQuantity),
[Possible value in language N](#PossiblevalueinlanguageN),
[Referenzdokument](#Referenzdokument),
[Symbol des Merkmals in einer gegebenen Merkmalsgruppe](#SymboldesMerkmalsineinergegebenenMerkmalsgruppe),
[Textformat-Item](#Textformat-Item),
[Unterer Grenzwert](#UntererGrenzwert),
[Zugewiesenes Merkmal](#ZugewiesenesMerkmal),
### Zugewiesenes Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#AssignedProperty`
Description | <p>Represents the assignment of a property and a property state to a feature of interest (FOI).</p>
Super-classes |[http://www.w3id.org/opm#Property](http://www.w3id.org/opm#Property) (c)<br />
Restrictions |[iddo:hasPropertyReference](hatMerkmalreferenz) (op) **exactly** 1<br />[http://www.w3id.org/opm#hasPropertyState](http://www.w3id.org/opm#hasPropertyState) **min** 1<br />
In domain of |[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />
In range of |[iddo:hasProperty](hatMerkmal) (op)<br />
### Oberer Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMax`
Description | <p>Grenzwertintervall bestehend aus der oberen(maxValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[iddo:Units](Einheiten) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />
In domain of |[iddo:Units](Einheiten) (op)<br />
### Unterer Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMin`
Description | <p>Boundary limit interval consisting of the lower(minValue) interval boundary</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />[iddo:Units](Einheiten) (op) **exactly** 1<br />
In domain of |[iddo:Units](Einheiten) (op)<br />
In range of |[iddo:hasBoundaryLimit](Boundaryvalue) (op)<br />
### Grenzwertliste
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValue`
Description | <p>Pair  (List of boundary intervals of possible values for the property, unit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasBoundaryLimit](Boundaryvalue) (op) **max** 1 [iddo:BoundaryLimitMax](ObererGrenzwert) (c)<br />[iddo:hasBoundaryLimit](Boundaryvalue) (op) **max** 1 [iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />
In domain of |[iddo:hasBoundaryLimit](Boundaryvalue) (op)<br />
In range of |[iddo:hasBoundary](Boundaryvalues) (op)<br />
### Defining value item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValueItem`
Description | <p>Contains a defining value of an array in the form of a literal</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:DefiningValue](Definingvalue) (op)<br />
### Defining values list
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValuesList`
Description | <p>In case of an array, this attribute provides the defining values when applicable, the datatype is given by the attribute PA030</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DefiningValueItem](Definingvalueitem) **min** 1<br />
In domain of |[iddo:DefiningValue](Definingvalue) (op)<br />
In range of |[iddo:DefiningValues](DefinierendeWerte) (op)<br />
### Data dictionary
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dictionary`
Description | <p>Centralized repository of information about data such as meaning, relationships to other data, origin, usage and format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[iddo:hasDictionarySubset](hasdictionarysubset) (op) **min** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />
In domain of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Referenzdokument
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
Description | <p>Definiert eine Teilmenge oder Untergruppierung eines Datenkatalogs</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op) **exactly** 1<br />[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />
In domain of |[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op)<br />
In range of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Digitales Format-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormatItem`
Description | <p>Pair for digital text type (precision, unit) Precision is the number of significant digits</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Precision](Toleranz) (dp) **exactly** 1<br />[iddo:Unit](Einheit) (op) **exactly** 1<br />
In domain of |[iddo:Precision](Toleranz) (dp)<br />[iddo:Unit](Einheit) (op)<br />
In range of |[iddo:DigitalFormat](Digitalformat) (op)<br />
### Dimension
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dimension`
Description | <p>In case of a physical quantity, dimension according to ISO 80000 (all parts) This attribute allows the dimension to be machine readable; as all physical quantities are derived from 7 base quantities, it is provided with the power (as a rational number) attached to a basic dimension in the following order and with one space between each</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasL](hasL) (dp) **exactly** 1<br />[iddo:hasT](hasT) (dp) **exactly** 1<br />[iddo:hasN](hasN) (dp) **exactly** 1<br />[iddo:hasJ](hasJ) (dp) **exactly** 1<br />[iddo:hasM](hasM) (dp) **exactly** 1<br />[iddo:hasTheta](hasTheta) (dp) **exactly** 1<br />[iddo:hasI](hasI) (dp) **exactly** 1<br />
In range of |[iddo:hasDimension](Dimension) (op)<br />
### External Dictionary Reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExternalDictionaryReference`
Description | <p>Pair (property internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing properties</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty](http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty) **exactly** 1<br />[http://inf.bi.rub.de/ontology/dt#hasExternalDictionary](http://inf.bi.rub.de/ontology/dt#hasExternalDictionary) **exactly** 1<br />
In range of |[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />
### Group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupOfProperties`
Description | <p>Sammlung, die es ermoeglicht, die Merkmale vorauszuplanen oder zu organisieren</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:RevisionNumber](Revisionnumber) (dp) **exactly** 1<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[iddo:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **exactly** 1<br />[iddo:ParentGroupOfProperties](Parentgroupofproperties) (op) **min** 0 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:DateOfVersion](Dateofversion) (dp) **exactly** 1<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[iddo:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp) **exactly** 1<br />[iddo:ParentGroupOfProperties](Parentgroupofproperties) (op) **max** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:hasDimension](Dimension) (op) **min** 0<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:VisualRepresentation](Visualrepresentation) (dp) **min** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />
In domain of |[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:VersionNumber](Versionsnummer) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:NameInLanguage](NameinlanguageN) (dp)<br />[iddo:ParentGroupOfProperties](Parentgroupofproperties) (op)<br />[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:DateOfVersion](Dateofversion) (dp)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp)<br />[iddo:RevisionNumber](Revisionnumber) (dp)<br />
In range of |[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:GroupsOfProperties](Group(s)ofproperties) (op)<br />[iddo:ParentGroupOfProperties](Parentgroupofproperties) (op)<br />[iddo:hasPropertyGroupReference](haspropertygroupreference) (op)<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op)<br />
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PhysicalQuantity`
Description | <p>List of pairs (physical quantity | language) Physical quantities are expressed in International System (SI) units Non-physical quantities such as text are expressed with the value "without" This is equivalent to a measure in ISO 16739-1 and ISO 10303 Only one physical quantity can be attached to a property. This attribute is used to provide the quantity in plain text with all the needed translations</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:hasDimension](Dimension) (op) **some** [iddo:Dimension](Dimension1) (c)<br />
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
Description | <p>Inhaerente oder erworbene Eigenschaft eines Datenelements</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:CountryOfOrigin](Ursprungsland) (dp) **max** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:hasDimension](Dimension) (op) **min** 0 [iddo:Dimension](Dimension1) (c)<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:RevisionNumber](Revisionnumber) (dp) **exactly** 1<br />[iddo:hasBoundary](Boundaryvalues) (op) **exactly** 1 [iddo:BoundaryValue](Grenzwertliste) (c)<br />[iddo:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp) **min** 0<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[iddo:DefiningValues](DefinierendeWerte) (op) **min** 0 [iddo:DefiningValuesList](Definingvalueslist) (c)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp) **min** 0<br />[iddo:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **min** 0<br />[iddo:DigitalFormat](Digitalformat) (op) **min** 0 [iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:DescriptionInLanguage](BeschreibunginSpracheN) (dp) **min** 0<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op) **min** 0 [iddo:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />[iddo:ExampleInLanguage](ExampleinlanguageN) (dp) **min** 0<br />[iddo:hasPhysicalQuantity](Physicalquantity) (dp) **min** 1<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:hasDimension](Dimension) (op) **max** 1 [iddo:Dimension](Dimension1) (c)<br />[iddo:NameOfTheDefiningValues](NamederdefinierendenWerte) (dp) **min** 0<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:DynamicProperty](DynamischesMerkmal) (dp) **exactly** 1<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:TextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](Textformat-Item) (c)<br />[iddo:GroupsOfProperties](Group(s)ofproperties) (op) **min** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:DataType](Datentyp(GUID)) (dp) **exactly** 1<br />[iddo:Units](Einheiten) (op) **min** 0<br />[iddo:DateOfVersion](Dateofversion) (dp) **exactly** 1<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />
In domain of |[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:GroupsOfProperties](Group(s)ofproperties) (op)<br />[iddo:DataType](Datentyp(GUID)) (dp)<br />[iddo:VersionNumber](Versionsnummer) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:hasBoundary](Boundaryvalues) (op)<br />[iddo:hasExternalDictionaryReference](hasExternalDictionaryReference) (op)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />[iddo:DescriptionInLanguage](BeschreibunginSpracheN) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:NameInLanguage](NameinlanguageN) (dp)<br />[iddo:Units](Einheiten) (op)<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op)<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />[iddo:DigitalFormat](Digitalformat) (op)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:hasDimension](Dimension) (op)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:DateOfVersion](Dateofversion) (dp)<br />[iddo:hasPhysicalQuantity](Physicalquantity) (dp)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp)<br />[iddo:TextFormat](Textformat) (op)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op)<br />[iddo:Tolerance](Tolerance) (dp)<br />[iddo:RevisionNumber](Revisionnumber) (dp)<br />[iddo:DefiningValues](DefinierendeWerte) (op)<br />[iddo:ExampleInLanguage](ExampleinlanguageN) (dp)<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp)<br />[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />
In range of |[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op)<br />[iddo:hasConnectedProperty](VerbundeneMerkmale) (op)<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />
### Symbol des Merkmals in einer gegebenen Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolOfTheProperty`
Description | <p>Pair (symbol of the property, globally unique identifier of the group of properties (attribute GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op) **exactly** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Symbol](Symbol) (dp) **exactly** 1<br />
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
In domain of |[iddo:Encoding](Encoding) (dp)<br />[iddo:NumberOfCharacters](AnzahlderZeichen) (dp)<br />
In range of |[iddo:TextFormat](Textformat) (op)<br />

## Object Properties
[Defining value](#Definingvalue),
[Definierende Werte](#DefinierendeWerte),
[Digital format](#Digitalformat),
[Gegebene Merkmalsgruppe](#GegebeneMerkmalsgruppe),
[Group(s) of properties](#Group(s)ofproperties),
[Liste moeglicher Werte in Sprache N](#ListemoeglicherWerteinSpracheN),
[Liste ersetzter Merkmalsgruppen](#ListeersetzterMerkmalsgruppen),
[List of replaced properties](#Listofreplacedproperties),
[Liste ersetzender Merkmalsgruppen](#ListeersetzenderMerkmalsgruppen),
[Liste ersetzender Merkmale](#ListeersetzenderMerkmale),
[Parameters of the dynamic property](#Parametersofthedynamicproperty),
[Parent group of properties](#Parentgroupofproperties),
[Relations of the group of properties identifiers in the interconnected data dictionaries](#Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries),
[Symbols of the property in a given property group](#Symbolsofthepropertyinagivenpropertygroup),
[Textformat](#Textformat),
[Einheit](#Einheit),
[Einheiten](#Einheiten),
[Boundary values](#Boundaryvalues),
[Boundary value](#Boundaryvalue),
[Verbundene Merkmale](#VerbundeneMerkmale),
[hat den Verweis auf ein Referenzdokument](#hatdenVerweisaufeinReferenzdokument),
[has dictionary subset](#hasdictionarysubset),
[Dimension](#Dimension),
[has external dictionary](#hasexternaldictionary),
[has external dictionary property](#hasexternaldictionaryproperty),
[has External Dictionary Reference](#hasExternalDictionaryReference),
[hat Merkmal](#hatMerkmal),
[has property group reference](#haspropertygroupreference),
[hat Merkmalreferenz](#hatMerkmalreferenz),
[](Definingvalue)
### Defining value
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValue`
Description | Contains a defining value of an array
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DefiningValuesList](Definingvalueslist) (c)<br />
Range(s) |[iddo:DefiningValueItem](Definingvalueitem) (c)<br />
[](DefinierendeWerte)
### Definierende Werte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValues`
Description | Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:DefiningValuesList](Definingvalueslist) (c)<br />
[](Digitalformat)
### Digital format
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormat`
Description | Pair for digital text type (precision, unit) Precision is the number of significant digits
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
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Group(s)ofproperties)
### Group(s) of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupsOfProperties`
Description | List of globally unique identifiers of groups of properties (attribute GA001) to which the property is attached
Usage Note | PA021
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
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
Description | Liste von globalen Bezeichnern fuer die ersetzten Merk-malsgruppen
Usage Note | GA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Listofreplacedproperties)
### List of replaced properties
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
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
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
[](Parametersofthedynamicproperty)
### Parameters of the dynamic property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ParametersOfTheDynamicProperty`
Description | Liste von GUIDs von Merkmalen, welche Parameter der Funktion fuer ein dynamisches Merkmal sind
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](Parentgroupofproperties)
### Parent group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ParentGroupOfProperties`
Description | Ermoeglicht die Ver-knuepfung einer Unter-gruppe mit einer ueber-geordneten Gruppe ueber ihre global ein-deutigen Bezeichner (Attribut GA001) jedes einer Gruppe zugehoerige Merkmal wird von der/den Untergruppe(n) uebernommen
Usage Note | GA023
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries)
### Relations of the group of properties identifiers in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | List of pairs (group of properties internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing groups of properties
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Symbolsofthepropertyinagivenpropertygroup)
### Symbols of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolsOfTheProperty`
Description | Liste von Paaren (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />
[](Textformat)
### Textformat
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormat`
Description | Paar fuer den Texttyp (Ver-schluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:TextFormatItem](Textformat-Item) (c)<br />
[](Einheit)
### Einheit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Unit`
Description | Masseinheit fuer den digitalen Texttyp
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](Einheiten)
### Einheiten
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Units`
Description | Eine Einheit zur Darstellung einer Skala, die es ermoeglicht, einen Wert zu messen es ist moeglich, dieses Attribut zu verwenden, um zu erlaeutern, dass dem Merkmal keine Einheit zugeordnet ist, indem einheitslos verwendet wird
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />[iddo:BoundaryLimitMax](ObererGrenzwert) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](Boundaryvalues)
### Boundary values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundary`
Description | Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:BoundaryValue](Grenzwertliste) (c)<br />
[](Boundaryvalue)
### Boundary value
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundaryLimit`
Description | Single Boundary value interval
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryValue](Grenzwertliste) (c)<br />
Range(s) |[iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />
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
Range(s) |[iddo:DictionaryReferenceDocument](Referenzdokument) (c)<br />
[](hasdictionarysubset)
### has dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDictionarySubset`
Super-properties |[dcat:dataset](http://www.w3.org/ns/dcat#dataset)<br />
Domain(s) |[iddo:Dictionary](Datadictionary) (c)<br />
Range(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
[](Dimension)
### Dimension
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDimension`
Description | Im Falle einer physikalischen Groesse, Dimension nach ISO 80000 (alle Teile) dieses Attribut ermoeglicht, dass die Dimension maschinenlesbar ist; da alle physikalischen Groessen von 7 Basisgroessen abgeleitet sind, wird es durch Angabe der Basisdimensionen mit zugehoeriger Potenz (als rationale Zahl) in der folgenden Reihenfolge und mit jeweils einem Leerzeichen dazwischen angegeben
Usage Note | PA028
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Dimension](Dimension1) (c)<br />
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
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />
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
Description | Attaches a property group reference to a iddo:ReferenceDocument
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:ReferenceDocument](https://w3id.org/iddo/v2#ReferenceDocument) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](hatMerkmalreferenz)
### hat Merkmalreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyReference`
Description | Attaches a property reference to a property assignment
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />

## Datatype Properties
[Kategorie der Merkmalsgruppe](#KategoriederMerkmalsgruppe),
[Ursprungsland](#Ursprungsland),
[Country of use](#Countryofuse),
[Creator's language](#Creator'slanguage),
[Datentyp (GUID)](#Datentyp(GUID)),
[Datum der Aktivierung](#DatumderAktivierung),
[Datum der Erstellung](#DatumderErstellung),
[Date of deactivation](#Dateofdeactivation),
[Date of last change](#Dateoflastchange),
[Datum der Ueberarbeitung](#DatumderUeberarbeitung),
[Date of version](#Dateofversion),
[Definition in Sprache N](#DefinitioninSpracheN),
[Deprecation explanation](#Deprecationexplanation),
[Beschreibung in Sprache N](#BeschreibunginSpracheN),
[Dynamisches Merkmal](#DynamischesMerkmal),
[Encoding](#Encoding),
[Example in language N](#ExampleinlanguageN),
[Global eindeutiger Bezeichner (GUID)](#GlobaleindeutigerBezeichner(GUID)),
[Method of measurement](#Methodofmeasurement),
[Name in language N](#NameinlanguageN),
[Name der definierenden Werte](#NamederdefinierendenWerte),
[Anzahl der Zeichen](#AnzahlderZeichen),
[Toleranz](#Toleranz),
[Revision number](#Revisionnumber),
[Status](#Status),
[Subdivision of use](#Subdivisionofuse),
[Symbol](#Symbol),
[Tolerance](#Tolerance),
[Versionsnummer](#Versionsnummer),
[Visual representation](#Visualrepresentation),
[has I](#hasI),
[has J](#hasJ),
[has L](#hasL),
[has M](#hasM),
[has N](#hasN),
[Physical quantity](#Physicalquantity),
[has T](#hasT),
[has Theta](#hasTheta),
[](KategoriederMerkmalsgruppe)
### Kategorie der Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CategoryOfGroupOfProperties`
Description | Specifies the category of the created property group
Usage Note | GA022
Example | ````Composed property`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Ursprungsland)
### Ursprungsland
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfOrigin`
Description | Country from where the requirement for this property/group of properties originated
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Countryofuse)
### Country of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfUse`
Description | Land (Gruppe von Laendern, Kon-tinent), in dem das Merkmal/die Merkmalsgruppe fuer den Markt, auf dem die Beteiligten arbeiten, relevant ist
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Creator'slanguage)
### Creator's language
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CreatorsLanguage`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property; this explanation has to be written in international English (EN)
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Datentyp(GUID))
### Datentyp (GUID)
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
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderErstellung)
### Datum der Erstellung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfCreation`
Description | Datum der Validierung der An-frage zur Erstellung des Merkmals durch Sachverstaendige
Usage Note | PA003/GA003
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofdeactivation)
### Date of deactivation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfDeactivation`
Description | Datum der Deaktivierung
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateoflastchange)
### Date of last change
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfLastChange`
Description | Date of validation of the last change request by experts
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderUeberarbeitung)
### Datum der Ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfRevision`
Description | Datum der Ueberarbeitung
Usage Note | PA006/GA006
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofversion)
### Date of version
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfVersion`
Description | Date of version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DefinitioninSpracheN)
### Definition in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefinitionInLanguage`
Description | List of pairs (definition of the property/group of properties, language)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Deprecationexplanation)
### Deprecation explanation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DeprecationExplanation`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property/group of properties; this explanation has to be written in international English (EN)
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
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
[](DynamischesMerkmal)
### Dynamisches Merkmal
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
Domain(s) |[iddo:TextFormatItem](Textformat-Item) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ExampleinlanguageN)
### Example in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExampleInLanguage`
Description | List of pairs (example of the property, language)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](GlobaleindeutigerBezeichner(GUID))
### Global eindeutiger Bezeichner (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GloballyUniqueIdentifier`
Description | Eindeutiger Bezeichner, der mit dem in RFC 4122 beschriebenen Algorithmus erzeugt wird
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Methodofmeasurement)
### Method of measurement
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#MethodOfMeasurement`
Description | Evaluation of construction products to ensure their fitness according to requirements in harmonised technical specifications
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
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
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
[](Revisionnumber)
### Revision number
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RevisionNumber`
Description | This revision number allows tracking of minor changes e.g. new translation, changes of typos: if the version number changes, the revision number starts again at 1 Experts decide if a new revision number can be applied or if a new revision is needed
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
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
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
[](Subdivisionofuse)
### Subdivision of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SubdivisionOfUse`
Description | Dokumentierte geographische Region, in der das Merkmal/ die Merkmalsgruppe verwendet wird
Usage Note | PA025/GA020
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
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
[](Tolerance)
### Tolerance
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Tolerance`
Description | Fuer numerische Werte; der Gesamtbetrag, um den eine be-stimmte Einheit schwanken darf; sie ist die Differenz zwischen dem Hoechstwert und dem Mindestwert fuer die Einheit
Usage Note | PA036
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Versionsnummer)
### Versionsnummer
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VersionNumber`
Description | Diese Versionsnummer ermoeglicht die Verfolgung groesserer aenderungen. Sachverstaendige entscheiden, ob eine neue Ver-sionsnummer angewendet werden muss.
Usage Note | PA009/GA009
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Visualrepresentation)
### Visual representation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VisualRepresentation`
Description | Visual representation of the group of properties through sketches, photos, videos or other multimedia objects
Usage Note | PA023/GA018
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](hasI)
### has I
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasI`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](hasJ)
### has J
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasJ`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](hasL)
### has L
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasL`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](hasM)
### has M
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasM`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](hasN)
### has N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasN`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Physicalquantity)
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPhysicalQuantity`
Description | Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.
Usage Note | PA027
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](hasT)
### has T
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasT`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](hasTheta)
### has Theta
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasTheta`
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />

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