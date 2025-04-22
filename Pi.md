Raspberry Pi 4 + Raspberry Pi OS (64-bit) + SanDisk 30 GB

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
│   ├── `sudo raspi-config`
│   │   └── Interface Options
│   │       └── VNC
│   │           └── Yes
│   ├── Set VNC username password
│   │   ├── `mkdir -p ~/.config/wayvnc`

```
echo "address=0.0.0.0
enable_auth=true
username=pi
password=yournewpassword" > ~/.config/wayvnc/config
```
│   │   ├── `cat ~/.config/wayvnc/config`
│   ├──
│   ├──
│   ├──
│
│
└── RVNC Viewer


Man... I gev up
