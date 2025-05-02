# 🛡️ Slowloris DDoS Simulation & Wireshark Analysis

> **Educational use only.** Launch this script **solely in a controlled lab** you own. Attacking third‑party servers without permission is illegal.

## What it does
1. Opens hundreds of half‑open HTTP sockets (Slowloris technique).  
2. Keeps them alive with partial headers to exhaust the target’s connection pool.  
3. Provides a ready‑made Wireshark capture (`pcap/attack_sample.pcapng`) so you can inspect the packet pattern.

## Quick start

```bash
# clone
git clone https://github.com/<user>/slowloris-ddos-simulation.git
cd slowloris-ddos-simulation

# install deps
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

# run against a local VM
sudo python src/slowloris.py --host 192.168.56.10 --sockets 300
