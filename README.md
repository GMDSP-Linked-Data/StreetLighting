StreetLighting
==============

Modelling streetlighting data for the [Greater Manchester Data Synchronisation Programme][gmdsp]

[gmdsp]: http://gmdsp.org.uk/


Contents
----------
This repository contains:


- Generic Open Refine model, along with associated XML file/graph
- Sample RDF XML & Graphs for each local authority
- Exported Open Refine projects for each local authority
- Mapping file of source datasets

To follow:

- Example/useful SPARQL queries


Streetlighting ontology
------------------------
The GMDSP Streetlighting ontology is hosted in a [dedicated GMDSP ontologies repostory][ont] 

[ont]: https://github.com/GMDSP-Linked-Data/ontologies


Data summary (12 Dec 2014)
---------------------------
From the five data sources, a total of 174,648 records were modelled.

This resulted in a total of 3,922,426 triples (facts) being published

| Dataset    | Records | Triples   |
|------------|---------|-----------|
| Manchester | 61,505  | 1,414,686 |
| Salford    | 26,912  | 566,315   |
| Stockport  | 33,327  | 733,166   |
| Tameside   | 26,042  | 625,028   |
| Trafford   | 26,862  | 583,231   |
| TOTALS     | 174,648 | 3,922,426 |

Live data
----------
Production data can be found at the GMDSP [QuadStore][quad]

[quad]: http://data.gmdsp.org.uk/themes


SPARQL endpoint
---------------
The GMDSP [SPARQL endpoint][sp] can be used to query the production datasets.

[sp]: http://data.gmdsp.org.uk/sparql
