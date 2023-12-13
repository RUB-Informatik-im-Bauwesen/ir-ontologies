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
[Assigned property](#Assignedproperty),
[Boundary values list](#Boundaryvalueslist),
[Datenkatalog](#Datenkatalog),
[Defining value item](#Definingvalueitem),
[Defining values list](#Definingvalueslist),
[Dictionary subset](#Dictionarysubset),
[Digitales Format-Item](#DigitalesFormat-Item),
[Dimension](#Dimension1),
[External Dictionary Reference](#ExternalDictionaryReference),
[Merkmalsgruppe](#Merkmalsgruppe),
[Oberer Grenzwert](#ObererGrenzwert),
[Physical quantity](#Physicalquantity),
[Possible value in language N](#PossiblevalueinlanguageN),
[Property](#Property),
[Reference document](#Referencedocument),
[Symbol des Merkmals in einer gegebenen Merkmalsgruppe](#SymboldesMerkmalsineinergegebenenMerkmalsgruppe),
[Text format item](#Textformatitem),
[Unterer Grenzwert](#UntererGrenzwert),
### Assigned property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#AssignedProperty`
Description | <p>Repraesentiert die Zweisung eines Merkmals und einer Merkmalszustandes an ein Feature of Interest (FOI)</p>
Super-classes |[http://www.w3id.org/opm#Property](http://www.w3id.org/opm#Property) (c)<br />
Restrictions |[http://www.w3id.org/opm#hasPropertyState](http://www.w3id.org/opm#hasPropertyState) **min** 1<br />[iddo:hasPropertyReference](hasPropertyReference) (op) **exactly** 1<br />
In domain of |[iddo:hasPropertyReference](hasPropertyReference) (op)<br />
In range of |[iddo:hasProperty](hasproperty) (op)<br />
### Oberer Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMax`
Description | <p>Grenzwertintervall bestehend aus der oberen(maxValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[iddo:hasUnit](hasunit) (op) **exactly** 1<br />[sdo:value](https://schema.org/value) **exactly** 1<br />
In domain of |[iddo:hasUnit](hasunit) (op)<br />
### Unterer Grenzwert
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryLimitMin`
Description | <p>Boundary limit interval consisting of the lower(minValue) interval boundary</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />[iddo:hasUnit](hasunit) (op) **exactly** 1<br />
In domain of |[iddo:hasUnit](hasunit) (op)<br />
In range of |[iddo:hasBoundaryLimit](Boundaryvalue) (op)<br />
### Boundary values list
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValue`
Description | <p>Pair  (List of boundary intervals of possible values for the property, unit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasBoundaryLimit](Boundaryvalue) (op) **max** 1 [iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />[iddo:hasBoundaryLimit](Boundaryvalue) (op) **max** 1 [iddo:BoundaryLimitMax](ObererGrenzwert) (c)<br />
In domain of |[iddo:hasBoundaryLimit](Boundaryvalue) (op)<br />
In range of |[iddo:hasBoundary](Grenzwerte) (op)<br />
### Defining value item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValueItem`
Description | <p>Enthaelt einen definierenden Wert eines Arrays in Form eines Literals</p>
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
### Datenkatalog
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dictionary`
Description | <p>Centralized repository of information about data such as meaning, relationships to other data, origin, usage and format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op) **min** 1<br />
In domain of |[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
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
Description | <p>Definiert eine Teilmenge oder Untergruppierung eines Datenkatalogs</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op) **exactly** 1<br />[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />
In domain of |[iddo:hasDictionaryReferenceDocument](hatdenVerweisaufeinReferenzdokument) (op)<br />
In range of |[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Digitales Format-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormatItem`
Description | <p>Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Precision](Tolerance) (dp) **exactly** 1<br />[iddo:Unit](Unit) (op) **exactly** 1<br />
In domain of |[iddo:Unit](Unit) (op)<br />[iddo:Precision](Tolerance) (dp)<br />
In range of |[iddo:DigitalFormat](Digitalformat) (op)<br />
### Dimension
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dimension`
Description | <p>In case of a physical quantity, dimension according to ISO 80000 (all parts) This attribute allows the dimension to be machine readable; as all physical quantities are derived from 7 base quantities, it is provided with the power (as a rational number) attached to a basic dimension in the following order and with one space between each</p>
Super-classes |[qudt:QuantityKindDimensionVector_SI](http://qudt.org/schema/qudt/QuantityKindDimensionVector_SI) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:hasT](hasT) (dp) **exactly** 1<br />[iddo:hasI](hasI) (dp) **exactly** 1<br />[iddo:hasM](hasM) (dp) **exactly** 1<br />[iddo:hasTheta](hasTheta) (dp) **exactly** 1<br />[qudt:dimensionExponentForLength](http://qudt.org/schema/qudt/dimensionExponentForLength) **exactly** 1<br />[iddo:hasJ](hasJ) (dp) **exactly** 1<br />[iddo:hasN](hasN) (dp) **exactly** 1<br />
In range of |[iddo:hasDimension](Dimension) (op)<br />
### External Dictionary Reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ExternalDictionaryReference`
Description | <p>Pair (property internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing properties</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty](http://inf.bi.rub.de/ontology/dt#hasExternalDictionaryProperty) **exactly** 1<br />[http://inf.bi.rub.de/ontology/dt#hasExternalDictionary](http://inf.bi.rub.de/ontology/dt#hasExternalDictionary) **exactly** 1<br />
In range of |[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />
### Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupOfProperties`
Description | <p>Collection enabling the properties to be prearranged or organized</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:RevisionNumber](Revisionnumber) (dp) **exactly** 1<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 1<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp) **exactly** 1<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp) **min** 0<br />[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:hasDimension](Dimension) (op) **min** 0<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **max** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:CountryOfOrigin](Countryoforigin) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Tolerance](Toleranz) (dp) **min** 0<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:DateOfRevision](Dateofrevision) (dp) **exactly** 1<br />
In domain of |[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:RevisionNumber](Revisionnumber) (dp)<br />[iddo:DateOfRevision](Dateofrevision) (dp)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op)<br />[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp)<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp)<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:CountryOfOrigin](Countryoforigin) (dp)<br />
In range of |[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op)<br />[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:ListOfReplacingGroupsOfProperties](ListeersetzenderMerkmalsgruppen) (op)<br />[iddo:hasPropertyGroupReference](haspropertygroupreference) (op)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />
### Physical quantity
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PhysicalQuantity`
Description | <p>Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.</p>
Super-classes |[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:hasDimension](Dimension) (op) **some** [iddo:Dimension](Dimension1) (c)<br />
### Possible value in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PossibleValueInLanguageN`
Description | <p>Moeglicher Wert fuer das Merkmal und Sprache Werte koennen String oder Zahlen sein</p>
Usage Note | PA039
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:ListOfPossibleValuesInLanguageN](ListofpossiblevaluesinlanguageN) (op)<br />
### Property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Property`
Description | <p>Inhaerente oder erworbene Eigenschaft eines Datenelements</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[http://inf.bi.rub.de/ontology/dt#LibraryComponent](http://inf.bi.rub.de/ontology/dt#LibraryComponent) (c)<br />
Restrictions |[iddo:TextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](Textformatitem) (c)<br />[iddo:hasConnectedProperty](Connectedproperties) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:CountryOfOrigin](Countryoforigin) (dp) **min** 0<br />[iddo:DataType](Datatype) (dp) **exactly** 1<br />[iddo:RevisionNumber](Revisionnumber) (dp) **exactly** 1<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:Tolerance](Toleranz) (dp) **min** 0<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:hasPhysicalQuantity](PhysikalischeGroesse) (dp) **min** 1<br />[iddo:ListOfPossibleValuesInLanguageN](ListofpossiblevaluesinlanguageN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **max** 1<br />[iddo:DefiningValues](DefinierendeWerte) (op) **min** 0 [iddo:DefiningValuesList](Definingvalueslist) (c)<br />[iddo:CountryOfOrigin](Countryoforigin) (dp) **max** 1<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:NameOfTheDefiningValues](NamederdefinierendenWerte) (dp) **min** 0<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op) **min** 0 [iddo:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />[iddo:hasDimension](Dimension) (op) **max** 1 [qudt:QuantityKindDimensionVector](http://qudt.org/schema/qudt/QuantityKindDimensionVector) (c)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 0<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp) **min** 0<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:hasUnit](hasunit) (op) **min** 0 [qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />[iddo:DateOfRevision](Dateofrevision) (dp) **exactly** 1<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp) **exactly** 1<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:DigitalFormat](Digitalformat) (op) **min** 0 [iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp) **min** 0<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op) **min** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp) **min** 0<br />[iddo:hasDimension](Dimension) (op) **min** 0 [qudt:QuantityKindDimensionVector](http://qudt.org/schema/qudt/QuantityKindDimensionVector) (c)<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:DynamicProperty](DynamischesMerkmal) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp) **min** 0<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op) **min** 0 [iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:ExampleInLanguage](BeispielinSpracheN) (dp) **min** 0<br />[iddo:ListOfPossibleValuesInLanguageN](ListofpossiblevaluesinlanguageN) (op) **min** 0<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:hasBoundary](Grenzwerte) (op) **exactly** 1 [iddo:BoundaryValue](Boundaryvalueslist) (c)<br />
In domain of |[iddo:hasConnectedProperty](Connectedproperties) (op)<br />[iddo:DigitalFormat](Digitalformat) (op)<br />[iddo:DefiningValues](DefinierendeWerte) (op)<br />[iddo:DataType](Datatype) (dp)<br />[iddo:DeprecationExplanation](Deprecationexplanation) (dp)<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op)<br />[iddo:hasUnit](hasunit) (op)<br />[iddo:hasExternalDictionaryReference](hatexterneDictionaryReferenz) (op)<br />[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op)<br />[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:CreatorsLanguage](Creator'slanguage) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:hasBoundary](Grenzwerte) (op)<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:hasPhysicalQuantity](PhysikalischeGroesse) (dp)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />[iddo:Tolerance](Toleranz) (dp)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:TextFormat](Textformat) (op)<br />[iddo:CountryOfOrigin](Countryoforigin) (dp)<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp)<br />[iddo:hasDimension](Dimension) (op)<br />[iddo:DateOfRevision](Dateofrevision) (dp)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:ListOfPossibleValuesInLanguageN](ListofpossiblevaluesinlanguageN) (op)<br />[iddo:RevisionNumber](Revisionnumber) (dp)<br />[iddo:ExampleInLanguage](BeispielinSpracheN) (dp)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:Status](Status) (dp)<br />
In range of |[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:hasPropertyReference](hasPropertyReference) (op)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:hasConnectedProperty](Connectedproperties) (op)<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op)<br />
### Symbol des Merkmals in einer gegebenen Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolOfTheProperty`
Description | <p>Pair (symbol of the property, globally unique identifier of the group of properties (attribute GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Symbol](Symbol) (dp) **exactly** 1<br />[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op) **exactly** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
In domain of |[iddo:Symbol](Symbol) (dp)<br />
In range of |[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />
### Text format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormatItem`
Description | <p>Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:NumberOfCharacters](AnzahlderZeichen) (dp) **exactly** 1<br />[iddo:Encoding](Encoding) (dp) **exactly** 1<br />
In domain of |[iddo:NumberOfCharacters](AnzahlderZeichen) (dp)<br />[iddo:Encoding](Encoding) (dp)<br />
In range of |[iddo:TextFormat](Textformat) (op)<br />

## Object Properties
[Defining value](#Definingvalue),
[Definierende Werte](#DefinierendeWerte),
[Digital format](#Digitalformat),
[Given group of properties](#Givengroupofproperties),
[Merkmalsgruppe(n)](#Merkmalsgruppe(n)),
[List of possible values in language N](#ListofpossiblevaluesinlanguageN),
[List of replaced groups of properties](#Listofreplacedgroupsofproperties),
[Liste ersetzter Merkmale](#ListeersetzterMerkmale),
[Liste ersetzender Merkmalsgruppen](#ListeersetzenderMerkmalsgruppen),
[Liste ersetzender Merkmale](#ListeersetzenderMerkmale),
[Parameter des dynamischen Merkmals](#ParameterdesdynamischenMerkmals),
[uebergeordnete Merkmalsgruppe](#uebergeordneteMerkmalsgruppe),
[Relations of the group of properties identifiers in the interconnected data dictionaries](#Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries),
[Symbols of the property in a given property group](#Symbolsofthepropertyinagivenpropertygroup),
[Text format](#Textformat),
[Unit](#Unit),
[Grenzwerte](#Grenzwerte),
[Boundary value](#Boundaryvalue),
[Connected properties](#Connectedproperties),
[hat den Verweis auf ein Referenzdokument](#hatdenVerweisaufeinReferenzdokument),
[hat Teilmenge eines Katalogs](#hatTeilmengeeinesKatalogs),
[Dimension](#Dimension),
[has external dictionary](#hasexternaldictionary),
[has external dictionary property](#hasexternaldictionaryproperty),
[hat externe Dictionary Referenz](#hatexterneDictionaryReferenz),
[has property](#hasproperty),
[has property group reference](#haspropertygroupreference),
[has Property Reference](#hasPropertyReference),
[has unit](#hasunit),
[](Definingvalue)
### Defining value
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValue`
Description | Enthaelt einen definierenden Wert eines Arrays
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
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:DefiningValuesList](Definingvalueslist) (c)<br />
[](Digitalformat)
### Digital format
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormat`
Description | Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
[](Givengroupofproperties)
### Given group of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GivenGroupsOfProperties`
Description | Global eindeutiger Bezeichner einer Merkmalsgruppe (Attribut GA001) fuer das dem Merkmal zugeordnetem Symbol
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Merkmalsgruppe(n))
### Merkmalsgruppe(n)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupsOfProperties`
Description | Liste von global eindeutigen Bezeichnern von Merkmalsgruppen (Attribut GA001), denen das Merkmal angehoert
Usage Note | PA021
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](ListofpossiblevaluesinlanguageN)
### List of possible values in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfPossibleValuesInLanguageN`
Description | Liste von Paaren (moeglicher Wert fuer das Merkmal und Sprache) Werte koennen String oder Zahlen sein
Usage Note | PA039
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />
[](Listofreplacedgroupsofproperties)
### List of replaced groups of properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacedGroupsOfProperties`
Description | Liste von globalen Bezeichnern fuer die ersetzten Merk-malsgruppen
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
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
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
[](ListeersetzenderMerkmale)
### Liste ersetzender Merkmale
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ListOfReplacingProperties`
Description | Globally unique identifier (attribute PA001) of the replacing property (or properties)
Usage Note | PA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](ParameterdesdynamischenMerkmals)
### Parameter des dynamischen Merkmals
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ParametersOfTheDynamicProperty`
Description | List of GUIDS of properties which are parameters of the function for a dynamic property
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
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
Description | Liste von Paaren (inter-ner Bezeichner der Merkmalsgruppe, ent-sprechender Daten-katalog-Bezeichner) dieses Attribut sollte fuer die Kompatibilitaet zwischen bereits vorhandenen Merk-malsgruppen verwen-det werden
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Symbolsofthepropertyinagivenpropertygroup)
### Symbols of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolsOfTheProperty`
Description | Liste von Paaren (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />
[](Textformat)
### Text format
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormat`
Description | Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
[](Unit)
### Unit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Unit`
Description | Unit of measurement for the digital text type
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](Grenzwerte)
### Grenzwerte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundary`
Description | Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:BoundaryValue](Boundaryvalueslist) (c)<br />
[](Boundaryvalue)
### Boundary value
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasBoundaryLimit`
Description | Single Boundary value interval
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryValue](Boundaryvalueslist) (c)<br />
Range(s) |[iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />
[](Connectedproperties)
### Connected properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasConnectedProperty`
Description | List of the globally unique identifier of the connected properties (attribute PA001); the value of one property is related to the values of the other ones. For example, a sound absorption coefficient is given for a specific frequency, in this case sound absorption and frequency are connected properties
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](hatdenVerweisaufeinReferenzdokument)
### hat den Verweis auf ein Referenzdokument
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasDictionaryReferenceDocument`
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />
Domain(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
Range(s) |[iddo:DictionaryReferenceDocument](Referencedocument) (c)<br />
[](hatTeilmengeeinesKatalogs)
### hat Teilmenge eines Katalogs
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
Domain(s) |[iddo:Property](Property) (c)<br />
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
[](hatexterneDictionaryReferenz)
### hat externe Dictionary Referenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasExternalDictionaryReference`
Description | Liste von Paaren (interner Merk-malsbezeichner, entsprechender Datenkatalog-Bezeichner) dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden
Usage Note | PA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[iddo:ExternalDictionaryReference](ExternalDictionaryReference) (c)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasProperty`
Description | Fuegt ein Merkmal zu einem Feature of Interest (FOI) hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[iddo:AssignedProperty](Assignedproperty) (c)<br />
[](haspropertygroupreference)
### has property group reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyGroupReference`
Description | Attaches a property group reference to a iddo:ReferenceDocument
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
Domain(s) |[iddo:AssignedProperty](Assignedproperty) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](hasunit)
### has unit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasUnit`
Description | Eine Einheit zur Darstellung einer Skala, die es ermoeglicht, einen Wert zu messen es ist moeglich, dieses Attribut zu verwenden, um zu erlaeutern, dass dem Merkmal keine Einheit zugeordnet ist, indem einheitslos verwendet wird
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:BoundaryLimitMax](ObererGrenzwert) (c)<br />[iddo:BoundaryLimitMin](UntererGrenzwert) (c)<br />
Range(s) |[qudt:Unit](http://qudt.org/schema/qudt/Unit) (c)<br />

## Datatype Properties
[Kategorie der Merkmalsgruppe](#KategoriederMerkmalsgruppe),
[Country of origin](#Countryoforigin),
[Country of use](#Countryofuse),
[Creator's language](#Creator'slanguage),
[Data type](#Datatype),
[Datum der Aktivierung](#DatumderAktivierung),
[Datum der Erstellung](#DatumderErstellung),
[Datum der Deaktivierung](#DatumderDeaktivierung),
[Date of last change](#Dateoflastchange),
[Date of revision](#Dateofrevision),
[Datum der Version](#DatumderVersion),
[Definition in Sprache N](#DefinitioninSpracheN),
[Deprecation explanation](#Deprecationexplanation),
[Description in language N](#DescriptioninlanguageN),
[Dynamisches Merkmal](#DynamischesMerkmal),
[Encoding](#Encoding),
[Beispiel in Sprache N](#BeispielinSpracheN),
[Globally Unique Identifier (GUID)](#GloballyUniqueIdentifier(GUID)),
[Method of measurement](#Methodofmeasurement),
[Name in Sprache N](#NameinSpracheN),
[Name der definierenden Werte](#NamederdefinierendenWerte),
[Anzahl der Zeichen](#AnzahlderZeichen),
[Tolerance](#Tolerance),
[Revision number](#Revisionnumber),
[Status](#Status),
[Unterteilung der Verwendung](#UnterteilungderVerwendung),
[Symbol](#Symbol),
[Toleranz](#Toleranz),
[Version number](#Versionnumber),
[Bildliche Darstellung](#BildlicheDarstellung),
[has I](#hasI),
[has J](#hasJ),
[has L](#hasL),
[has M](#hasM),
[has N](#hasN),
[Physikalische Groesse](#PhysikalischeGroesse),
[has T](#hasT),
[has Theta](#hasTheta),
[](KategoriederMerkmalsgruppe)
### Kategorie der Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CategoryOfGroupOfProperties`
Description | Gibt die Kategorie der erstellten Merkmalsgruppe an
Usage Note | GA022
Example | ````Composed property`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](Countryoforigin)
### Country of origin
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfOrigin`
Description | Land, aus dem die Anforderung an dieses Merkmal/dieser Merkmalsgruppe stammt
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Countryofuse)
### Country of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfUse`
Description | Country (group of countries, continent) in which the property is relevant for the market the stakeholders operate in
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Creator'slanguage)
### Creator's language
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CreatorsLanguage`
Description | Satz, der den Grund fuer die Ab-lehnung erlaeutert, der erklaeren kann, wie Werte umzurechnen sind, damit sie dem neuen Merkmal entsprechen; diese Er-laeuterung muss in internatio-nalem Englisch (EN) geschrieben werden
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Datatype)
### Data type
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
Description | Datum, nach dem das Merkmal verwendet werden kann
Usage Note | PA04/GA04
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderErstellung)
### Datum der Erstellung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfCreation`
Description | Date of validation of the property creation request by experts
Usage Note | PA003/GA003
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderDeaktivierung)
### Datum der Deaktivierung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfDeactivation`
Description | Datum der Deaktivierung
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateoflastchange)
### Date of last change
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfLastChange`
Description | Date of validation of the last change request by experts
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofrevision)
### Date of revision
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
[](DefinitioninSpracheN)
### Definition in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefinitionInLanguage`
Description | Liste von Paaren (Definition des Merkmals/der Merkmalsgruppe, Sprache)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Deprecationexplanation)
### Deprecation explanation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DeprecationExplanation`
Description | Satz, der den Grund fuer die Ablehnung erlaeutert, der erklaeren kann, wie Werte umzurechnen sind, damit sie dem neuen Merkmal/der neuen Merkmalsgruppe entsprechen; diese Erlaeuterung muss in internationalem Englisch (EN) geschrieben werden
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
[](GloballyUniqueIdentifier(GUID))
### Globally Unique Identifier (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GloballyUniqueIdentifier`
Description | Eindeutiger Bezeichner, der mit dem in RFC 4122 beschriebenen Algorithmus erzeugt wird
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
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
Description | Die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
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
Domain(s) |[iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Revisionnumber)
### Revision number
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
Description | Status of the property during its life cycle
Usage Note | PA002/GA002
Example | ````inactive`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Property) (c)<br />
[](UnterteilungderVerwendung)
### Unterteilung der Verwendung
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
Domain(s) |[iddo:SymbolOfTheProperty](SymboldesMerkmalsineinergegebenenMerkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Toleranz)
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
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
[](PhysikalischeGroesse)
### Physikalische Groesse
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPhysicalQuantity`
Description | List of pairs (physical quantity | language) Physical quantities are expressed in International System (SI) units Non-physical quantities such as text are expressed with the value "without" This is equivalent to a measure in ISO 16739-1 and ISO 10303 Only one physical quantity can be attached to a property. This attribute is used to provide the quantity in plain text with all the needed translations
Usage Note | PA027
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
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