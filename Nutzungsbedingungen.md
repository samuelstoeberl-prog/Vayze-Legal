# Nutzungsbedingungen

**Vayze App – Entscheidungshilfe für iOS und Android**

**Version:** 2.0.1
**Stand:** 17. Februar 2026

**Anbieter:** Samuel Stöberl / Vayze Apps  
**Adresse:** Josef-Schwab-Straße 7, 94559 Niederwinkling, Deutschland  
**E-Mail:** vayze.app@gmail.com

---

## Präambel

Diese Nutzungsbedingungen regeln die Verwendung der Vayze App ("App"). Mit der Installation und Nutzung der App erklärst du dich mit diesen Bedingungen einverstanden.

**Wichtige Änderung gegenüber früheren Versionen:** Diese Version korrigiert die Beschreibung der tatsächlich eingesetzten Cloud-Dienste, Drittanbieter und technischen Funktionen der App.

---

## §1 Anbieter und Vertragspartner

**Samuel Stöberl / Vayze Apps**  
Josef-Schwab-Straße 7  
94559 Niederwinkling  
Deutschland  
E-Mail: vayze.app@gmail.com

---

## §2 Leistungsumfang der App

### §2.1 Grundfunktionen

Vayze ist eine mobile Anwendung für iOS und Android, die dich bei Entscheidungen unterstützt. Die App bietet:

- **Entscheidungsboards:** Strukturierte Bewertung von Optionen nach verschiedenen Kriterien mit Gewichtung und Score-Berechnung
- **Modi:** Mehrere Entscheidungsmethoden (z.B. PMI, Pro/Contra, Gewichtete Kriterien, 6 Thinking Hats)
- **Journal-Funktion:** Reflexion und Dokumentation von Entscheidungen mit Texten, Fotos und Sprachnotizen
- **Insights:** Lokale Analyse deines Entscheidungsverhaltens mit personalisierten Einblicken
- **Account-System:** Optionales Benutzerkonto für Cloud-basierte Funktionen
- **Push-Benachrichtigungen:** Erinnerungen, Streak-Warnungen und Re-Engagement-Nachrichten

### §2.2 Privacy-First mit Cloud-Komponenten

**Lokale Datenspeicherung:**  
Alle deine persönlichen Inhalte (Boards, Karten, Bewertungen, Journal-Einträge mit Texten, Fotos und Sprachnotizen) werden ausschließlich lokal auf deinem Gerät gespeichert. Wir haben keinen Zugriff auf diese Daten.

**Cloud-Funktionen:**  
Für Account-Verwaltung und Push-Benachrichtigungen nutzen wir Cloud-Dienste von Google (Firebase). Dabei werden ausschließlich Account-bezogene Daten und technische Metadaten verarbeitet (siehe Datenschutzerklärung).

### §2.3 Verfügbarkeit

Wir bemühen uns um eine möglichst hohe Verfügbarkeit der App und der Cloud-Dienste. Es besteht jedoch kein Anspruch auf ununterbrochene Verfügbarkeit. Wartungsarbeiten, technische Störungen oder höhere Gewalt können zu vorübergehenden Ausfällen führen.

### §2.4 Verhaltens-Profiling und Personalisierung

Die App analysiert dein Entscheidungsverhalten lokal auf deinem Gerät, um dir personalisierte Einblicke zu geben:

- **Nutzer-Archetypen:** Kategorisierung deines Entscheidungsstils (z.B. "Der Sichere Entscheider", "Der Vorsichtige Analytiker")
- **Musteranalyse:** Erkennung von Stärken, Wachstumsbereichen und Bias-Tendenzen
- **Personalisierte Empfehlungen:** Vorschläge zur Verbesserung deiner Entscheidungsfindung

**Wichtig:** Diese Analyse geschieht ausschließlich lokal auf deinem Gerät mittels regelbasierter Algorithmen. Es wird kein Machine Learning oder künstliche Intelligenz im engeren Sinne eingesetzt. Die Ergebnisse werden niemals an unsere Server oder Dritte übertragen.

---

## §3 Account und Registrierung

### §3.1 Account-Erstellung

Die Nutzung der App ist grundsätzlich ohne Account möglich. Ein Account ist erforderlich, wenn du folgende Funktionen nutzen möchtest:

- Push-Benachrichtigungen
- Cloud-basierte Streak-Verfolgung
- Zukünftige Synchronisationsfunktionen (in Planung)

Für die Registrierung benötigst du eine gültige E-Mail-Adresse und ein sicheres Passwort.

### §3.2 Pflichten des Nutzers

Du verpflichtest dich:

- Wahrheitsgemäße Angaben bei der Registrierung zu machen
- Deine Zugangsdaten geheim zu halten und nicht an Dritte weiterzugeben
- Uns unverzüglich zu informieren, wenn du Anhaltspunkte für einen Missbrauch deines Accounts hast
- Die App nicht missbräuchlich zu nutzen oder für rechtswidrige Zwecke zu verwenden

### §3.3 Account-Sicherheit

Wir setzen technische und organisatorische Maßnahmen ein, um deinen Account zu schützen:

- **Passwort-Hashing:** Dein Passwort wird mit einem iterativen SHA-256-Verfahren (10.000 Runden) mit zufälligem Salt gehasht, bevor es an Firebase übertragen wird
- **Geräte-Fingerprinting:** Zur Erkennung verdächtiger Login-Versuche erstellt die App einen SHA-256-Hash aus Geräteinformationen
- **Sicherheits-Protokoll:** Die App protokolliert Sicherheitsereignisse (Login-Versuche, Account-Änderungen) lokal auf deinem Gerät

Du bist selbst dafür verantwortlich, ein starkes Passwort zu wählen und deine Zugangsdaten sicher zu verwahren.

### §3.4 Account-Löschung

Du kannst deinen Account jederzeit in den App-Einstellungen unter "Account löschen" unwiderruflich löschen.

**Folgen der Account-Löschung:**
- Alle Account-Daten in Firebase (E-Mail, Anzeigename, Push-Tokens, Aktivitätsdaten) werden unwiderruflich gelöscht
- Alle lokalen Daten (Entscheidungen, Boards, Journal-Einträge mit Fotos und Sprachnotizen) werden vom Gerät entfernt
- **Sicherheits-Protokoll:** Die lokal gespeicherten Sicherheitsereignisse werden nicht vollständig gelöscht, sondern anonymisiert. Die E-Mail-Adresse in den Events wird durch `[deleted]` ersetzt, aber die Geräteinformationen und Zeitstempel bleiben aus Sicherheitsgründen erhalten (Betrugsprävention, Nachvollziehbarkeit von Sicherheitsvorfällen)

**Eine Wiederherstellung gelöschter Daten ist nicht möglich.**

---

## §4 Datenschutz und Datenverarbeitung

### §4.1 Geltung der Datenschutzerklärung

Für die Verarbeitung personenbezogener Daten gilt unsere separate Datenschutzerklärung, die integraler Bestandteil dieser Nutzungsbedingungen ist.

### §4.2 Lokale Datenspeicherung

Alle deine Entscheidungsinhalte werden ausschließlich lokal auf deinem Gerät gespeichert:

- Boards und Karten mit allen Bewertungen
- Journal-Einträge mit Texten, Fotos (bis zu 5 pro Eintrag) und Sprachnotizen
- Kommentare und Checklisten auf Karten
- Onboarding-Umfragedaten (Entscheidungskontext, bevorzugter Stil, gewünschte Ergebnisse)
- Lokale Profiling-Ergebnisse (Archetypen, Musteranalyse)

**Diese Daten verlassen niemals dein Gerät** und werden nicht an uns oder Dritte übertragen.

### §4.3 Cloud-Speicherung

Für die Bereitstellung bestimmter Funktionen speichern wir folgende Daten in der Cloud (Firebase/Google LLC, USA):

- **Account-Daten:** E-Mail-Adresse, Passwort (verschlüsselt), Anzeigename, Benutzer-ID
- **Push-Notification-Daten:** Expo Push Token, Plattform (iOS/Android), App-Version
- **Aktivitätsdaten für Benachrichtigungslogik:** Zeitstempel der letzten Entscheidung, Streak-Anzahl

**Entscheidungsinhalte (Boards, Karten, Journal-Texte, Fotos, Sprachnotizen) werden NICHT in der Cloud gespeichert.**

### §4.4 Android-Backup

Die App erlaubt Android-System-Backups. Das bedeutet, dass deine lokal gespeicherten App-Daten in Android-Cloud-Backups (Google Drive) enthalten sein können, sofern du diese Funktion auf deinem Gerät aktiviert hast. Du kannst Android-Backups für Vayze in den Android-Einstellungen unter "Google > Sicherung" deaktivieren.

---

## §5 Geistiges Eigentum und Lizenzen

### §5.1 Urheberrechte

Die App, einschließlich aller Inhalte, Designs, Grafiken, Texte und Software, ist urheberrechtlich geschützt. Alle Rechte liegen bei Samuel Stöberl / Vayze Apps oder unseren Lizenzgebern.

### §5.2 Nutzungslizenz

Mit dem Download der App erhältst du eine nicht-exklusive, nicht-übertragbare, widerrufliche Lizenz zur persönlichen, nicht-kommerziellen Nutzung der App auf deinen eigenen Geräten.

### §5.3 Verbotene Handlungen

Folgende Handlungen sind untersagt:

- Reverse Engineering, Dekompilierung oder Disassemblierung der App
- Entfernung oder Veränderung von Urheberrechtsvermerken
- Kommerzielle Nutzung ohne schriftliche Genehmigung
- Verbreitung, Verkauf oder Vermietung der App
- Verwendung automatisierter Systeme (Bots, Scraper) zur Interaktion mit der App

---

## §6 Push-Benachrichtigungen

### §6.1 Funktionsweise

Die App bietet folgende Push-Benachrichtigungen an:

**Implementierte Benachrichtigungs-Typen:**
1. **Streak-Warnungen:** Tägliche automatische Prüfung (20:00 UTC) aller Benutzer durch unsere Cloud Functions. Wenn du an einem Tag keine Entscheidung getroffen hast und dein Streak unterbrochen zu werden droht, erhältst du eine Warnung
2. **Re-Engagement:** Tägliche automatische Prüfung (10:00 UTC) aller Benutzer. Wenn du 7 oder mehr Tage inaktiv warst, erhältst du eine Erinnerungs-Nachricht
3. **Streak-Meilensteine:** Automatische Glückwunsch-Benachrichtigung bei Erreichen von Streak-Meilensteinen (ausgelöst beim Erstellen einer Entscheidung)
4. **Broadcast-Benachrichtigungen:** Gelegentliche Nachrichten an alle Benutzer (z.B. wichtige Updates, neue Features)

**Technische Umsetzung:**
- Nutzung von Firebase Cloud Functions zur Benachrichtigungslogik
- Zustellung über Expo Push Notification Service
- Automatische Subscription zum Firebase Cloud Messaging Topic `all_users`
- Speicherung deines Push-Tokens in Firebase Firestore unter `users/{userId}/tokens/{token}`

### §6.2 Einwilligung und Widerruf

Push-Benachrichtigungen erfordern deine ausdrückliche Einwilligung bei der ersten Verwendung. Du kannst diese Einwilligung jederzeit widerrufen:

- In den App-Einstellungen unter "Benachrichtigungen"
- In den Geräte-Einstellungen deines Smartphones

Der Widerruf führt dazu, dass du keine Push-Benachrichtigungen mehr erhältst. Die bereits gespeicherten Push-Tokens werden bei der nächsten Synchronisation aus der Datenbank entfernt.

---

## §7 Berechtigungen

### §7.1 Erforderliche Berechtigungen

Die App benötigt folgende Geräte-Berechtigungen:

**Automatisch erteilte Berechtigungen:**
- **INTERNET:** Netzwerkzugriff für Account-Verwaltung und Push-Benachrichtigungen
- **RECEIVE_BOOT_COMPLETED:** Neuregistrierung von Benachrichtigungen nach Geräte-Neustart
- **VIBRATE:** Vibration bei eingehenden Benachrichtigungen
- **SCHEDULE_EXACT_ALARM:** Zeitgenaue Zustellung von geplanten Benachrichtigungen
- **MODIFY_AUDIO_SETTINGS:** Anpassung der Audio-Einstellungen für Sprachnotizen

**Berechtigungen mit Zustimmungsabfrage (Runtime Permissions):**
- **Kamera:** Aufnahme von Fotos für Journal-Einträge (optional)
- **Fotobibliothek (READ_EXTERNAL_STORAGE / iOS-Foto-Zugriff):** Auswahl vorhandener Fotos aus deiner Galerie (optional)
- **Mikrofon (RECORD_AUDIO):** Aufnahme von Sprachnotizen für Journal-Einträge (optional)
- **Speicher (WRITE_EXTERNAL_STORAGE, Android < 13):** Speicherung von Foto- und Audio-Dateien (optional)
- **Push-Benachrichtigungen:** Empfang von Erinnerungen und Streak-Warnungen (optional)

**Entwickler-Berechtigungen (nur in Debug-Builds):**
- **SYSTEM_ALERT_WINDOW:** Anzeige von Entwickler-Tools über anderen Apps (nur für Testzwecke)

### §7.2 Optionale Funktionen

Die App funktioniert auch ohne Erteilung der optionalen Berechtigungen (Kamera, Fotobibliothek, Mikrofon, Push-Benachrichtigungen). In diesem Fall stehen dir lediglich die entsprechenden Funktionen (Foto-/Audio-Anhänge, Benachrichtigungen) nicht zur Verfügung.

Du kannst alle erteilten Berechtigungen jederzeit in den Geräte-Einstellungen widerrufen.

---

## §8 Haftungsausschluss

### §8.1 Keine Rechtsberatung

Vayze ist ein Werkzeug zur Strukturierung und Reflexion von Entscheidungen. Die App bietet keine Rechtsberatung, Finanzberatung, medizinische Beratung oder sonstige professionelle Beratung. Für wichtige Entscheidungen solltest du zusätzlich qualifizierte Fachleute konsultieren.

### §8.2 Gewährleistung

Wir bemühen uns um eine fehlerfreie Funktion der App, können diese jedoch nicht garantieren. Die App wird "wie sie ist" bereitgestellt, ohne ausdrückliche oder stillschweigende Gewährleistung.

**Wir haften nicht für:**
- Datenverlust aufgrund technischer Fehler oder Geräte-Defekte
- Fehlentscheidungen, die aufgrund der Nutzung der App getroffen wurden
- Inkompatibilitäten mit bestimmten Geräten oder Betriebssystem-Versionen
- Schäden durch höhere Gewalt, Stromausfälle, Internetausfälle oder Drittanbieter-Dienste

### §8.3 Haftungsbegrenzung

Die Haftung für leichte Fahrlässigkeit ist ausgeschlossen, soweit nicht vertragswesentliche Pflichten (Kardinalpflichten) oder Schäden aus der Verletzung des Lebens, des Körpers oder der Gesundheit betroffen sind.

Bei Verletzung wesentlicher Vertragspflichten durch leichte Fahrlässigkeit ist die Haftung auf den vertragstypischen, vorhersehbaren Schaden begrenzt.

Die Haftung nach dem Produkthaftungsgesetz bleibt unberührt.

---

## §9 Drittanbieter-Dienste

### §9.1 Eingesetzte Dienste

Für die Bereitstellung der App nutzen wir folgende Drittanbieter-Dienste:

| Dienst | Anbieter | Zweck |
|--------|----------|-------|
| Firebase Authentication | Google LLC, USA | Account-Verwaltung, Login, Passwort-Reset |
| Firebase Firestore | Google LLC, USA | Speicherung von Push-Tokens, Aktivitätsdaten |
| Firebase Cloud Functions | Google LLC, USA | Serverlose Logik für Push-Benachrichtigungen |
| Expo Push Notification Service | Expo Inc., USA | Technische Zustellung von Push-Benachrichtigungen |
| Firebase Analytics (optional, derzeit inaktiv) | Google LLC, USA | Nutzungsstatistiken (nur mit Opt-in) |

**Datenschutzerklärungen der Drittanbieter:**
- Google Firebase: https://firebase.google.com/support/privacy
- Expo: https://expo.dev/privacy

**Nutzungsbedingungen der Drittanbieter:**
- Google Firebase: https://firebase.google.com/terms
- Expo: https://expo.dev/terms

### §9.2 Datenübertragung in die USA

Alle eingesetzten Cloud-Dienste werden von Anbietern mit Sitz in den USA betrieben. Die Datenübertragung erfolgt auf Grundlage der EU-Standardvertragsklauseln gemäß Art. 46 Abs. 2 lit. c DSGVO.

**Hinweis:** Die USA verfügen derzeit nicht über ein von der EU-Kommission anerkanntes angemessenes Datenschutzniveau. Es besteht das Risiko, dass US-Behörden unter bestimmten Umständen auf deine Daten zugreifen können.

### §9.3 Keine Kontrolle über Drittanbieter

Wir haben keine Kontrolle über die Datenverarbeitungspraktiken der Drittanbieter-Dienste. Für deren Datenschutzpraktiken sind die jeweiligen Anbieter verantwortlich. Wir empfehlen dir, die Datenschutzerklärungen der Drittanbieter zu lesen.

### §9.4 Account-Löschung bei Drittanbietern

Bei der Löschung deines Vayze-Accounts werden deine Daten auch bei unseren Auftragsverarbeitern (Firebase) gelöscht. Bitte beachte jedoch, dass die Sicherheits-Protokolle auf deinem Gerät anonymisiert, aber nicht vollständig gelöscht werden (siehe §3.4).

---

## §10 Analytics und Tracking

### §10.1 Analytics-Funktion

Die App verfügt über eine Analytics-Infrastruktur (Firebase Analytics), die **derzeit de facto inaktiv** ist, da das benötigte Firebase Analytics Modul nicht in der App-Konfiguration aktiviert ist.

**Status:** Die Analytics-Einstellung in der App ist vorhanden, hat aber derzeit keine Funktion.

**Falls die Analytics-Funktion in zukünftigen Versionen aktiviert wird**, würden bei aktivierter Analytics-Einstellung folgende Event-Daten an Google Firebase Analytics (USA) übertragen:
- Entscheidungs-Events (Start, Abschluss) mit Modus, Kategorie und Gewichtungs-Preset
- Journal-Events (Erstellung, Löschung) mit Metadaten (Wortanzahl, ob Fotos/Audio vorhanden)
- Navigation-Events (Tab-Wechsel)

**Keine Übertragung von Inhalten:** Es werden niemals die Inhalte deiner Entscheidungen, Karten oder Journal-Einträge an Analytics übertragen.

### §10.2 Opt-out

Du kannst die Analytics-Funktion jederzeit in den App-Einstellungen deaktivieren (auch wenn sie derzeit nicht aktiv ist). Standardmäßig ist Analytics deaktiviert.

### §10.3 Kein Tracking außerhalb der App

Wir verwenden keine Tracking-Pixel, Cookies oder ähnliche Technologien zur Verfolgung deines Verhaltens außerhalb der App.

---

## §11 Änderungen der Nutzungsbedingungen

Wir behalten uns vor, diese Nutzungsbedingungen bei Bedarf zu ändern. Über wesentliche Änderungen informieren wir dich rechtzeitig über die App oder per E-Mail.

Wenn du den geänderten Nutzungsbedingungen nicht zustimmst, kannst du die Nutzung der App einstellen und deinen Account löschen.

Die weitere Nutzung der App nach Inkrafttreten der Änderungen gilt als Zustimmung zu den neuen Bedingungen.

---

## §12 Kündigung und Sperrung

### §12.1 Kündigung durch den Nutzer

Du kannst die Nutzung der App jederzeit ohne Einhaltung einer Frist beenden, indem du die App deinstallierst und ggf. deinen Account löschst.

### §12.2 Sperrung durch uns

Wir behalten uns vor, deinen Account zu sperren oder zu löschen, wenn:

- Du gegen diese Nutzungsbedingungen verstößt
- Du die App für rechtswidrige Zwecke nutzt
- Du missbräuchliche oder betrügerische Aktivitäten durchführst
- Wir dazu gesetzlich verpflichtet sind

Im Falle einer Sperrung informieren wir dich über die Gründe, sofern keine rechtlichen Gründe dagegensprechen.

---

## §13 Schlussbestimmungen

### §13.1 Anwendbares Recht

Für diese Nutzungsbedingungen und die Nutzung der App gilt deutsches Recht unter Ausschluss des UN-Kaufrechts.

### §13.2 Gerichtsstand

Sofern du Kaufmann, juristische Person des öffentlichen Rechts oder öffentlich-rechtliches Sondervermögen bist, ist ausschließlicher Gerichtsstand für alle Streitigkeiten Straubing, Deutschland.

### §13.3 Salvatorische Klausel

Sollten einzelne Bestimmungen dieser Nutzungsbedingungen unwirksam sein oder werden, bleibt die Wirksamkeit der übrigen Bestimmungen davon unberührt. Die unwirksame Bestimmung wird durch eine wirksame ersetzt, die dem wirtschaftlichen Zweck der unwirksamen Bestimmung am nächsten kommt.

### §13.4 Vertragssprache

Die Vertragssprache ist Deutsch.

---

## §14 Kontakt

Bei Fragen zu diesen Nutzungsbedingungen kannst du uns jederzeit kontaktieren:

**Samuel Stöberl / Vayze Apps**  
Josef-Schwab-Straße 7  
94559 Niederwinkling  
Deutschland  
E-Mail: vayze.app@gmail.com

---

## Änderungshistorie

### Version 2.0.1 (17. Februar 2026) – Redaktionelle Korrekturen und Übersetzungsverbesserungen

**Korrekturen:**
1. **§6.1 Firestore-Pfad:** Korrektur von `users/{userId}/tokens/{token}` zu `users/{email}/tokens/{token}` in der englischen Version (konsistent mit Datenschutzerklärung)
2. **Alle nicht-deutschen Versionen:** Sprachvorrang-Klausel ergänzt in §13.4: „Bei Abweichungen zwischen den Sprachversionen gilt die deutsche Version."
3. **Indonesische Version:** Hinweis auf indonesisches Datenschutzgesetz (UU PDP, Nr. 27/2022) in der Präambel ergänzt
4. **Chinesische Version:** Sprachvorrang-Klausel in der Präambel und §13.4 ergänzt

---

### Version 2.0.0 (7. Februar 2025) – Vollständige Überarbeitung nach Legal-Technical-Audit

**Kritische Korrekturen:**

- **§9.4 "Keine weiteren Drittanbieter"** → Ersetzt durch vollständige Auflistung aller eingesetzten Drittanbieter-Dienste (Firebase Authentication, Firestore, Cloud Functions, Expo Push, Firebase Analytics) mit Links zu deren Datenschutzerklärungen und Nutzungsbedingungen

- **§10.1 "Keine Cloud"** → Ersetzt durch korrekte Beschreibung: Account-Daten, Push-Tokens und Aktivitätsdaten in Firebase (Google Cloud), Entscheidungsinhalte bleiben lokal

- **§10.3 "Kein Tracking"** → Korrigiert: Analytics-Infrastruktur existiert, derzeit de facto inaktiv, aber bei Aktivierung würden Events an Google Firebase Analytics gesendet

- **§2.4 "Keine KI"** → Ergänzt: App führt lokales Verhaltens-Profiling durch (Archetypen, Musteranalyse, Empfehlungen) mittels regelbasierter Algorithmen, kein Machine Learning

- **§4.3 "Daten nur lokal"** → Differenziert: Entscheidungsinhalte lokal, Account-Daten, Push-Tokens und Aktivitätsdaten in der Cloud

- **§6 Benachrichtigungen** → Vollständige Aktualisierung mit tatsächlichen Implementierungsdetails (Cloud Functions, Cron-Jobs um 20:00 UTC und 10:00 UTC, Topic-Subscriptions, Streak-Warnungen, Re-Engagement, Broadcast, Meilensteine)

- **§3.4 / §9.4 Account-Löschung** → Ergänzt: Sicherheitsereignisse werden anonymisiert, aber nicht vollständig gelöscht (E-Mail wird zu `[deleted]`, Gerätedaten bleiben erhalten)

**Neue Abschnitte:**

- §9.2: Datenübertragung in die USA mit Hinweis auf EU-Standardvertragsklauseln und Risiken
- §2.2: Klare Differenzierung zwischen lokaler und Cloud-Speicherung
- §4.4: Hinweis auf Android-Backup-Funktion
- Detaillierte Tabelle aller Drittanbieter-Dienste in §9.1
- Vollständige Liste aller Berechtigungen in §7.1

**Entfernte Falschaussagen:**

- "Keine weiteren Drittanbieter"
- "Keine Cloud-Speicherung"
- "Kein Tracking" (ohne Einschränkung)
- "Push-Benachrichtigungen derzeit nicht implementiert"
- "Keine KI" (ohne Erwähnung des lokalen Profilings)

### Version 1.4.0 (vorherige Version)

- Initiale öffentliche Version (enthielt die oben genannten Ungenauigkeiten und Auslassungen)

---

**Stand:** 17. Februar 2026
**Version:** 2.0.1
