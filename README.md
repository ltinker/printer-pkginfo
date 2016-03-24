printer-pkginfo
===============

Creates a nopkg style pkginfo file to install a printer with Munki

### Example
```# ./printer-pkginfo --plist example-hp4100.plist -> example_pkginfo-1.0.plist```


### Recipe Keys
Printer Recipes currently support the following Recipe Keys being parsed by printer-pkginfo

|Key|Type|Required|Notes|
|---|---|---|---|
|version|String|False| If not specified in recipe default is version is 0.1   |
|name|String|True|   |
|queue_name|String|True|   |
|display_name|String|True||
|ppd|String|True|This is the installed printer drivers path|
|protocol|String|False|If not specified in recipe default is value is 'lpd'|
|location|String|False|This is optional and will be written as "" if nothing is specified|
|address|String|True| This is network location of the printer|
|default_catalog|String|False| If not specified in recipe default is value is 'testing'|
|default_category|String|False| If not specified in recipe default is value is 'Printers'|
|icon|String|False| allows you to set the image url for the package.
|requires|Array|False||
|options|Array|False| Add special printer options here e.g. 'landscape' see see cups manual for more details|
