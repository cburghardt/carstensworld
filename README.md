# ESPHome Configs

ESPHome Konfigurationen für meine Smart Home Projekte aus dem YouTube Kanal **Carsten's World**.

## 📁 Projekte

### E-Ink Display (Xiao 7.5")
- **Hardware:** Seeed Studio Xiao ESP32 + 7.5" E-Paper Display
- **Video:** https://youtu.be/-BWdE85hcqw
- **Files:** `eink-display/`

## 🚀 Quick Start

1. **Repository klonen:**
   ```bash
   git clone https://github.com/cburghardt/carstensworld.git
   cd carstensworld
   ```

2. **Secrets einrichten:**
   ```bash
   cp eink-display/secrets.example.yaml eink-display/secrets.yaml
   # Bearbeite secrets.yaml mit deinen Werten
   ```

3. **In ESPHome einbinden:**
   - ESPHome Dashboard → New Device → Import existing YAML
   - Oder per CLI: `esphome run eink-display/xiao-epaper.yaml`

4. **Auf ESP32 flashen:**
   - USB anschließen
   - In ESPHome Dashboard auf "Install" klicken

## 🔒 Secrets

Die Datei `secrets.yaml` enthält sensible Daten (WiFi, API Keys) und ist in `.gitignore` eingetragen. **Niemals committen!**

Verwende `secrets.example.yaml` als Template mit Platzhaltern.

## 📺 YouTube Kanal

Besuche [Carsten's World](https://youtube.com/@carstensworld) für Videos zu:
- Home Assistant Integrationen
- ESPHome Projekte
- Smart Home Automation mit AI

## 📄 Lizenz

MIT License - Siehe [LICENSE](LICENSE)

---

**Happy Hacking! 🤖**
