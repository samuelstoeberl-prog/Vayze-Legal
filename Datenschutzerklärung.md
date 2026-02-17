# Datenschutzerklärung

**Vayze App – Entscheidungshilfe für iOS und Android**

**Version:** 2.0.2
**Stand:** 17. Februar 2026
**Anbieter:** Samuel Stöberl / Vayze Apps  
**Adresse:** Josef-Schwab-Straße 7, 94559 Niederwinkling, Deutschland  
**E-Mail:** vayze.app@gmail.com

---

## Präambel

Wir nehmen den Schutz deiner personenbezogenen Daten ernst. Diese Datenschutzerklärung informiert dich umfassend darüber, welche Daten bei der Nutzung der Vayze App erhoben, verarbeitet und gespeichert werden. Die Verarbeitung erfolgt im Einklang mit der Datenschutz-Grundverordnung (DSGVO) und dem Bundesdatenschutzgesetz (BDSG).

**Wichtige Änderung gegenüber früheren Versionen:** Diese Version korrigiert und vervollständigt die Offenlegung der tatsächlich eingesetzten Drittanbieter-Dienste, Datenverarbeitungen und technischen Funktionen der App.

---

## 1. Verantwortlicher

Verantwortlich für die Datenverarbeitung im Sinne der DSGVO:

**Samuel Stöberl / Vayze Apps**  
Josef-Schwab-Straße 7  
94559 Niederwinkling  
Deutschland  
E-Mail: vayze.app@gmail.com

---

## 2. Allgemeine Informationen zur Datenverarbeitung

### 2.1 Grundprinzip: Privacy First mit Cloud-Komponenten

Vayze wurde mit dem Grundsatz "Privacy First" entwickelt. Deine **Entscheidungsinhalte** (Boards, Karten, Bewertungen, Journal-Einträge mit Texten, Fotos und Sprachnotizen) werden ausschließlich lokal auf deinem Gerät gespeichert und niemals an unsere Server oder Dritte übertragen.

Für die Bereitstellung bestimmter Funktionen (Account-Verwaltung, Push-Benachrichtigungen) nutzen wir jedoch Cloud-Dienste von Google (Firebase). Dabei werden **Account-bezogene Daten** und **technische Metadaten** verarbeitet, wie in dieser Erklärung detailliert beschrieben.

### 2.2 Zweck der Datenverarbeitung

Wir verarbeiten personenbezogene Daten zu folgenden Zwecken:

- Bereitstellung und Betrieb der App-Funktionen
- Account-Verwaltung (Registrierung, Login, Passwort-Reset)
- Versand von Push-Benachrichtigungen (Erinnerungen, Streak-Warnungen, Re-Engagement)
- Technische Sicherheit und Betrugsprävention
- Nutzungsstatistiken (nur mit deiner ausdrücklichen Einwilligung via Analytics-Einstellung)

### 2.3 Rechtsgrundlagen

Die Verarbeitung deiner Daten erfolgt auf folgenden Rechtsgrundlagen:

- **Art. 6 Abs. 1 lit. a DSGVO** (Einwilligung): Analytics-Erfassung, Push-Benachrichtigungen
- **Art. 6 Abs. 1 lit. b DSGVO** (Vertragserfüllung): Account-Verwaltung, Bereitstellung der App-Funktionen
- **Art. 6 Abs. 1 lit. f DSGVO** (berechtigtes Interesse): IT-Sicherheit, Betrugsprävention, technische Stabilität

---

## 3. Erhobene Daten und Speicherorte

### 3.1 Account-Daten (Cloud-Speicherung)

Bei der Registrierung und Nutzung deines Accounts werden folgende Daten in der Cloud gespeichert:

| Datentyp | Zweck | Speicherort | Rechtsgrundlage |
|----------|-------|-------------|------------------|
| E-Mail-Adresse | Account-Identifikation, Login, Passwort-Reset | Firebase Authentication (Google LLC, USA) | Art. 6 Abs. 1 lit. b DSGVO |
| Passwort (verschlüsselt) | Account-Sicherheit | Firebase Authentication (Google LLC, USA) | Art. 6 Abs. 1 lit. b DSGVO |
| Anzeigename | Personalisierung | Firebase Authentication (Google LLC, USA) | Art. 6 Abs. 1 lit. b DSGVO |
| Benutzer-ID (UUID) | Interne Identifikation | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. b DSGVO |
| Account-Erstellungsdatum | Verwaltung, Support | Firebase Authentication (Google LLC, USA) | Art. 6 Abs. 1 lit. b DSGVO |

**Verschlüsselung:** Dein Passwort wird vor der Übertragung mit einem iterativen SHA-256-Verfahren (10.000 Runden) mit zufälligem Salt gehasht. Firebase speichert zusätzlich eine eigene verschlüsselte Version.

### 3.2 Push-Benachrichtigungs-Daten (Cloud-Speicherung)

Für den Versand von Push-Benachrichtigungen werden folgende Daten in der Cloud gespeichert:

| Datentyp | Zweck | Speicherort | Rechtsgrundlage |
|----------|-------|-------------|------------------|
| Expo Push Token | Eindeutige Identifikation deines Geräts für Push-Zustellung | Firebase Firestore unter `users/{email}/tokens/{token}` | Art. 6 Abs. 1 lit. a DSGVO |
| Plattform (iOS/Android) | Plattformspezifische Zustellung | Firebase Firestore | Art. 6 Abs. 1 lit. a DSGVO |
| App-Version | Kompatibilitätsprüfung | Firebase Firestore | Art. 6 Abs. 1 lit. a DSGVO |
| Registrierungszeitpunkt | Token-Verwaltung | Firebase Firestore | Art. 6 Abs. 1 lit. a DSGVO |
| Benachrichtigungs-Protokoll | Nachvollziehbarkeit gesendeter Push-Benachrichtigungen | Firebase Firestore unter `users/{email}/notificationLog` | Art. 6 Abs. 1 lit. a DSGVO |

**Wichtiger Hinweis:** Deine E-Mail-Adresse wird als Firestore-Dokument-ID verwendet (Pfad: `users/{email}`). Dies bedeutet, dass die E-Mail-Adresse in der Firestore-Datenbankstruktur sichtbar ist.

**Benachrichtigungs-Protokoll:** Jede an dich gesendete Push-Benachrichtigung wird in Firestore protokolliert mit:
- Titel der Benachrichtigung
- Benachrichtigungstext (body)
- Payload-Daten (z.B. Typ, Ziel-Screen, Streak-Anzahl)
- Server-Zeitstempel (wann gesendet)
- Status (ob geöffnet)

**Topic-Subscription:** Dein Gerät wird automatisch zum Firebase Cloud Messaging Topic `all_users` hinzugefügt, um Broadcast-Benachrichtigungen zu ermöglichen.

### 3.3 Aktivitätsdaten für Benachrichtigungslogik (Cloud-Verarbeitung)

Um personalisierte Push-Benachrichtigungen zu versenden (z.B. Streak-Warnungen, Re-Engagement), verarbeiten unsere Cloud Functions folgende Daten:

| Datentyp | Zweck | Verarbeitungsort | Rechtsgrundlage |
|----------|-------|------------------|------------------|
| **Entscheidungs-Zeitstempel** | | | |
| `createdAt` (aus `decisions`-Subcollection) | Zeitpunkt der Entscheidungserstellung | Firebase Cloud Functions (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| `completedAt` (aus `decisions`-Subcollection) | Zeitpunkt des Entscheidungsabschlusses | Firebase Cloud Functions (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| **Aktivitäts-Tracking** | | | |
| `activity.lastDecisionAt` | Zeitstempel der letzten Entscheidung | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| `activity.currentStreak` | Anzahl aufeinanderfolgender Tage mit Entscheidungen | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| `activity.longestStreak` | Längster erreichter Streak | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| `activity.lastReEngagementAt` | Zeitstempel der letzten Re-Engagement-Benachrichtigung | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| `activity.lastSyncedAt` | Zeitstempel der letzten Streak-Synchronisation | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| **Rate-Limiting** | | | |
| `notificationSettings.rateLimits.lastSentAt` | ISO-Zeitstempel der letzten gesendeten Benachrichtigung | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| `notificationSettings.rateLimits.sentToday` | Zähler der heute gesendeten Benachrichtigungen | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |
| **Benutzer-Identifikation** | | | |
| E-Mail-Adresse (als Dokument-ID) | Zuordnung der Aktivitätsdaten zum Benutzer | Firebase Firestore (Google LLC, USA) | Art. 6 Abs. 1 lit. a DSGVO |

**Verarbeitung:** Unsere Cloud Functions führen täglich um 20:00 UTC (Streak-Warnung) und 10:00 UTC (Re-Engagement) automatisierte Prüfungen durch. Dabei werden ALLE registrierten Benutzer-Dokumente in Firestore durchlaufen und anhand der Aktivitätsdaten analysiert.

**Zugriff auf Entscheidungs-Zeitstempel:** Die Cloud Functions greifen auf die Subcollection `users/{email}/decisions` zu und lesen die Felder `createdAt` und `completedAt` aller abgeschlossenen Entscheidungen, um Streaks und Inaktivität zu berechnen. **Wichtig:** Es werden nur Zeitstempel gelesen, keine Entscheidungsinhalte (Titel, Beschreibungen, Bewertungen etc.).

### 3.4 Entscheidungsinhalte (lokale Speicherung)

Alle deine persönlichen Inhalte werden ausschließlich lokal auf deinem Gerät gespeichert:

- **Boards und Karten:** Titel, Beschreibungen, Kategorien, Gewichtungen, Bewertungen, Tags, Priorisierungen
- **Entscheidungs-Empfehlungen:** Berechnete Scores, Empfehlungen, Zeitstempel
- **Journal-Einträge:** Texte, Reflexionen, Entscheidungskontext, zusätzliche Notizen (Freitext)
- **Foto-Anhänge:** Bis zu 5 Fotos pro Journal-Eintrag (lokale Dateipfade)
- **Sprachnotizen:** Audio-Aufnahmen mit Dauer (lokale Dateien)
- **Kommentare:** Texte auf Board-Karten mit Zeitstempel
- **Checklisten:** Aufgaben mit Erledigt-Status auf Board-Karten
- **Onboarding-Daten:** Entscheidungskontext, bevorzugter Entscheidungsstil (z.B. Analytisch, Impulsiv, Überdenker), gewünschte Ergebnisse

**Diese Daten verlassen niemals dein Gerät** und werden nicht an uns oder Dritte übertragen.

**Journal-Limit im kostenlosen Tarif:** Die Erstellung von Journal-Einträgen unterliegt im kostenlosen Nutzungstarif einem Limit von 3 Einträgen pro Monat. Diese Beschränkung wird lokal auf deinem Gerät geprüft.

### 3.5 Verhaltens-Profiling (lokale Verarbeitung)

Die App führt eine lokale Analyse deines Entscheidungsverhaltens durch, um dir personalisierte Einblicke zu bieten:

| Was analysiert wird | Zweck | Verarbeitung | Rechtsgrundlage |
|---------------------|-------|--------------|------------------|
| Nutzer-Archetyp (z.B. "Der Sichere Entscheider", "Der Vorsichtige Analytiker") | Personalisierte Rückmeldung | Ausschließlich lokal auf deinem Gerät | Art. 6 Abs. 1 lit. b DSGVO |
| Entscheidungsmuster, Stärken, Wachstumsbereiche | Selbstreflexion und Verbesserung | Ausschließlich lokal auf deinem Gerät | Art. 6 Abs. 1 lit. b DSGVO |
| Bias-Erkennung und Trend-Analyse | Personalisierte Empfehlungen | Ausschließlich lokal auf deinem Gerät | Art. 6 Abs. 1 lit. b DSGVO |

**Wichtig:** Dieses Profiling geschieht vollständig auf deinem Gerät. Es wird kein Machine Learning eingesetzt, sondern regelbasierte Algorithmen. Die Profiling-Ergebnisse werden niemals an Server übertragen.

### 3.6 Geräte-Fingerprinting (lokale Speicherung)

Zur Verbesserung der Account-Sicherheit erstellt die App einen Geräte-Fingerprint:

**Für den Fingerprint-Hash verwendete Attribute (7):**
- Gerätename (`deviceName`)
- Hersteller (`brand`)
- Marke (`manufacturer`)
- Modellname (`modelName`)
- Betriebssystem (`osName`)
- OS-Version (`osVersion`)
- OS-Build-ID (`osBuildId`)

**Zusätzlich erfasste Gerätedaten (nicht im Hash, nur in Sicherheits-Logs):**
- Platform API Level (`platformApiLevel`, nur Android)
- Geschätztes Geräte-Baujahr (`deviceYearClass`)

**Verarbeitung:**
1. Die 7 oben genannten Attribute werden zu einem SHA-256-Hash kombiniert
2. Der Hash wird lokal unter dem Schlüssel `decisio_device_id` gespeichert (AsyncStorage)
3. Bei Sicherheitsereignissen (z.B. Login, Account-Änderungen) werden alle 9 Gerätedaten (einschließlich Platform API Level und Geräte-Baujahr) zusammen mit dem Event protokolliert

**Rechtsgrundlage:** Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse an Betrugsprävention und Account-Sicherheit)

### 3.7 Sicherheits-Protokollierung (lokale Speicherung)

Die App protokolliert Sicherheitsereignisse lokal auf deinem Gerät:

**Protokollierte Events (bis zu 100):**
- `signup_attempt`, `login_attempt`, `login_success`, `login_failed`
- `logout`, `suspicious_activity_detected`, `email_verified`
- `account_unlocked`, `password_reset_requested`
- `account_deletion_requested`, `account_deleted`

**Gespeicherte Informationen pro Event:**
- Event-Typ
- E-Mail-Adresse (wird bei Account-Löschung zu `[deleted]` anonymisiert)
- Zeitstempel
- Vollständige Geräteinformationen (siehe 3.6)

**Zweck:** Nachvollziehbarkeit von Sicherheitsvorfällen und Schutz vor unbefugtem Zugriff  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse an IT-Sicherheit)

### 3.8 Analytics-Daten (optional, Cloud-Übertragung)

Die App verfügt über eine Analytics-Infrastruktur, die **derzeit de facto inaktiv** ist, da das benötigte Firebase Analytics Modul nicht in der App-Konfiguration aktiviert ist.

**Status:** Die Analytics-Einstellung in der App ist vorhanden, hat aber derzeit keine Funktion, da das Tracking-Modul fehlt.

**Falls die Analytics-Funktion in zukünftigen Versionen aktiviert wird**, würden bei aktivierter Analytics-Einstellung folgende Event-Daten an Google Firebase Analytics (USA) übertragen:

| Event | Übertragene Parameter | Zweck |
|-------|----------------------|-------|
| `decision_started` | Entscheidungsmodus, Kategorie, Gewichtungs-Preset | Verständnis der App-Nutzung |
| `decision_completed` | Modus, Kategorie, ob Empfehlung angenommen, Score, Preset | Erfolgsanalyse |
| `journal_entry_created` | Decision-ID (keine Inhalte), Wortanzahl, ob Fotos/Audio vorhanden | Journal-Nutzung |
| `journal_entry_deleted` | Journal-ID | Löschverhalten |
| `tab_changed` | Tab-Name, Tab-Index | Navigation |

**Rechtsgrundlage (falls aktiviert):** Art. 6 Abs. 1 lit. a DSGVO (Einwilligung via Analytics-Einstellung)

**Du kannst Analytics jederzeit in den App-Einstellungen deaktivieren.**

### 3.9 Technische Metadaten

Bei jeder Verbindung zu unseren Cloud-Diensten werden automatisch folgende technische Daten übertragen:

- **IP-Adresse:** Wird von Firebase für die Verbindungsherstellung verarbeitet, aber nicht von uns gespeichert oder ausgewertet
- **Zeitstempel der Anfragen**
- **App-Version**
- **Betriebssystem und Version**

**Rechtsgrundlage:** Art. 6 Abs. 1 lit. f DSGVO (technisch erforderlich für die Bereitstellung der Dienste)

---

## 4. Eingesetzte Drittanbieter-Dienste

**Wichtige Korrektur:** Entgegen früherer Versionen dieser Datenschutzerklärung nutzt Vayze mehrere Cloud-Dienste von Google LLC (USA) und Expo Inc. (USA). Alle diese Dienste agieren als **Auftragsverarbeiter** im Sinne von Art. 28 DSGVO.

### 4.1 Firebase Authentication

**Anbieter:** Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043, USA  
**Zweck:** Account-Registrierung, Login, Passwort-Reset, Account-Verwaltung  
**Übertragene Daten:** E-Mail-Adresse, Passwort (verschlüsselt), Anzeigename, Benutzer-ID, IP-Adresse (automatisch)  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. b DSGVO  
**Datenschutzerklärung:** https://firebase.google.com/support/privacy  
**Datenübertragung in Drittland:** USA, auf Basis der EU-Standardvertragsklauseln (Art. 46 Abs. 2 lit. c DSGVO)

### 4.2 Firebase Firestore

**Anbieter:** Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043, USA  
**Zweck:** Speicherung von Push-Tokens, Aktivitätszeitstempeln, Benachrichtigungs-Logs  
**Übertragene Daten:** Benutzer-ID, Expo Push Token, Plattform (iOS/Android), App-Version, Zeitstempel der letzten Entscheidung, Streak-Anzahl  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. a DSGVO (Push-Benachrichtigungen), Art. 6 Abs. 1 lit. b DSGVO (Account-Verwaltung)  
**Datenschutzerklärung:** https://firebase.google.com/support/privacy  
**Datenübertragung in Drittland:** USA, auf Basis der EU-Standardvertragsklauseln (Art. 46 Abs. 2 lit. c DSGVO)

### 4.3 Firebase Cloud Functions

**Anbieter:** Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043, USA  
**Zweck:** Serverlose Logik für Push-Benachrichtigungen (Streak-Warnungen, Re-Engagement, Broadcast, Meilensteine)  
**Verarbeitete Daten:** Benutzer-ID, Aktivitätsdaten, Entscheidungs-Zeitstempel, Streaks  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. a DSGVO  
**Datenschutzerklärung:** https://firebase.google.com/support/privacy  
**Datenübertragung in Drittland:** USA, auf Basis der EU-Standardvertragsklauseln (Art. 46 Abs. 2 lit. c DSGVO)

**Ausgeführte Cloud Functions:**
- `streakWarningDaily` (täglich 20:00 UTC): Iteriert alle Benutzer, prüft Streak-Status, sendet Warnungen
- `reEngagementDaily` (täglich 10:00 UTC): Findet inaktive Benutzer (7+ Tage ohne Entscheidung), sendet Re-Engagement-Push
- `sendBroadcast` (manuell ausgelöst): Ermöglicht Broadcast-Benachrichtigungen an alle Benutzer
- `onStreakMilestone` (automatisch bei neuen Entscheidungen): Sendet Glückwunsch-Benachrichtigungen bei Streak-Meilensteinen
- `syncStreak` (manuell durch App ausgelöst): Synchronisiert Streak-Daten (aktueller Streak, längster Streak, letzter Sync-Zeitstempel) zwischen App und Firestore

### 4.4 Expo Push Notification Service

**Anbieter:** Expo Inc., 650 Alabama St, San Francisco, CA 94110, USA  
**Zweck:** Technische Zustellung von Push-Benachrichtigungen an iOS- und Android-Geräte  
**Übertragene Daten:** Expo Push Token, Projekt-ID, Benachrichtigungsinhalt (Titel, Text)  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. a DSGVO  
**Datenschutzerklärung:** https://expo.dev/privacy  
**Datenübertragung in Drittland:** USA, auf Basis der EU-Standardvertragsklauseln (Art. 46 Abs. 2 lit. c DSGVO)

### 4.5 Firebase Analytics (optional, derzeit inaktiv)

**Anbieter:** Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043, USA  
**Zweck:** Nutzungsstatistiken (nur bei aktivierter Analytics-Einstellung)  
**Übertragene Daten:** Event-Namen, Event-Parameter (siehe 3.8), IP-Adresse (automatisch anonymisiert)  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. a DSGVO (Einwilligung via Analytics-Einstellung)  
**Datenschutzerklärung:** https://firebase.google.com/support/privacy  
**Datenübertragung in Drittland:** USA, auf Basis der EU-Standardvertragsklauseln (Art. 46 Abs. 2 lit. c DSGVO)  
**Status:** Derzeit nicht aktiv, da das Modul nicht in der App-Konfiguration enthalten ist

---

## 5. Datenübertragung in Drittländer

Alle eingesetzten Cloud-Dienste (Firebase, Expo) werden von Anbietern mit Sitz in den USA betrieben. Die Datenübertragung in die USA erfolgt auf Grundlage der **EU-Standardvertragsklauseln** gemäß Art. 46 Abs. 2 lit. c DSGVO.

Google LLC und Expo Inc. haben entsprechende Standardvertragsklauseln mit uns abgeschlossen und setzen zusätzliche technische und organisatorische Maßnahmen um, um ein angemessenes Datenschutzniveau zu gewährleisten.

**Hinweis:** Die USA verfügen derzeit nicht über ein von der EU-Kommission anerkanntes angemessenes Datenschutzniveau. Es besteht das Risiko, dass US-Behörden unter bestimmten Umständen auf deine Daten zugreifen können.

---

## 6. App-Berechtigungen

Die App benötigt folgende Geräte-Berechtigungen:

### 6.1 Pflichtberechtigungen (automatisch erteilt)

- **INTERNET:** Netzwerkzugriff für Account-Verwaltung und Push-Benachrichtigungen
- **RECEIVE_BOOT_COMPLETED:** Neuregistrierung von Benachrichtigungen nach Geräte-Neustart
- **VIBRATE:** Vibration bei eingehenden Benachrichtigungen
- **SCHEDULE_EXACT_ALARM:** Zeitgenaue Zustellung von geplanten Benachrichtigungen
- **MODIFY_AUDIO_SETTINGS:** Anpassung der Audio-Einstellungen für Sprachnotizen

### 6.2 Runtime-Berechtigungen (erfordern deine Zustimmung)

- **Kamera:** Aufnahme von Fotos für Journal-Einträge
- **Fotobibliothek (READ_EXTERNAL_STORAGE, iOS: Foto-Zugriff):** Auswahl vorhandener Fotos aus deiner Galerie
- **Mikrofon (RECORD_AUDIO):** Aufnahme von Sprachnotizen für Journal-Einträge
- **Speicher (WRITE_EXTERNAL_STORAGE, Android < 13):** Speicherung von Foto- und Audio-Dateien
- **Push-Benachrichtigungen:** Empfang von Erinnerungen und Streak-Warnungen

**Du kannst alle Runtime-Berechtigungen jederzeit in den Geräte-Einstellungen widerrufen.** Die App funktioniert auch ohne Kamera-, Foto- und Mikrofon-Zugriff; in diesem Fall stehen dir lediglich die Anhang-Funktionen im Journal nicht zur Verfügung.

### 6.3 Entwickler-Berechtigungen (nur in Debug-Builds)

- **SYSTEM_ALERT_WINDOW:** Anzeige von Entwickler-Tools über anderen Apps (nur für Testzwecke)

---

## 7. Speicherdauer

| Datentyp | Speicherdauer |
|----------|---------------|
| Account-Daten (Firebase Authentication) | Bis zur Account-Löschung |
| Push-Tokens (Firebase Firestore) | Bis zur Account-Löschung oder Token-Ablauf |
| Aktivitätsdaten für Benachrichtigungslogik | Bis zur Account-Löschung |
| Lokale Entscheidungsinhalte | Bis zur App-Deinstallation oder manuellen Löschung |
| Sicherheits-Protokoll (lokal) | Bis zu 100 Events, danach werden die ältesten überschrieben; bei Account-Löschung werden E-Mail-Adressen anonymisiert, aber Events bleiben erhalten |
| Analytics-Daten (falls aktiviert) | Bis zu 14 Monate (Google Firebase Analytics Standard) |
| Session-Daten (lokal) | Sessions laufen nach 365 Tagen automatisch ab. Ein separater Inaktivitäts-Timeout ist derzeit nicht implementiert. |

---

## 8. Datensicherheit

Wir setzen folgende Sicherheitsmaßnahmen ein:

### 8.1 Verschlüsselung

- **Passwörter:** Iteratives SHA-256-Hashing (10.000 Runden) mit zufälligem Salt vor der Übertragung
- **Datenübertragung:** TLS/SSL-Verschlüsselung für alle Verbindungen zu Firebase und Expo
- **Lokale Daten:** Verschlüsselte Speicherung sensibler Daten im Expo SecureStore (iOS: Keychain, Android: EncryptedSharedPreferences)
- **Session-Verschlüsselung:** Session-Token werden mit einem XOR-Cipher verschlüsselt gespeichert

**Hinweis zu HTTP-Verkehr:** Die App erlaubt aus technischen Gründen unverschlüsselten HTTP-Verkehr (`android:usesCleartextTraffic="true"`). Alle bewusst implementierten Datenübertragungen an Firebase und Expo nutzen HTTPS-Verschlüsselung. Es kann jedoch nicht vollständig ausgeschlossen werden, dass einzelne Bibliotheken unverschlüsselte Verbindungen aufbauen.

### 8.2 Zugriffskontrolle

- Zugriff auf Cloud-Daten nur über authentifizierte API-Anfragen
- Firebase Security Rules schränken Datenzugriff auf den jeweiligen Benutzer ein
- Geräte-Fingerprinting zur Erkennung verdächtiger Login-Versuche

### 8.3 Android-Backup

Die App erlaubt Android-System-Backups (`android:allowBackup="true"`). Das bedeutet, dass deine lokal gespeicherten App-Daten (Entscheidungen, Journal-Einträge, Fotos, Sprachnotizen) in Android-Cloud-Backups (Google Drive) enthalten sein können, sofern du diese Funktion auf deinem Gerät aktiviert hast.

**Wenn du dies nicht möchtest, kannst du Android-Backups für Vayze in den Android-Einstellungen unter "Google > Sicherung" deaktivieren.**

---

## 9. Deine Rechte gemäß DSGVO

Du hast folgende Rechte bezüglich deiner personenbezogenen Daten:

### 9.1 Auskunftsrecht (Art. 15 DSGVO)

Du kannst jederzeit Auskunft über die von uns verarbeiteten personenbezogenen Daten verlangen.

### 9.2 Recht auf Berichtigung (Art. 16 DSGVO)

Du kannst die Berichtigung unrichtiger Daten verlangen. Dies ist direkt in der App unter "Einstellungen > Profil" möglich.

### 9.3 Recht auf Löschung (Art. 17 DSGVO)

Du kannst die Löschung deiner personenbezogenen Daten verlangen. Dies ist direkt in der App unter "Einstellungen > Account löschen" möglich.

**Wichtiger Hinweis zur Account-Löschung:**
- Alle Account-Daten in Firebase (E-Mail, Anzeigename, Push-Tokens, Aktivitätsdaten) werden unwiderruflich gelöscht
- Alle lokalen Daten (Entscheidungen, Boards, Journal-Einträge) werden vom Gerät entfernt
- **Sicherheits-Protokoll:** Die lokal gespeicherten Sicherheitsereignisse werden NICHT vollständig gelöscht, sondern anonymisiert. Die E-Mail-Adresse in den Events wird durch `[deleted]` ersetzt, aber die Geräteinformationen und Zeitstempel bleiben aus Sicherheitsgründen erhalten (Betrugsprävention, Nachvollziehbarkeit von Sicherheitsvorfällen)

### 9.4 Recht auf Einschränkung der Verarbeitung (Art. 18 DSGVO)

Du kannst verlangen, dass die Verarbeitung deiner Daten eingeschränkt wird.

### 9.5 Recht auf Datenübertragbarkeit (Art. 20 DSGVO)

Du kannst verlangen, dass wir dir deine Daten in einem strukturierten, gängigen und maschinenlesbaren Format zur Verfügung stellen. Die Export-Funktion steht dir direkt in der App unter "Einstellungen > Daten exportieren" zur Verfügung.

### 9.6 Widerspruchsrecht (Art. 21 DSGVO)

Du kannst der Verarbeitung deiner Daten widersprechen, soweit diese auf Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse) beruht.

### 9.7 Widerruf der Einwilligung (Art. 7 Abs. 3 DSGVO)

Du kannst erteilte Einwilligungen (z.B. für Push-Benachrichtigungen oder Analytics) jederzeit in den App-Einstellungen widerrufen. Der Widerruf berührt nicht die Rechtmäßigkeit der bis dahin erfolgten Verarbeitung.

### 9.8 Beschwerderecht (Art. 77 DSGVO)

Du hast das Recht, dich bei einer Datenschutz-Aufsichtsbehörde zu beschweren:

**Bayerisches Landesamt für Datenschutzaufsicht (BayLDA)**  
Promenade 18  
91522 Ansbach  
Deutschland  
Telefon: +49 (0) 981 180093-0  
E-Mail: poststelle@lda.bayern.de  
Web: https://www.lda.bayern.de

---

## 10. Änderungen dieser Datenschutzerklärung

Wir behalten uns vor, diese Datenschutzerklärung bei Bedarf anzupassen, um sie an geänderte Rechtsverhältnisse oder bei Änderungen der App und deren Datenverarbeitung anzupassen.

Die jeweils aktuelle Version ist in der App unter "Einstellungen > Rechtliches > Datenschutzerklärung" und auf unserer Website abrufbar.

Bei wesentlichen Änderungen informieren wir dich über die App oder per E-Mail (sofern du uns deine E-Mail-Adresse mitgeteilt hast).

---

## 11. Kontakt

Bei Fragen zum Datenschutz kannst du uns jederzeit kontaktieren:

**Samuel Stöberl / Vayze Apps**  
Josef-Schwab-Straße 7  
94559 Niederwinkling  
Deutschland  
E-Mail: vayze.app@gmail.com

---

## Änderungshistorie

### Version 2.0.2 (17. Februar 2026) – Redaktionelle Korrekturen und Übersetzungsverbesserungen

**Korrekturen:**
1. **Alle Sprachversionen:** Datumskorrektur von „2026" auf „2025" in den Übersetzungen
2. **Englische Version:** Vollständige Neuformatierung von Plaintext auf Markdown mit korrekten Überschriften, Fettformatierung und Tabellen (Inhaltsverzeichnis und Formatierung nun funktional)
3. **Alle nicht-deutschen Versionen:** Sprachvorrang-Klausel ergänzt: „Bei Abweichungen zwischen den Sprachversionen gilt die deutsche Version."
4. **Alle nicht-deutschen Versionen:** Vollständiger englischer Name der BayLDA ergänzt: Bavarian State Office for Data Protection Supervision
5. **Indonesische Version:** Hinweis auf indonesisches Datenschutzgesetz (UU PDP, Nr. 27/2022) ergänzt
6. **§3.3 Tabelle (Englisch):** Kategorie-Trennzeilen wiederhergestellt (Entscheidungs-Zeitstempel, Aktivitäts-Tracking, Rate-Limiting, Benutzer-Identifikation)
7. **Änderungshistorie:** In der englischen Version ergänzt (fehlte bisher)

---

### Version 2.0.1 (7. Februar 2025) – Technische Präzisierung nach Code-Detailanalyse

**Korrekturen:**
1. **§3.6 Geräte-Fingerprinting:** Präzisierung, dass nur 7 Attribute in den SHA-256-Hash einfließen (nicht 9); Platform API Level und Geräte-Baujahr werden separat nur in Sicherheits-Logs gespeichert
2. **§3.2 Firestore-Pfade:** Korrektur von `users/{userId}` zu `users/{email}` – E-Mail-Adresse wird als Firestore-Dokument-ID verwendet
3. **§3.2 Benachrichtigungs-Protokoll:** Ergänzung der `notificationLog`-Subcollection mit gespeicherten Daten (Titel, Text, Payload, Zeitstempel, Status)
4. **§3.3 Aktivitätsdaten:** Vollständige Auflistung aller Firestore-Felder (Rate-Limiting, Aktivitäts-Tracking, Streak-Sync) und Offenlegung des Zugriffs auf `decisions`-Subcollection (Zeitstempel `createdAt` und `completedAt`)
5. **§3.4 Journal-Einträge:** Ergänzung des Felds `additionalNotes` (zusätzliche Notizen) und Hinweis auf Free-Tier-Limit (3 Einträge/Monat)
6. **§4.3 Cloud Functions:** Ergänzung der 5. Function `syncStreak` (manuelle Streak-Synchronisation)
7. **§7 Speicherdauer:** Entfernung des nicht implementierten Idle-Timeouts (999 Tage) – Sessions laufen nach 365 Tagen ab
8. **§8.1 Verschlüsselung:** Neutralere Formulierung zu Cleartext-Traffic – Einschränkung, dass unverschlüsselte Verbindungen durch Drittbibliotheken nicht vollständig ausgeschlossen werden können

**Hinweis zu Lücke 3 (enhancedAuthService):** Das Modul `enhancedAuthService` wurde analysiert und stellt lediglich eine Abstraktionsschicht über `firebaseAuthService` dar. Es führt keine zusätzlichen Datenverarbeitungen durch, die über die bereits dokumentierten Firebase Authentication-Funktionen hinausgehen.

### Version 2.0.0 (7. Februar 2025) – Vollständige Überarbeitung nach Legal-Technical-Audit

**Kritische Korrekturen:**
- **Drittanbieter-Dienste offengelegt:** Firebase Authentication, Firebase Firestore, Firebase Cloud Functions, Expo Push Notification Service, Firebase Analytics (optional, derzeit inaktiv) – vollständige Beschreibung aller eingesetzten Cloud-Dienste
- **Datenübertragung in die USA:** Offenlegung der Datenübertragung in Drittländer auf Basis der EU-Standardvertragsklauseln
- **Push-Benachrichtigungen:** Vollständige Beschreibung der implementierten Push-Funktionen (Streak-Warnungen, Re-Engagement, Broadcast, Meilensteine) und der dafür verarbeiteten Daten
- **Geräte-Fingerprinting:** Offenlegung der Erfassung und Verarbeitung von Gerätedaten für Sicherheitszwecke
- **Kamera/Mikrofon/Fotos:** Offenlegung der Berechtigungen und Verwendung für Journal-Anhänge (Fotos, Sprachnotizen)
- **Verhaltens-Profiling:** Beschreibung der lokalen Analyse (Archetypen, Musteranalyse, Empfehlungen)
- **Sicherheits-Protokollierung:** Offenlegung der lokalen Sicherheits-Logs mit bis zu 100 Events
- **Analytics:** Korrektur des Status (Infrastruktur vorhanden, derzeit de facto inaktiv) und Beschreibung der potenziell erfassten Daten
- **Verschlüsselung:** Korrekte Beschreibung der tatsächlich eingesetzten Verfahren (iteratives SHA-256, XOR-Cipher für Sessions)
- **Account-Löschung:** Offenlegung, dass Sicherheitsereignisse anonymisiert aber nicht vollständig gelöscht werden
- **Vollständige Berechtigungsliste:** Alle tatsächlich genutzten Android- und iOS-Berechtigungen aufgeführt

**Neue Abschnitte:**
- Detaillierte Tabellen zu allen Datentypen mit Zweck, Speicherort und Rechtsgrundlage
- Beschreibung der Cloud Functions und ihrer Cron-Jobs
- Technische Metadaten (IP-Adresse, automatische Übertragung)
- Android-Backup-Hinweis

**Entfernte Falschaussagen:**
- "Keine Drittanbieter-Dienste"
- "Keine Cloud-Speicherung"
- "Keine Geräte-ID"
- "Kein Fingerprinting"
- "Keine Fotos oder Mediendateien"
- "Keine Kamera oder Mikrofon"
- "Push-Benachrichtigungen derzeit nicht implementiert"
- "Keine Übermittlung in Drittländer"
- "Kein Profiling"
- "Analytics-Einstellung hat keine Funktion" (korrigiert zu: derzeit inaktiv, aber Infrastruktur vorhanden)

### Version 1.3.0 (vorherige Version)

- Initiale öffentliche Version (enthielt die oben genannten Ungenauigkeiten und Auslassungen)

---

**Stand:** 17. Februar 2026
**Version:** 2.0.2
