<img align="right" width="177" height="119" src="http://schuelerseite.otto-triebes.de/schuelerinfos/CFromm/DSL%20Logo.jpg">

# ALPHA - Imagetracking Test Case

Fallversuche bei 120Hz und 240Hz als Referenz für verschiedene Auswertungsmethoden.

Die Aufnahmen aus Olympus-Kamera sind bzgl. der Framerate sehr stabil und werden zuverlässig auf den Computer übertragen. Die Kamera schneidet das Ende des Videos ab, so dass die Aufnahme nicht zu früh beendet werden sollte, da anderenfalls das Ende des Experiments nicht sichtbar sein könnte.

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

Testauswertung von Georg dauerte ca. 40 Minuten und funktionierte größtenteils problemlos. Kleinere Arbeitsschritt-Korrekturen sind in die Anleitung bereits eingepflegt.
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

Tracking musste teilweise manuel durchgeführt werden, weil Viana das Objekt nicht erkannte. Automatisches Tracking erzeugt einige extreme Ausreißer. Sowohl manuelles als auch automatisches Tracking erzeugt sehr verrauschte Daten, insb. im Vergleich zu Track-Mate

![Viana.NET Plot](https://raw.githubusercontent.com/hausler89/alpha/master/Viana_120.png)
