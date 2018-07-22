# choropleth-map

Creates a choropleth map from input data. You can choose from a few preset maps or provide your own GeoJSON file that specifies the shape of the map.

### For developers: Adding a preset

If you are a developer working on the Workbench source code, you can add new presets to the module for everyone to use. To add a new preset, use the following steps:

1. Find a GeoJSON file for your new preset map geometry
2. If the GeoJSON file does not have it already, add a `name` property to every feature that should indicate the location name for each map area. For example, if the GeoJSON is for US states and you expect the data to have full state names, the `name` attribute for New York should be `New York`
3. Wrap the GeoJSON object in an `export default ...;` clause and save it as a `.js` file. Put this file under the source code's `assets/js/wfparameters/choropleth/geojson` directory
4. Update the `MapLocationPresets.js` file to include your new preset (see comments there for instructions). The file is located in the `assets/js/wfparameters/choropleth` directory
5. Once the changes are merged and deployed, the job is done
