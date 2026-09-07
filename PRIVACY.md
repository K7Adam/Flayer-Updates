# Flayer Privacy Policy

**Last updated:** 2026-09-07

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
- Xtream / provider credentials (server URL, username, password). Credentials are encrypted using Android Keystore / EncryptedSharedPreferences.
- App settings (theme, language, UI preferences, watchlist, continue-watching progress, search history, hidden categories).
- TMDB artwork and metadata cache.
- User profiles and profile-specific data.

None of this data is sent to us.

## Data that leaves your device

Your device may send data to third parties only as part of using the app:

- **Your IPTV provider:** when you add an M3U URL or Xtream account, the app contacts your provider to download playlists, EPG and metadata. This includes the credentials and server address you entered.
- **The Movie Database (TMDB):** the app sends programme / movie / series titles to `api.themoviedb.org` and `image.tmdb.org` to fetch artwork, cast, descriptions and recommendations.
- **GitHub:** in the **self-hosted** build, the app contacts the public `K7Adam/Flayer-Updates` repository to check for signed update metadata and, if an update is available, to download the APK. The Play build does not contact GitHub.

The app never shares your provider credentials with TMDB or GitHub.

## HTTPS and unencrypted providers

The app permits `http://` provider URLs because some IPTV providers still require cleartext HTTP. When you enter an `http://` provider URL, the app shows an in-app warning that the connection is unencrypted and that your provider login and streams may be readable by others on the same network.

## Permissions

The app requests the following permissions and explains why at runtime where required:

- `INTERNET` and `ACCESS_NETWORK_STATE` — required to fetch playlists, EPG and artwork.
- `ACCESS_LOCAL_NETWORK` (Android 17+) — required for the TV web-setup server so a phone on the same network can add a playlist to the TV app.
- `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_DATA_SYNC` — required so WorkManager can import or refresh playlists and sync EPG in the background.
- `POST_NOTIFICATIONS` — required to show progress for background import / sync operations.
- `READ_EPG_DATA` / `WRITE_EPG_DATA` — required to add your in-progress and watchlisted content to the Android TV Home / Watch Next rows.

## Data retention and deletion

All data is kept locally on the device until you delete it or uninstall the app. Uninstalling Flayer removes the app data, the credential store and the local database.

You can also use the in-app "Delete all local data" feature at any time in **Settings > Delete all local data**. This permanently clears all playlists, channels, EPG, provider credentials, watch history, settings, and cached metadata without needing to uninstall the app.

## Children's privacy

Flayer is not directed at children under 13 years of age. We do not knowingly collect personal data from children.

## Changes to this policy

We may update this privacy policy from time to time. The latest version will always be available at https://github.com/K7Adam/Flayer-Updates/blob/main/PRIVACY.md.

## Contact

For privacy questions, contact the app owner at the address listed under "Controller".

---

## Datenschutzerklärung

**Letzte Aktualisierung:** 2026-09-07

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
- Xtream-/Anbieter-Zugangsdaten (Server-URL, Benutzername, Passwort). Zugangsdaten werden mit Android Keystore / EncryptedSharedPreferences verschlüsselt.
- App-Einstellungen (Design, Sprache, UI-Einstellungen, Watchlist, Weiterschauen-Fortschritt, Suchverlauf, ausgeblendete Kategorien).
- TMDB-Bilder- und Metadaten-Cache.
- Nutzerprofile und profilspezifische Daten.

Keine dieser Daten werden an uns gesendet.

## Daten, die dein Gerät verlassen

Dein Gerät kann Daten nur in folgenden Fällen an Dritte senden:

- **Dein IPTV-Anbieter:** Wenn du eine M3U-URL oder einen Xtream-Account hinzufügst, kontaktiert die App deinen Anbieter, um Playlists, EPG und Metadaten herunterzuladen. Dazu gehören die von dir eingegebenen Zugangsdaten und Serveradresse.
- **The Movie Database (TMDB):** Die App sendet Programm-/Film-/Serientitel an `api.themoviedb.org` und `image.tmdb.org`, um Bilder, Besetzung, Beschreibungen und Empfehlungen abzurufen.
- **GitHub:** In der **self-hosted** Version kontaktiert die App das öffentliche Repository `K7Adam/Flayer-Updates`, um signierte Update-Metadaten zu prüfen und gegebenenfalls das APK herunterzuladen. Die Play-Version kontaktiert kein GitHub.

Die App teilt deine Anbieter-Zugangsdaten niemals mit TMDB oder GitHub.

## HTTPS und unverschlüsselte Anbieter

Die App erlaubt `http://`-Anbieter-URLs, weil einige IPTV-Anbieter weiterhin unverschlüsseltes HTTP erfordern. Wenn du eine `http://`-Anbieter-URL eingibst, zeigt die App eine Warnung an, dass die Verbindung unverschlüsselt ist und dein Anbieter-Login sowie deine Streams im selben Netzwerk mitgelesen werden können.

## Berechtigungen

Die App fordert folgende Berechtigungen an und erklärt diese bei Bedarf zur Laufzeit:

- `INTERNET` und `ACCESS_NETWORK_STATE` — erforderlich, um Playlists, EPG und Bilder abzurufen.
- `ACCESS_LOCAL_NETWORK` (Android 17+) — erforderlich für den TV-Web-Einrichtungsserver, damit ein Telefon im selben Netzwerk eine Playlist zur TV-App hinzufügen kann.
- `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_DATA_SYNC` — erforderlich, damit WorkManager Playlists im Hintergrund importieren / aktualisieren und EPG synchronisieren kann.
- `POST_NOTIFICATIONS` — erforderlich, um Fortschrittsanzeigen für Hintergrund-Importe / -Synchronisationen anzuzeigen.
- `READ_EPG_DATA` / `WRITE_EPG_DATA` — erforderlich, um deine laufenden und watchlisteten Inhalte in die Android-TV-Startseite / Watch-Next-Zeile hinzuzufügen.

## Datenaufbewahrung und Löschung

Alle Daten werden lokal auf dem Gerät aufbewahrt, bis du sie löschst oder die App deinstallierst. Die Deinstallation von Flayer entfernt App-Daten, den Zugangsdatenspeicher und die lokale Datenbank.

Du kannst zudem jederzeit die In-App-Funktion "Alle lokalen Daten löschen" unter **Einstellungen > Alle lokalen Daten löschen** nutzen. Dies löscht alle Playlists, Sender, EPG, Anbieter-Zugangsdaten, den Watch-Verlauf, Einstellungen und zwischengespeicherte Metadaten vollständig und dauerhaft, ohne dass die App deinstalliert werden muss.

## Datenschutz für Kinder

Flayer richtet sich nicht an Kinder unter 13 Jahren. Wir sammeln wissentlich keine personenbezogenen Daten von Kindern.

## Änderungen dieser Datenschutzerklärung

Wir können diese Datenschutzerklärung von Zeit zu Zeit aktualisieren. Die aktuellste Version ist immer unter https://github.com/K7Adam/Flayer-Updates/blob/main/PRIVACY.md verfügbar.

## Kontakt

Bei Datenschutzfragen kontaktiere den App-Betreiber unter der im Abschnitt "Verantwortlicher" angegebenen Adresse.
