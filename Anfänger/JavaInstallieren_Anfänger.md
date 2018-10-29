# Wie installiere ich Java unter Ubuntu

Java zu installieren könnte nicht einfacher sein. In der
Regel wollen wir Java 8 installieren. Java 10 und 11 sind
zwar schon Verfügbar, aber viele IDEs, Programme und auch
die meisten Vorlesungen und Praktikas sind für Java 8
gemacht.  
Das kann sich natürlich ändern weshalb ich auch anfügen
werde wie ihr leicht die default-jvm wechseln könnt.

## Installation
```bash
sudo apt update
sudo apt install -y openjdk-8-jdk
```
Diese beiden Commandline Befehle sollten alles nötige
installieren. Fertig.

```bash
update-java-alternatives
```
Kannst du benutzen um zwischen mehreren installierten
Java Versionen zu wechseln.
