# SheetLedger – Benutzerhandbuch & Hilfe

[ View in English 🇺🇸 ](help)

---

### ⚡ 1. App-Start & Verbindungsstabilität
* **Synchronisierung beim Start:** SheetLedger synchronisiert beim Starten der Anwendung Ihren lokalen Zustand mit Ihrem Cloud-Hauptbuch.
* **Google API-Quota-Limits:** Die Google Sheets-APIs unterliegen weltweit strengen Nutzungslimits pro Minute. Wenn Ihr lokales Hauptbuch ein hohes Volumen an Batch-Operationen aufweist, können Synchronisierungsanfragen in eine Warteschlange gestellt und leicht verzögert werden.
* **Verbindungsfehler:** Wenn eine Synchronisierung oder Google Drive-Autorisierung aufgrund vorübergehender Netzwerküberlastung oder API-Rate-Limiting fehlschlägt, **keine Panik**. Ihre lokalen Daten sind absolut sicher. Warten Sie einfach einen Moment und versuchen Sie es erneut.

### 💎 2. Abonnementstufen & Google Sheets-Kontingente
Um zu verhindern, dass ein einzelner Nutzer das gesamte API-Verkehrskontingent erschöpft, und um die Stabilität des Dienstes für alle zu gewährleisten, **ist die maximale Anzahl gleichzeitig verknüpfter Google Sheets basierend auf Ihrer Abonnementstufe (Kostenlos vs. Premium) beschränkt**. Bitte überprüfen Sie das In-App-**Abonnement-Menü**, um Ihre aktuellen Limits einzusehen.

### ✈️ 3. Echte Offline-Funktionalität (Local-First)
* **Keine Netzwerkabhängigkeit:** SheetLedger ist als reine Local-First-Anwendung konzipiert. Sie können Ihre Finanzdaten überall einsehen, hinzufügen oder bearbeiten – selbst im Flugzeug oder ohne jegliche Verbindung.
* **Automatische Wiederaufnahme:** Sobald Ihr Gerät wieder eine Netzwerkverbindung herstellt, nimmt unsere interne State Machine den Betrieb im Hintergrund automatisch wieder auf und lädt Ihre zwischengespeicherten Änderungen sicher in die Cloud hoch.

### ⚠️ 4. Wichtig: Bearbeiten Sie das Google Sheets-Dokument nicht manuell
* **Kryptografische & strukturelle Integrität:** Das verknüpfte Google Sheets-Dokument fungiert als verschlüsselter Speicher-Backend. SheetLedger erzwingt strenge kryptografische Validierungen und relationale Schema-Prüfungen.
* **Risiko von Datenkorruption:** **Fügen Sie niemals manuell Zeilen, Zellen oder Spalten direkt in der Web- oder Mobiloberfläche von Google Sheets hinzu, löschen oder ändern Sie diese nicht.** Manuelle Eingriffe verletzen den Hash zur Überprüfung der Datenkonsistenz. Dies führt dazu, dass die App das Hauptbuch als beschädigt eingestuft, um Ihre Finanzsicherheit zu schützen. Alle Operationen müssen über die SheetLedger-App ausgeführt werden.

### 👥 5. Synchronisierung zwischen mehreren Geräten
Sie können sich mit Ihrem persönlichen Google-Konto auf mehreren Geräten (z. B. Ihrem Android-Smartphone und -Tablet) gleichzeitig sicher anmelden. Die Local-First-Architektur sorgt dafür, dass alle Geräte über die Cloud sicher auf dem selben Hauptbuchstand zusammengeführt werden.

### 🤝 6. Sichere Zusammenarbeit für mehrere Benutzer (Gemeinsame Hauptbücher)
SheetLedger unterstützt nativ die verteilte Buchhaltung für mehrere Benutzer mit Zugriffskontrolle auf Branchenniveau:
1. **So teilen Sie Daten:** Verwenden Sie einfach die offizielle Google Drive/Sheets-Oberfläche, um Ihr Tabellendokument über deren Google-Konto mit Ihren Partnern, Familienmitgliedern oder Geschäftspartnern zu teilen.
2. **Verknüpfung der App:** Lassen Sie diese Personen SheetLedger auf ihren Geräten öffnen und mit genau demselben freigegebenen Google Sheet verknüpfen.
3. **Identitätsbasierte Sicherheit:** Um unbefugte Manipulationen zu verhindern, **sind alle Transaktionsprotokolle an die eindeutige Google-Konto-ID des Erstellers gebunden**. Obwohl mehrere Benutzer innerhalb desselben freigegebenen Hauptbuchs zusammenarbeiten und Daten einsehen können, überprüft unsere State Machine streng die Identitäten: Einträge, die von einer Google-ID erstellt wurden, können von einer anderen ID nicht geändert oder gefälscht werden. Dies garantiert absolute Manipulationssicherheit.

---

### ❓ Häufig gestellte Fragen (FAQ)

#### F1: Warum wird meine Transaktion nicht sofort in Google Sheets angezeigt?

SheetLedger funktioniert nach dem Local-First-Prinzip. Ihre Änderungen werden sofort auf Ihrem Gerät gespeichert, sodass keine Daten verloren gehen. Die Synchronisierung mit Google Sheets erfolgt im Hintergrund, kann jedoch aufgrund von Google-API-Ratenbegrenzungen oder einer schwachen Internetverbindung gelegentlich in eine Warteschlange gestellt werden oder sich verzögern. Seien Sie unbesorgt: Ihre Daten sind lokal absolut sicher.

#### F2: Was passiert, wenn ich versehentlich eine Zeile direkt in Google Sheets bearbeite oder lösche?

Direkte manuelle Bearbeitungen können die strukturelle Integrität und die Sicherheits-Validierungshashes Ihres Hauptbuchs beschädigen. Wenn SheetLedger ungültige manuelle Änderungen erkennt, wird die Synchronisierung für dieses Tabellenblatt zum Schutz Ihrer Daten möglicherweise pausiert. Sollte dies passieren, löschen Sie bitte zuerst das Hauptbuch in der SheetLedger-App, um das weitere Übertragen von Daten zu verhindern. Stellen Sie anschließend die Tabelle über Google Sheets -> Datei -> Versionsverlauf auf eine vorherige Version wieder her (oder kontaktieren Sie den Support). Erstellen Sie schlussendlich ein neues Hauptbuch in SheetLedger und verbinden Sie Ihre Cloud-Daten erneut.

#### F3: Kann ich dasselbe Hauptbuch auf mehreren Geräten bearbeiten?

Ja! Melden Sie sich einfach auf Ihren verschiedenen Geräten mit demselben Google-Konto an und verknüpfen Sie SheetLedger mit demselben Cloud-Tabellenblatt. Das ist eines der größten Highlights dieser App: Das Erlebnis nahtloser Cloud-Daten bei vollständiger Kontrolle über Ihre Daten in Ihrem eigenen Google Drive. Niemand sonst kann darauf zugreifen – selbst wenn die Daten bei Google gespeichert sind, kann Google sie ohne den Entschlüsselungsschlüssel nicht entschlüsseln.

#### F4: Kann ich gemeinsam mit meinem Ehe- oder Lebenspartner Ausgaben in einem Hauptbuch erfassen?

Ja! Teilen Sie dazu einfach das verknüpfte Google-Tabellenblatt über Google Drive mit dem Google-Konto Ihres Partners (erteilen Sie ihm Bearbeiter-Rechte). Lassen Sie Ihren Partner anschließend SheetLedger auf seinem Gerät öffnen und sich mit diesem geteilten Tabellenblatt verbinden. Sie beide können Ausgaben erfassen – unsere Identitätsprüfung stellt sicher, dass alle Einträge fälschungssicher bleiben. In der App können Sie Daten zudem ganz einfach nach bestimmten Benutzern filtern: Während Standarddiagramme die Daten aller Personen analysieren, können Sie eine E-Mail-Adresse als Filter festlegen, wenn Sie beispielsweise nur die Einträge Ihres Partners sehen möchten.

### F5: Warum muss ich mich erneut anmelden, wenn ich ein geteiltes Tabellenblatt auswähle?

Um Ihre Privatsphäre und Datensicherheit zu schützen, fordert SheetLedger nur die minimal erforderliche Berechtigung (drive.file) an. Dadurch kann die App nur auf Tabellenblätter zugreifen, die Sie ausdrücklich autorisieren. Die Auswahl eines von anderen Personen geteilten Tabellenblatts nutzt die offizielle Google Picker-API, welche eine browserbasierte Authentifizierung erfordert. Aus diesem Grund öffnet SheetLedger Ihren externen Webbrowser, damit Sie sich sicher anmelden und das geteilte Tabellenblatt auswählen können.

### F6: Warum kann ich ein von mir manuell erstelltes Google-Tabellenblatt nicht finden?

Aus Datenschutz- und Sicherheitsgründen fordert SheetLedger nur die minimal erforderliche Berechtigung (drive.file) an. Dadurch hat die App ausschließlich Zugriff auf Tabellenblätter, die direkt in dieser App erstellt wurden. Wenn Sie ein Tabellenblatt verknüpfen möchten, das Sie manuell in Google Drive erstellt haben (oder das von einer anderen Person mit Ihnen geteilt wurde), wählen Sie bitte stattdessen die Option „Geteiltes Tabellenblatt verknüpfen“ (Freigegebene Tabellenkalkulation verknüpfen).

#### F7: Welche Einschränkungen gibt es bei der kostenlosen Version im Vergleich zum Premium-Abonnement?

Die Cloud-Funktionen stehen nur mit einem aktiven Abonnement zur Verfügung. Da Google-API-Aufrufe nicht kostenlos sind, müssen wir Limits für die Cloud-Nutzung durchsetzen, um die Betriebskosten zu decken und das Projekt nachhaltig zu betreiben. Bei den lokalen Funktionen (ohne Cloud) sind alle Versionen absolut identisch – es gibt weder Funktionseinschränkungen noch störende Werbung. Wenn Sie keine Cloud-Funktionen benötigen, ist kein Abonnement erforderlich. Für die meisten Nutzer, die Cloud-Funktionen wünschen, empfehlen wir den Basic-Tarif, der alle grundlegenden Cloud-Funktionen abdeckt und die Anforderungen der meisten Anwender vollkommen erfüllt.

#### F8: Kann ich SheetLedger auf Reisen oder ohne Internetverbindung nutzen?

Ja, absolut! SheetLedger ist offline voll funktionsfähig. Sie können Transaktionen jederzeit ohne Netzverbindung hinzufügen, bearbeiten oder suchen. Sobald Sie wieder online sind, synchronisiert SheetLedger alle ausstehenden Offline-Änderungen automatisch mit Ihren Google Sheets.


#### F9: Wie übertrage ich meine Hauptbücher auf ein neues Smartphone oder Tablet?

- Für Cloud-verknüpfte Daten: Laden Sie SheetLedger einfach auf Ihr neues Gerät herunter, melden Sie sich mit demselben Google-Konto an und verbinden Sie es mit Ihrem bestehenden Google-Tabellenblatt-Hauptbuch. Alle Ihre Finanzdaten werden nahtlos abgerufen und synchronisiert.

- Für rein lokale Daten (ohne Cloud): Wenn Ihr Hauptbuch ausschließlich lokal gespeichert und nicht mit Google Sheets verknüpft ist, können Sie unsere integrierte Sicherungs- und Wiederherstellungsfunktion (Backup & Restore) nutzen, um Ihre Daten zu exportieren und auf das neue Gerät zu übertragen.

#### F10: Warum gibt es keine Wiederherstellungsfunktion für Cloud-Daten?

Cloud-Daten werden über eine verteilte Schreibarchitektur verarbeitet. Eine direkte Wiederherstellungsfunktion könnte Schreibkonflikte auslösen und zu Datenbeschädigungen führen. Aus diesem Grund bieten wir keine integrierte Wiederherstellungsfunktion für Cloud-Hauptbücher an. Wenn Sie Ihre Cloud-Daten sichern oder wiederherstellen möchten, können Sie einfach direkt in Google Drive eine Kopie Ihres Google-Tabellenblatts als Backup erstellen. Wenn Sie eine Wiederherstellung benötigen, erstellen Sie einfach ein neues Hauptbuch in SheetLedger und verknüpfen Sie es mit dieser gesicherten Kopie.

---

© 2026 gophini. Entwickelt für ultimative Finanzsouveränität.  
Benötigen Sie technische Unterstützung? Kontaktieren Sie uns unter: **gophini.support@gmail.com**


