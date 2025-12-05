Got it — here’s a **drop-in replacement** for your `setup/FLASHING.md` section that matches how you flashed **Mochi via Huy Khong’s web installer**. Just copy-paste this over your old “Flashing” section (no other files changed).

---

## Flashing Mochi (Huy Khong Web Installer)

> This build was flashed **directly from the Huy Khong Mochi website** using the browser installer (no esptool/PlatformIO).

### Prereqs

* **Google Chrome** or **Microsoft Edge** (desktop) with Web Serial support
* A **data** USB-C cable (not charge-only)

### First-time install (ESP32-C3)

1. Open the Mochi installer page in Chrome/Edge.
2. Put the ESP32-C3 into bootloader (if needed):

   * Hold **BOOT**, tap **RESET**, then release **BOOT**.
3. Click **Install / Connect** (or similar) on the page.
4. In the port picker, select your ESP32-C3 device and **Connect**.
5. Choose **ESP32-C3** when prompted, then click **Install**.
6. Wait for erase + flash to complete, then click **Reset** (or press the board’s **RESET** button).
7. After reboot:

   * If the site shows a setup flow, follow it (Wi-Fi/Bluetooth).
   * Otherwise, the device should boot into Mochi.

### Updating to a new version (same method)

1. Reopen the Mochi installer page.
2. Click **Connect**, choose the ESP32-C3 port.
3. Click **Install** (you can keep settings if the page offers that).
4. After it says **Done**, **Reset** the board.

### Troubleshooting

* **No port listed:** try another USB port/cable, or press **BOOT+RESET** again.
* **Flash fails midway:** close other serial monitors, reconnect, and retry.
* **Nothing on OLED after flash:** power cycle; check wiring for OLED (SDA/SCL, VCC, GND).
* **Bluetooth not visible:** reset once after flashing; confirm your phone’s BT is on and not already paired to an old name.

> Notes:
>
> * You don’t need `esptool.py` or PlatformIO for this method.
> * On Windows, drivers are usually not required for ESP32-C3 (CDC). If the port still doesn’t appear, install your board’s USB driver.
