# Sicherheit und Grenzen

**Stand: 02.10.2026. Technische Beschreibung eines noch nicht freigegebenen Entwicklungsstands.**

PraxisSchutz verschlüsselt PDFs lokal mit PDF-AES-256 über qpdf. Der Patientencode wird auf
Papier übergeben. Der lokale Tresor ist unter Windows an das Benutzerkonto gebunden; portable
Sicherungen sind zusätzlich mit einem eigenen Wiederherstellungsschlüssel verschlüsselt.
Es gibt keinen Patienten-Cloud-Dienst, laufenden Lizenzserver oder Versand durch die App.

Die Sperre der erneuten Codeanzeige nach bestätigtem Kartendruck schützt vor beiläufigem
Nachsehen in der Oberfläche. Sie ist keine Zusage, dass ein kompromittierter Praxis-PC die
Codes nicht erfassen kann. Beim Verschlüsseln muss der Code verfügbar sein. Ein zusätzlicher
Praxisschlüssel, der vor der Verschlüsselung pro Sitzung eingegeben wird, ist in Arbeit;
sein Schutz darf erst nach technischer Prüfung und Freigabe behauptet werden.

PraxisSchutz schützt weder das Originaldokument, unverschlüsselte E-Mail-Metadaten noch vor
Phishing oder Schadsoftware auf dem Praxis-PC. Windows-Updates, getrennte Konten,
Geräteverschlüsselung, sichere Druckerablage und getestete Datensicherungen bleiben
Aufgaben der Praxis-IT. Die rechtliche Eignung eines konkreten Versandprozesses ist getrennt
zu prüfen.

Registrierungsschlüssel, Patientencode und Wiederherstellungsschlüssel haben verschiedene
Zwecke. Der Registrierungsschlüssel schaltet Arbeitsvorgänge frei, öffnet aber keine PDFs.
