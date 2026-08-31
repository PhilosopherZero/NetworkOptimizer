# EtherifyZero NetworkOptimizer (BETA)
Smart Windows 10/11 latency desktop optimizer that benchmarks, auto-tunes, and stabilizes your network for gaming and real-time performance. Improves ping, jitter, and throughput across Wi-Fi and Ethernet using intelligent UDP/TCP optimization.


## License
This software is proprietary and not open-source.  
Redistribution, modification, or resale is prohibited without explicit permission.  
See [License.txt](./License.txt) for details.

## 💬 Join the Community
Join our Discord to share feedback, report bugs, or discuss network optimization ideas!  
👉 [Join NetworkOptimizer Discord](https://discord.gg/CxKqr6sexW)

## 🚀 Features
full desktop gui
<img width="1018" height="597" alt="after optimizer+dns" src="https://github.com/user-attachments/assets/3b34c1bb-02c3-4e72-b8f0-a0244131e23c" />

# ⚡ Etherify Zero

**Etherify Zero** is a one-click network optimizer for Windows 10 and 11. It reads your hardware and needs — Wi-Fi or Ethernet, low latency, faster downloads, or stability — and picks the right profile to tune your network: **Wi-Fi Latency**, **Ethernet Latency**, or **Wi-Fi Download**.

Every change can be previewed before applying, restored to Windows defaults, or rolled back with a system restore point.

## ⚙️ Core Optimizations
- 🧠 **Auto Optimize** – one-click profile detection + full optimization
- 🧠 **CPU / RSS** – routes network traffic to the best core, away from busy core 0, for stable networking
- 🌐 **MTU detection** – finds the best packet size, fast and accurate (~16s avg), preventing fragmentation and packet loss
- 🧩 **DNS optimization** – picks the lowest-latency, most stable resolvers (~6 mins avg)
- 🔧 **TCP optimization** – faster, more reliable connections
- ⚙️ **IPv6 preference** – control IPv6 vs IPv4

## 🧰 Network Tools
- 🔁 **Adapter restart** – quick and hard resets
- 🧹 **Cache reset** – clears DNS, ARP, Winsock
- ⚙️ **Reset to defaults** – restore original Windows network settings

## 📏 Custom Settings
- Set custom MTU / MTU 1280 preset / show current MTU
- Pick congestion controller
- Show TCP settings (coming back soon)

## 📈 Benchmarking & Diagnostics
- Latency, jitter, and DNS measurement
- Assess performance and diagnose issues with plain-language results
- Benchmark history – compare performance over time

## 📊 Info & System
- 📊 **Info tab** – full system + adapter details (CPU, RAM, GPU, IP, DNS, MTU, Wi-Fi signal)
- 🏠 **Home page** – key actions, adapter info, profile status, pinned tools, recommendations
- 💾 **Backups** – create named restore points, roll back safely
- 🚀 Start after login
- 📌 Pin favorite tools
- 🔴 Restart-required indicator
- 👀 Change review popup before applying
- 📡 Live status bar for background tasks

## 🧩 System Integration
- Windows 10 & 11 detection (optimize-aware)
- Wi-Fi & Ethernet detection (optimize-aware)
- Near 0% CPU / GPU use when idle


# ⚙️ Etherify Zero — Optimizations

Settings are chosen per hardware and per profile (Wi-Fi Latency / Ethernet Latency / Wi-Fi Download).

## TCP
- Auto-tuning – adapts the receive window to connection speed
- Pacing profile – smooths traffic for stable latency
- ECN – detects congestion earlier
- Fast Open – faster connection setup
- Hystart – controls slow-start behavior to reduce overly aggressive ramp-up
- PRR – faster loss recovery
- Duplicate ACK handling – consistent recovery under loss
- Timestamps – clearer round-trip measurement
- Min RTO – quicker retransmit timing
- Initial congestion window – better start speed
- RACK / Tail Loss Probe – improves detection and recovery from certain losses
- Delayed ACK – tuned ACK timing
- Congestion controller – best algorithm for your OS

## Windows Stack
- Default TTL – standard packet lifetime
- MTU discovery – prevents fragmentation
- Selective ACK (SACK) – efficient recovery
- TIME-WAIT – faster socket reuse
- Network throttling index – reduced throttling
- System responsiveness – stays snappy under load
- Name resolution priority – faster lookups

## Profiles
- Wi-Fi Latency – favors stable low latency Wi-Fi environment 
- Ethernet Latency – favors responsiveness
- Wi-Fi Download – favors throughput

## Auto Optimize
- Order: DNS (optional) → congestion → MTU → RSS core → profile + cache reset

## MTU
- Finds the largest usable packet size — fast, accurate, verified
- Falls back to a conservative size if unverifiable

## DNS
- Benchmarks well-known and current resolvers
- Applies best two as primary / secondary

## CPU / RSS
- RSS base CPU – dynamically selects the first logical processor of the second physical CPU core as the RSS starting point, keeping RSS off core 0. (Windows / app bloat) for stable networking rather than assuming a fixed CPU number
- Windows CPU topology detection – detects physical cores, logical
  processors, SMT, and efficiency classes
- SMT-aware logical processor mapping
- Global NDIS RSS configuration

## Benchmarking
- Latency / jitter / DNS measurement with score + rank
- Used to assess performance and diagnose
- Benchmark history – compare performance over time

## Tools
- Adapter restart (quick) – reset primary adapter
- Adapter restart (hard) – disable, 3s wait, re-enable
- Cache reset – DNS, ARP, Winsock
- Reset to default – restore Windows + congestion defaults

## Custom
- Set MTU / MTU 1280 / show MTU
- IPv6 preference – IPv6 > IPv4, prefer IPv4, or disable IPv6 transition (native stays on)
- Set congestion controller – manual pick instead of auto

## System Integration
- OS detection (Win 10 / 11) – tunes accordingly
- Network detection (Wi-Fi / Ethernet) – matches profile
- Info tab – full system + adapter details
- Restore point backups
- Review popup / restart indicator

## ⭐ Optimization Philosophy

Etherify Zero does not apply a universal set of "gaming tweaks."

Configurations are selected according to the detected network type,
hardware, and selected performance goal. Latency-oriented profiles
prioritize responsiveness, while throughput-oriented profiles make
different tradeoffs.

All optimizations can be reviewed before application and restored
through the application's reset/backup mechanisms.

## changelog 

[CHANGELOG.md](./CHANGELOG.md)

