## Python Skript zur Generation von Volumen

Hey, ich hab in der letzten Zeit mal etwas an einem kleinen (eher schlechten) Skript geschrieben um mir ausgehend von den Eckpunkten eines Volumens mittels konvexer Hülle und trianguliering die Plattenmaße ausgeben zu lassen.

Hier sind auch die Abschrägewinkel der Platten untereinander dabei.

Ich hab hier jetzt mal die Erste Version hochgeladen. Sie funktioniert, wenn auch einiges an Modifikation nötig ist.

### Was tut das Skript?

Wenn ihr ganz nach unten scrollt seht ihr ein paar Punkte die ich definiere. Eines heißt pentagon, das andere pyramid.

Wenn man nun tun kann ist zwei funktionen auf diese Punkte anwenden:

- display: Generiert einen 3d plot des Volumens. Man sollte sich mit der Maus darin bewegen können.

- draw_plates: Generiert svg dateien im Ordner in dem das Skript ausgeführt wird. Für jedes Dreieck der Triangulierung eines. Hier sind die Eckpunkte mit index, winkel an der Ecke und die Kanten mit Länge und DOPPELTEM Abschrägewinkel eingezeichnet.

Ich habe mal ein Beispiel der platten der Pyramide als svg dateien mit dazugetan.

### Usage

Einfach Python installieren und die Pakete
 - matplotlib
 - mpl_toolkits (vermutlich automatisch)
 - numpy
 - scipy
 - drawsvg

 installieren. Dann das skript aussführen auf die Art der Wahl.

### TODO

Ich hab die Grundplatte aktuell definiert als all Dreiecke mit z koordinate = 0, d.h [x,y,0]. Das sollte man abfragen.

Aktuell funktioniert es nur für konvexe volumen.

Angrenzende Dreiecke mit Abschrägewinkel 180° bzw. 0° sind eigentlich die selbe platte. Ich muss die noch verbinden.

Wenn man richtig Lust hat kann man die svg dateien in einen cutlist optimierer geben um den Ausschuss zu minimieren.


### Reality Check

Wir haben das Pentagon volumen tatsächlich schon gebaut. Zumidest versucht. Die Winkel passen alle. Die Längen auch. Leider waren wir handwerklich zu unbegabt die Grundfläche plan zu halten und unser Hobel hat den Geist aufgegeben...

Daher sind wir noch nicht fertig, aber wir haben zumindest einen ganz guten Anfang. Ein Bild ist auch im Ordner.
