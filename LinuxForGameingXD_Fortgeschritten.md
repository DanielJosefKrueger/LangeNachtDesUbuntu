# Linux for Gameing xD
Jetzt wo wir endlich eingesehen haben das Linux das einzig wahre Betriebsystem
ist wollen wir nicht mehr zurück, aber manchmal vermissen wir doch diese eine
Spiel das wir so gerne gespielt haben und das gibt es leider nur für Windows.

Wir haben jetzt mehrere Möglichkeiten.

1. Virtuelle Maschine benutzen
2. Wine benutzen
3. Steam Proton benutzen

## Virtuelle Maschinen
Die sind toll wir können einfach schnell Windows installieren und dann sind wir
im Spiel. Nur leider braucht einen VM doch etwas Leistung und wir wollen nichts
von unserem PC abgeben, außerdem Windows *igit*.

## Wine benutzen
Einige Spiele laufen unter Wine wirklich gut. Einfach mal probieren am besten
mit Tools wie PlayOnLinux oder Crossover. Es kann manchmal etwas nervig sein
und man muss etwas Zeit investieren bis man alle Abhängigkeiten installiert hat
in der Entsprechenden Wine Umgebung.

## Steam Proton
Das ist relativ neu und kann in den Settings von Steam aktiviert werden. Nicht
alle Spiele laufen jedoch, aber teilweise läuft es besser als mit Wine und
wesentlich einfacher ist es sowieso, aber wenn es nicht auf anhieb funktioniert
kann ja noch wine helfen also nicht verzagen.

## Controller
So jetzt haben wir endlich Dark Souls zum laufen bekommen mit Steam Proton, aber
das mit unserem Gamepad funktioniert noch nicht so ganz. Dann habt ihr ein ganz
ähnliches Problem wie ich. Die meisten Gamepads funktionieren out of the box.

xboxdrv könnte euch helfen.

Erst einmal sollte man aber testen ob es mit xboxdrv besser ist.
Einfach mal
```sh
sudo xboxdrv
```
gestartet und sehen ob alles so funktioniert wie erwartet.

Ihr könnt euch xboxdrv installieren und als Deamon starten.
```sh
sudo xboxdrv -D --mimic-xpad
```
Ihr könnt auch sicherheitshalber noch xpad deaktivieren.
```sh
sudo modprobe -r xpad
```

Wenn ihr euch jetzt denkt, aber ich möchte nicht ständig wieder xboxdrv starten.
Dann geht es euch genauso wie mir. Hier würde ich euch empfehlen mit systemd
warm zu werden und herausfinden wie man seinen eigenen service schreibt.
