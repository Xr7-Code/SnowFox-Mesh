# 🦊 SnowFoxOS: Krisen- und Kriegsszenario (Einsatzdokumentation)

Dieses Dokument simuliert das Verhalten und die Protokolle von **SnowFoxOS** und dem integrierten **SnowFox-Mesh** im Falle einer hybriden, modernen Kriegsführung. 

---

## 🛑 Rahmenbedingungen des Szenarios
* **Schauplatz:** Eine durchschnittliche Kleinstadt (ca. 10.000 Einwohner).
* **Infrastruktur:** 10 aktive SnowFoxOS-Knoten (verteilt auf private Haushalte, Rathaus und Feuerwehr). ca. 8.000 Smartphones/Laptops in der Bevölkerung.
* **Bedrohungslage:** Umfassender Cyberangriff auf das Stromnetz (Blackout), gezieltes Jamming (Funkstörung) staatlicher Frequenzen und Destabilisierung der Kommunikation durch den Aggressor.

---

## 🕒 Chronologischer Ablauf: Krise, Ausfall und Gegenmaßnahmen

<Timeline>
{/* Reason: Chronologische Darstellung des Kriegs-Szenarios über 72 Stunden, bei dem die exakten Zeiten den Verlauf der technologischen Eskalation und das Gegensteuern von SnowFoxOS verdeutlichen. */}
  <TimelineEvent title="Stunde 00:00 – Der Erstschlag (Cyberwar)" time="Tag 1 - 04:00 Uhr">
    Ein koordinierter Angriff auf die Leitsysteme (SCADA) trennt die Region vom europäischen Verbundnetz. **Totaler Blackout.** Das kommerzielle Internet bricht zusammen, DNS-Server sind nicht mehr erreichbar. Mobilfunkmasten laufen auf Notstrom-Batterien.
  </TimelineEvent>
  <TimelineEvent title="Stunde 00:05 – Autonomer Systemwechsel" time="Tag 1 - 04:05 Uhr">
    Die Go-Hintergrunddienste der 10 SnowFoxOS-Knoten registrieren den dauerhaften Verlust des Internet-Gateways. Das OS reagiert vollautomatisch: **Weg 1 (WLAN)** wechselt in den offenen Captive-Portal-Modus (*„FoxNet“*). Die RNode-Modems für **Weg 2 & 3 (LoRa)** werden initialisiert.
  </TimelineEvent>
  <TimelineEvent title="Stunde 00:30 – Das Sterben der Masten" time="Tag 1 - 04:30 Uhr">
    Die Pufferbatterien der regulären Mobilfunkmasten sterben. Das offizielle Netz ist komplett tot. Smartphones der Bürger scannen panisch nach Signalen und buchen sich automatisch in das starke, lokale WLAN der SnowFoxOS-Knoten ein. Erste Informationswelle rollt über das lokale Wiki.
  </TimelineEvent>
  <TimelineEvent title="Stunde 12:00 – Elektronische Kampfführung" time="Tag 1 - 16:00 Uhr">
    Der Feind setzt breitbandige Störsender (Jammer) ein, um den staatlichen Digitalfunk (TETRA) und Satelliten-Uplinks zu blockieren. Auch das militärisch sensible **868-MHz-Band (Weg 3)** meldet plötzlich eine extreme Fehlerrate (Noise Floor steigt massiv).
  </TimelineEvent>
  <TimelineEvent title="Stunde 12:05 – Der manuelle Frequenz-Hebel" time="Tag 1 - 16:05 Uhr">
    Die Admins der Knoten reagieren auf das Jamming. Über das Web-Interface wird der physische Hebel umgelegt: **Weg 3 (868 MHz) wird deaktiviert, Weg 2 (LoRa 2,4 GHz) wird scharfgeschaltet.** Das Mesh taucht im dichten Frequenzmüll des städtischen 2,4-GHz-Bandes (Bluetooth, Mikrowellen, tote WLANs) unter und funkt trotz Störung weiter.
  </TimelineEvent>
  <TimelineEvent title="Stunde 36:00 – Ressourcen-Knappheit" time="Tag 2 - 16:00 Uhr">
    Die Akkus der privaten Knoten sinken unter 20%. Das **5-Prioritäten-System** greift radikal. Alle privaten Chats (P2/P3) und Datentransfers (P1) werden netzweid blockiert. Die verbleibende Energie wird exklusiv für militärische/behördliche Notrufe und System-Routing (P4/P5) reserviert.
  </TimelineEvent>
  <TimelineEvent title="Stunde 72:00 – Dezentraler Sieg" time="Tag 4 - 04:00 Uhr">
    Die Stadt ist physisch isoliert, aber informationstechnisch intakt. Die Einsatzkräfte im Rathaus koordinieren über die krypto-isolierten Reticulum-Kanäle die Verteilung von Brunnenwasser und sichern die medizinische Notversorgung der 10.000 Bürger, während der Feind die Stadt für kommunikativ blind hält.
  </TimelineEvent>
</Timeline>

---

## 🛡️ Taktische Analyse: Warum der Feind scheitert

### 1. Das Protokoll-Dilemma des Angreifers
Militärische Aufklärung sucht nach bekannten Mustern: IP-Header, unverschlüsselte Routing-Tabellen oder MAC-Adressen von bekannten Herstellern. 
* **Die SnowFoxOS-Abwehr:** Reticulum nutzt das kryptografische *Noise-Protokoll*. Ein feindlicher Funkscanner sieht nur unstrukturierte, zufällige Datenblöcke. Da das System asynchron arbeitet und keine permanenten Baken-Signale (Beacons) sendet, bleibt das Mesh für automatisierte Drohnen-Suchsysteme unsichtbar. Es gibt kein dauerhaftes Signal, das man anpeilen könnte.

### 2. Der "Geiz-Modus" gegen Triangulation
Wenn der Feind Funksignale orten will, benötigt er eine gewisse Sendedauer des Ziels, um die Position mathematisch zu berechnen (Triangulation).
* **Die SnowFoxOS-Abwehr:** Durch die strikte Durchsetzung des **5-Prioritäten-Systems** im Katastrophenfall werden Datenpakete auf ein absolutes Minimum komprimiert. Eine P5-Notfallnachricht der Feuerwehr benötigt nur Bruchteile einer Sekunde für die Übertragung durch den Äther. Bevor die feindliche Elektronik den Sender erfassen kann, ist der Funkkanal bereits wieder absolut still.

### 3. Auslastungs-Matrix im Extremfall (Pro Knoten)

| Übertragungsweg | Alltags-Zustand | Kriegs-Zustand (Blackout) | Taktische Funktion im Szenario |
| :--- | :--- | :--- | :--- |
| **Weg 1: WLAN (2,4 GHz)** | Gateway zum Internet | Lokales Captive Portal (Web-Server) | **Pufferwand:** Fängt die 1.000 Endgeräte pro Knoten lokal ab. Verhindert das Fluten des Funknetzes. |
| **Weg 2: LoRa (2,4 GHz)** | Standby / Privates Testnetz | **Primärer Kommunikationskanal** | **Tarnung:** Nutzt CSS-Modulation im überlasteten 2,4-GHz-Band. Unempfindlich gegen Schmalband-Jammer. |
| **Weg 3: LoRa (868 MHz)** | Standby / Reichweitentest | Deaktiviert nach Stunde 12:00 | **Weitstrecken-Reserve:** Wird nur kurzzeitig für P5-Meldungen zu Nachbarstädten hochgefahren. |

> **Einsatzbefehl für Admins im Kriegsfall:** 
> Niemals Dateien oder Bilder (P1) im Mesh freigeben. Das unbefugte Senden von Medien blockiert den Duty-Cycle und gefährdet die Anonymität des Knotens durch verlängerte Sendezeiten. Das System erzwingt diesen Zustand bei Gateway-Verlust automatisch.
