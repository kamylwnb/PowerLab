<div align="center">

# ⚡ PowerLab v6.5

**Professional Power Supply Control & Diagnostics System**

[![Version](https://img.shields.io/badge/version-6.5-00ccff?style=for-the-badge)](https://github.com/kamylwnb/PowerLab/releases)
[![Platform](https://img.shields.io/badge/platform-Windows-0078d4?style=for-the-badge&logo=windows)](https://github.com/kamylwnb/PowerLab/releases)
[![License](https://img.shields.io/badge/license-MIT-00ffcc?style=for-the-badge)](LICENSE)
[![Author](https://img.shields.io/badge/author-Dr.Mosfet-ff5555?style=for-the-badge)](https://github.com/kamylwnb)

</div>

---

## 🖥️ O aplikacji

**PowerLab** to aplikacja desktopowa do **sterowania i monitorowania zasilaczy laboratoryjnych** przez interfejs RS232/Modbus RTU.PowerLab to zaawansowana aplikacja do sterowania i monitorowania zasilaczy laboratoryjnych poprzez port szeregowy (RS485/Modbus RTU). Interfejs graficzny (GUI) został przygotowany przy wsparciu AI, ponieważ nie czuję się najlepiej w Pythonie – moim ulubionym środowiskiem jest C oraz Asembler, więc preferuję podejście terminalowe. Mam jednak nadzieję, że to nie przeszkadza; cała analiza protokołu oraz logika "pod maską" zostały napisane przeze mnie ręcznie.

```
┌─────────────────────┬──────────────────────────────────┐
│  ⚡ POWERLAB CTRL   │   Napięcie [V]                   │
│                     │   ▁▂▄▆█▆▄▂▁  12.00 V            │
│  Port:  COM3  ▼     │                                  │
│  [ POŁĄCZ ]         ├──────────────────────────────────┤
│                     │   Prąd [A]                       │
│  Napięcie [V]       │   ▁▁▂▂▃▃▂▂▁  2.500 A            │
│  ┌──────────────┐   │                                  │
│  │   12.00      │   └──────────────────────────────────┘
│  └──────────────┘
│  Prąd [A]           │  ██████ 12.00 V
│  ┌──────────────┐   │  ██████  2.500 A
│  │    2.500     │   │  ██████ 30.00 W
│  └──────────────┘   │
│  [ ZASTOSUJ ]       │
│                     │
│  ── PROFILE ──      │
│  3.3V (MCU)         │
│  5.0V (USB)         │
│  12.0V (Auto)       │
│  24.0V (Ind)        │
│  MAX POWER          │
└─────────────────────┘
```

---

## ✨ Funkcje

| Funkcja | Opis |
|---------|------|
| 📊 **Live wykresy** | Napięcie i prąd rysowane w czasie rzeczywistym (100 próbek) |
| ⚡ **Precyzyjna regulacja** | Ustawianie napięcia (0–32V) i prądu (0–10A) |
| 🎯 **Profile jednym klikiem** | 3.3V / 5V / 12V / 24V / MAX POWER |
| 🔌 **Auto-detekcja COM** | Automatyczne wykrywanie portów szeregowych |
| 📟 **Konsola debug** | Log komunikacji Modbus w czasie rzeczywistym |
| 🌑 **Dark theme** | Profesjonalny wygląd w stylu laboratoryjnym |

---

## 🚀 Pobieranie i uruchomienie

### ⬇️ Gotowy plik EXE (zalecane)

> **Nie wymaga instalacji Pythona ani żadnych bibliotek!**

1. Przejdź do zakładki **[Releases](https://github.com/kamylwnb/PowerLab/releases)**
2. Pobierz `PowerLab.exe`
3. Uruchom dwuklikiem ✅

---

## 🔌 Podłączenie sprzętu

```
[Zasilacz RS232] ──── [Konwerter USB→RS232] ──── [PC / Laptop]
                                                        │
                                                   PowerLab.exe
```

### Wymagania
- Zasilacz z interfejsem **RS232 / Modbus RTU**
- Konwerter **USB → RS232** (CH340, FT232, CP2102)
- System: **Windows 10/11** (64-bit)

---

## 📡 Protokół Modbus RTU over RS232

**Baud:** 9600 | **Parity:** None | **Stop bits:** 1 | **Address:** 0x01

| Rejestr | Typ | Opis |
|---------|-----|------|
| `0x0001` | Float | Napięcie zadane [V] |
| `0x0003` | Float | Prąd zadany [A] |
| `0x001D` | Float | Napięcie aktualne [V] |
| `0x001F` | Float | Prąd aktualny [A] |

---

## 📊 Parametry techniczne

| Parametr | Wartość |
|----------|---------|
| Maks. napięcie | 32.0 V |
| Maks. prąd | 10.0 A |
| Maks. moc | 320 W |
| Częstotliwość odczytu | 5 Hz (co 200ms) |
| Historia wykresu | 100 próbek |

---

## 🛠️ Technologie

![Python](https://img.shields.io/badge/Python-3.10-3776ab?style=flat-square&logo=python&logoColor=white)
![Tkinter](https://img.shields.io/badge/Tkinter-GUI-ff6b35?style=flat-square)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Charts-11557c?style=flat-square)
![PySerial](https://img.shields.io/badge/PySerial-RS485-green?style=flat-square)
![PyInstaller](https://img.shields.io/badge/PyInstaller-EXE-yellow?style=flat-square)

---

<div align="center">

**⚡ PowerLab v6.5 © 2026 — made with ❤️ by Dr.Mosfet**

</div>
