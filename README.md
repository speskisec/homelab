# 🧪 Homelab – virtuelles Security-Lab

Ein komplett virtuelles Lab auf einem einzelnen PC, um Netzwerk- und Security-Themen praktisch zu lernen: Firewall, Segmentierung, Active Directory, SIEM, IDS – und das Erkennen simulierter Angriffe.

Das Lab ist vollständig vom Heimnetz isoliert. Nach außen gibt es nur einen NAT-Zugang ins Internet; alle Lab-Netze sind interne virtuelle Netze.

## Aufbau

| Netz | Adressbereich | Zweck |
|---|---|---|
| WAN | NAT über den Host | nur Internetzugang |
| Servernetz | 10.10.10.0/24 | Linux-Server, Wazuh, Checkmk |
| Clientnetz | 10.10.20.0/24 | Windows-Clients, Domain Controller |
| Angreifernetz | 10.10.99.0/24 | Kali Linux, nur für Tests im Lab |

Router und Firewall zwischen allen Netzen: **OPNsense**.

Netzplan: siehe [`netzplan/`](netzplan/)

## Projekte

| Nr. | Projekt | Status |
|---|---|---|
| 01 | [Lab-Grundgerüst](01-lab-grundgeruest/) | 🔵 in Arbeit |
| 02 | Firewall-Regeln & Segmentierung | ⚪ geplant |
| 03 | Active Directory | ⚪ geplant |
| 04 | Wazuh-SIEM | ⚪ geplant |
| 05 | Angriff & Erkennung | ⚪ geplant |
| 06 | Checkmk im Lab + eigener Check | ⚪ geplant |
| 07 | Suricata-IDS | ⚪ geplant |

🟢 fertig · 🔵 in Arbeit · ⚪ geplant

## Werkzeuge

VirtualBox · OPNsense · Ubuntu Server · Windows Server (Testversion) · Wazuh · Checkmk Raw · Kali Linux · Suricata · draw.io

## Hinweis

Alle Angriffe finden ausschließlich innerhalb dieses isolierten Labs gegen eigene Systeme statt. In diesem Repo stehen keine echten Zugangsdaten und keine Daten von Arbeitgebern.
