GeoData Formats
===============

GeoJSON
-------

The most commonly used GeoData format for applications on the web.

GeoJSON is a format for encoding a variety of geographic data structures.

.. sourcecode:: json

  {
    "type": "Feature",
    "geometry": {
      "type": "Point",
      "coordinates": [125.6, 10.1]
    },
    "properties": {
      "name": "Dinagat Islands"
    }
  }


GeoJSON supports the following geometry types: Point, LineString, Polygon,
MultiPoint, MultiLineString, and MultiPolygon. Geometric objects with additional
properties are Feature objects. Sets of features are contained by FeatureCollection objects.

`Read More <http://geojson.org/geojson-spec.html>`_

TopoJSON
--------

TopoJSON is an extension of GeoJSON that encodes topology.

CSV (Comma Seperated Values)
----------------------------

Comma-separated values (CSV) is a file which stores tabular data (numbers and text) in plain text.

WKT (Well-known text)
---------------------

**Well-known text (WKT)** is a text markup language for representing vector
geometry (Points, Lines, Polygons, etc...).

=============   ================
     Type           Examples
=============   ================
Point           POINT(45 -75)
LineString      LINESTRING (30 10, 10 30, 40 40)
Polygon         POINT(45 -75)
=============   ================

WKB (Well Known Binary)
-----------------------

**Well-known binary (WKB)** is the WKT binary equivalent which is used to transfer
and store the same information on databases, such as PostGIS, Microsoft SQL Server and DB2.

Shapefiles
----------

A shapefile is an ESRI vector data storage format for storing the location,
shape, and attributes of geographic features.
