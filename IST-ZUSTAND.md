# Ist-Zustand – Echt Hamburg GmbH

## Netzwerk
- Standort: Neue Räumlichkeiten in der Hafencity
- Verkabelung abgeschlossen, Server + Clients installiert
- Internetzugang über Router
- Domäne: `eHH.de`
- Server stehen in separatem Serverraum

## Serverdienste
1. **DNS**
   - Zone `eHH.de`
   - Forward- & Reverse-Lookup eingerichtet
   - Aliasse:
     - `www.echt-hamburg.de` (Webservice)
     - `mail` (E-Mailservice)
     - `db` (Datenbank)

2. **DHCP**
   - Server = feste IPs
   - Clients = dynamische Adressen
   - Gateway, DNS und Domänenname werden verteilt

3. **Verzeichnisdienst (AD)**
   - Authentifizierung über Anmeldeserver
   - Benutzer nach Organigramm strukturiert
   - Anmeldenamen: `vorname.nachname@eHH.de`
   - Gast-Accounts: `gast_1` – `gast_10`
   - Homelaufwerke für Beschäftigte (h:\), automatisch eingebunden
   - Gäste = kein Homelaufwerk

4. **Fileservice**
   - Abteilungsverzeichnisse (mit Änderungsrechten für Mitglieder)
   - Vorstand = Leserechte
   - Globalverzeichnis mit Leserechten für alle
   - Gäste = keine Laufwerke/Berechtigungen

5. **Webservice**
   - Öffentlicher Webserver: `www.echt-hamburg.de`
   - Funktionen:
     - Startseite
     - Eventbuchung
     - Onlineshop
     - Barangebote

6. **Datenbankservice**
   - Datenbank `eHH` für Shop & Events
   - Adminnutzer mit vollen Rechten
   - Zugriff über Webshop-Frontend

7. **E-Mailservice**
   - Adressen: `vorname.nachname@eHH.de`
   - Protokolle: IMAP & SMTP
   - Kalenderfunktion
   - Gastnutzer ausgeschlossen

8. **FTP**
   - Für Event-Mitarbeiter und Vorstand
   - Zugriff per Tablet/Laptop (Dateien hoch- & runterladen)

9. **Softwareverteilung**
   - Zentrale Verteilung von:
     - PDF-Reader
     - VLC
     - Firefox
   - Alte Versionen werden automatisch deinstalliert

10. **Zentralisierter Virenschutz**
    - Updates zentral auf Server, dann auf alle Clients verteilt

11. **Benutzerumgebung (GPO)**
    - Nur benötigte Ressourcen nutzbar
    - Standardordner werden auf Homelaufwerk umgeleitet
    - Einschränkungen für Gäste (Kioskmode, kein Drucken, keine Softwareinstallation)

12. **Druckservice**
    - Zentraler Netzwerkdrucker für Beschäftigte
    - PDF-Drucker vorhanden
    - Gäste = keine Druckrechte

13. **Updateservice**
    - Zentral gesteuerte Updates für Server & Clients
    - Stichtag: 20. jedes Monats, 17:00 Uhr

14. **Backup**
    - Nach "Großvater-Vater-Sohn-Prinzip"

15. **Ausfallsicherheit**
    - RAID-System implementiert

## Schwachstellen
- Dienste werden lokal gehostet
- Manuelle Einrichtung & Wartung
- Kein Monitoring
- Reaktion auf Fehler/Ausfälle zu spät
- Prozesse = zeit- und kostenintensiv
