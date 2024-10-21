# <img src="../images/MyTado_icon.png" width="60"/> Plugin MyTado

Das **MyTado**-Plugin ruft alle Ihre verbundenen Tado-Geräte sowie die von Tado gesammelten Wetterdaten ab.

Die Daten werden alle 30 Minuten aktualisiert.

>**Verwaltete Geräte**
>
>Geräte der Modelle AC0X, BU0X, RU0X und VA0X werden vollständig unterstützt (normalerweise unabhängig von der Version, die Sie haben). 
>Für andere Modelle sind nur die Grundfunktionen verfügbar (Zugriff auf die gemessene Temperatur, Ein-/Ausschalten/Automatik, Datenaktualisierung). Für alle nicht aufgeführten Geräte kontaktieren Sie bitte den Entwickler und geben Sie an, welches Modell Sie haben, welche Funktionen Ihnen fehlen und alle weiteren Informationen, die Sie für relevant halten.

# Konfiguration

## Plugin-Konfiguration

Sie müssen die folgenden 3 Felder angeben:
1. Die E-Mail-Adresse, die Sie zur Erstellung Ihres Tado-Kontos verwendet haben.
2. Das von Ihnen definierte Passwort.
3. Ihren genauen Hausnamen in der Tado-App (Groß-/Kleinschreibung beachten).

Die Temperatureinheit ist optional, **das Plugin verwendet jedoch standardmäßig Celsius**.
Dasselbe gilt für die Benennungskonvention Ihrer Geräte.

Nach dem Speichern der Konfiguration klicken Sie bitte auf die **Synchronisations-Schaltfläche**, um alle Ihre Geräte zu laden.

## Gerätekonfiguration

>**INFORMATION**
>
>Sie müssen lediglich den Befehl **Synchronisierung** ausführen, um alle Ihre Tado-Objekte sowie das Gerät zur Abfrage der von Tado gesammelten Wetterdaten aufzulisten.

### Ihre Tado-Geräte  <img src="../images/AC01.png" width="60"/><img src="../images/BU01.png" width="60"/><img src="../images/RU01.png" width="60"/><img src="../images/VA01.png" width="60"/>

Durch Klicken auf ein Tado-Objekt gelangen Sie zu seiner Konfigurationsseite:

- **Gerätename** : Der Name des Objekts basierend auf seiner Seriennummer.
- **Übergeordnetes Objekt** : Zeigt das übergeordnete Objekt an, dem Ihr Gerät angehört. Sie können es definieren.
- **Kategorie** : Ermöglicht die Auswahl der Kategorie Ihres Geräts.

Durch Klicken auf die Registerkarte **Befehle** finden Sie alle verfügbaren Befehle sowie die Option zum Historisieren numerischer Werte.
Ihre Daten werden alle 30 Minuten automatisch aktualisiert, jedoch können Sie die Aktualisierung mit dem Befehl **Aktualisieren** erzwingen.

Das Widget zeigt das Bild Ihres Geräts sowie seine Grunddaten an.
Sie können auch den Modus Ihres Geräts definieren:
- 'Autonom': Der Zeitplan, den Sie in der Tado-App festgelegt haben, wird berücksichtigt;
- 'Manuell': Ermöglicht das manuelle Festlegen einer oder mehrerer Einstellungen, abhängig von den Fähigkeiten Ihres Geräts;
- 'Aus': Ihr Gerät ist gestoppt.

>**Wichtiger Aspekt**
>
>Wenn Sie die erwartete Temperatur manuell einstellen, beachten Sie, dass alle Ihre Geräte, die sich in derselben Zone befinden, entsprechend dieser Einstellung ausgerichtet werden (so funktioniert Tado, keine Umgehung möglich).

### Wetter zu Hause <img src="../images/WeatherEq.svg" width="60"/>

Durch Klicken auf das Gerät **Wetter zu Hause** gelangen Sie zu seiner Konfigurationsseite:

- **Gerätename** : Der Standardname dieses Geräts.
- **Übergeordnetes Objekt** : Zeigt das übergeordnete Objekt an, dem Ihr Gerät angehört. Sie können es definieren.
- **Kategorie** : Ermöglicht die Auswahl der Kategorie Ihres Geräts.
- **Breitengrad** : Breitengrad, der bei Tado für Ihr Zuhause festgelegt ist und zur Abfrage Ihrer Wetterdaten verwendet wird.
- **Längengrad** : Längengrad, der bei Tado für Ihr Zuhause festgelegt ist und zur Abfrage Ihrer Wetterdaten verwendet wird.

Durch Klicken auf die Registerkarte **Befehle** finden Sie alle verfügbaren Befehle sowie die Option zum Historisieren aller numerischen Werte und des Wetters.
Ihre Daten werden alle 30 Minuten automatisch aktualisiert, jedoch können Sie die Aktualisierung mit dem Befehl **Aktualisieren** erzwingen.

Das Widget zeigt ein Bild des aktuellen Wetterzustands und zeigt die aktuelle Temperatur und Sonnenintensität an.