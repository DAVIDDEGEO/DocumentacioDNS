# Documentation DNS
## Description of the proyect
The proyect consist in a instalation of service DNS in a envairoment net. where we will install 3 name resolution zones on 2 machines.

## Creation of the 3 name resolucion zones
For it, we install bind9 on both machines, then we configure the 3 zones in the named.conf.local file in /etc/bind. The zones will be called zones A, B and C. Zone A and B are master and C is eslave. now configure this files in /var/lib/bind.
Now we will try to create 3 domains to organize the web pages.
We must configure this in our two Dns machines, we will call it ByViruzz and ByViruzz2. After
configuring them as DNS we will go to the /etc/bind/named.conf.local section
These two machines previously we must configure them as All this we must do once we install
bind9.
Bind9 is the service that will resolve the names of the domains by associating them with some
IPs that we will create
Once appointed we must configure some reverse zones between the DNS servers so that they
communicate and ask each other
Within the file I previously named to name the domains and subdomains

## Configure this zones
After created this files, we will configure with the parameters of the zones. When the client makes a name resolution query, zone A and B will answer first, in case of not finding answers, it will answer zone C and if there is no response, it will search worldwide servers.

## Serve cache.
In server Homer we will install a server cache

# Other dates 
## Boss of proyect
David Jesús Albújar Castro

## Employee
Abel Asensio Mancera


