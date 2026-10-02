# PraxisSchutz v0.2.0-rc.1 — Stand der öffentlichen Vorabversion

Stand: 02.10.2026. Diese Version ist für Windows 11 x64 vorgesehen. Der Gründer hat die
öffentliche Bereitstellung für eine betreute Einführung entschieden. Sie ist **eine
Vorabversion**, kein vollständig abgenommener Final-Release.

## Enthalten

- Lokale Verschlüsselung von PDF-Dateien mit AES-256 über qpdf; eine Papierkarte pro
  Patientin oder Patient enthält den persönlichen Dokumentencode. Die App versendet
  weder PDF noch Code selbst.
- Patientenliste und Codes im lokalen Windows-Benutzerkonto. Zusätzlich schützt ein
  selbst gewählter Praxisschlüssel ab zwölf Zeichen oder ein erzeugter Zufallsschlüssel
  die gespeicherten Codes. Neue PDF-Arbeit erfordert einmaliges Entsperren je Sitzung;
  erneute Codeanzeige und Codewechsel verlangen eine frische Schlüsselbestätigung.
- Portable verschlüsselte Sicherung mit eigenem Wiederherstellungsschlüssel. Sie
  umfasst Patienten, Codes und Einstellungen, aber keine Original-PDFs und keine Lizenz.
- Offline-Lizenzschlüssel für 299 EUR netto pro Praxis/Jahr, bis zu drei getrennte
  Installationen. Externe Rechnung und Überweisung. Jede Installation hat eine eigene
  Installations-ID; der Hersteller stellt den passenden Schlüssel aus.
- Manueller Updateweg: neueren Installer von diesem Repository laden, Prüfsumme
  vergleichen und nach frischer Sicherung im vorgesehenen Windows-Konto installieren.
  Die App lädt keine Updates selbst herunter.

## Nachgewiesen und noch offen

Der GitHub-Actions-Bau prüft Rust/TypeScript, baut den Windows-Installer, installiert
ihn still und führt einen synthetischen Selbsttest aus. Die vollständige Abnahme des
**exakten herunterladbaren Installers** auf Windows 11 ist noch offen (39 Prüfpunkte
im privaten Testprotokoll). Dazu gehören Papierdruck, zweites Windows-Konto, reales
Update, Wiederherstellung und Registrierung auf dem Ziel-PC. Der Installer und die
mitgelieferten Programmdateien sind derzeit **nicht digital signiert**. Windows kann
„Unbekannter Herausgeber“ anzeigen; verwaltete Geräte können die Installation sperren.

Beim ersten manuellen Update von der alten 0.1-Version in einer Windows-11-Test-VM
schlug die vorgewählte Option „Vor der Installation deinstallieren“ mit
„Error launching installer“ und „Unable to uninstall“ fehl. Mit „Nicht deinstallieren“
schloss 0.2 die Installation ab und der synthetische Patient blieb sichtbar. Dies ist
ein offener Update-Befund; bestehende Installationen nur nach frischer Sicherung und
mit Herstellerbegleitung aktualisieren. Eine Neuinstallation auf einem leeren PC ist
von diesem Altversions-Befund nicht betroffen.
Eine solche Sperre sollte durch die Praxis-IT geklärt werden, nicht durch Abschalten
einer Schutzfunktion.

Vor der Verarbeitung echter Patientendaten mit **synthetischen Beispieldaten** auf dem
konkreten PC die Installation, Kartendruck, Verschlüsselung und Öffnung des PDFs,
Sicherung und Wiederherstellung durchspielen. Originaldokumente, Drucker, Benutzerkonten,
BitLocker, Virenschutz und E-Mail-Prozess bleiben Teil der Praxis-IT. Ein verlorener
Praxisschlüssel kann vom Hersteller nicht wiederhergestellt werden.

Die Binärdatei des Releases und die `.sha256`-Datei müssen denselben SHA-256-Wert
ergeben. Eine neu veröffentlichte Version erhält einen eigenen Tag und eine neue
Prüfsumme; vorhandene Assets werden nicht still ersetzt.

Weitere Informationen:
[Installation und Updates](installation-und-updates.md),
[Sicherheit und Grenzen](sicherheit.md),
[Lizenz und Rechnung](lizenz.md).
