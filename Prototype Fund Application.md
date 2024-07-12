
# Info

- https://prototypefund.de/bewerbung/faq/
- https://prototypefund.de/die-perfekte-bewerbung/
- https://bewerbung.prototypefund.de/documents/2/PTF_Checkliste_07.2023.pdf

# Application
https://bewerbung.prototypefund.de/prototype-fund-runde-16/

### Projekttitel *

World-Wide-Lab

### Name für den Account *

WorldWideLab

Unter diesem Namen wird das Benutzerkonto auf der Bewerbungsplattform angelegt. Es kann sich dabei um einen Klarnamen, ein Pseudonym oder einen Teamnamen handeln.

### Hast du einen Account bei GitHub, BitBucket oder einer ähnlichen Plattform? Wenn ja, gib bitte den entsprechenden Link an.

https://github.com/jansim

### Beschreibe dein Projekt kurz. *

Limit this field to 100 words.

World-Wide-Lab ist eine neue Platform für die Online-Datenergebung und zur Entwicklung partizipativer Methoden. Ziel des Projektes ist es eine Plattform zu entwickeln, welche einfach genug ist um auch von Nicht-Entwicklern genutzt zu werden und gleichzeitig flexibel genug um neue und interaktive Methoden der Datensammlung auszuprobieren. Dabei werden die Komplexitäten der Datenerhebung im Web (automatische Skalierung, Umgang mit unzuverlässigem Internet, Hosting, etc.) so weit wie möglich von der Software gehandhabt und verständlich dokumentiert. Die Hauptzielgruppe des Projektes sind dabei sog. Citizen Scientists; das heißt Initiativen bei denen die Allgemeinheit gemeinsam Daten sammelt, sowohl als Teilnehmer wie auch als Organisatoren.

### Welche gesellschaftliche Herausforderung willst du mit dem Projekt angehen? *

Limit this field to 175 words.

Das Projekt zielt darauf ab, die Kluft zwischen technologischer Kompetenz und partizipativer Wissenschaft zu überbrücken. In einer Welt, in der Daten immer mehr an Bedeutung gewinnen, ist es entscheidend, dass jeder die Möglichkeit hat, erstens an der Erhebung von Daten teilzunehmen und zweitens selbst Daten zu erheben. Aktuell gibt es jedoch noch immer weite Teile der Bevölkerung die nicht ausreichend in vorliegenden Daten repräsentiert sind und deren  Perspektiven dadurch in resultierenden (KI-)Systemen nicht wiedergespiegelt werden.

Die Plattform soll es Bürgerwissenschaftler:innen ermöglichen, ohne umfangreiche technische Kenntnisse Projekte zu initiieren und zu leiten. Dies fördert das Engagement der Öffentlichkeit und stärkt die demokratische Teilhabe am Diskurs. Indem die Plattform technischen Barrieren abbaut, können auch unterrepräsentierte Gruppen ihre Perspektiven einbringen und wertvolle Daten liefern. So wird die Vielfalt an Daten erhöht und eine inklusivere Gesellschaft wie auch Wissenschaft gefördert. World-Wide-Lab halt als Ziel, dass das Potenzial von Citizen Science voll ausgeschöpft wird und dass sowohl Erkenntnisse wie auch Daten nicht nur von einer kleinen Gruppe von Experten, sondern von der gesamten Gesellschaft generiert werden können.

### Wie willst du dein Projekt technisch umsetzen? *

Limit this field to 175 words.

World-Wide-Lab (WWL) wird als Server-Applikation für Node.js in Typescript entwickelt. Dies hat den Vorteil, dass sowohl für den Server (Backend) wie auch für die Begleitbibliotheken (Frontend), welche zur einfachen Nutzung mitentwickelt werden, die gleiche Programmiersprache verwendet werden kann. Die Server-Applikation wird außerdem so entwickelt, dass sie mittels Electron als eigenständige Applikation auf Window, Mac und Linux installiert werden kann um neue WWL-Projekte lokal ausprobieren zu können, bevor man diese im Internet "deployed".

Die Server Applikation speichert Daten in einer Datenbank (lokal: SQLite; online: Postgres) und ist bewusst so entwickelt, dass mehrere Instanzen der Applikation die gleiche Datenbank verwenden können um eine flexible Skalierung zu ermöglichen. Neben dem Server ist die wichtigste Hilfsbibliothek der Client, welcher im Browser der Nutzer läuft und mit dem Server kommuniziert. Dabei werden Komplexitäten wie mehrere Versuche bei fehlgeschlagener Kommunikation etc. im Client gehandhabt. Aufbauend auf dem Client werden dann spezielle Integrationen für beliebte Citizen Science Bibliotheken (z.B. jsPsych) entwickelt um die Nutzung auch für nicht-Informatiker möglichst einfach zu gestalten. Es ist außerdem eine Hilfsbibliothek für Cloude-deployments via pulumi geplant.

### Hast du schon an der Idee gearbeitet? Wenn ja, beschreibe kurz den aktuellen Stand und erkläre die geplanten Neuerungen. *

Limit this field to 100 words.

Ich habe über die letzten Monate hinweg einen ersten Prototypen von World-Wide-Lab entwickelt, welcher erfolgreich mehrere tausend Datenpunkte am Tag verarbeitet. Es gibt aktuell bereits erste Versionen des Servers, Klienten, der Elektron-basierten Applikation, der Deployment-Bibliothek, eine erste Integration, sowie Teile der Dokumentation. Es gibt außerdem bereits eine erste CI/CD Pipeline, welche automatisch ein gewisses Maß an Code Qualität sicherstellt, sowie Docker Images und die Applikation generiert.

Die nächsten Schritte in der Entwicklung werden ein offizielles Release der Software und weitere praktische Tests mit externen Nutzern sein, welche bereits ihr Interesse bekundet haben. Darüber hinaus sind viele weitere Features geplant.

### Link zum bestehenden Projekt (falls vorhanden)

### Welche ähnlichen Ansätze gibt es schon und was wird dein Projekt anders bzw. besser machen? *

Limit this field to 60 words.

Es gibt mehrere ähnliche Ansätze die jedoch entweder closed source und bezahlt sind (Pavlovia, cognition.run) und/oder nicht auf die spezifischen Probleme von Citizen Science (wie z.B. spontane Spikes an Traffic) ausgelegt sind (JATOS). Es gibt eine FOSS Bibliothek welche ein ähnliches Problem angeht (Pushkin), die jedoch so komplex ist, dass sie nicht viel genutzt wird und relativ fragil ist. 

### Wer ist die Zielgruppe und wie soll dein Projekt sie erreichen? *

Limit this field to 100 words.

Alle, welche an gemeinsamer Datensammlung und insbesondere Citizen Science interessiert sind. Dazu gehören einerseits Forscher:innen der Natur und Sozialwissenschaften, das Projekt richtet sich jedoch gezielt darüber hinaus auch an die Allgemeinheit. Spezifisch ist es geplant auch Bürgerinitiativen und "grassroots" Kampagnen zur gemeinsamen Datensammlung zu unterstützen.

Um die Zielgruppen zu erreichen, sind Online- und Präsenz-Workshops geplant, in denen World-Wide-Lab erklärt wird. Diese könnten zum Beispiel mit Initiativen wie dem Civic Data Lab durchgeführt werden und es gibt bereits ein Netzwerk an interessierten Forschungsgruppen. Außerdem soll eine aktive Community aufgebaut werden, welche sich idealerweise auch gegenseitig bei Problemen helfen kann.

### An welchen Software-Projekten hast du / habt ihr bisher gearbeitet? Bei Open-Source-Projekten bitte einen Link zum Repository angeben.

Max. 3 Projektbeispiele angeben (mit Namen und/oder Link zum Repository)

Limit this field to 100 words.

Ich war damals der Hauptentwickler und helfe immer noch bei der Instandhaltung von https://www.themusiclab.org/, einer Citizen Science Website mit > 4 Millionen Teilnehmern bisher. Die Website fungiert auch als Testbett für die erste Version von World-Wide-Lab. Ich habe außerdem bereits an mehreren Open Source Projekten gearbeitet. Unter anderem habe ich im Rahmen meiner Promotion ein R Paket zur Kodierung von Berufen (https://github.com/occupationMeasurement/occupationMeasurement) entwickelt und war Hauptentwickler für ein Modul für die Statistik Software JASP (https://github.com/jasp-stats/jaspPower und https://github.com/jansim/jaspPower, da beim release der Code kopiert statt geforkt wurde). Ich habe außerdem bereits mehrfach mittels Rull Requests Änderungen zu anderen FOSS Projekten beigesteuert.

### Erfahrung, Hintergrund, Motivation, Perspektive: Was sollen wir über dich (bzw. euch) wissen und bei der Auswahl berücksichtigen? *

Limit this field to 100 words.

Ich forsche im Rahmen meiner Promotion zu Fairness in Machine Learning (FairML) und habe in diesem Kontext bemerkt, dass sowohl in FairML als auch darüber hinaus sehr viele Probleme letztendlich auf Probleme in Daten zurückgeführt werden können. Da ich mich in meiner Forschung viel mit dieser Art von Problemen beschäftige, würde ich durch dieses Projekt gerne mehr an einer (potenziellen) Lösung für diese Probleme arbeiten. Durch meine abgeschlossene Ausbildung als Fachinformatiker und Erfahrung in der Entwicklung und Support von themusiclab.org, fühle ich mich dabei optimal darauf vorbereitet dieses Projekt erfolgreich durchzuführen.
### Bewerbt ihr euch als Team um die Förderung? *

Ja
Nein

### Namen der Teammitglieder

Limit this field to 30 words.

### Wie viele Stunden willst du (bzw. will das Team) in den 6 Monaten Förderzeitraum insgesamt an der Umsetzung arbeiten? *

Bitte eine Zahl eintragen - max. 950 h.
Die Maximalförderung von 47.500€ leitet sich aus einer Vollzeitstelle für eine Person für ein halbes Jahr (ca. 950 h) ab. Dies entspricht einem Stundensatz von 50 €. Wer einen höheren Stundensatz abrufen will, muss mit Rechnungen belegen, diese bereits als Entwickler*in abgerufen zu haben. Die Stundenanzahl und die entsprechende Finanzierung darf natürlich auch zwischen mehreren Teammitgliedern aufgeteilt werden. Alle Förderprojekte einer Runde haben Anspruch auf die maximale Fördersumme, eine hohe Stundenzahl beeinflusst also nicht die Auswahl.

### Skizziere kurz die wichtigsten Meilensteine, die im Förderzeitraum umgesetzt werden sollen. *

Limit this field to 100 words.

Das wichtigste Feature, welches ich im Förderzeitraum gerne umsetzen möchte ist die Möglichkeit Dateien hochzuladen. Dies ist ein etwas komplexeres Problem, da sowohl Autoskalierung wie auch unterschiedliche Cloud Provider / Hosting Strategien unterstützt werden sollen. Hier gibt es drei Meilensteine: (#1) grundlegender Support für Uploads, (#2) Upload von HTML-Studien und (#3) Upload von Teilnehmer-Antworten.
Sobald diese Meilensteine erfüllt sind, ist es geplant, in einem neuen Meilenstein (#4) die Möglichkeit zur Datenspende mittels einer neuen Hilfsbibliothek zu unterstützen. Darüber hinaus ist die Sammlung von Paradaten (#5) und damit Erkennung von Bot / KI generierten Daten (#6) geplant.

### Ich habe die Checkliste für Bewerber*innen gelesen. *

on

### Ich habe die Informationen zum Datenschutz gelesen und stimme der Verwendung meiner Daten im Rahmen der Programmziele des Prototype Funds zu. *

on

### Ich bin über 18 Jahre alt und habe meinen Hauptwohnsitz in Deutschland. *

on

### Ich bin damit einverstanden, die Projektergebnisse unter einer Open-Source-Lizenz (z. B. MIT-Lizenz), öffentlich zugänglich (z. B. über Github oder BitBucket) zur Verfügung zu stellen. *

on