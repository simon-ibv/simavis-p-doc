# SIMAVIS P Release Notes

  * [Version 8.2.x](#version-82)
  * [Version 8.1.x](#version-81)
  * [Version 7.1.x](#version-71)
  * [Version 6.2.x](#version-62)



## Version 8.2

### Version 8.2.3 (21.12.2016)
- `FIXED` Fehler bei Sortierung der Sollwerten behoben

### Version 8.2.2 (15.12.2016)
- `FIXED` Löschen des aktiven Typs im Frontend wird verhindert
- `FIXED` Fehler bei Berechnung von Typ- und Sollwert-Indices behoben
- `IMPROVED` JAI-Filter-Treiber im Setup abhakbar

### Version 8.2.1 (24.11.2016)
- `CRITICAL` Absturz bei leerem Dateipfad in D Bild lesen behoben
- `FIXED` D Text schreiben erstellt jetzt auch bei den Operation "CSV Eintrag schreiben" und "Vor Zeile einfügen" eine nicht vorhandene Datei
- `FIXED` Erneute Initialisierung in B Bildaufnahme VISION funktioniert auch mit Sony XCG-Kameras
- `IMPROVED` Performance der Overlays im Frontend verbessert
- `IMPROVED` Performance in H Merkmale deutlich verbessert
- `IMPROVED` M Bild wurde durch M Leinwand ersetzt. Die "Fenster in Bild" Möglichkeit existiert bereits seit längerem über F Fenster kopieren.
- `IMPROVED` Bei der Installation kann der JAI Filter-Treiber deaktiviert werden (dieser sollte nur für GigE-Vision-Kameras aktiviert werden)

### Version 8.2 (17.10.2016)
- `NEW` Neues Prüfelement B Bildaufnahme VISION für die GigeVision- und USB3Vision-Standards
- `NEW` Neues Prüfelement F Mustersuche++
- `NEW` T Timer hat nun als Eingang einen Index (es können mehrere Timer verwendet werden)
- `NEW` Prüfelement B Bildaufnahme lässt sich jetzt auch mit den aktuellen Kameras von IDS (mit Sony-Pregius-Chips) verwenden
- `NEW` Aktualisierung auf IDS-Treiberpaket 4.80.2
- `NEW` Ab sofort wird (sofern vorhanden) bei der Verwendung von B Bildaufnahme mit IDS-Kameras automatisch der erste Parametersatz geladen
- `NEW` Verbesserter Lizenz-Manager im Frontend mit Möglichkeit der Lizenz-Key-Eingabe im Setup
- `NEW` SIMAVKS Keyboard (Touch-Tastatur) wird automatisch ausgeblendet und lässt sich minimieren
- `NEW` SIMATIC S71200 und S71500 werden ab sofort unterstützt
- `NEW` Typen und Sollwerte werden ab sofort in INI-Dateien gespeichert (Kopie zwischen verschiedenen Projekten möglich)
- `NEW` Versionsnummer wird bei Archivierung im Archiv (project.ini) abgelegt
- `NEW` Hilfe-Button im Frontend, der eine projektspezifische Hilfe-PDF öffnet (sofern diese im Projektverzeichnis abgelegt ist)
- `FIXED` Fixed: QMT wird bei automatischem Slot-Wechsel korrekt geladen
- `FIXED` Fixed: Pfad für Leinwand-Dateien wird jetzt korrekt abgelegt und nicht an verschiedenen Stellen gespeichert
- `FIXED` Fixed: Frontend blieb beim Slotwechsel manchmal hängen
- `FIXED` Fixed: F Normalisierung funktioniert nur mit Monochrom-Bildern
- `FIXED` Fixed: Absturz bei F Skalierung, wenn Skalierung zu klein gewählt ist
- `FIXED` Fixed: Absturz bei D Bild lesen, wenn die Datei nicht existiert
- `FIXED` Fixed: Pfad für Leinwand-Dateien wird korrekt gesetzt
- `FIXED` Fixed: Halconroot-Umgebungsvariable muss nicht mehr gesetzt werden
- `FIXED` Fixed: Speicherbutton wurde nach Benutzerwechsel manchmal nicht angezeigt
- `FIXED` Fixed: Absturzursache in F DMC Lesen
- `FIXED` Fixed: FE Bildausgabe lieferte manchmal ein falsch kodiertes Gesamtergebnis zurückgeliefert



## Version 8.1

### Version 8.1.10 (08.03.2016)
- `CRITICAL` Behebung eines Fehlers der in manchen Situationen zu einem Absturz bei der Benutzung der Fill-Up-Operation in F Morphologie führen konnte.

### Version 8.1.9 (24.02.2016)
- `CRITICAL` Fehler aus D Bild lesen entfernt, der zur Kumulierung und zu Abstürzen führen konnte
- `CRITICAL` Fehler aus O Aufruf entfernt, der zu Abstürzen führen konnte
- `FIXED` Sollwerte gingen sporadisch beim Kopieren und Einfügen neuer Sollwerte verloren

### Version 8.1.8 (17.12.2015)
- `CRITICAL` Es wurden mehrere Fehler behoben, die unter Umständen zu Abstürzen führen konnten. Betroffen waren die Prüfelmente FE Overlay Text und FE Overlay Grafik.
- `CRITICAL` In M Fenster war unter bestimmten Bedingungen noch ein Speicherleak vorhanden, der mit diesem Release entfernt ist.
- `FIXED` Korrekturen an I Tinkerforge IO

### Version 8.1.7 (01.12.2015)
- `FIXED` Einseitige Schwelle bei F Binärisierung korrigiert (so wie bei F Morphologie bzw. beidseitigen F Binärisierungs-Schwellen)
- `FIXED` Opening / Closing F Morphologie generiert keinen schwarzen Rand mehr
- `FIXED` Leere Meldung beim Starten des Backends über das Frontend (bei eingeschränkten Benutzerrechten) entfernt
- `IMPROVED` Information über gedrehte Templates bei F Mustersuche ergänzt

### Version 8.1.6 (17.11.2015)
- `FIXED` F Fenster kopieren ändert jetzt den Leinwand-Modus in "Farbe" wenn das Eingangsfenster farbig ist
- `FIXED` Grau-Kanal wird jetzt von F Fenster kopieren, F Skalierung und F Normalisierung generiert wenn das Eingangsfenster farbig ist
- `FIXED` O Fenster laden verändert jetzt nicht die Fenstergröße (war bisher der Fall, wenn z.B. durch F Skalierung ein Fenster mit geradzahliger Breite und Höhe generiert wurde)

### Version 8.1.5 (05.11.2015)
- `FIXED` F DMC Lesen++ war in vorigen Releases (ab 8.1) nicht voll funktionsfähig
- `FIXED` Verbesserungen beim Speichern von Typen und Sollwerten um zu verhindern, dass diese verloren gehen

### Version 8.1.4 (21.10.2015)
- `CRITICAL` Fehler in D Bild lesen behoben, der u.a. zu Abstürzen führen konnte
- `FIXED` Händischer Typwechsel löschte Statistikbalken (Frontend)
- `FIXED` Sollwerte gingen bei automatischem Typwechsel (via Backend) während dem Editieren verloren
- `IMPROVED` Lizenz-Manager öffnet sich jetzt nur einmal (auch wenn dieser manuell geöffnet wurde)

### Version 8.1.3 (03.09.2015)
- `FIXED` Fehler im Frontend der dazu führen konnte, dass das Bild nicht ausgegben wurde.
- `IMPROVED` K Musterkorrelation kann jetzt auch ohne vorheriges Einlernen verwendet werden.

### Version 8.1.2 (13.08.2015)
- `FIXED` Lage-Referenz wurde in manchen Fällen nicht korrekt gesetzt
- `IMPROVED` Genauigkeit von T Sleep erhöht
- `IMPROVED` Aktualisierung der IDS-Treiber auf Version 4.70

### Version 8.1 (10.08.2015)
- `CRITICAL` Fehler behoben, der bei mehrfach verschachtelten Unterprogrammen zu Fehlverhalten oder gar Abstürzen führen konnte
- `CRITICAL` Fehler behoben, der dazu führte, dass bei manchen Prüfelementen der Fensterausgang invalide wurde. Dadurch konnten weitere Bildverarbeitungs-Algorithmen nicht mehr korrekt ausgeführt werden
- `CRITICAL` Fehler in VSX Betriebsart behoben, der zu Abstürzen führte
- `FIXED` Steuerbuttons-Navigation war in manchen Fällen nicht mehr möglich
- `FIXED` EXE-Dateien lassen sich als Autostart-Datei im Projekt (Frontend Projekteinstellungen) vorwählen, auch wenn Leerzeichen im Pfad existieren
- `FIXED` D Bild lesen liest berechnet den Graukanal jetzt korrekt, wenn ein Farbbild geladen wird
- `FIXED` K Merkmale bezieht sich jetzt korrekt auf den Eingangsvektor (bislang wurde der Vektor neu aus dem Bild berechnet, d.h. vorgeschaltete Glättungsfunktionen hatten keine Auswirkung)
- `FIXED` Offline-Bildpfad wird im Frontend jetzt korrekt angezeigt
- `FIXED` Benutzer-Rechte können jetzt wieder korrekt gesetzt werden
- `FIXED` QMT kann manchmal nicht angezeigt werden
- `FIXED` Position der Overlays im Frontend verbessert
- `FIXED` Ringpuffer funktioniert bei Speicherung der Bilder über FE Bildausgabe jetzt korrekt
- `FIXED` Automatisches QMT-Ergebnis wurde in manchen Fällen falsch ausgegeben
- `FIXED` Fehler in V Aufpunktsuche behoben, der dazu führte, dass eine doppelte Kantenspitze nicht als Kante gefunden wurde
- `FIXED` Fenster Winkel wurde bei F Morphologie trunkiert
- `FIXED` Strichpunkt darf in Bezeichnung der Frontend Sollwerte vorhanden sein
- `FIXED` Fehler behoben, der im Zusammenhang mit Subtyp-Referenzen dazu führte, dass diese erst beim Neustart gelöscht werden konnten
- `FIXED` Fehler behoben, der dazu führte, dass die Fenster-Inhalte im Backend in manchen Fällen falsch extrahiert wurden
- `FIXED` Dearchivieren und Überschreiben per Doppelklick ohne "Programs"-Verzeichnis führt nicht mehr zur Löschung der vorhandenen Programme

- `IMPROVED` Auto-Speichern und Auto-Dauertrigger können jetzt auch per Rechtsklick aktiviert werden
Dadurch wird die Touch-Unterstützung verbessert, da manche Touch-Monitore keinen langen Links-Klick ermöglichen
- `IMPROVED` Visuelle Rückmeldung des Speichern-Buttons verbessert
- `IMPROVED` Overlay-Positionen im Frontend korrigiert
- `IMPROVED` Darstellungsfehler der Dauertrigger-Button Autostopp-Funktion korrigiert
- `IMPROVED` Pixel-Zähler in F Farbbinärisierung an F Binärisierung angepasst (es werden auch invers die weißen Pixel gezählt)

- `NEW` Neues Prüfelement F Skalierung
- `NEW` Neue Touch-Tastatur inkl. Support für kyrillische Schriftzeichen
- `NEW` Mehrere Backend-Fenster lassen sich jetzt parallel öffnen
- `NEW` Neues Prüfelement F Fenster kopieren
- `NEW` Neues Prüfelement F Normalisieren
- `NEW` Performance von F Filter verbessert und weitere Filter hinzugefügt
- `NEW` Performance von F Binärisierung verbessert und weitere Möglichkeiten hinzugefügt
- `NEW` Performance von F Morphologie verbessert, weitere morphologische Operatoren hinzugefügt und Opening sowie Closing korrigiert (Fenster wird aufgeweitet)
- `NEW` Backend in englischer Sprache verfügbar
- `NEW` Performance von D Bild lesen optimiert
- `NEW` Verfügbarer Speicher (des Backends) wird im Frontend-About-Dialog angezeigt, sowie eine Speicher-Warnung ausgegeben, sollte dieser unter 200 MB fallen
- `NEW` Beim Stoppen des Backends wird die Markierung nicht mehr verändert
- `NEW` Anzeigefenster werden im Backend besser positioniert
- `NEW` D Bild lesen puffert Bilder intelligenter und kann auch "ohne Fenster" eingelesen werden
- `NEW` Lizenz-Manager im Frontend akzeptiert nun die Eingabe von Kleinbuchstaben und fügt Bindestriche automatisch hinzu
- `NEW` Neues Prüfelement FE Slot zur Überprüfung und zum Setzen des aktuell angewählten Frontend-Slots



## Version 7.1

### Version 7.1.14 (17.12.2015)
- `CRITICAL` Es wurden mehrere Fehler behoben, die unter Umständen zu Abstürzen führen konnten. Betroffen waren die Prüfelmente FE Overlay Text und FE Overlay Grafik.
- `CRITICAL` In M Fenster war unter bestimmten Bedingungen noch ein Speicherleak vorhanden, der mit diesem Release entfernt ist.
- `FIXED` Korrekturen an I Tinkerforge IO

### Version 7.1.13 (09.10.2015)
- `FIXED` Händischer Typwechsel löschte Statistikbalken (Frontend)
- `FIXED` Sollwerte gingen bei automatischem Typwechsel (via Backend) während dem Editieren verloren
- `IMPROVED` Lizenz-Manager öffnet sich jetzt nur einmal (auch wenn dieser manuell geöffnet wurde)

### Version 7.1.12 (05.08.2015)
- `CRITICAL` Fehler aus O Aufruf entfernt, der unter manchen Umständen zu Abstürzen führen konnte

### Version 7.1.11 (16.07.2015)
- `CRITICAL` Fehler behoben, der zu Abstürzen führen konnte

### Version 7.1.10 (02.06.2015)
- `CRITICAL` Fehler in O Aufruf entfernt, die zu Abstürzen führen konnten
- `CRITICAL` Fehler in VSX Betriebsart behoben, der zu Abstürzen führte
- `FIXED` Fehler in V Aufpunktsuche behoben, der dazu führte, dass eine doppelte Kantenspitze nicht als Kante gefunden wurde
- `FIXED` Fenster Winkel wurde bei F Morphologie trunkiert

### Version 7.1.9 (12.05.2015)
- `FIXED` Um Abstürze besser lokalisieren zu können, wurden die Log-Ausgaben in diesem Fall erweitert.

### Version 7.1.8 (08.05.2015)
- `FIXED` QMT kann manchmal nicht angezeigt werden.
- `FIXED` Position der Overlays im Frontend verbessert.
- `FIXED` EXE-Dateien können jetzt auch gestartet werden, wenn Leerzeichen im Pfad existieren.
- `FIXED` Steuerbuttons-Navigation war in manchen Fällen nicht mehr möglich.
- `IMPROVED` Auto-Speichern und Auto-Dauertrigger können jetzt auch per Rechtsklick aktiviert werden.
Dadurch wird die Touch-Unterstützung verbessert, da manche Touch-Monitore keinen langen Links-Klick ermöglichen.
- `IMPROVED` Visuelle Rückmeldung des Speichern-Buttons verbessert.

### Version 7.1.7 (05.05.2015)
- `CRITICAL` Fehler behoben, der dazu führte, dass bei manchen Prüfelementen der Fensterausgang invalide wurde. Dadurch konnten weitere Bildverarbeitungs-Algorithmen nicht mehr korrekt ausgeführt werden.

### Version 7.1.6 (24.04.2015)
- `CRITICAL` Fehler behoben, der bei mehrfach verschachtelten Unterprogrammen zu Fehlverhalten oder gar Abstürzen führen konnte

### Version 7.1.5 (20.03.2015)
- `FIXED` Fehler behoben, der dazu führt, dass nicht in jedem Fall die Offline-Bildpfade im Frontend angezeigt werden.

### Version 7.1.4 (12.03.2015)
- `FIXED` Fehler bei allen Kreisprofil-Prüfelementen wie z.B. K Merkmale behoben.

### Version 7.1.3 (28.11.2014)
- `CRITICAL` Fehler in B Bildaufnahme im Zusammenhang mit mehreren Kameras entfernt, der teilweise zu Abstürzen führen konnte.
- `CRITICAL` Alte nicht mehr vorhandene Referenzen werden beim Öffnen des Backend entfernt. Dadurch werden Abstürze und weitere Probleme beim Editieren behoben.
- `FIXED` Fehler in B Bildaufnahme im Zusammenhang mit dem Wechsel von asynchronem Hardware-Trigger zu Software-Trigger entfernt.
Der Fehler äußerte sich dadurch, dass die Kameras im Software-Trigger-Modus ständig getriggert wurden, nachdem zuvor der asynchrone Hardware-Trigger-Modus aktiv war.
- `FIXED` Fehler im Frontend behoben, der die Bedienung negativ beeinflussen konnte
- `FIXED` Lizenz-Key wird besser zwischen Backend und Frontend synchronisiert
- `FIXED` Bildpfad im Einzeltrigger auch immer anzeigen
- `FIXED` Bei IDS-Kameras nun auch einseitig (gegenüber der Kamera-Auflösung) verkleinerte Leinwand möglich
- `FIXED` Fehler aus I TCP Kommunikation und I Digital/Analog I/O entfernt der zur Verlangsamung des Backends führte
- `FIXED` FE Bildausgabe verhält sich nun bei Systemfehler-Ausgabe identisch (d.h. die Einstellung **Bildaufnahme vorausgesetzt** wirkt sich ab sofort auch bei Systemfehlern aus.


### Version 7.1.2 (14.10.2014)
- `FIXED` I Digital/Analog I/O liest die digitalen Eingänge jetzt immer korrekt

### Version 7.1.1 (22.09.2014)
- `CRITICAL` Korrektur der Auto-Referenzierung, die dazu führte, dass Prüfelemente nicht mehr funktionierten
- `CRITICAL` Kritischen Fehler in B Bildformat entfernt, der zu Abstürzen führen konnte
- `CRITICAL` Fehler in F DMC Lesen beseitigt, der dazu führte, dass die aktuellen Bild-Inhalte gelöscht wurden
- `FIXED` Die Prüfelemente TS Klassen-Grenze und TS Normierung erscheinen jetzt wieder im Prüfelemente-Vorrat
- `FIXED` QMT-Bild Überschrift optimiert
- `FIXED` Letzten QMT-Tab und QMT-Position beim Starten des Frontends anwählen
- `FIXED` IO-Bereiche in PDF-Protokollen "übermalen" jetzt nicht mehr die Diagramm-Achsen
- `FIXED` Button "Herunterfahren" lässt sich jetzt korrekt per Rechteverwaltung deaktivieren
- `FIXED` Eingestellter Typ wird jetzt beim Hochfahren übernommen
- `IMPROVED` F DMC Lesen gibt jetzt einen genaueren Qualitätswert aus


### Version 7.1 (01.09.2014)
#### Bug-Fixes
- `CRITICAL` Neue IDS-Treiber-Version integriert, welche Probleme mit nahezu allen GigE-Kameras behebt, die bislang zu Aufhängern der Kamera geführt haben
- `FIXED` Der gesetzte Timeout bei I TCP Kommunikation wirkt sich jetzt tatsächlich auf die Verbindung und auf das Empfangen von Texten aus
- `FIXED` FE Bildausgabe funktioniert jetzt auch ohne dass ein Typ angewählt ist
- `FIXED` Abgespeicherte Bilder werden jetzt auch wieder in QMT abgespeichert
- `FIXED` TCP Kommunikation trennt Verbindung nicht mehr, wenn leerer Text gesendet wird
- `FIXED` Behebung eines Fehlers, der dazu führte, dass Benutzer-Rechte nicht korrekt gesetzt werden konnten

#### Allgemeine Neuerungen
- `NEW` Software- und Hardware-Lizenzierung im Wechsel möglich
- `NEW` SIMAVIS P wurde für Mehrbenutzer optimiert:
- Alle veränderlichen Daten werden jetzt standardmäßig im Projektverzeichnis abgelegt (z.B. Log-Files)
- Das Projektverzeichnis ist standardmäßig im Benutzerordner abgelegt, d.h. jeder Benutzer kann seine eigene Projektverwaltung verwenden
- AGLink-Konfigurations-Dateien (für S7-Kommunikation) werden jetzt standardmäßig im **Miscellaneous**-Verzeichnis des aktuellen Projekts gesucht. Dieses Verzeichnis wird automatisch erstellt und dient der Ablage sonstiger projektrelevanter Dateien. Weitere Infos siehe I S7 Verbindung.

#### Neue Frontend-Features
- `NEW` Kontrollbereich im Frontend optimiert. Buttons werden jetzt nicht mehr deaktiviert, sondern ganz ausgeblendet, wenn sie nicht "drückbar" sind
- `NEW` Neuen Button **Herunterfahren** in der Titelleiste
- `NEW` Min- und Max-Markierung in QMT wird jetzt auch während des Betriebs angezeigt
- `NEW` Speichern-Button im Frontend wird beim Bild-Abspeichern über das Backend als visuelle Rückmeldung gedrückt
- `NEW` Touch-Tastatur wird beim Beenden vom Frontend automatisch geschlossen
- `NEW` Die Buttons in der Titelleiste können per Rechteverwaltung deaktiviert werden. Hier ein Beispiel wo nur Herunterfahren erlaubt ist, daneben die Titelleiste mit allen Berechtigungen

#### Neue Backend-Features
- `NEW` Optimierte Referenzierung im Backend: Einmaliger Klick auf gesetzten Referenz-Haken entfernt diesen
- `NEW` Neues Prüfelement H Merkmale, welches das PE H Statistikmerkmale ersetzt
- `NEW` Neues Prüfelement I Digital/Analog I/O für digitale/analoge I/O-Baugruppe
- `NEW` Neues Prüfelement F DMC Lesen
- `NEW` Einfügen eines Prüfelements aus dem Vorrat während sich das Backend im Run befindet ist jetzt möglich (nach Bestätigung einer Abfrage)
- `NEW` Help-Dateien aktualisiert



## Version 6.8

### Version 6.8.14 (17.12.2015)
- `CRITICAL` Es wurden mehrere Fehler behoben, die unter Umständen zu Abstürzen führen konnten. Betroffen waren die Prüfelmente FE Overlay Text und FE Overlay Grafik.
- `CRITICAL` In M Fenster war unter bestimmten Bedingungen noch ein Speicherleak vorhanden, der mit diesem Release entfernt ist.

### Version 6.8.13 (05.08.2015)
- `CRITICAL` Fehler aus O Aufruf entfernt, der unter manchen Umständen zu Abstürzen führen konnte

### Version 6.8.12 (28.05.2015)
- `CRITICAL` Fehler in O Aufruf entfernt, die zu Abstürzen führen konnten
- `CRITICAL` Fehler in VSX Betriebsart behoben, der zu Abstürzen führte
- `FIXED` Fehler in V Aufpunktsuche behoben, der dazu führte, dass eine doppelte Kantenspitze nicht als Kante gefunden wurde
- `FIXED` Fenster Winkel wurde bei F Morphologie trunkiert

### Version 6.8.11 (12.05.2015)
- `FIXED` Um Abstürze besser lokalisieren zu können, wurden die Log-Ausgaben in diesem Fall erweitert.

### Version 6.8.10 (05.05.2015)
- `CRITICAL` Fehler behoben, der dazu führte, dass bei manchen Prüfelementen der Fensterausgang invalide wurde. Dadurch konnten weitere Bildverarbeitungs-Algorithmen nicht mehr korrekt ausgeführt werden.
- `CRITICAL` Fehler behoben, der bei mehrfach verschachtelten Unterprogrammen zu Fehlverhalten oder gar Abstürzen führen konnte

### Version 6.8.9 (14.01.2015)
- `FIXED` Fehler in allen Ringprofil Prüfelementen entfernt, der eine Glättung des Profils verhinderte (z.B. K Merkmale, K Aufpunktsuche oder K Musterkorrelation).
- `FIXED` Behebung eines Fehlers, der dazu führte, dass Benutzer-Rechte nicht korrekt gesetzt werden konnten.

### Version 6.8.8 (29.10.2014)
- `CRITICAL` Fehler in B Bildaufnahme im Zusammenhang mit mehreren Kameras entfernt, der teilweise zu Abstürzen führen konnte.
- `FIXED` Fehler in B Bildaufnahme im Zusammenhang mit dem Wechsel von asynchronem Hardware-Trigger zu Software-Trigger entfernt.
Der Fehler äußerte sich dadurch, dass die Kameras im Software-Trigger-Modus ständig getriggert wurden, nachdem zuvor der asynchrone Hardware-Trigger-Modus aktiv war.

### Version 6.8.7 (10.10.2014)
- `FIXED` I Digital/Analog I/O liest die digitalen Eingänge jetzt immer korrekt

### Version 6.8.6 (09.09.2014)
- `IMPROVED` F DMC Lesen gibt jetzt einen genaueren Qualitätswert aus

### Version 6.8.5 (01.09.2014)
- `CRITICAL` Neue IDS-Treiber-Version integriert, welche Probleme mit nahezu allen GigE-Kameras behebt, die bislang zu Aufhängern der Kamera geführt haben

### Version 6.8.4 (14.08.2014)
- `CRITICAL` Absturzursache in B Bildaufnahme behoben (Problem kann auftreten, wenn FE-Slot und Kamera-Index unterschiedlich sind).

### Version 6.8.3 (08.08.2014)
- `FIXED` Abgespeicherte Bilder werden jetzt auch wieder in QMT abgespeichert.

### Version 6.8.2 (09.07.2014)
- `CRITICAL` B Bildaufnahme bleibt aufgrund eines uEye-Fehlers bei GigE-Kameras manchmal hängen. Dafür gibt es bereits eine Vorab-Version der uEye-Treiber 4.41. Diese ist aber aufgrund des Beta-Stadiums noch nicht in dem Setup enthalten und wird erst in der Version 6.8.3 verwendet werden. Sollten Sie uEye-GigE-Kameras verwenden, installieren Sie diese Vorab-Version im Anschluss an die SIMAVIS P Installation!
- `CRITICAL` Behebung eines Fehlers beim Speichern von Projekten, wenn mit uEye-Kameras gearbeitet wird.
- `CRITICAL` Fehler in I Digital IO behoben (mehrere Bits mit Offset setzen).
- `FIXED` V Musterkorrelation geht jetzt auch ohne eingelerntem Vektor, z.B. über ein Vergleich mit einem Fenster aus einer Datei.
- `FIXED` Probleme mit asynchronem Software-Trigger bei uEye-Kameras behoben.
- `FIXED` Kamera-Konfig-Tool von B Bildaufnahme lässt sich jetzt wieder öffnen.
- `FIXED` Abgehakte Schwellen in den Frontend-Sollwerten werden vollständig ignoriert, auch wenn diese nicht plausibel sind.
- `FIXED` PPM- und CpK-Werte werden jetzt nicht mehr angezeigt, wenn diese negativ sind (macht keinen Sinn).
- `FIXED` Wenn im Frontend kein Typ vorgewählt ist, wird trotzdem der Ergebnis-Rahmen korrekt angezeigt.
- `FIXED` Schichtprotokoll jetzt auch vollständig auf englisch übersetzt.
- `FIXED` Vorschau von Offlinebildern im Frontend korrigiert.
- `FIXED` Automatische Bewertung des Gesamtergebnis (FE Bildausgabe) funktioniert nun auch ohne QMT-Aktivierung.
- `FIXED` Beim Herauszoomen werden die QMT-Werte nun auch im Automatik-Start-Modus geladen.
- `FIXED` M Bild: Problem beim Laden eines Grauwertbilds in eine farbige Leinwand behoben.
- `FIXED` O Aufruf löscht jetzt den Bild-Zwischenspeicher, wenn es ohne Bildübertragung aufgerufen wird. Bislang wurde dann in B Bildformat trotzdem das zuletzt in den Zwischenspeicher übertragene Bild geladen.
- `FIXED` Prüfelement-Fenster lassen sich jetzt nicht mehr mehrfach öffnen.
- `FIXED` Ein unbewerteter Messwert wird im Statistikzähler des Einzeldiagramms nun als nicht relevant (grau) angezeigt (wurde vorher rot angezeigt).
- `FIXED` Aktualisierung der uEye-Treiber auf Version 4.40.
- `FIXED` Fehler bei der automatischen Erstellung der V7-Dateien (vom Frontend) behoben.
- `FIXED` Korrektur bei IO-Bereich-Markierung in QMT.
- `FIXED` Korrektur der Messwert-Bewertung von FE Messwerte und dem Frontend.
- `FIXED` Rechte in der Benutzerverwaltung sind nun wieder korrekt sortiert.
- `FIXED` Fehler behoben, der dazu führte, dass sich Bilder aus der Offline-Bildauswahl nicht löschen lassen.
- `FIXED` Wird ein Projekt dearchiviert, welches keine QMT-Daten hat, werden trotzdem alle anderen Dateien dearchiviert.
- `FIXED` Sigma und Mittelwert in QMT werden jetzt korrekt dargestellt.
- `FIXED` Original-Bilder werden nun mit der krorekten Dateiendung (BMP) gespeichert.
- `FIXED` Gruppen in QMT können nun auch umbenannt werden, wenn weitere (abgehakte) Sollwerte mit dem ursprünglichen Gruppennamen existieren.
- `FIXED` Wenn der Statistikbalken ausgeblendet werden soll, wird dieser nun auch im Vorschaufenster (Mehrslot-Betrieb) ausgeblendet.
- `FIXED` Absturz bei Kamera-Treiber-Wechsel (z.B. von Baumer auf uEye) behoben.
- `FIXED` Performance-Verbesserung bei D Bild lesen, wenn dieses nur als Fenster geladen wird.
- `FIXED` Fehler in der manuellen Protokollgenerierung behoben.
- `FIXED` Zeichnen der Overlays im Backend (F8) kann in den Einstellungen nicht mehr deaktiviert werden. Daher kommt auch bei Windows-Benutzerwechsel keine Meldung mehr beim Starten des Backends.
- `FIXED` FE Messwerte berücksichtigt jetzt auch nur einseitig angelegte Schwellen.
- `FIXED` Backend-Helpfiles gehen jetzt in eigenem Fenster auf (nicht mehr über den Browser).
- `FIXED` Prüfelemente-Vorrat bereinigt.
- `FIXED` Klick auf Auto Start / Dauertrigger / Video im Frontend lädt die QMT-Werte jetzt neu.
- `FIXED` Bei einem Betriebsart-Wechsel von Stopp auf Automatik wird zu dem aktuellsten QMT-Datensatz gesprungen.
- `FIXED` Dauertrigger mit aktivierter Auto-Stopp-Funktion überspringt nun keine Bilder mehr.
- `FIXED` Fehler in I Digital IO behoben (im Zusammenhang mit COM-Port-Wechsel).
- `FIXED` Frontend-Hilfe geht jetzt auch mit englischem Frontend auf.
- `FIXED` Hilfe-Datei für B Bildaufnahme erweitert und korrigiert.
- `FIXED` Einzeltrigger im Frontend synchronisiert nun die QMT-Werte.
- `FIXED` Fehler in D Text lesen behoben (CSV lesen ging nicht).

### Version 6.8.1 (16.12.2013)
- `NEW` Qualitäts Management Tool (QMT) für statistische Analyse der Bildverarbeitung inkl. neuer Prüfelemente FE Messwerte und FE Bildausgabe
- `NEW` Automatische Bewertung der Messwerte / Prüfwerte aufgrund eingestellter Bewertungsmodi in den Sollwerten
- `NEW` Verbesserung des Help-System (Integration des Help-Buttons in das Frontend)
- `NEW` Design-Verbesserungen: Kontrollbereich kann verkleinert und sogar ganz ausgeblendet werden
- `NEW` Debugging in Unterprogrammen erleichtert
- `NEW` Performance-Optimierung (Multithreading) einiger Prüfelemente (z.B. F Farbbinärisierung und F Morphologie)
- `NEW` Tastenkombinationen überarbeitet und erweitert
- `NEW` Erweiterung von FE Bildausgabe um die Möglichkeit, Fenster vor der Bildausgabe in ein Bild zu painten.
- `NEW` Frontend merkt sich den Bildschirm, auf dem es zuletzt geöffnet wurde, und startet direkt auf diesem.
- `FIXED` F Mustersuche stürzte bei nicht validen Eingängen ab.



## Version 6.2

### Version 6.2.11 (07.01.2014)
- `FIXED` Performance-Verbesserungen (gegenüber 6.2.10, welche durch die Speicher-Berücksichtigung langsamer wurde).

### Version 6.2.10 (01.10.2013)

- `CRITICAL` Die Verwaltung der Unterprogramme erfolgt nun bezogen auf den benötigten und verfügbaren Arbeitsspeicher intelligenter.
Dabei wird nun der verfügbare Arbeitsspeicher korrekt ermittelt und der Speicherbedarf der Unterprogramme mitgeloggt.
Dadurch ist eine intelligentere Verwaltung der Unterprogramme möglich, so dass kein Absturz oder Fehler mehr aufgrund von
zu geringen Speicher-Resourcen auftritt.

- `CRITICAL` Wenn ein Block mit Sprüngen auf Marken innerhalb dieses Blocks kopiert und in ein anderes Projekt
eingefügt wurde, haben die Sprünge bislang nicht mehr korrekt funktioniert. Es wurde immer auf das nachfolgende
Prüfelement gesprungen. Dieser Fehler ist jetzt behoben.

- `CRITICAL` Vereinzelt traten Abstürze bei der Verwendung des Prüfelements **I Tinkerforge IO** auf.

- `CRITICAL` Auch die Verwaltung der Offline-Bilder (B Bildaufnahme) erfolgt nun intelligent. Dabei werden für Offlinebilder (je Kamera)
maximal 500MB Arbeitsspeicher zur Verfügung gestellt. Sollte jedoch nicht mehr so viel Arbeitsspeicher verfügbar sein, werden
die Bilder einzeln von der Festplatte geladen.

- `FIXED` Alle Prüfelemente sind nun Schleifenfähig. Vereinzelt gab es Prüfelemente (insbesondere Kreis-Prüfelemente),
welche den Bildinhalt in Schleifen nicht aktualisiert haben. In Zukunft aktualisiert jedes Prüfelement die Bilddaten
bei jedem Durchlauf.

- `FIXED` Endlosschleifen in Unterprogrammen konnten bislang nicht wirklich nachvollzogen werden. Das ändert sich mit der
Version 6.2.10, da in der Statuszeile das aktuell ausgeführte Unterprogramm und das aktuell ausgeführte Prüfelement
angezeigt wird. Dadurch ist es möglich zu erkennen, ob ein Unterprogramm, oder ein einzelnes Prüfelement hängen geblieben ist.
Des weiteren werden jetzt rekursiv alle laufenden Unterprogramme beendet, wenn auf Stopp geklickt wird. Dadurch
wird selbst ein Unterprogramm mit einer Endlosschleife korrekt beendet, ohne dass das Backend neu gestartet werden muss.

- `FIXED` M Fenster und M Bild können nun mit Farbbildern korrekt umgehen.

- `FIXED` Verschiedene kleinere Stabilitäts-Verbesserungen des Frontends.<b id="6.2.9"></b>

- `FIXED` Paralleler Betrieb von Halcon und SIMAVIS P nun möglich, ohne dass Meldungen von Halcon ausgegeben werden.

### Version 6.2.9 (03.07.2013)
- `FIXED` Fernwartung kann direkt aus dem Backend gestartet werden. Bislang hatte der dafür vorgesehene Menüpunkt
keine Auswirkung

- `FIXED` Im Baum des Backends wird jetzt auch korrekt zu dem entsprechenden Prüfelement gesprungen, auch wenn die
Prüfelement-Nummer nur einstellig ist. Wurde bislang beispielsweise eine '3' eingegeben, sprang die Markierung
zum Prüfelement 30.

- `FIXED` Mit der Leertaste können ab sofort alle Lernmodi durchgeschaltet werden. D.h. man kann auch ein schon gelerntes
Prüfelement einfrieren und die Lerndaten verwerfen.

- `FIXED` Wird im Baum des Backends eine Marke markiert, werden alle Sprünge, die auf diese Marke springen ebenfalls
blau hervorgehoben.

- `FIXED` Nach einer Referenzänderung in einem IF-Prüfelement und einem anschließenden Klick auf "Ok" werden die
geänderten Referenzen sofort markiert.

- `FIXED` Die Performance beim Abspeichern von Prüfprogrammen wurde verbessert. Dies wirkt sich besonders dann
aus, wenn eingelernte Prüfelemente verwendet werden.

- `FIXED` F DMC Lesen++ beendet das Backend nun nicht mehr, wenn kein Halcon-Dongle angesteckt ist.

- `FIXED` I Digital IO kann auch nach einem Speichern-Vorgang oder nach Schließen eines Projekts die
Verbindung zu der COM-Schnittstelle erneut aufbauen.

- `FIXED` Das Prüfelement M Bild funktioniert jetzt auch mit Farbbildern korrekt. Bislang war das Ausgangsfenster
nicht korrekt dargestellt worden. Des weiteren wurde die Performance leicht verbessert.

- `FIXED` Das Prüfelement F Fenster positionieren funktioniert jetzt ebenfalls mit Farbbildern korrekt und wurde
beschleunigt.

- `FIXED` Das Prüfelement B Bildformat kann nun mit der Return- oder Escape Taste geschlossen werden. Dabei werden
Änderungen beim drücken der Return-Taste übernommen.

- <b id="6.2.8"></b>`FIXED` Wird während des Video-Betriebs auf Einzeltrigger geklickt, so passierte es manchmal, dass der
Einzeltrigger-Button nicht mehr herausspringt und im Backend trotzdem als Betriebsart "Stopp" angezeigt wurde.

### Version 6.2.8 (21.06.2013)
- `CRITICAL` Speicher-Leak aus D Bild schreiben behoben. Es waren alle Farbbild-Speichervorgänge betroffen.

- <b id="6.2.7"></b>`FIXED` Fehler aus SIMAVIS_UTIL.dll entfernt, der dazu führte, dass in FE Betriebsart als Typ '---' eingelesen wurde,
wenn ganz schnell nach der Einzeltrigger-Bildausgabe FE Betriebsart abgefragt wurde.

### Version 6.2.7 (13.06.2013)
- `FIXED` Fehler behoben, der dazu führte, dass temporäre Sollwerte schon beim nächsten Öffnen des Sollwertfensters
verworfen wurden.

- `FIXED` Fehler in T Text analysieren behoben, bei welchem unter manchen Umständen 2 Zeichen als Subtext zurückgeliefert
wurden, obwohl als Subtext-Länge nur 1 Zeichen angewählt war.

- `FIXED` Werden alle Steuerbuttons vom Backend ausgeblendet, wird der Platz für die Buttonleiste freigegeben,
so dass das Bild größer dargestellt werden kann.

- `FIXED` Es ist nun auch möglich, Steuerbuttons einen leeren Text vorzugeben.<b id="6.2.6"></b>

- `FIXED` Fehler aus M Bild behoben, so dass dieses jetzt auch mit Farbbildern korrekt funktioniert

### Version 6.2.6 (06.06.2013)
- `CRITICAL` Probleme behoben, welche dazu führten, dass keine Kamera-Bildaufnahmen durchgeführt wurden.

- `FIXED` Suche nach M Punkt und M Fenster: Auswahl wird richtig gesetzt und es wird auch richtig gesucht. Vorher
gab es Probleme mit der Suche nach M Punkt, M Fenster und M Bild.

- `FIXED` Tool zur Kamera-Konfiguration in dem Prüfelement B Bildaufnahme funktioniert jetzt auch, wenn keine
Java Runtime Environment auf dem System installiert ist mit dem mitgelieferten JRE des Frontends.

- `FIXED` Wechsel zwischen Software-Trigger und Hardware-Trigger bzw. asynchronen Hardware-Trigger funktioniert jetzt
auch für uEye-Kameras<b id="6.2.5"></b>

- `FIXED` Fehler in T Text analyisieren behoben, bei welchem der Subtext ein Zeichen zu kurz war, wenn über die Textlänge
hinaus gekürzt wurde.

### Version 6.2.5 (29.05.2013)
- `CRITICAL` Fehler aus F Mustersuche entfernt, der zu einem Absturz unter Windows XP führte, sobald
das Prüfelement gelernt war oder gelernt wurde.
Dieser Fehler ist seit der Version 5.4 bis zur Version 6.2.4 enthalten.

- `FIXED` Im Frontend können nun alle Dialoge mit Escape geschlossen werden und werden mittig über dem Frontend
angezeigt.

- `FIXED` Der alte Button "Backend starten" wurde durch das SIMAVIS P Backend-Logo ersetzt und links oben (unterhalb
der Tabs) verschoben.

- `FIXED` Probleme bei der Typvorwahl unter Windows XP behoben.

- `FIXED` Darstellung der Tool-Tip-Texte optimiert.<b id="6.2.4"></b>

- `FIXED` Altes Prüfelement **F Mustersuche** aus Prüfelementevorrat entfernt

### Version 6.2.4 (16.05.2013)
- `FIXED` B Bildformat lädt übergebene Bilder nun intelligent:
Jede Instanz von B Bildformat lädt nur einmalig die übergebenen Bilddaten.
Damit sind alle Debug-Möglichkeiten gegeben, ohne dass
das Prüfelement B Bildformat im Unterprogramm die Bilddaten bei jedem Durchlauf überschreibt.

- `FIXED` Fehler behoben, der dazu führte, dass das Vor- und Zurückschalten (linke bzw.
rechte Maustaste auf Einzeltrigger im Frontend) nicht funktionierte, wenn keine Betriebsart
im Backend abgefangen wurde.

- `FIXED` B Bildaufnahme wird jetzt nur durchlaufen, wenn entweder das Frontend in einer
Triggerbetriebsart ist, oder als B Bildaufnahme-Modus "Kamera initialisieren"
gewählt wurde.
Bisher wurden immer Bilder aufgenommen, die dann aber
nicht ausgegeben wurden (wenn Kamera online war). Im Offline-Modus wurden
die Bilder eingelesen, dann aber nicht in die Leinwand kopiert.

- `FIXED` Offlinepfade im Frontend werden nun auch von FE Bildausgabe zurückgesetzt, wenn
das Frontend nicht in einer Triggerbetriebsart ist. Dadurch werden nicht mehr
mehrere Pfade gleichzeitig (und damit auch falsche) angezeigt!

- `FIXED` Das gleiche gilt ab jetzt auch für Overlays, diese werden ebenfalls bei jedem
erfolgreichem Durchlauf von FE Bildausgabe zurückgesetzt (Status >= 0).

- `FIXED` Auch die Offline-Bild-Richtung (Rechts- oder Linksklick auf Einzeltrigger) wird
zurückgesetzt, wenn der Einzeltrigger oder Lernzyklus Modus zurückgesetzt wird.
Dadurch wird verhindert, dass nach einem Rechtsklick auf Einzeltrigger und
anschließendem Dauertrigger, die Bilder rückwärts durchlaufen werden.
