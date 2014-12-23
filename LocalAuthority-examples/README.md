Refine models
==============

Data Overview
==============
All five local authorities have provided streetlighting data.

These datasets have now been modelled to RDF in a consistent approach, and can be found on the live GDMSP datastore: http://gmdsp-staging.publishmydata.com/themes/street-lighting


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

Source data
==============
Source data for streetlighting was provided directly to GMDSP.  

This data is publically available in only two of the five local authorities:

Manchester
--------------
* Open data portal: http://open.manchester.gov.uk/
* Streetlight data: not available
* DataGM: not listed

Salford
--------------
* Open data portal: http://www.salford.gov.uk/opendata.htm
* Streetlight data: http://www.salford.gov.uk/d/StreetLights.csv (CSV file)
* DataGM: http://datagm.org.uk/dataset/salford-street-lighting

Stockport
--------------
* Open data portal: http://www.stockport.gov.uk/services/councildemocracy/yourcouncil/transparency/
* Streetlight data: not available
* DataGM: not listed

Tameside
--------------
* Open data portal: www.tameside.gov.uk/opendata
* Streetlight data: not available
* DataGM: not listed

Trafford
--------------
* Open data portal: http://www.trafford.gov.uk/about-your-council/data-protection/open-data/open-data.aspx
* Streetlight data: http://www.infotrafford.org.uk/custom/resources/streetlights_from_GIS_Lat_Lng.csv (CSV file - labelled as XML)
* DataGM: http://datagm.org.uk/dataset/trafford-council-streetlights (404 link, as XML file is not active)


Source datasets transformed using [Open Refine][or] and [RDF plugin][ordf]

[or]: http://openrefine.org/
[ordf]: http://refine.deri.ie/


Data comparison
=================
The data supplied by local authorities has been mapped against the broad structure of a "GMDSP Streetlight".  

This involves describing each Streetlight uniquely, alongside subsequent locative and specific facets.

This data is also available as a [Google spreadsheet][gss]

[gss]: https://docs.google.com/spreadsheets/d/1fWb-tCd-KUFJB5aCKsRZWjTmpmJ8VHcxbQkD7dTzMiw/edit?usp=sharing

| Subject     | Mapping                     | Manchester     | Salford                | Stockport        | Tameside             | Trafford    |   | Links to                                             |
|-------------|-----------------------------|----------------|------------------------|------------------|----------------------|-------------|---|------------------------------------------------------|
| Identifiers | (ID used)                   | OBJECTID       | id                     | central_asset_id | ID                   | ^ID2        |   |                                                      |
|             | dc:alternative              | UNITNO         | Feature ID             |                  |                      |             |   |                                                      |
|             |                             |                |                        |                  |                      |             |   |                                                      |
| Location    | rdfs:label                  | *Address label | *Address label         | *address label   | *Full address        | DESCRIPTION |   |                                                      |
|             |                             |                |                        |                  |                      |             |   |                                                      |
| Address     | gmdsp:hasPlotNumber         | UNITNO         |                        | plot_number      | Unit No.             | TITLE       |   |                                                      |
|             | gmdsp:hasSiteCode           |                |                        | site_code        |                      |             |   |                                                      |
|             | locn:thoroughfare           | STREET         | RoadName               | site_name        | Address 1            | STREET_NAME |   |                                                      |
|             | dcterms:description         | LOCATION       |                        |                  |                      | DESCRIPTION |   |                                                      |
|             | locn:addressArea            |                | Town                   |                  | Address 2            |             |   | g50k:NamedPlace                                      |
|             | admingeo:ward               |                | Ward                   |                  |                      |             |   | admingeo:MetropolitanDistrictWard                    |
|             | skos:notaion                |                |                        |                  |                      | USRN        |   |                                                      |
|             |                             |                |                        |                  |                      |             |   |                                                      |
| Geometry    | osspr:easting               | EASTING        | Easting                | feat_cent_east   | Easting              | EASTING     |   |                                                      |
|             | osspr:northing              | NORTHING       | Northing               | feat_cent_north  | Northing             | NORTHING    |   |                                                      |
|             | geo:lat                     |                |                        | lat              | Lats                 | Latitude    |   |                                                      |
|             | geo:long                    |                |                        | long             | Long                 | Longitude   |   |                                                      |
|             |                             |                |                        |                  |                      |             |   |                                                      |
| Streetlight | gmdsp:lampType              | UNITTYPE       | Lamp Type              |                  | LT - LAMP TYPE       |             |   | gmdsp.org.uk/def/streetlighting/lamp-type            |
|             | gmdsp:columnType            |                |                        | Type             | CT- COLUMN TYPE      |             |   | gmdsp.org.uk/def/streetlighting/column-type          |
|             | gmdsp:columnHeight          | COLHEIGHT      | Mounting Height        |                  | MH - MOUNTING HEIGHT |             |   |                                                      |
|             | gmdsp:eligibleSupply        | ELIGIBLE       | Eligible Supply        |                  |                      |             |   |                                                      |
|             | gmdsp:wattage               | LAMPWATTS      | Lamp Wattage           |                  | LW - LAMP WATTS      |             |   |                                                      |
|             | gmdsp:dimmingClassification |                | Dimming Classification |                  |                      |             |   |                                                      |
|             | gmdsp:condition             |                | Condition              |                  |                      |             |   | gmdsp.org.uk/def/streetlighting/condition            |
|             | gmdsp:lanternManufacturer   |                | Lantern Manufacturer   |                  |                      |             |   | gmdsp.org.uk/def/streetlighting/lantern-manufacturer |
|             | gmdsp:columnManufacturer    |                | Column Manufacturer    |                  |                      |             |   | gmdsp.org.uk/def/streetlighting/column-manufacturer  |
|             | gmdsp:serviceRoute          |                |                        |                  |                      | ROUTE       |   |                                                      |
|             | dcterms:description         |                | Asset Type             |                  |                      |             |   |                                                      |
|             | skos:notaion                |                |                        | central_asset_id |                      |             |   |                                                      |

^generated from OBJECT_NUMBER
**Concatenations of existing fields






