## How to connect a Pi to a Android Mobile using USB Tethering

<br>

- Raspberry Pi 4  
- Raspberry Pi OS (64-bit)
- SanDisk 30 GB
  
<br>

```
Raspberry Pi Imager
│
├── Raspberry Pi Device
├── Choose OS
├── Storage
│
└── OS Customisation
    │
    ├── Services
    │   └── Enable SSH
    │       └── Password authentication 
    │
    └── General
        ├── hostname ── raspberrypi.local
        ├── username ── pi
        ├── password ── raspberry
        │
        ├── SSID ── Mobile Hotsopt name
        └── pass ── 12345678

Android Mobile
│
├── Hotspot
│   └── Conneted Devices
│       └── Pi ip
│
├── Port Authority
│   ├── need wifi to scan ip
│   └── Copy Pi ip
│
├── Termux
│   ├── `pkg install openssh`
│   │
│   ├── `ssh-keygen -R 192.168.117.125`
│   │   └── to remove the old key from your known_hosts file in Termux
│   │
│   ├── `ssh pi@192.168.xx.xx`
│   │   └── yes
│   │
│   ├── `ssh pi@192.168.xx.xx`
│   │   └── password
│   │
│   ├── `sudo raspi-config`
│   │   └── Interface Options
│   │       └── VNC
│   │           └── Yes
│   │
│   └── hostname -I
│       └── 192.168.xx.xx   192.168.xx.xx
│                           └── copy 2nd ip
│
└── RVNC Viewer
    └── create new connection
        └── 2nd ip is the connection address
            └── connect
                │
                ├── username: pi
                └── password: raspberry

```
