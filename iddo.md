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
[Boundary values list](#Boundaryvalueslist),
[Data dictionary](#Datadictionary),
[Definierender Wert-Item](#DefinierenderWert-Item),
[Dictionary subset](#Dictionarysubset),
[Digital format item](#Digitalformatitem),
[Grenzwerte](#Grenzwerte),
[Liste definierender Werte](#ListedefinierenderWerte),
[Merkmal](#Merkmal),
[Merkmalsgruppe](#Merkmalsgruppe),
[Possible value in language N](#PossiblevalueinlanguageN),
[Reference document](#Referencedocument),
[Relation of propertiy identifier in the interconnected data dictionaries](#Relationofpropertiyidentifierintheinterconnecteddatadictionaries),
[Relation of the group of properties identifier in the interconnected data dictionaries](#Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries),
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
### Boundary values list
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValuesList`
Description | <p>Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Unit](Unit) (op) **exactly** 1<br />[iddo:BoundaryValue](Boundaryvalue) (op) **min** 1 [iddo:BoundaryValueItem](Grenzwerte) (c)<br />
In domain of |[iddo:BoundaryValue](Boundaryvalue) (op)<br />
In range of |[iddo:BoundaryValues](Boundaryvalues) (op)<br />
### Definierender Wert-Item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefiningValueItem`
Description | <p>Enthaelt einen definierenden Wert eines Arrays in Form eines Literals</p>
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
In range of |[iddo:DefiningValues](Definingvalues) (op)<br />
### Data dictionary
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Dictionary`
Description | <p>Centralized repository of information about data such as meaning, relationships to other data, origin, usage and format</p>
Super-classes |[dcat:Catalog](http://www.w3.org/ns/dcat#Catalog) (c)<br />
Restrictions |[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[dc:issued](http://purl.org/dc/terms/issued) **exactly** 1<br />[dc:publisher](http://purl.org/dc/terms/publisher) **exactly** 1<br />[dc:type](http://purl.org/dc/terms/type) **exactly** 1<br />[iddo:hasDictionarySubset](hasdictionarysubset) (op) **min** 1<br />[dc:identifier](http://purl.org/dc/terms/identifier) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />
In domain of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Reference document
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
Description | <p>Defines a subset or subgrouping of a data catalog</p>
Super-classes |[dcat:Dataset](http://www.w3.org/ns/dcat#Dataset) (c)<br />
Restrictions |[dc:description](http://purl.org/dc/terms/description) **exactly** 1<br />[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op) **exactly** 1<br />[dc:title](http://purl.org/dc/terms/title) **exactly** 1<br />[dcat:accessURL](http://www.w3.org/ns/dcat#accessURL) (ap) **exactly** 1<br />
In domain of |[iddo:hasDictionaryReferenceDocument](hasrelationtoareferencedocument) (op)<br />
In range of |[iddo:hasDictionarySubset](hasdictionarysubset) (op)<br />
### Digital format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormatItem`
Description | <p>Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Precision](Toleranz) (dp) **exactly** 1<br />[iddo:Unit](Unit) (op) **exactly** 1<br />
In domain of |[iddo:Unit](Unit) (op)<br />[iddo:Precision](Toleranz) (dp)<br />
In range of |[iddo:DigitalFormat](DigitalesFormat) (op)<br />
### Merkmalsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GroupOfProperties`
Description | <p>Sammlung, die es ermoeglicht, die Merkmale vorauszuplanen oder zu organisieren</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:ParentGroupOfProperties](Parentgroupofproperties) (op) **max** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **max** 1<br />[iddo:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp) **exactly** 1<br />[iddo:ParentGroupOfProperties](Parentgroupofproperties) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 1<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **min** 0<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[iddo:Dimension](Dimension) (dp) **min** 0<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op) **min** 0 [iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op) **min** 0 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
In domain of |[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:DateOfCreation](Dateofcreation) (dp)<br />[iddo:DateOfActivation](Dateofactivation) (dp)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:CategoryOfGroupOfProperties](KategoriederMerkmalsgruppe) (dp)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp)<br />[iddo:VersionNumber](Versionsnummer) (dp)<br />[iddo:ParentGroupOfProperties](Parentgroupofproperties) (op)<br />[iddo:Status](Status) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />
In range of |[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:ListOfReplacedGroupsOfProperties](ListeersetzterMerkmalsgruppen) (op)<br />[iddo:ParentGroupOfProperties](Parentgroupofproperties) (op)<br />[iddo:hasPropertyGroupReference](haspropertygroupreference) (op)<br />
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
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[iddo:TextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](Textformatitem) (c)<br />[iddo:CountryOfUse](Countryofuse) (dp) **min** 1<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **min** 0<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp) **min** 1<br />[iddo:Dimension](Dimension) (dp) **max** 1<br />[iddo:ConnectedProperties](Connectedproperties) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op) **min** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp) **max** 1<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **max** 1<br />[iddo:DateOfActivation](Dateofactivation) (dp) **min** 0<br />[iddo:DynamicProperty](DynamicProperty) (dp) **exactly** 1<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp) **exactly** 1<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp) **min** 0<br />[iddo:PhysicalQuantity](PhysikalischeGroesse) (dp) **min** 1<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossiblevalueinlanguageN) (c)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp) **min** 0<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:DefiningValues](Definingvalues) (op) **min** 0 [iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op) **min** 0 [iddo:RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries](Relationofpropertiyidentifierintheinterconnecteddatadictionaries) (c)<br />[iddo:MethodOfMeasurement](Messverfahren) (dp) **min** 0<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:Dimension](Dimension) (dp) **min** 0<br />[iddo:NameOfTheDefiningValues](NamederdefinierendenWerte) (dp) **min** 0<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **min** 0<br />[iddo:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[iddo:BoundaryValues](Boundaryvalues) (op) **exactly** 1 [iddo:BoundaryValuesList](Boundaryvalueslist) (c)<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp) **min** 0<br />[iddo:DigitalFormat](DigitalesFormat) (op) **min** 0 [iddo:DigitalFormatItem](Digitalformatitem) (c)<br />[iddo:SymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op) **min** 0 [iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:ExampleInLanguage](ExampleinlanguageN) (dp) **min** 0<br />[iddo:DataType](Datentyp(GUID)) (dp) **exactly** 1<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp) **exactly** 1<br />[iddo:Units](Units) (op) **min** 0<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:DateOfVersion](DatumderVersion) (dp) **exactly** 1<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />
In domain of |[iddo:CountryOfUse](Countryofuse) (dp)<br />[iddo:DefiningValues](Definingvalues) (op)<br />[iddo:VisualRepresentation](BildlicheDarstellung) (dp)<br />[iddo:DigitalFormat](DigitalesFormat) (op)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:MethodOfMeasurement](Messverfahren) (dp)<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp)<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op)<br />[iddo:PhysicalQuantity](PhysikalischeGroesse) (dp)<br />[iddo:DescriptionInLanguage](DescriptioninlanguageN) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:DateOfCreation](Dateofcreation) (dp)<br />[iddo:DateOfActivation](Dateofactivation) (dp)<br />[iddo:DateOfVersion](DatumderVersion) (dp)<br />[iddo:DataType](Datentyp(GUID)) (dp)<br />[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:TextFormat](Textformat) (op)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:Dimension](Dimension) (dp)<br />[iddo:DateOfDeactivation](Dateofdeactivation) (dp)<br />[iddo:BoundaryValues](Boundaryvalues) (op)<br />[iddo:DateOfRevision](DatumderUeberarbeitung) (dp)<br />[iddo:VersionNumber](Versionsnummer) (dp)<br />[iddo:Units](Units) (op)<br />[iddo:Status](Status) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp)<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />[iddo:RevisionNumber](Nummerderueberarbeitung) (dp)<br />[iddo:Tolerance](Tolerance) (dp)<br />[iddo:ExampleInLanguage](ExampleinlanguageN) (dp)<br />[iddo:DefinitionInLanguage](DefinitioninSpracheN) (dp)<br />[iddo:ConnectedProperties](Connectedproperties) (op)<br />[iddo:CountryOfOrigin](Ursprungsland) (dp)<br />[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:SymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />
In range of |[iddo:hasPropertyReference](hatMerkmalreferenz) (op)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op)<br />[iddo:ListOfReplacingProperties](ListeersetzenderMerkmale) (op)<br />[iddo:ConnectedProperties](Connectedproperties) (op)<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />
### Relation of propertiy identifier in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries`
Description | <p>Paar (interner Merkmalsbezeichner, entsprechender Datenkatalog-Bezeichner) Dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden</p>
Usage Note | PA014
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp) **exactly** 1<br />
In domain of |[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp)<br />
### Relation of the group of properties identifier in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | <p>Paar (interner Bezeichner der Merkmalsgruppe, entsprechender Datenkatalog-Bezeichner) dieses Attribut sollte fuer die Kompatibilitaet zwischen bereits vorhandenen Merkmalsgruppen verwendet werden</p>
Usage Note | GA014
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GloballyUniqueIdentifier(GUID)) (dp) **exactly** 1<br />[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp) **exactly** 1<br />
In domain of |[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp)<br />
In range of |[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op)<br />
### Symbol of the property in a given property group
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolOfTheProperty`
Description | <p>Paar (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GivenGroupsOfProperties](GegebeneMerkmalsgruppe) (op) **exactly** 1 [iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Symbol](Symbol) (dp) **exactly** 1<br />
In domain of |[iddo:Symbol](Symbol) (dp)<br />
In range of |[iddo:SymbolsOfTheProperty](SymboledesMerkmalsineinergegebenenMerk-malsgruppe) (op)<br />
### Text format item
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormatItem`
Description | <p>Paar fuer den Texttyp (Verschluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Encoding](Encoding) (dp) **exactly** 1<br />[iddo:NumberOfCharacters](AnzahlderZeichen) (dp) **exactly** 1<br />
In domain of |[iddo:NumberOfCharacters](AnzahlderZeichen) (dp)<br />[iddo:Encoding](Encoding) (dp)<br />
In range of |[iddo:TextFormat](Textformat) (op)<br />

## Object Properties
[Boundary value](#Boundaryvalue),
[Boundary values](#Boundaryvalues),
[Connected properties](#Connectedproperties),
[Defining value](#Definingvalue),
[Defining values](#Definingvalues),
[Digitales Format](#DigitalesFormat),
[Gegebene Merkmalsgruppe](#GegebeneMerkmalsgruppe),
[Merkmalsgruppe(n)](#Merkmalsgruppe(n)),
[Liste moeglicher Werte in Sprache N](#ListemoeglicherWerteinSpracheN),
[Liste ersetzter Merkmalsgruppen](#ListeersetzterMerkmalsgruppen),
[List of replaced properties](#Listofreplacedproperties),
[List of replacing groups of properties](#Listofreplacinggroupsofproperties),
[Liste ersetzender Merkmale](#ListeersetzenderMerkmale),
[Parameters of the dynamic property](#Parametersofthedynamicproperty),
[Parent group of properties](#Parentgroupofproperties),
[Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen](#BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen),
[Relations of the property identifiers in the interconnected data dictionaries](#Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries),
[Symbole des Merkmals in einer gegebenen Merk-malsgruppe](#SymboledesMerkmalsineinergegebenenMerk-malsgruppe),
[Textformat](#Textformat),
[Unit](#Unit),
[Units](#Units),
[has relation to a reference document](#hasrelationtoareferencedocument),
[has dictionary subset](#hasdictionarysubset),
[has property](#hasproperty),
[has property group reference](#haspropertygroupreference),
[hat Merkmalreferenz](#hatMerkmalreferenz),
[](Boundaryvalue)
### Boundary value
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValue`
Description | Single Boundary value interval
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryValuesList](Boundaryvalueslist) (c)<br />
Range(s) |[iddo:BoundaryValueItem](Grenzwerte) (c)<br />
[](Boundaryvalues)
### Boundary values
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#BoundaryValues`
Description | Pair (list of boundary intervals of possible values for the property, unit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:BoundaryValuesList](Boundaryvalueslist) (c)<br />
[](Connectedproperties)
### Connected properties
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#ConnectedProperties`
Description | List of the globally unique identifier of the connected properties (attribute PA001); the value of one property is related to the values of the other ones. For example, a sound absorption coefficient is given for a specific frequency, in this case sound absorption and frequency are connected properties
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
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
[](DigitalesFormat)
### Digitales Format
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DigitalFormat`
Description | Pair for digital text type (precision, unit) Precision is the number of significant digits
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
Description | List of globally unique identifiers of groups of properties (attribute GA001) to which the property is attached
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
Description | Global eindeutiger Bezeichner des ersetzten Merkmals (oder der Merkmale)
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
Description | global eindeutiger Bezeichner (Attribut PA001) des ersetzenden Merkmals (oder der Merkmale)
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
Description | Liste von Paaren (interner Merk-malsbezeichner, entsprechender Datenkatalog-Bezeichner) dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden
Usage Note | PA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />
[](SymboledesMerkmalsineinergegebenenMerk-malsgruppe)
### Symbole des Merkmals in einer gegebenen Merk-malsgruppe
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#SymbolsOfTheProperty`
Description | Liste von Paaren (Symbol des Merkmals, global eindeutiger Bezeichner der Merkmalsgruppe (Attribut GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />
[](Textformat)
### Textformat
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#TextFormat`
Description | Pair for text type (encoding, number of characters) The encoding is set according to Name of encoding standard of IANA, RFC 2978
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:TextFormatItem](Textformatitem) (c)<br />
[](Unit)
### Unit
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Unit`
Description | Unit of measurement for the digital text type
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](Units)
### Units
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#Units`
Description | A unit to represent a scale that enables a value to be measured It is possible to use this attribute to explain there is no unit attached to the property by using unitless
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
Description | Attaches a property group reference to a iddo:ReferenceDocument
Super-properties |[dcat:distribution](http://www.w3.org/ns/dcat#distribution)<br />[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:ReferenceDocument](https://w3id.org/iddo/v2#ReferenceDocument) (c)<br />
Range(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
[Erlaeuterung fuer die Ablehnung](#ErlaeuterungfuerdieAblehnung),
[Datentyp (GUID)](#Datentyp(GUID)),
[Date of activation](#Dateofactivation),
[Date of creation](#Dateofcreation),
[Date of deactivation](#Dateofdeactivation),
[Date of last change](#Dateoflastchange),
[Datum der Ueberarbeitung](#DatumderUeberarbeitung),
[Datum der Version](#DatumderVersion),
[Definition in Sprache N](#DefinitioninSpracheN),
[Erlaeuterung fuer die Ablehnung](#DeprecationExplanation),
[Description in language N](#DescriptioninlanguageN),
[Dimension](#Dimension),
[Dynamic Property](#DynamicProperty),
[Encoding](#Encoding),
[Example in language N](#ExampleinlanguageN),
[Globally Unique Identifier (GUID)](#GloballyUniqueIdentifier(GUID)),
[Interconnected Data Dictionary ID](#InterconnectedDataDictionaryID),
[Messverfahren](#Messverfahren),
[Name in Sprache N](#NameinSpracheN),
[Name der definierenden Werte](#NamederdefinierendenWerte),
[Anzahl der Zeichen](#AnzahlderZeichen),
[Physikalische Groesse](#PhysikalischeGroesse),
[Toleranz](#Toleranz),
[Nummer der ueberarbeitung](#Nummerderueberarbeitung),
[Status](#Status),
[Subdivision of use](#Subdivisionofuse),
[Symbol](#Symbol),
[Tolerance](#Tolerance),
[Versionsnummer](#Versionsnummer),
[Bildliche Darstellung](#BildlicheDarstellung),
[](KategoriederMerkmalsgruppe)
### Kategorie der Merkmalsgruppe
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
Description | Country from where the requirement for this property/group of properties originated
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Countryofuse)
### Country of use
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CountryOfUse`
Description | Country (group of countries, continent) in which the property is relevant for the market the stakeholders operate in
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ErlaeuterungfuerdieAblehnung)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#CreatorsLanguage`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property; this explanation has to be written in international English (EN)
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Description | Datum, nach dem das Merkmal verwendet werden kann
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
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofdeactivation)
### Date of deactivation
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfDeactivation`
Description | Date of deactivation
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateoflastchange)
### Date of last change
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfLastChange`
Description | Date of validation of the last change request by experts
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderUeberarbeitung)
### Datum der Ueberarbeitung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfRevision`
Description | Date of revision
Usage Note | PA006/GA006
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderVersion)
### Datum der Version
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DateOfVersion`
Description | Date of version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DefinitioninSpracheN)
### Definition in Sprache N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DefinitionInLanguage`
Description | List of pairs (definition of the property/group of properties, language)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DeprecationExplanation)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DeprecationExplanation`
Description | Satz, der den Grund fuer die Ablehnung erlaeutert, der erklaeren kann, wie Werte umzurechnen sind, damit sie dem neuen Merkmal/der neuen Merkmalsgruppe entsprechen; diese Erlaeuterung muss in internationalem Englisch (EN) geschrieben werden
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](DescriptioninlanguageN)
### Description in language N
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#DescriptionInLanguage`
Description | Liste von Paaren (Beschreibung des Merkmals, Sprache)
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
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](GloballyUniqueIdentifier(GUID))
### Globally Unique Identifier (GUID)
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#GloballyUniqueIdentifier`
Description | Eindeutiger Bezeichner, der mit dem in RFC 4122 beschriebenen Algorithmus erzeugt wird
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](InterconnectedDataDictionaryID)
### Interconnected Data Dictionary ID
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#InterConDictID`
Description | Corresponding data dictionary identifier
Usage Note | PA014
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries](Relationofpropertiyidentifierintheinterconnecteddatadictionaries) (c)<br />[iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Messverfahren)
### Messverfahren
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#MethodOfMeasurement`
Description | Evaluation of construction products to ensure their fitness according to requirements in harmonised technical specifications
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
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
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
[](PhysikalischeGroesse)
### Physikalische Groesse
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#PhysicalQuantity`
Description | Liste von Paaren (physikalische Groesse | Sprache) Physikalische Groessen werden in Einheiten des Internationalen Einheitensystems (SI) angegeben nicht physikalische Groessen wie z. B. Text werden mit dem Wert "ohne" angegeben dies ist gleichbedeutend mit einem Mass in ISO 16739-1 und ISO 10303 nur eine physikalische Groesse kann einem Merkmal zugeordnet werden. Dieses Attribut wird ver-wendet, um die Groesse in Klartext mit allen benoetigten ueberset-zungen bereitzustellen.
Usage Note | PA027
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[rdf:langString](http://www.w3.org/1999/02/22-rdf-syntax-ns#langString) (c)<br />
[](Toleranz)
### Toleranz
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
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />
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
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](BildlicheDarstellung)
### Bildliche Darstellung
Property | Value
--- | ---
IRI | `https://w3id.org/iddo/v2#VisualRepresentation`
Description | Visual representation of the group of properties through sketches, photos, videos or other multimedia objects
Usage Note | PA023/GA018
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Merkmalsgruppe) (c)<br />[iddo:Property](Merkmal) (c)<br />
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
[Dataset_1](#Dataset_1),
[Dictionary_1](#Dictionary_1),
[Group of properties example 1](#Groupofpropertiesexample1),
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
### Group of properties example 1 <sup>c</sup>
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
Description | Repraesentiert die Validierung mit Hilfe von SHACL der Zweisung eines Merkmals und einer Merkmalszustandes an ein Feature of Interest (FOI)
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