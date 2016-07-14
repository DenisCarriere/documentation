GeoServer
=========

Preview the live DLCSPM GeoServer

https://api.dlcspm.com/geoserver

Features
--------

- Successfully tested over the DWAN with valid SSL certificate.
- Ability to connect to Microsoft SQL Server (not tested, but plugin was successfully installed)
- Successfully loaded single GeoTIFF or multiple GeoTIFF.
- Successfully loaded Shapefiles
- Successfully loaded MBTiles
- Successfully used a Web Adapter for HTTPS connections (All data served over SSL)


Fallbacks
---------

- GeoPackages, lots of bugs reported by the community and I've personally had no success loading any sample data. Bug tracker: https://osgeo-org.atlassian.net/browse/GEOS-7166
- There isn't a good built-in Web Adapter, I used Nginx for this since IIS wasn't able to accomplish this task without intense configurations.

Supported OGC Services
----------------------

- WCS
  - 1.0.0
  - 1.1.0
  - 1.1.1
  - 1.1
  - 2.0.1
- WFS
  - 1.0.0
  - 1.1.0
  - 2.0.0
- WMS
  - 1.1.1
  - 1.3.0
- WPS
  - 1.0.0
- TMS
  - 1.0.0
- WMS-C
  - 1.1.1
- WMTS
  - 1.0.0

Supported Data sources
----------------------

Vector Data Sources
~~~~~~~~~~~~~~~~~~~

- Shapefiles
- GeoPackage
- Microsoft SQL Server
- PostGIS

Raster Data Sources
~~~~~~~~~~~~~~~~~~~

- ArcGrid - ASCII GRID Coverage
- DTED - Digital Terrain Elevation Data
- ERDAS Imagine Coverage
- GeoPackages (mosaic)
- GeoTIFF
- MBTiles - Lightweigth SQLite raster catalog
- NITF - Military imagery standard
- RPFTOC - Military raster format typically used in CADRG

Software Requirements
---------------------

- `Windows Server 2012 R2 <https://www.microsoft.com/en-us/cloud-platform/windows-server-2012-r2>`_
- `Nginx for Windows <http://nginx.org/en/docs/windows.html>`_
- `GeoServer 2.10.X <http://geoserver.org/>`_
- `Java SE Runtime Environment 8 <http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html>`_

Hardware Requirements
---------------------

- 1 Core
- 500MB RAM
- 30 GB SSD Storage

Special Instructions
--------------------

- Enable ports [80,8080,443] on Windows Firewall
- Add SSL certificates
- Configure Nginx

GeoServer Install
-----------------

- Download & Install GeoServer 2.10
- Install GDAL 2.1.0
- Configure `PATH` & `GDAL_DATA` environment variables

Extensions (Plugins)
--------------------

- GeoPackage
- WPS
- GDAL
- SQL Server

Links
-----

- `32bit GDAL Windows binaries <http://www.gisinternals.com/query.html?content=filelist&file=release-1500-gdal-2-1-0-mapserver-7-0-1.zip>`_
- `Installing GDAL for Windows <http://sandbox.idre.ucla.edu/sandbox/tutorials/installing-gdal-for-windows>`_
