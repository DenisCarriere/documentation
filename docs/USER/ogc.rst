OGC
===

Overview
--------

Open Geospatial Consortium is a collection of standards for geospatial file
formats & web protocols for GIS applications. Many applications which have mapping
components are built on top of these standards. It is important for GIS service
providers to publish according to OGC standards for greater interoperability
with consumers.

WMS
---

**Web Mapping Service (WMS)** is a web protocol which allows an application to
display raster maps from a given bounding box and coordinate system. The maps
can consist of imagery or a combination of styled vector layers.

WFS
---

**Web Feature Service (WFS)** is a web protocol which allows an application to
read a collection of vector data from a given bounding box and coordinate system.
Additional metadata can be extracted from each individual feature to create a
dynamic application with rich content provided by the feature service.

WFS-T
-----

**Web Feature Service Transactional (WFS-T)** is much like a WFS, however with
the ability to modify the features directly by the application. The types of
modifications consist of **Read/Update/Add/Delete**. To enable a transactional
service you must have your GIS data stored in a geo-enabled database such as
SQL Server 2012.

WCS
---

**Web Coverage Service (WCS)** is a web protocol which allows an application to
the true pixel values of a collection of rasters instead of RGB. For example an
elevation service would typically be a coverage service to extract the elevation
height in meters/feet of the raster, having this type of elevation service
available allows applications to perform line of sight calculations and many
other types of calculations that are based on elevation models.

GeoPackage
----------

Content Here
