# Ideenwerk – Business Dashboard

Öffne **index.html** per Doppelklick in einem aktuellen Browser. Es ist keine Installation erforderlich. Die drei Dateien index.html, style.css und app.js müssen im selben Ordner bleiben.

## Funktionen

- Ideen erstellen, bearbeiten und nach Aktiv, Wartend oder Nicht mehr verfolgt einordnen.
- Themenbezogene Vorschläge über einen Vorlagengenerator erstellen und anschließend bearbeiten. Dies ist kein KI-Dienst.
- Umsatz und Steuern je Idee eintragen. Unter „+ Ressource“ einzelne Kosten und Stunden mit Datum und Beschreibung erfassen.
- Nettogewinn wird aus Umsatz minus Ressourcenkosten minus erfassten Steuern berechnet. Nur vollständig erfasste Kosten und Steuern ergeben einen vollständigen Nettogewinn; unbezahlte Zeit wird nicht automatisch in Kosten umgerechnet.
- Ideen und Ressourcen unabhängig als CSV exportieren. Exporte und Kennzahlen berücksichtigen die aktuellen Filter. Semikolon und Dezimalkomma sind für deutsches Excel vorbereitet.
- Vollständige JSON-Sicherungen herunterladen und wieder importieren. Import ersetzt nach Bestätigung die aktuelle Liste.

## Speicherung und Veröffentlichung

Die Anwendung speichert ausschließlich im lokalen Browser (localStorage). Keine Konten, kein Server, keine Synchronisierung zwischen Geräten. Bei Browserwechsel, Dateiverschiebung oder Löschen der Browserdaten können die Daten fehlen. Deshalb regelmäßig eine Sicherung herunterladen. Vorhandene kompatible Daten im Browser unter „business-ideas“ werden übernommen; Daten aus der speziellen window.storage-Umgebung des ursprünglichen JSX sind nicht automatisch zugänglich.

Zum Veröffentlichen die drei Webdateien auf einen statischen Webhost hochladen. Die Seite ist dafür vorbereitet, aber noch nicht öffentlich veröffentlicht. Auch bei Veröffentlichung bleiben Daten pro Browser getrennt. Für gemeinsame Konten, geräteübergreifende Daten und echte KI-Generierung wäre ein Backend mit Datenbank und sicher angebundenem KI-Dienst erforderlich.

## Technischer Aufbau

Die Funktionen des bereitgestellten React-Entwurfs wurden als eigenständig lauffähige HTML/CSS/JavaScript-Seite umgesetzt. Keine externen Bibliotheken, CDN-Abhängigkeiten oder API-Schlüssel erforderlich. Nutzereingaben werden bei der HTML-Ausgabe maskiert, CSV-Textfelder gegen Formelausführung abgesichert und Importe vor dem Speichern validiert.
