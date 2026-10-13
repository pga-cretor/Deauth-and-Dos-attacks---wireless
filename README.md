<p align="center">
<img width="1254" height="1254" alt="image" src="https://github.com/user-attachments/assets/b7da575e-64fe-4042-b105-dd70be416421" />

</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-active-brightgreen" alt="Status">
  <img src="https://img.shields.io/badge/scope-authorized%20testing%20only-red" alt="Scope">
  <img src="https://img.shields.io/badge/license-educational-blue" alt="License">
  <img src="https://img.shields.io/badge/standard-IEEE%20802.11-informational" alt="802.11">
  <img src="https://img.shields.io/badge/python-3.8%2B-yellow" alt="Python">
</p>

<h1 align="center">WiFi Deauth & DoS Toolkit</h1>

<p align="center">
  Strumento didattico per lo studio delle vulnerabilità dei <b>management frame IEEE 802.11</b><br>
  e degli attacchi di <b>Denial of Service</b> su reti wireless.
</p>

<p align="center">
  <a href="#-disclaimer-legale">Disclaimer</a> •
  <a href="#-contesto-tecnico">Contesto</a> •
  <a href="#-installazione">Installazione</a> •
  <a href="#-utilizzo">Utilizzo</a> •
  <a href="#-contromisure-consigliate">Contromisure</a> •
  <a href="#-contatti--social">Contatti</a>
</p>

---

## ⚠️ legal disclaimer 

> This tool is dangerous for those who cannot take responsibility when they do not know how to use it
>
> The aurore of this instrument assumes no responsibility for improper, llegal or unauthorized use of this instrument. Performing deauthentication or DoS attacks on networks for which you do not have explicit and written authorization constitutes a crime under current regulations (in Italy, Articles 615-ter and 635-bis of the Criminal Code, in addition to the legislation on telecommunications jamming).

> **Use this tool exclusively:**
> - taking your responsibility for this tool;
> - you need to know what you're using, not to do everything randomly;
> - it is not a tool to take revenge against a person;

---

## technical context

The **IEEE 802.11** protocol, in its basic implementation, involves sending **management frames** (including deauthentication and disassociation) **unauthenticated and unencrypted**. This architectural feature makes it possible, in the absence of countermeasures, to forcibly disconnect a client from a wireless network.

This repository documents:

- the operation of the 802.11 management frames involved in the attack;
- the laboratory conditions necessary for ethical and controlled testing;
- existing countermeasures (802.11w/PMF, WIDS/WIPS, spectrum monitoring).

---

## requirements


| Requirement | Detail |
|---|---|
| Wireless Card | Support **Monitor Mode** and **Packet Injection** |
| Operating System | Linux (Kali Linux / Parrot OS recommended) |
| Python | 3.8 or higher |
| Permits | Root/Administrator Login |


---

## installation

```bash
# sends several deauthentication frames to a client
kali@kali~$ sudo aireplay-ng -O 40 -a 00:25:00:FF:94:73 -c 00:0F:B5:AE:CE:9D wlan0
# flag -0 prompts *aireplay-ng* to send deauthentication packets, *40* is the number of packets to send
```
---
```bash
# would tell a client to access the *WIFI*, flooding that access point with a flurry of requests from fake clients, thus taking the access point offline.
kali@kali~$ sudo mdk4 --fullhelp


```
---

##  Recommended Countermeasures

- Enable **802.11w (Protected Management Frames)** on access points and clients
- Implement **WIDS/WIPS** systems for anomaly detection in management frames
- Constantly monitor RF spectrum and authentication logs
- Segment the wireless network from that sensitive data

---

## Structure of the Repository

| File / Folder | description|
|---|---|
| [`docs/LEGAL.md`](docs/LEGAL.md) | WI-FI traffic monitoring |

---

## contribute

Contributions, bug reports, and suggestions are welcome. Before opening a pull request, see ['CONTRIBUTING.md'](CONTRIBUTING.md).

---

##  Contatti & Social

<p align="left">
  <a href="https://x.com/TracetheleakS"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white"></a>
</p>

---

<p align="center">
  <i>Made with 🔒 for the security research community</i>
</p>
