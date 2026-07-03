# 🦊 SnowFox Mesh

SnowFox Mesh ist ein dezentrales, selbstorganisierendes Kommunikationsprotokoll, das darauf ausgelegt ist, die Netzwerkverfügbarkeit in Szenarien mit eingeschränkter oder fehlender zentraler Infrastruktur zu gewährleisten. Das Projekt verfolgt das Ziel, die digitale Resilienz zu erhöhen und ein Kommunikationsnetzwerk zu schaffen, das **ohne zentrale Server** sowie **unabhängig von zentraler Internet-Infrastruktur** betreibbar ist.

## 🏗 Architektur

### Übersicht
SnowFox Mesh arbeitet auf einer Layer-2/3-Hybrid-Ebene, um eine dynamische Netzwerktopologie ohne zentrale Instanzen zu ermöglichen.

*   **Transportmedien:** Primär 802.11 (WLAN).
*   **Protokoll-Stack:** Nutzung von UDP zur Paketübertragung zur Minimierung des Overheads.
*   **Routing-Verfahren:**
    *   **Flood-Routing mit TTL:** Zur Sicherstellung der Zustellbarkeit in hochdynamischen Mesh-Umgebungen bei gleichzeitigem Schutz vor unendlichen Paketschleifen.
    *   **Sequence Numbers:** Zur Vermeidung von Duplikaten pro Nachricht.
*   **Peer Discovery:** Automatisierte Broadcasting-Mechanismen zur Erkennung benachbarter Knoten.
*   **Frontend:** Browser-basiertes Interface (Web-Proxy). Benutzer verbinden sich mit einem lokalen Access Point eines Knotens; es ist keine dedizierte Anwendung (App) auf den Endgeräten erforderlich.

### System-Voraussetzungen
Obwohl das Netzwerk **unabhängig von Internet-Providern** agiert, bleibt die Funktionalität an physische Ressourcen gebunden:
*   **Hardware:** WLAN-fähige Endgeräte (Router, Einplatinencomputer oder Smartphones).
*   **Energie:** Lokale Stromversorgung der Routing-Knoten.

### Sicherheit & Kryptographie
*   **E2E-Verschlüsselung:** Einsatz des [Noise Protocol Frameworks] für Authentifizierung und Verschlüsselung der Payloads.
*   **Bedrohungsmodell:** Das Protokoll zielt darauf ab, passive Inhaltsanalysen zu verhindern. Metadaten (Verkehrsmuster) sind prinzipbedingt sichtbar, sofern keine zusätzlichen Obfuskations-Layer implementiert werden. Es wird kein Anspruch auf absolute Anonymität erhoben.

## 📊 System-Eigenschaften

| Merkmal | Eigenschaft |
| :--- | :--- |
| Topologie | Dezentral (Mesh) |
| Zentraler Server | Nicht erforderlich |
| Internet-Infrastruktur | Unabhängig |
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
Version: 0.9 (Entwicklung)
