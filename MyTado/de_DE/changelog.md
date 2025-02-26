# Änderungsprotokoll Plugin MyTado - Beta

# 20.02.2025 - Version 4.1

- Für **TadoX**-Geräte wird jetzt die **vom Gerät gemessene Temperatur** angezeigt (und nicht mehr die der Zone).
- Das **Tado Home-Widget** zeigt nun **die Anzahl der anwesenden Personen** an.

# 16.02.2025 - Version 4.0

- Der Dämon basiert nun auf dem JeedomDaemon-Modul von Mips, das alle Speicherlecks behebt.
- Das Hausequipment hat eine neue Aktion, mit der festgestellt werden kann, wie viele Benutzer zu Hause sind.
- Objekte mit mehreren Rollen (z. B.: Heizkessel- und Warmwassersteuerung) werden jetzt durch ein Gerät pro Funktion dargestellt.
- Die Parameter der Aktionen sind jetzt bei Befehlsprüfungen und in Szenarien verfügbar.

# 01.2025 - Version 3.1

- Die möglichen Werte der verschiedenen Parameter für Klimaanlagenmodule werden jetzt dynamisch abgerufen.  
- Behebung eines Problems beim Abrufen des Status eines TadoX-Geräts, wenn es sich im manuellen Modus für eine bestimmte Dauer befindet.  
- Aktualisierung der Dokumentation, um die Verwaltung von Szenarien mit MyTado zu beschreiben.

# 12.2024 - Version 3.0

- TadoX-Geräte werden jetzt unterstützt
- Wetter wird in ein Zuhause umgewandelt und die Verbindungskonfiguration wurde auf dieses "Zuhause"-Gerät verlagert
- Es ist möglich, mehrere Häuser zu konfigurieren, falls man sowohl Tado- als auch TadoX-Geräte besitzt (was zwei separate Häuser erfordert)
- 4 neuen Befehlen für Tado(X)-Geräte hinzugefügt: Aktivieren, Deaktivieren, Datum des letzten Daten-Updates und Batteriestand
- Die Verwaltung der Verbindung zu Tado verwendet jetzt einen Daemon, um Latenzzeiten in PHP zu vermeiden

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