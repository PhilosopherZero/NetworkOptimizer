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
