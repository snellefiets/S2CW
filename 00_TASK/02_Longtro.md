# Spec2Code Coding Dojo — Ausführliche Anleitung

> Diese Datei ist die lange Version des Tagesablaufs. Sie erklärt, **was ihr tut, warum ihr es tut und wie ihr am besten vorgeht** — Schritt für Schritt, für alle drei Tasks.

---

## Task 1 — High Level & Detail Requirements

**Ziel:** Mit KI Pingpong die zwei Skills schreiben — einen für High Level Requirements, einen für Detail Requirements.

---

### Was ist KI Pingpong?

Bevor ihr anfangt: KI Pingpong bedeutet, dass ihr nicht einfach einen Prompt hinschickt und hofft. Es ist ein echter Dialog — ihr gebt einen Impuls, die KI antwortet, ihr korrigiert, schärft nach, hinterfragt. Hin und her, bis das Ergebnis stimmt.

Das sieht in der Praxis so aus:

1. Ihr beschreibt grob, was ihr wollt
2. Die KI macht einen Vorschlag
3. Ihr sagt, was nicht stimmt oder fehlt
4. Die KI passt an
5. Wiederholen — bis es gut ist

Mehr dazu: [KI PingPong erklärt](assets/00_KI_PingPong.md)

---

### Schritt 0 — Git Projekt auschecken

Das Repository mit dem Input-Dokument liegt hier:

> **[https://github.com/snellefiets/S2CW](https://github.com/snellefiets/S2CW)**

Keine Ahnung, wie man ein Git-Projekt auscheckt? Macht nichts — fragt einfach die KI:

> *„Check mir dieses Git Projekt in diesem Space aus: https://github.com/snellefiets/S2CW"*

Die KI erledigt das für euch. Das ist schon KI Pingpong in Aktion.

---

### Schritt 1 — High Level Requirements

Ihr habt jetzt das Repo und darin das Anforderungsdokument (PDF in `input/`). Jetzt geht es darum, gemeinsam mit der KI herauszufinden: **Was soll diese Software eigentlich können?**

Startet mit einer offenen Frage im Chat:

> *„Ich habe hier ein Anforderungsdokument. Lies es dir durch und erkläre mir in einfachen Worten, was diese Software tun soll."*

Dann: Pingpong. Hinterfragt, was die KI sagt. Fügt hinzu, was fehlt. Streicht, was nicht stimmt. Ziel ist eine Liste von High Level Requirements — also grobe, verständliche Aussagen wie „Nutzer können Produkte suchen" oder „Admins verwalten Berechtigungen".

**Wenn ihr mit dem Ergebnis zufrieden seid**, lasst euch einen Skill daraus schreiben:

> *„Fasse zusammen, was wir erarbeitet haben — als Skill. Also als strukturierte Aufgabenbeschreibung mit Ziel, Eingabe, Vorgehen, Ausgabe und Regeln. Speicher das als Markdown-File."*

Die KI erstellt dann einen Skill, den ihr später immer wieder auf das Dokument anwenden könnt. Alles in **ein File** — eine Übersicht aller High Level Requirements.

Ein fertiger Skill sieht in etwa so aus wie die Skills in [`skills/skill-001-spec-highlevel.md`](../skills/skill-001-spec-highlevel.md) — schaut da gerne rein als Referenz.

---

### Schritt 2 — Detail Requirements

Ihr habt jetzt eure High Level Requirements. Für jeden davon geht ihr jetzt **eine Ebene tiefer**: Was genau bedeutet das? Welche Regeln gelten? Wer ist betroffen? Was passiert, wenn etwas schiefläuft?

Wieder per KI Pingpong:

> *„Lass uns [High Level Requirement X] gemeinsam durchdenken. Was sind die Details dahinter — Nutzergruppen, Geschäftsregeln, Sonderfälle?"*

Wenn die Details für einen High Level Requirement stehen: Skill schreiben lassen, **ein File pro High Level Requirement**.

> 💡 **ProTipp:** Wenn ihr mehrere Details parallel erarbeiten wollt — fragt die KI nach Subagents. Die kann mehrere Aufgaben gleichzeitig bearbeiten.

---

### Schritt 3 — Gemeinsames Debriefing

Alle kommen wieder zusammen. Jedes Team zeigt kurz:
- Wie hat KI Pingpong funktioniert?
- Was war einfach, was war schwierig?
- Was habt ihr rausgekriegt, was ihr nicht erwartet hattet?

Erst dann geht es weiter zu Task 2.

---

## Task 2 — Module & Architektur

**Ziel:** Die SpecKit Skills als Referenz nehmen und mit KI Pingpong einen eigenen, abgespeckten Skill für den konkreten Use Case definieren — nach deren Vorbild, aber im Kleinen.

---

> **Wichtig vor dem Start:** Findet jetzt feste gemischte Teams — je eine Person aus Business und eine aus Technik. Diese Teams bleiben zusammen durch alle weiteren Debriefings und vergleichen immer ihre eigenen Ergebnisse miteinander.

Dann trennt ihr euch: Business geht in einen Raum, Technik in einen anderen.

---

### 🧑‍💼 Business-Zweig

**Ziel:** In den Product Owner Flow reinkommen — mit KI Pingpong durch Specify, Clarify und Modulbausteine arbeiten und spüren: Führt das zu Tickets? Wie fühlt sich das als PO an?

#### Was ist Specify und Clarify?

SpecKit kennt zwei zentrale Operationen, die für euch als Referenz dienen:

- **Specify** — Ihr nehmt ein High Level Requirement und schreibt daraus eine vollständige Feature-Spec: Was soll es können, wer nutzt es, was sind die Erfolgskriterien? Technologie-unabhängig, für Stakeholder geschrieben, nicht für Entwickler. Jedes Feature bekommt **ein eigenes File**.
  → Referenz: [`skills/speckit-commands/speckit.specify.md`](skills/speckit-commands/speckit.specify.md)

- **Clarify** — Ihr nehmt eure Specs und fragt die KI: Was ist noch unklar, zu vage, widersprüchlich? Die KI stellt bis zu fünf gezielte Rückfragen. Ihr beantwortet sie — die Spec wird präziser.
  → Referenz: [`skills/speckit-commands/speckit.clarify.md`](skills/speckit-commands/speckit.clarify.md)

#### Vorgehen

1. **Skills anpassen** — Nehmt die SpecKit Skills als Vorlage und passt sie per KI Pingpong auf eure eigenen High Level Requirements an. Nicht kopieren und fertig — versteht, was der Skill tut, und baut eine vereinfachte Version für euren Use Case. Ein Skill pro Detailebene.

2. **Specify** — Alle Detail Requirements durchspezifizieren. Für jedes Detail ein eigenes File. Haltet es businessnah — was will der Nutzer, warum, unter welchen Bedingungen?

3. **Clarify** — Alle Spec-Files zusammen durch Clarify laufen lassen. Offene Fragen werden sichtbar und beantwortet.

4. **Module überlegen** — Aus Business-Sicht: In welche fachlichen Bausteine lässt sich das Ganze aufteilen? Denkt in Bereichen wie „Kundenverwaltung", „Bestellprozess", „Reporting" — nicht in technischen Komponenten. Auch das macht ihr mit KI Pingpong.

---

### 🛠️ Technik-Zweig

**Ziel:** Mit KI Pingpong herausfinden, wie sich Technik und Architektur sauber dokumentieren lassen — und was die KI braucht, um damit gut arbeiten zu können.

#### Die Kernidee: Ideen kopieren, nicht Skills

Schaut euch den SpecKit Clarify-Skill an: [`skills/speckit-commands/speckit.clarify.md`](skills/speckit-commands/speckit.clarify.md)

Was macht der? Er nimmt eine Spec, sucht gezielt nach Lücken und Unklarheiten, und stellt maximal fünf gezielte Rückfragen — bis die Spec vollständig ist.

Jetzt die entscheidende Frage: **Was wäre, wenn man dasselbe für Architektur macht?**

Nicht den Skill kopieren. Die **Idee** dahinter kopieren und zweckentfremden:
- Clarify fragt: *„Was ist in dieser Feature-Spec noch unklar?"*
- Euer Architektur-Skill fragt: *„Was ist in dieser Architektur-Beschreibung noch unklar?"*

Das Prinzip ist identisch — der Anwendungsfall ist ein völlig anderer. Genau darum geht es in Task 2 auf Technikseite: erkennen, dass ein gutes Konzept portierbar ist, und es für den eigenen Zweck neu bauen. Mit KI Pingpong.

Startet so:
> *„Schau dir diesen Clarify-Skill an. Was ist die Kernidee dahinter? Wie könnten wir dasselbe Prinzip nutzen, um Architektur-Dokumente zu hinterfragen?"*

#### Vorgehen

1. **Technische Anforderungen ableiten** — Schaut euch die High Level Requirements an und fragt gemeinsam mit der KI: Was brauchen wir technisch, um das umzusetzen? Welche Systeme, Schnittstellen, Datenhaltung? KI Pingpong: grob rein, verfeinern, nochmal.

2. **Grobe Architektur entwickeln** — Wie könnte eine Architektur aussehen? Bewusst grob halten — kein vollständiges System-Design. Ziel: ein Bild davon, welche Teile es gibt und wie sie zusammenhängen.

3. **Darstellungsform finden** — Das ist ein Experiment: Welche Form liest die KI am besten? Probiert verschiedene Varianten aus — Fließtext, Stichpunkte, strukturiertes Markdown, ASCII-Diagramm. Fragt die KI direkt:
   > *„Welches Format wäre für dich am einfachsten zu verarbeiten, wenn ich dir eine Architektur beschreibe?"*

4. **Bausteine identifizieren** — Welche technischen Komponenten gibt es? Frontend, Backend, Datenbank, externe Services? Auch hier: KI Pingpong, bis die Liste vollständig und sinnvoll ist.

---

### 🔁 Roadmap (Business & Technik parallel)

Der Scope ist gesetzt — jetzt nutzt das. Mit KI Pingpong alle MVP-Specs in eine sinnvolle Reihenfolge bringen.

- **Business:** In welcher Reihenfolge sollte man die Features abarbeiten / priorisieren? Was hat den größten Nutzen zuerst?
- **Technik:** In welcher Reihenfolge lassen sich die Bausteine implementieren? Was sind Abhängigkeiten, was kann parallel?

Jede Seite erstellt ihre eigene Roadmap — aus der jeweiligen Perspektive, auf Basis der gleichen MVP-Specs.

---

### 🔁 Gemeinsames Debriefing

Die gemischten Teams kommen wieder zusammen. Die zwei Roadmaps werden abgeglichen: Was passt zusammen, wo gibt es Konflikte? Ziel ist eine gemeinsame, abgestimmte Roadmap — und ein klares Bild davon, was als nächstes gebaut wird.

---

## Task 3 — Scoping via CLAUDE.md / Copilot Instructions

**Ziel:** Den MVP-Scope festschreiben — so dass die KI ihn ab jetzt immer kennt, egal was man fragt.

---

### Der Trick: CLAUDE.md und Copilot Instructions

`CLAUDE.md` und `.github/copilot-instructions.md` sind spezielle Dateien, die von der KI bei **jedem einzelnen Prompt automatisch mitgelesen** werden — ohne dass ihr sie jedes Mal anhängen oder erwähnen müsst. Was dort steht, gilt immer.

Das bedeutet: Wenn ihr dort schreibt „Arbeite immer nur im MVP-Scope, MVP bedeutet nur die Kundenstrecke, kein Login", dann hält sich die KI daran — auch wenn ihr einfach fragt „Wie würde man das implementieren?"

Das ist kein Trick, das ist Absicht. Nutzt es.

---

### 🧑‍💼 Business-Zweig

**Ziel:** In den Product Owner Flow reinkommen — mit KI Pingpong durch Specify, Clarify und Modulbausteine arbeiten und spüren: Führt das zu Tickets? Wie fühlt sich das als PO an?

1. **MVP markieren** — Geht durch eure High Level und Detail Requirements und kennzeichnet: Was ist MVP, was ist out of scope? Das kann so einfach sein wie ein `[MVP]`-Tag oder eine eigene Spalte in eurer Übersicht.

2. **Scope präzisieren** — Was genau bedeutet MVP für euren Use Case? Zum Beispiel: „MVP = nur Kundenstrecke, kein Admin-Bereich, kein Login". Macht das explizit und konkret.

3. **CLAUDE.md schreiben** — Schreibt den Scope als feste Anweisung in eine `CLAUDE.md`-Datei im Root des Projekts:
   > *„Wir arbeiten ausschließlich im MVP-Scope. MVP bedeutet: [eure Definition]. Alles außerhalb des MVP-Scopes ist out of scope und soll nicht berücksichtigt werden."*
   
   Testet danach: Stellt eine Frage zu einem Feature außerhalb des MVPs. Schränkt die KI die Antwort ein?

---

### 🛠️ Technik-Zweig

**Ziel:** Mit KI Pingpong herausfinden, wie sich Technik und Architektur sauber dokumentieren lassen.

1. **Technischen MVP-Scope ableiten** — Welche Bausteine und Architekturteile sind für das MVP relevant, welche fallen raus? Mit KI Pingpong durcharbeiten.

2. **Copilot Instructions / CLAUDE.md schreiben** — Technische Constraints und Scope als feste Anweisung hinterlegen. Zum Beispiel:
   > *„Wir bauen ein Frontend-only MVP. Kein echtes Backend. APIs werden gemockt. Technologie: [eure Wahl]. Scope: nur Kundenstrecke."*

3. **Verifizieren** — Stellt Fragen außerhalb des Scopes und schaut, ob die KI ablehnt oder einschränkt. KI Pingpong zum Testen des eigenen Scopings.

---

### 🔁 Roadmap (Business & Technik parallel)

Der Scope ist jetzt gesetzt und in der `CLAUDE.md` verankert. Nutzt das: Die KI weiß ab jetzt immer, was MVP ist — ohne dass ihr es wiederholen müsst.

Jetzt erstellt jede Seite per KI Pingpong eine Roadmap, die **nur noch MVP-Inhalte** enthält:

- **Business:** In welcher Reihenfolge sollte man die MVP-Features abarbeiten und priorisieren?
- **Technik:** In welcher Reihenfolge lassen sich die MVP-Bausteine implementieren?

---

### 🔁 Gemeinsames Debriefing

Alle kommen zusammen — gemischte Teams. Jedes Team gleicht seine Business-Roadmap mit der Technik-Roadmap ab:

- Was deckt sich?
- Wo gibt es Konflikte (Business will X zuerst, Technik sagt Y muss vorher)?
- Was ist die finale, gemeinsame Reihenfolge?

Am Ende steht eine abgestimmte MVP-Roadmap — das Fundament für alles, was danach kommt.
