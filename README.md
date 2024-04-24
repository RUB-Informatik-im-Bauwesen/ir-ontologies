# Harmonization project for LOIN, Data Templates, and Properties on an ontological basis

* **Contributors**
  * [Liu Liu](https://orcid.org/0000-0001-5907-7609)
    [[ORCID]](https://orcid.org/0000-0001-5907-7609)
    (<liu.liu-m6r@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/liu_liu.html.en)
  * [Marthina Mellenthin-Filardo](https://orcid.org/0000-0001-7759-7579)
    [[ORCID]](https://orcid.org/0000-0001-7759-7579)
    (<martina.mellenthin.filardo@uni-weimar.de></a>) of [Bauhaus-Universitaet Weimar](https://www.uni-weimar.de/en/civil-engineering/chairs/construction-engineering-and-management/people/martina-mellenthin-filardo-msc/)
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
  * [Sven Zentgraf](https://orcid.org/0000-0001-6058-7614)
    [[ORCID]](https://orcid.org/0000-0001-6058-7614)
    (<sven.zentgraf@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/sven_zentgraf.html.en)

## Table of contents
### Documentation

[ISOProps / ISO 23386 Ontology Documentation (formerly IDDO ontology)](isoprops.md)   
[LOIN / EN 17412–1 Ontology Documentation](loin.md)   
[Data Templates /ISO 23387 Ontology Documentation](dt.md)   
[Examples Documentation](loin-dt-iddo.md)   
[Evaluation of FAIR Data principles](fair-data.md)   

### Ontology data
[ISOProps / ISO 23386 Ontology (TTL)](iddo.ttl)   
[LOIN / EN 17412–1 Ontology (TTL)](loin.ttl)   
[Data Templates /ISO 23387 Ontology (TTL)](dt.ttl)   
[Example (TTL)](loin-dt-iddo.ttl)   

### Work process
After every edit execute:
```
./pylode.exe -i loin.ttl -o loin.md -f md
./pylode.exe -i iddo.ttl -o iddo.md -f md
./pylode.exe -i dt.ttl -o dt.md -f md
```
for documentation.

 
