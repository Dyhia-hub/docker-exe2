# docker-exe2

Exercice 2

## le contenu du fichier Dockerfile:
"FROM fabric8/tomcat-9

LABEL maintainer=”dyhiaaouabed@gmail.com”

ADD webapp.war /opt/tomcat/webapps/
"

## Builder l'image tomcat à partir du docker file
docker build -t tomcat:v1    .

## le port utilisé
docker inspect tomcat:v1
![img.png](img.png)

## Lancer le conteneur TOM en deamon
docker run -d -p 8080:20200 --name DyhiaContainer tomcat:v1
![img_1.png](img_1.png)

## la page d'acceuil Tomcat:
![img_2.png](img_2.png)
echo "If you're seeing this, you've successfully installed Tomcat. Congratulations!" > result.txt

## création d'un user tomcat dans le conteneur:
cd /opt/tomcat/conf/
"vi tomcat-users.xml"
"<user name="logwire" password="docker" roles="admin-gui,admin-script,manager-gui,manager-status,manager-script,manager-jmx"/>"
![img_4.png](img_4.png)
## Charger ll'image crée dans le compte Docker-hub

docker login
docker image tag tomcat:v1 14101994/tomcat:v1
docker push 14101994/tomcat:v1
![img_3.png](img_3.png)

## Pusher les fichier sur Origin main
git add .
git commit -m"EXERCICE2"
git push origin main 
## FIN D'EXERCICE
