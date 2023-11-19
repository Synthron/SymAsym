# SymAsym

High Power Audio Amplifier based on the Red Devil SymAsym PCBs from audiopcb.de

For complete system schematic of a stereo amplifier, refer to _**Overview_Schematic.pdf**_

Specs:  

- 350W @ 4 Ohm
- 185W @ 8 Ohm

Zusätzliches Empfangsmodul "Up2Stream Pro V3" empfohlen.

## Warenkörbe Reichelt

- [Black Devil Amplifier](https://www.reichelt.de/my/2100439) 
  - 2x benötigt für Stereo
  - Extra Kühlkörper benötigt - siehe unten
- [Netzfilter und Softstart](https://www.reichelt.de/my/2100481)
  - designed für Stereo, für Mono in der Mitte teilen
- [VU-Meter](https://www.reichelt.de/my/2100492)
- [Digital-Support](https://www.reichelt.de/my/2100502)
  - Extra OLED benötigt (I2C-Schnittstelle, siehe unten)

## Einstellung

- Vor Inbetriebnahme Poti so drehen, dass zwischen unterem Pin R24 und linkem Pin R9 500 Ohm Widerstand gemessen werden.  
- Kurzschlussbrücke am Signaleingang einstecken für Abgleich.  
- Spannung anschließen und am Ausgang messen, sollte ca. 0V betragen.  
- Jetzt Poti so lange drehen, bis zwischen TP1->TP3 und TP2->TP3 jeweils 55mV (0,055V) anliegen.  
- Fertig

## Anmerkungen

### Amplifier

**Wichtig!!!**  
Der Warenkorb ist nur für eine Platine! Für einen Stereo-Verstärker bitte zwei mal bestellen!

**2N5551 und 2N5401 Transistoren:**  
Anstatt passender Anzahl sind in den Warenkörben zu viele eingetragen. Dadurch hat man genug Transistoren um die drei notwendingen Paare matchen zu können. Siehe Schaltplan, welche Transistoren gematcht sein müssen.

**Kühlkörper**  
Die Leistungstransistoren müssen mit einer Glimmerscheibe gegen den Kühlkörper isoliert werden. Elektrisch isolierende Wärmeleitpads sind auch ok. Keinesfalls nur Wärmeleitpaste benutzen!

Beispiel [Silikonfolie](https://www.reichelt.de/silikon-isolierfolie-200x200x0-18mm-si-4018-p35416.html?&trstct=pos_1&nbc=1); [Glimmer TO220](https://www.reichelt.de/glimmerscheibe-fuer-gehaeuse-to-220-glimmer-to-220-p8194.html?&trstct=pos_5&nbc=1)  
Die Isolierbuchsen (im Warenkorb) müssen bei den MJE-Transistoren (TO220) verwendet werden!

---

### Netzfilter und Softstart

Die Sicherungshalter sind einzelne Federn, beim Einlöten mit 5x20mm Feinsicherung ausrichten.  

---

### VU-Meter

Vorsicht: LEDs und Potis auf Rückseite und alles außer LEDs/Terminals ist SMD.

Zum Abgleichen: maximale gewollte Lautstärke aufdrehen, mit Potis so einstellen, dass nur die erste rote LED leuchtet.  
Für beide Kanäle einzeln einrichten.

---

### Digital-Support

Die Sicherungshalter sind einzelne Federn, beim Einlöten mit 5x20mm Feinsicherung ausrichten.  
Fast alle Bauteile sind SMD.

NTC-Widerstände werden direkt an die Kühlkörper geschraubt!

Die Bedienung erfolg neben dem Drehencoder über ein OLED, original wird [dieses](https://www.reichelt.de/entwicklerboards-display-oled-2-42-128x64-pixel-debo-oled-2-42-p335005.html?&trstct=pos_3&nbc=1) benutzt.

Wenn **kein** Up2Stream benutzt wird, PD2 und GND verbinden.

Konfiguration für Standard Eingang:

| Standard Eingang      | PD3 | PD4 |
|-----------------------|:---:|:---:|
| Kein Eingang          | GND | GND |
| Eingang 1 (Klinke)    |  5V | GND |
| Eingang 2 (Cinch)     | GND |  5V |
| Eingang 3 (Up2Stream) |  5V |  5V |

Der Kanal kann über den Drehencoder jederzeit geändert werden.  
Wenn das Up2Stream-Modul angeschlossen ist, werden je nach Möglichkeit aktuelle Song-Infos auf dem OLED angezeigt. 

---

### Gehäuse

Beim Entwurf wurde alles auf [dieses Gehäuse](https://www.reichelt.de/19-rack-gehaeuse-3-he-sin-3-he-sw-p247242.html?&trstct=pos_0&nbc=1) ausgelegt.

---

### Kühlkörper

Pro Verstärkerplatine sollte ein Kühlkörper mit maximal 0,5K/W vorgesehen werden. Für das oben genannte Gehäuse bietet sich [dieser Kühlkörper](https://www.reichelt.de/kuehlkoerper-100-mm-alu-0-4-k-w-sk-56-100-sa-p227981.html?&trstct=pol_5&nbc=1) an. Er ist 1cm zu lang, das kann aber zur Not gekürzt werden. 