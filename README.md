
# 💡 Standby-Killer für Steckdosen (Blueprint)

**Version:** 1.0  
**Autor:** Martin 
**Erstellt:** Mai 2025  

Dieser Home Assistant Blueprint schaltet eine smarte Steckdose automatisch aus, wenn der Stromverbrauch über eine frei definierbare Zeit unter einen bestimmten Schwellenwert fällt.

## ✅ Funktionen

- Automatische Abschaltung bei niedrigem Verbrauch (z. B. Standby)
- Einstellbare Wartezeit von 1 bis 24 Stunden (Schieberegler)
- Fehlerprüfung (ignoriert `unavailable` oder `unknown`)
- Manuell aktivierbar/deaktivierbar per `input_boolean`
- Dauerbetrieb-Modus abschaltbar per `input_boolean`

## ⚙️ Voraussetzungen

- Stromsensor (`sensor.*`) mit Watt-Wert
- Schaltbare Steckdose (`switch.*`)
- Zwei `input_boolean` Helfer:
  - `input_boolean.standby_killer_aktiv`
  - `input_boolean.dauerbetrieb_aktiv`

## 📂 Ablage

Lege die YAML-Datei unter:

```
config/blueprints/automation/standby_killer/standby_killer_v1.yaml
```

## 🛠️ Verwendung

1. Gehe in Home Assistant zu **Einstellungen → Automationen & Szenen → Blaupausen**
2. Klicke auf **„Blueprints neu laden“**
3. Erstelle eine neue Automation basierend auf diesem Blueprint
4. Wähle Sensor, Steckdose und Helfer aus
