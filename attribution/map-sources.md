# Offline overview map

`world-land.geojson` is Natural Earth 1:110 million land geometry, obtained from the project's [official vector repository](https://github.com/nvkelso/natural-earth-vector/blob/master/geojson/ne_110m_land.geojson).

Natural Earth data is public domain. See the project's [licence statement](https://github.com/nvkelso/natural-earth-vector/blob/master/LICENSE.md).

This generalized world layer is an orientation reference. It is not a nautical chart, bathymetric survey or navigation product. No precise organism locations are derived from it.

# Detailed basemap / offline packs

The optional online source is [OpenFreeMap](https://openfreemap.org/), serving OpenMapTiles-compatible vector data. BioSync renders it with its own native Qt style. Required attribution remains visible in the map and in saved MBTiles metadata: OpenFreeMap, © OpenMapTiles and © OpenStreetMap contributors. See [OpenStreetMap copyright and ODbL](https://www.openstreetmap.org/copyright). OpenFreeMap's published offline limits are respected with a 3,000-tile / 50 MB limit and fewer than four simultaneous requests.

Public OpenStreetMap raster servers are not bulk downloaded; see the [OSMF tile policy](https://operations.osmfoundation.org/policies/tiles/). Custom imagery must have the operator's own authorization and attribution. No third-party map fonts, sprites, or browser renderer are bundled.
