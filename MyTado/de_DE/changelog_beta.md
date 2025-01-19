# Änderungsprotokoll Plugin MyTado - Beta

# 01/2025 - Version 3.1

- Behebung eines Problems beim Abrufen von Klimamodulen, wenn diese ausgeschaltet sind  
- Behebung eines Problems beim Abrufen des Zustands eines TadoX-Geräts, wenn es sich für eine festgelegte Dauer im manuellen Modus befindet  

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