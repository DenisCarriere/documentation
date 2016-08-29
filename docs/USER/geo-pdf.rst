GeoPDF
======

TerraGo Composer can be used to create official GeoPDFs from geospatialPDFs (as it is in our
particular workflow).  This could be an option if the decision is made to drop TerraGo Publisher;
however, TerraGo Publisher does have benefits that ArcGIS alone doesn’t provide.  It would depend
on what the cost benefit analysis of these extra features would be for the Army NDGSS on LCSS Lvl II network.
 
As I mentioned below, some of the benefits that TerraGo Publisher for ArcGIS provides over just ArcGIS exports:

Features
--------

- Ability to customize layers in a PDF. Turn them on and off, ability for the user to see the attributes of a feature, etc.
- Ability for the user to draw on a map (collect their data) and return the PDF to the Geo Cell in order to be convert the drawings to a shapefile. Very useful for planning.
- Ability to insert hyperlinks in PDF. Can add pictures, reports, etc. and can still be used offline.
- able to embed hyperlinks in GeoPDF exports (this cannot be done in ArcGIS and could be very powerful depending on the requirement for hyperlinking);
- greater control over what feature class attribution to embed into the GeoPDF (more on this below);
- ability to import GeoMarks (.twz files);
- ability to import geospatial/GeoPDFs into an ArcGIS environment as a georeferenced image (not as individual layers, but still useful);
- ability to maintain visible scale range settings.

For the feature class attribution that is embedded, there are a few things that I have found.
In an ArcGIS export, the layer has to have the following criteria set:

- layer checked on,
- have some sort of symbology set (colour, size, etc.)
- must be on top of any raster present in the layout (any feature class below a raster will not
have attribution exported)
 
For a TerraGo export, there is less criteria:

- layer checked on,
- does not have to have any symbology set (can be invisible: e.g. no colour or size)
- can be above or below a raster source in the layout.

Background
----------
 
Types of PDFs: 

- a non-geospatial PDF (no geospatial information embedded),
- a geospatial PDF (a PDF with geospatial information embedded from any software other than TerraGo products), and
- a GeoPDF (created using the TerraGo products:  Publisher for ArcGIS, TerraGo Composer for Adobe Acrobat, etc.).
 
At HSO(E), our main ArcGIS workstations are on the DWAN.  The current version is ArcGIS 10.2
with licencing levels ranging from ArcBasic to ArcStandard.  The DWAN workstations do not have
the following ArcGIS extensions:

- TerraGo Publisher for ArcGIS
- Data Interoperability
- xToolsPro.
 
Our secondary system is a stand-alone processing computer, currently running ArcGIS 10.1 at
the ArcAdvanced licence level.  The stand-alone system has the following ArcGIS extensions:

- TerraGo Publisher for ArcGIS v6.03.92
- Data Interoperability 10.1
- xToolsPro v11.0.1328.

DWAN TerraGo Toolbar is at 6.6.2.3


Geospatial PDF Creation Process
-------------------------------
 
With the DWAN as our main production platform and without the TerraGo Publisher for ArcGIS,
we can only produce geospatial PDFs using the standard ArcGIS Export functionality with the
“Export Map Georeference Information” box checked under the Advanced tab.  These geospatial
PDFs are non-compliant GeoPDFs – and as such are not recognized by the TerraGo Toolbar in
Adobe Reader/Acrobat on the DWAN (therefore, no GeoMark functionality, coordinate readouts,
etc.).  However, the products do contain geospatial information and coordinates can be displayed
using the native Adobe tools (Tools > Analyze > Geospatial Location Tool and Measuring Tool). 

Geospatial PDF to GeoPDF Process
--------------------------------
In order to convert these geospatial PDFs to fully compliant TerraGo GeoPDFs, the geospatial
PDFs are taken to the stand-alone system and converted using Adobe Acrobat 9 Pro Extended with
TerraGo Composer (v6.0.2.141) extension.  Once converted, they can be opened by any DWAN Adobe
Reader/Acrobat application with the TerraGo Toolbar installed and it will recognize it as a
GeoPDF and all the functionality of the TerraGo Toolbar is now available to the client.

GeoPDF Observations and Testing
-------------------------------

A couple of observations that I would like another Geo Tech to try to replicate on their systems
to see if the results are similar or unique to HSO(E):
 
Observation 1
~~~~~~~~~~~~~
- PDFs that are converted using the Data Interoperability extension or the standard ArcGIS export
functionality are not recognized as GeoPDFs on the DWAN using Adobe Reader/Acrobat with the current
DWAN TerraGo Toolbar (v6.6.2.3).  These geospatial PDFs are recognized with the native Adobe Tools
to read geospatial coordinates; however, the TerraGo Toolbar on the DWAN does not become active when
these geospatial PDFs are opened and therefore the ability to write GeoMarks is unavailable.
Also clients become confused when they don’t see the automatic readouts at the bottom of the PDF,
and therefore think that it isn’t a GeoPDF (not realizing that they could turn on the Adobe Tools
to read the coordinates).
 
Observation 2
~~~~~~~~~~~~~
- I am unable to email any PDF created using the Data Interoperability extension.  The DND email system
says the file is unscannable.

Data Interoperability Observations
----------------------------------
 
- Only creates a geospatial PDF not GeoPDF.
 
- For custom DRS type of products, the Data Interoperability does not allow for full customization
that is available in an ArcGIS layout for cartographic display.  Yes, the option to use the PDF Styler
and a few other tools/transformers exist for FME Workbench; however, the ‘make the product look good’
approach can only be set by visual cues in the layout and any special requirements of the client.
The ability to set transparencies, move/rotate text around, add insets, photos, unique grids, customize
the surround, etc. is lacking in this approach.
 
- The only real benefit that I can see for Data Interoperability is for bulk conversion of feature classes
to a geospatial PDF (with less emphasis on how the product looks). 

Recommendations
---------------
 
Since the TerraGo Toolbar is now standard on DWAN and CSNI workstations, Geo Techs must have the ability to
create and support GeoPDFs.  It is highly recommended to keep TerraGo Publisher for ArcGIS for its ability
to create an official GeoPDF recognized by the TerraGo Toolbar in Adobe Reader/Acrobat on the DWAN and CSNI. 
 
It is also highly recommended to include TerraGo Composer for Adobe Acrobat.  See comments above for benefits
of TerraGo Composer.

Collaborators
-------------
- Sgt Mercier (4 ESR)
- Rod Woods (HSO Esquimalt)
- Martin de Zuviria
- Denis Carriere
- Dave Rowlands
