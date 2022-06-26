## EXERCICE 3:

## création du fichier docker-compose.yml

Networks:
lan_network:
driver: bridge

services:
Tomcat9:
hostname: dyhia
image: 14101994/tomcat:v1
ports:
- 20900:8080

[img_5.png](img_5.png)
