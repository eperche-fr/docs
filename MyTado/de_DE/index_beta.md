# <img src="../images/MyTado_icon.png" width="60"/> Plugin MyTado

Das **MyTado** Plugin ermöglicht das Abrufen von Daten Ihrer verbundenen Tado und Tado X Geräte sowie Wetterinformationen, die von Tado verwaltet werden.

Die Daten werden alle 30 Minuten aktualisiert.

>**Unterstützte Geräte**
>
>Derzeit werden nur die Modelle BU0X, BP0, BR0X, CK04, RU0X, SU0X, VA0X und WR0X vollständig unterstützt (unabhängig von ihrer Version).
>Wenn Sie Probleme mit nicht unterstützten Geräten oder mit einem der aufgeführten Geräte haben, folgen Sie bitte den Anweisungen im Abschnitt [Bei Problemen](#bei-problemen).

# Konfiguration

## Plugin Konfiguration

Gehen Sie zuerst zur Plugin-Konfiguration.
Stellen Sie sicher, dass die Abhängigkeiten installiert und der Daemon gestartet sind.
Wenn Sie den Daemon nicht starten können, ist der Standardport (59969) möglicherweise bereits belegt.
In diesem Fall legen Sie in der Konfigurationssektion einen verfügbaren Port fest, speichern und versuchen Sie den Daemon erneut zu starten.
Wenn das Problem weiterhin besteht, folgen Sie den Anweisungen im Abschnitt [Bei Problemen](#bei-problemen).

Optional können Sie auch die folgenden zwei Parameter ändern:
1. Die anzuzeigende Temperatureinheit. **Celsius ist die Standardeinheit**.
2. Das Namensschema für Ihre Geräte.

Sobald der Daemon läuft, schließen Sie die Konfigurationsseite, um zur Hauptseite des Plugins zurückzukehren, und folgen Sie diesen Schritten:
1. Klicken Sie auf "Haus hinzufügen".
2. Geben Sie Ihrem Haus einen Namen (der Name muss nicht mit dem in Tado übereinstimmen) und klicken Sie dann auf "Ok".
3. Geben Sie die drei Informationen zu Ihrem Tado-Konto ein:
    - Die E-Mail-Adresse, die Sie zur Erstellung Ihres Tado-Kontos verwendet haben.
    - Ihr Tado-Konto Passwort.
    - Den genauen Namen (Groß- und Kleinschreibung beachten) Ihres Hauses in der Tado-App.
4. Speichern Sie Ihr Haus.

Wenn die Informationen korrekt sind, werden zusätzliche Details zu Ihrem Haus hinzugefügt und Tado- oder TadoX-Geräte (je nach Ihrem Haus) werden innerhalb weniger Sekunden synchronisiert.
Schließen Sie das Haus, um zu überprüfen, ob Ihre Geräte erscheinen.
Wenn nach einigen Sekunden nichts passiert, aktualisieren Sie die Seite manuell.
Wenn Ihre Geräte nicht angezeigt werden, überprüfen Sie die Protokolle, um festzustellen, ob Sie das Problem selbst beheben können.
Andernfalls folgen Sie den Anweisungen im Abschnitt [Bei Problemen](#bei-problemen).

Schließlich, wenn Sie Geräte zu Ihrem Tado/TadoX-Haus hinzufügen, verwenden Sie die **Synchronisierung**-Schaltfläche, um sie abzurufen.

>**INFORMATION**
>
>Wenn Sie sowohl Tado- als auch TadoX-Geräte besitzen, haben Sie zwei Häuser. Sie müssen für jedes Ihrer Tado-Konten ein Haus erstellen.
>Alle Geräte werden unabhängig davon, aus welchem Haus sie stammen, aufgelistet.

## Gerätekonfiguration

>**ERINNERUNG**
>
>Verwenden Sie einfach den **Synchronisierung**-Befehl, um neue verbundene Geräte abzurufen, die zu Ihrem Tado-Haus hinzugefügt wurden, oder nach einem Plugin-Update, das einen neuen Gerätetyp unterstützt, den Sie besitzen.

### Ihre verbundenen Tado-Geräte
<img src="../images/WR0X.png" width="60"/><img src="../images/BU0X.png" width="60"/><img src="../images/RU0X.png" width="60"/><img src="../images/VA0X.png" width="60"/><img src="../images/VA04.png" width="60"/><img src="../images/RU04.png" width="60"/><img src="../images/CK04.png" width="60"/>

Wenn Sie auf ein verbundenes Tado-Gerät klicken, gelangen Sie direkt zu seiner Konfigurationsseite:

- **Gerätename**: Name des Geräts basierend auf seiner Seriennummer.
- **Übergeordnetes Objekt**: Gibt das übergeordnete Objekt an, zu dem das Gerät gehört. Dies definieren Sie.
- **Kategorie**: Ermöglicht die Auswahl der Kategorie des Geräts.

Wenn Sie auf den **Befehle**-Tab klicken, wird eine Liste aller verfügbaren Befehle und die Möglichkeit zur Protokollierung numerischer Werte angezeigt.
Die Daten werden alle 30 Minuten aktualisiert, aber Sie können mit dem **Aktualisieren**-Befehl eine Aktualisierung auf Abruf erzwingen.

Im Dashboard zeigt das Widget das Bild an, das Ihrem Gerät entspricht, sowie die aktuellen Informationen und Konfigurationen.
Sie können auch den Betriebsmodus Ihres Geräts festlegen:
- 'Autonom': Der auf der Tado-App erstellte Zeitplan wird angewendet;
- 'Manuell': Ermöglicht das Verlassen des automatischen Modus und das Festlegen der Parameter Ihrer Wahl;
- 'Aus': Das Gerät ist vollständig ausgeschaltet.

>**Wichtige Information**
>
>Im Falle einer manuellen Temperaturänderung wird diese auf alle Geräte in derselben Zone wie Ihr Gerät angewendet (so funktioniert Tado).

### Tado Haus <img src="../images/HomeEq.svg" width="60"/>

Wenn Sie auf Ihr Tado-Haus klicken, gelangen Sie direkt zu seiner Konfigurationsseite:

- **Gerätename**: Name, den Sie Ihrem Haus in Jeedom gegeben haben.
- **Übergeordnetes Objekt**: Gibt das übergeordnete Objekt an, zu dem das Gerät gehört. Dies definieren Sie.
- **Kategorie**: Ermöglicht die Auswahl der Kategorie des Geräts.
- **Breitengrad**: In Tado für Ihr Haus referenzierter Breitengrad, der zur Abrufung des entsprechenden Wetters verwendet wird.
- **Längengrad**: In Tado für Ihr Haus referenzierter Längengrad, der zur Abrufung des entsprechenden Wetters verwendet wird.

Sowie Ihre Tado-Anmeldeinformationen für dieses Haus (vergessen Sie nicht, Ihr Passwort hier zu ändern, wenn Sie es auf der Tado-Website ändern!).

Wenn Sie auf den **Befehle**-Tab klicken, wird eine Liste aller verfügbaren Befehle und die Möglichkeit zur Protokollierung numerischer Werte und des Wetterzustands angezeigt.
Die Daten werden alle 30 Minuten aktualisiert, aber Sie können mit dem **Aktualisieren**-Befehl eine Aktualisierung auf Abruf erzwingen (beachten Sie, dass dies die Aktualisierung der Wetterdaten sowie aller Geräte, die zu diesem Haus gehören, erzwingt).

Das Widget zeigt das Wetter in Form eines Bildes sowie die aktuelle Temperatur und Helligkeit an.

### Szenarien verwalten

Verschiedene Befehle erfordern einen oder mehrere Parameter. Bis eine zukünftige Version von MyTado verfügbar ist, die es ermöglicht, die gewünschten Parameter direkt einzugeben oder auszuwählen, müssen Sie die JSON-Version der Szenarien verwenden, um den gewünschten Parameter zu übermitteln (Schaltfläche „Textbearbeitung“ in der Befehlskonfiguration des Szenarios).  
> **ACHTUNG**  
> Änderungen an Ihrem Szenario sollten nur über die Schaltfläche im JSON-Bearbeitungsmodus gespeichert werden, da Sie sonst Ihre spezifischen Optionen verlieren.

Mit MyTado wird dringend empfohlen, in Ihren Szenarien nur die folgenden Befehle zu verwenden:  
- **„aktivieren“**: Schaltet Ihr Modul in den „AUTO“-Modus.  
- **„deaktivieren“**: Schaltet Ihr Modul aus.  
- **„Modus ändern“**: Ermöglicht insbesondere das Umschalten in den manuellen Modus und das Festlegen anderer Parameter, die Sie ändern möchten.

**Wie wird der Befehl „Modus ändern“ verwendet?**  

Fügen Sie in den Optionen den Schlüssel `mode` mit dem Wert `MANUAL` hinzu.  
Um die gewünschte Temperatur zu ändern, verwenden Sie den Schlüssel `expected_temperature` gefolgt von der gewünschten Temperatur (der Punkt wird als Dezimaltrennzeichen verwendet).  
Für Klimaanlagen geben Sie den gewünschten Wert **in Großbuchstaben** an (verfügbare Werte finden Sie im Widget), und zwar in Kombination mit einem der folgenden Schlüssel:  
- `AC_mode`  
- `fan_speed`  
- `vertical_swing_mode`  
- `horizontal_swing_mode`

> Beispiel für das Feld `options` für ein Thermostatventil:  
> ```json
> "options": {
>     "mode": "MANUAL",
>     "expected_temperature": "17.5",
>     "enable": "1",
>     "background": "0"
> }
> ```

> Beispiel für das Feld `options` für ein Klimamodul:  
> ```json
> "options": {
>     "mode": "MANUAL",
>     "expected_temperature": "17.5",
>     "AC_mode": "HEAT",
>     "enable": "1",
>     "background": "0"
> }
> ```

### Bei Problemen

Kontaktieren Sie den Entwickler und geben Sie die Modelle Ihrer Tado-/TadoX-Geräte, fehlende Funktionen oder bestehende Probleme sowie alle relevanten Informationen an.  
Vergessen Sie nicht, die Protokolle des Plugins und des Daemons bereitzustellen (achten Sie darauf, persönliche Daten zu anonymisieren).
