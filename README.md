Einstellbarer Rechtecksignalgenerator (Taktgeber)
1. Projektbeschreibung
Im Rahmen dieses Projekts wurde ein einstellbarer Rechtecksignalgenerator entwickelt. Ziel des Projekts ist die Erzeugung eines Rechtecksignals mit einstellbarer Frequenz und Ausgangsamplitude.
Die elektrische Schaltung wurde mit KiCad 9 entworfen. Anschließend wurde auf Grundlage des Schaltplans eine vierlagige Leiterplatte (PCB) entwickelt.
Das Projekt umfasst den Schaltplan, das Leiterplattenlayout, die Bauteilliste (BOM) sowie die zugehörigen Fertigungsdaten.
2. Technische Daten
* Frequenzbereich: 1 Hz bis 1 kHz (Auslegungsziel)
* Ausgangsamplitude: 5 V bis 15 V (Auslegungsziel)
* Versorgungsspannungen: +18 V und +5 V
* Leiterplatte: 4 Lagen
* Entwicklungssoftware: KiCad 9
3. Funktionsweise
3.1 Spannungsversorgung
Die Eingangsspannung wird zunächst über einen Brückengleichrichter (GBU4G) gleichgerichtet und anschließend durch einen Glättungskondensator stabilisiert.
Zwei Spannungsregler stellen die benötigten Versorgungsspannungen bereit:
* L7818CV: +18 V für die entsprechende Schaltungselektronik
* L7805CV: +5 V für den Mikrocontroller und das LCD
Zusätzlich wurde ein zweipoliger Anschluss J5 für einen externen Hauptschalter vorgesehen. Dieser ermöglicht die Unterbrechung einer Eingangsleitung vor dem Brückengleichrichter.
3.2 Signalerzeugung
Zur Erzeugung des Rechtecksignals wird der CMOS-Timer ICM7555IPAZ verwendet.
Die Frequenz wird über Widerstände, ein Potentiometer und umschaltbare Kondensatoren eingestellt.
Ein CD4013BE dient zur Frequenzteilung.
3.3 Einstellung der Ausgangsamplitude
Die Ausgangsstufe basiert auf einem LM358P.
Über ein Potentiometer wird die gewünschte Ausgangsamplitude eingestellt.
3.4 Mikrocontroller und Anzeige
Ein ATmega328P ist zur Verarbeitung der Signale und zur Ansteuerung eines 16×2-LCDs vorgesehen.
Das LCD dient zur Darstellung der relevanten Ausgangsgrößen.
Der Mikrocontroller soll separat programmiert und anschließend in seinen DIP-Sockel eingesetzt werden.
4. Leiterplattenaufbau
Die Leiterplatte wurde mit vier Kupferlagen entworfen:
LageFunktionF.CuSignalleitungen und VersorgungsverbindungenIn1.CuGND-FlächeIn2.CuGetrennte Versorgungsflächen für +5 V und +18 VB.CuSignalleitungen und VersorgungsverbindungenDie Leiterplatte besitzt vier Montagebohrungen (H1–H4) zur mechanischen Befestigung.
Für die Hauptstromversorgung wurden entsprechend breitere Leiterbahnen vorgesehen.
5. Projektdateien
Das Repository enthält folgende Projekt- und Dokumentationsdateien:
* Flachbaugruppe.kicad_pro – KiCad-Projekteinstellungen
* Flachbaugruppe.kicad_sch – Elektrischer Schaltplan
* Flachbaugruppe.kicad_pcb – Vierlagiges Leiterplattenlayout
* Gerber/ – Gerber-Dateien, Bohrdateien und Bauteilpositionsdateien
* Flachbaugruppe_BOM_Final.csv – Aus KiCad exportierte Stückliste
* Rechtecksignalgenerator_BOM_Final.xlsx – Detaillierte Stückliste mit Hersteller- und Bauteilangaben
* Rechtecksignalgenerator_Fertigungsunterlagen.pdf – Fertigungs- und Bestückungsdokumentation
Die Fertigungsdokumentation wird an den aktuellen Entwicklungsstand angepasst.
6. Projektstatus
Der elektrische Schaltplan und das vierlagige Leiterplattenlayout wurden erstellt.
Im weiteren Entwicklungsverlauf wurde ein Anschluss für einen externen Hauptschalter (J5) ergänzt und in das PCB-Layout integriert.
Anschließend wurden die Leiterbahnen angepasst und die Design-Rule-Prüfung (DRC) durchgeführt.
Ergebnis der letzten DRC-Prüfung:
* 0 Leiterplattenverstöße
* 0 unverbundene Elemente
* 4 Hinweise zur Schaltplanparität aufgrund der ausschließlich auf der Leiterplatte vorhandenen Montagebohrungen H1–H4
Die Gerber-Dateien, Bohrdateien und Bauteilpositionsdateien wurden exportiert. Die Stückliste wurde aktualisiert.
Eine physische Fertigung und Bestückung der Leiterplatte sowie eine messtechnische Funktionsprüfung wurden bisher nicht durchgeführt.
7. Fazit
Im Rahmen des Projekts wurde ein vollständiger Schaltungsentwurf mit zugehörigem vierlagigem Leiterplattenlayout für einen einstellbaren Rechtecksignalgenerator erarbeitet.
Die Entwicklung umfasst die Spannungsversorgung, Signalerzeugung, Frequenzteilung, Ausgangsstufe sowie die vorgesehene Mikrocontroller- und LCD-Anbindung.
Die Projektdateien stehen zur weiteren Überprüfung, Weiterentwicklung und gegebenenfalls späteren Fertigung zur Verfügung.

