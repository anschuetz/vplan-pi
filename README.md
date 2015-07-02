# vplan-pi
Einsatz auf einem RaspberryPi als Digitale Anzeigentafel.
Momentane Funktion:
- Anzeige einer HTTP-Seite.
  Fehler wie Netzwerkkabel steckt nicht, DNS ist kaputt, Webserver läuft nicht,... 
  werden abgefangen und ordentliche  Meldungen angezeigt. 
  Periodisch (default 10s) wird geprüft, ob ein Fehler vorliegt (oder wieder behoben wurde) 
  und dann das System wieder hergestellt.
- Anzeige einer Impress-Präsentation (ODT-Datei)
  Steuerung momentan noch durch Anlegen einer Datei, die den Pfad zur Präsentation enthält.

Installation:
- Kopieren des Repos nach /opt/vplan-pi (cd /opt/ ; git clone https://github.com/anschuetz/vplan-pi)
- Anpassen der Konfiguration in /opt/vplan-pi/etc/vplan-config
- Einrichten eines cron-jobs, der alle 5 Minuten /opt/vplan-pi/bin/vplan-checkobserver aufruft.

Vorarbeiten:
- Raspbian wheezy auf SD-Karte kopieren
- Nachinstallieren von unclutter, midori, x11vnc
