# 🦊 SnowFox Mesh

SnowFox Mesh ist ein dezentrales, autarkes Kommunikationsprotokoll, das darauf ausgelegt ist, die Netzwerkverfügbarkeit in Szenarien mit eingeschränkter oder fehlender zentraler Infrastruktur zu gewährleisten. Das Projekt dient dem Ziel, die digitale Resilienz zu erhöhen und eine von Internet-Providern unabhängige Kommunikationsinfrastruktur zu schaffen.

## 🏗 Architektur

### Übersicht
SnowFox Mesh arbeitet auf einer Layer-2/3-Hybrid-Ebene, um eine dynamische Netzwerktopologie ohne zentrale Server zu ermöglichen.

*   **Transportmedien:** Primär 802.11 (WLAN).
*   **Protokoll-Stack:** Nutzung von UDP zur Paketübertragung, um den Overhead zu minimieren.
*   **Routing-Verfahren:**
    *   **Flood-Routing mit TTL:** Zur Sicherstellung der Zustellbarkeit in hochdynamischen Mesh-Umgebungen bei gleichzeitigem Schutz vor unendlichen Schleifen.
    *   **Sequence Numbers:** Zur Vermeidung von Duplikaten pro Nachricht.
*   **Peer Discovery:** Automatisches Broadcasting zur Erkennung benachbarter Knoten.
*   **Frontend:** Browser-basiertes Interface (Web-Proxy). Nutzer verbinden sich mit einem lokalen Access Point; es ist keine dedizierte Anwendung (App) auf den Endgeräten erforderlich.

### Infrastruktur-Anforderungen
*   **Hardware:** Benötigt werden WLAN-fähige Endgeräte (Router, Einplatinencomputer oder Smartphones).
*   **Stromversorgung:** Das System ist autark gegenüber ISP-Gateways, benötigt jedoch eine lokale Stromversorgung für die Routing-Knoten.

### Sicherheit & Kryptographie
*   **E2E-Verschlüsselung:** Einsatz des [Noise Protocol Frameworks] für Authentifizierung und Verschlüsselung der Nutzdaten.
*   **Bedrohungsmodell:** Das Protokoll zielt darauf ab, passive Beobachtung der Inhalte zu verhindern. Metadaten (Verkehrsmuster) sind prinzipbedingt sichtbar, sofern keine zusätzlichen Obfuskations-Layer implementiert werden.

## 📊 System-Eigenschaften

| Merkmal | Eigenschaft |
| :--- | :--- |
| Topologie | Mesh (Peer-to-Peer) |
| Zentraler Server | Nicht erforderlich |
| Internet-Infrastruktur | Nicht erforderlich |
| Open Source | Ja |
| Offline-Betrieb | Vollständig möglich |
| Notfall-Priorisierung | Implementiert (Applikations-Ebene) |

## 🛠 Roadmap & Entwicklung
Der Fokus liegt derzeit auf der Performance-Optimierung der Routing-Logik durch eine Go-Implementierung.

*   **Alpha-Phase:** Implementierung der Basisfunktionalität (Paket-Routing, Discovery).
*   **Optimierung:** Reduktion von Latenzzeiten und Implementierung von TTL/Sequence-Number-Logik.
*   **Security:** Integration der Noise-Protokoll-Bibliotheken.

## 📝 Entwicklungsgrundsätze
Das Projekt verfolgt einen pragmatischen Ansatz zur technischen Resilienz. Ich lade Entwickler zur Mitarbeit an der Protokollspezifikation und der Routing-Effizienz ein. Die Architektur soll nachvollziehbar, modifizierbar und robust gegenüber Knoten-Ausfällen sein.

---
*Disclaimer: SnowFox Mesh ist ein experimentelles Open-Source-Projekt. Die Nutzung erfolgt auf eigene Gefahr. IT-Systeme unterliegen stets Risiken; absolute Sicherheit oder Verfügbarkeit können nicht garantiert werden.*

Dokument erstellt: 2026-07-03
Version: 0.8 (Entwicklung)
