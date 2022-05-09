# docker-nginx-php-mysql-template

# Installation
Klont das GIT Repo
```
git clone ****
```
<br>

Mit dem Befehl fahren wir die Container hoch. Die Option -d sorgt dafür, dass sie im Hintergrund laufen.
``` 
docker compose up -d 
```
<br>

Öffnet eine Shell im php Container
```
docker compose exec php bash
```
<br>

Mit Composer eine neue Symfony App im Hauptverzeichnis erstellen ohen Unterordner. 
```
composer create-project symfony/skeleton .
```
anschließend App aufrufen über 

http://localhost:8080/

<br>

shell mit exit wieder verlassen

<br>

Herunterfahren können wir die Container mit
```
docker compose down
```
oder 
```
docker compose kill
```



<br>
Wenn wir Änderungen am PHP Dockerfile vornehmen und das Image neu erstellen möchten, führen wir den Befehl so aus

``` 
docker compose up -d --build
```



# Verzeichnisse

## App
Anwendungscode

## nginx/default.conf
Webserverconfiguration wie von Symphony empfohlen

## php/Dockerfile
PHP Image aus dem Docker Hub so zu erweitern, dass wir Composer und eine PHP-Erweiterung verwenden können.

## docker-compose.yml
Herzstück unserer Entwicklungsumgebung. Hier werden wir die Container definieren, die wir verwenden wollen.




