
# Änderungsprotokoll Plugin MyTado - Beta

# 10.11.2025 - Version 8.0

- Neue Konfigurationsoption des Plugins: Der manuelle Modus kann beim nächsten geplanten Zeitfenster der Zone eines Geräts automatisch wieder aktiviert werden
- Anzeige des nächsten geplanten Zeitfensters und der darin vorgesehenen Temperatur (neue Befehle: „Nächste Programmänderung um“ und „Nächste programmierte Temperatur")

# 30.10.2025 - Version 7.4

- Cron wird jetzt beim Deaktivieren des Plugins entfernt
- Hinzugefügt:
  - Info-Befehl `Status der Verbindung` für Geräte (zeigt den Verbindungsstatus des Geräts)
  - Konfigurationsoption `Tägliche Synchronisation der Geräte` (Konfig-Schlüssel `daily_sync_equipments`), ermöglicht eine automatische tägliche Gerätesynchronisation über den täglichen Cron (standardmäßig aktiviert, wenn Auto-Assist ausgewählt ist)
- Berichtigung:
  - Der Befehl `Status`, der zuvor den Verbindungsstatus anzeigte, meldet jetzt, ob das Gerät aus- oder eingeschaltet ist (je nach ausgewähltem `mode`)
  - Die Erkennung offener Fenster ist zwischen pre-TadoX und TadoX vereinheitlicht (zur Behebung einer API-Inkonsistenz)

# 18.10.2025 - Version 7.3

- Fehlerbehebungen:
  - Der Tagesrekord der API-Aufrufe wird jetzt angezeigt
  - Der Modus „Fenster offen“ sollte jetzt für Geräte vor tadoX funktionieren
- Falls die Tado-API Befehle zum Aktivieren/Deaktivieren des Modus „Fenster offen“ enthält, funktionieren diese trotzdem nicht. Diese Befehle werden daher aus Ihren Geräten entfernt. **Führen Sie unbedingt eine neue Synchronisierung durch, damit sie verschwinden.**

# 08.10.2025 - Version 7.2

- Fehlerbehebung für Widgets von Klimageräten: Der AC-Modus wird jetzt wieder korrekt abgerufen.

# 27.09.2025 - Version 7.1

- **NEU: Täglicher Maximalrekord für API-Aufrufe**: Anzeige des Maximalrekords für API-Aufrufe, die an einem einzigen Tag seit der Installation durchgeführt wurden
- Fehlerbehebungen:
  - Problem mit Swing-Befehlen behoben
  - Änderungen der gewünschten Temperatur funktionieren wieder in den Widgets

# 14.09.2025 - Version 7.0

- **NEU: Intelligente API-Aufruf-Verwaltung aufgrund der Tado-Beschränkungen (September 2025)**
  - Obligatorische Auto-Assist-Konfiguration: Wählen Sie, ob Sie ein Tado Auto-Assist-Abonnement haben
  - Adaptive Beschränkung: 100 Aufrufe/Tag ohne Auto-Assist vs. 20.000 Aufrufe/Tag mit Auto-Assist
  - Echtzeit-API-Aufruf-Zähler in der Konfiguration
  - Automatische Frequenz-Synchronisation entsprechend Ihrem Abonnement
  - Selektive Synchronisationsoptionen (Wetter, Geolokalisierung) zur Optimierung der Aufrufe
  - **Aktion erforderlich: Konfigurieren Sie Ihren Auto-Assist-Modus in der Plugin-Konfiguration**
- Befehl zur Erkennung eines offenen Fensters hinzugefügt. **Achtung: Abhängigkeiten müssen aktualisiert und die Synchronisierung erneut durchgeführt werden.**
- Der Befehl **Gewünschte Temperatur einstellen** ist jetzt vom Untertyp *Schieberegler*. **Achtung: Dies wirkt sich auf Szenarien aus, daher ist eine Anpassung nach dem Update erforderlich.**
- Hinzugefügt: Unterscheidung zwischen relativer Entfernung und berechneter Entfernung für Benutzerausstattungen (neuer Befehl)
- Vereinfachung der Befehlsverwaltung für mehr Flexibilität in der Zukunft.
- Plugin in die Kategorie „Komfort" verschoben.

# 05.04.2025 - Version 6.2

- Fehler bei der Synchronisierung behoben (eingeführt in Version 6.0)  

# 01.04.2025 - Version 6.1

- Fehler bei der Erstellung von Befehlen für ein neues Haus behoben (eingeführt in Version 6.0)  

# 23.03.2025 - Version 6.0

- Anpassung der Verbindung zu Tado aufgrund der API-Änderung vom 21.03.2025  

# 19.03.2025 - Version 5.1

- Neuanordnung der Anzeige auf der Geräteeinstellungsseite  
- Problem mit der Synchronisierung bei einer Neuinstallation des Plugins behoben  
- Bildanzeige für Geräte des Modells RU02B korrigiert (RU02 verwaltet Thermostat und Warmwasser)  

# 09.03.2025 - Version 5.0

- Überarbeitung der Verwaltung der Gerätekonfigurationen für mehr Flexibilität in der Zukunft, unabhängig von den Plugin-Versionen.
- Hinzufügen von **Benutzer**-Geräten, um detaillierte Informationen über die Standorte der Tado-Benutzer für Ihre Szenarien zu erhalten.
- Es ist jetzt möglich, Benutzerbilder anzupassen, die auf dem **Haus**-Widget bei Anwesenheit angezeigt werden.
- Möglichkeit, die Aktualisierungsfrequenz der Daten zu wählen.

# 20.02.2025 - Version 4.1

- Für **TadoX**-Geräte wird jetzt die **vom Gerät gemessene Temperatur** angezeigt (und nicht mehr die der Zone).
- Das **Tado Home-Widget** zeigt nun **die Anzahl der anwesenden Personen** an.

# 16.02.2025 - Version 4.0

- Der Dämon basiert nun auf dem JeedomDaemon-Modul von Mips, das alle Speicherlecks behebt.
- Das Hausequipment hat eine neue Aktion, mit der festgestellt werden kann, wie viele Benutzer zu Hause sind.
- Objekte mit mehreren Rollen (z. B.: Heizkessel- und Warmwassersteuerung) werden jetzt durch ein Gerät pro Funktion dargestellt.
- Die Parameter der Aktionen sind jetzt bei Befehlsprüfungen und in Szenarien verfügbar.

# 19.01.2025 - Version 3.1


- Die möglichen Werte der verschiedenen Parameter für Klimaanlagenmodule werden jetzt dynamisch abgerufen.  
- Behebung eines Problems beim Abrufen des Status eines TadoX-Geräts, wenn es sich im manuellen Modus für eine bestimmte Dauer befindet.  
- Aktualisierung der Dokumentation, um die Verwaltung von Szenarien mit MyTado zu beschreiben.

# 12.2024 - Version 3.0

- TadoX-Geräte werden jetzt unterstützt
- Wetter wird in ein Zuhause umgewandelt und die Verbindungskonfiguration wurde auf dieses "Zuhause"-Gerät verlagert
- Es ist möglich, mehrere Häuser zu konfigurieren, falls man sowohl Tado- als auch TadoX-Geräte besitzt (was zwei separate Häuser erfordert)
- 4 neuen Befehlen für Tado(X)-Geräte hinzugefügt: Aktivieren, Deaktivieren, Datum des letzten Daten-Updates und Batteriestand

# 11.2024 - Version 2.0

- Die Verwaltung der Verbindung zu Tado verwendet jetzt einen Daemon, um Latenzzeiten in PHP zu vermeiden

# 30.10.2024 - Version 1.6

- Fehler bei der Abfrage der Fähigkeiten eines Objekts vom Typ AC führen nicht mehr dazu, dass die Abfrage anderer Geräten blockiert wird

# 17.10.2024 - Version 1.5

- Die Heizleistung wird nun für RU0X-Geräte erfasst und angezeigt
- Es ist jetzt möglich, die Standardbenennung Ihrer Geräte zu ändern
- Spanische Übersetzung jetzt verfügbar

# 13.10.2024 - Version 1.4

- Fehlerbehebung: Standardname der Wetterbefehle sichergestellt
- Verschiedene Versionen desselben Typs eines bekannten Objektmodells sind nun auf die gleiche Weise konfiguriert

# 25.05.2024 - Version 1.3

- Klimaanlagen- und Kochgeräte werden nun verwaltet
- Übersetzung ins Deutsche hinzugefügt

# 08.05.2024 - Version 1.2

- Befehle zum Aktivieren/Deaktivieren durch Modusinformationen und Setzen des Modus ersetzt
- Geräte-Widget entsprechend aktualisiert

# 05.05.2024 - Version 1.1

- Neue Befehle zum Aktivieren/Deaktivieren von Geräten sowie zum manuellen Einstellen der Zieltemperatur
- Erste Versionen der Widgets

# 25.04.2024 - Version 1.0

- Erste stabile Version