# ⚡ Etherify Zero (beta)

**Etherify Zero** is a smart Windows 10/11 network optimizer for **latency, jitter, throughput, and stability**. It detects your hardware and network type, benchmarks where needed, and applies the appropriate optimizations for Wi Fi or Ethernet.

Profiles are selected automatically based on hardware and network type, with manual override available when needed.

Every change can be reviewed before applying, restored to Windows defaults, or rolled back using a system restore point.

🌐 **Website:** https://etherifyzero.com/

## 🚀 Features

full desktop gui
<img width="1018" height="597" alt="after optimizer+dns" src="https://github.com/user-attachments/assets/3b34c1bb-02c3-4e72-b8f0-a0244131e23c" />

### ⚙️ Core Optimizations

**Auto Optimize** — automatic profile detection and full optimization

**CPU / RSS** — dynamically selects an RSS starting CPU from physical CPU topology instead of using a fixed processor number

**MTU Detection** — finds and verifies the largest usable packet size in ~16 seconds on average

**DNS Optimization** — benchmarks Cloudflare, Google, Quad9, OpenDNS, and AdGuard DNS and applies the best two based on latency and stability

**TCP Optimization** — profile based TCP tuning for latency, throughput, and stability

**IPv6 Preference** — choose IPv6 preference, IPv4 preference, or disable IPv6 transition mechanisms

### 📶 Profiles

**Wi Fi Latency** — optimized for low latency and stability

**Ethernet Latency** — optimized for responsiveness

**Wi Fi Download** — optimized for throughput

Profiles are selected automatically and can be manually overridden from the profile selector.

### 🧰 Network Tools

**Adapter Restart** — quick and hard restart options

**Cache Reset** — DNS, ARP, and Winsock

**Reset to Defaults** — restore Windows networking and congestion settings

**Custom MTU** — view or manually set MTU, including a 1280 preset

**Congestion Controller** — manually select the congestion control algorithm

### 📈 Benchmarking & Diagnostics

**Latency, jitter, and DNS benchmarking**

**Performance scores and rankings**

**Benchmark history**

**Plain language diagnostics**

### 📊 System Information

**Info Tab** — detailed CPU, RAM, GPU, IP, DNS, MTU, adapter, Wi Fi signal, interface metric, and other system and network information

### 🖥️ Application

**Home** — key actions, adapter information, profile status, pinned tools, and recommendations

**Backups** — named system restore points and rollback

**Review Changes** — preview changes before applying

**Restart Indicator** — shows when changes require a restart

**Live Status** — background operation status

**Start on Login** — optional delayed startup

## 🧩 System Integration
- Windows 10 & 11 detection (optimize-aware)
- Wi-Fi & Ethernet detection (optimize-aware)
- Near 0% CPU / GPU use when idle

## ⭐ Optimization Philosophy

Etherify Zero does not apply a universal set of "gaming tweaks."

Configurations are selected according to the detected network type,
hardware, and selected performance goal. Latency-oriented profiles
prioritize responsiveness, while throughput-oriented profiles make
different tradeoffs.

All optimizations can be reviewed before application and restored
through the application's reset/backup mechanisms.

## 📚 Documentation

**[FEATURES.md](./FEATURES.md)** — complete feature and capability list

**[OPTIMIZATIONS.md](./OPTIMIZATIONS.md)** — detailed optimization reference

**[CHANGELOG.md](./CHANGELOG.md)** — version history

## 💬 Community

Join the Etherify Zero Discord to report bugs, share feedback, and discuss network optimization.

👉 **[Join the Etherify Zero Discord](https://discord.gg/CxKqr6sexW)**

## 📄 License

Etherify Zero is proprietary software and is not open source.

Redistribution, modification, or resale is prohibited without explicit permission.

See **[License.txt](./License.txt)** for details.
