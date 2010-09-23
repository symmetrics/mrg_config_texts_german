* DOCUMENTATION

** INSTALLATION
Extrahieren Sie den Inhalt dieses Archivs in Ihr Magento Verzeichnis.
! Das Modul überschreibt den Block footer_links !

** USAGE
Das Modul erstellt Blöcke mit Beispieltexten und 
installiert deutsche E-Mail Templates. Alle Webshops,
die in Deutschland betrieben werden, müssen bestimmte
 Voraussetzungen erfüllen und unterschiedliche Informationen 
für den Verbraucher beinhalten. So muss der Verbraucher 
über z.B. Versandkosten, Bezahlmethoden, Bestellprozess usw. 
explizit im Shop informiert werden. Um die Arbeit für 
den Shopbetreiber zu erleichern, installiert das Modul 
alle benötigten Texte, die u.A. auch vom Modul
Symmetrics_ConfigGerman, Symmetrics_Agreement usw. 
verwendet werden. 

Es werden auch rechtskonforme E-Mail Templates
 installiert, die AGBs und Widerrufsbelehrungen beinhalten. 
Die Templates sind alle in Deutsch übersetzt. 

Symmetrics_ConfigGermanTexts erstellt u.A. Blöcke 
für AGBs und Widerrufsbelehrungen, die überall auf der 
Webseite verwendet werden können. Dies erleichtert die 
Arbeit erheblich, wenn die Texte ausgetauscht oder 
angepasst werden müssen, da die relevanten Stellen nun
 alle zentralisiert werden, ebenso greift die Zentralisierung 
bis auf die E-mail Templates, die die Textänderungen ebenso 
bekommen würden. 
Am Beispiel der AGB: 

Sie ändern den eigentlichen AGB-Text in CMS -> Static
Blocks und die Änderungen erscheinen in 
Bestellbedingungen am Ende des Checkout-Prozesses
 (Voraussetzung ist, dass das Modul Symmetrics_Agreement
installiert ist), auf der Seite "AGB" und in allen
 E-Mail Templates. 
ACHTUNG! Das Modul überschreibt die Konfiguration von
 E-Mail Templates. Die E-Mail Templates werden aber nicht 
ersetzt. Es werden neue E-Mail Templates hinzugefügt und 
die Konfiguration so angepasst, dass diese E-Mail 
Templates benutzt werden.
 
WICHTIG! Die Daten aus config.xml werden nur bei einer 
Neuinstallation des Moduls in die Datenbank
 geschrieben. Alle weiteren Aenderungen in config.xml
 werden ignoriert. Alle Aenderungen, die nach der
 Installation gemacht werden, müssen über die Admin-
Oberfläche erfolgen.

 Das Modul Symmetrics_ConfigGermanTexts arbeitet eng 
mit dem Modul Symmetrics_Agreement zusammen. Es ist
 empfehlenswert das Modul Symmetrics_Agreement ebenfalls 
zu installieren. Symmetrics_ConfigGermanTexts erstellt 
Blöcke und Seiten, die von Symmetrics_Agreement benutzt 
werden. 

Es besteht auch eine Verbindung zu dem Modul
Symmetrics_Imprint, welches die Impressuminformationen
 liefert. Auf der CMS-Seite Impressum und in AGBs finden
 Sie die Programmaufrufe von diesem Modul. Es werden 
auch Beispieltexte für Symmetrics_Imprint installiert.
Sichtbar werden diese aber nur, wenn das Modul 
Symmetrics_Imprint installiert ist. 

Das Modul installiert auch Beispieltexte für andere 
Symmetrics Konfigurations-Module, wie z.B. 
Symmetrics_InvoicePdf und Symmetrics_InvoicePdf.

** FUNCTIONALITY
*** A: Erstellt Seiten für:
        Seite nicht gefunden
        Impressum
        Zahlungsarten
        Datenschutz
        Lieferung
        Bestellvorgang

*** B: Erstellt zentrale Blöcke für AGBs und Widerrufsrecht
        mrg_business_terms -> AGB
        mrg_revocation -> Widerrufsbelehrung

*** C: Erstellt untere Link-Leiste (inkl. leere AGB- und 
        Widerrufsrecht-Links)

*** D: Ersetzt Standard E-Mail Templates mit Rechtskonformen
        und übersetzten E-Mail Templates inkl. AGB und 
        Widerrufsbelehrung

*** E: Alle Texte sind vor der Installation zentral über 
        HTML-Dateien veränderbar (app/locale/de_DE)
        
*** F: Übersetzt einige fehlende bzw. nicht-rechtskonform
        übersetzte Strings. Sichtbar sind diese unter
        app/locale/de_DE/Symmetrics_ConfigGermanTexts.csv

** TECHNICAL 
Die gesamte Funktionalität des Moduls findet in einem Migrationsskript
 gekoppelt mit dem Setup-Model statt.

** PROBLEMS
  Keine Probleme bekannt.

* TESTCASES
** BASIC
*** A: Prüfen Sie, ob die Seiten entsprechend angelegt wurden
*** B: Prüfen Sie, ob die Blöcke entsprechend angelegt wurden
*** C: Prüfen Sie, ob die untere Linkleiste korrekt angelegt wurde
        und alle Links funktionieren
*** D: Prüfen Sie, ob die Emails entsprechend angelegt wurden.
        Gehen Sie ins Back-End unter "System" -> "Transactions-Emails".
        Klicken Sie bei jeder Email auf "Vorschau". Falls Sie eine leere Seite
        sehen, bedeutet das, dass der Fehler aufgetreten ist.
*** E: Ändern Sie vor der Installation die Dateien und prüfen Sie,
        ob die Texte übernommen werden.
*** F: Überprüfen Sie, ob die Strings alle korrekt übersetzt werden.