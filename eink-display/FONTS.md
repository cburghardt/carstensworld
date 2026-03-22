# Fonts für E-Ink Display

Diese Datei erklärt wie du die benötigten Font-Dateien für das ESPHome-Projekt erhältst.

## Benötigte Fonts

1. **Montserrat-Black.ttf** - Haupt-Font für Labels und Temperaturen
2. **materialdesignicons-webfont.ttf** - Icons für Wetter, Personen, etc.

## Option A: Fonts lokal speichern (empfohlen für Production)

### Montserrat von Google Fonts herunterladen:

1. Gehe zu https://fonts.google.com/specimen/Montserrat
2. Klicke auf "Download family" (oben rechts)
3. Entpacke das ZIP
4. Kopiere `Montserrat-Black.ttf` (Weight 900) in den `fonts/` Ordner

### Material Design Icons herunterladen:

1. Gehe zu https://github.com/Templarian/MaterialDesign-Font
2. Lade die `materialdesignicons-webfont.ttf` herunter
3. Kopiere sie in den `fonts/` Ordner

### Ordnerstruktur:
```
eink-display/
├── xiao-epaper.yaml
├── secrets.example.yaml
└── fonts/
    ├── Montserrat-Black.ttf
    └── materialdesignicons-webfont.ttf
```

## Option B: Google Fonts direkt nutzen (einfacher für Tests)

Ändere in der `xiao-epaper.yaml`:

```yaml
# Statt lokaler Datei:
font:
  - file: "gfonts://Montserrat"
    id: data_font
    size: 38
    weight: 900  # Black
```

**Vorteil:** Keine Dateien nötig  
**Nachteil:** Braucht Internetverbindung beim ESPHome-Compile

## Option C: Fonts im Repo mitliefern

⚠️ **Achtung:** Font-Dateien können groß sein (~500KB jede). Für GitHub Repos:

- ✅ OK wenn < 10MB insgesamt
- ⚠️ Git LFS empfohlen für größere Dateien

Wenn du die Fonts im Repo mitliefern willst:

```bash
cd eink-display
mkdir fonts
# Fonts hierhin kopieren
git add fonts/
git commit -m "Add font files"
git push
```

---

## Quick Test

Nachdem Fonts vorhanden sind:

```bash
esphome compile eink-display/xiao-epaper.yaml
```

Wenn es ohne Fehler durchläuft → Fonts sind korrekt! ✅
