# Sicherheit und Grenzen

**Stand: 02.10.2026. Technische Beschreibung eines noch nicht freigegebenen Entwicklungsstands.**

PraxisSchutz verschlüsselt PDFs lokal mit PDF-AES-256 über qpdf. Der Patientencode wird auf
Papier übergeben. Der lokale Tresor ist unter Windows an das Benutzerkonto gebunden; portable
Sicherungen sind zusätzlich mit einem eigenen Wiederherstellungsschlüssel verschlüsselt.
Es gibt keinen Patienten-Cloud-Dienst, laufenden Lizenzserver oder Versand durch die App.

Der neue, noch nicht für Patientendaten freigegebene Entwicklungsstand legt gespeicherte
Codes in eine zusätzliche age/Scrypt-Hülle. Ein selbst gewählter Praxisschlüssel braucht
mindestens zwölf Zeichen; alternativ erzeugt die App einen zufälligen Schlüssel. Die
Praxis entsperrt ihn einmal pro Sitzung vor neuen PDFs. Zum Anzeigen eines bestätigten
Codes oder Erneuern ist eine frische Eingabe erforderlich. Ein kompromittierter laufender
Prozess kann Passwort und Codes dennoch möglicherweise erfassen. Die Windows-Abnahme des
exakten Installers und die Praxisfreigabe stehen aus.

PraxisSchutz schützt weder das Originaldokument, unverschlüsselte E-Mail-Metadaten noch vor
Phishing oder Schadsoftware auf dem Praxis-PC. Windows-Updates, getrennte Konten,
Geräteverschlüsselung, sichere Druckerablage und getestete Datensicherungen bleiben
Aufgaben der Praxis-IT. Die rechtliche Eignung eines konkreten Versandprozesses ist getrennt
zu prüfen.

Registrierungsschlüssel, Patientencode und Wiederherstellungsschlüssel haben verschiedene
Zwecke. Der Praxisschlüssel schützt gespeicherte Codes. Der Registrierungsschlüssel
schaltet Arbeitsvorgänge frei, öffnet aber keine PDFs. Für Codes in einer neuen portablen
Sicherung sind Wiederherstellungs- **und** Praxisschlüssel nötig.
