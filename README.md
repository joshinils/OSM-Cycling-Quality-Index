# OSM Cycling Quality Index
A Python script for QGIS that generates a cycling quality index from OpenStreetMap data for every way segment. The type of way, width and surface attributes, characteristics of parallel roads and a few other attributes are processed and an index value from 0 to 100 is calculated, which indicates the suitability of a way/road segment for cycle traffic.

### Included way and road properties
* Distinction of 16 way types, depending on OSM tagging (e.g. cycle tracks and different types of lanes, sidepath or non-sidepath cycle path, shared or segregated path, shared footways/roads/traffic or bus lanes, bicycle roads, crossings, links...)
* Basic geometric sidepath detection, if not tagged explicitly
* Evaluation of width attributes and surface characteristics (surface and smoothness)
* Evaluation of the road classification and maximum speed (for shared roads and side paths)
* Evaluation of separation and buffer characteristics
* Evaluation of other attributes such as lighting, adjacent parking lanes or surface colour
* Calculation of index values and factors for the mentioned property groups and derivation of a total index

### How to use this script
1. Run [Overpass-Query](https://overpass-turbo.eu/s/1G3t) for for the desired area/region to get road and way network suitable for cycling 
2. Export result as GeoJSON to 'data/way_import.geojson'
3. Run this python script in QGIS
   1. "Plugins" => "Python Console"
   1. (If internal Python Editor Panel is hidden: Right click in Console => "Show Editor")
   1. Open File in QGIS Python Editor
   1. Run from there (Note: Do _not_ use the "Browser" => File => "Run Script")

### Example visualization
An interactive demo map for Berlin can be found here: [OpenStreetMap Verkehrswende / Cycling Quality Index](https://www.osm-verkehrswende.org/cqi/map/)
![grafik](https://github.com/SupaplexOSM/OSM-Cycling-Quality-Index/assets/66696066/c13688d4-9a82-490c-bcfd-33290fd4d7b0)
