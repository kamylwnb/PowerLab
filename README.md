# ⚡ PowerLab v6.5

**Professional Power Supply Control & Diagnostics System**

> Autor: **Dr.Mosfet**

---

## 📋 Opis

PowerLab to zaawansowana aplikacja do sterowania i monitorowania zasilaczy laboratoryjnych przez port szeregowy (RS485/Modbus RTU).

### ✨ Funkcje

- 📊 **Wykresy live** — napięcie i prąd w czasie rzeczywistym
- ⚡ **Sterowanie napięciem i prądem** — precyzyjna regulacja
- 🎯 **Profile szybkiego dostępu** — 3.3V / 5V / 12V / 24V / MAX
- 🔌 **Auto-detekcja portów COM**
- 🌑 **Dark theme** — styl laboratoryjny

---

## 🚀 Uruchomienie

Pobierz `PowerLab.exe` z zakładki [Releases](../../releases) i uruchom — **nie wymaga instalacji Pythona**.

### Wymagania sprzętowe
- Zasilacz z interfejsem RS485 / Modbus RTU
- Konwerter USB→RS485

---

## 🖥️ Screenshot

```
┌─────────────────────────────────────────┐
│  POWERLAB CONTROL   │  Wykres V live    │
│  Port: COM3         │  ───/\/\/\───     │
│  [POŁĄCZ]           │                   │
│  Napięcie: 12.00 V  │  Wykres I live    │
│  Prąd:      2.500 A │  ───────────      │
│  Moc:      30.00 W  │                   │
└─────────────────────────────────────────┘
```

---

## 📡 Protokół

Modbus RTU @ 9600 baud, adresy rejestrów:
| Rejestr | Opis |
|---------|------|
| 0x0001 | Napięcie zadane |
| 0x0003 | Prąd zadany |
| 0x001D | Napięcie aktualne |
| 0x001F | Prąd aktualny |

---

*PowerLab v6.5 © 2026 Dr.Mosfet*
