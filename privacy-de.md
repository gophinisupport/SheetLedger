# SheetLedger – Datenschutzerklärung

[ View in English 🇺🇸 ](privacy)
*(Diese Datenschutzerklärung ist zu Ihrer Bequemlichkeit auch auf Englisch verfügbar.)*

**Zuletzt aktualisiert: 18. November 2026**

Diese Datenschutzerklärung erläutert, wie SheetLedger („wir“, „uns“ oder „unser“) mit Ihren Informationen umgeht. SheetLedger wurde als datenschutzfreundliche, dezentrale und serverlose Utility-Anwendung entwickelt. Unsere Kernphilosophie ist einfach: **Ihre Finanzdaten gehören Ihnen, und wir haben absolut keinen Zugriff darauf.**

Durch die Nutzung von SheetLedger stimmen Sie den in dieser Richtlinie beschriebenen Bedingungen zu.

---

### 1. Keine Erfassung von Finanz- oder personenbezogenen Daten
SheetLedger ist eine Local-First-Anwendung. Im Gegensatz zu herkömmlichen Buchhaltungs-Apps besitzen, betreiben oder unterhalten wir **keine** zentralen Server.
- **Ihre Finanzdaten:** Alle Transaktionsprotokolle, Kontostände und Buchungseinträge werden lokal auf Ihrem Gerät in einer SQLite-Datenbank gespeichert.
- **Keine Abfangung durch Server:** Wir sammeln, lesen, übertragen oder monetarisieren Ihre persönlichen Finanzinformationen nicht. Ihre Buchhaltungsdaten berühren zu keinem Zeitpunkt eine von uns kontrollierte Infrastruktur von Drittanbietern und werden niemals an Werbenetzwerke weitergegeben.

### 2. Integration von Google Drive und Google Sheets
Um eine Cloud-Synchronisierung und Datensicherung zu ermöglichen, können Sie Ihr persönliches Google-Konto mit SheetLedger verknüpfen.
- **Datenzugriff (Scopes):** Die App fordert einen eingeschränkten Zugriff auf Ihr Google Drive und Google Sheets an, der ausschließlich dazu dient, die von SheetLedger generierten verschlüsselten Tabellen zu erstellen, zu synchronisieren und zu verwalten.
- **Client-seitige Ende-zu-Ende-Verschlüsselung:** Alle Buchungseinträge werden lokal auf Ihrem Gerät verschlüsselt, bevor sie mit Google Sheets synchronisiert werden. Ihre Google Sheets speichern ausschließlich verschlüsselten Geheimtext, sodass Ihre Finanzdaten auch in Ihrem Cloud-Speicher ohne Ihren lokalen Entschlüsselungsschlüssel unlesbar bleiben.
- **Direkte Kommunikation:** Die gesamte Datenübertragung erfolgt direkt zwischen Ihrem Gerät und den offiziellen APIs von Google. Wir agieren nicht als Zwischenhändler und haben keine Möglichkeit, Ihre Google-Zugangsdaten, Verschlüsselungsschlüssel oder synchronisierten Dateien einzusehen.
- **Dateneigentum:** Sie behalten das vollständige Eigentum an den in Ihrem Google Drive gespeicherten Tabellendateien. Sie können diese Dateien jederzeit direkt über Ihr Google Drive sichern, exportieren oder löschen.

### 3. In-App-Käufe und Abrechnung (RevenueCat)
Wir verwenden RevenueCat zur Verwaltung von Premium-Abonnements und In-App-Käufen.
- Wenn Sie ein Abonnement oder Upgrade über Google Play erwerben, werden anonymisierte Transaktionsdaten (wie Produkt-IDs, Kaufzeitpunkt und Abonnementstatus) sicher verarbeitet, um Ihre Premium-Funktionen freizuschalten und Werbung zu entfernen.
- Es werden niemals persönliche Identitätsdaten oder spezifische finanzielle Zahlungsmethoden (wie Kreditkartennummern) an uns weitergegeben oder von uns gespeichert.

### 4. Werbung in der kostenlosen Version (Google AdMob)
Um die kontinuierliche Weiterentwicklung und Wartung von SheetLedger zu finanzieren, zeigt die kostenlose Version der App Werbung an, die von **Google AdMob** bereitgestellt wird.
- **Von Google erhobene Daten:** Google und seine Werbepartner können bestimmte Geräte- und Nutzungsdaten erfassen und verarbeiten – wie etwa die Werbe-ID Ihres Geräts (AAID), die IP-Adresse, allgemeine Geräteinformationen sowie Metriken zur Werbeinteraktion –, um Anzeigen bereitzustellen und deren Leistung zu messen.
- **Vollständige Trennung von Ihren Finanzen:** AdMob arbeitet völlig unabhängig von Ihrer lokalen Datenbank und Ihren Google Sheets. Ihre Finanzeinträge, Kategorien und Kontostände werden von Google AdMob **niemals** abgerufen oder mit diesem geteilt.
- **Werbeeinstellungen & werbefreie Option:** Sie können personalisierte Werbung jederzeit in den Einstellungen Ihres Android-Geräts deaktivieren (**Einstellungen > Google > Werbung**). Darüber hinaus deaktiviert ein Upgrade auf die Premium-Version von SheetLedger jegliche Werbung vollständig und unterbindet alle werbebezogenen Netzwerkanfragen.

### 5. Geräteberechtigungen
Die App fordert die folgenden Berechtigungen nur an, um die Kernfunktionalität zu gewährleisten:
- **Internetzugriff:** Erforderlich, um Ihre verschlüsselte lokale Datenbank mit Ihren persönlichen Google Sheets zu synchronisieren, den Zahlungsstatus über Google Play zu überprüfen und Werbung in der kostenlosen Version der App zu laden.

### 6. Dienste von Drittanbietern
Obwohl SheetLedger selbst keine personenbezogenen Daten erhebt oder speichert, nutzt die App vertrauenswürdige Dienste von Drittanbietern, die gemäß deren jeweiligen Datenschutzrichtlinien Informationen erfassen können:
- [Google Play Services Datenschutzerklärung](https://policies.google.com/privacy)
- [Google AdMob & Datenschutz bei Werbung](https://policies.google.com/technologies/ads)
- [RevenueCat Datenschutzerklärung](https://www.revenuecat.com/privacy)

### 7. Einhaltung der DSGVO (Europäische Nutzer)
Da SheetLedger keine personenbezogenen Daten auf Servern speichert, verarbeitet oder kontrolliert, halten wir uns strikt an die Grundsätze der Datenminimierung und des „Privacy-by-Design“ gemäß der Datenschutz-Grundverordnung (DSGVO).
- **Ihre Finanzdaten:** Verbleiben verschlüsselt und ausschließlich auf Ihrem Gerät oder in Ihrem persönlichen Google Drive, wodurch Sie die volle Kontrolle über Datenlöschung und Datenübertragbarkeit behalten.
- **Einwilligung zur Werbung:** Für Nutzer im Europäischen Wirtschaftsraum (EWR) und im Vereinigten Königreich fragt die User Messaging Platform (UMP) von Google beim ersten Start Ihre Einwilligung bezüglich personalisierter oder nicht-personalisierter Werbung ab. Sie können Ihre Einwilligungseinstellungen jederzeit widerrufen oder ändern.

### 8. Änderungen dieser Datenschutzerklärung
Wir können unsere Datenschutzerklärung von Zeit zu Zeit aktualisieren, um technische, funktionale oder regulatorische Änderungen widerzuspiegeln. Alle Aktualisierungen werden auf dieser Seite mit einem aktualisierten Datum („Zuletzt aktualisiert“) veröffentlicht.

### 9. Kontakt
Wenn Sie Fragen oder Feedback zu dieser datenschutzorientierten Richtlinie haben, kontaktieren Sie uns bitte per E-Mail unter: gophini.support@gmail.com
