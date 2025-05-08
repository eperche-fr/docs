# <img src="../images/MyHeatzy_icon.png" width="60"/> MyHeatzy-Plugin

Das **MyHeatzy**-Plugin ermöglicht den Abruf von Daten Ihrer verbundenen Heatzy-Geräte.

Die Daten werden regelmäßig entsprechend dem gewählten Cron-Intervall aktualisiert (zwischen 5 und 30 Minuten).

---

> **Unterstützte Geräte**
>
> Derzeit werden nur die Modelle Pilote und Glow vollständig unterstützt (unabhängig von ihrer Version).
> Bei nicht unterstützten Geräten oder Problemen mit unterstützten Geräten folgen Sie bitte dem Abschnitt [Bei Problemen](#bei-problemen).

---

# Konfiguration

## Plugin-Konfiguration

1. Gehen Sie zur Plugin-Konfiguration.
2. Installieren Sie die Abhängigkeiten.
3. Starten Sie den Daemon.

Wenn der Daemon nicht startet, ist der Standardport (59769) möglicherweise bereits belegt. Wählen Sie in diesem Fall einen freien Port (z. B. 59770), speichern Sie und starten Sie den Daemon neu. Besteht das Problem weiterhin, siehe [Bei Problemen](#bei-problemen).

Folgende Informationen müssen angegeben und gespeichert werden:
- Ihre Heatzy-Benutzerkennung.
- Ihr Heatzy-Passwort.
- Aktualisierungsfrequenz: cron 5, 10, 15 oder 30 Minuten (nur ein Cron aktiv lassen). Der tägliche Cron muss ebenfalls aktiv bleiben.

Nach erfolgreicher Eingabe werden die Geräte automatisch synchronisiert. Schließen Sie die Konfiguration. Falls Ihre Geräte nicht angezeigt werden, aktualisieren Sie die Seite oder prüfen Sie die Logs.

## Geräte-Konfiguration

> **ERINNERUNG**
>
> Verwenden Sie den Befehl **Synchronisieren**, um neue oder neu unterstützte Geräte zu laden.

### Verbundene Heatzy-Geräte
<img src="../images/Pilote.png" width="60"/><img src="../images/Glow.png" width="60"/>

Ein Klick auf ein Heatzy-Gerät zeigt:

- **Gerätename**: Name aus der Heatzy-App.
- **Übergeordnetes Objekt**: Nach Ihrer Organisation definieren.
- **Kategorie**: Wählen Sie die passende Kategorie.

**Befehle**-Reiter:
- Liste verfügbarer Befehle.
- Möglichkeit zur Historisierung numerischer Werte.
- Manueller Refresh über **Aktualisieren**-Befehl.

Im Dashboard zeigt das Widget das Gerätesymbol, Informationen und aktuelle Konfiguration.

Verfügbare Modi:
- **Komfort**
- **Eco**
- **Frostschutz**
- **Aus**

Je nach Gerät:
- Boost-Modus aktivieren
- Urlaubsmodus aktivieren
- Wunschtemperatur einstellen (vorher auf Komfort oder Eco wechseln)
- Zeitsteuerung aktivieren/deaktivieren

---

# Szenarien verwalten

Wechseln Sie unbedingt in den Eco- oder Komfortmodus, bevor Sie in Szenarien eine Temperatur setzen! (Nur bei bestimmten Geräten verfügbar.)

---

# Bei Problemen

1. Setzen Sie die **MyHeatzy**-Logs auf **Debug**.
2. Starten Sie den Daemon neu.
