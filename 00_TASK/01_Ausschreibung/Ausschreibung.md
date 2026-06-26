# Ausschreibung: Rail Guide Pets

**Auftraggeber:** Express Transport GmbH  
**Dokumenttyp:** Werkvertrag  
**Veröffentlichung:** 19.03.2026  
**Angebotsfrist:** 24.03.2026  
**Leistungszeitraum:** 26.03.2026 – 31.12.2027  
**Leistungsstandort:** Frankfurt am Main (Nearshore möglich)

---

## Inhaltsverzeichnis

1. [Beschreibung des Themenkontextes](#1-beschreibung-des-themenkontextes)
2. [Gegenstand der Leistung](#2-gegenstand-der-leistung)
3. [Technische Rahmenbedingungen](#3-technische-rahmenbedingungen)
4. [Anforderungen an den Dienstleister](#4-anforderungen-an-den-dienstleister)
5. [Datenschutz & IT-Sicherheit](#5-datenschutz--it-sicherheit)
6. [Rollen im System](#6-rollen-im-system)
7. [Sonstige Bestimmungen](#7-sonstige-bestimmungen)
8. [Ansprechpartner & Einreichung](#8-ansprechpartner--einreichung)

---

## 1. Beschreibung des Themenkontextes

### 1.1 Projektbeschreibung

Die **Express Transport GmbH** ist ein Anbieter von Fernverkehrsleistungen mit Fokus auf Produkt- und Servicequalität. Im Rahmen der Erweiterung des Serviceangebots plant die Express Transport GmbH die Einführung eines neuen, kostenpflichtigen Begleitservices für **alleinreisende Haustiere: Rail Guide Pets**.

Zwei Tierbetreuer des Serviceerbringers **Proki Tierevents** begleiten dabei maximal 15 Haustiere fachkundig und fürsorglich auf ausgewählten Fernverkehrsverbindungen. Der Service beginnt mit der Übergabe am Startbahnhof durch die abgebende Person und endet mit der Übergabe an eine abholende Person am Zielbahnhof. Ein Einstieg/Ausstieg an Zwischenhalten ist nicht möglich.

Im **MVP-Zeitraum (Pilotphase)** wird das Angebot über die **Sommer- und Herbstferien 2026** getestet – an allen Freitagen und Sonntagen zwischen dem **26. Juni 2026** und dem **8. November 2026** auf ausgewählten Strecken mit hohem Reiseaufkommen.

---

## 2. Gegenstand der Leistung

### 2.1 Gegenstand und Zielsetzung

Gegenstand dieser Ausschreibung ist die **Konzeption, Umsetzung, Test, Dokumentation, Inbetriebnahme und Übergabe** eines webbasierten Buchungstools für den Rail Guide Pets-Service im MVP-Umfang sowie – sofern beauftragt – der anschließende Betrieb.

Das Buchungssystem besteht aus drei Bereichen:

1. **Kunden-Microsite (Frontend)** zur Suche, Auswahl und Buchung von Rail Guide Pets-Fahrten inkl. Erfassung der erforderlichen Haustier- und Kontaktinformationen sowie Bereitstellung von Buchungsbestätigungen und Dokumenten.
2. **Backoffice/Proki-Bereich** für den Super Admin zur Anlage und Steuerung der buchbaren Verbindungen, Disposition, Datenexporten, Ausnahmebearbeitung sowie Rollenzuweisung.
3. **Betreuenden-Bereich** (rollenbasiert, verbindungsbezogen) zur Anzeige der zugewiesenen Verbindungen und Haustierlisten sowie zur Dokumentation der Übergaben und operativer Ereignisse.

### 2.2 Angebotsstruktur

Das Angebot ist in folgende vier Teile zu gliedern:

| Teil | Inhalt |
|------|--------|
| 1 | Konzeption, Umsetzung, Test, Dokumentation, Inbetriebnahme und Übergabe des Buchungstools (MVP) |
| 2 | Anbindungsprozess an die Partnerschnittstelle der Express Transport GmbH |
| 3 | Betrieb des Buchungstools und Datenverarbeitung nach Go-Live |
| 4 | Weiterentwicklung zur Ausbaustufe auf Basis der definierten Use Cases |

### 2.3 Liefergegenstände und Liefertermine

> **Hinweis:** Die nachfolgenden Termine sind Soll-Termine und müssen auf Machbarkeit geprüft werden. Falls nicht umsetzbar, ist frühestmöglich ein alternativer Liefertermin vorzuschlagen. Zu langfristige Liefertermine können zum Ausschluss führen.

#### Liefertermin 1 – drei Wochen nach Auftragserteilung (Zwischenlieferung)

- Technisches Design / Architektur (System-, Daten- und Sicherheitsarchitektur), Schnittstellenkonzept, Logging/Audit-Konzept, Retention-/Löschkonzept
- Testkonzept inkl. Testfälle für kritische Pfade (Buchung, Zahlung, Login/Rollen, Übergabe-Dokumentation)
- UX-/UI-Design (Buchungsjourney & Backoffice) inkl. Informationsarchitektur, Copy (DE/EN) und Barrierefreiheitskonzept gemäß WCAG 2.2 Level AA

#### Liefertermin 2 – 15.06.2026 (Zwischenlieferung)

- Implementierter MVP in Staging-/Testumgebung inkl. Kunden-Microsite, Verbindungs-/Verfügbarkeitsanzeige, Buchung inkl. Zahlungsintegration, Bestätigungs-E-Mails und PDF-Generierung
- Backoffice (Proki-Bereich) inkl. Rollen/Rechte, Verbindungsanlage, Gruppenübersichten je Verbindung, Übergabe-Dokumentation (digitale Unterschrift) sowie Reporting-Grundfunktionen
- Testdokumentation der Tests durch den Auftragnehmer

#### Liefertermin 3 – 15.07.2026 (Endlieferung MVP)

- Produktiv gesetzter MVP inkl. Go-Live-Support, Monitoring/Alerting-Basis, Backup/Restore-Nachweis
- Vollständige technische Dokumentation (Setup, Architektur, Schnittstellen, Betrieb, Security, Retention/-Löschung), Übergabedokumentation und Wissenstransfer
- Handbücher/Guides: Kurzhandbuch Backoffice (Super Admin, Betreuende) sowie Admin-Dokumentation

#### Liefertermin 4 – 15.07.2026 (Anbindung Partnerschnittstelle)

- Anbindung an die Partnerschnittstelle der Express Transport GmbH
- Umsetzung der Use Cases, die von der Anbindung der Partnerschnittstelle abhängig sind

#### Liefertermin 5 – ab Go-Live (Betriebsaufnahme / Betriebsphase bis Ende MVP)

- Betriebsaufnahme (Produktionsbetrieb) inkl. Hosting/Plattformbetrieb und technischem Support
- Sicherstellung der Verfügbarkeit (mindestens 99 %, 24/7)
- Monitoring & Alerting im laufenden Betrieb
- Datenverarbeitung und Datenmanagement nach Go-Live
- Betriebsdokumentation & Übergaben im Betrieb

### 2.4 Abnahmekriterien

Für den MVP wird ein Abnahmezeitraum von **drei Wochen** vereinbart. Folgende Kriterien werden geprüft:

- Last-/Performancetest in produktionsnaher Umgebung inkl. Dokumentation
- Testszenarien: Login/Rollen, Verfügbarkeit, Buchung inkl. Zahlung, Bestätigung/PDF/E-Mail, Übergabe
- Alle Fehler der Fehlerklassen 1 und 2 sind behoben
- Für Fehler der Fehlerklassen 3 und 4 wurde eine Bewertung abgegeben und ein Behebungsplan erstellt
- Vollständige Dokumentation liegt vor

Bei Nichterfüllung: Maßnahmenplan und Wiederholungstest; Abnahme erst nach Zielerreichung oder schriftlicher Abweichungsfreigabe.

---

## 3. Technische Rahmenbedingungen

### 3.1 Laufzeitumgebung

Das entwickelte System muss in einer Enterprise Cloud der Express Transport GmbH lauffähig sein. Erlaubte Cloud-Dienstleister:

- AWS Enterprise Cloud Managed
- Azure Enterprise Cloud Managed

### 3.2 Berechtigungssteuerung

Berechtigungen der Nutzer (Tierhalter, Admins, Betreuende) sind durch ein Identity & Access Control Produkt zu verwalten. Eine perspektivische Integration in das Kundenkonto der Express Transport GmbH (Kunden) sowie in das Single Sign On / Microsoft Active Directory (Mitarbeitende) ist vorzusehen.

### 3.3 Browser-Unterstützung

Mindestens folgende Browser müssen unterstützt werden: Chrome, Safari, Firefox, Edge.

### 3.4 Digitale Barrierearmut

Die Barrierearmut gemäß **WCAG 2.2, Level AA** muss nachgewiesen werden.

### 3.5 Performance und Mengengerüste

Folgende Antwortzeiten sind durch einen Last- und Performancetest nachzuweisen:

| Vorgang | Anforderung (95. Perzentil) |
|---------|----------------------------|
| Buchung | ≤ 10 Sekunden |
| Reporterstellung | ≤ 5 Sekunden |
| Alle anderen Frontend-Zugriffe | ≤ 1 Sekunde |

**MVP (abnahmerelevant):**

- Kunden: bis 180 Buchungen/Woche, Peak bis 50 Buchungen/Stunde, zusätzlich Peak bis 1.000 sonstige Aufrufe/Stunde
- Backoffice/Betreuende: 50 gleichzeitige Nutzer, bis 500 Aufrufe/Stunde

**Ausbaustufe (nicht abnahmerelevant für MVP):**

- Kunden: bis 1,5 Mio. Buchungen/Jahr, Peak bis 50.000/Woche
- Backoffice/Betreuende: 200 gleichzeitige Nutzer, bis 2.000 Aufrufe/Stunde

Die Architektur ist so auszulegen, dass eine **Skalierung ohne grundlegende Neuarchitektur** möglich ist.

---

## 4. Anforderungen an den Dienstleister

### 4.1 Fachliche Anforderungen

Der Dienstleister muss nachweisen, dass er über Erfahrung in folgenden Bereichen verfügt:

- Entwicklung und Betrieb von webbasierten Buchungs- und Transaktionssystemen
- Integration von Zahlungsdienstleistern
- Umsetzung von Backoffice-/Admin-Portalen mit rollenbasiertem Zugriff
- Barrierefreie Frontend-Entwicklung (WCAG 2.2 AA)
- Hosting und Betrieb in deutschen oder EU-Cloud-Umgebungen
- Kenntnisse im Bereich DSGVO-konformer Softwareentwicklung

### 4.2 Kaufmännische Anforderungen

- Das Angebot ist im **PDF-Format** einzureichen (optional zusätzlich als Word oder PowerPoint)
- Bestätigung, dass alle gestellten Anforderungen an die Leistungserbringung erfüllt werden
- Beschreibung des Vorgehens, der Meilensteine, des Teams/der Rollen und der Qualitätssicherung
- Darstellung der kaufmännischen Angebotsbestandteile unter Berücksichtigung der genannten Rahmenbedingungen
- Angabe benötigter Beistellleistungen (Zugänge, Ansprechpartner, Inhalte) sowie Annahmen/Abhängigkeiten
- Sonstiges (Risiken, offene Punkte, Ausbaustufen)

---

## 5. Datenschutz & IT-Sicherheit

Die vom Vertrag abgedeckten Informationen und Anwendungen unterliegen einem **sehr hohen Schutzbedarf**. Der Auftragnehmer hat folgende Anforderungen zu erfüllen:

- Umsetzung technischer und organisatorischer Maßnahmen gemäß **DSGVO** (Privacy by Design & Default)
- Verschlüsselungsverfahren nach aktuellem Stand der Technik
- Differenziertes Berechtigungskonzept nach dem **Need-to-know-Prinzip**
- Mandantentrennung (sichere technische Trennung)
- Datenminimierung; Unterstützung der Betroffenenrechte (Berichtigung, Löschung, Auskunft nach Art. 15 DSGVO)
- Exportfunktion für Daten in maschinenlesbarem Format (Recht auf Datenübertragbarkeit)
- Konfigurierbare Aufbewahrungsfristen mit automatisierter Löschung
- **Datenverarbeitung und -speicherung ausschließlich in Deutschland, EU oder EWR**
- Benennung der physischen Standorte der Daten sowie der Zugriffsorte (Wartung, Pflege, Support)

---

## 6. Rollen im System

| Rolle | Beschreibung |
|-------|--------------|
| **Kunde (Tierhalter)** | Sucht, bucht und verwaltet Fahrten für Haustiere; registrierungspflichtig |
| **Super Admin Proki** | Verwaltet Verbindungen, Tierbetreuer, Passagierlisten und Betriebssteuerung im Backoffice |
| **Tierbetreuer (Proki)** | Begleiten die Haustiere und dokumentieren Übergaben und Vorfälle über das Tool |

---

## 7. Sonstige Bestimmungen

- **Verlängerungsoption:** Dieser Vertrag kann vom Auftraggeber nach Ende der Leistungserbringung jährlich um weitere 12 Monate verlängert werden. Die Verlängerungsmitteilung muss spätestens einen Monat vor Ende der Leistungserbringung versendet sein.
- Es gelten vollumfänglich die Bestimmungen des jeweils gültigen Rahmenvertrags der Express Transport GmbH.
- Präsentationen und Anbietergespräche finden ab **25.03.2026** statt. Die Entscheidung wird anschließend gefällt.

---

## 8. Ansprechpartner & Einreichung

Rückfragen zur Ausschreibung sind ausschließlich über das offizielle Anfrageportal einzureichen. Gestellte Fragen sowie die zugehörigen Antworten sind für alle Rahmenvertragspartner einsehbar. Auf die Anonymität der Rückfragen ist zu achten.

Angebote sind einzureichen an:

> **Express Transport GmbH**  
> Projektmanagement Onboard Services  
> Frankfurt am Main  
>
> **Einsendeschluss: 24.03.2026**
