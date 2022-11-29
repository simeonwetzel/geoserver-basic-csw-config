# Basic GeoServer configuration sample for OGC-CSV support:
This brief document should provide a minimum configuration example of GeoServer to enable Harvesting of services to external metadata catalogues.

### ***Requirements***:
* An instance of GeoServer with existing layers
* An instance of GeoNetwork

# Steps:
1. Installation of the GeoServer CSW extension
2. Installation of the [ISO Metadata Profile community module](https://docs.geoserver.org/maintain/en/user/community/csw-iso/index.html)
3. Installation of the GeoServer [Metadata community module](https://sourceforge.net/projects/geoserver/files/GeoServer/2.22-M0/extensions/geoserver-2.22-M0-metadata-plugin.zip/download)
4. Replacing the configuration files with the ones provided in this repository
5. Start a Harvester in GeoNetwork


## (1) Installation of the GeoServer CSW extension:
Follow the installation instructions of the [documentation](https://docs.geoserver.org/stable/en/user/services/csw/installing.html).

**Please note**: the provided plugin download link is broken. Instead, search for the extension [here](https://geoserver.org/release/)

## (2) Installation of the ISO Metadata Profile community module:
Download and install the `geoserver-{version}-M0-csw-iso-plugin.zip` extension [here](https://sourceforge.net/projects/geoserver/files/GeoServer/)

The installation should create a directory **./csw** in the data folder (in Windows usually: ***C:\ProgramData\GeoServer\csw***)

## (3) Installation of the GeoServer Metadata community module:
Download and install the `geoserver-{version}-metadata-plugin.zip` extension for your GeoServer version [here](https://sourceforge.net/projects/geoserver/files/GeoServer/)

The installation should create a directory **./metadata** in the data folder (in Windows usually: ***C:\ProgramData\GeoServer\metadata***)

## (4) Replacing the configuration files with the ones provided in this repository
Replace the files in the **./csw** folder with the files in [this folder](/csw).

Replace the files in the **./metadata** folder with the files in [this folder](/metadata)

## (5) Start a harvester in GeoNetwork
* In GeoNetwork go to ***Admin console -> Harvesting***
* Then create a new "OGC CSW 2.0.2 Harveter"
* For **Service URL**: paste your GeoServer CSW endpoint (e.g. ***http://localhost:8080/geoserver/ows?service=csw&version=2.0.2&request=GetCapabilities***)
* For **Sort by**: paste `gmd:fileIdentifier/gco:CharacterString`
* Start harvester and see harvested results!
* One might also check the harvester logs in the ***\logs*** directory of GeoNetwork
