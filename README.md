# Bluetooth DOS Script

⚠️ **DISCLAIMER**  
This script is provided for **educational and research purposes only**.  
The author does **not** take responsibility for misuse.  
Use at your own risk and only on devices you own or have explicit permission to test.

---

## 📌 Description
This Python script attempts a **Bluetooth Denial of Service (DoS) attack** using the `l2ping` utility from the BlueZ toolkit.  

It works by:
1. Scanning for nearby Bluetooth devices.
2. Listing available devices with their MAC addresses.
3. Allowing you to select a target device.
4. Spawning multiple threads that flood the target with `l2ping` requests.

---

## ⚙️ Requirements

- Linux environment with Bluetooth support  
- `bluez` tools installed (`hcitool`, `l2ping`, etc.)  
- Python 3.x  
- Root privileges (needed for Bluetooth commands)

### Install dependencies on Ubuntu/Debian:
```bash
sudo apt-get update
sudo apt-get install -y python3 python3-pip bluez bluez-hcidump bluetooth
```

## Usage

- Clone or copy the script.
- Run the script with root privileges:
```
sudo python3 script.py
```
- Accept the disclaimer (y).
- Script will scan for nearby Bluetooth devices:
```
|id   |   mac_addres      |   device_name|
|0    |   00:11:22:33:44:55 |   MyHeadset |
```
- Enter the target ID or MAC address.
- Provide packet size (integer).
- Provide thread count (integer).
- The DoS attack will begin.

## 🛑 Example
```
sudo python3 bt_dos.py
```

Sample interaction:
```
Do you agree? (y/n) > y
Scanning ...
|id   |   mac_addres      |   device_name|
|0    |   00:11:22:33:44:55 |   MySpeaker |

Target id or mac > 0
Packages size > 600
Threads count > 5
```
