# Video stoppt bei Notification
Jeder der sich zuhause ins Bett gelegt hat eine Karaffe kalte Milch bereitgesellt
hat und IT Crowd sehen wollte und jedes mal wieder auf play drücken musste als
er wieder eine nervige Nachricht einer schönen Frau/Mann bekommen hat wird sich
fragen wieso und wie kann ich das ausstellen.

Die Lösung ist ganz Simpel. Eine Notification ist als Telefon Anruf registriert.
Und es gibt ein entsprechendes Modul in Pulseaudio das aktiviert wird sobald ein
Telefon Anruf eingeht.

Wir wollen also Pulseaudio verändern. Dazu gehen wir in das Verzeichnis in dem
alle Konfigurationen zu finden sind.

```sh
cd /etc
```

Dort suchen wir nach pulseaudio oder so ähnlich.

`cd /etc/pul` <kbd>TAB</kbd>

Wir landen in `/etc/pulse` dort gibt es eine Datei
`sudo gedit default.pa`.  
Sucht mal ein wenig nach einem passenden Modul und
kommentiert das passende Modul einfach aus `#`. Fertig.
