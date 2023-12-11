# Map explorer


## Notes on exploring (OSM) maps

### PostGIS

Deploying a local copy of the OSM db:
https://wiki.openstreetmap.org/wiki/Osmosis/PostGIS_Setup

### Command line tools

* [osmium-tool](https://osmcode.org/osmium-tool/manual.html), a command line tool to manipulate OSM data
* [osmfilter](https://wiki.openstreetmap.org/wiki/Osmfilter), a command line tool to filter OSM data

### Python

* [overpassify](https://github.com/LivInTheLookingGlass/overpassify), a python library to OverpassQL transpiler
* [Cartes](https://cartes-viz.github.io/osm.html), a python library offers some facilities to request and parse the results from the OpenStreetMap Nominatim (search engine) and Overpass (map data database) API.

### Other

* [Overpass API via XML](https://wiki.openstreetmap.org/wiki/Overpass_API/Language_Guide)
* [osmdata](https://docs.ropensci.org/osmdata/reference/opq.html), R package to build Overpass querie

### ChatGPT

* [KID2 Spot Application](https://github.com/dw-innovation/kid2-spot), a natural language interface for querying OpenStreetMap data via GPT.

## Notes on subway station structure in OpenStreetMap

* A relation [public_transport=stop_area](https://wiki.openstreetmap.org/wiki/FR:Tag:public transport=stop area) corresponds to a subway station of a single line. ```name=``` corresponds to the name of the station, possibly with the name of the line in parenthesis. Example: [République (11)](https://www.openstreetmap.org/relation/7731272).
* A relation [public_transport=stop_area_group](https://wiki.openstreetmap.org/wiki/Relation:public_transport#public_transport.3Dstop_area_group) contain multiple stop areas, each of them corresponding to a single line. Its name can be different from the contained stop areas. Example: [La Chapelle](https://www.openstreetmap.org/relation/965959) vs [Gare du Nord](https://www.openstreetmap.org/relation/7938398).
* Interesting elements of a```public_transport=stop_area``` (example [La Chapelle](https://www.openstreetmap.org/relation/965959)):
    * ```railway=stop``` such as [329096792](https://www.openstreetmap.org/node/3417692500) and [329096792](https://www.openstreetmap.org/node/329096792), that are part of a relation ```type=route``` corresponding to the metro line: [4728208](https://www.openstreetmap.org/relation/4728208) and [123917](https://www.openstreetmap.org/relation/123917) (one in each direction)
    * ```railway=subway_entrance``` with a name, such as [Rue du Faubourg Saint-Denis](https://www.openstreetmap.org/node/775370144) and [Rue Marx Dormoy](https://www.openstreetmap.org/node/775370145)

