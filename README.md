# 🦊 SnowFox Mesh

SnowFox Mesh ist ein dezentrales, autarkes Kommunikationsprotokoll. Ich entwickle dieses System als Antwort auf die zunehmende Fragilität zentralisierter Infrastrukturen. Das Ziel ist die Schaffung eines Netzwerks, das auch dann funktioniert, wenn staatliche oder kommerzielle Systeme (ISP-Gateways, Stromnetz) ausfallen.

## 📋 Motivation & Philosophie
Ich arbeite alleine an diesem Projekt, um maximale Unabhängigkeit zu wahren. Ich bin nicht an Firmeninteressen oder regulatorische Vorgaben gebunden, was mir erlaubt, die Stabilität und Sicherheit der Bevölkerung als höchste Priorität zu definieren.

*   **Autonomie:** Ich lehne die Abhängigkeit von zentralen „Single Points of Failure“ ab.
*   **Reaktion auf Infrastruktur-Schwächen:** Ich sehe eine Fehlentwicklung in der aktuellen Priorisierung von Ressourcen. Mein Fokus liegt auf einer funktionalen, krisenfesten Basis-Infrastruktur.
*   **Umgang mit Restriktionen:** Ich bin mir bewusst, dass ein solches Tool auf Widerstand stoßen könnte. Ein kritischer Diskurs über digitale Souveränität ist ein inhärenter Teil dieses Projekts. Mein Ziel ist nicht die Konfrontation, sondern die Schaffung einer technischen Alternative, die im Ernstfall die Kommunikation sichert.

## 🛠 Technische Spezifikation

### Architektur-Konzept
SnowFox Mesh nutzt ein Peer-to-Peer-Routing, um Nachrichten über mehrere Hops zu relayen. 

*   **Routing-Konzept:** Ich implementiere [BATMAN / OLSR-basierte] Ansätze zur dynamischen Pfadfindung.
*   **Peer Discovery:** Mechanismen zur automatischen Erkennung benachbarter Knoten im Funkbereich.
*   **NAT-Traversal:** Strategien zur Überwindung von Netzwerk-Restriktionen zwischen Endpunkten.
*   **Gateway-Konzept:** Dedizierte Knoten fungieren als Übergangspunkte, das Protokoll ist jedoch darauf ausgelegt, auch in isolierten lokalen Meshes (Node-to-Node) zu kommunizieren.

### Kryptographie & Sicherheit
Ich verfolge den Ansatz, die Hürden für unautorisierte Datenanalyse durch Verschlüsselung und Protokoll-Obfuskation signifikant zu erschweren.

*   **E2E-Verschlüsselung:** Einsatz von [X25519 / Ed25519 / Noise Protocol Framework] zur Absicherung der Payloads.
*   **Sicherheitsmodell:** Ich erkenne an, dass E2E-Verschlüsselung zwar Inhalte schützt, Metadaten (Verkehrsmuster, Signalquellen) jedoch durch physische Messungen oder Traffic-Analyse prinzipiell untersuchbar bleiben.
*   **Abgrenzung:** Das System zielt darauf ab, passive Beobachtung und einfache Inhaltsanalyse zu verhindern. Ich erhebe keinen Anspruch auf Unknackbarkeit gegenüber hochspezialisierten Akteuren, sondern arbeite kontinuierlich daran, den Aufwand für potenzielle Angreifer so hoch wie möglich zu schrauben.

## 📊 Vergleich: Behörden vs. SnowFox Mesh

| Merkmal | Behördliche Systeme | SnowFox Mesh |
| :--- | :--- | :--- |
| **Infrastruktur** | Zentral (SPOF-anfällig) | Dezentral (Resilient) |
| **Abhängigkeit** | Strom, Internet, Provider | Keine (Autark) |
| **Priorisierung** | Politisch / Administrativ | Algorithmen (Notruf = Prio 1) |
| **Einsatzbarkeit** | Bürokratisch gebunden | Sofort / Jederzeit |
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
Version: 0.5 (Alpha/Entwicklung)
