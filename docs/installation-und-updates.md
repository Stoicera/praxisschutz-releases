# Installation, Datensicherung und Updates

**Stand: 02.10.2026. Öffentliche Vorabversion; vollständige Windows-11-Abnahme und digitale Signatur stehen noch aus.**

Für die betreute Einführung:

1. Den Windows-11-x64-Installer aus diesem Repository herunterladen und die veröffentlichte
   SHA-256-Prüfsumme mit der heruntergeladenen Datei vergleichen. Nur das ausdrücklich
   öffentliche Release verwenden, keine internen CI-Artefakte. Windows kann „Unbekannter
   Herausgeber“ anzeigen; bei einer Sperre durch die Praxis-IT nicht die Schutzfunktion abschalten.
2. Im vorgesehenen Windows-Benutzerkonto installieren und starten. Die Installations-ID
   unter „Lizenz & Freischaltung“ für eine externe Rechnung an Lugmayr-Kern übermitteln.
   Bitte keine Patientendaten mitsenden.
3. Den nach Zahlungseingang ausgestellten Registrierungsschlüssel in der App eintragen.
   Jede Installation unter einem Windows-Benutzerkonto benötigt eine eigene Aktivierung.
4. Einen Praxisschlüssel mit mindestens zwölf Zeichen selbst wählen oder den erzeugten
   Zufallsschlüssel geschützt notieren. Er gehört nicht in E-Mails oder unverschlüsselte
   Dateien. Nach jedem Neustart ist er einmal für neue PDFs einzugeben.

Die portable Sicherung enthält Patientenangaben, Codes und Praxiseinstellungen, aber keine
Original-PDFs und keine Lizenz. Jede Sicherung hat einen eigenen Wiederherstellungsschlüssel.
Sicherungsdatei, gedruckten Wiederherstellungsschlüssel und Praxisschlüssel getrennt
aufbewahren. Beide Schlüssel sind für die Nutzung der gesicherten Codes nötig. Änderungen nach dem Export
sind nicht in dieser Sicherung enthalten. Die Wiederherstellung regelmäßig mit Testdaten
auf einem getrennten Windows-PC üben.

Die direkte Windows-Installation prüft nicht selbst im Netz auf Updates. Vor einem Update
eine neue portable Sicherung erstellen, Versionshinweise und offenen Prüfstand lesen, die Prüfsumme
vergleichen und den neueren Installer im vorgesehenen Benutzerkonto installieren. Danach Start,
Lizenzstatus, Patientenliste und eine Verschlüsselung mit Testdaten prüfen. Eine Wiederherstellung
mit Testdaten auf einem getrennten Windows-Konto üben. Für einen neuen PC oder ein anderes
Windows-Konto ist eine neue Installations-ID und abgestimmte Aktivierung erforderlich.

**Bekannter Befund beim Wechsel von 0.1 auf 0.2:** In einer Windows-11-Test-VM scheiterte
die im Installer vorausgewählte Deinstallation der alten Version. Die Option „Nicht
deinstallieren“ installierte 0.2; der synthetische Patient blieb erhalten. Dieser Weg
ist noch nicht vollständig abgenommen. Bestehende Installationen nur nach frischer
Sicherung und mit Herstellerbegleitung aktualisieren.

Bei Problemen Tresordateien nicht manuell löschen. Version, Zeitpunkt und eine neutrale
Fehlerbeschreibung an den Hersteller senden, aber niemals Patientendaten, Codes oder
Wiederherstellungsschlüssel.
