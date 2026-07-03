# 🦊 SnowFox Mesh

SnowFox Mesh ist ein dezentrales, autarkes Kommunikationsprotokoll. Ich entwickle dieses System als direkte Antwort auf die zunehmende Fragilität zentralisierter Infrastrukturen und als technisches Instrument zur Sicherung der digitalen Souveränität.

## 🏛 Gesellschaftspolitische Einordnung

Ich beobachte eine kritische Entwicklung: Die Abhängigkeit von zentralen, staatlich oder kommerziell kontrollierten Infrastrukturen führt zu einer systemischen Schwachstelle. Wenn Kommunikation ausschließlich über Masten, Rechenzentren und Internet-Provider läuft, verliert der Bürger seine Handlungsfähigkeit bei deren Ausfall.

*   **Systemische Verwundbarkeit:** Aktuelle Behördensysteme folgen der Logik: „Das Nötigste reicht“. Ich halte dies für ein Versagen, da Sicherheit in Krisenzeiten keine ökonomische Abwägung sein darf, sondern eine garantierte Funktionalität erfordert.
*   **Widerstand als Legitimation:** Die Autonomie meines Systems ist bewusst gewählt. Wenn Firmen oder staatliche Akteure ein solches Tool einschränken oder verbieten wollen, sehe ich dies als Bestätigung seiner Relevanz. Jedes Verbot ist der Beweis, dass das System die monopolartige Kontrolle über die Infrastruktur untergräbt und den Menschen die Unabhängigkeit zurückgibt.
*   **Freiheit durch Dezentralität:** Mein Ziel ist es, die Macht über die Kommunikation von zentralen Instanzen zurück in die Hände der Bevölkerung zu legen. Es ist ein Projekt für eine Gesellschaft, die sich auf den Fall vorbereiten will, in dem offizielle Systeme aufgrund politischer Fehlpriorisierungen oder technischer Überlastung versagen.

## 🛠 Technische Spezifikation

### Architektur-Konzept
SnowFox Mesh nutzt Peer-to-Peer-Routing, um Nachrichten über mehrere Hops zu relayen. 

*   **Routing-Konzept:** Implementierung von [BATMAN / OLSR-basierten] Ansätzen zur dynamischen Pfadfindung.
*   **Peer Discovery:** Mechanismen zur automatischen Erkennung benachbarter Knoten im Funkbereich.
*   **Gateway-Konzept:** Dedizierte Knoten fungieren als Übergangspunkte, das Protokoll ist jedoch darauf ausgelegt, auch in isolierten lokalen Meshes (Node-to-Node) zu kommunizieren.

### Kryptographie & Sicherheit
Ich verfolge den Ansatz, die Hürden für unautorisierte Datenanalyse durch Verschlüsselung und Protokoll-Obfuskation signifikant zu erschweren.

*   **E2E-Verschlüsselung:** Einsatz von [X25519 / Ed25519 / Noise Protocol Framework] zur Absicherung der Payloads.
*   **Sicherheitsmodell:** Ich erkenne an, dass E2E-Verschlüsselung zwar Inhalte schützt, Metadaten (Verkehrsmuster, Signalquellen) jedoch durch physische Messungen oder Traffic-Analyse untersuchbar bleiben. Das System zielt darauf ab, einfache Inhaltsanalyse zu verhindern; es gibt keine Garantie auf absolute Anonymität gegenüber hochspezialisierten Akteuren.

## 📊 Vergleich: Behörden vs. SnowFox Mesh

| Merkmal | Behördliche Systeme | SnowFox Mesh |
| :--- | :--- | :--- |
| **Infrastruktur** | Zentral (SPOF-anfällig) | Dezentral (Resilient) |
| **Abhängigkeit** | Strom, Internet, Provider | Keine (Autark) |
| **Priorisierung** | Politisch / Administrativ | Algorithmen (Notruf = Prio 1) |
| **Zielvorgabe** | "Minimaler Standard" | Maximale Stabilität |
| **Kontrolle** | Staat / Konzern | Unabhängig (Open Source) |

## 🛠 Status & Roadmap

*   **Aktueller Status:** Das Fundament steht. Das System ist in der frühen Entwicklungsphase und noch nicht für den produktiven Notfalleinsatz geeignet. 
*   **Performance:** Ich migriere derzeit von Python-Subprozessen auf eine hochperformante Go-Implementierung, um die Latenz bei hoher Knotendichte zu senken.
*   **Last-Management:** Ein Beispiel für die adaptive Logik: Erkennt ein Knoten eine Verbindungsqualität von < 25%, priorisiert er automatisch ausschließlich "Critical"-Payloads und drosselt den Overhead.

## 📝 Entwicklungsgrundsätze & Mitwirkung
Dieses Projekt ist ein fortlaufender Lern- und Entwicklungsprozess. Ich strebe keine absolute Sicherheit an, da IT-Systeme niemals perfekt sind, sondern arbeite an einer stetigen Reduktion der Angriffsfläche.

*   **Transparenz:** Ich lade fachlich versierte Entwickler ein, die Architektur zu hinterfragen und zur Robustheit beizutragen.
*   **Diskurs:** Feedback zu Routing-Algorithmen, Protokoll-Design und Kryptographie ist ausdrücklich erwünscht.

---
*Disclaimer: SnowFox Mesh ist ein experimentelles Open-Source-Projekt. Die Nutzung erfolgt auf eigene Gefahr. Es werden keinerlei Garantien hinsichtlich Verfügbarkeit oder Sicherheit gegeben.*

Dokument erstellt: 2026-07-03
Version: 0.1 (Alpha/Entwicklung)
