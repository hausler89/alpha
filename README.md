<img align="right" width="177" height="119" src="http://schuelerseite.otto-triebes.de/schuelerinfos/CFromm/DSL%20Logo.jpg">

# ALPHA - Image-Tracking Test Case

Wir untersuchen verschiedene Tracking-Methoden zur Video-Auswertung eines bewegten Körpers. Ziel ist die Erfassung einer Trajektorie in physikalischen Einheiten in 2D. Die Daten sollen geeignet sein, Bewegungen auf ihre Geschwindigkeiten und Beschleunigungen hin zu untersuchen.

Wir testen drei verschiedene Systeme, die eine Video-Datei einlesen und die Bewegung eines Körpers erfassen können:

* TrackMate - ImageJ Plugin. https://imagej.net/TrackMate
* Viana.NET Windows Version für Physikunterricht. http://www.viananet.de/
* OpenCV Computer Vision - Verschiedene Tracking-Algorithmen, eingehüllt in selbstgeschriebener PyQT Oberfläche https://opencv.org/

## Daten
Vorhanden sind Referenzaufnahmen von Fallversuchen bei 120Hz und 240Hz für drei verschieden geformte Körper mit selber Masse. Die Fallbewegung wird mit allen drei Systemen getracked und die Trajektorie als t-y-Diagram dargestellt.

Die Aufnahmen aus Olympus-Kamera sind bzgl. der Framerate stabil (<0.1%) und werden zuverlässig auf den Computer übertragen. Die Kamera schneidet das Ende des Videos ab, so dass die Aufnahme nicht zu früh beendet werden sollte, da anderenfalls das Ende des Experiments nicht sichtbar sein könnte.

Wünschenswert wäre eine Kamera mit manuellen Belichtungseinstellungen.
- - - -
## Track-Mate

### Vorteile
* Zuverlässig und Reproduzierbar
* Keine Blackbox (Einblick in die Methode)
### Nachteile
* Viele Arbeitsschritte
* Unhandliches Ausgabeformat XML
  * Python-Script zum Plotten ist aber schon geschrieben und funktioniert zuverlässig.

Testauswertung von Georg dauerte ca. 40 Minuten und funktionierte größtenteils problemlos. Geübt dauert die Auswertung nicht länger als 5 Minuten. Kleinere Arbeitsschritt-Korrekturen sind in die Anleitung bereits eingepflegt.
![Track-Mate Plot](https://raw.githubusercontent.com/hausler89/alpha/master/TrackMate_120.png)
- - - -
## Viana.NET

### Vorteile
* In Schulen bekannt
* Relativ wenige Arbeitsschritte
* Ausgabe in CSV
### Nachteile
* Instabil, stürzt häufig ab.
* Unzuverlässige Erkennung
* Benötigt externe Video-Konvertierung
* Manuelles Tracking über 30Hz Bildrate mühsam und langsam

Tracking musste teilweise manuell durchgeführt werden, weil Viana das Objekt nicht erkannte. Automatisches Tracking erzeugt einige extreme Ausreißer. Sowohl manuelles als auch automatisches Tracking erzeugt sehr verrauschte Daten, insb. im Vergleich zu Track-Mate.

Auswertung dauert *geübt* etwa 15 Minuten. Ungeübt gibt es noch keine Messung.

![Viana.NET Plot](https://raw.githubusercontent.com/hausler89/alpha/master/Viana_120.png)
- - - -
## Python mit OpenCV
tbd
