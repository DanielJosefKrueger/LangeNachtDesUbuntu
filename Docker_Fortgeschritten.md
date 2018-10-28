# Docker
Docker ist praktisch für die Entwicklung und auch für
Praktikas. Man kann zum
Beispiel einfach einen Datenbank Server installieren und ihn
nachher löschen.
Man kann sich auch leicht mehrere Versionen installieren und
das System bleibt
Müllfrei.

## Installation
Ich würde hier die Installation wie [hier](https://docs.docker.com/install/linux/docker-ce/ubuntu/#set-up-the-repository) beschrieben empfehlen.

Für eure Entwicklungsinstanz müsst ihr euch nicht unbedingt
eine Version
festlegen.

## Benutzung
Wenn ich jetzt zum Beispiel eine MongoDB Instanz für das
Datenbank Praktikum
brauche kann ich das einfach auf https://hub.docker.com gehen
in die Suche
"mongo" eingeben und dann am besten die offizielle Quelle
nehmen.  

## Erstellen
Dort findet man dann auch gleich das richtige Kommando:
```sh
docker run --name some-mongo -d mongo
```
Damit erstellt man sich einen MongoDB Server mit dem Namen
"some-mongo".

## Verwalten
Wir können uns alle Docker Container und ihren aktuellen Status
anzeigen lassen. Natürlich können wir auch die Container
starten, stoppen oder löschen.
```sh
docker ps
docker start some-mongo
docker stop some-mongo
docker rm some-mongo
```

## Auf MongoDB zugreifen
Wir wollen aber nicht nur eine MongoDB Datenbank sondern wir
wollen auch auf die Daten darauf zugreifen.
```sh
docker exec -it some-mongo mongo
```
Das führt und das Programm "mongo" im Container aus. Wir können
auch ganz einfach "bash" ausführen und befinden uns dann völlig
im Container.

## Dateien in den Container kopieren.
Wenn wir jetzt Dateien austauschen wollen können wir entweder
schon bei der Erstellung einen gemeinsamen Mount Punkt angeben,
oder wir nutzen.
```sh
docker cp /home/dude/fh/mongoprak.js some-mongo:/tmp
```
Damit wird die Datei in den Container kopiert und wir können
sie auch von dort aus finden.

## Aufräumen
So wenn man viel mit Mongo macht und vielleicht auch mal
selbst Dockerimages bastelt kann es schnell passieren, dass
die Festplatte schnell voll wird.
Zum einen können wir ungenutzte Container wie oben einfach
löschen, aber alte Images und Volumes bleiben auf dem System.
```sh
docker stop some-mongo && docker rm some-mongo
docker image prune
docker volume prune
```
Damit werden alle ungenutzen Images und Volumes gelöscht und
man hat schnell wieder viel Speicher zur Verfügung.
