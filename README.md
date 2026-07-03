# 🦊 SnowFox Mesh: Architektur für eine autonome Krisenkommunikation

## 📋 Mission Statement
SnowFox Mesh ist ein dezentrales, autarkes Kommunikationsnetzwerk, das als unmittelbare Antwort auf die wachsende Fragilität zentralisierter Infrastrukturen entwickelt wurde. In einer Welt, in der moderne Kommunikationssysteme – seien es staatliche Warnsysteme oder kommerzielle Netze – zunehmend von instabilen Versorgungsnetzen (Strom, Internet) und bürokratischer Lähmung abhängig sind, bietet SnowFox Mesh eine technologische Alternative. Hier steht der Schutz der Bevölkerung und die garantierte Erreichbarkeit an absolut erster Stelle.

## ⚠️ Die Problematik: Warum offizielle Systeme scheitern

Aktuelle behördliche Warn- und Kommunikationssysteme in Deutschland und anderen Teilen der Welt leiden unter strukturellen Defiziten, die im Ernstfall zu einer Sicherheitslücke führen:

*   **Zentralisierung als Schwachstelle:** Bestehende Systeme basieren auf zentralen Funkmasten und Rechenzentren, die bei großflächigen Krisen (Stromausfall, Cyberattacken, physische Zerstörung) zum Ausfall führen[cite: 1].
*   **Mentalität des "Minimalismus":** Politisch und administrativ wird oft das Ziel verfolgt: *"Das Nötigste ist genug"*. Wenn jedoch Menschenleben auf dem Spiel stehen, darf diese Mentalität nicht existieren. SnowFox Mesh strebt 100 % Zuverlässigkeit an, da bei Leben und Tod keine Kompromisse akzeptiert werden[cite: 1].
*   **Fehlpriorisierung ökonomischer Mittel:** Öffentliche Budgets fließen oft in die Interessen großer Konzerne oder Rüstungsprojekte, während die Basis-Infrastruktur zur Resilienz der eigenen Bevölkerung vernachlässigt wird[cite: 1].
*   **Bürokratische Blockaden:** Komplexe gesetzliche und regulatorische Rahmenbedingungen verhindern oft schnelle, effiziente Lösungen. Die Sicherheit wird durch Umständlichkeit gefährdet (z. B. regulatorische Hürden, die im Notfall irrelevant sind)[cite: 1].

## 📊 Vergleich: Behörden vs. SnowFox Mesh

| Merkmal | Behördliche Systeme | SnowFox Mesh |
| :--- | :--- | :--- |
| **Infrastruktur** | Zentral (SPOF-anfällig) | Dezentral (Resilient) |
| **Abhängigkeit** | Strom, Internet, Provider | Keine (Autark) |
| **Priorisierung** | Administrativ / Politisch | Algorithmen (Notruf = Prio 1) |
| **Einsatzbarkeit** | Bürokratisch gebunden | Sofort / Jederzeit |
| **Zielvorgabe** | "Das Nötigste reicht" | 100% Funktionalität |
| **Kontrolle** | Staat / Konzern | Unabhängig (Open Source) |

## 💡 Der SnowFox-Ansatz: Freiheit & Autonomie

SnowFox Mesh ist ein technologischer Gegenentwurf. Wir sind nicht an Firmeninteressen, staatliche Vorgaben oder restriktive regulatorische Regelungen gebunden, die den Schutz der Bürger behindern könnten.

*   **Technologische Unabhängigkeit:** Das System benötigt keine speziellen Lizenzen oder Hardware-Freigaben. Jeder Knoten im Netzwerk ist gleichberechtigt[cite: 1].
*   **Plattform-Unabhängigkeit:** Durch das browserbasierte Web-Interface können Nutzer mit jedem internetfähigen Gerät (Apple, Google, Samsung etc.) ohne App-Installation Teil des Mesh-Netzwerks werden[cite: 1].
*   **Intelligentes Last-Management:** Bei schwacher Signalqualität (Regulierung bei < 50% / < 25%) schaltet das System automatisch in einen "Notfall-Modus". Kritische Notrufe werden priorisiert durchgestellt, während unwichtiger Datenverkehr gedrosselt wird, um das Mesh stabil zu halten[cite: 1].
*   **Absolute Freiheit:** Da das System kein kommerzielles Produkt ist, unterliegt es keinem Profit-Druck. Die Regeln bestimmen sich ausschließlich durch die Notwendigkeit der Funktionsfähigkeit[cite: 1].

## 🛠 Status & Roadmap (Development Status)

SnowFox Mesh befindet sich derzeit in der aktiven Entwicklungsphase. Es ist ein komplexes Unterfangen, ein solches System von Grund auf zu entwickeln.

*   **Aktueller Status:** Das Fundament ist gelegt, aber das System ist **noch nicht zu 100 % einsatzbereit**. Viele Komponenten befinden sich in einem frühen Stadium oder werden derzeit konzeptionell überarbeitet.
*   **Technische Schwerpunkte:**
    *   **Mehr-Hop-Routing:** Implementierung von OLSR/BATMAN zur Flächendeckung[cite: 1].
    *   **Selbstheilung:** Entwicklung von Watchdogs und Health-Checks zur automatischen Fehlerbehebung bei Abstürzen[cite: 1].
    *   **Performance:** Übergang von Python-Subprozessen auf eine hochperformante Go-Implementierung, um Latenzzeiten massiv zu senken[cite: 1].
*   **Qualitätsanspruch:** Die Entwicklung folgt der Roadmap aus `SnowFox-Net.md`. Erst wenn alle Funktionen unter realen Bedingungen validiert wurden, wird das System als vollwertige Alternative betrachtet[cite: 1].

*Hinweis: SnowFox Mesh ist ein Open-Source-Projekt. Die Nutzung und Weiterentwicklung dient ausschließlich der technologischen Resilienz und dem Schutz der Bevölkerung in Krisenzeiten. Da sich das System in einer frühen Entwicklungsphase befindet, sind kontinuierliche Tests und Code-Optimierungen für den angestrebten 100%-Standard notwendig.*

---
Dokument erstellt: 2026-07-03
Version: 1.0 (Entwicklung)
