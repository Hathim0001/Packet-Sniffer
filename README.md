# Packet Sniffer

A **Network Packet Sniffer** developed in **Python 3**.
Packets are disassembled in real-time as they arrive at a specified network interface controller (NIC) and their details are displayed on the screen.

---

## Features

- Real-time packet capture and disassembly.
- Monitor specific interfaces or all available interfaces.
- Optional display of raw packet data.
- Ability to build a standalone executable.

---

## Installation

### I. Development Mode

Clone the repository, install dependencies, and run:

```bash
git clone https://github.com/Hathim0001/Packet-Sniffer
cd Packet-Sniffer
pip install -r requirements.txt   # or use poetry install
sudo python3 packet_sniffer/sniffer.py
```

> **Note:**
> - `sudo` is required because `socket.SOCK_RAW` needs administrative privileges.
> - If using a virtual environment, activate it before installing dependencies and running the application.

---

### II. (Optional) Build a Binary

You can compile a standalone executable using **PyInstaller**:

```bash
# After installing dependencies
python3 build.py
```

This will generate a standalone binary file suitable for your system.

---

## Usage

```bash
sniffer.py [-h] [-i INTERFACE] [-d]
```

| Argument | Description |
|:---------|:------------|
| `-h`, `--help` | Show help message and exit. |
| `-i INTERFACE`, `--interface INTERFACE` | Capture packets from a specific network interface (default monitors all interfaces). |
| `-d`, `--data` | Output raw packet data during capture. |

### Example

Capture packets from the `eth0` interface and output raw data:

```bash
sudo python3 packet_sniffer/sniffer.py -i eth0 -d
```

---

## Requirements

- Python 3.8+
- Other dependencies listed in `requirements.txt`
