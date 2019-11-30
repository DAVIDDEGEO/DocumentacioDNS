# Documentation DNS
## Description of the proyect
The proyect consist in a instalation of service DNS in a envairoment net. where we will install 3 name resolution zones on 2 machines.

## Creation of the 3 name resolucion zones
The section on creating three sub-kings is a section based on real circumstances that can help us solve this problem.
Try to configure 4 virtual machines in such a way that configuring them so that the first and second, second and third, third and fourth have connection to each other, that is, we need them to have connection between them from the first to the last.
For this we will configure it in VmWare, an app that is used to create and configure virtual machines.
For this we must create mainly the 4 machines, these are windows, debian (router), windows server (router2) and lubuntu Zone A will be windows and debian Zone B will be the two routers and zone C will be windows server and lubuntu To create these areas we must put the corresponding Vnets must be one Vnet per zone. Next so that they can make a connection between them we must modify the corresponding files to create the routes. These routes are direct connections of the machines we want
For it, we install bind9 on both machines, then we configure the 3 zones in the named.conf.local file in /etc/bind. The zones will be called zones A, B and C. Zone A and B are master and C is eslave. now configure this files in /var/lib/bind.

## Configure this zones
After created this files, we will configure with the parameters of the zones. When the client makes a name resolution query, zone A and B will answer first, in case of not finding answers, it will answer zone C and if there is no response, it will search worldwide servers.

## Serve cache.
In server Homer we will install a server cache
