<p align="center">
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/ec699f25-88ca-4a30-8cb9-ee24461616e3" />

</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-active-brightgreen" alt="Status">
  <img src="https://img.shields.io/badge/scope-authorized%20testing%20only-red" alt="Scope">
  <img src="https://img.shields.io/badge/license-educational-blue" alt="License">
  <img src="https://img.shields.io/badge/standard-IEEE%20802.11-informational" alt="802.11">
  <img src="https://img.shields.io/badge/python-3.8%2B-yellow" alt="Python">
</p>

<h1 align="center">WiFi Traffic Monitoring Toolkit</h1>

<p align="center">
  Teaching tool for traffic analysis and monitoring over wireless networks <b>IEEE 802.11</b>,<br>
  designed for audit, research and training activities in cybersecurity.
</p>

<p align="center">
  <a href="#-disclaimer-legal">Disclaimer</a> •
  <a href="#-technical-context">Context</a> •
  <a href="#-installation">Installation</a> •
  <a href="#-use">Use</a> •
  <a href="#-feature">Feature</a> •
  <a href="#-contatti - social">Contatti</a>
</p>

---

## Legal Disclaimer

> Responsibility is assumed by the person in whom he uses this tool, and he must be aware that it is not a game
>
> The author **takes no responsibility** for improper, illegal, or unauthorized use of this instrument. The interception or analysis of other people's network traffic, in the absence of explicit and written authorization, constitutes a **crime** pursuant to current regulations (in Italy, art. 617-quater of the Criminal Code — interception of computer communications — and privacy legislation, Legislative Decree 196/2003 and GDPR).
>
> **Use this tool exclusively:**
> - on networks and devices owned by you;
> - in isolated and controlled laboratories;
---

## technical context

**IEEE 802.11** networks transmit data over the air, making it possible, with appropriate hardware and software, to capture and analyze passing frames. Wireless traffic monitoring is a fundamental practice in:

- **network troubleshooting** (interference analysis, bottlenecks, roaming);
- **security audit** (detection of unauthorized devices, AP rogues, abnormal traffic);
- **incident response** (identification of ongoing attacks, such as deauth flooding or ARP spoofing).

> This repository documents the use of wireless cards in **monitor mode** for passive capture of 802.11 frames and their subsequent analysis.

---

## project goals

>  Provide tools for wireless traffic acquisition and inspection 
>  Identificare dispositivi connessi, punto di accesso e modello di traffico 

---

## Requirements

| Requirement | Detail |
|---|---|
| Wireless card | Support **monitor mode** |
| Operating System | Linux (Kali Linux / Parrot OS recommended) |
| Python | 3.8 or higher |
| Permits | Root/Administrator Login |
| Optional Tools | Wireshark / tshark for advanced '.pcap' analysis |

---

## installing

```bash
kali@kali:~$ sudo apt install realtek-rtl8814au-dkms
# Now use the *iwconfig* command to verify that the adapter has been installed and configured correctly:
kali@kali:~$ iwconfig
```

---

## using

> Before each acquisition, verify that you have **written authorization** and that you operate in an isolated environment or on a network you own.

For operational details, configuration parameters, and usage examples, see the dedicated guide:

📄 [`docs/USAGE.md`](docs/USAGE.md)

---

## Good Practices and Privacy

- Limit capture to only necessary metadata when possible (avoid sensitive payloads)
- Store '.pcap' catches safely and encrypted
- Anonymousize or delete data collected at the end of the audit activity
- Always comply with applicable privacy regulations (GDPR included)
  
---

## 🤝 Cto attribute

Contributions, bug reports, and suggestions are welcome. Before opening a pull request, see ['CONTRIBUTING.md'](CONTRIBUTING.md).

---

## License

Distributed under the **Educational Use Only** license — see ['LICENSE'](LICENSE) for full details.

---

<p align="center">
  <i>Made with 🔒 for the security research community</i>
</p>
