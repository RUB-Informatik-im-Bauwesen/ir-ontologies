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
1. [Named Individuals](#namedindividuals)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[Assigned property](#Assignedproperty),
[Data dictionary](#Datadictionary),
[Definierender Wert-Item](#DefinierenderWert-Item),
[Defining values list](#Definingvalueslist),
[Dictionary subset](#Dictionarysubset),
[Digitales Format-Item](#DigitalesFormat-Item),
[Grenzwerte](#BoundaryValueItem),
[Grenzwertliste](#Grenzwertliste),
[Merkmalsgruppe](#Merkmalsgruppe),
[Possible value in language N](#PossiblevalueinlanguageN),
[Property](#Property),
[Reference document](#Referencedocument),
[Relation of propertiy identifier in the interconnected data dictionaries](#Relationofpropertiyidentifierintheinterconnecteddatadictionaries),
[Relation of the group of properties identifier in the interconnected data dictionaries](#Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries),
[Symbol of the property in a given property group](#Symbolofthepropertyinagivenpropertygroup),
[Text format item](#Textformatitem),
### Assigned property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#AssignedProperty`
Description | <p>Represents the assignment of a property and a property state to a feature of interest (FOI).</p>
Super-classes |[http://www.w3id.org/opm#Property](http://www.w3id.org/opm#Property) (c)<br />
Restrictions |[http://www.w3id.org/opm#hasPropertyState](http://www.w3id.org/opm#hasPropertyState) **min** 1<br />[iddo:hasPropertyReference](hatMerkmalreferenz) (op) **exactly** 1<br />
In domain of |[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />
In range of |[iddo:hasProperty](hasproperty) (op)<br />
### Grenzwerte
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValueItem`
Description | <p>Grenzwertintervall bestehend aus der unteren(minValue) und der oberen(maxValue) Intervallgrenze</p>
Usage Note | PA040
Super-classes |[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[sdo:minValue](https://schema.org/minValue) **exactly** 1<br />[sdo:maxValue](https://schema.org/maxValue) **exactly** 1<br />
In range of |[iddo:BoundaryValue](Grenzwert) (op)<br />
### Grenzwertliste
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValuesList`
Description | <p>Pair  (List of boundary intervals of possible values for the property, unit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Unit](Unit) (op) **exactly** 1<br />[iddo:BoundaryValue](Grenzwert) (op) **min** 1 [iddo:BoundaryValueItem](BoundaryValueItem) (c)<br />
In domain of |[iddo:BoundaryValue](Grenzwert) (op)<br />
In range of |[iddo:BoundaryValues](Grenzwerte) (op)<br />
### Definierender Wert-Item
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
Description | <p>Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DefiningValueItem](DefinierenderWert-Item) **min** 1<br />
In domain of |[iddo:DefiningValue](Definingvalue) (op)<br />
In range of |[iddo:DefiningValues](DefinierendeWerte) (op)<br />
### Data dictionary
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dictionary`
Description | <p>Centralized repository of information about data such as meaning, relationships to other data, origin, usage and format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op) **min** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />
In domain of |[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Reference document
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionaryReferenceDocument`
Description | <p>Publikation, die hinzugezogen wird, um bestimmte Informationen zu finden, insbesondere in einer technischen oder wissenschaftlichen Domaene</p>
Super-classes |[dcat:Distribution](http://www.w3.org/ns/dcat#Distribution) (c)<br />
Restrictions |[iddo:hasPropertyGroupReference](haspropertygroupreference) (op) **exactly** 1<br />
In range of |[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
### Dictionary subset
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DictionarySubset`
Description | <p>Definiert eine Teilmenge oder Untergruppierung eines Datenkatalogs</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op) **exactly** 1<br />
In domain of |[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
In range of |[iddo:hasDictionarySubset](hatTeilmengeeinesKatalogs) (op)<br />
### Digitales Format-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormatItem`
Description | <p>Pair for digital text type (precision, unit) Precision is the number of significant digits</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Unit](Unit) (op) **exactly** 1<br />[iddo:Precision](Tolerance) (dp) **exactly** 1<br />
In domain of |[iddo:Precision](Tolerance) (dp)<br />[iddo:Unit](Unit) (op)<br />
In range of |[iddo:DigitalFormat](DigitalesFormat) (op)<br />
### Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupOfProperties`
Description | <p>Collection enabling the properties to be prearranged or organized</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Tolerance](Toleranz) (dp) **min** 0<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:Dimension](Dimension) (dp) **min** 0<br />[iddo:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **exactly** 1<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **max** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **max** 1<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries) (op) **min** 0 [iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 1<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **min** 0<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp) **exactly** 1<br />[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DateOfVersion](Dateofversion) (dp) **exactly** 1<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp) **min** 0<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:DateOfActivation](Dateofactivation) (dp) **min** 0<br />
In domain of |[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp)<br />[iddo:NameInLanguage](NameinlanguageN) (dp)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:Status](Status) (dp)<br />[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:DateOfVersion](Dateofversion) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:DateOfActivation](Dateofactivation) (dp)<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp)<br />
In range of |[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op)<br />[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:hasPropertyGroupReference](haspropertygroupreference) (op)<br />
### Possible value in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PossibleValueInLanguageN`
Description | <p>Possible value for the property and language Values can be string or numbers</p>
Usage Note | PA039
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:ListOfPossibleValuesInLanguageN](ListofpossiblevaluesinlanguageN) (op)<br />
### Property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Property`
Description | <p>Inhaerente oder erworbene Eigenschaft eines Datenelements</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:ListOfPossibleValuesInLanguageN](ListofpossiblevaluesinlanguageN) (op) **min** 0<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:BoundaryValues](Grenzwerte) (op) **exactly** 1 [iddo:BoundaryValuesList](Grenzwertliste) (c)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 0<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **max** 1<br />[iddo:Tolerance](Toleranz) (dp) **min** 0<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:NameInLanguage](NameinlanguageN) (dp) **min** 1<br />[iddo:DefiningValues](DefinierendeWerte) (op) **min** 0 [iddo:DefiningValuesList](Definingvalueslist) (c)<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **min** 0<br />[iddo:ExampleInLanguage](BeispielinSpracheN) (dp) **min** 0<br />[iddo:NameOfTheDefiningValues](Namesofthedefiningvalues) (dp) **min** 0<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp) **min** 0<br />[iddo:MethodOfMeasurement](Messverfahren) (dp) **min** 0<br />[iddo:Units](Einheiten) (op) **min** 0<br />[iddo:ConnectedProperties](Connectedproperties) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:DateOfCreation](DatumderErstellung) (dp) **exactly** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **min** 0<br />[iddo:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp) **min** 0<br />[iddo:Dimension](Dimension) (dp) **min** 0<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **max** 1<br />[iddo:DigitalFormat](DigitalesFormat) (op) **min** 0 [iddo:DigitalFormatItem](DigitalesFormat-Item) (c)<br />[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op) **min** 0 [iddo:RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries](Relationofpropertiyidentifierintheinterconnecteddatadictionaries) (c)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:DateOfVersion](Dateofversion) (dp) **exactly** 1<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op) **min** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DataType](Datatype) (dp) **exactly** 1<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op) **min** 0 [iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />[iddo:VersionNumber](Versionnumber) (dp) **exactly** 1<br />[iddo:TextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](Textformatitem) (c)<br />[iddo:DynamicProperty](DynamischesMerkmal) (dp) **exactly** 1<br />[iddo:PhysicalQuantity](PhysikalischeGroesse) (dp) **min** 1<br />[iddo:ListOfPossibleValuesInLanguageN](ListofpossiblevaluesinlanguageN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op) **min** 0 [iddo:Property](Property) (c)<br />[iddo:Dimension](Dimension) (dp) **max** 1<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />
In domain of |[iddo:PhysicalQuantity](PhysikalischeGroesse) (dp)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />[iddo:ExampleInLanguage](BeispielinSpracheN) (dp)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:NameInLanguage](NameinlanguageN) (dp)<br />[iddo:SubdivisionOfUse](UnterteilungderVerwendung) (dp)<br />[iddo:ConnectedProperties](Connectedproperties) (op)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:Status](Status) (dp)<br />[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:DataType](Datatype) (dp)<br />[iddo:BoundaryValues](Grenzwerte) (op)<br />[iddo:DateOfVersion](Dateofversion) (dp)<br />[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op)<br />[iddo:ListOfPossibleValuesInLanguageN](ListofpossiblevaluesinlanguageN) (op)<br />[iddo:Units](Einheiten) (op)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp)<br />[iddo:DateOfCreation](DatumderErstellung) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op)<br />[iddo:DefiningValues](DefinierendeWerte) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:Tolerance](Toleranz) (dp)<br />[iddo:Dimension](Dimension) (dp)<br />[iddo:TextFormat](Textformat) (op)<br />[iddo:VersionNumber](Versionnumber) (dp)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:DigitalFormat](DigitalesFormat) (op)<br />[iddo:DateOfActivation](Dateofactivation) (dp)<br />[iddo:MethodOfMeasurement](Messverfahren) (dp)<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp)<br />
In range of |[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />[iddo:ListOfReplacedProperties](ListeersetzterMerkmale) (op)<br />[iddo:ParametersOfTheDynamicProperty](ParameterdesdynamischenMerkmals) (op)<br />[iddo:ConnectedProperties](Connectedproperties) (op)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />
### Relation of propertiy identifier in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries`
Description | <p>Paar (interner Merkmalsbezeichner, entsprechender Datenkatalog-Bezeichner) Dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden</p>
Usage Note | PA014
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:InterConDictID](MiteinanderverbundeneDatenkatalogID) (dp) **exactly** 1<br />
In domain of |[iddo:InterConDictID](MiteinanderverbundeneDatenkatalogID) (dp)<br />
### Relation of the group of properties identifier in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | <p>Pair (group of properties internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing groups of properties</p>
Usage Note | GA014
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:InterConDictID](MiteinanderverbundeneDatenkatalogID) (dp) **exactly** 1<br />[iddo:InterConDictID](MiteinanderverbundeneDatenkatalogID) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />
In domain of |[iddo:InterConDictID](MiteinanderverbundeneDatenkatalogID) (dp)<br />
In range of |[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries) (op)<br />
### Symbol of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolOfTheProperty`
Description | <p>Paar (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op) **exactly** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Symbol](Symbol) (dp) **exactly** 1<br />
In domain of |[iddo:Symbol](Symbol) (dp)<br />
In range of |[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />
### Text format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormatItem`
Description | <p>Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:NumberOfCharacters](AnzahlderZeichen) (dp) **exactly** 1<br />[iddo:Encoding](Kodierung) (dp) **exactly** 1<br />
In domain of |[iddo:Encoding](Kodierung) (dp)<br />[iddo:NumberOfCharacters](AnzahlderZeichen) (dp)<br />
In range of |[iddo:TextFormat](Textformat) (op)<br />

## Object Properties
[Grenzwert](#Grenzwert),
[Grenzwerte](#Grenzwerte),
[Connected properties](#Connectedproperties),
[Defining value](#Definingvalue),
[Definierende Werte](#DefinierendeWerte),
[Digitales Format](#DigitalesFormat),
[Given group of properties](#Givengroupofproperties),
[Merkmalsgruppe(n)](#Merkmalsgruppe(n)),
[List of possible values in language N](#ListofpossiblevaluesinlanguageN),
[List of replaced groups of properties](#Listofreplacedgroupsofproperties),
[Liste ersetzter Merkmale](#ListeersetzterMerkmale),
[List of replacing groups of properties](#Listofreplacinggroupsofproperties),
[Liste ersetzender Merkmale](#ListeersetzenderMerkmale),
[Parameter des dynamischen Merkmals](#ParameterdesdynamischenMerkmals),
[uebergeordnete Merkmalsgruppe](#uebergeordneteMerkmalsgruppe),
[Relations of the group of properties identifiers in the interconnected data dictionaries](#Relationsofthegroupofpropertiesidentifiersintheinterconnecteddatadictionaries),
[Relations of the property identifiers in the interconnected data dictionaries](#Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries),
[Symbols of the property in a given property group](#Symbolsofthepropertyinagivenpropertygroup),
[Textformat](#Textformat),
[Unit](#Unit),
[Einheiten](#Einheiten),
[has relation to a reference document](#hasrelationtoareferencedocument),
[hat Teilmenge eines Katalogs](#hatTeilmengeeinesKatalogs),
[has property](#hasproperty),
[has property group reference](#haspropertygroupreference),
[hat Merkmalreferenz](#hatMerkmalreferenz),
[](Grenzwert)
### Grenzwert
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
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:BoundaryValuesList](Grenzwertliste) (c)<br />
[](Connectedproperties)
### Connected properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ConnectedProperties`
Description | Liste der global eindeutigen Bezeichner der verbundenen Merkmale (Attribut PA001); der Wert eines Merkmals steht zu den Werten der anderen in einer Beziehung. Beispielsweise ist ein Schallabsorptionsgrad fuer eine bestimmte Frequenz gegeben, in diesem Fall sind Schallabsorp-tionsgrad und Frequenz ver-bundene Merkmale.
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](Definingvalue)
### Defining value
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValue`
Description | Contains a defining value of an array
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DefiningValuesList](Definingvalueslist) (c)<br />
Range(s) |[iddo:DefiningValueItem](DefinierenderWert-Item) (c)<br />
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
[](DigitalesFormat)
### Digitales Format
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
Description | Globally unique identifier of a group of properties (attribute GA001) for the symbol assigned to the property.
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
Description | Globally unique identifier of the replaced property (or properties)
Usage Note | PA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
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
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](ParameterdesdynamischenMerkmals)
### Parameter des dynamischen Merkmals
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ParametersOfTheDynamicProperty`
Description | Liste von GUIDs von Merkmalen, welche Parameter der Funktion fuer ein dynamisches Merkmal sind
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />
[](uebergeordneteMerkmalsgruppe)
### uebergeordnete Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ParentGroupOfProperties`
Description | Ermoeglicht die Ver-knuepfung einer Unter-gruppe mit einer ueber-geordneten Gruppe ueber ihre global ein-deutigen Bezeichner (Attribut GA001) jedes einer Gruppe zugehoerige Merkmal wird von der/den Untergruppe(n) uebernommen
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
Range(s) |[iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />
[](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries)
### Relations of the property identifiers in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries`
Description | List of pairs (property internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing properties
Usage Note | PA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />
[](Symbolsofthepropertyinagivenpropertygroup)
### Symbols of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolsOfTheProperty`
Description | Liste von Paaren (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />
[](Textformat)
### Textformat
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
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](Einheiten)
### Einheiten
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Units`
Description | Eine Einheit zur Darstellung einer Skala, die es ermoeglicht, einen Wert zu messen es ist moeglich, dieses Attribut zu verwenden, um zu erlaeutern, dass dem Merkmal keine Einheit zugeordnet ist, indem einheitslos verwendet wird
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](hasrelationtoareferencedocument)
### has relation to a reference document
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
Domain(s) |[iddo:Dictionary](Datadictionary) (c)<br />
Range(s) |[iddo:DictionarySubset](Dictionarysubset) (c)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasProperty`
Description | Attaches a property to a feature of interest (FOI)
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[iddo:AssignedProperty](Assignedproperty) (c)<br />
[](haspropertygroupreference)
### has property group reference
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyGroupReference`
Description | Attaches a property group reference to a iddo:ReferenceDocument
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:ReferenceDocument](https://w3id.org/iddo/v2#ReferenceDocument) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
[](hatMerkmalreferenz)
### hat Merkmalreferenz
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#hasPropertyReference`
Description | Fuegt ein Merkmal zu einer Merkmalszuweisung hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:AssignedProperty](Assignedproperty) (c)<br />
Range(s) |[iddo:Property](Property) (c)<br />

## Datatype Properties
[Kategorie der Merkmalsgruppe](#KategoriederMerkmalsgruppe),
[Ursprungsland](#Ursprungsland),
[Country of use](#Countryofuse),
[Erlaeuterung fuer die Ablehnung](#ErlaeuterungfuerdieAblehnung),
[Data type](#Datatype),
[Date of activation](#Dateofactivation),
[Datum der Erstellung](#DatumderErstellung),
[Datum der Deaktivierung](#DatumderDeaktivierung),
[Date of last change](#Dateoflastchange),
[Datum der Ueberarbeitung](#DatumderUeberarbeitung),
[Date of version](#Dateofversion),
[Definition in Sprache N](#DefinitioninSpracheN),
[Erlaeuterung fuer die Ablehnung](#DeprecationExplanation),
[Description in language N](#DescriptioninlanguageN),
[Dimension](#Dimension),
[Dynamisches Merkmal](#DynamischesMerkmal),
[Kodierung](#Kodierung),
[Beispiel in Sprache N](#BeispielinSpracheN),
[Global eindeutiger Bezeichner (GUID)](#GlobaleindeutigerBezeichner(GUID)),
[Miteinander verbundene Datenkatalog ID](#MiteinanderverbundeneDatenkatalogID),
[Messverfahren](#Messverfahren),
[Name in language N](#NameinlanguageN),
[Names of the defining values](#Namesofthedefiningvalues),
[Anzahl der Zeichen](#AnzahlderZeichen),
[Physikalische Groesse](#PhysikalischeGroesse),
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
Example | ````Composed property`<br />```
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
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Countryofuse)
### Country of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfUse`
Description | Country (group of countries, continent) in which the property is relevant for the market the stakeholders operate in
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
[](Dateofactivation)
### Date of activation
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
Description | Datum der Validierung der An-frage zur Erstellung des Merkmals durch Sachverstaendige
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
Description | Datum der Validierung der letzten Aenderungsanfrage durch Sachverstaendige
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
[](Dateofversion)
### Date of version
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfVersion`
Description | Date of version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DefinitioninSpracheN)
### Definition in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefinitionInLanguage`
Description | Liste von Paaren (Definition des Merkmals/der Merkmalsgruppe, Sprache)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DeprecationExplanation)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DeprecationExplanation`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property/group of properties; this explanation has to be written in international English (EN)
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
[](Dimension)
### Dimension
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dimension`
Description | In case of a physical quantity, dimension according to ISO 80000 (all parts) This attribute allows the dimension to be machine readable; as all physical quantities are derived from 7 base quantities, it is provided with the power (as a rational number) attached to a basic dimension in the following order and with one space between each
Usage Note | PA028
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](DynamischesMerkmal)
### Dynamisches Merkmal
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DynamicProperty`
Description | Wenn es sich um ein dynamisches Merkmal handelt, haengt der Wert von den im Attribut PA032 bereitgestellten Parametern ab
Usage Note | PA031
Example | ````no`<br />```
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
[](BeispielinSpracheN)
### Beispiel in Sprache N
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
Description | Eindeutiger Bezeichner, der mit dem in RFC 4122 beschriebenen Algorithmus erzeugt wird
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](MiteinanderverbundeneDatenkatalogID)
### Miteinander verbundene Datenkatalog ID
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#InterConDictID`
Description | Corresponding data dictionary identifier
Usage Note | PA014
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />[iddo:RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries](Relationofpropertiyidentifierintheinterconnecteddatadictionaries) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Messverfahren)
### Messverfahren
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
Description | Liste von Paaren (Name des Merkmals und Sprache) Dieses Attribut kann verwendet werden, um Synonyme fuer verschiedene Domaenen hinzuzufuegen
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
[](AnzahlderZeichen)
### Anzahl der Zeichen
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#NumberOfCharacters`
Description | The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](PhysikalischeGroesse)
### Physikalische Groesse
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PhysicalQuantity`
Description | List of pairs (physical quantity | language) Physical quantities are expressed in International System (SI) units Non-physical quantities such as text are expressed with the value "without" This is equivalent to a measure in ISO 16739-1 and ISO 10303 Only one physical quantity can be attached to a property. This attribute is used to provide the quantity in plain text with all the needed translations
Usage Note | PA027
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
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
[](Nummerderueberarbeitung)
### Nummer der ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RevisionNumber`
Description | This revision number allows tracking of minor changes e.g. new translation, changes of typos: if the version number changes, the revision number starts again at 1 Experts decide if a new revision number can be applied or if a new revision is needed
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Domain(s) |[iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />
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
Description | Diese Versionsnummer ermoeglicht die Verfolgung groesserer aenderungen. Sachverstaendige entscheiden, ob eine neue Ver-sionsnummer angewendet werden muss.
Usage Note | PA009/GA009
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Property) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Description | Code, der zur Identifizierung des Attributs verwendet werden kann
Domain(s) |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Range(s) |[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#Literal) (c)<br />

## Named Individuals
[Dataset_1](#Dataset_1),
[Dictionary_1](#Dictionary_1),
[Merkmalsgruppenbeispiel 1](#Merkmalsgruppenbeispiel1),
[Property example 1](#Propertyexample1),
[ReferenceDocument_1](#ReferenceDocument_1),
[Zugewiesenes Merkmal SHACL Shape](#ZugewiesenesMerkmalSHACLShape),
### Dataset_1 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://www.example.com/property#Dataset_1`
* **Contributor(s)**
  * [iddo:DictionarySubset](https://w3id.org/iddo/v2#DictionarySubset)
### Dictionary_1 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://www.example.com/property#Dictionary_1`
* **Contributor(s)**
  * [iddo:Dictionary](https://w3id.org/iddo/v2#Dictionary)
### Merkmalsgruppenbeispiel 1 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://www.example.com/property#GroupOfProperties_1`
* **Contributor(s)**
  * [iddo:GroupOfProperties](https://w3id.org/iddo/v2#GroupOfProperties)
Description | Collection enabling the properties to be prearranged or organized
### Property example 1 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://www.example.com/property#Property_1`
* **Contributor(s)**
  * [iddo:Property](https://w3id.org/iddo/v2#Property)
### ReferenceDocument_1 <sup>c</sup>
Property | Value
--- | ---
IRI | `http://www.example.com/property#ReferenceDocument_1`
* **Contributor(s)**
  * [iddo:DictionaryReferenceDocument](https://w3id.org/iddo/v2#DictionaryReferenceDocument)
### Zugewiesenes Merkmal SHACL Shape <sup>c</sup>
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#AssignedPropertyShape`
* **Contributor(s)**
  * [sh:NodeShape](http://www.w3.org/ns/shacl#NodeShape)
Description | Represents the validation using SHACL of the assignment of a property and a property state to a feature of interest (FOI).
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