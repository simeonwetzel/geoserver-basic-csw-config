# Basic GeoServer configuration sample for OGC-CSV support:
This brief document should support GeoServer maintainers in the configuration of service metadata to make it harvestable by metadata catalogues.

Goal:
Install and enable CSW ISO metadata profile in Geoserver and start a harvester in GeoNetwork.

# Necessary config steps:
1. Installation of the GeoServer CSW extension
2. Installation of the [ISO Metadata Profile community module](https://docs.geoserver.org/maintain/en/user/community/csw-iso/index.html)
3. Installation of the GeoServer [Metadata community module](https://sourceforge.net/projects/geoserver/files/GeoServer/2.22-M0/extensions/geoserver-2.22-M0-metadata-plugin.zip/download)
4. Replacing the configuration files with the ones provided in this repository


## (1) Installation of the GeoServer CSW extension:
Follow the installation instructions of the [documentation](https://docs.geoserver.org/stable/en/user/services/csw/installing.html).

**Please note**: the provided plugin download link is broken. Instead, search for the extension [here](https://geoserver.org/release/)

## (2) Installation of the ISO Metadata Profile community module:
Download and install the extension [here](https://sourceforge.net/projects/geoserver/files/GeoServer/2.22-M0/extensions/geoserver-2.22-M0-csw-iso-plugin.zip/download)

The installation should create a directory **./csw** in the data folder (in Windows usually: ***C:\ProgramData\GeoServer\csw***)

## (3) Installation of the GeoServer Metadata community module:
Download and install the extension [here](https://sourceforge.net/projects/geoserver/files/GeoServer/2.22-M0/extensions/geoserver-2.22-M0-metadata-plugin.zip/download)

The installation should create a directory **./metadata** in the data folder (in Windows usually: ***C:\ProgramData\GeoServer\metadata***)

## (4) Replacing the configuration files with the ones provided in this repository

Replace the files in the **./csw** folder with the files in [this folder](/csw).

Replace the files in the **./metadata** folder with the files in [this folder](/metadata)
