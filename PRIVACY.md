# Flayer Privacy Policy

**Last updated:** 2026-10-07

This privacy policy applies to the Flayer Android app.

## Controller

Adam Karepin  
GitHub: [https://github.com/K7Adam](https://github.com/K7Adam)  
Contact: [77991070+K7Adam@users.noreply.github.com](mailto:77991070+K7Adam@users.noreply.github.com)  
Project Repository: [https://github.com/K7Adam/Flayer-Updates/issues](https://github.com/K7Adam/Flayer-Updates/issues)

## What Flayer is

Flayer is a local IPTV player. The app does not provide channels, movies or series. It plays playlists and subscriptions that the user adds manually.

## Data we collect

We do **not** collect any personal data. Flayer does not send data to the app developer. There are no analytics, no ads and no tracking.

## Data stored locally on your device

The following data is stored locally in the app:

- Playlist metadata (name, URL, upload type, settings).
- Channel and EPG / programme data downloaded from your provider.
- Programme reminders you set (channel, programme title and time).
- Xtream / provider credentials (server URL, username, password). Credentials are encrypted with AES-256-GCM using a key held in the Android Keystore.
- App settings (theme, language, UI preferences, watchlist, continue-watching progress, search history, hidden categories).
- TMDB artwork and metadata cache. TMDB database records expire after 150 days. After startup, the app also clears the shared memory/disk image cache when its persisted last-clear timestamp is unknown or older than 150 days. "Delete TMDB data" in Settings clears TMDB records and the shared image cache, including provider images. Images and metadata may be fetched again on demand.
- User profiles and profile-specific data.
- On phones and tablets, the titles you are currently watching also appear in the app's launcher shortcuts and in the "Continue watching" home-screen widget if you add it.
- Diagnostics (Settings > Diagnostics): the reasons Android reports for recent app exits (for example a crash, a hang or a stop by the system for memory or CPU use, with the code locations of a hang), a crash summary limited to error types and code locations (no error messages), statistics of your last 20 playbacks (playback type, start time, buffering, dropped frames, video resolution, bitrate and codec, error code; no titles, channel names or addresses), basic device facts (model, Android version, memory, supported video decoders) and, on Android 16 and later, performance traces the system records when the app hangs or is stopped for excessive memory or CPU use. "Clear" there deletes everything the app stored; the exit history itself is kept by Android, and after "Clear" Flayer no longer shows the older entries.

None of this data is sent to us.

## Data that leaves your device

Your device may send data to third parties only as part of using the app:

- **Your IPTV provider:** when you add an M3U URL or Xtream account, the app contacts your provider to download playlists, EPG and metadata. This includes the credentials and server address you entered.
- **The Movie Database (TMDB):** the app sends programme / movie / series titles or TMDB IDs to `api.themoviedb.org` and requests images from `image.tmdb.org` to fetch artwork, cast, descriptions and recommendations. TMDB/Xperi in the USA receives the device's public IP address as part of these network connections.
- **Optional background TMDB enrichment:** "Add metadata from TMDB" is off by default and separately enabled on phone or TV. Its purpose is to fill missing catalogue genre/year information and store metadata locally. After import/sync, or when enabled, it sends distinct movie/series TMDB IDs already supplied by the provider; for entries without an ID it may send a cleaned title and a known release year. The recipients are TMDB/Xperi in the USA, who also receive your public IP address. No playlist URLs, provider credentials, categories or profile data are sent. Downloads run only over an unmetered connection (usually Wi-Fi) and when the battery is not low. Turning this off cancels background work and prevents new enrichment requests; an already sent request cannot be recalled. Existing cached content expires within 150 days. "Delete TMDB data" turns enrichment off and removes its metadata, keywords, progress/checkpoints and all title mappings, including manual choices. On-demand detail/artwork requests remain available when you use those features. TMDB-derived information is never sent to AI/LLM features or Android assistants by Flayer.
- **GitHub:** in the **self-hosted** build, the app contacts the public `K7Adam/Flayer-Updates` repository to check for signed update metadata and, if an update is available, to download the APK. The Play build does not contact GitHub.
- **Google Cast (optional, phones and tablets only):** only after you turn on "Chromecast (beta)" in Settings. Google Play services then discover Cast devices on your network. When you cast, the stream address of the selected item (for Xtream providers this address contains your login), its title and artwork are sent to the Cast device you chose, which loads the stream directly from your provider. Other Cast-enabled apps on the same network can see what is playing. While Casting is on, Google's Cast library may send technical usage and diagnostic data to Google under Google's privacy policy. Casting is off by default.

- **Experimental assistant access:** When enabled on a supported device, authorized Android assistants can request catalogue searches and playback actions using your active Flayer profile and playlist. Flayer shares only relevant titles, content types, local identifiers and action results. It does not share provider credentials, stream addresses, HTTP headers or your complete viewing history. The assistant may process your request and returned information using its own online services and privacy policy. Disabling access prevents new requests and invalidates pending Flayer assistant actions.

- **A diagnostics report you choose to share:** only when you tap "Share report" in Settings > Diagnostics and pick an app (for example email) the report text goes to that app and to whoever you send it. Addresses, IP addresses, host names and login data are removed from it before it is shown or shared. System performance traces are never included.

The app never shares your provider credentials with TMDB or GitHub.

## HTTPS and unencrypted providers

The app permits `http://` provider URLs because some IPTV providers still require cleartext HTTP. When you enter an `http://` provider URL, the app shows an in-app warning that the connection is unencrypted and that your provider login and streams may be readable by others on the same network.

## Permissions

The app requests the following permissions and explains why at runtime where required:

- `INTERNET` and `ACCESS_NETWORK_STATE` — required to fetch playlists, EPG and artwork.
- `ACCESS_LOCAL_NETWORK` (Android 17+) — required for the TV web-setup server so a phone on the same network can add a playlist to the TV app.
- `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_DATA_SYNC` — required so WorkManager can import or refresh playlists and sync EPG in the background.
- `POST_NOTIFICATIONS` — required to show progress for background import / sync operations and the programme reminders you set.
- `FOREGROUND_SERVICE_MEDIA_PLAYBACK` — shows media controls in the notification and on the lock screen while a Cast session is running.
- `READ_EPG_DATA` / `WRITE_EPG_DATA` — required to add your in-progress and watchlisted content to the Android TV Home / Watch Next rows.

## Data retention and deletion

Local settings and user data remain until you delete them or uninstall the app. TMDB content, automatic mappings and enrichment checkpoints/progress expire within 150 days; manual mappings store your own ID choice until reset/deletion and never extend cached content retention. Uninstalling Flayer removes the app data, the credential store and the local database.

You can also use the in-app "Delete all local data" feature at any time in **Settings > Delete all local data**. This permanently clears all playlists, channels, EPG, provider credentials, watch history, settings, and cached metadata without needing to uninstall the app.

## Children's privacy

Flayer is not directed at children under 13 years of age. We do not knowingly collect personal data from children.

## Changes to this policy

We may update this privacy policy from time to time. The latest version will always be available at https://github.com/K7Adam/Flayer-Updates/blob/main/PRIVACY.md.

## Contact

For privacy questions, contact the app owner at the address listed under "Controller".

---

## Datenschutzerklärung

**Letzte Aktualisierung:** 2026-10-07

Diese Datenschutzerklärung gilt für die Android-App Flayer.

## Verantwortlicher

Adam Karepin  
GitHub: [https://github.com/K7Adam](https://github.com/K7Adam)  
Kontakt: [77991070+K7Adam@users.noreply.github.com](mailto:77991070+K7Adam@users.noreply.github.com)  
Projekt-Repository: [https://github.com/K7Adam/Flayer-Updates/issues](https://github.com/K7Adam/Flayer-Updates/issues)

## Was Flayer ist

Flayer ist ein lokaler IPTV-Player. Die App stellt keine Sender, Filme oder Serien bereit. Sie spielt Playlists und Abos ab, die der Nutzer manuell hinzufügt.

## Daten, die wir erheben

Wir erheben **keine** personenbezogenen Daten. Flayer sendet keine Daten an den App-Entwickler. Es gibt keine Analyse-Tools, keine Werbung und kein Tracking.

## Lokal auf deinem Gerät gespeicherte Daten

Folgende Daten werden lokal in der App gespeichert:

- Playlist-Metadaten (Name, URL, Upload-Typ, Einstellungen).
- Sender- und EPG-/Programmdaten, die vom Anbieter heruntergeladen wurden.
- Von dir gesetzte Sendungserinnerungen (Sender, Sendungstitel und Uhrzeit).
- Xtream-/Anbieter-Zugangsdaten (Server-URL, Benutzername, Passwort). Zugangsdaten werden mit AES-256-GCM und einem im Android Keystore gehaltenen Schlüssel verschlüsselt.
- App-Einstellungen (Design, Sprache, UI-Einstellungen, Watchlist, Weiterschauen-Fortschritt, Suchverlauf, ausgeblendete Kategorien).
- TMDB-Bilder- und Metadaten-Cache. TMDB-Datenbankeinträge verfallen nach 150 Tagen. Nach dem Start leert die App auch den gemeinsamen Bilder-Cache im Arbeitsspeicher und auf dem Datenträger, wenn der gespeicherte Zeitpunkt der letzten Leerung unbekannt oder älter als 150 Tage ist. „TMDB-Daten löschen“ entfernt TMDB-Einträge und den gemeinsamen Bilder-Cache einschließlich Anbieterbildern. Bilder und Metadaten werden bei Bedarf erneut geladen.
- Nutzerprofile und profilspezifische Daten.

Keine dieser Daten werden an uns gesendet.

## Daten, die dein Gerät verlassen

Dein Gerät kann Daten nur in folgenden Fällen an Dritte senden:

- **Dein IPTV-Anbieter:** Wenn du eine M3U-URL oder einen Xtream-Account hinzufügst, kontaktiert die App deinen Anbieter, um Playlists, EPG und Metadaten herunterzuladen. Dazu gehören die von dir eingegebenen Zugangsdaten und Serveradresse.
- **The Movie Database (TMDB):** Die App sendet Programm-/Film-/Serientitel oder TMDB-IDs an `api.themoviedb.org` und ruft Bilder von `image.tmdb.org` ab, um Bilder, Besetzung, Beschreibungen und Empfehlungen zu laden. TMDB/Xperi in den USA erhält bei diesen Verbindungen auch die öffentliche IP-Adresse deines Geräts.
- **Optionale TMDB-Anreicherung im Hintergrund:** „Metadaten von TMDB ergänzen“ ist standardmäßig ausgeschaltet und wird auf Smartphone oder TV gesondert aktiviert. Sie ergänzt fehlende Genre-/Jahresangaben und speichert Metadaten lokal. Nach Import/Synchronisierung oder beim Einschalten sendet sie unterschiedliche, bereits vom Anbieter gelieferte Film-/Serien-TMDB-IDs; für Einträge ohne ID gegebenenfalls einen bereinigten Titel mit bekanntem Erscheinungsjahr. Empfänger ist TMDB/Xperi in den USA, das dabei auch deine öffentliche IP-Adresse erhält. Playlist-URLs, Anbieter-Zugangsdaten, Kategorien und Profildaten werden nicht gesendet. Downloads laufen nur über eine nicht getaktete Verbindung (meist WLAN) und bei ausreichendem Akkustand. Abschalten beendet die Hintergrundarbeit und verhindert neue Anreicherungsanfragen; bereits versendete Anfragen lassen sich nicht zurückholen. Gespeicherte Inhalte verfallen innerhalb von 150 Tagen. „TMDB-Daten löschen“ schaltet die Anreicherung aus und entfernt Metadaten, Schlagwörter, Fortschritt/Prüfstände sowie alle Zuordnungen einschließlich manueller Auswahl. Abrufe für geöffnete Detailseiten und Bilder bleiben verfügbar. Flayer gibt TMDB-Daten niemals an KI-/LLM-Funktionen oder Android-Assistenten weiter.
- **GitHub:** In der **self-hosted** Version kontaktiert die App das öffentliche Repository `K7Adam/Flayer-Updates`, um signierte Update-Metadaten zu prüfen und gegebenenfalls das APK herunterzuladen. Die Play-Version kontaktiert kein GitHub.
- **Google Cast (optional, nur Smartphones und Tablets):** Nur wenn du in den Einstellungen „Chromecast (Beta)“ einschaltest. Die Google Play-Dienste suchen dann Cast-Geräte in deinem Netzwerk. Beim Übertragen werden die Stream-Adresse des gewählten Inhalts (bei Xtream-Anbietern enthält diese Adresse deine Zugangsdaten), sein Titel und sein Bild an das ausgewählte Cast-Gerät gesendet, das den Stream direkt bei deinem Anbieter abruft. Andere Cast-fähige Apps im selben Netzwerk können sehen, was gerade läuft. Solange die Übertragung eingeschaltet ist, kann die Cast-Bibliothek von Google technische Nutzungs- und Diagnosedaten nach der Datenschutzerklärung von Google an Google senden. Die Übertragung ist standardmäßig ausgeschaltet.

- **Experimenteller Assistentenzugriff:** Wenn du ihn auf einem unterstützten Gerät einschaltest, können autorisierte Android-Assistenten Katalogsuchen und Wiedergabeaktionen für dein aktives Flayer-Profil und deine Playlist anfordern. Flayer teilt nur relevante Titel, Inhaltstypen, lokale Kennungen und Aktionsergebnisse. Anbieter-Zugangsdaten, Stream-Adressen, HTTP-Header und dein vollständiger Wiedergabeverlauf werden nicht geteilt. Der Assistent kann deine Anfrage und die erhaltenen Informationen mit seinen eigenen Onlinediensten und nach seiner eigenen Datenschutzerklärung verarbeiten. Abschalten verhindert neue Anfragen und macht ausstehende Flayer-Assistentenaktionen ungültig.

Die App teilt deine Anbieter-Zugangsdaten niemals mit TMDB oder GitHub.

## HTTPS und unverschlüsselte Anbieter

Die App erlaubt `http://`-Anbieter-URLs, weil einige IPTV-Anbieter weiterhin unverschlüsseltes HTTP erfordern. Wenn du eine `http://`-Anbieter-URL eingibst, zeigt die App eine Warnung an, dass die Verbindung unverschlüsselt ist und dein Anbieter-Login sowie deine Streams im selben Netzwerk mitgelesen werden können.

## Berechtigungen

Die App fordert folgende Berechtigungen an und erklärt diese bei Bedarf zur Laufzeit:

- `INTERNET` und `ACCESS_NETWORK_STATE` — erforderlich, um Playlists, EPG und Bilder abzurufen.
- `ACCESS_LOCAL_NETWORK` (Android 17+) — erforderlich für den TV-Web-Einrichtungsserver, damit ein Telefon im selben Netzwerk eine Playlist zur TV-App hinzufügen kann.
- `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_DATA_SYNC` — erforderlich, damit WorkManager Playlists im Hintergrund importieren / aktualisieren und EPG synchronisieren kann.
- `POST_NOTIFICATIONS` — erforderlich, um Fortschrittsanzeigen für Hintergrund-Importe / -Synchronisationen und die von dir gesetzten Sendungserinnerungen anzuzeigen.
- `FOREGROUND_SERVICE_MEDIA_PLAYBACK` — zeigt während einer Cast-Übertragung Wiedergabe-Steuerelemente in der Benachrichtigung und auf dem Sperrbildschirm.
- `READ_EPG_DATA` / `WRITE_EPG_DATA` — erforderlich, um deine laufenden und watchlisteten Inhalte in die Android-TV-Startseite / Watch-Next-Zeile hinzuzufügen.

## Datenaufbewahrung und Löschung

Lokale Einstellungen und Nutzerdaten bleiben, bis du sie löschst oder die App deinstallierst. TMDB-Inhalte, automatische Zuordnungen und Prüfstände/Fortschritt der Anreicherung verfallen innerhalb von 150 Tagen; manuelle Zuordnungen speichern deine eigene ID-Auswahl bis zum Zurücksetzen/Löschen und verlängern niemals die Aufbewahrung zwischengespeicherter Inhalte. Die Deinstallation von Flayer entfernt App-Daten, den Zugangsdatenspeicher und die lokale Datenbank.

Du kannst zudem jederzeit die In-App-Funktion "Alle lokalen Daten löschen" unter **Einstellungen > Alle lokalen Daten löschen** nutzen. Dies löscht alle Playlists, Sender, EPG, Anbieter-Zugangsdaten, den Watch-Verlauf, Einstellungen und zwischengespeicherte Metadaten vollständig und dauerhaft, ohne dass die App deinstalliert werden muss.

## Datenschutz für Kinder

Flayer richtet sich nicht an Kinder unter 13 Jahren. Wir sammeln wissentlich keine personenbezogenen Daten von Kindern.

## Änderungen dieser Datenschutzerklärung

Wir können diese Datenschutzerklärung von Zeit zu Zeit aktualisieren. Die aktuellste Version ist immer unter https://github.com/K7Adam/Flayer-Updates/blob/main/PRIVACY.md verfügbar.

## Kontakt

Bei Datenschutzfragen kontaktiere den App-Betreiber unter der im Abschnitt "Verantwortlicher" angegebenen Adresse.
