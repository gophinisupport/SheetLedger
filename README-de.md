# SheetLedger

[ 🇺🇸 View in English ](./) | [ Datenschutz 🛡️ ](privacy-de) | [ Nutzungsbedingungen 📄 ](service-de) | [ Hilfe ❓ ](help-de)

---

## Zweck der Anwendung (Application Purpose Statement)

**SheetLedger** ist eine Local-First-Anwendung für persönliche Finanzen, Ausgabenverfolgung und Budgetverwaltung. Der Hauptzweck von **SheetLedger** besteht darin, Nutzern das Erfassen, Organisieren und Analysieren ihrer täglichen Finanztransaktionen, Kontostände und Budgets in einer sicheren und datenschutzorientierten Umgebung zu ermöglichen.

Um nahtlose Cloud-Backups, Datensynchronisierung und die Zusammenarbeit mehrerer Nutzer ohne zentrale Drittanbieter-Server zu ermöglichen, integriert **SheetLedger** direkt Google-Dienste. Dadurch behalten Nutzer die vollständige Datenhoheit über ihre Finanzdaten innerhalb ihres eigenen Google-Kontos.

---

## Google OAuth-Berechtigungen & Datenschutzhinweise

**SheetLedger** fordert spezifische Google OAuth-Berechtigungen ausschließlich zur Bereitstellung der Kernfunktionen an. Die Berechtigungen werden wie folgt verwendet:

* **`email` (Nutzeridentifikation & Änderungshistorie):** Wird ausschließlich verwendet, um den Ersteller oder Bearbeiter von Transaktionseinträgen in gemeinsamen Haushaltsbüchern zu identifizieren. Dies stellt sicher, dass in kollaborativen Tabellen Einträge korrekt den jeweiligen Personen zugeordnet werden können.
* **`https://www.googleapis.com/auth/drive.file` (Zugriff auf eigene Tabellen):** Wird verwendet, um Google Spreadsheet-Datenbankdateien zu erstellen, zu lesen, zu aktualisieren und zu verwalten, die explizit von **SheetLedger** im persönlichen Google Drive des Nutzers erstellt oder damit geöffnet wurden.
* **`https://www.googleapis.com/auth/spreadsheets` (Zugriff auf freigegebene Tabellen):** Wird nur bei Bedarf (On-Demand) angefordert, wenn der Nutzer von Dritten freigegebene Tabellen verknüpfen und gemeinsam bearbeiten möchte. Dies ermöglicht **SheetLedger** das Lesen und Synchronisieren von Einträgen in freigegebenen Tabellen, bei denen die `drive.file`-Sandbox-Grenzen greifen.

### Absolute Datenschutzgarantie
* **Kein Drittanbieter-Backend:** **SheetLedger** arbeitet vollständig serverlos. Alle Google-Nutzerdaten und Finanzeinträge werden lokal auf Ihrem Gerät verarbeitet und direkt an die offiziellen APIs von Google übertragen. Wir speichern, sammeln, verkaufen oder übertragen Ihre Daten nicht an externe Server.
* **Einhaltung der Richtlinien für begrenzte Nutzung (Limited Use Compliance):** Die Nutzung und Übertragung von Informationen, die von Google-APIs empfangen wurden, an andere Apps durch **SheetLedger** entspricht den [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), einschließlich der Anforderungen für die begrenzte Nutzung.

---

## Hauptmerkmale & Architektur

* **Absolute Datenhoheit:** Serverlose Finanzanwendung für Nutzer, die die vollständige Kontrolle über ihre Daten verlangen.
* **Local-First-Performance:** Lokale Transaktionen, Kontoeinstellungen und Kategorien werden sofort in der sicheren Anwendungs-Sandbox des Geräts gespeichert.
* **Zusammenarbeit mehrerer Nutzer:** Native Unterstützung für freigegebene Haushaltsbücher mit automatischer Zuordnung der Bearbeiter über deren E-Mail-Kennung.
* **Automatisierter Datenschutz:** Verschlüsselungsmetadaten, Datenbankstrukturen und Systemkonfigurationen werden automatisch in den App Properties der Tabelle verwaltet, ohne dass komplexe Passwörter vom Nutzer gemerkt werden müssen.

---

## Download & Verfügbarkeit

Erhältlich im [Google Play Store](https://play.google.com/store/apps/details?id=com.king011.apps.sheetledger).

---

© 2026 gophini (`The Powerpuff Penguin`). Mit Sorgfalt entwickelt.  
Support & Kontakt: [gophini.support@gmail.com](mailto:gophini.support@gmail.com)
