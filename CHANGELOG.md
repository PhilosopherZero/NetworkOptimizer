# 🧾 Changelog

## [0.3.0] - 2026-08-30

### ✨ New Features
- 🎛️ Added profile selector — available profiles: Wi-Fi Latency, Ethernet Latency, and Wi-Fi Download
- 📶 Added Wi-Fi Download profile — optimized for throughput
- 🌐 Added IPv6 preference dropdown — choose IPv6 off, priority over IPv4, or the opposite
- 🧠 Added RSS base CPU optimization — dynamically picks the RSS starting core from detected CPU topology instead of blindly setting a static value (see optimizations.md)
- 📊 Info tab now shows the interface metric for the primary adapter (better diagnosis)
- ➕ Added more optimizations (e.g. TcpMaxDupAcks)

### 🧩 Fixes & Improvements
- 🔍 DNS optimization is now more transparent — each tested DNS server's score and stats (latency, loss, rank) are shown live in the console, followed by a full leaderboard and the chosen primary/secondary DNS
- ⚙️ Congestion controller selection converted from input box to dropdown
- 🔘 All action buttons now reflect state — they gray out while their task is running
- 📡 All actions now report progress in the status bar (previously only a few did)
- 💬 All action buttons now show a description on hover explaining what each action does
- 🌍 Fixed wrong IPv6 optimization — now recommends configuring and enabling IPv6 for better performance, as some servers and CDN nodes are dedicated to IPv6 and it can bypass CGNAT, among other benefits


### ⚡ Performance
- 🚀 App starts up faster and detects system info faster
- ⚡ Actions such as Auto Optimize and Reset to Default show change diffs faster

### 🛡️ Security & Compatibility
- 🛡️ Improved antivirus compatibility — reduced false-positive detections by removing unnecessary behaviors that could trigger heuristic antivirus analysis
🔏 Added executable signing — release executables are now Authenticode-signed to provide signature-based file integrity verification and identify the signing certificate

## [0.2.0] - 2026-06-21

### ✨ New Features
- 🖥️ Added GUI with near 0% CPU / GPU usage when idle  
- 💾 Added backup tab system using Windows restore points  
- 🚀 Added option to start Etherify Zero after login with a 1-minute delay  
- 📊 Added Info tab showing full system and adapter details, including CPU, RAM, GPU(s), MTU, IP, DNS, and other network/interface statistics
- 🏠 Added Home page for quick access to key actions, adapter info, profile status, recommendations, and pinned tools (MTU optimization, adapter restart, etc.)  
- 🧰 Added Tools tab with full network utilities: MTU optimization, DNS optimization, IPv4/IPv6 MTU configuration (global), soft/hard adapter restarts, and network cache reset  
- 📈 Added Benchmark tab with detailed network performance metrics (min/avg/max latency, packet loss, and score) with basic interpretation and actionable insights (more interpretation planned)  
- ⚙️ Added Settings tab with startup control and option to reset to default Windows network settings  
- 📌 Added ability to pin favorite tool actions to the Home page for faster access  
- 👀 Added changelog preview popup before applying auto-optimizations or reset actions (shows pending changes before execution)  
- 🔴 Added restart-required indicator widget that glows red when an action requires a system reboot  
- 📡 Added status bar for ongoing background operations to prevent accidental app closure during processes (some tasks may still lack consistent reporting)  
- 🕒 Added local benchmark history tracking to view network performance over time for troubleshooting and analysis (interpretation improvements planned)
- 💎Added 6 new optimizations that improve network priority, stability and performance

---

### 🧩 Fixes & Improvements
- 🧰 Improved MTU discovery process now ~16s average and ~4.6× faster, with higher accuracy  
- 🚀 DNS optimization process improved ~6 minutes and ~4× faster with better accuracy  
- ⚙️ Fixed startup behavior app now launches more reliably after installation  
- 🌐 Improved DHCP/DNS reset handling when restoring default network settings  
- 🌙 Fixed light mode users experiencing unusable UI by defaulting to dark mode (light mode may be added later if needed)
- 🩹 Updated and fixed network optimization parameters and settings default values to be based on latest version of windows documentation and fresh windows install iso



## [0.1.1] - 2025-10-20

### 🧩 Fixes & Improvements
- 🧰 **Fixed perfect MTU setter** not working for Ethernet (was assuming Wi-Fi only)  
- ⚙️ **Failed to Fix startup issue** — app now launches more reliably on boot *(tentative fix)*  
- 🚀 **Fixed launcher integration** — “Launch Software” now correctly opens the main app  
- 🌐 **Added & fixed congestion controller reset** when restoring default network settings  


## [0.1.0] - 2025-10-17

### 🚀 Features

#### ⚙️ Core Optimizations
- 🧠 **Auto Optimize** – One-click intelligent optimization  
- ⚡ **Latency Benchmark** – Measure real-world ping and jitter  
- 🌐 **MTU Optimization** – Prevents fragmentation and packet loss  
- 🧩 **DNS Optimization** – Selects lowest latency + highest stability resolvers  
- 🔧 **TCP Optimization** – Tunes congestion and performance settings  
- 🛡 **Latency Shield Lite** – Reduces instability under fluctuating network load  

#### 🧰 Network Tools
- 🔁 **Adapter Restart** – Quickly refreshes network interfaces  
- 🧹 **Cache Reset** – Clears cached network data (DNS, ARP, etc.)  
- ⚙️ **Reset to Default** – Restores original network configuration  

#### 🧮 Custom Settings
- 📏 **Set Custom MTU** – Define manual MTU values  
- 🎯 **Set MTU 1280** – Quick preset for minimal fragmentation  
- 🧭 **Show MTU Value** – Displays current adapter MTU  
- 🌍 **Show TCP Settings** – Displays both Global and Supplemental TCP settings  

#### 🧩 System Integration
- 💻 **OS Detection** – Supports Windows 10 and Windows 11 *(optimize-aware)*  
- 🛜 **Network Detection** – Supports Wi-Fi & Ethernet *(optimize-aware)*  
