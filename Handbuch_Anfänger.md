# Das Handbuch
Unter Linux gibt es ein sehr praktisches Programm.
Es ist sozusagen das google das lokal läuft und sehr detailliert und richtig
erklärt wie etwas funktioniert.

Das Programm heißt `man`.

Das wohl erste was man in C macht ist das typische "Hello World" Programm.
```
#include <stdio.h>

int main(int argc, char** argv) {
  printf("Hello World\n");
}
```
Wenn man jetzt zum Beispiel `man stdio` aufruft bekommt man alle Funktionen
die einem dadurch bereitstehen. Wir können einfach mit dem Mouserad scrollen
und wenn wir das Programm beenden wollen drücken wir einfach <kbd>q</kbd>.

Dort finden wir auch `printf(3)`.

Wir können jetzt einfach `man 3 printf` benutzen und bekommen einen ausführliche
Erklärung zu `printf`.

Bei Problemen oder auch wenn man sein wissen erweitern möchte um zu verstehen
was eine Funktion macht ist das Manual eine einfach und schnelle Möglichkeit.

Wenn wir zum Beispiel nur wissen wollen was von der Funktion printf zurück
geliefert wird können wir uns die Beschreibung des `RETURN VALUE` ansehen.
Um nicht lange danach suchen zu müssen kannst du einfach `/RETURN` eingeben und
mit Enter bestätigen und schon springen wir an die richtige Stelle.

Das Handbuch hat aber nicht nur Informationen zu C sondern zu fast jedem CLI
Programm. Wollen wir zum Beispiel eine detaillierte Informationen zu man selbst
haben wollen können wir einfach `man man` eingeben. Oder Wenn wir alles über
`ifconfig` wissen wollen tippen wir `man ifconfig`.

> Wer braucht schon google wenn er `man` hat.
