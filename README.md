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
easiest way to install is using kevins setup helper. Manually add the repo using the following settings:

package name: GenAutoCurrent
github user: drtinaz
branch/tag: main
