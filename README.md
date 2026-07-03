# 🦊 SnowFox Mesh

SnowFox Mesh ist ein dezentrales, autarkes Kommunikationsprotokoll, das als Antwort auf die zunehmende Fragilität zentralisierter Infrastrukturen entwickelt wurde. Mein Ziel ist die Schaffung eines Netzwerks, das auch bei Ausfall staatlicher oder kommerzieller Systeme (ISP-Gateways, Stromnetz) die Kommunikation aufrechterhält.

## 🏛 Gesellschaftspolitische Einordnung
Ich beobachte eine kritische Entwicklung: Die Abhängigkeit von zentralen, staatlich oder kommerziell kontrollierten Infrastrukturen führt zu einer systemischen Schwachstelle. Wenn Kommunikation ausschließlich über Masten, Rechenzentren und Internet-Provider läuft, verliert der Bürger seine Handlungsfähigkeit bei deren Ausfall.

*   **Systemische Verwundbarkeit:** Aktuelle Behördensysteme folgen der Logik: „Das Nötigste reicht“. Ich halte dies für ein Versagen. Sicherheit in Krisenzeiten darf keine ökonomische Abwägung sein, sondern erfordert garantierte Funktionalität.
*   **Widerstand als Legitimation:** Die Autonomie meines Systems ist bewusst gewählt. Wenn Firmen oder staatliche Akteure ein solches Tool einschränken oder verbieten wollen, sehe ich dies als Bestätigung seiner Relevanz. Jedes Verbot ist der Beweis, dass das System die monopolartige Kontrolle über Infrastruktur untergräbt und den Menschen die Unabhängigkeit zurückgibt.
*   **Digitale Souveränität:** Mein Ziel ist es, die Macht über die Kommunikation von zentralen Instanzen zurück in die Hände der Bevölkerung zu legen. Es ist ein Projekt für eine Gesellschaft, die sich auf den Fall vorbereiten will, in dem offizielle Systeme aufgrund politischer Fehlpriorisierungen oder technischer Überlastung versagen.

## 🚀 Technische Innovation: Abgrenzung
SnowFox Mesh ist kein klassisches "Mesh-Framework", sondern eine **applikationszentrierte Krisen-Kommunikationslösung**. Während bestehende Systeme (Meshtastic, B.A.T.M.A.N.) spezifische Probleme wie Hardware-Reichweite oder Layer-2-Routing lösen, fokussiere ich mich auf:

*   **Zero-App-Adoption:** Durch ein browserbasiertes Proxy-Modell ist die Einstiegshürde bei Null. SnowFox ist ein "Just-in-Time"-Netzwerk, das keine Installation auf Endgeräten erfordert.
*   **Layer-7-Priorisierung:** Mein Fokus liegt auf dem "Survival-Mode". Während klassische Protokolle versuchen, alles zu routen, trifft SnowFox Mesh bei schwachem Signal (< 25%) harte Entscheidungen auf Applikations-Ebene, um Notrufe zu garantieren und den Overhead zu minimieren.
*   **Obfuskation:** Ich priorisiere die Unauffälligkeit des Knotens gegenüber aggressivem Peer-Discovery, um die Identifizierbarkeit in einem überwachten Umfeld zu minimieren.

## 🛠 Technische Spezifikation

### Architektur
*   **Routing:** Dynamische Pfadfindung basierend auf optimierten Routing-Ansätzen (BATMAN/OLSR-Prinzipien).
*   **Peer Discovery:** Automatisierte Erkennung benachbarter Knoten im Funkbereich.
*   **Gateway-Konzept:** Unterstützt Übergangspunkte, ist jedoch für den Betrieb als isoliertes, autarkes Node-to-Node Mesh optimiert.

### Kryptographie & Sicherheit
Ich verfolge den Ansatz, die Hürden für unautorisierte Datenanalyse durch Verschlüsselung und Protokoll-Obfuskation signifikant zu erschweren.

*   **E2E-Verschlüsselung:** Einsatz von [X25519 / Ed25519 / Noise Protocol Framework] zur Absicherung der Payloads.
*   **Sicherheitsmodell:** E2E-Verschlüsselung schützt Inhalte; ich bin mir bewusst, dass Metadaten (Verkehrsmuster, Signalquellen) durch physische Messungen oder Traffic-Analyse prinzipiell untersuchbar bleiben. Das System zielt darauf ab, einfache Inhaltsanalyse zu verhindern. Ich erhebe keinen Anspruch auf absolute Unknackbarkeit gegenüber hochspezialisierten Akteuren, arbeite aber kontinuierlich daran, den Aufwand für potenzielle Angreifer zu maximieren.

## 📊 Vergleich: Behörden vs. SnowFox Mesh

| Merkmal | Behördliche Systeme | SnowFox Mesh |
| :--- | :--- | :--- |
| **Infrastruktur** | Zentral (SPOF-anfällig) | Dezentral (Resilient) |
| **Abhängigkeit** | Strom, Internet, Provider | Keine (Autark) |
| **Priorisierung** | Politisch / Administrativ | Algorithmen (Notruf = Prio 1) |
| **Zielvorgabe** | "Minimaler Standard" | Maximale Stabilität |
| **Kontrolle** | Staat / Konzern | Unabhängig (Open Source) |

## 🛠 Status & Roadmap

*   **Aktueller Status:** Das Fundament steht. Das System ist in einer frühen Entwicklungsphase und noch nicht für den produktiven Notfalleinsatz geeignet. 
*   **Performance:** Ich migriere derzeit von Python-Subprozessen auf eine hochperformante Go-Implementierung, um die Latenz bei hoher Knotendichte zu senken.
*   **Last-Management:** Adaptive Logik: Bei Verbindungsqualität < 25% priorisiert der Knoten ausschließlich kritische Payloads.

## 📝 Entwicklungsgrundsätze & Mitwirkung
Dieses Projekt ist ein fortlaufender Lern- und Entwicklungsprozess. Ich strebe keine absolute Sicherheit an, da IT-Systeme niemals perfekt sind, sondern arbeite an einer stetigen Reduktion der Angriffsfläche.

*   **Transparenz:** Ich lade fachlich versierte Entwickler ein, die Architektur zu hinterfragen und zur Robustheit beizutragen.
*   **Diskurs:** Feedback zu Routing-Algorithmen, Protokoll-Design und Kryptographie ist ausdrücklich erwünscht.

---
*Disclaimer: SnowFox Mesh ist ein experimentelles Open-Source-Projekt. Die Nutzung erfolgt auf eigene Gefahr. Es werden keinerlei Garantien hinsichtlich Verfügbarkeit oder Sicherheit gegeben.*

Dokument erstellt: 2026-07-03
Version: 0.7 (Alpha/Entwicklung)
