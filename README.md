# Bangladesh Camera Scanner - Combined Tool

<div align="center">

![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fbadol%2Fcamera-scanner&label=Visitors&countColor=%23263759&style=flat)
![GitHub Views](https://komarev.com/ghpvc/?username=badol&label=Profile%20Views&color=0e75b6&style=flat)
[![GitHub Stars](https://img.shields.io/github/stars/badol?style=social)](https://github.com/badol)
[![GitHub Followers](https://img.shields.io/github/followers/badol?style=social)](https://github.com/badol)

![Python Version](https://img.shields.io/badge/python-3.7%2B-blue?style=flat&logo=python)
![Termux Support](https://img.shields.io/badge/Termux-Compatible-green?style=flat&logo=android)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Windows%20%7C%20Android-lightgrey?style=flat)
![License](https://img.shields.io/badge/license-MIT-green?style=flat)

### 🎯 Real-Time Visitor Counter - See Who's Visiting! 👆

</div>

A powerful tool that combines IP range collection and camera scanning functionality for Bangladesh networks.

## Features

- 🌐 Fetch Bangladesh IPv4 ranges from APNIC database
- 📹 Scan for IP cameras and web services
- 🔍 Detect multiple camera brands:
  - **Anjhua-Dahua Technology Cameras**
  - **HIK Vision Cameras**
- 💾 Live save - Results saved instantly as they're found
- 💻 Termux compatible (Android)
- 🎨 Colorful terminal interface
- 🚀 Multi-threaded scanning (100 threads)
- 📊 Detailed camera information (IP, Port, URL, Timestamp)

## Download Camera Live View App

https://w8team.online/badol//index.php?user/publicLink&fid=eeb7f4Fmgo5rHTKhT4KOm61nzgob0933QBWTguLs9XTdkVbmCloYXbIU6Ey6Y8rO6LgHsh1bZXTzhDGz9ZE3w3i5Snp2e5VopypU6G5jzwXw1W8bsms3uQ&file_name=/DMSS_1_99_623_222.apk

Altanitive.. https://gofile.io/d/fr8rOB

## Installation

### For Termux (Android)

# Update packages

```
pkg update && pkg upgrade
```
# Install required packages
```
pkg install python git
```
```
pkg install git -y
```

# Install Python dependencies
```
pip install requests aiohttp pyfiglet
```
# Optional: For colors (if colorama install fails, the script works without it)

```
pip install colorama
```
### For Desktop (Windows/Linux/Mac)

# Install Python dependencies

```
pip install requests aiohttp pyfiglet colorama
```
## Usage
Run and clone the script:
```
git clone https://github.com/badol/W8CameraHackV1
```
```
cd W8CameraHackV1
```
```
python W8CameraHackV1.py
```


### Menu Options

1. **Update IP Ranges from APNIC** - Downloads latest Bangladesh IP ranges
2. **Scan IP Ranges for Cameras** - Scans the IP ranges for cameras (requires BDALLIP.txt)
3. **Update & Scan (Both)** - Does both operations in sequence
4. **Exit** - Quit the program

### 🎮 Scan Controls

During scanning, you can use:
- **Ctrl+C** - ⛔ Stop scan immediately (instant exit)
- **Ctrl+Z** - ⏸️ Pause/Resume scan (toggle on Linux/Mac/Termux)

## Output Files

- `BDALLIP.txt` - Contains Bangladesh IP ranges in CIDR notation
- `CCTV Found.txt` - All detected cameras with details (Live Save)
  - **Anjhua-Dahua Technology Cameras** (WEB SERVICE detection)
  - **HIK Vision Cameras** (login.asp detection)

### Output Format

Each detected camera is saved with:
- Camera Type (Brand/Model)
- IP Address
- Port Number
- Full URL
- Detection Timestamp
- Live saving (results appear immediately!)

**Example Output:**
```
============================================================
Camera Type: Anjhua-Dahua Technology Camera
IP Address: 192.168.1.100
Port: 80
URL: http://192.168.1.100
Detection Time: 2025-10-01 14:30:45
============================================================
```

See `SAMPLE_OUTPUT.txt` for more examples.

## How It Works

1. **IP Range Collection**: Fetches Bangladesh IPv4 ranges from APNIC's delegation database
2. **CIDR Parsing**: Converts custom CIDR notation (IP/count) to individual IP addresses
3. **Multi-threaded Scanning**: Uses 100 threads to scan ports 80 and 8080 simultaneously
4. **Detection**: Identifies cameras by looking for specific HTML titles and patterns

## Ports Scanned

- Port 80 (HTTP)
- Port 8080 (HTTP Alternative)

## Notes

- The scanner uses a 0.25 second timeout per connection
- Results are saved in real-time to output files (Live Save with `file.flush()`)
- **Instant Stop**: Press Ctrl+C to stop scanning immediately (no delay!)
- **Pause/Resume**: Press Ctrl+Z to pause and resume (Linux/Mac/Termux only)
- The tool is optimized for Termux with fallback color codes if colorama is not available
- All worker threads properly handle stop signals for clean shutdown

## Legal Disclaimer

This tool is for educational and authorized security testing purposes only. Always obtain proper authorization before scanning networks you don't own.

## Credits

<div align="center">

### 👨‍💻 Developed by: /badol

[![GitHub](https://img.shields.io/badge/GitHub-badol-181717?style=for-the-badge&logo=github)](https://github.com/badol)
[![Profile Views](https://komarev.com/ghpvc/?username=badol&label=Profile%20Views&color=blueviolet&style=for-the-badge)](https://github.com/badol)

**Team:** W8Team  
**Contact:** [GitHub Profile](https://github.com/badol)

</div>

### 📊 Repository Stats

![Repo Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fbadol%2Fcamera-scanner&labelColor=%23697689&countColor=%23ff8a65&style=plastic&labelStyle=upper)
![GitHub code size](https://img.shields.io/github/languages/code-size/badol/camera-scanner?style=plastic)
![GitHub repo size](https://img.shields.io/github/repo-size/badol/camera-scanner?style=plastic)

### Original Components
- 📡 All ASN Collector (IP Range Fetcher)
- 📹 W8IPCameraHK V4 (Camera Scanner)
- 🔧 Combined & Optimized by badol for Termux Support

---

<div align="center">

**⭐ If you like this project, please give it a star! ⭐**

Made with ❤️ by [@badol_112]

</div>





