<<<<<<< HEAD
# Mini Mochi Bot (ESP32-C3) — Build Notes

This repository documents my build of a **Mini Mochi Bot** powered by an **ESP32-C3 Mini** and flashed directly using the **official Mochi Web Installer by Huy Khong**.

* Wiring notes
* Hardware list
* Flashing method
* Photos / documentation of my build

---

## ✨ Overview

Mini Mochi Bot is a small OLED-based companion device that runs the **Mochi firmware** from Huy Khong.
My build uses:

* ESP32-C3 Mini
* 0.96" I²C OLED
* TP4056 Type-C charger
* TTP223 touch key
* Active buzzer
* SPDT slide switch
* 3.7V LiPo battery (WLY102040)

I flashed Mochi **entirely through the browser**, no PlatformIO or esptool needed.

---

## 🧱 Hardware Used

| Component    | Model                           |
| ------------ | ------------------------------- |
| MCU          | ESP32-C3 Mini                   |
| Display      | 0.96" SSD1306 I²C OLED          |
| Battery      | WLY102040 3.7V 800mAh LiPo      |
| Charger      | TP4056 (USB-C version)          |
| Touch Sensor | TTP223                          |
| Buzzer       | Active electromagnetic buzzer   |
| Switch       | 4mm SPDT 1P2T                   |
| Extras       | Wires, double tape, heat-shrink |

---

## 🔌 Wiring (My Build)

**OLED (I²C):**

* SDA → GPIO 6
* SCL → GPIO 7
* VCC → 3V3
* GND → GND

**Touch Sensor (TTP223):**

* OUT → GPIO 1
* VCC → 3V3
* GND → GND

**Buzzer (Active):**

* * → GPIO 2
* * → GND

**Battery + Charger:**

* TP4056 BAT+ → LiPo +
* TP4056 BAT- → LiPo -
* Output of TP4056 → ESP32 5V / VIN

**Switch:**

* Inline with battery output to ESP32 power

> ⚠ Pin numbers vary depending on your board revision; adjust as needed.

---

## 🚀 Flashing Mochi (Huy Khong Web Installer)

This build uses **Mochi from the official website**, not custom firmware.

### 1) Requirements

* Chrome / Edge browser
* USB-C data cable (not charge-only)

### 2) Flash Process

1. Open the Mochi Web Installer.
2. Connect ESP32-C3 to your PC.
3. Enter bootloader (if needed):

   * Hold **BOOT**, tap **RESET**, release BOOT
4. Click **Install / Connect**
5. Select **ESP32-C3**
6. Wait for flash to finish
7. Reset the board

### 3) First Boot

* OLED should display the Mochi face
* Bluetooth may appear as **Mochi**
* Touch sensor triggers sound/interaction

* You can see my setup/FLASHING for more detailed Flashing step-by-step process .
---

## 🧪 Troubleshooting

**OLED blank:**

* Power cycle
* SDA/SCL reversed
* Display pins not fully seated

**Bluetooth not showing:**

* Reset board after flashing
* Ensure no old pairing exists

**No sound:**

* Check buzzer polarity
* Buzzer must be **active type**, not passive

**Touch always triggered:**

* TTP223 too close to metal or wiring
* Adjust sensitivity jumper if needed

---

## 🖼 Photos
docs/images/

## 📜 License

MIT — free to modify and share.

---

## 🙌 Credits

* **Mochi Firmware:** Huy Khong
* Hardware build & documentation: Me
=======
# mini-mochi-bot
Mini Mochi Bot built using an ESP32-C3 Mini and the official Mochi firmware (Huy Khong). This repo contains wiring diagrams, flashing instructions, and build notes for recreating the project.
>>>>>>> 162e6a826c229ea3af3f0b387458b796d0eebdbc
