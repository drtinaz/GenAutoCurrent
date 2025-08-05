This service is intended to be used in parallel with a transfer switch service. Two options are available, and they are:
1. Kevin Windrem's Guimods, or
2. My simple transfer switch service which is not part of guimods. (The transfer switch service has been stripped from guimods to operate on it's own.)
   Either one of these options is best installed using kevin's setuphelper package. Kevin's guimods is included in the available list of packages.
   For my simple service, use the following:
       packagename: TransferSwitch
       github user: drtinaz
       branch/tag: main
   
the purpose of this service is to monitor the outdoor temperature, generator temperature, and altitude. The service then calculates a derated output for the generator based on these inputs. the base output (rated output) of the generator, the temperature derate variable, and the altitude derate variable can all be changed by editing auto_current.py. these variables are listed at the top of the script.

INSTALL

Before installing, one of the digital inputs should be setup in order to enable/disable the automatic derate function.
In the settings menu of the venus device, set one of the DI to 'Bilge Pump' and change the name to 'Gen Auto Current'.
You can then use the 'invert' option in the device menu to turn the function on or off.

The easiest way to install this package is by using kevins setup helper. Manually add the repo using the following settings:

package name: GenAutoCurrent
github user: drtinaz
branch/tag: main

First time installation will require some setup. Once the package has been downloaded, open a terminal session using ssh and navigate to the package directory
```
cd /data/GenAutoCurrent
```
copy the config file to the setupOptions directory
```
cp config.default /data/setupOptions/GenAutoCurrent/optionsSet
```
now you need to adjust the user settings in the config file to match your generator and system setup
```
nano /data/setupOptions/GenAutoCurrent/optionsSet
```
once you have adjusted your configuration to your needs, we now need to finish the installation
```
./setup install
```
