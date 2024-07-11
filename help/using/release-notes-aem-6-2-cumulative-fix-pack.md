---
title: AEM 6.2 Cumulative Fix Pack
description: Erfahren Sie mehr über die AEM 6.2 Cumulative Fix Pack-Versionshinweise.
exl-id: f1c2d4ff-590b-46b5-b2b1-e2b5141f7cc0
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '21082'
ht-degree: 72%

---

# AEM 6.2 Versionshinweise zum Cumulative Fix Pack{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived by way of UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Versionsinformationen {#release-information}

| **Produkt** | Adobe Experience Manager |
|---|---|
| **Version** | 6.2 |
| **Version** | Cumulative Fix Pack 6.2 SP1-CFP20 |
| **Voraussetzung** | [AEM 6.2 Service Pack 1](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) |
| **Allgemeine Verfügbarkeit** | 6. Juni 2019 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe hat ein Modell für die einmalige Bereitstellung für die Veröffentlichung von Fehlerbehebungen eingeführt. Anstatt Hotfixes für einzelne Probleme freizugeben, veröffentlicht Adobe jetzt jeden Monat ein Cumulative Fix Pack (CFP) (vorbehaltlich erfolgreicher Qualitätsprüfungen). Ein CFP ist ein aggregiertes Inhaltspaket für mehrere Fehlerbehebungen. CFPs enthalten in erster Linie Fehlerbehebungen, können aber auch Feature Packs enthalten. Sie bieten die folgenden Vorteile gegenüber einzelnen Hotfix-Versionen:

* Kumulative Natur (z. B. enthält CFP-Fehlerbehebungen, die durch frühere CFPs bereitgestellt wurden)
* Erhöhte Qualitätssicherung
* Vereinfachte Installation (Benutzerinnen bzw. Benutzer installieren CFPs als einzelnes Paket ohne Abhängigkeiten, außer dem neuesten Service Pack)

Weitere Informationen zu CFPs und anderen Versionstypen finden Sie unter [Maintenance Release Vehicle](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

## Informationen zur Version {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20 ist das letzte Cumulative Fix Pack für AEM 6.2 und ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) wichtige kundenspezifische Korrekturen enthält.

>[!CAUTION]
>
>Das Anwenden von CFP ohne Überprüfung der Kompatibilität zwischen installierten Feature Packs kann zu einem Systemfehler oder zum Verlust von benutzerdefinierten Konfigurationen führen, was eine Wiederherstellung von der Sicherung bis zur Auflösung erfordern könnte.

>[!NOTE]
>
>* Ein neues Sling `discovery- api`-Bundle Johnzon 1.0.0 ist im AEM Cumulative Fix Pack 6.2 SP1-CFP10 enthalten. Darüber hinaus wird ein sling-discovery-Dienstbenutzer mit Lese- und Schreibberechtigung für den Knoten */var/discovery* im CRX-Repository hinzugefügt.
>
>* Das E-Mail-Paket von Apache Commons **org.apache.commons/commons-email/1.5** wurde hinzugefügt und ersetzt **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
>
>* Adobe empfiehlt die Bereitstellung von CFP über den Installationsordner für die Kundschaft, die viele Benutzende auf AEM-Instanzen hat.
>

## Enthaltene Probleme {#issues-included}

In diesem Abschnitt werden alle im aktuellen CFP enthaltenen Probleme und Hotfixes aufgeführt.

Darüber hinaus enthält dieses CFP Hotfixes, die in [früheren Cumulative Fix Packs](#previous) bereitgestellt wurden.

### Integration {#integration}

* Rückportierung mehrerer Verbesserungen der Targeting-Personalisierung in Campaign. NPR-29163: Hotfix für CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler wird in eine unendliche Schleife verschoben und führt bei Veröffentlichungsinstanzen zu Aktualisierungen der Knoten. NPR-28561: Hotfix für CQ-4263096

### DAM - Allgemeines {#dam-general}

* Die Replikationsschaltfläche für Benutzer ohne Administratorrechte in bestimmten DAM-Ordnern kann nicht angezeigt/ausgeblendet werden. NPR-29026: Hotfix für CQ-4265361

### Schwachstelle {#vulnerability}

* Das CSRF Protection Framework funktioniert nicht mit AEM Foundation-Formularen. NPR-28612: Hotfix für GRANITE-22231

### Formulare {#forms}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package}

>[!NOTE]
>
>Für AEM Forms-Kunden ist es wichtig, das AEM Forms-Add-On-Paket nach der Installation von AEM Service Pack, Cumulative Fix Pack oder Feature Pack zu installieren.

>[!NOTE]
>
>AEM Forms-Add-on-Pakete helfen, die Formularfunktionalität mit AEM Service Packs und Cumulative Fix Packs abzustimmen. Daher ist es unerlässlich, das AEM Forms-Add-on-Paket nach der Installation eines AEM Service Packs, Cumulative Fix Packs oder Feature Packs zu installieren.

#### Adaptive Formulare {#adaptive-forms}

* Probleme mit der Benutzerfreundlichkeit bei der Scribble-Komponente für Geräte mit iOS 12.1. NPR-29082: Hotfix für CQ-4261765

#### Forms - Document Security {#forms-document-security}

* Beim Überprüfen aller Signaturen in einer PDF-Datei mit PAdES (PDF Advanced Electronic Signatures) wird eine InvalidOperationException ausgelöst. NPR-27848: Hotfix für CQ-4244837

#### Forms – Korrespondenz {#forms-correspondence}

* Bei der Vorschau des Briefs als PDF berücksichtigt das auf der primären Seite platzierte Textfeld nicht den auf der Registerkarte &quot;Daten&quot;eingegebenen Wert oder die angegebene Datenverknüpfung. NPR-29239: Hotfix für CQ-4266856.

#### Forms – Interaktive Kommunikation {#forms-interactive-communication}

* Wenn ein Apostroph hinzugefügt wird, erscheinen die vorab ausgefüllten Felder im Brief als ASCII-Zeichen anstelle von regulären Alphabeten. NPR-28863: Hotfix für CQ-4262900

### JEE-Installationsprogramm von Forms {#forms-jee-installer}

* Keine neuen Fehlerbehebungen im JEE-Installationsprogramm von AEM Forms.

## Hotfixes und Feature Packs, die in früheren Cumulative Fix Packs enthalten waren {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulative Fix Pack 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Unterstützung für MS® Translator API v3.0 in AEM 6.2 aktiviert
* Protokollmeldung nach erfolgreicher Installation des Pakets für alle SPs, CFPs und HFs hinzugefügt.

### Assets {#assets}

* Sie können einen DAM-Ordner nicht umbenennen, wenn die Berechtigung ACL bearbeiten fehlt. NPR-27555: Hotfix für CQ-104652
* Das Bildvorgabe-Editor-Tool ist in 6.2.1 CFP 17 und höher nicht responsiv. NPR-28147: Hotfix für CQ-4261041

### Sites {#sites}

* Der Link-Prüfer schließt den Vorgang nicht ab und bleibt bei nicht reagierenden Links hängen. NPR-27373: Hotfix für CQ-4256030
* Die Segmentdatei wird nicht richtig geladen, da ein zusätzliches Stammverzeichnis den Pfad des Segments unterbricht. NPR-28014: Hotfix für CQ-4260332

### Integration {#integration-1}

* Die Aufhebung der LiveCopy-Vererbung funktioniert für zielgerichtete Container nicht ordnungsgemäß. NPR-28129: Hotfix für CQ-4259813
* Die `cq:actions` werden bei einer zielgerichteten Komponente nicht berücksichtigt. NPR-27616: Hotfix für CQ-4257497

* Die Anzeige des Symbols zum Aufheben der Vererbung ist nicht kohärent. NPR-27671: Hotfix für CQ-4257779

### Felix {#felix}

* Die Details zur Web-Konsolenkomponente schlagen mit Meldung „500“ nach der CFP 18-Installation auf der AEM 6.2 SP1-Instanz fehl. NPR-28350: Hotfix für CQ-4261095

### Übersetzung {#translation}

* Aktivieren der Unterstützung für den MS® Translator-Service in AEM 6.3 nach der Aktualisierung von MS® Translator auf API-Version 3.0. NPR-28123: Hotfix für CQ-4259096

### Benutzeroberfläche - Foundation {#ui-foundation}

* OOTB-Sites-Kalender zeigt falsche Daten an. NPR-28392

### Granite {#granite}

* Das Wörterbuch ist für die Ressourcenpakete mit `sling:basename` nicht ungültig. NPR-27624

### Unterstützung {#sustenance}

* Die Aktivitätsprotokolle von Package Manager sollten in einer separaten Protokolldatei extrahiert werden. NPR-27323: Hotfix für Granite-14866
* Es wird ein(e) standardisierte(r) Wortgruppe/Wortlaut/Protokollzeile in error.log angezeigt, wenn die Installation abgeschlossen ist. NPR-27835
* Das Granite-Paket-Plugin übernimmt die Abhängigkeit einer niedrigeren Version von org.apache.sling.i18n. Hotfix für CQ-4263245
* Das com.adobe.cq.com.adobe.cq.ui.commons-Bundle wird bei der Installation des neuesten CFP nach 6.2SP1-CFP15 gelöscht. Hotfix für CQ-4258808

### Formulare {#forms-1}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-1}

#### Adaptive Formulare {#adaptive-forms-1}

* XML-Injection-Schwachstelle mit AEM Forms. NPR-27843: Hotfix für CQ-4257315

### JEE-Installationsprogramm von Forms {#forms-jee-installer-1}

* Keine neuen Fehlerbehebungen im JEE-Installationsprogramm von AEM Forms.

### Enthaltene OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included}

Im folgenden Text wird die Liste der im CFP enthaltenen OSGI-Bundles und Inhaltspakete dokumentiert.

Liste der in AEM 6.2 SP1-CFP19 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/cfp19_osgi_bundles.txt)

Liste der in AEM 6.2 SP1-CFP19 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/cfp19_content_packages.txt)

### Cumulative Fix Pack 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Unterstützung in DAM CommandLineProcess hinzugefügt, um den lang laufenden Prozess zu beenden.
* Sitzungsleck in ReplicationEventListener behoben.
* Unterstützung für Umleitung zur Kernseitenkomponente hinzugefügt.

### Assets {#assets-1}

* `Camera RAW`-Prozesse bleiben während Perioden massiver Aufnahmen hängen und blockieren schließlich die gesamte Workflow-Verarbeitung. NPR-26990: Hotfix für NPR-23860
* Die Download-Funktion verwendet AEM Assets über ein Asset-Download-Servlet, das anonymen Benutzern das Herunterladen aller Assets ermöglicht. NPR-27054: Hotfix für CQ-4254732
* Sonderzeichen werden in der Betreffzeile der E-Mail-Vorlagen in AEM unvollständig angezeigt. NPR-26470: Hotfix für CQ-4252368

### Sites {#sites-1}

* Aufgrund des falschen Verhaltens der ConfigPostProcessor-Klasse wird durch das Aussetzen des übergeordneten Bildes der Mischtyp `cq:LiveRelationship` von der untergeordneten Seite entfernt. NPR-26745: Hotfix für CQ-4254163
* Fügen Sie der Kernseitenkomponente Umleitungs-Unterstützung hinzu. NPR-26576: Hotfix für CQ-110529
* Migrieren von ContextHub zu `jQuery` 3. NPR-26956: Hotfix für CQ-4255472
* Ankereingabefelder erscheinen außerhalb des sichtbaren Bereichs des Browsers im Dialogfeld, bis es maximiert wird. NPR-26852: Hotfix für CQ-4255019
* Einfügen von unerwünschtem Text kopieren &lt;br> im Inhaltsfragment. NPR-26660: Hotfix für CRTE-151
* Der klassische Site-Administrator rendert die Liste für einige Seiten nicht im rechten Bereich. NPR-27247: Hotfix für CQ-4251621
* (Klassische Benutzeroberfläche) Der Versuch, Seiten zu verschieben/umzubenennen, führt zu einem Fehler: „Beim Verschieben der Seite ist ein Fehler aufgetreten.“ NPR-27179: Hotfix für CQ-4235907

### Integration {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever durchsucht den gesamten Baum, um die verfügbaren Marken zu sammeln. NPR-27060: Hotfix für CQ-4255790

### WCM - Foundation-Komponenten {#wcm-foundation-components}

* Problem mit der Suchfunktion bei der Foundation-Listenkomponente. NPR-26817: Hotfix für CQ-4250324

### Plattform {#platform}

* Aufgrund des Sonderzeichen-em-Bindestrichs tritt beim Publisher ein Problem beim Leeren des Caches auf. NPR-27199: Hotfix für CQ-4242790

### Granite {#granite-1}

* Package Validator überprüft keine Pakete, die in CFP/SP enthalten sind. NPR-26775: Hotfix für Granite-22825

### Replikation {#replication}

* JCR-Sitzungsleck in ReplicationListener. NPR-27063: Hotfix für CQ-4232088

### Formulare {#forms-2}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-2}

* Keine neuen Fehlerbehebungen im AEM Forms Add-On-Paket.

### JEE-Installationsprogramm von Forms {#forms-jee-installer-2}

* Keine neuen Fehlerbehebungen im JEE-Installationsprogramm von AEM Forms.

#### Enthaltene OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-1}

Liste der in AEM 6.2 SP1-CFP18 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/62cfp18updated_bundles.txt)

Liste der in AEM 6.2 SP1-CFP18 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Cumulative Fix Pack 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Unterstützung für URLs ohne Site-Erweiterung in at-integration.js hinzugefügt.
* Der S7-Abruf-Importer wurde aus der S7-Cloud-Service-Konfiguration entfernt.
* Änderungen an der Zielgruppenansicht zur Unterstützung der Ordnerstruktur für die Implementierung mit mehreren Mandanten.
* Aktualisierung auf jqueryui clientlib v1.12.1.

### Assets {#assets-2}

* Zum Starten von Workflows über die Asset-Benutzeroberfläche muss der Benutzer über Berechtigungen zum Schreiben/Löschen/Ändern verfügen. NPR-25688: Hotfix für CQ-4250140
* Schaltflächen zum Veröffentlichen und Rückgängigmachen der Veröffentlichung bleiben auch für Benutzer ohne Berechtigung zum Replizieren sichtbar. NPR-25094
* (Workflow) Der Workflow zum intelligenten Taggen von Assets wird nicht über die AEM-Proxy-Konfiguration verarbeitet. NPR-25915: Hotfix für CQ-4248202
* Entfernen des S7-Abruf-Importers aus der S7-Cloud-Service-Konfiguration. NPR-25239: Hotfix für CQ-95236

### Sites {#sites-2}

* Workflows, die über „Editor > Seiteninformationen“ gestartet werden, enthalten den Kontextpfad in der Payload. NPR-26389: Hotfix für CQ-76804
* (Prüfer für externe Links) Ungültige HTTPS-Links werden als gültige Links angezeigt. NPR-25541: Hotfix für CQ-4201333
* (Klassische Benutzeroberfläche) Beim Erstellen einer eigenständigen Seite unter einer Live Copy wird die Seite als Live Copy erstellt. NPR-25610: Hotfix für CQ-4249801
* Probleme mit Veröffentlichungsressourcen, die mit der Design Importer-Komponente verknüpft sind, wenn eine Seite aktiviert wird. NPR-25638: Hotfix für CQ-102532
* Die Symbolleiste des RTE-Rich-Text-Editors umfasst Auswahllisten. NPR-25165: Hotfix für CQ-4248948
* Migrieren von ContextHub zu jQuery 3. NPR-25059: Hotfix für Granite-19902
* Bei verschachtelten Parsys-Komponenten wird immer das erste (mit dem am wenigsten verschachtelten Pfad) passende Design aus mehreren verfügbaren Komponenten angewendet. Weitere Informationen finden Sie unter [Auflösung des Design-Pfads](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-25250: Hotfix für CQ-4246276

### Integration {#integration-3}

* Mithilfe der OOTB Target-Integration rendert die Targeting-Komponente die gesamte Seite anstelle einer leeren Targeting-Komponente. NPR-25273: Hotfix für CQ-4248003
* Wenn Sie im Targeting-Modus die Vererbung aufheben, wird die Komponente weiterhin als zielgerichtet angezeigt, ohne dass die Vererbung im Bearbeitungsmodus aufgehoben wird. NPR-25324: Hotfix für CQ-4248162
* Wenn eine Personalisierung auf einer Seite definiert und eine Zielgruppe aufgelöst wird, wird das entsprechende Erlebnis im Bearbeitungsmodus angezeigt. NPR-25731: Hotfix für CQ-4249465
* Fehlerhafte Teaser-URL bei Verwendung von AEM mit einem nicht standardmäßigen Kontextpfad. NPR-25971: Hotfix für CQ-4250953
* Leeres Rendering bei Verwendung von Opt-out. NPR-25295: Hotfix für CQ-4246792
* Erlebnisse, die aus der Autorenumgebung gelöscht wurden, werden bei der Seitenaktivierung nie von der Veröffentlichungsseite entfernt. NPR-24869: Hotfix für CQ-4247832

### DAM - DM Client {#dam-dm-client}

* (Chrome, Firefox) Video-Player ignoriert Mausklicks auf Touch-fähigen Geräten. Hotfix für CQ-4247370

### Plattform {#platform-1}

* Ermöglichen der Konfiguration der maximalen Anzahl von Wiederholungsversuchen beim Erfassen/Freigeben eines Pakets. NPR-25328: Hotfix für Granite-22376
* Falsche Protokollierung bei Replikationsfehlern. NPR-25308: Hotfix für CQ-4249402
* Die Installation von AEM 6.2 Forms CFP8 bis CFP14 führt zum Fehlschlagen von Apache POI. NPR-25053: Hotfix für Granite-21771

### Granite {#granite-2}

* Der Benutzersynchronisierungsprozess schlägt mit der Ausnahme OakConstraint0022 fehl. NPR-25729: Hotfix für Oak-7428

### Communities {#communities}

* cq-social-as-provider bundle startet nicht mit Mongo Driver 3.x-Versionen. NPR-26271: Hotfix für CQ-4252710

### Benutzeroberfläche - Foundation {#ui-foundation-1}

* Aktualisierung auf jqueryui clientlib v1.12.1. NPR-25090: Hotfix für Granite-21981, CQ-4248897

* (Omnisearch): Die Titeleigenschaft ist für Cross-Site-Scripting (XSS) in Sites anfällig. NPR-24994: Hotfix für Granite-19933

### Formulare {#forms-3}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-3}

#### Adaptive Formulare {#adaptive-forms-2}

* Falsche Kodierung beim Senden von Daten aus dem adaptiven Formular. NPR-25539

#### Forms – Verwaltung {#forms-management}

* Nicht verwandte Formular-Assets werden beim Veröffentlichen der Seite als Verweise gemeldet. NPR-26167: Hotfix für CQ-4251004

### Forms - JEE-Installationsprogramm {#forms-jee-installer-3}

#### Document Security {#document-security}

* Die Variable wird als Datentypliste ausgefüllt, der Untertyp ist eine Zeichenfolge, aber der Fehler &quot;Objekt kann nicht erzwungen werden&quot;tritt auf. NPR-26194: Hotfix für CQ-4252287
* Nach der Installation von 6.2-SP1-CFP15 kann nicht auf Wasserzeichenkonfigurationen zugegriffen werden. NPR-26130: Hotfix für CQ-4250984

### Enthaltene OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-2}

Liste der in AEM 6.2 SP1-CFP17 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/62cfp17updated_bundles.txt)

Liste der in AEM 6.2 SP1-CFP17 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* STARTTLS-Unterstützung im Day CQ Mail Service hinzugefügt.
* Die Ausrichtung der ContextHub-Symbole im Profil-Popup wurde korrigiert.
* Korrekturen in der Funktion zum Einblenden/Ausblenden der Dropdown-Komponente.
* Upgrade auf die neueste Jackson-Version 2.8.11

### Assets {#assets-3}

* Workflow kann nicht von einer Listenansicht aus initiiert werden. NPR-24393: Hotfix für CQ-4245788
* (Firefox/Chrome) Assets können nicht von der Assets Share-Seite heruntergeladen werden. NPR-24523: Hotfix für CQ-4224408
* Die Standardqualität für die Videovorschau in AEM wurde verbessert. NPR-24148: Hotfix für CQ-4244310

### Integration {#integration-4}

* Wenn eine Komponente auf eine Veröffentlichungsinstanz ausgerichtet ist, erscheint ein Flackern, das das Standarderlebnis vor dem zielgerichteten anzeigt. NPR-23992: Hotfix für CQ-4242038
* Erlebnisse, die aus der Autorenumgebung gelöscht wurden, werden bei der Seitenaktivierung nie von der Veröffentlichungsseite entfernt. NPR-24869: Hotfix für CQ-4247832

### Plattform {#platform-2}

* Patch jQuery 1.12.4 von clientlib enthält Sicherheitskorrektur. NPR-24129: Hotfix für Granite-20058
* STARTTLS-Unterstützung im Day CQ Mail Service hinzugefügt. NPR-23941: Hotfix für CQ-4240397
* Entfernen des standardmäßigen MERGE_PRESERVE aclHandling. NPR-24593: Hotfix für Granite-21889
* LineChecker kann Links nicht externalisieren, wenn eine Anfrage ungültige Abfrageparameter enthält. NPR-24127: Hotfix für CQ-4241893

### MSM {#msm}

* Proaktive Hotfixes für Cross-Site Scripting-Angriffe (XSS). NPR-21893: Hotfix für CQ-4223385
* MSM LiveRelationship: Eine effektive RolloutConfig ist falsch, wenn BlueprintConfig auf dem Stamm ist. NPR-23999: Hotfix für CQ-4243000

### Sites {#sites-3}

* Um ein Erlebnis in einem Live Copy-Bereich zu erstellen, muss die Vererbung zunächst unterbrochen werden, damit sie konfiguriert werden kann. NPR-24995: Hotfix für CQ-4248209
* (Touch-optimierte Benutzeroberfläche) Mehrere Symbole in der oberen Symbolleiste verschwinden beim Sperren oder Entsperren einer Seite. NPR-23954: Hotfix für CQ-4243345
* Die Felder sind in ContextHub nicht richtig ausgerichtet. NPR-23958
* Die Publish-Aktion auf der gesperrten Seite unterbricht die Bearbeitung. NPR-23970: Hotfix für CQ-4243203
* OOTB-Berichte in /etc/reports/ funktionieren nicht richtig und zeigen kein Diagramm mit historischen Daten an. NPR-20035: Hotfix für CQ-4220180
* Die Launch-Erstellung schlägt beim Initiieren des Workflows &quot;Launch anfordern&quot;für ein Projekt fehl. NPR-24255: Hotfix für CQ-4245030
* HTML-Tags und Attribute werden von E-Mails nach der CFP10-Installation ignoriert. NPR-24287: Hotfix für CQ-4240028
* Tag-Auswahl: Tag-Vorschlag im Tag-Metadatenschema-Tag-Feld fragt Knoten ab, die mit Tags versehen werden können, und benötigt daher viel Zeit zum Laden. NPR-24347: Hotfix für CQ-4244291
* Die Salesforce-Integration schlägt bei Proxy-Konfigurationen fehl. NPR-24418: Hotfix für CQ-4245300
* (WCM) Page Manager lässt die Seite während der Erstellung der Revision bei einer Ausnahme eingecheckt. NPR-24565: Hotfix für CQ-4246203
* Die Schaltfläche „Geräteemulator“ wird nach dem Anwenden von CFP14 aus dem Bearbeitungs- und Vorschaumodus nicht mehr angezeigt. NPR-24566: Hotfix für CQ-4247060
* (Klassische Benutzeroberfläche) Die gesamten Tags werden nach der Erstellung im Dialogfeld als leer angezeigt. NPR-24688: Hotfix für CQ-4246407
* Beim ersten Versuch kann keine Version erstellt werden. NPR-24774: Hotfix für CQ-4232176
* OOTB-Berichte in /etc/reports/ funktionieren nicht richtig und zeigen kein Diagramm mit historischen Daten an. NPR-24138: Hotfix für CQ-4220180

### Schwachstelle {#vulnerability-1}

* Die Salesforce-Integration ist anfällig für Server-seitige Anforderungsfälschung (SSRF, Server Side Request Forgery). NPR-24289: Hotfix für CQ-4245277
* SSRF-Sicherheitsanfälligkeit (Server Side Request Forgery) in ReportingServicesProxyServlet. NPR-24657: Hotfix für CQ-4246880

### Granite {#granite-3}

* Lesevorgänge für Metadaten werden nicht beendet. NPR-24240: Hotfix für Granite-19866
* Aktualisieren von Jetty auf 9.4.11.20180605, um Sicherheitslücken zu schließen. NPR-25033: Hotfix für Granite-22120

### WCM - Foundation-Komponenten {#wcm-foundation-components-1}

* PageComparator löst beim Sortieren von Seiten eine ClassCastException aus. NPR-24123: Hotfix für CQ-4244048
* Die Funktion zum Einblenden/Ausblenden der Formular-Dropdown-Komponente funktioniert nicht wie erwartet. NPR-24562: Hotfix für CQ-4222853

### Benutzeroberfläche {#user-interface}

* Aufgrund vieler Anforderungen in der Admin-Suchfunktion wird eine hohe CPU-Auslastung beobachtet. NPR-23588: Hotfix für Granite-21286
* (Klassische Benutzeroberfläche) Die Komponente zeigt die Standardwerte an, selbst wenn der zugehörige Formulardatenmodelldienst auf ein leeres Feld eingestellt ist. NPR-21903: Hotfix für GRANITE-19744
* Multifield-Ausgabe von NPE, wenn keine FormData zur Anforderung vorhanden ist. NPR-24513: Hotfix für Granite-21055

## Formulare {#forms-4}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-4}

#### Core {#core}

* (OSGI) AEM Forms-OSGI ist von der Sicherheitswarnung zur Datenbindung von Jackson betroffen. NPR-24274: Hotfix für CQ-4230245

#### Rights Management {#rights-management}

* Apache POI schlägt nach der Installation AEM 6.2 SP1-CFP14 fehl. NPR-25054, NPR-25052: Hotfix für CQ-4245898, CQ-4244778

#### HTML5-Formulare {#html-forms}

* Beim Vorausfüllen von mehrzeiligen Feldern in der HTML-Vorschau werden die Daten nicht aufgefüllt. NPR-23357: Hotfix für CQ-4244212
* Wenn eine Vorschau eines Briefs über eine Standardvorschau angezeigt wird, wird die Zuordnung eines Layoutfragments nicht angezeigt, während dasselbe beim Klicken auf Vorschau korrekt angezeigt wird. NPR-22993: Hotfix für CQ-4237745
* Problem mit der HTML-Vorschau eines Textfelds, wenn ein Muster einer Sozialversicherungsnummer auf eine Vorlage angewendet wird. NPR-23205

#### Adaptive Formulare {#adaptive-forms-3}

* Fehler „Guidelib ist nicht definiert“ beim Hinzufügen eines AEM-Formulars zur Parsys-Komponente. NPR-24269: Hotfix für CQ-4244546

### JEE-Installationsprogramm von Forms {#forms-jee-installer-4}

#### Forms – Installieren von LCM {#forms-install-lcm}

* Windows-Zeilenenden in Shell-Skriptdateien führen dazu, dass LCM unter UNIX® nicht ausgeführt wird. NPR-22958

### Enthaltene OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-3}

Liste der in AEM 6.2 SP1-CFP16 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Liste der in AEM 6.2 SP1-CFP16 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Proaktive Sicherheitskorrekturen in der Foundation-Tabelle zur Gewährleistung der Designkonsistenz.
* Unterstützung für TypeHint zum Speichern von Werten als Zeichenfolge hinzugefügt.
* Bietet erhöhte Sicherheit für den Vorbefüllungs-Service von Forms.
* Aktualisierung auf die neueste Datei adobe-reader-extensions-dsc.jar , um Fehlerbehebungen in der Reader-Erweiterung zu erhalten.
* Der Validierungs-Hook wurde angepasst, um `:invalid`-Elemente für die Eingabe der Boost-Nummer zu berücksichtigen.

### Assets {#assets-4}

* EmbedXMP-Daten werden für den TIFF-Pyramid-Generierungsprozess immer auf &quot;aktiv&quot;gesetzt. NPR-22776: Hotfix für CQ-4234498
* Es können nicht mehrere Standardwerte in Feldern mit mehreren Werten festgelegt werden. NPR-22900: Hotfix für CQ-4239000
* (Dynamic Media) Wenn Sie das Kontrollkästchen &quot;Dynamische Ausgabeformate&quot;aktivieren, gibt die heruntergeladene ZIP-Datei das Originalbild mit der TIFF-Nullbyte-Datei zurück. NPR-22410: Hotfix für CQ-4198471
* (Touch-optimierte Benutzeroberfläche) Standardmäßige Upload-Position für Assets in der Spaltenansicht. NPR-23475: Hotfix für CQ-4237057

### Integration {#integration-5}

* Im Target-Modus können Autorinnen und Autoren eine aus der Blueprint geerbte Komponente ändern, ohne die Vererbung abzubrechen. NPR-22751: Hotfix für CQ-4237907
* Die Pfadvariable ist nicht ordnungsgemäß kodiert, was zu nicht beständigem Cross-Site-Scripting (XSS) führt. NPR-22851

### MSM {#msm-1}

* Wenn beim Rollout einer LiveCopy mit mehreren Rollout-Konfigurationen ein ResourceNameConflict unterhalb des Stammverzeichnisses auftritt, wird der Rollout-Fluss beendet, ohne alle Verzweigungen einzuschließen. NPR-22842: Hotfix für CQ-4236188

### Plattform {#platform-3}

* Implementieren eines Abfragelimits in einer Anfrage für die umgekehrte Anwendung. NPR-23351: Hotfix für Granite-21135****
* Die Änderung des Meldungsmusters wird bei benutzerdefinierten Protokollen nicht berücksichtigt. NPR-23486: Hotfix für CQ-4241974

### Sites {#sites-4}

* Das Erstellen eines Links in einem Text eines Rich-Text-Editors zu einem Dokument mit Leerzeichen oder anderen Sonderzeichen funktioniert nicht. NPR-22289: Hotfix für CQ-4224321
* Wenn Sie das Segment mit einem riesigen Wert speichern (1000000000), wird die Steigerung auf 0 gesetzt, was zu einer Fehlermeldung führt. NPR-22524: Hotfix für CQ-4237006
* In der Mehrfachfeld-Komponente kann nicht auf „Element hinzufügen“ geklickt werden. NPR-22552: Hotfix für CQ-4237404
* Die horizontale Bildlaufleiste ist nicht sichtbar, wenn ein Segment einen langen Titel hat. NPR-22615: Hotfix für CQ-4237001
* Beim Laden einer leeren Zielgruppe wird ein falscher JavaScript-Code generiert. NPR-22974: Hotfix für CQ-4238734
* Beim Planen einer Aktivierung oder Deaktivierung ist der Workflow-Titel obligatorisch. Daher wird der benutzerdefinierte Workflow-Titel nicht in die Zeitleiste übersetzt. NPR-23121: Hotfix für CQ-4237552
* Anfrage zur Behebung von Problemen mit Target-Segmenten in Sites. NPR-23128
* (Firefox) Das Kontrollkästchen für die ausgewählte Rolle ist nicht die richtige. NPR-23345
* Beschriftungen für die verschiedenen Modi werden zusammen mit Symbolen angezeigt. NPR-23275
* Fehler „Invalid Recursion Selector Value“ bei der Migration einer Komponente von AEM 6.0 auf AEM 6.2. NPR-23503: Hotfix für CQ-4241258

### Communities {#communities-1}

* Web- und E-Mail-Benachrichtigungen werden nicht ausgelöst, da die Gruppen nicht benachrichtigt werden. NPR-23447: Hotfix für CQ-4242880

### Übersetzung {#translation-1}

* Asset-Sprachkopien werden erstellt, wenn das Asset &quot;Nicht übersetzen&quot;in der Übersetzungskonfiguration festgelegt ist. NPR-22540: Hotfix für CQ-4237962

### Benutzeroberfläche {#user-interface-1}

* Die Verwendung von Omnisearch mit einer Bindestrich-Abfrage gibt einen Server-Fehler zurück. NPR-22999: Hotfix für Granite-19674
* DatePicker unterstützt nicht das manuelle Festlegen externer Typhinweise, die von einem ausgeblendeten Feld festgelegt werden. Beim Ändern des Typhinweises wird ein Konvertierungsfehler ausgegeben. NPR-23333: Hotfix für Granite-21194

### WCM - Foundation-Komponenten {#wcm-foundation-components-2}

* Die CAPTCHA-Komponente wird jetzt aus Gründen der besseren Sicherheit nicht mehr unterstützt. Wenn Sie die CAPTCHA-Komponente verwenden, wird nach der Installation von 6.2 SP2-CFP15 oder höher die Meldung &quot;Captcha component is deprecated and should not be used&quot;angezeigt. Die AEM-Komponente kann angepasst werden, um reCAPTCHA für mehr Sicherheit einzubeziehen. NPR-22151: Hotfix für CQ-4220052
* Die WCM Foundation-Komponente „Tabelle“ ist anfällig für beständiges Cross-Site-Scripting. NPR-23206: Hotfix für CQ-4240760

### Schwachstelle {#vulnerability-2}

* Cross-Site-Scripting (XSS) in Verknüpfungen zum Admin-UI-Projekt. NPR-23272: Hotfix für CQ-4241795

## Formulare {#forms-5}

### Forms-Add-on-Paket {#forms-add-on-package-5}

#### Korrespondenzverwaltung {#correspondence-management}

* Wenn eine Vorschau eines Briefs über eine Standardvorschau angezeigt wird, wird die Zuordnung eines Layoutfragments nicht angezeigt, während dasselbe beim Klicken auf die Schaltfläche Vorschau korrekt angezeigt wird. NPR-23335: Hotfix für CQ-4237745
* Daten im Brief, die Bindungen entsprechen, die in XDP definiert sind, werden nicht über die Brief-URL gefüllt. NPR-24145: Hotfix für CQ-4244290

#### Mobile Forms {#mobile-forms}

* (Korrespondenzverwaltung) Datenversatz beim Laden des Briefes mit Ziel-XML. NPR-22993: Hotfix für CQ-4237663

#### Reader Extensions-Service {#reader-extensions-service}

* Reader Extension kann nicht auf Adobe PDF angewendet werden. NPR-23067

#### Forms Manager {#forms-manager}

* Forms, die in die Site eingebettet sind, werden beim erneuten Veröffentlichen der Site-Seite nicht veröffentlicht. NPR-23014: Hotfix für CQ-4236566

#### Schwachstelle {#vulnerability-3}

* Proaktive Hotfixes für siteübergreifendes Skripting. NPR-20624: Hotfix für CQ-4206055
* Sicherheitslücke bei Cross-Site Scripting (XSS) auf der Registerkarte &quot;Notizen&quot;von Forms Manager gespeichert. NPR-27157: Hotfix für CQ-4255556

#### Encryption-Service {#encryption-service}

* (OSGI) [JEE] Falscher Signaturstatus für PDF mit Anhang bei der Überprüfung mit &quot;PDF überprüfen&quot;. NPR-23269, NPR-23737

### JEE-Installationsprogramm von Forms {#forms-jee-installer-5}

#### Core {#core-1}

* Die in der statischen Code-Analyse von Core-ext gemeldeten Probleme sollten behoben sein. NPR-13947

#### PDFG Service {#pdfg-service}

* Konverter „HTML in PDF“ funktioniert nicht. NPR-21545

### Enthaltene OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-4}

Im folgenden Text wird die Liste der im CFP enthaltenen OSGI-Bundles und Inhaltspakete dokumentiert.

Liste der in AEM 6.2 SP1-CFP15 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Liste der in AEM 6.2 SP1-CFP15 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Cumulative Fix Pack 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Verbesserte Editierbarkeit der Metadateneigenschaften von Assets.
* Der Vorgang zur Benachrichtigung über ein abgelaufenes Kennwort wurde für Assets neu konfiguriert, die sich bereits im abgelaufenen Zustand befinden.
* Touch-optimierte Benutzeroberflächenkonsole angepasst und durch zusätzliche Gebietsschemata erweitert.
* Aktualisierung von cq-msm-core für eine effiziente Livecopyindex-Synchronisierung.
* Optimierte Replikationsfunktionen für verschiedene Rollouts.

### Assets {#assets-5}

* Benutzer können keine Assets mit Haftungsausschluss und langen Dateinamen herunterladen. NPR-22163: Hotfix für CQ-4235274
* Ein einfaches Anführungszeichen verhindert, dass die Metadaten in der Massenansicht aktualisiert werden und die Benutzeroberfläche beim Öffnen der Eigenschaften eines Assets mithilfe der Schnellaktionen in der Symbolleiste beschädigt wird. NPR-22317, NPR-22353: Hotfix für CQ-4236990, CQ-4236469
* Der Vorgang &quot;Asset-Ablaufbenachrichtigung&quot;deaktiviert die abgelaufenen Assets nicht. NPR-22346: Hotfix für CQ-4237188
* Asset-Download schlägt fehl, wenn Digital Rights Management in Assets in Safari verwendet wird. NPR-22378: Hotfix für CQ-4236460
* Die Web-Ausgabedarstellung für kleine Bilder weist eine ungenaue Pixelgröße auf. NPR-22435: Hotfix für CQ-4236742

### Sites {#sites-5}

* (Touch-optimierte Benutzeroberfläche) Ein verschobenes Tag wird in den Seiteneigenschaften an alten und neuen Positionen angezeigt. NPR-21921: Hotfix für CQ-4238598
* (Touch-optimierte Benutzeroberfläche) Rich-Text-Editor entfernt alle Attribute außer ID aus dem &lt;a>-Tag. NPR-22045: Hotfix für CQ-4234133
* Beim direkten Einfügen von Inhalten in den Rich-Text-Editor mit Strg+V werden die Zeilenumbrüche übersprungen. NPR-22117: Hotfix für CUI-5881
* (Touch-Benutzeroberfläche) Es können nicht mehr als 40 Tags unter einem Namespace angezeigt werden. NPR-22290: Hotfix für CQ-99114
* RSS-Feed-Probleme, Port -1 zu AEM 6.2. NPR-22158: Hotfix für CQ-4233339
* (IE) Beim erstmaligen Verfassen eines Zeichens im Feld Rich-Text wird dem Zeichen ein nachstehendes Leerzeichen hinzugefügt. NPR-22443: Hotfix für CQ-4235343
* Beim Versuch, den Paketnamen abzugleichen, friert das Java™ Use-Objekt den SightlyJavaCompilerService aufgrund eines nachgestellten Leerzeichen in der Paketdeklaration ein. NPR-22557: Hotfix für Granite-20836
* Die Touch-optimierte Benutzeroberflächenkonsole erfasst keine neuen Sprachen für das Tagging. NPR-22250: Hotfix für CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Sowohl das Veröffentlichungsdatum als auch das Deckungsdatum sind erforderliche Felder für Folios, bevor sie in DPS hochgeladen werden. NPR-22484

### Commerce {#commerce}

* Mehrere Schwachstellen bei Site-übergreifendem Scripting (XSS) im Commerce - Assistenten zum Erstellen eines Katalogs . NPR-22344: Hotfix für CQ-4237017

### MSM {#msm-2}

* Die LiveCopyIndex-Synchronisierung führt bei langen Indexaktualisierungen zu einer Überlastung der Threads. NPR-22214: Hotfix für CQ-90667
* `cq:cugEnabled`-Eigenschaft ist deaktiviert, wenn ein anderes Feld in einer Live Copy bearbeitet wird, wodurch die Seite ungeschützt wird. NPR-22246: Hotfix für CQ-4236050
* Die Aktion „Seiten-Rollout“ kann untergeordnete Elemente nicht aktualisieren, wenn eine Seite ausgesetzt wird. NPR-22483: Hotfix für CQ-4236956
* Rollout einer Struktur, die in einer primären Ursache verschoben wurde, um einen falschen Wert zu erzielen `cq:moveTarget`. NPR-22373: Hotfix für CQ-4232536

### Integration {#integration-6}

* Der Versuch, Angebote in der Angebotsauswahlbibliothek zu sortieren, führt zu einem fehlerhaften Verhalten. NPR-22208: Hotfix für CQ-4235439
* TargetContentImpl verlangsamt AEM bei langwierigen Abfragen. NPR-22361: Hotfix für CQ-4236907
* Die Target-Engine (mbox.js, at.js) verwendet keine verwalteten URLs und URLs, die Doppelpunkte enthalten, die bei bestimmten Implementierungen fehlschlagen könnten. NPR-22366: Hotfix für CQ-4237854
* Die Seitenpersonalisierung erfordert die Veröffentlichung direkt auf dem Markenknoten. NPR-22370: Hotfix für CQ-4236895

### Foundation {#foundation}

* Apache Sling Scripting Sightly-Modelle verwenden Anbieter-Bundle **org.apache.sling.scripting.siwelly.models.provider/1.0.18**. NPR-22614: Hotfix für Sling-5944, Sling-6866

### Projekte {#projects}

* Workflow Starter kann den TypeHint -Wert von String nicht akzeptieren. NPR-22436: Hotfix für CQ-4237855

### Übersetzung {#translation-2}

* Untersuchen von Problemen mit der Vorschaufunktion. NPR-22201: Hotfix für CQ-4223753

### Benutzeroberfläche {#user-interface-2}

* (Klassische Benutzeroberfläche) Die Komponente zeigt die Standardwerte an, selbst wenn der zugehörige Formulardatenmodelldienst auf ein leeres Feld eingestellt ist. NPR-21903: Hotfix für GRANITE-19744

### WCM - Foundation-Komponenten {#wcm-foundation-components-3}

* Fehler beim Veröffentlichen einer Live Copy-Seite, die auf eine Importer-Seite in Adobe Campaign verweist. NPR-22470: Hotfix für CQ-4237164
* JavaScript-Fehler beim Öffnen des Editors für Experience Fragments. NPR-22598: Hotfix für CQ-4238415

### Workflow {#workflow}

* Der E-Mail-Benachrichtigungs-Service des Day CQ-Workflows löst eine E-Mail pro Mongo-Knoten für WorkflowCompleted- und WorkflowAborted-Benachrichtigungen aus. NPR-22486: Hotfix für CQ-4238172

## Formulare {#forms-6}

### Forms-Add-on-Paket {#forms-add-on-package-6}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

#### Adaptive Formulare {#adaptive-forms-4}

* Inkonsistenz des Dropdown-Platzhalterwerts im adaptiven Formular in IE11 und Chrome. NPR-22405: Hotfix für CQ-4227096

### JEE-Installationsprogramm von Forms {#forms-jee-installer-6}

#### Installieren von LCM {#install-lcm}

* Aktualisieren von Jsafe Jars auf Cryptoj 6.1.3.1 im Installationsprogramm und LCM. NPR-22744

### Enthaltene Feature Packs {#feature-packs-included}

#### Prozessverwaltung {#process-management}

* (HTML Workspace) Wenn ein Benutzer eine Aufgabe anfordert, wird die Anzahl der Warteschlangen nur für diesen bestimmten Benutzer aktualisiert. Das heißt, es sei denn, die Seite wird aktualisiert. NPR-19778: Hotfix für CQ-4233665

### In CFP14 enthaltende OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-in-cfp}

Liste der in AEM 6.2 SP1-CFP14 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Liste der in AEM 6.2 SP1-CFP14 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
AEM Cumulative Fix Pack 6.2 SP1-CFP13 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Aktivierung der Konfiguration von statischen Parameterfeldern in den Target-Komponenteneinstellungen bei Verwendung von AT.js als Client-Bibliothek.
* Korrekturen in der Funktion zum Einblenden/Ausblenden der Dropdown-Komponente.
* Fehlerbehebungen bei der Verwendung von Zielen zum Synchronisieren von Zielgruppen.
* Die Vielseitigkeit der Korrespondenzverwaltung wurde verbessert, sodass Sonderzeichen berücksichtigt werden.

### Assets {#assets-6}

* Bei der Versionsbereinigung werden alte Versionen von Assets nicht entfernt. NPR-21682: Hotfix für CQ-4212996
* Die Neuanordnung von Ordnern mit einem neu zu sortierenden Ordner wird nicht beibehalten. NPR-21964: Hotfix für CQ-4231761

### Sites {#sites-6}

* (Touch-optimierte Benutzeroberfläche)(Klassische Benutzeroberfläche) Mehrere Cross-Site-Scripting (XSS)-Sicherheitslücken in HTL- und Kernkomponenten. NPR-21532: Hotfix für CQ-4232305 und CQ-4232511
* Das Erstellen/Formatieren von Inhalten (z. B. Zuweisen/Entfernen neuer Listenstile) in einem ausgewählten Text funktioniert in Internet Explorer 11 nicht einwandfrei. NPR-21533: Hotfix für CQ-4230689
* (Safari) Benutzer können nicht alle Assets im Asset Finder-Bedienfeld anzeigen. NPR-21981: Hotfix für CQ-4213720
* Timewarp gibt den Fehler &quot;RecursionTooDeepException&quot;mit einer durcheinandergewürfelten Seite zurück und es wird keine neue Version erstellt, selbst wenn das Datum geändert wird. NPR-21707: Hotfix für CQ-4199536
* Beim Laden einer Seite im Editor wird der WorkflowStatusProvider (pageinfo.json) dreimal geladen, wodurch die AEM Instanz langsam ausgeführt wird. NPR-21778: Hotfix für CQ-59232

### Integration {#integration-7}

* Die Erstellung von Zielgruppen für Mobilgeräte und Browser im Authoring-Modus „Target“ funktioniert in AEM nicht. NPR-21676, NPR-21681: Hotfix für CQ-4232100
* Bei hoher Latenz während einer Aktualisierung einer Zielkomponente kann ein weiteres Angebot hinzugefügt werden, bevor die Komponente vollständig aktualisiert wird. NPR-21744: Hotfix für CQ-4233158/CQ-4234293
* Benutzer können keine statischen Parameterwerte im Mbox-Aufruf sehen, die beim Testen mit AT.js als Client-Bibliothek in der Cloud-Konfiguration angezeigt werden. NPR-21930: Hotfix für CQ-4234520

### Plattform {#platform-4}

* Leistungsprobleme bei der Benutzersynchronisierung bei einer großen Anzahl von Benutzern oder Gruppen. NPR-20431: Hotfix für CQ-4223282
* Benutzer können nicht mit der Benutzersynchronisierung mithilfe von Sling Distribution synchronisieren. NPR-21911: Hotfix für Granite-20404
* Verhindern, dass Stoppwörter in Suchauszügen (auf einer Geometrixx-Seite) hervorgehoben werden. NPR-21835: Hotfix für Granite-21067 
Hinweis: Für diese Fehlerbehebung ist Oak CFP 1.4.20 oder höher erforderlich.

### Übersetzung {#translation-3}

* Die Eigenschaft jcr fehlt für die Benutzer-ID des Initiators beim Erstellen eines Übersetzungsprojekts. NPR-21715: Hotfix für CQ-4230713

### WCM - Foundation-Komponenten {#wcm-foundation-components-4}

* Die Funktion zum Einblenden/Ausblenden der Formular-Dropdown-Komponente funktioniert nicht wie erwartet. NPR-22164: Hotfix für CQ-4235288

## Formulare {#forms-7}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

### Forms-Add-on-Paket {#forms-add-on-package-7}

#### Adaptive Formulare {#adaptive-forms-5}

* XML External Entity (XXE)-Injektion in adaptiven Formularen. NPR-21982: Hotfix für CQ-109878
* (iOS11) Wenn auf eine Dateianhangskomponente geklickt wird, öffnet der Dateianhang die Kamera statt den Datei-Browser des Geräts. NPR-21926: Hotfix für CQ-4214348
* Fehlender Titel in der Benutzeroberfläche für die Design-Erstellung verursacht eine Ausnahme und ein fehlerhaftes Rendern des Dialogfelds. Hotfix für CQ-4236143

#### Korrespondenzverwaltung {#correspondence-management-1}

* Rendering-Probleme bei XML-Daten, die Sonderzeichen enthalten. NPR-21712: Hotfix für CQ-4229137

### JEE-Installationsprogramm von Forms {#forms-jee-installer-7}

#### Assembler-Service {#assembler-service}

* Die mit `6.2.0-ASM-1017-003` erzeugte PDF-Datei ist defekt. NPR-21427: Hotfix für CQ-4228046

#### PDFG Service {#pdfg-service-1}

* OCR-Fehler aufgrund unerwarteter Seitengröße (PDF) aus PNG-, JPEG- und TIFF-Dateien. NPR-19489: Hotfix für CQ-4209079

## In CFP13 enthaltende OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-in-cfp-1}

Liste der in AEM 6.2 SP1-CFP13 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Liste der in AEM 6.2 SP1-CFP13 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Verbesserte Verarbeitung von Metadaten für Felder mit mehreren Werten.
* Unterstützung von mehrstelligen (mehr als zwei Stellen) Länder-Codes in Übersetzungs-Workflows.
* Verbessertes Rendering von Seiten mit mehreren verschachtelten Komponenten.
* Verbesserte Synchronisierung der Veröffentlichungsdaten für Assets zwischen AEM und Adobe Digital Publishing Suite.

### Assets {#assets-7}

* Zu viele Zeichen in OmniSearch können zum Absturz des AEM-Servers führen. NPR-21083: Hotfix für CQ-4223602
* Werte, die in der zweiten Option in einem Feld mit mehreren Werten im Metadatenschema angegeben sind, werden nicht an die zuvor in CRX-de angegebenen Werte angehängt. NPR-21220: Hotfix für CQ-4224526
* Asset-Download schlägt fehl, wenn Digital Rights Management in Assets in Safari verwendet wird. NPR-21387: Hotfix für CQ-4230287

### Sites {#sites-7}

* (DAM) (Klassische Benutzeroberfläche) Mehrere XSS-Sicherheitslücken (Cross-Site Scripting) in einigen SWF-Dateien im AEM CQ Author/Publish-Schnellstart. NPR-21073, NPR-21074: Hotfix für NPR-20612
* Die Tag-Auswahl übersetzt keine Tags, die in mehreren Sprachen verfügbar sind. NPR-21221: Hotfix für CQ-78855
* Rendering-Probleme mit der AEM-Artikelkonsole, da die Verwendung mehrerer verschachtelter Komponenten sie träge macht. NPR-21271: Hotfix für CQ-4224158

### Integration {#integration-8}

* Beim Hinzufügen eines Target-Frameworks ist der Targeting-Modus nicht in der Liste Select mode im Editor verfügbar. NPR-21047

### Mobile On-Demand {#mobile-on-demand-1}

* (Digital Publishing Suite) Die Veröffentlichungsdaten für Folios in AEM entsprechen nicht den Datumsangaben, die in Folio Producer angezeigt werden. NPR-21145

### MSM {#msm-3}

* Der Prozess zum Zurücksetzen der Live Copy wird nach dem Löschen der ersten lokalen Seite im LC angehalten. NPR-21276: Hotfix für CQ-4229743

### Plattform {#platform-5}

* Benutzerdefinierte Tag-Lib, die als Skript implementierte Referenztags enthält, werden nach der Aktualisierung auf AEM 6.3 nicht gefunden. NPR-20149: Hotfix für Granite-18433

### Übersetzung {#translation-4}

* Übersetzungsworkflows schlagen mit lang_country-Codes fehl, die länger als zwei Zeichen sind. NPR-21088: Hotfix für CQ-4197439
* Übertragen Sie eine Asset-Seite erst wieder an ein Übersetzungsprojekt, wenn das Projekt abgeschlossen ist. NPR-21219: Hotfix für CQ-4209908

### Benutzeroberfläche {#user-interface-3}

* Die Komponente &quot;Auswählen&quot;löscht die Ziel-Eigenschaft nicht während der Formularübermittlung. NPR-21163: Hotfix für GRANITE-14125
* HTTP.encodePathOfURI erweitert doppelte Kodierung des Pluszeichens &#39;+&#39;. NPR-21417: Hotfix für GRANITE-16340

### Schwachstelle {#vulnerability-4}

* Site-übergreifende Skripterstellung (XSS) im DAM-Metadateneditor. NPR-21434: Hotfix für CQ-83472
* Mehrere SWF-Dateien sind anfällig für Cross-Site-Scripting (XSS). NPR-20612: Hotfix für CQ-4213297

## Formulare {#forms-8}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

### Forms-Add-on-Paket {#forms-add-on-package-8}

#### Korrespondenzverwaltung {#correspondence-management-2}

* (IE11) Das anfängliche Rendering des HTML-Inhalts erfolgt nur auf der linken Seite, während die rechte Seite nach dem Laden der vollständigen Benutzeroberfläche gelegentlich geladen wird. NPR-21554
* Die Senden-Schaltfläche für die Briefvorschau wird nach der Installation von AEM 6.2 SP1-CFP9 deaktiviert. NPR-21547
* Wenn Sie den Asset-Verknüpfungstyp auswählen, wird das Fenster &quot;Asset-Auswahl&quot;nicht im Assistenten &quot;Briefdatenbindung bearbeiten&quot;geöffnet. NPR-21164: Hotfix für CQ-4194567
* Um einen Inline- oder bearbeitbaren Textbaustein zu bearbeiten, tippen Sie auf das relevante Symbol zum Bearbeiten oder doppelklicken Sie auf den relevanten Textbaustein in der Briefvorschau. NPR-21402

#### Adaptive Formulare {#adaptive-forms-6}

* Die Komponente für die Senden-Schaltfläche in AEM Forms zeigt „type=&quot;button&quot;“ anstelle von „type=&quot;submit&quot;“ an. NPR-21007
* Beim Hinzufügen oder Löschen neuer Bedienfelder für wiederholbare Bedienfelder bleiben die Daten erhalten. NPR-21408

### JEE-Installationsprogramm von Forms {#forms-jee-installer-8}

#### Core {#core-2}

* Bei der Aktualisierung auf das neueste Java™ 8 Update 131 wird eine Ausnahme ausgegeben: &quot;JsafeJCE Provider ist deaktiviert, eine für FIPS 140 erforderliche Prüfung der Selbstintegrität ist fehlgeschlagen.&quot; NPR-21355

**Hinweis:** Diese NPR erfordert mehr Einstellungen. Siehe [Neueste Java™ 8-Aktualisierung](#latest-java-update-throws-an-exception-npr).

* Die Jsafe-JAR-Dateien wurden auf CryptoJ 6.1.3.1 in Core, Encryption, Signature &amp; Document Security aktualisiert. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Installieren von LCM {#install-lcm-1}

* Aktualisieren Sie Jsafe Jars auf Cryptoj 6.1.3.1 im Installationsprogramm und LCM. NPR-21362

#### PDFG Service {#pdfg-service-2}

* Aktualisieren Sie Jsafe Jars auf Cryptoj 6.1.3.1 in PDFG. NPR-21359

#### Prozessverwaltung {#process-management-1}

* (HTML Workspace) Aktivieren der Spaltengrößenanpassung, damit die Namenskategorie nicht abgeschnitten erscheint. NPR-19770: Hotfix für CQ-4233668

#### Reader Extensions-Service {#reader-extensions-service-1}

* Die Jsafe Jars wurden in RE auf CryptoJ 6.1.3.1 aktualisiert. NPR-21357

## In CFP12.1 enthaltende OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-in-cfp-2}

Liste der in AEM 6.2 SP1-CFP12.1 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Liste der in AEM 6.2 SP1-CFP12.1 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Aktualisierung von cq-msm-core für eine effiziente Livecopyindex-Synchronisierung.
* Verbesserte Bearbeitungseffizienz für Inhaltsfragmente.
* Es bietet eine Validierungsoption im Package Manager zum Erkennen von ACL-Berechtigungen.
* Einführung der Möglichkeit, in Campaign die E-Mail-ID für die Kundenkorrespondenz anzugeben.
* Verbesserte Videokodierungsfunktionen für Dynamic Media-Dateien.
* Fehlerbehebungen in der Sightly-Komponente und in LiveCopies.

### Assets {#assets-8}

* Die Dynamic Media-Videokodierung schlägt bei Dateien fehl, die Leerzeichen in ihren Namen enthalten. NPR-20818: Hotfix für CQ-102469
* Mehrere XSS-Sicherheitslücken (Cross-Site Scripting) in einigen SWF-Dateien im AEM CQ Author/Publish-Schnellstart. NPR-21071, NPR-21072
* Benutzer können keine Assets mit Haftungsausschluss und langen Dateinamen herunterladen. NPR-20255: Hotfix für CQ-4222139

### Sites {#sites-8}

* AEM- und Campaign-Integration: Spezielle Links werden in Adobe Campaign umgeschrieben, so dass Kunden keine mailto:-Hyperlinks in ihren E-Mails senden können. NPR-20787: Hotfix für CQ-4225760
* (Touch-optimierte Benutzeroberfläche) Probleme mit der Benutzerfreundlichkeit und Leistung von AEM, wenn die Sprache auf Französisch eingestellt ist. NPR-20854: Hotfix für CQ-4227628
* Wenn Sie eine kodierte Asset-Datei mit einem Link-Plug-in im RTE verknüpfen, wird ein leerer Link zurückgegeben. NPR-20626, NPR-21059: Hotfix für CQ-4223011
* Der Metadaten-Editor für Inhaltsfragmente verhindert, dass Inhaltsautoren Änderungen an Inhaltsfragmenten speichern. NPR-20641: Hotfix für CQ-4224755
* Der Alias für die Seiteneigenschaft führt zu „Veröffentlichung anfordern“/„Veröffentlichung aufheben anfordern“. NPR-20731: Hotfix für CQ-4226227
* Probleme mit Textkomponenten bei der Codierung der Verknüpfung im RTE-Element. NPR-20755: Hotfix für CQ-4224321

### Plattform {#platform-6}

* ResourceResolverImpl.map() ruft ResourceDecorator nicht auf. NPR-20788: Hotfix für GRANITE-19718
* `org.apache.sling.i18n.DefaultLocaleResolver` kann keine Anforderungen über org.apache.sling.engine.SlingRequestProcessor verarbeiten. NPR-20706: Hotfix für CQ-94880
* Anforderung des Hinzufügens einer Überprüfungsoption in Package Manager, um festzustellen, ob ACL-Berechtigungen/-Rechte für ein bestimmtes Paket geändert wurden. Hotfix für CQ-4229196

### Workflow {#workflow-1}

* Stabilitätsprobleme bei der Bereitstellung des AEM-Produktions-Servers. NPR-20979: Hotfix für Granite-19104

### Projekte {#projects-1}

* (Touch-optimierte Benutzeroberfläche) Einem Projekt können keine Team-Mitglieder hinzugefügt werden. NPR-20990: Hotfix für CQ-4205375

### WCM – Foundation-Komponenten {#wcm-foundation-components-5}

* Sightly Image component &#39;link to&#39; generiert einen 403-Fehler aufgrund der fehlenden .html-Erweiterung. NPR-20823: Hotfix für CQ-4195909
* Auf einer Blueprint-Site mit Live Copy löscht der Versuch, eine Formularkomponente zu löschen, eine NullPointerException und fügt die Formularkomponente wieder ein, anstatt sie zu löschen. NPR-20855: Hotfix für CQ-4204628
* Die LiveCopyIndex-Synchronisierung führt bei langen Indexaktualisierungen zu einer Überlastung der Threads. NPR-20634: Hotfix für CQ-90667

### Sicherheit {#security}

* Proaktive XSS-Bibliotheksaktualisierung. NPR-21174
* Aktualisieren Sie auf Apache Commons Email 1.5, das eine vereinfachte API zum Senden von E-Mails enthält. NPR-20509: Hotfix für Granite-18240
* Sicherheits-Patch auf die Apache Sling XSS Protection-API angewendet, um die Möglichkeit der XSS-Umgehung auszuschließen. NPR-21290: Hotfix für GRANITE-19924
* XSS-Umgehung in der XSSAPI#getValidHref-Funktion. NPR-21174: Hotfix für Granite-19924

### Mobile Apps {#mobile-apps}

* Es wurden Probleme mit Curl Head-Anforderungen für OOTB-Assets in AEM behoben. NPR-20511: Hotfix für CQ-4221520 und CQ-103024

## Formulare {#forms-9}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

Die wichtigsten Merkmale von AEM Forms sind:

* Zertifikatsauthentifizierung für Workbench-Benutzer aktiviert.
* Korrekturen an der Benutzerfreundlichkeit für die Korrespondenzverwaltung, HTML5-Formulare und den AEM Forms-Workspace.

### Forms-Add-on-Paket {#forms-add-on-package-9}

#### HTML5-Formulare {#html-forms-1}

* Probleme mit der Benutzerfreundlichkeit bei der Scribble-Komponente für Geräte mit iOS 10 und 11. NPR-21092

#### Korrespondenzverwaltung {#correspondence-management-3}

* (Correspondence UI) Deaktivieren Sie die Senden-Schaltfläche nach einem Klick. NPR-21078

### JEE-Installationsprogramm von Forms {#forms-jee-installer-9}

#### Assembler-Service {#assembler-service-1}

* docConvertor erzeugt keine PDF/A mit der Fehlermeldung &quot;Das Präfix &quot;stEvent&quot;für Element `stEvt:action` ist nicht gebunden.&quot; NPR-21032: Hotfix für CQ-4222540
* Beim Aufrufen des Dienstes „OMPFSubmission/PDFA/PDFtoPDFA“ wird eine Ausnahme mit dem Namen `java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE` ausgelöst. Diese Ausnahme verhindert, dass der kurzlebige Signaturüberprüfungsprozess abgeschlossen wird, bis der Server neu gestartet wird. NPR-20792

#### Workbench {#workbench}

* Zertifikatsauthentifizierung für Workbench-Benutzer aktivieren. NPR-17548: Hotfix für CQ-4214486

#### Prozessverwaltung {#process-management-2}

* Der Prepare Data Process ruft mehrmals auf, wenn ein mobiles Formular mit Datenfeldern-Parametern wiedergegeben wird. NPR-19801: Hotfix für CQ-4230427: CQ-4230400

## In CFP11 enthaltende OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-in-cfp-3}

Liste der in AEM 6.2 SP1-CFP11 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Liste der in AEM 6.2 SP1-CFP11 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Es wurde die Dienstprogrammfunktion „onDialogLoaded“ für Tests hinzugefügt.
* Tests und Konfigurationen der Frontend-Einheiten wurden zu ClientLibraryProxyServlet hinzugefügt.
* Leistungsverbesserungen in der integrierten Editor-Komponente für mehrere Bilder.
* Konfigurationsaktualisierungen in Apache Sling JCR ResourceBundleProvider.

### Assets {#assets-9}

* Die Asset-Vorschau funktioniert nicht, wenn die Workflows für die Asset-Aktualisierung deaktiviert sind. NPR-20543: Hotfix für CQ-4204986
* Rendering-Probleme mit der in Granite hinzugefügten Klasse: Klasseneigenschaft (cq-damadmin-admin-assets-upload). NPR-20514: Hotfix für CQ-4219238
* Miniatur-Assets mit Sonderzeichen im Titel zeigen Java™-Objekt im alt-Attribut von NPR-20347: Hotfix für CQ-4223620
* Ersetzen des Codes für den Versionsvergleich durch Adobe-eigenen Code aufgrund von Lizenzproblemen. NPR-20273: Hotfix für CQ-4223758
* Verarbeitungsfehler beim Hochladen von CMYK PSB-Dateien mit mehreren Alpha-Ebenen. NPR-20251: Hotfix für CQ-4220869
* Internationalisierungswörterbücher funktionieren, wenn der Server in org.apache.sling.i18n 2.5.6 neu gestartet wird. NPR-20525: Hotfix für Granite - 19490
* Es werden keine Thread-Sicherheitskopien gemäß der Planung mit der standardmäßigen Thread Dump Collector-Konfiguration (Standard AEM Start-up) generiert. NPR-20288: Hotfix für GRANITE-19488/GRANITE-12741 CQ-90647.

### Sites {#sites-9}

* Wenn der geänderte Datumsfilter nach dem Öffnen der gespeicherten Suche geändert wird, hat dies keine Auswirkungen auf die Ergebnisse. Die angezeigten Ergebnisse sind mit dem zuvor gespeicherten Wert des geänderten Datumsfilters identisch. NPR-19739: Hotfix für CQ-4219425
* Seiten mit verschachtelten Komponenten konnten nicht geladen werden. NPR-20312
* Der Workflow für Löschanfragen wird beim Löschen von Workflow-Paketen ausgelöst. NPR-20266: Hotfix für CQ-4221686
* (Touch-optimierte Benutzeroberfläche) Problem beim Kopieren/Einfügen mit der Zwischenablage des Betriebssystems und der internen AEM-Zwischenablage. NPR-20228: Hotfix für CQ-4220383
* Die AEM-Instanz wird in der Listenansicht träge, wenn mehrere Assets (mehr als 100) geladen werden. NPR-20034: Hotfix für CQ-4222695
* (Touch-Benutzeroberfläche) Durch das Löschen von Launches über die Konsole &quot;Klassische Benutzeroberfläche&quot;können alle Seiten nicht bearbeitet werden. NPR-20520: Hotfix für CQ-4225074
* Das Dropdown-Menü „Zielgruppe“ funktioniert nicht mit mehreren RTE-Komponenten in einem Dialogfeld. NPR-20345: Hotfix für CQ-4220981

### Plattform {#platform-7}

* Beim Zugriff über eine anonyme Sitzung proxyliert ClientLibraryProxyServlet nicht die Anforderungen an Client-Bibliotheken auf der veröffentlichten Instanz und gibt den Fehler HTTP 404 not found aus. NPR-20195: Hotfix für Granite-14409

### Integration {#integration-10}

* Wenn Sie die Ziel-Engine als Adobe Target auswählen, wird verhindert, dass die Komponente geladen wird, und es wird ein Fehler im Serverprotokoll ausgegeben. NPR-20058: Hotfix für CQ-88071, CQ-109698, CQ-4201600

### Commerce {#commerce-1}

* Beim Erstellen von Produkten aus derselben Seite wird keine Bestätigungs- oder Umleitungs-Popup-Meldung angezeigt. NPR-20257: Hotfix für CQ-4223414

### Benutzeroberfläche {#user-interface-4}

* Wenn die Datumsauswahl ein Feld in einem Mehrfachfeld ist, werden die in Datumsfeldern gespeicherten Werte beim Bearbeiten der Komponente nicht beibehalten. NPR-20077: Hotfix für GRANITE-19147
* Vorherige Abfragen werden nicht abgebrochen, wenn aufeinanderfolgende Abfragen ausgelöst werden, die zu falschen Ergebnissen führen. NPR-20397: Hotfix für GRANITE-19306

### WCM - Foundation-Komponenten {#wcm-foundation-components-6}

* Die ImageMap-Eigenschaft ist auch nach dem Entfernen der Bilder aus der Editorkomponente &quot;Mehrfach-Bild im Kontext&quot;weiterhin vorhanden. NPR-20142: Hotfix für CQ-4222982

## Formulare {#forms-10}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

### Forms-Add-on-Paket {#forms-add-on-package-10}

#### Adaptive Formulare {#adaptive-forms-7}

* valueCommit-Skript wird für DropDownList zweimal ausgeführt, wenn es über die Benutzeroberfläche geändert wird. NPR-19989: Hotfix für CQ-110212

### JEE-Installationsprogramm von Forms {#forms-jee-installer-10}

**Prozessverwaltung**

* Das CFP-Paket enthält AEM Forms HTML Workspace Version 2.2.26. NPR-20099
* Das vorausgefüllte Formular funktioniert nicht, wenn das Formular für Mobilgeräte so konfiguriert ist, dass es als PDF angezeigt wird. NPR-20566

**Rights Management**

* Das Dialogfeld zur Zertifikatauswahl für CAC/Mutual Authentication sollte Zertifikate mit erweiterter Schlüsselverwendung (EKU) als Client-Autoren- oder Smart-Card-Anmeldung anzeigen. NPR-20708
* Forms JEE unterstützt die gegenseitige Authentifizierung mit PKCS#11. NPR-15001

## In CFP10 enthaltende OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-in-cfp-4}

Liste der in AEM CFP 6.2 SP1-CFP10 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/bundle-list-cfp10.txt)

Liste der in AEM CFP 6.2 SP1-CFP10 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Klassische Analytics-Benutzeroberflächenkonfiguration wurde für die Geheimniseingabe angepasst.
* Fehlerbehebungen für unabhängigen Persistenzcache für ContextHub.
* Genaue Berechnung der Asset-Dimensionen.
* Die AEM-Leistung wurde beim Veröffentlichen von Assets in Brand Portal optimiert.
* Korrekturen im Wert `Resourcetype` im Arbeitsflächenknoten.
* Die Suchfunktion für Dokumentfragment-Inhalte wurde mit der Unterscheidung zwischen Groß- und Kleinschreibung und Sonderzeichen aktiviert.
* Adaptive Formulare wurden verbessert, um PDF als Anlagen in Safari anzuhängen.
Diese Erfahrung bietet eine neue Dynamic Media, die eine Verbindung zur neuen Dynamic Media Publishing-Infrastruktur herstellt, um die Replikation zu beschleunigen und zu skalieren.

### Assets {#assets-10}

* AEM Assets kann keine Unter-Asset-Verweise für InDesign-Assets extrahieren, die doppelte Verknüpfungen zum Asset enthalten. NPR-19006: Hotfix für CQ-4204186
* Die Option „Sortieren“ funktioniert nicht für Assets innerhalb der Sammlung unter Commerce. NPR-19508: Hotfix für CQ-4213622
* Wenn ein Asset mit demselben Namen wie ein bereits vorhandenes Asset an denselben Speicherort verschoben wird, wird der Wert von `cq:lastReplicationAction` für die Assets untereinander vertauscht, was die Erstellung falscher Metadaten verursacht. NPR-19531
* Beim Veröffentlichen vieler Assets wird eine Fehlermeldung angezeigt, obwohl alle Assets korrekt veröffentlicht wurden. NPR-19629: Hotfix für CQ-4219611
* Statische Ausgabedarstellungen werden mit festen Abmessungen aufgeführt und spiegeln nicht die Größe der tatsächlichen Ausgabedarstellung wider. NPR-20004
* Wenn mehrere Assets (mehr als 4) in Brand Portal veröffentlicht werden sollen, reagiert die AEM-Instanz nur langsam. NPR-20009

### Sites {#sites-10}

* AEM zeigt unerwartetes Verhalten an, wenn ein Benutzer versucht, die Veröffentlichung vorzunehmen `/unpublish/create` -Version einer Seite, die von einem anderen Benutzer gesperrt wurde. NPR-19249; Hotfix für CQ-4215298 und CQ-4203856
* Beim manuellen Weiterleiten des verschachtelten Launches wird die untergeordnete Seite gelöscht. NPR-19704
* Persistenzprobleme, wenn ContextHub-Stores die standardmäßige Persistenzschicht während der Initialisierung überschreiben. NPR-19979: Hotfix für CQ-4218399
* Inhaltsfragmente überschneiden sich mit anderen Schaltflächen. NPR-19980: Hotfix für CQ-4221519
* Die Site-Seite wird nicht angezeigt, wenn sie mit einem Alias in SiteAdmin angezeigt wird. NPR-20053: Hotfix für CQ-4221478
* Fehler beim Veröffentlichen einer Live Copy-Seite, die auf eine Importer-Seite in Adobe Campaign verweist. NPR-20066: Hotfix für CQ-4220846

### Plattform {#platform-8}

* Apache POI wurde auf Version 3.16 aktualisiert, um die Einbeziehung des Hintergrundbilds von PPT-Folien in Ausgabedarstellung zu unterstützen. NPR-18286
* Rendering-Probleme mit Internet Browser 11 und Edge beim Hochladen mehrerer Assets in denselben Ordner. NPR-20062

### Integration {#integration-11}

* Die benutzerdefinierte at.js-Datei wird nicht veröffentlicht, wenn der Zugriff via anonymer Benutzer erfolgt. NPR-19542: Hotfix für CQ-4219592
* Migration vorhandener Analytics-Anmeldeinformationen zur WSSE-Authentifizierung. NPR-19962

### Brand Portal {#brand-portal}

* Aktivieren von Veröffentlichungs-Tags von AEM in Brand Portal über die Tagadmin-/Tagging-Konsole NPR-20271

## Formulare {#forms-11}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

### Forms-Add-on-Paket {#forms-add-on-package-11}

#### Korrespondenzverwaltung {#correspondence-management-4}

* Funktionalität zum Suchen nach aktuellem Text in Dokumentfragmenten aktiviert, wenn ein Brief in der Vorschau angezeigt wird. NPR-19712

#### Adaptive Formulare {#adaptive-forms-8}

* Adaptive Formulare wurden verbessert, um PDF als Anlagen in Safari anzuhängen. Um dieselbe Funktion in vorhandenen Formularen zu unterstützen, ändern Sie die Konfiguration im Anhang-Widget und aktualisieren Sie unter &quot;Unterstützte Dateitypen&quot;den Wert application/pdf anstelle von .pdf. NPR-19623

#### Forms Manager {#forms-manager-1}

* Wenn validationState in einem Feld des adaptiven Formulars nicht definiert ist und das ElementFocusChanged -Ereignis auftritt, wird ein Fehlerereignis (errorState) an den Adobe Analytics-Server zurückgegeben. NPR-19513

### JEE-Installationsprogramm von Forms {#forms-jee-installer-11}

#### Core {#core-3}

* Der Verbindungsmanager ist während des Herunterfahrens nicht verfügbar. JBoss® schneidet die JDBC-Abhängigkeit ab, bevor die Autoren-EAR nicht mehr bereitgestellt wird, was zu Korruptionsproblemen führt. NPR-19703

## Enthaltene Feature Packs {#feature-packs-included-1}

* Miniaturbildkorrektur und Transparenzverbesserungen in Dynamic Media. NPR-15207

## In CFP9 enthaltende OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-in-cfp-5}

Liste der in AEM 6.2 SP1-CFP9 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Liste der in AEM 6.2 SP1-CFP9 aktualisierten OSGi-Bundles

[Datei laden](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Einführung von Tags für benutzerdefinierte Vorlagen im Adobe-E-Mail-Vorlagen-Service.
* Verbesserungen der Schaltflächen in der Touch-optimierten Benutzeroberfläche des Desktop-Programms.
* Die Senden-Schaltfläche beim Klicken wurde deaktiviert, um zu verhindern, dass mehrere Formulare auf einer Übersetzungsseite gesendet werden.
* Mehrere RTE-Komponenten wurden in einem Dialogfeld konfiguriert.
* Verbesserte Aktualisierungen von Referenzen in Live Copy.
* Die Suchfunktion für Dokumentfragment-Inhalte wurde mit der Unterscheidung zwischen Groß- und Kleinschreibung aktiviert.
* Eine Liste mit Linux®®-Bibliotheken wurde zur Installationsdokumentation von AEM Forms hinzugefügt.

### Assets {#assets-11}

* Probleme bei der Anwendung des Omnisearch-Filters auf Smart-Sammlungen im Safari-Browser. NPR-19511
* PDF-Stichwortmetadaten werden nicht korrekt extrahiert und geändert, wenn mehrere Stichwörter mit einem PDF-Asset verknüpft sind. Um das Problem zu beheben, wurde die Metadateneigenschaft für das Feld „Betreff“ für PDF-Assets entfernt. Sie können das Metadatenschema jedoch bearbeiten, um ein Textfeld mit mehreren Werten für das Feld „Betreff“ hinzuzufügen. NPR-19126
* Der Workflow-Benachrichtigungsdienst kodiert die Links nicht in E-Mails, was verhindert, dass sie geladen werden, nachdem Benutzer darauf geklickt haben. NPR-19490: Hotfix für CQ-4218055
* Eine vollständige Liste der Seiten/Assets kann nicht mit Chrome in der Spaltenansicht geladen werden. NPR-19458: Hotfix für CQ-4214248
* Das falsche Symbol Ausschaltzeit wird im AEM Posteingang angezeigt, wenn der Workflow &quot;Aktivierungsanfrage&quot;aktiviert wird. NPR-19365: CQ-4216174
* Probleme mit der Sortierung in der Listenansicht. NPR-19217: CQ-95602
* Beim Ändern des Titels oder des Miniaturbilds in den Einstellungen des Asset-Ordners werden die ursprüngliche Gruppe und die Berechtigungen des Ordners überschrieben. NPR-19283: Hotfix für CQ-4216080
* `Windows 10`-Workstations wechseln automatisch in den Touch-Modus, wodurch einige Schaltflächen nicht mehr funktionieren. NPR-19183

### Sites {#sites-11}

* Probleme mit mehreren RTE-Komponenten in einem Dialogfeld. NPR-19311: NPR-19587
* Die automatische Versionsbereinigung in Vanilla AEM 6.2 funktioniert nur einmal, nachdem VersionManagerImpl initialisiert wurde. NPR-19315: Hotfix für CQ-4217175
* Die Workflow-Instanz hängt am Workflow-Schritt &quot;Salesforce.com Export&quot; fest. NPR-19222: Hotfix für CQ-4212976
* Sprachkopien von Seiten, die aus Live Copies erstellt wurden, können nicht bearbeitet werden. NPR-18967
* ReferencesUpdateAction kann Links in eine verschachtelte LiveCopy mit Hierarchieänderung nicht aktualisieren. NPR-18715: Hotfix für CQ-4214105

### Plattform {#platform-9}

* Der Adobe-E-Mail-Vorlagendienst fügt benutzerdefinierten Benutzervorlagen Tags hinzu. NPR-19190: Hotfix für CQ-4217113

### Projekte {#projects-2}

* Projekt-Editoren können keine Assets in den Projekt-Asset-Ordner kopieren/einfügen. NPR-19619
* Nach der Installation von 6.2 SP1-CFP1 kann keine Vorschau für Übersetzungsprojekte generiert werden. NPR-16481: CQ-4204655

### Integration {#integration-12}

* Zugriffseigenschaften für Artikel werden in Adobe Digital Publishing Solution in der klassischen Benutzeroberfläche falsch eingestellt. NPR-19366
* Reduziertes Rendering von Miniaturansichten aufgrund von Artikeln in voller Größe in AEM Artikelkonsole. NPR-19086: CQ-4217148
* Falsches Verhalten der automatischen Faltung bei der Personalisierung von Angeboten über Campaign, wenn Benutzer Zugriff auf mehrere Bereiche haben. NPR-19290: Hotfix für CQ-4218029
* Das Targeting-Dialogfeld wird nicht im Targeting-Modus angezeigt, wenn ein Zielmodul bearbeitet und mehrmals gespeichert wird. NPR-19144: Hotfix für CQ-4216708

### Workflow {#workflow-2}

* Benutzer können die Benachrichtigungen im Posteingang nicht nach Benutzer/Gruppe in der Benutzeroberfläche von Inbox Classic filtern. NPR-19122: Hotfix für CQ-4215374
* Die in der HTL-Bildkomponente ausgewählten Koordinaten werden in der Imagemap nicht beibehalten. NPR-18911: CQ-4211584

## Formulare {#forms-12}

* AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-12}

* Wenn Inhalte aus Microsoft® Word oder einem Webbrowser in den Correspondence Manager-Texteditor kopiert werden, geht der Stil verloren. NPR-19530
* Inhalt ohne Zeilenumbruch im Texteditor kann nicht umgebrochen werden. NPR-19481
* Funktionalität zum Suchen nach aktuellem Text in Dokumentfragmenten aktiviert, wenn ein Brief in der Vorschau angezeigt wird. NPR-17792: Hotfix für CQ-4214501

#### Korrespondenzverwaltung {#correspondence-management-5}

>[!NOTE]
>
>Diese Suchfunktion für Textfragmente hat einige Einschränkungen:-
>
>* Bei Dokumentfragment-Inhalten wird die Groß-/Kleinschreibung beachtet, bei Titeln wird nicht zwischen Groß- und Kleinschreibung unterschieden.
>* Suchergebnisse werden nicht hervorgehoben, wenn ein Teil des gesuchten Wortes in einem anderen Stil gehalten wird oder ein Sonderzeichen wie &quot; oder &quot; oder &quot; enthält.
>* Die Suche funktioniert nicht für dynamischen Inhalt (wie Datenwörterbuchelementwerte oder Variablenwerte) im Dokumentfragment.

#### Forms Manager {#forms-manager-2}

* Die XML-Schemaeigenschaften von adaptiven Formularen können nach Anwendung von CFP6 auf AEM 6.2 nicht bearbeitet werden. Hotfix für CQ-4219684
* Alle Dienste des AEM Forms Manager-Kernpakets werden beim Neustart des Servers nicht gestartet. Hotfix für CQ-4217014

### JEE-Installationsprogramm von Forms {#forms-jee-installer-12}

#### Installieren von LCM {#install-lcm-2}

* Auf dem Administratorbildschirm unter Microsoft® Windows wird nach der Installation von CFP6 die Versionsnummer 6.0 angezeigt. Hotfix für CQ-4217573

## Enthaltene Feature Packs {#feature-packs-included-2}

* Verbesserungen der Schaltflächen in der Touch-optimierten Benutzeroberfläche des Desktop-Programms. NPR-18676

## In CFP8 enthaltene OSGi-Bundles {#osgi-bundles-included-in-cfp}

Liste der in AEM 6.2 SP1-CFP8 aktualisierten OSGi-Bundles

[Datei laden](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Liste der in AEM 6.2 SP1-CFP8 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Verhaltensänderung bei der Anzeige von Titeln auf der Grafikkarte für Bild mit dc: title-Eigenschaft auf String (multifield) eingestellt.
* Fehlerkorrekturen in Leistungsproblemen mit Dynamic Media-Cloud Services, Touch-Benutzeroberfläche und Benutzeroberfläche für Sicherheit.
* Fehlerbehebungen in Apache Felix HTTP Bridge 3.0.8
* Binärlose Replikation (BLR) zwischen Autoren- und Veröffentlichungsumgebung wurde korrigiert.
* Die Unterstützung für die Target-Bibliotheksdatei AT.JS, eine Implementierungsbibliothek für die Client-seitige Integration mit Adobe Target, ist sowohl für typische Webimplementierungen als auch für Einzelseitenanwendungen entwickelt.
* Die Leistung von AEM wurde verbessert, indem eine benutzerkonfigurierbare Zeitüberschreitungsdauer für die Verbindung mit Analytics, DTM und Target eingeführt wurde.

### Assets {#assets-12}

* Beim Testen der Videoaufnahme mit AEM 6.3, die mit Dynamic Media-Cloud Services konfiguriert wurde, wird die Ausnahme „Zu viele geöffnete Dateien“ ausgelöst. NPR-18734; Hotfix für CQ-4211407
* Die Einstellung für die Vanity-URL für Assets auf einer Seite funktioniert nicht, nachdem die AEM-Instanz neu gestartet wurde. NPR-18634; Hotfix für Granite-18085
* In der Touch-optimierten Benutzeroberfläche wird die Schaltfläche „Veröffentlichen“ für Benutzer ohne Berechtigung zum Veröffentlichen von Assets angezeigt. NPR-18620; Hotfix für CQ-4214042
* Die Option zur dynamische Ausgabedarstellung ist im Dialogfeld „Herunterladen“ für ein Asset nicht vorhanden, nachdem die Lizenzvereinbarung für dieses Element festgelegt wurde. NPR-18607; Hotfix für CQ-4212342
* Dynamische Ausgabedarstellungen können nicht für Assets heruntergeladen werden, die Leerzeichen in ihren Namen enthalten. NPR-18571; Hotfix für CQ-4211738
* Bei der Freigabe des Asset-Ordners mit Creative Cloud kann nicht mehr als ein Benutzer gespeichert werden. NPR-18489; Hotfix für CQ-103297
* dc: title und dc: Die Beschreibung ändert sich nicht in einen Wert für mehrere Felder in crx/de. NPR-18474; Hotfix für CQ-4209086
* Der Vorgang zum Verschieben von Assets führt zu einer Leistungsbeeinträchtigung. NPR-18346
* In der Zeitleiste werden keine Elemente angezeigt, wenn die Standardoption „Alle anzeigen“ aktiviert ist. NPR-18302; Hotfix für CQ-4211957
* Ein Fehler tritt auf, wenn eine ASCII/UTF-8-kodierte Textdatei in AEM Assets hochgeladen wird und die Erstellung von Miniaturbildern fehlschlägt. NPR-18006: CFP für CQ-4209345
* Aktionsschaltflächen in Publish sind auch dann sichtbar, wenn der Benutzer nicht über den Replikationszugriff verfügt. NPR-17353; Hotfix für CQ-4209269
* Sowohl Site-Admin als auch Misc-Admin funktionieren nicht, wenn die Minimierung mit min:gcc;obfuscate=true aktiviert ist. NPR-18593; Hotfix für CQ-4209220
* Benutzerdefinierte Menüelemente werden erst angezeigt, wenn der Bildschirm jedes Mal aktualisiert wird. NPR-18500; Hotfix für CQ-4213581
* Aktualisierung von moment.js auf 2.10.6. NPR-18596; Hotfix für Granite-11881
* Das Anwenden von Berechtigungen für DM-Makros unterbricht die Ansicht für den Admin-Benutzer. NPR-18544; Hotfix für CQ-4211729
* Durch „Später veröffentlichen“ für Assets wird eine ungültige ArgumentException ausgelöst. CQ-4214532

### Sites {#sites-12}

* Auf einem aktiven Autoren-Cluster mit MongoDB versuchen beide Autoren, die Inhaltsreplikation für denselben Trigger durchzuführen, wenn die -Zeit den für den Inhalt festgelegten Einschaltzeitwert erreicht. NPR-18708; Hotfix für CQ-4210982
* NPE beim Verschieben einer Ressource mit einem Verweis ohne jcr: content-Knoten. NPR-18664
* Platzhalter sind nicht auf einer Seite sichtbar, die mehrere Parsys-Komponenten enthält. NPR-18645; Hotfix für CQ-110253
* Parallelitätsprobleme bei AbstractCopyMoveCommand. NPR-18591
* Wenn Text von einer anderen AEM-Instanz in eine Parsys-Komponente kopiert wird, wird die Parsys ohne einen festgelegten Ressourcentyp erstellt. NPR-18511; Hotfix für CQ-4212306

### Plattform {#platform-10}

* JCR Installer aktualisiert die Bundle-Version nach der Paketinstallation nicht. NPR-18728; Hotfix für NPR-15135
* Binärlose Replikation (BLR) schlägt bei Binärdateien zwischen Autoren- und Veröffentlichungsumgebung fehl. NPR-18704
* Apache Felix HTTP Bridge-Auflösungsanforderung in einer AEM Umgebung. NPR-18297
* Die Replikation schlägt fehl, wenn mehrere Seiten mit ähnlicher Struktur gleichzeitig mit der Sling Content Distribution repliziert werden. NPR-18665; Hotfix für Granite-13712
* Sling Distribution-Pakete bauen sich auf und werden nicht selbst bereinigt. NPR-18601; Hotfix für Granite-16183

### Integration {#integration-13}

* Beim Anzeigen werden Ergebnisse, die aus Bibliotheksordnern veröffentlicht wurden, in NPE angeboten. NPR-18732; Hotfix für CQ-4214593
* Das Start-/Enddatum für eine Aktivität wird in JCR und Target nicht aktualisiert, wenn es von einem bestimmten Datum in „Bei Aktivierung/Deaktivierung“ geändert wird. NPR-18612; Hotfix für CQ-104831
* Für die Analytics-Integration mit AEM wurden keine Verbindungs- oder Socket-Zeitüberschreitungen für die httpclient-Verbindungen festgelegt. NPR-18497
* Für die DTM-Integration mit AEM wurden keine Verbindungs- oder Socket-Zeitüberschreitungen für die httpclient-Verbindungen festgelegt. NPR-18495
* Für die Target-Integration mit AEM wurden keine Verbindungs- oder Socket-Zeitüberschreitungen für die httpclient-Verbindungen festgelegt. NPR-18494
* Target-Aktivität wird deaktiviert, nachdem ein zusätzliches Erlebnis hinzugefügt wurde. NPR-18227; Hotfix für CQ-4201895

### WCM – Foundation-Komponenten {#wcm-foundation-components-7}

* Bei Imagemaps werden die ausgewählten Koordinaten in der HTL-Bildkomponente nicht beibehalten. NPR-18530; Hotfix für CQ-4211584

### Übersetzung {#translation-5}

* In Ergebnissen einer Übersetzungssuche sind keine Namen von Übersetzungsprojekten enthalten. NPR-18224; Hotfix für CQ-4210658

### Brand Portal {#brand-portal-1}

* Aktivieren von Veröffentlichungs-Tags von AEM in Brand Portal über die Tagadmin-/Tagging-Konsole CQ-4212165

## Formulare {#forms-13}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-13}

#### Korrespondenzverwaltung {#correspondence-management-6}

* Die korrekten Daten werden erst dann im Bearbeitungsbedienfeld angezeigt, wenn das Fragment gespeichert wurde. NPR-19092
* Das Hinzufügen von Dokumentfragmenten zu einem Brief nimmt viel Zeit in Anspruch. NPR-18958
* Wenn eine XML-Deklaration in einer XML-Datendatei vorhanden ist und die Ausgabedarstellung von Briefen über eine POST-Anfrage initiiert wird, zeigt der entsprechende Brief keine Daten an. NPR-18870
* Für Aktionen, die an CM-Assets vorgenommen werden, werden keine Auditprotokolle generiert. NPR-16618

>[!NOTE]
>
>Installieren Sie dieses CFP-Add-On-Paket nicht, wenn Sie von den folgenden zwei Problemen betroffen sind:
>
>* &quot;Aus Word/Web in CM-Texteditor kopieren&quot;zeigt Zeilenumbruchinhalte an. NPR-19530
>* Inhalte ohne Zeilenumbruch im CM-Texteditor können nicht umgebrochen werden. NPR-19449
>

#### Adaptive Formulare {#adaptive-forms-9}

* Beim Hinzufügen eines Bereichs für wiederholbare Bereiche wird der Wert des Dropdown-Felds im vorherigen Bereich gelöscht. NPR-18772
* Adaptive Formularfelder, die als Ganzzahlen markiert sind, akzeptieren auch einige Sonderzeichen aus dem Ziffernblock. NPR-18680
* Ein Skript zum Ändern des Schaltflächentitels beim Initialisierungs-Ereignis des Guide-Stammbereichs funktioniert nicht. NPR-18476
* Die Bildlaufleiste wird im rechten Bereich für Regeln, die im Regeleditor erstellt wurden, nicht angezeigt. NPR-18716

#### AEM Forms-App {#aem-forms-app}

* Formulare werden in der AEM Forms-App nicht ordnungsgemäß gerendert, wenn sie sich im Offline-Modus befindet oder nicht mit dem Netzwerk verbunden ist. CQ-4218368

### JEE-Installationsprogramm von Forms {#forms-jee-installer-13}

#### PDFG Service {#pdfg-service-3}

* PDF Generator kann keine PDF-Dokumente mit bestimmten Lesezeichenebenen erstellen. Hotfix für CQ-4211102

## In CFP7 enthaltene OSGi-Bundles {#osgi-bundles-included-in-cfp-1}

Liste der in AEM 6.2 SP1-CFP7 aktualisierten OSGi-Bundles

[Datei laden](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Liste der in AEM 6.2 SP1-CFP7 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Effiziente Verwaltung ausgeblendeter Komponenten im Layout-Modus auf dem Tablet.
* Einführung von Schnellaktionen auf Hybrid-Geräten.
* Beheben von Synchronisierungsproblemen auf Komponentenebene mit Live Copies.

### Assets {#assets-13}

* Ein Kunde wird blockiert, wenn ein Benutzer, der nicht über die erforderliche Berechtigung verfügt, versucht, den Vorgang für ein Asset zu verschieben. NPR-18330; Hotfix für CQ-4212560
* Das Zusammenführen mehrerer Konfigurationen für intelligente Content Services führt zu Problemen mit der Benutzerfreundlichkeit. NPR-18273; Hotfix für CQ-4201557
* Die Aktion &quot;Auschecken&quot;/-Workflows sind nicht einmal in der Timeline-Konsole verfügbar. Im Ordner &quot;Assets&quot;werden 80 Fragmente hinzugefügt. NPR-18257; Hotfix für CQ-4211214 und NPR-18251; Hotfix für CQ-4211216.
* Das System stürzt bei nicht genügend Speicher ab. Außerdem fehlt die Paginierung bei Assets-Berichten. NPR-17865; Hotfix für CQ-4209759
* Das veröffentlichte Video kann bei codierten Video-Assets nicht wiedergegeben werden. NPR-17849; Hotfix für CQ-4210739
* Eine Miniaturansicht für die PDF wird nicht generiert. NPR-17831, NPR-17750; Hotfix für CQ-4210547
* Der Adobe CQ DAM-Ablaufbenachrichtigungsauftrag deaktiviert keine abgelaufenen Assets. NPR-17666; Hotfix für CQ-107766
* Die Aktivitäten zum Ablauf von Assets werden beendet, wenn einem Asset kein Eigentümer zugewiesen ist. NPR-17665; Hotfix für CQ-4197946
* Wenn ein Asset-Ordner mit mehr als 150 eingehenden Referenzen verschoben wird, wird eine Null Pointer-Ausnahme ausgelöst. CQ-4200981

### Sites {#sites-13}

* Personalization funktioniert nur für die erste IP-Adresse, wenn die Segmentierungsregel für einen IP-Bereich festgelegt ist. NPR-18121; Hotfix für CQ-83767
* Die Anmeldung schlägt aufgrund von NumberFormatException fehl, wenn die Eigenschaft historyShow aktiviert ist. NPR-18073; Hotfix für CQ-101965
* Gelöschte Seiten, die als markiert sind, sind in der Touch-Benutzeroberfläche sichtbar. NPR-18025; Hotfix für CQ-86694
* Leistungsprobleme beim Laden einer Seite mit großen (über 2000) Zielgruppen. NPR-17884; Hotfix für CQ-4209567
* Sie können kein Bild auswählen, nachdem Sie ein anderes Bild auf der Seite entfernt haben. NPR-17711; Hotfix für CQ-4201323

### Plattform {#platform-11}

* Die Steuerelemente der Touch-Benutzeroberfläche sind für Benutzer mit den erforderlichen Berechtigungen ausgeblendet. NPR-17945; Hotfix für CQ-4211231
* Japanische Tags fehlen im Tag-Auswahlfeld. NPR-17768; Hotfix für CQ-4210456
* Die Abfrage getsize () gibt falsche Ergebnisse zurück, wenn FastQuerySize aktiviert ist. NPR-18018
* Auf die Web-Konsole in der Standby-Instanz kann nicht zugegriffen werden. NPR-17861; Hotfix für Granite-14582

### Commerce {#commerce-2}

* Die Durchsicht von Abfragen erfolgt, wenn für einen Katalog-Blueprint keine Bedingung für einen Abschnitt definiert ist. NPR-18229; Hotfix für CQ-4211924

### Communities {#communities-2}

* PollingImporterImpl. verzögert das Herunterfahren von AEM. NPR-18298; Hotfix für CQ-96133

### Integrationen {#integrations}

* Behebung von Fehlern in der AEM-Suchkomponente, die auftreten können, wenn AEM Day HTTP Client 3.1 OSGI mit einem Proxy konfiguriert ist, für den die Digest-Authentifizierung erforderlich ist. NPR 18128
* Kontrollkästchen fehlt, damit Sie die Vererbung wiederherstellen können. NPR-17753; Hotfix-Anfrage für GRANITE-4210139
* Benutzer können die Priorität nicht festlegen, wenn sie auf eine Komponente mit mehreren Aktivitäten abzielen. NPR-18658; Hotfix für CQ-4210727
* Benutzer können den Ordner „/etc/segmentation“ nicht durchsuchen, um eine Zielgruppe auszuwählen, die unter dem Ordner „/etc/segmentation/group1“ erstellt wurde. NPR-18522

### Sicherheit {#security-1}

* Der Assistent zum Verschieben von Assets bleibt hängen, wenn der Benutzer keine Schreibberechtigung für den Zielordner hat. NPR-18300
* Anfrage zur Verwendung einer aktualisierten Version von org.apache.sling.servlets.post servlet (2.3.22) in der Apache Sling API, um eine XSS-Schwachstelle zu verhindern. NPR-18963

### Übersetzung {#translation-6}

* Die Übermittlung der Asset-Seite sollte für ein Übersetzungsprojekt erst nach Abschluss des Projekts erforderlich sein. NPR-18249; Hotfix für CQ-4209908

### WCM – Foundation-Komponenten {#wcm-foundation-components-8}

* Die WCM Foundation Iparsys-Komponente kann nicht in bearbeitbaren Vorlagen verwendet werden. NPR-18223; Hotfix für CQ-4210384
* Die in der HTL-Bildkomponente ausgewählten Koordinaten werden in der Imagemap nicht beibehalten. NPR-18032; Hotfix für CQ-4211584
* Wenn eine HTL-Bildkomponente gerendert wird, wird der Dateiname in der URL umbenannt, was zu einer fehlerhaften URL führt. NPR-17908; Hotfix für CQ-4211587
* Die Seiteneigenschaften können nach Durchführung der Änderungen nicht mehr verlassen werden. NPR-17832; Hotfix für CQ-96110

## Formulare {#forms-14}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-14}

**Korrespondenzverwaltung**

* Das Datenwörterbuch wird beim Rendern von Briefen wiederholt gelesen. NPR-18482: Hotfix für CQ-4210805
* JavaDocs für die Klasse com.adobe.livecycle.content hinzugefügt. NPR-18467
* Beim Erstellen eines Briefs wird die Beschreibung des Briefs nicht gespeichert. NPR-18039
* Wenn ein Textmodul gespeichert wird und ein Ausdruck im Textmodul keine öffnenden oder schließenden Ausdrucks-Tags enthält, wird keine Fehlermeldung angezeigt. Das Textmodul zeigt eine Fehlermeldung an und Rendering im Brief funktioniert nicht. NPR-17798
* Unerwartete Fehler werden in den Protokollen zur Installation eines Add-On-Pakets angezeigt. NPR-18295

**Forms Manager**

* In der Benutzeroberfläche von AEM Forms werden die Assets beginnend mit dem ältesten aufgelistet. Benutzende können die Assets nicht in der Reihenfolge „Neueste zuerst“ sortieren. NPR-18451

### JEE-Installationsprogramm von Forms {#forms-jee-installer-14}

**Ausgabe-Service**

* Leistung des Ausgabe-Service für AEM Forms 6.2 wurde verbessert. NPR-18033

**Signatur-Service**

* Ein PDF-Dokument kann nicht mit einem Remote-Hardware-Sicherheitsmodul signiert werden. NPR-18017

## In CFP6 enthaltene OSGi-Bundles {#osgi-bundles-included-in-cfp-2}

Liste der in AEM 6.2 SP1-CFP6 aktualisierten OSGi-Bundles

[Datei laden](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Liste der in AEM 6.2 SP1-CFP6 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Es wurden mehrere Probleme mit der Benutzeroberfläche beim Freigeben, Verschieben, Veröffentlichen und Herunterladen von Assets behoben.
* Verbesserte Kapazität des Dialogfelds „Verschieben“ bei der Anzeige referenzierter Assets.
* Es wurden mehrere Probleme mit WCM-Komponenten und Workflows behoben, z. B. „Veröffentlichung aufheben“ und „Versionsbereinigung“.
* Verbesserte Reaktionsfähigkeit der Aktionsleiste bei der Anzeige von Symbolleistenaktionen und Coral-Komponenten.

### Assets {#assets-14}

* Leistungsverbesserungen in der Funktionalität zum Veröffentlichen im Brand Portal. NPR-17189; Hotfix für CQ-4204150
* Bei der Freigabe eines Assets mit der Option „Link freigeben“ wird keine ZIP-Datei mit einer flachen Ordnerstruktur zum Herunterladen erstellt. NPR-17513; Hotfix für CQ-4209381
* Wenn Sie ein Asset in DAM auswählen und auf „Veröffentlichen“ klicken, wird die Option „Im Brand Portal veröffentlichen“ auf der Seite „Asset-Details“ nicht angezeigt. NPR-17351; Hotfix für CQ-94905
* In DAM-Workflow-Schritten müssen binäre Streams, die von Session oder ResourceResolver erfasst wurden, in einem endgültigen Block geschlossen werden. Dadurch wird sichergestellt, dass keine Ressourcenlecks auftreten. NPR-17385; Hotfix für CQ-4209452
* Das Hochladen eines Word-Dokuments in DAM führt zu einer Null-Zeiger-Ausnahme und die Workflow-Instanz bleibt im Status „Wird ausgeführt“ hängen. NPR-17160; Hotfix für CQ-4207358
* Die Schaltflächen „Freigeben“, „Verschieben“, „Veröffentlichen“ und „Herunterladen“ sind für abgelaufene Assets auf der Seite „Metadaten-Editor“ für Benutzer ohne Administratorrechte sichtbar. NPR-16903; Hotfix für CQ-101440/CQ-104535
* Aktionen wie „Freigeben“, „Verschieben“, „Veröffentlichen“ und „Kopieren“ sollten für Administratoren in der Assets-Konsole sichtbar sein. NPR-16902; Hotfix für CQ-4207111

### Sites {#sites-14}

* Beim Verschieben einer Seite mithilfe der klassischen oder der Touch-optimierten Benutzeroberfläche werden im Dialogfeld „Verschieben“ keine Verweise über 150 angezeigt, sodass Benutzende diese Verweise nicht aktualisieren und die Seite nicht erneut veröffentlichen können. Dieses Problem wurde behoben, indem eine Eigenschaft für die klassische Benutzeroberfläche eingeführt wurde: &quot;maxRefNo&quot;, die auf dem Site-Admin-Knoten konfiguriert werden kann: `'/libs/wcm/core/content/siteadmin'`. Diese Eigenschaft gibt die maximale Anzahl von Verweisen (Standardwert 150) an, die vor einem umfangreichen Verschiebevorgang angezeigt wird. Wenn eine Seite mehrere Verweise enthält, werden diese nicht im Dialogfeld „movePage“ angezeigt. Diese Konfiguration funktioniert auch für dam admin und misc admin , indem die Konfiguration auf die Knoten angewendet wird: `'/libs/wcm/core/content/damadmin'` und `'/libs/wcm/core/content/miscadmin'` bzw. NPR-17222; Hotfix für CQ-85878

* Beim Arbeiten mit WCM-Komponenten werden Hyperlinks mit Leerzeichen im Rich-Text-Editor der Touch-optimierten Benutzeroberfläche entfernt. NPR-17698, NPR-17570; Hotfix für CQ-4206768
* Beim Auslösen des Workflows zum Anfordern des Rückgängigmachens der Veröffentlichung aus den Seiteneigenschaften werden für Benutzer ohne Replikationsrechte JavaScript-Fehler angezeigt. NPR-17294; Hotfix für CQ-102064
* Beim Rendern oder Exportieren einer HTL-Bildkomponente wird die URL in eine Zahl geändert, wobei der Dateiname umbenannt wird, wodurch fehlerhafte Links entstehen. NPR-17245; Hotfix für CQ-59616
* Wenn ein Launch in einem verschachtelten Launch gelöscht wird, sind die Sub-Launches verwaist. NPR-17228; Hotfix für CQ-4202639
* Die Ausführung von Versionsbereinigungen in AEM 6.2 mit Oak 1.4.13 verursacht eine ständig wiederkehrende Warnung in den Protokollen. NPR-17391; Hotfix für CQ-4206870
* Nach der Installation eines Hotfixes oder einer Aktualisierung für die ContextHub-Komponente überschreibt das Inhaltspaket alle Segmente in „/etc/segmentation/contexthub“, wodurch alle benutzerdefinierten ContextHub-Segmente verloren gehen. NPR-17250; Hotfix für CQ-79958
* Beim Ausführen eines Workflows mit verschachtelten Gruppen als Workflow-Benutzer führt der WorkflowStatusProvider (pageinfo.json) zu einer Sperrung der Workflow-Instanz. NPR-17555; Hotfix für CQ-4202056
* Bei Verwendung der WCM-Seiten-Editor-Komponenten ist am Ende der Seite im Bearbeitungsmodus in der Touch-optimierten Benutzeroberfläche der Autoreninstanz ein riesiger Leerraum vorhanden. NPR-17510; Hotfix für CQ-4205441
* Beim Rendern oder Exportieren einer HTL-Bildkomponente wird die URL in eine Zahl geändert, wodurch fehlerhafte Links entstehen. NPR-17245; Hotfix für CQ-59616

### Benutzeroberfläche {#ui}

* Wenn Sie ein Asset auswählen und auf „Developer Tools“ klicken, werden die Aktionen der Symbolleiste in der Aktionsleiste bei langsamen Verbindungen nicht immer angezeigt, und die Seite muss neu geladen werden. NPR-17568; Hotfix für CQ-108365
* Die Aktionsleiste sollte aktualisiert werden, um zwei Container zu verwenden: „coral-actionbar-primary“ und „coral-actionbar-secondary“, anstelle von „coral-actionbar-container“. NPR-17591; Hotfix für GRANITE-15225

### Mobile On-Demand {#mobile-on-demand-2}

* Benutzer mit der Berechtigung &quot;Schreibgeschützt&quot;für das AEM Mobile-Programm können keine Inhaltsvorschau auf der Seite &quot;AEM Mobile Content Management&quot;anzeigen. NPR-17390; Hotfix für CQ-4209690

### Sicherheit {#security-2}

* XSS-Sicherheitsanfälligkeit in der von HTMLRendererServlet generierten Ausgabe. NPR-17136
* Anfrage, die Offenlegung der AEM-Version auf der Seite „AEM Web Syndication Feeds“ zu verhindern. NPR-16219

### Formulare {#forms-15}

#### Forms-Add-on-Paket {#forms-add-on-package-15}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

**Adaptive Formulare**

* Für ein adaptives Formular mit Anhang werden doppelte Einträge für die afSubmissionInfo -Tags in der gesendeten XML erstellt, wenn das Formular zum zweiten Mal gesendet wird. NPR-17364
* Bei Verwendung des Google Chrome-Browsers wird nach dem Entfernen einer Anlage aus einem Formular ein Fehler ausgegeben, wenn versucht wird, dieselbe Anlage erneut anzuhängen. NPR-17297
* Falls in XSD-basierten adaptiven Formularen oder in adaptiven Formularen ohne Formularmodell verschachtelte, wiederholbare Lazy-Loading-Bedienfelder vorhanden sind, werden die im Formular ausgefüllten Werte nicht im Datensatzdokument (DOR) beibehalten. NPR-17176
* Fehler, die im Fehlerprotokoll für den Regel-Editor angezeigt werden, sollten im catch-Block eines JavaScript-Codes für den try/catch-Block hinzugefügt werden. NPR-16757
* Wenn Sie auf eine Dateianlage in einem Formular klicken, wird ein Browser-Konsolenfehler ausgegeben und die Vorschau der Anlage wird nicht angezeigt. NPR-17174

**Korrespondenzverwaltung**

* Die Benutzeroberflächenfunktionalität „Korrespondenz erstellen“ bricht ab, wenn Inline-Text oder eine Leerzeile in die Benutzeroberfläche eingefügt wird. NPR-17748
* Der Browser flimmert, wenn ein Brief zur Bearbeitung geöffnet wird. NPR-17576
* Wenn Remote-Funktionen in berechneten Datenwörterbuchelementen hinzugefügt werden, wird die Bildlaufleiste nicht auf der Registerkarte angezeigt, wenn die Anzahl der Funktionen größer ist als die Länge der Registerkarte mit Remote-Funktionen. NPR-17359
* Die API-Methode `com.adobe.icc.services.api.LetterInstanceService` zum Importieren funktioniert nicht. NPR-17922, NPR-16008
* Eine in einem Textbaustein hinzugefügte Variable ist während der Bearbeitung eines Briefes im Datenbindungsbedienfeld nicht sichtbar. NPR-17940
* Die Correspondence Management-Benutzeroberfläche wird nicht gestartet, wenn eine HTML-Übermittlungsaktion die POST-Methode verwendet. NPR-17595

**Forms Manager**

* Wenn ein für AB-Tests konfiguriertes adaptives Formular auf AB Testing starten klickt, wird der Test nicht gestartet und ein Browser-Konsolenfehler ausgegeben. NPR-17838

**Formular-Service**

* Die Fehler, die in der statischen Code-Analyse von OSGI-Formularen gemeldet wurden, sollten behoben sein. NPR-13951

#### JEE-Installationsprogramm von Forms {#forms-jee-installer-15}

**Ausgabe-Service**

* Die Verwendung AEM Forms 6.2 Output Service zum Zusammenführen eines bestimmten Formulars mit einer Daten-XML dauert 20 Mal länger. Es wurde jetzt in Windows- und Linux®-Umgebungen behoben. NPR-17501

**Installieren von LCM**

* Nach der Installation des AEM Forms 6.2 GM-Builds und der Anwendung des AEM 6.2 CFP zeigt LiveCycle Configuration Manager ein unerwünschtes Semikolon in den Versionsinformationen an und das Installationsdatum des Patches wird nicht aktualisiert. NPR-14322

**Prozessverwaltung**

* Die TaskContext-Variable wird für AEM Forms-Prozesse nicht gefüllt. CQ-4211857

#### AEM Forms JEE-Bundles-Paket {#aem-forms-jee-bundles-package}

* Die Funktionen der Formularbenutzer sollten unabhängig davon, ob sie die JEE Admin UI-Konsole oder die OSGi-Konsole verwenden, identisch sein. NPR-17670

### In CFP5 enthaltene Feature Packs {#feature-packs-included-in-cfp}

**Forms JEE-Paket**

Prozessverwaltung – HTML Workspace

* Beim Zuweisen eines Workspace-Schritts sollte auf der Registerkarte „Workspace-Anlagen“ ein Zähler für die Anlagen oder Notizen angezeigt werden, falls mehrere Anlagen oder Notizen vorhanden sind. NPR-17771
* Anfrage zur Unterstützung von Office 365 in AEM JEE Forms für E-Mail-Funktionen im Formular-Workflow. NPR-13866

**Forms-Add-on-Paket**

Korrespondenzverwaltung

* Beim Bearbeiten von Fragmenten im Texteditor während einer Briefvorschau sollte der verarbeitete Text anstelle der in Fragmenten verwendeten Inline-Bedingungen zur Bearbeitung angezeigt werden. NPR-15748, NPR-17504

### In CFP5 enthaltene OSGi-Bundles {#osgi-bundles-included-in-cfp-3}

Liste der in AEM 6.2 SP1-CFP5 aktualisierten OSGi-Bundles

[Datei laden](assets/do-not-localize/cfp5_osgi_bundles.txt)

Liste der in AEM 6.2 SP1-CFP5 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 wichtige kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Packs sind:

* Fehlerbehebungen in Assets für die Ausgabedarstellung von Camera Raw-Dateien, die Ansicht der Zeitleiste und die Bildausrichtung
* Verbesserungen in

   * WCM-Launches für Sites
   * Projekte-Workflow
   * ContextHub-Komponenten

* Fehlerbehebungen für Campaign, Mobile On-Demand und Übersetzung
* Verbesserungen der Benutzerfreundlichkeit im Regel-Editor für adaptive Formulare
* Erweiterter Editor für Inline-Bedingungen für die Korrespondenzverwaltung in Formularen
* Fehlerbehebungen bei Prozessverwaltung und Ausgabe-Service für AEM Forms on JEE
* Mit Forms Designer zusammenhängende Fehlerbehebung im Skript-Editor

### Plattform {#platform-12}

* Spalten zur **Assets OmniSearch** Ergebnisse durch Überlagerung in `/apps` funktioniert nicht. NPR-16737: Hotfix für CQ-4206785
* Die Seite **Diagnose-Tool** funktioniert nach einem direkten Upgrade von AEM 6.1 SP2 auf AEM 6.2 SP1 nicht. NPR-17121; Hotfix für CQ-4196786
* HTL: Beim Auswählen eines Forums und beim Erstellen eines Themas oder eines Beitrags wird durch `Sightly SightlyCompiledScript` eine falsche `addSelectors`-Eigenschaft zu `RequestDispatcherOption` hinzugefügt. NPR-17008: Hotfix für GRANITE-16384

* Unterstützung für `CRON expressions` in `ManagedPollConfigs` hinzugefügt, die von `ReportImporter` verwendet werden. NPR-16608: Hotfix-Anfrage für GRANITE-4206066

* Das Hochladen eines Avatar-Bildes für einen LDAP-Benutzer schlägt fehl. NPR-16561; Hotfix für Granite-17013
* Die Anzahl der Ergebnisse, die auf dem Bildschirm Benutzerverwaltung angezeigt werden, unterscheidet sich in der Karten- und Listenansicht. NPR-16241; Hotfix für GRANITE-16914
* Workflow-Benachrichtigungen werden beim Anzeigen im Google Chrome-Browser im Vollbildmodus nicht verzögert geladen. NPR-17013: Hotfix für CQ-4207567

### Assets {#assets-15}

* Die Bildausrichtung wird beim Importieren eines Bildes mit einer definierten Ausrichtung nicht korrekt angewendet. NPR-16750: Hotfix für CQ-4204356
* In der Ansicht „Assets-Zeitleiste“ wird kein Asset angezeigt, obwohl „Alle anzeigen“ standardmäßig festgelegt ist. NPR-16957: Hotfix für CQ-98780
* `Camera RAW`-Dateien (einschließlich ARW, CR2, NEF, DNG und EPS), die als Ausgabedarstellung in Assets hinzugefügt wurden, können nicht ausgewählt oder gelöscht werden. Diese Dateien werden automatisch heruntergeladen, wenn der Benutzer darauf klickt. NPR-16949: Hotfix für CQ-4206846
* Beim Erstellen einer PDF in einer anderen PDF in der Assets-Benutzeroberfläche werden die erstellten PDF nicht in der DAM-Benutzeroberfläche angezeigt. Die PDF sind jedoch im CRX-Repository sichtbar. NPR-16833: Hotfix für CQ-4206501
* Das Hochladen eines Assets als direkt untergeordneter Knoten mit der Touch-optimierten Benutzeroberfläche verursacht ein Problem. Das Asset wird als direkt untergeordnetes Element des zuvor ausgewählten Assets hochgeladen. NPR-16534: Hotfix für CQ-4204287
* In der DAM-Benutzeroberfläche wird beim Kommentieren eines Assets und beim Taggen eines Benutzers im Kommentar keine E-Mail-Benachrichtigung generiert. NPR-16589: Hotfix für CQ-102318

### Projekte {#projects-3}

Die Workflow-Konsole &quot;Projekte&quot;zeigt eine NullPointerException auf der Seite an, wenn Workflows bereinigt werden. NPR-17017: Hotfix für CQ-4194269

### Sites {#sites-15}

* Dateien im `ContextHub` werden in der Autoreninstanz nicht minimiert. NPR-17022: Hotfix für CQ-79456
* Die Launch-Promotion WCM-Launches benötigt eine lange Zeit, um einen Launch zu bewerben, der aus einer großen Baumstruktur einer Seite besteht. NPR-16480: Hotfix für CQ-82731
* `ClientContext`-Segment Condition Renderer stürzt ab, wenn ein Segment (oder eine Zielgruppe) mit einer nicht funktionierenden oder nicht abgeschlossenen Regel erstellt wird. NPR-16759: Hotfix für CQ-4205104
* In WCM Launches können Seiten, die mit einem Launch verknüpft sind, nicht depubliziert werden, wenn die Aktion über die Seiteneigenschaften in der Touch-Benutzeroberfläche initiiert wird. NPR-16560: Hotfix für CQ-4204681
* Link Rewriter schreibt fälschlicherweise href-Werte neu, die einen Doppelpunkt enthalten, in der Annahme, dass der Doppelpunkt „:“ einen JCR-Namespace definiert. NPR-16753: Hotfix für CQ-4203762
* Wenn Sie in WCM-Design Importer eine Test-Importtool-Seite öffnen und versuchen, eine ZIP-Datei hochzuladen, treten Probleme auf, wenn sie zuvor hochgeladen und gelöscht wurde. NPR-16486: Hotfix für CQ-90962
* Navigieren zum **[!UICONTROL Globale Navigation]** -Fenster mit Firefox- oder Google Chrome-Browsern bietet ein anderes Benutzererlebnis. Der Firefox-Browser zeigt die **[!UICONTROL Instrumente]** Menü. Der Google Chrome-Browser zeigt die **[!UICONTROL Navigation]** Menü. NPR-16770; Hotfix für CQ-4200456

### Campaign {#campaign}

* Beim Testen AEM Kampagnenvorlagen und Ändern von Testadressen, um &quot;Zusatzdaten&quot;einzuschließen, verschwindet die Dropdown-Liste Adobe Campaign auf dem Touch UI ContextHub. NPR-16771: Hotfix für CQ-105748

### Mobile On-Demand {#mobile-on-demand-3}

* Wenn Sie eine Veröffentlichung in AEM Autoreninstanz vorbereiten, verursacht eine Preflight-Aktion, die länger als fünf Sekunden dauert, eine ungewöhnliche Spitze im Dashboard AEMM - AEM PECS Integration Splunk mit einer hohen Anzahl von Statusanfragen. NPR-16908: Hotfix für CQ-4207055
* Die Konfigurationsverwaltung von AEM Mobile schlägt nach der Installation des Updates AEM-6.2-SP1-CFP1-1.0 fehl. NPR-16909: Hotfix für CQ-4204892

### Übersetzung {#translation-7}

* Die Vorschau von Übersetzungsaufträgen funktioniert nach der Installation von 6.2 SP1 - CFP1 nicht. NPR-16481; Hotfix für CQ-4204655
* Die mittels Übersetzung erstellte Sprachkopie verweist auf den Root-Primär statt auf die lokale Länder-LiveCopy. NPR-17257; Hotfix für CQ-4208287

### Sicherheit {#security-3}

* Es wird keine MIME-Typ-Validierung durchgeführt, wenn Binärdateien von Dateien in AEM hochgeladen werden. NPR-16617
* Probleme beim Hochladen von Avatar-Bildern für LDAP-Benutzer. NPR-16561

### Formulare {#forms-16}

#### Forms-Add-on-Paket {#forms-add-on-package-16}

**Adaptive Formulare**.

* Im adaptiven Forms-Editor sollte der Kommentar zur Zieleinstellung in head.jsp durch die neue ContextHub-Anweisung ersetzt werden. NPR-17173
* Im Regeleditor für adaptive Forms wird die **[!UICONTROL Element auswählen]** zeigt das Ereignis als &quot;null&quot;an. NPR-17139
* Das gesendete Formular wird erneut gesendet, indem Sie mit dem Pfeil nach vorne (>) nach vorne navigieren. NPR-17080
* Beim Senden eines adaptiven Formulars über AJAX wird die Rückruffunktion &quot;error&quot;nie aufgerufen, wenn ein Fehler aufgetreten ist. NPR-17034
* Wenn Sie im Regel-Editor zur Laufzeit auf die Schaltfläche **[!UICONTROL Formular speichern]** klicken, wird das Formular nicht gespeichert. NPR-16905
* Statischer Text sollte in adaptiven Formularen von der Tabulatorreihenfolge ausgeschlossen werden. NPR-16749
* Der berechnete Wert eines Dezimalfelds wird nicht korrekt angezeigt. NPR-16596
* Das Symbol zum Anzeigen des Hilfeinhalts sollte in adaptiven Formularen in der Tabulatorreihenfolge enthalten sein. NPR-16484
* Unterstützung für regulären Ausdruck des Typs `dataRef=C:/Users/`im **[!UICONTROL Standardkonfiguration für Vorbefüllungs-Dienst]**. Dieser Typ dient zum Vorbefüllen von Daten für adaptive Forms. NPR-16425

* Überprüfungen werden nicht korrekt für alle Bedienfelder ausgelöst, wenn ein verschachteltes Lazy-Loading-Szenario vorliegt. NPR-15821

**Korrespondenzverwaltung**

* Die Ausgabedarstellung von Briefen schlägt fehl, wenn ein Brief einen leeren Textbaustein (einen ohne Text) enthält. NPR-17054
* Zeilenumbrüche und Tabulator-Leerzeichen werden nach dem Einfügen im Text-Editor aus dem Inhalt entfernt. NPR-17039
* Die Anzeige von Verweisen eines Textbausteins dauert sehr lange, wenn der Textbaustein in vielen Briefen referenziert wird. NPR-17035
* Das Bearbeiten, Speichern, Löschen und Festlegen von Verweisen für Dokumentfragmente dauert sehr lange. NPR-17033
* Text mit Blocksatz wird bei der Vorschau des Briefes in einer anderen Schriftart dargestellt. NPR-16976
* Die Suchfunktion funktioniert nicht ordnungsgemäß, wenn der gesuchte Text mehrmals vorkommt. NPR-16920
* Die Symbolleiste des Text-Editors wird im Browser nur sporadisch angezeigt. NPR-16919
* Das Konstrukt **[!UICONTROL Formular speichern]** aus dem Regeleditor funktioniert nicht. NPR-16905
* Die Dropdown-Liste &quot;Schrift&quot;füllt die Schriftfamilie nicht beim Erstellen eines Textmoduls, das auf einem Datenwörterbuch mit Internet Explorer basiert. NPR-16944
* Nach dem Erstellen eines Textfragments ändert sich die Schriftart des Briefs bei der Briefvorschau. NPR-16830
* Briefe mit Tabulatorzeichen am Anfang oder zwischen Ausdrücken im Dokumentfragment können nicht gerendert oder in der Vorschau angezeigt werden. NPR-16769

**Mobile Forms**

* Die Vorschau für Mobile Forms zeigt überlappenden Inhalt an, obwohl das Formular für die PDF-Ausgabe korrekt angezeigt wird. NPR-17105

**Formularportal**

* Durch Klicken auf den **[!UICONTROL Download]**-Link für ein gesendetes Formular wird eine HTML-Seite anstelle eines PDF-Formulars geöffnet. NPR-17082

* `Upload Comments` für Dateianlagen werden nicht in der Benutzeroberfläche für gesendete Instanzen angezeigt, obwohl sie in der im CRX-Repository gespeicherten XML-Datei vorhanden sind. NPR-17075

**Reader Extensions-Service**

* Für eine bestimmte Datei wird bei der AEM Forms-OSGI-Installation die Reader-Erweiterung nicht eingerichtet. NPR-16625

#### JEE-Installationsprogramm von Forms {#forms-jee-installer-16}

**Core**

* Während des Aktualisierungsprozesses schlägt Configuration Manager mit einer Zeitüberschreitung fehl. NPR-16774 (Siehe [Konfigurieren der Zeitüberschreitung für Vorgänge auf Komponentenebene](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Prozessverwaltung – HTML Workspace**

* Der Startpunkt einer Startaufgabe beginnt nicht mit den Daten, die zum Zeitpunkt der Startpunktübermittlung gesendet werden. NPR-16917
* Durch Klicken auf die Schaltfläche **[!UICONTROL Zurück]** für ein Formular in HTML Workspace wird das Formular nicht geschlossen, sondern in die Gruppenwarteschlange zurückgestellt.
NPR-16352

**Prozessverwaltung**

* Benutzern erlauben, den Anzeigenamen früherer Aufgaben auf eine der nächsten Aufgaben in einer Prozessinstanz festzulegen. NPR-15382

**Ausgabe-Service**

* Output Service kann eine PDF nicht verarbeiten, die geändert wird, um ein zusätzliches &quot;millisec&quot;-Feld in die `date-time format` Metadaten. NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer-Skript-Editor berücksichtigt die Standardeinstellungen für Formulareigenschaften für `Calculate Event` und `Validate Event` nicht. NPR-15921

### In CFP4 enthaltene Feature Packs {#feature-packs-included-in-cfp-1}

**Forms-Add-on-Paket**

* Erweiterung im Editor für Inline-Bedingungen für die Korrespondenzverwaltung. NPR-10981

### In CFP4 enthaltene OSGi-Bundles {#osgi-bundles-included-in-cfp-4}

Liste der OSGi-Bundles, die zwischen AEM 6.2 SP1 und CFP4 aktualisiert wurden

Die wichtigsten Highlights von CFP3 sind:

* Effizientere Suchfunktion für die klassische Benutzeroberfläche und für die AEM-Suchkomponente unter Verwendung von Proxy mit Digest-Authentifizierung
* Fehlerbehebungen beim Hochladen von Assets und beim Anzeigen von Asset-Metadaten
* Behebt Probleme beim Erstellen von Ordnern und Verschieben von Seiten, wenn der Titel Sonderzeichen enthält.
* Fehlerbehebungen bei der Verwendung von Zielgruppen-Synchronisierungen, der Veröffentlichung von Kampagnen und der Auswahl der Zielmetrik in der Touch-optimierten Benutzeroberfläche
* Behebt Synchronisationsprobleme bei Übersetzungsvorgängen
* Bietet erhöhte Sicherheit für den Vorbefüllungs-Service von Forms.
* Verbesserungen der Entwurfs- und Übermittlungskomponente von Forms Portal und des Barcoded Forms-Dienstes
* Verbesserungen der Benutzerfreundlichkeit für adaptive Formulare, die Widgets für Dateianhänge oder Lazy Loading-Fragmente enthalten.
* Verbesserungen der Benutzerfreundlichkeit in der Korrespondenzverwaltung, einschließlich verbesserter Suchfunktion, Protokollierung gelöschter Assets und Importierung von Datenwörterbüchern.

### Plattform {#platform-13}

* Eine Race-Bedingung in der **ModelAdapterFactory**, die auftreten kann, wenn zwei Threads versuchen, dasselbe Feld zu injizieren, führt zu einem Fehler bei der Modellerstellung. NPR-16443: Hotfix für SLING-6584
* Validierungsoption in Package Manager, um Konflikte zwischen überlagerter Datei (JSP- oder JavaScript-Datei) unter `/apps` und die , die in einem Hotfix unter `/libs`. Betroffene Überlagerungen können dann neu erstellt werden, um Änderungen aus der Datei unter einzubeziehen. `/libs`. NPR-16216: Hotfix für CQ-81729
* Die Protokollierung in „error.log“ stoppt manchmal einige Sekunden nach dem Starten von Publisher und muss gelöscht werden, um erneut ausgeführt zu werden. Anfrage zur Aktualisierung des Logging-Frameworks und Bereitstellung der Sling-Protokollierung. NPR-15913: Hotfix für Granite-15452
* Anfrage zur Aktualisierung der JavaScript &quot;`use"`-API, um Fehler bei der Implementierung der HTL JavaScript Use-API zu vermeiden. NPR-16461: Hotfix für SLING-6780

### Sites {#sites-16}

* Nach der Aktualisierung von AEM 6.0 auf AEM 6.2 zeigt die klassische Benutzeroberfläche aufgrund zahlreicher Abfragen eine langsame Leistung bei der Suche nach Tags. Um das Problem zu beheben, führen Sie die unter [Deaktivieren des Replikationsstatus in der Tagging-Konsole (klassische Benutzeroberfläche)](#disable-replication-status-in-tagging-console-classic-ui-npr) kann befolgt werden. NPR-15842: Hotfix für CQ-4201748.

* Beim Erstellen einer Seite in der Touch-Benutzeroberfläche wird bei der Eingabe für das Feld &quot;Name&quot;das Sonderzeichen &quot;Apostroph&quot;nicht geprüft (wie in der klassischen Benutzeroberfläche). Daher kann die Seite nicht verschoben werden. NPR-16404: Hotfix für CQ-4205321.
* Durch Anwenden verschiedener Stile auf zwei Zeilen im Rich-Text-Editor und anschließendes Zusammenführen werden die auf die zweite Zeile angewendeten Stile entfernt. NPR-16389: Hotfix für CQ-4203835.
* Der Versuch, eine Seite in eine Seite ohne Unterseiten einzufügen, funktioniert im Bildschirm &quot;Websites der Touch-optimierten Benutzeroberfläche&quot;nicht, da die Schaltfläche &quot;Einfügen&quot;nicht verfügbar ist. NPR-15894: Hotfix für CQ-4201696.
* Beim Scrollen der Registerkarte &quot;Seiten&quot;im Bereich &quot;Inhaltssuche&quot;werden einige Seitensätze in der klassischen Benutzeroberfläche auf unbestimmte Zeit angezeigt, während in der Touch-Benutzeroberfläche nur wenige nicht wiederholende Seiten angezeigt werden. NPR-16271: Hotfix für CQ-4202371
* Durch Öffnen der Seiteneigenschaften einer Live Copy in der Touch-optimierten Benutzeroberfläche und Klicken auf „Speichern“, ohne dass Änderungen vorgenommen wurden, werden alle LiveCopy-Registerkarten überschrieben und ein LiveSync-Konfigurationsknoten erstellt. NPR-16327: Hotfix für CQ-108562
* Die Formularbeschränkung kann die `ConstraintMessage`-Eigenschaft nicht lesen. NPR-16388: Hotfix für CQ-101330
* Die Komponente `wcm/foundation/components/parsys` zeigt den Platzhalter **[!UICONTROL Komponenten hierher ziehen]** nicht an. NPR-16748: Hotfix für CQ-4205187

### Assets {#assets-16}

* Der PDF-Rasterassistent funktioniert nicht mehr und verursacht Probleme mit dem Arbeitsspeicher nach der Installation von 6.2 SP1 oder Hotfix 12430. NPR-15991
* In den Metadaten für eine Zeichenfolgeneigenschaft wird `documentNumber` als Datum angezeigt, es sollte sich jedoch um eine Zahl handeln. NPR-16134: Hotfix für GRANITE-16916
* Textabschneidungen in Ereignisblasen in der Zeitleiste. NPR-16226: Hotfix für CQ-85226
* Wenn ein Ordner unter der Inhaltshierarchie mit einem Titel erstellt wird, der Sonderzeichen enthält, wird die kodierte Version dieser Zeichen angezeigt. NPR-15935: Hotfix für CQ-4202987
* Der Benutzer kann keine Assets hochladen oder Ordner erstellen, während er durch Assets navigiert. Dies liegt an einem inkonsistenten Verhalten, das bei Verwendung der Schaltfläche &quot;Erstellen&quot;angezeigt wird. NPR-16410: Hotfix für CQ-4204793
* Beim Hochladen freigegebener HTML-Ressourcen aus der Artikelansicht im AEM-Authoring treten unerwartete Fehler auf. NPR-16133: Hotfix für AEMM-4155970

### Integration {#integration-14}

* Wenn Sie die Proxy-Authentifizierung mit der Digest-Authentifizierung aktivieren, gibt die AEM-Suchkomponente eine ConcurrentModificationException aus. NPR-15309: Hotfix für CQ-4199191
* Beim Erstellen einer Target-A/B-Test-Aktivität in AEM synchronisiert die Zielgruppe nicht mit Target und zeigt &quot;keine Zielgruppen&quot;. NPR-16229: Hotfix für CQ-4204210
* Nach der Installation von SP1+NPR-11577 v1.2 wird die Dropdown-Liste der Metriken nie geladen, wenn Sie beim Targeting in der Touch-optimierten Benutzeroberfläche die Option „Analytics-Metrik verwenden“ für die Zielmetrik auswählen. NPR-16129: Hotfix für CQ-4204316
* Bei Verwendung der Zielgruppenbestimmung wird bei der Veröffentlichung der Kampagne nicht automatisch der gesamte Baum einschließlich der Marke und des Hauptteils veröffentlicht. NPR-15855: Hotfix für CQ-94630

### Übersetzung {#translation-8}

* Der Synchronisierungsübersetzungsauftrag wird jetzt automatisch ausgelöst und AEM Abruf erfolgt jetzt, ohne die Übersetzungsprojekte abzufragen. NPR-15163: Hotfix für CQ-90856

### Formulare {#forms-17}

#### Forms-Add-on-Paket {#forms-add-on-package-17}

**Adaptive Formulare**.

* Beim Speichern eines adaptiven Formulars mit einem Anhang wird der vollständige Pfad des Anhangs zum `fileAttachment` -Tag der generierten XML statt des Namens des Anhangs. NPR-16529
* In XDP-basierten adaptiven Formularen ist der `afData/afBoundData`-Wrapper in der gesendeten XML vorhanden, auch wenn die XML zum Vorausfüllen keine `afData/afBoundData`-Wrapper aufweist. NPR-16118

* Exponentialschreibweise im Feld „Zahl“: Wenn bei der Verwendung adaptiver Formulare eine Zahl mit einem Dezimalbruch eingegeben wird, der insgesamt mehr als zehn Zeichen umfasst, wird die Zahl im übermittelten XML in Exponentialschreibweise umgewandelt. NPR-16106
* Bei Formularen, die sowohl eine Dateianlagenkomponente als auch ein Lazy Loading-Fragment enthalten, enthält die XML-Datei für die gesendeten Daten keine Informationen für die Dateianlagenkomponente. NPR-16022
* Bei einem wiederholbaren Lazy Loading-Bedienfeld, das keinen wiederholbaren Vorgänger hat, können sich wiederholbare untergeordnete Elemente in einer zweiten Instanz des Bedienfelds nicht wiederholen. NPR-15944
* Beim Versuch, ein Fragment in einem Fragment im Formulareditor zu speichern, füllt der Fragmentmodellstamm den Wert des untergeordneten Fragments nicht. NPR-15943
* Beim Erstellen eines Kontrollkästchens mit nur einem Element und beim Anzeigen des Kontrollkästchentitels wird bei der Aktion zum Erstellen eines Wörterbuchs eine `ArrayIndexOutOfBoundException` zurückgegeben, wenn der Text des Elements leer ist. Das Wörterbuch wird nicht erstellt und es wird kein Fehler auf dem Bildschirm generiert. NPR-15816
* Bei adaptiven Formularen mit Widgets für Dateianhänge werden einige Teile des Formulars deaktiviert, nachdem die angehängte Datei in der Vorschau angezeigt wurde.
NPR-16611

* Bei Dateianhang-Widgets, die mehrere Anhänge zulassen, führt das Senden einer neuen Formularinstanz mit einer Anlage auf einem Widget, das bereits über einen vorherigen Anhang verfügt, zu einem angezeigten Fehlercode. Dieser Fehler tritt beim Öffnen des hinzugefügten Anhangs anstelle des tatsächlichen Inhalts auf. NPR-16258
* Sichern des Formularvorbefüllungs-Service vor unbefugtem Zugriff durch Protokolle wie `file://`, `http://` und `ftp://`. Siehe [Konfigurieren des Vorbefüllungs-Dienstes mithilfe von Configuration Manager](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15414

* Fordern Sie im Überprüfungsschritt an, das adaptive Formular im PDF-Format anstatt im HTML-Format wiederzugeben, und hängen Sie alle Anlagen an die PDF an, damit der Ausdruck das vollständige Formular anzeigt. NPR-9011

**Korrespondenzverwaltung**

* Beim Arbeiten mit Textfragmenten in einem Brief im Vorschau- oder Bearbeitungsmodus schlägt die Funktionalität der ganzen Briefe fehl, wenn Text in eine Liste konvertiert wird. Außerdem wird ein JavaScript-Fehler erzeugt. NPR-16460
* Der Import einer XSD-Datei zum Erstellen eines Datenwörterbuchs im Knoten Correspondence Management schlägt fehl, da der Browser bei jedem Hochladen der XSD-Datei und bei Auswahl des Stammknotens nicht mehr reagiert. Dieses Problem ist Browser-unabhängig und wird nicht in Serverprotokollen angezeigt. NPR-16452
* Während der Vorschau eines Briefs mit dem Internet Explorer-Browser und dem Versuch, die Schriftgröße des Inhalts zu bearbeiten, werden in der Dropdown-Liste für die Schriftgröße doppelte Werte von 8 bis 72 angezeigt. NPR-16387
* Wenn ein schwebendes Feld als Eingabefeld aus einem XDP-Fragment angezeigt wird, wird das Feld in der Briefvorschau bei Verwendung des Internet Explorer-Browsers nicht erweitert. NPR-16367
* Beim Versuch, einen Brief direkt von der Vorschau zu senden, wird das Popup für den Briefnamen nicht korrekt angezeigt, da er ausgeblendet ist. NPR-16353
* Zeilenabstände, die beim Bearbeiten eines Briefes hinzugefügt werden, werden im Vorschaufenster nicht angezeigt. Bei Listen in Textfragmenten zeigt die PDF-Ausgabe nicht den richtigen Abstand an. NPR-16267
* Beim Bearbeiten eines Textdokumentfragments mit dem Internet Explorer-Browser schlägt der Versuch, einen Einzug in den Text bereitzustellen, fehl, da der Cursor keinen Texteinzug zulässt. NPR-16128
* Das Hinzufügen oder Ändern eines Datenwörterbuchs zu einem vorhandenen Textdokumentfragment dauert viel Zeit und der Benutzer wird nicht immer benachrichtigt. NPR-16102
* Bei der Vorschau eines Briefs mit bildlauffähigem Inhalt mit dem Internet Explorer-Browser überschneidet sich die Bildlaufleiste des Browsers mit der Bildlaufleiste des Briefs. Daher kann für Fragmente auf der rechten Seite nicht der gesamte Inhalt angezeigt werden. NPR-16068
* Beim Erstellen oder Bearbeiten von Textdokumentfragmenten mit dem Google Chrome-Browser wird das Dropdown-Menü für die Farbauswahl automatisch angezeigt und kann nicht entfernt werden. Der Benutzer muss die Liste als Typ des Dateneintrags auswählen, damit er das Fragment bearbeiten kann. NPR-16067
* Bei Verwendung der `Letterinstance`-API funktioniert die `import com.adobe.icc.services.api.LetterInstanceService`-Methode nicht. NPR-16008
* Das Ändern der Datumsanzeigeformate auf `locale=en_US; dateFormat=MMM dd,yyyy;` in der Asset Composer-Konfiguration funktioniert nicht wie erwartet und das Datumsformat wird als fehlerhafte Zeichen angezeigt. NPR-16007
* Die Art der Datenverknüpfung in Briefen während der Neuerstellung wird als &quot;Benutzer&quot;angezeigt, auch wenn sie zuvor anders festgelegt wurde. NPR-16619

**Formularportal**

* Die Aktualisierungsszenarien für Entwurfs- und Übermittlungskomponenten funktionieren mit dem Datenbankimplementierungsbeispiel nicht. NPR-16752

**Barcoded Forms Service (BCF)**

* Die statische Code-Analyse von Barcoded Forms Service (BCF) meldet Probleme. NPR-13855

#### JEE-Installationsprogramm von Forms {#forms-jee-installer-17}

**Prozessverwaltung – HTML Workspace**

* Sichern des Vorbefüllungs-Dienstes für Formulare vor unbefugtem Zugriff über Protokolle wie &quot;file://&quot;, &quot;http://&quot;und &quot;ftp://&quot;. Weitere Informationen finden Sie unter [Konfigurieren des Vorbefüllungs-Dienstes mit Configuration Manager](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15434

**Benutzerverwaltung**

* Der SAML-Anmeldebildschirm zeigt eine falsche Version (6.1.0) des AEM 6.2-Servers an. NPR-13825
* Wenn AEM Forms für die Single-Sign-on (Kerberos)-Authentifizierung konfiguriert ist und die Benutzerauthentifizierung bei der Anmeldung fehlschlägt, wird der Fehler-Code „404“ zurückgegeben. Der Benutzer wird erst nach dem Aktualisieren der Seite zur Anmelde-Site weitergeleitet. NPR-15015

#### Forms Designer {#forms-designer-1}

* Das Ändern des Gebietsschemas des Formulars auf Französisch (Kanada) in der Rechtschreibprüfung des Wörterbuchs funktioniert in AEM Forms Designer nicht.
NPR-15896

### In CFP3 enthaltene Feature Packs {#feature-packs-included-in-cfp-2}

**Forms-Add-on-Paket**

* Beim Löschen eines Assets in Correspondence Management sollte eine Warnmeldung in der Datei error.log protokolliert werden. NPR-13225
* Verbessern Sie die Suchfunktion bei der Vorschau eines Briefs in Correspondence Management, um die Suche nach Text im Textfragmentinhalt zu aktivieren, anstatt nur den Brieftitel oder die Beschriftung zu durchsuchen. NPR-16103

### In CFP3 enthaltene OSGi-Bundles {#osgi-bundles-included-in-cfp-5}

Liste der OSGi-Bundles, die zwischen AEM 6.2 SP1 und CFP3 aktualisiert wurden

[Datei abrufen](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt).
Die wichtigsten Highlights von Cumulative Fix Pack 2 sind:

* Stabilitäts- und Leistungsverbesserungen in der AEM-Plattform, einschließlich Sling-Framework und -Betrieb
* Verbesserte Asset-Verwaltung mit mehreren Korrekturen für den Zugriff auf, das Verschieben, Suchen, Hochladen und Veröffentlichen von Assets
* Verbessertes Authoring und Management von Sites mit Fehlerbehebungen in Inhaltsfragmenten, Anker-Plug-in, Bildschirmpräsentation und ContextHub-Komponenten
* Mehrere Fehlerbehebungen in der Touch-optimierten Benutzeroberfläche, einschließlich Text-Editor, Omnisearch und Variantenerstellungsprozess
* Verbesserte Workflows; erweiterter Microsoft®-Connector für die Verwendung neuer Übersetzungs-APIs für das Azure-Portal
* Fehlerbehebungen in Projekten und Campaign
* Verbessertes Authoring und Management mit Fehlerbehebungen in den Funktionen für adaptive Formulare, Korrespondenzverwaltung und Formularportal
* Fehlerbehebungen in Forms JEE-Kern-, XTG- und HTML Workspace-Komponenten

### Plattform {#platform-14}

* Der `SlingPostProcessor` wird ausgelöst, wenn die Seite, die direkt auf das Sling-Framework verweist, bearbeitet wird. NPR-15754: Hotfix für CQ-104153

* Der Wert für Tags mit dem `tagBasePath` -Eigenschaft wird beim Navigieren zu einer Seitenkomponente nicht im Dialogfeld Klassische Benutzeroberfläche abgerufen. NPR-15543: Hotfix für CQ-4199950

* Wenn Sie während der Ausführung von Sling-Vorgängen einen Block mit dem Namen „chunk_n_n-1“ haben, läuft `SlingFileUpload handler.getLastChunk` in eine Endlosschleife mit leeren Blöcken. NPR-15455: Hotfix für SLING-5701

* Wenn eine Schnittstelle eine andere Schnittstelle erweitert, werden die injizierbaren Methoden der Superschnittstelle nicht korrekt injiziert. NPR-15202: Hotfix für SLING-5710
* Bei Verwendung des Funktionsaufrufs `com.adobe.granite.infocollector.impl.FilesTraversal` wird eine potenzielle Null-Zeiger-Ausnahme nicht verhindert. NPR-15169; Hotfix für CQ-4197640
* Der Workflow-Status ist für einige sekundäre Knoten inkonsistent und es wird ein Fehler beim Versenden von Beobachtungsereignissen für diesen Knoten angezeigt. NPR-15701: Hotfix für GRANITE-13786
* Ein Benutzer wählt einen Knoten in CRXDE aus (zum Beispiel `/content/dam/`). Klicken Sie dann auf die Registerkarte &quot;Zugriffssteuerung&quot;, um sicherzustellen, dass eine Zugriffssteuerungsliste vorhanden ist. Beim Ziehen und Ablegen einiger Elemente werden die Elemente verschoben, nicht das ausgewählte. NPR-15696; Hotfix für GRANITE-16300
* Die Auswahl eines Benutzers aus der Dropdown-Liste, um für ihn stellvertretend zu agieren, lässt das gesamte Benutzer-Pop-up verschwinden. NPR-15774: Hotfix für CQ-4201738/GRANITE-11895
* In Omnisearch funktioniert die Suche nach Tags mit automatisch ausgefüllten Vorschlägen nicht. NPR-15088: Hotfix für GRANITE-14426.
Hinweis: Für diese Fehlerbehebung ist Oak CFP 1.4.11 oder höher erforderlich.

### Mobile AEM Author {#mobile-aem-author}

* Wenn Sie AEM Mobile- und ContentSync-Pakete mit einem Hybrid-Programm verwenden, antwortet AEM auf eine Abrufanforderung (mit Zeitstempeln) des Programms mit dem ältesten Paket statt mit dem vom Programm angeforderten Paket. NPR-15749: Hotfix für CQ-104153

### Sites {#sites-17}

* Der Änderungsstatus für den Workflow-Posteingang im WCM-Core ändert sich nicht, wenn ein Benutzer eine Seite nach der Aktivierung eines Workflows ändert. NPR-15684: Hotfix für CQ-4196974
* Das Anker-Plug-in im Rich-Text-Editor für die Touch-Benutzeroberfläche generiert nicht kompatible HTML 5, wenn der Benutzer auf das Ankersymbol klickt und einen Namen hinzufügt. Es sollte ein id-Attribut anstelle eines name-Attributs im HTML5-Tag für das Ankerelement hinzufügen. NPR-15650: Hotfix für CQ-89782
* Wenn ein Metadatenschema mit zahlreichen Feldern erstellt und auf die Metadaten des Inhaltsfragments angewendet wird, wird keine Bildlaufleiste auf dem Metadatenbildschirm des Inhaltsfragments erstellt, sodass die Felder nicht bearbeitet werden können. NPR-15478: Hotfix für CQ-4202622
* Beim Bearbeiten der Feldkomponente `TagInput` werden die zuvor konfigurierten Werte für die Dialogfelder nicht angezeigt. NPR-15464: Hotfix für CQ-4200360

* Wenn in der Benutzeroberfläche des Inhaltsfragment-Editors Varianten eines Inhaltsfragments erstellt werden, zeigt das seitliche Bedienfeld nicht die Bildlaufleiste an, um durch alle Varianten zu navigieren. NPR-15445: Hotfix für CQ-4199444
* Wenn Benutzer aus direkten Gruppen entfernt werden, werden sie zu geerbten Gruppen hinzugefügt. NPR-15400: Hotfix für CQ-98758
* WCM-Authoring: Die Touch-optimierte Benutzeroberfläche für Autoren erlaubt keine Bearbeitung von Seiten, die Kommas im Namen haben. NPR-15396: Hotfix für CQ-4199723
* Bei der Verwendung der Touch-optimierte Benutzeroberfläche zum Authoring übergibt die Funktion `Granite.author.editableHelper.doSelectParent` Argumente in der falschen Reihenfolge, was zu einem JavaScript-Fehler führt. NPR-15349: Hotfix für CQ-4198594
* Das ContextHub-Segment zeigt das Erlebnis auch dann an, wenn das Opt-out-Cookie vorhanden ist. NPR-15293: Hotfix für CQ-4198024
* Die Bildschirmpräsentationskomponente in der klassischen Benutzeroberfläche kann keine Folien erstellen oder Bilder per Drag-and-Drop verschieben, um neue Folien zu erstellen. NPR-15281: Hotfix für CQ-4194164
* Unabhängig von der Berechtigung werden Benutzenden die Menüoptionen „Erstellen“ wie „Seite erstellen“, „Site erstellen“, „Live Copy erstellen“, „Launch erstellen“ und „Katalog erstellen“ in der Site Admin Console angezeigt. NPR-15278: Hotfix für CQ-94436
* Nach der Installation von AEM 6.2 Service Pack 1 funktioniert der Regler „Unterseiten einschließen“ nicht mehr bei Seitenaufrufen. NPR-15230: Hotfix für CQ-4198449
* Anfrage, die Versionsbereinigung zu verbessern, um Versionen in Blöcken abzurufen und zu verarbeiten und in der Lage zu sein, einen angegebenen Pfad in einer XPath-Abfrage zu verwenden. NPR-15186: Hotfix für CQ-109205
* Die Schaltfläche Löschen fehlt auf der Registerkarte Miniaturansicht der Seiteneigenschaften in der Komponente Sites . NPR-15143; Hotfix für CQ-4196997
* Bei einer Site, die Live Copies verwendet, zeigt das Kontrollkästchen &quot;Live Copy&quot;im Spaltenbereich der Site-Admin Console den Live Copy-Status nicht richtig an und nur das HTML-Markup wird angezeigt. NPR-15108: Hotfix für CQ-97086
* Wenn der Benutzer beim Bearbeiten von Inhaltsfragmenten zur Bearbeitung auf „Fertig“ („√“) klickt, bevor er die Antwort des Beitrags erhält, wird der bearbeitete Inhalt nicht korrekt gespeichert. NPR-15014: Hotfix für CQ-4194095
* Wenn Sie die Seite &quot;Bearbeiten&quot;während des Timewarp-Modus schließen und versuchen, sie erneut vom Site-Administrator zu öffnen, wird ein Fehler mit dem Status angezeigt `500`. NPR-14965: Hotfix für CQ-109647:
* In der Benutzeroberfläche von Digital Asset Manager (DAM) führt die Suche nach Autorisierungen bei der Benutzerauswahl zu einer Ausnahme vom Typ „Unzureichender Speicher“. NPR-15307: Hotfix für CQ-98542

### Assets {#assets-17}

* Nach der Suche nach einem Asset in Omnisearch, der Auswahl eines Assets und dem Versuch, Eigenschaften zu bearbeiten, klicken Sie auf **Eigenschaften anzeigen**, dann die **Speichern** -Schaltfläche leitet Benutzer zu einer leeren Seite weiter. NPR-15900: Hotfix für CQ-4202372
* Die Assets- Benutzeroberfläche reagiert nicht auf Ereignisse. Das Auswählen eines Assets und Klicken auf „Veröffentlichen“ oder „Ausgabedarstellungen“ führt zu keiner Aktivität. NPR-15828: Hotfix für CQ-4202247
* Beim Veröffentlichen eines Assets in der Kartenansicht wird die Karte nicht mit einem veröffentlichten Status aktualisiert. Stattdessen wird die Seite aktualisiert. NPR-15826: Hotfix für CQ-102732
* Kumulativer Hotfix mit Hotfixes für Assets. NPR-15225
* Wenn ein kaufmännisches Und-Zeichen (&#39;&amp;&#39;) im Namen eines Asset-Ordners enthalten ist, wird der Ordnername beim Navigieren zum Asset nicht korrekt angezeigt. NPR-15775: Hotfix für CQ-4201735
* Die Verwendung von kaufmännischem Und („&amp;“) im Namen einer Asset-Datei verursacht Probleme beim Zugriff auf ihre Eigenschaften. NPR-15770: Hotfix für CQ-4201737
* Wenn der Benutzer beim Navigieren in Assets und im Anzeigemodus &quot;Spaltenansicht&quot;die Seite aktualisiert, nachdem er ein Asset ausgewählt und geklickt hat, werden die Asset-Details anstelle des aktualisierten Inhalts angezeigt. NPR-15768: Hotfix für CQ-4201727
* Die PDS-Aufnahme beansprucht 100 % CPU-Auslastung mit einem Heap von Bibliotheken für PDF-Services. NPR-15606; Hotfix für GRANITE-12929
* Wenn Sie mit dem Firefox-Browser auf die Benutzeroberfläche &quot;Meine Linkfreigabe&quot;zugreifen, werden die freigegebenen Elemente oder Benutzer nicht angezeigt und der Bildschirm ist nicht verwendbar. NPR-15539: Hotfix für CQ-4200992
* Wenn bei der Verwendung von Digital Asset Manager eine Seite mit einem Bildsatz verknüpft ist, wird die Seitenzuordnung durch Verschieben der Bilder in einen neuen Ordner unterbrochen. Daher fehlen auf der verknüpften Seite einige der Bilder. NPR-15538: Hotfix für CQ-111479
* In der Dam Viewer-Komponente führt die Verwendung des Ausführungsmodus „nosamplecontent“ zu Fehlern bei Dynamic Media. NPR-15449: Hotfix für CQ-4195425
* Wenn beim Erstellen von Videoprofilen sowohl eine Voreinstellung für die Videokodierung in hoher als auch in mittlerer Qualität ausgewählt wird, werden die vorgenommenen Änderungen nicht gespeichert. NPR-15447: Hotfix für CQ-4195482
* Auch wenn das Hochladen eines Assets in das Brand Portal aufgrund eines Server-Fehlers fehlschlägt, wird der Status auf der Brand Portal-Benutzeroberfläche auf „Veröffentlicht“ aktualisiert, wodurch es schwierig wird, die fehlende Datei zu verfolgen. NPR-15442: Hotfix für CQ-4197968
* Beim Veröffentlichen eines Asset-Ordners in Brand Portal, dessen Veröffentlichung mehr als eine Stunde dauert, können einige Dateien nicht veröffentlicht werden. NPR-15441: Hotfix für CQ-4199493
* Bei Verwendung der Asset Finder-Konsole in der Spaltenansicht schlägt der Versuch, einen Ordner zu erstellen, fehl, obwohl es bei einem erneuten Versuch erfolgreich war. NPR-15370: Hotfix für CQ-4199448
* Wenn ein in der DAM-Benutzeroberfläche ausgewähltes Asset oder Ordner im Namen ein Komma enthält, ist die Registerkarte &quot;Verweise&quot;nicht verfügbar und zeigt die Meldung &quot;Liste der Verweise ist nicht für mehrere Auswahlen verfügbar&quot;an. NPR-15362: Hotfix für CQ-4199721
* Beim Veröffentlichen eines Ordners in Brand Portal wird der Status „Veröffentlicht“ des Ordners nicht geändert, auch wenn die Assets im Ordner erfolgreich veröffentlicht wurden. NPR-15292: Hotfix für CQ-4197667
* Beim Navigieren zur Assets-Konsole in der Touch-optimierten Benutzeroberfläche wird beim Aktivieren bestimmter Assets eine Ausnahme angezeigt. NPR-15217: Hotfix für CQ-108779
* Veröffentlichen eines Videos auf YouTube, wenn die Verbindung über einen Proxy-Server erfolgt. NPR-15109: Hotfix für CQ-110332
* Die Verwendung eines Assets mit einem Namen, der einen Punkt (.) in data-sly-resource enthält, wird nicht in dasselbe Asset aufgelöst, und der Ausgabepfad wird am Punkt beendet. NPR-15069: Hotfix für CQ-4195914
* Nach der Aktualisierung von AEM 6.2 auf Service Pack 1 schlägt die Synchronisation von Assets in Scene7 fehl. Die Eigenschaft `dam:Scene7FileStatus` zeigt den Status `UploadFailed` auch für veröffentlichte Assets an. NPR-15269: Hotfix für CQ-4197708

### Benutzeroberfläche {#user-interface-5}

* In **[!UICONTROL Touch-Benutzeroberfläche]**, wird das gespeicherte Datum für Datumsfelder angezeigt, die jetzt den Typ=&#39;datetime&#39; aufweisen, während Internet Chrome Browser Version 56.0.2924.87 verwendet wird. NPR-15383: Hotfix für GRANITE-16481
* In der **[!UICONTROL Touch-optimierten Benutzeroberfläche]** entfernt der Rich-Text-Editor den Thread und die Beschriftungselemente während der Wiedergabe aus den HTML-Tabellen. NPR-15267: Hotfix für CRTE-41
* `FileUpload Validator` behandelt keine Fälle, in denen „autostart“ „true“ ist oder `uploadFile()` manuell aufgerufen wird, und generiert in diesen Fällen einen ungültigen Überprüfungsbericht. NPR-15295: Hotfix für GRANITE-13499

* Omnisearch erlaubt Kunden nicht, die `/apps` , um eine Spaltendatenquelle hinzuzufügen, da davon ausgegangen wird, dass die Standortkonfiguration unter */libs/granite/omnisearch/content/metadata/*. NPR-13188; Hotfix für GRANITE-16479
* Bei Verwendung der **[!UICONTROL Touch-optimierten Benutzeroberfläche]** werden Produktvarianten nicht auf derselben Ebene wie das Produkt erstellt. Der Benutzer wird nicht über den Status der Variantenerstellung informiert. NPR-15345: Hotfix für CQ-4198948

**Scene7**

* Die Ausführung des Scene7-Workflows führt zu geöffneten Dateien, die nicht geschlossen werden. Anfrage zur Verbesserung des AEM-S7-Diensts, damit eine einzelne HttpClient-Instanz mit freigegebener Pooling-Konfiguration verwaltet und wiederverwendet wird. NPR-15357: Hotfix für CQ-109958

### Übersetzung {#translation-9}

* Bei der Verwendung von Übersetzungsprojekten führt die Aktualisierung von Sprachkopien vom englischen Primär zu 11 separaten Launches, die alle denselben Namen und denselben Quell-Stamm aufweisen. Sie haben jedoch jeweils etwas unterschiedliche Launch-Stämme, falls der Seitenname einem bestimmten Muster folgt. NPR-15605: Hotfix für CQ-4200699
* Übersetzungsprojekte werden nicht für Seiten erstellt, deren sprachliche Root Bindestriche und Gedankenstriche im Namen haben. NPR-15171: Hotfix für CQ-96286
* Anfrage, den Microsoft®-Connector zu aktualisieren, um die Microsoft® Translator-APIs verwenden zu können, die Microsoft® im Azure-Portal zur Verfügung stellt. NPR-15320: Hotfix für CQ-101010

### Projekte {#projects-4}

* Im Projektbildschirm sind nur 20 inaktive Projekte sichtbar, obwohl mehr als 20 inaktive Projekte im Repository vorhanden sind. NPR-15656: Hotfix für CQ-4200903

### Campaign {#campaign-1}

* Bei Verwendung von Campaign - Targeting und `MAC` - Test- und Target-Integrationskomponenten: Durch die Aufhebung der Veröffentlichung von Aktivitäten wird der Aktivitätsstatus in der Primären Benutzeroberfläche nicht aktualisiert. NPR-15401: Hotfix für CQ-4199839
* Beim Verschieben eines Produkts in AEM Commerce fehlen dem Produktverschiebungsassistenten die vorab ausgefüllten Werte für den Produktnamen, den Titel, die referenzierten Seiten, den Erstellungsautor und das Erstellungsdatum. NPR-15228: Hotfix für CQ-98617

### Sicherheit {#security-4}

* CSRF-Token-Parameter wurde Formularen mit einer GET-Methode hinzugefügt. NPR-15229

### Formulare {#forms-18}

#### Forms-Add-on-Paket {#forms-add-on-package-18}

`**Adaptive Forms**`

* Standardwerte werden beim Vorausfüllen des adaptiven Formulars mit Eingabe-XML durch leere Werte in XML überschrieben. NPR-15721
* Die `afData/afBoundData` Der Wrapper ist in der gesendeten XML vorhanden, obwohl die XML zum Vorbefüllen nicht `afData/afBoundData` Wrapper in XML-schemabasierten adaptiven Formularen. NPR-15541

* Die Titel in der Accordion-Leiste sollten bearbeitbare HTML-Überschriften des Typs „h2“ anstelle des Tags „a“ sein. NPR-15475
* Das Accordion-Layout eines Formularbedienfelds ist für Benutzer von Bildschirmlesehilfen nicht verfügbar. Benutzer können nicht allein mit der Bildschirmlesehilfe-Software wie JAWS oder NVDA zur Accordion-Registerkarte navigieren. NPR-15474

`**Correspondence Management**`

* Das Speichern, Löschen und Festlegen von Verweisen für Dokumentfragmente dauert sehr lange. NPR-15939
* Die Registerkartenausrichtung, die in „Assets verwalten“ für Text mit mehreren Überschriften festgelegt wurde, schlägt in der CCR-Benutzeroberfläche fehl. NPR-15818
* Miniaturansichten von Textbausteinen zeigen keine ausgerichteten Inhalte an, obwohl der Text ausgerichtete Inhalte enthält, die mit Registerkarten in Google Chrome erstellt wurden. NPR-15819

`**Forms Portal**`

* Der Vorbefüllungs-Dienst funktioniert nicht für XDP Forms. NPR-15466
* Beim Speichern von Entwürfen und Übermittlungen adaptiver Formulare in der Datenbank wird der Status des adaptiven Formulars beschädigt, wenn die Datenbankverbindung aus irgendeinem Grund fehlschlägt (z. B. nach einer langen Inaktivität). NPR-15297

#### JEE-Installationsprogramm von Forms {#forms-jee-installer-18}

`**Core**`

* Nach der Aktualisierung auf die neueste Version von Java™ 1.8.0_121-b13 ist die Admin-Benutzeroberfläche in AEM Forms nicht verfügbar. NPR-15330

`**XTG**`

* Beim Verwenden des Output-Dienstes zum Zusammenführen eines bestimmten Formulars mit einem Dataxml beträgt die Antwortzeit 20-mal in Bezug auf die von einem ES4 SP1-Server benötigte Zeit. NPR-15283

#### AEM Forms-App {#aem-forms-app-1}

* Die Meldung, die beim Wiederherstellen von ungespeicherten Aufgaben angezeigt wird, muss deutlicher gemacht werden, um Benutzerfehler zu reduzieren. NPR-15377
* Die AEM Forms-App rendert keine Formulare, die aus benutzerdefinierten Vorlagen erstellt wurden. NPR-15892
* Benutzer können sich nicht bei der AEM Forms-App anmelden. NPR-15891

Die wichtigsten Highlights von AEM 6.2 SP2-CFP1 sind:

* Optimiert die Replikationsfunktionen in Sites:

* Behebung verschiedener Probleme mit Rollout, LiveCopy und fehlerhaftem Schreiben

* Verbessert die Reaktionsfähigkeit der Touch-optimierten Benutzeroberfläche bei:

* Asset-Suchvorgängen
* größenbasierten Sortiervorgängen

* Verbessert das Tag-Management in Smart-Sammlungen
* Strengere Zugriffskontrollen bei CRUD-Vorgängen in Ordnern

### Plattform {#previous}

* Anfrage, `ReplicationQueue#forceRetry`-API-Aufrufe beim Starten von Replikationsagenten zu entfernen, da solche Aufrufe die Instanz erheblich verlangsamen, insbesondere, wenn es viele Replikationsagenten gibt. NPR-14032: Hotfix für GRANITE-13095
* Anforderung einer `DurboImportConfigurationProviderService`-OSGi-Konfiguration zur Unterstützung von Feldern, in denen ein Array von Werten gespeichert werden kann. NPR-14570: Hotfix für CQ-108684
* Die Verwendung der Sightly-Komponente auf einer Seite nach der Migration auf AEM 6.2 führt dazu, dass das Dialogfeld „Eigenschaften“ der Seite nicht mehr funktioniert. NPR-14328: Hotfix für CQ-108355
* Durch das Aufheben der Planung eines zuvor geplanten Vorgangs wird der entsprechende Knoten unter */var/eventing/scheduled-jobs* nicht entfernt. NPR-14253: Hotfix für SLING-5666
* Wenn ein Administrator versucht, sich als ein gelöschter Benutzer auszugeben, kann die Benutzeroberfläche nicht aktualisiert werden. NPR-14247: Hotfix für CQ-107446
* XSS-Schutzprüfung, die eine falsche Kodierung in der Sightly-Komponente verursacht. NPR-14004: Hotfix für CQ-93821
* Anfrage zum Upgrade des Jackrabbit File-Vault auf Version 3.1.30, um mehrere Probleme zu beheben. NPR-13454
* Der Cache-Fehler tritt auf, wenn Sling Distribution die Verteilungspakete vom Autor zur Veröffentlichung synchronisiert. NPR-13034: Hotfix für GRANITE-13970

### Sites {#sites-18}

* Probleme mit VersionManagerImpl. Es werden falsche Versionen aus dem Versionsverlauf gelöscht. NPR-14372
* Die WCM Sightly Foundation-Parsys-Komponente ignoriert die Tag-Namen der Komponentendeklaration `cq:htmlTag / cq:tagName`. NPR-14225
* Wenn Sightly Parsys zum Rendern von Komponenten verwendet wird, die über JavaScript in die Touch-optimierte Benutzeroberfläche eingefügt wurden, wird die benutzerdefinierte Dekoration nach dem Aktualisieren der Seite ignoriert. NPR-14122
* Dropdown-Listen für Target funktionieren nicht im Dialogfeld &quot;Touch-Benutzeroberfläche&quot;, wenn mehrere Rich-Text-Felder (z. B. Links) erstellt werden. NPR-13911
* Beim Bearbeiten eines Textfelds mit mehreren RTE-Eigenschaften (Rich-Text-Editor) in einem Dialogfeld (Touch UI) wird der Fokus zufällig auf eine bestimmte RTE-Eigenschaft verschoben. NPR-13703
* Die standardmäßige Videokomponente rendert die Videominiatur nicht. NPR-14976
* Informationen werden langsam auf die Registerkarte Live-Nutzung im Vorlageneditor geladen. NPR-14880: Hotfix für CQ-83417
* Durch die Installation von Hotfix-10936 auf einer AEM 6.2-Instanz wird die Iparsys-Komponente deaktiviert. NPR-14330: Hotfix für CQ-106982
* Mehrere Probleme mit der Rollout-Komponente und ein Problem mit Live Copy nach der Migration auf AEM 6.1 SP1. NPR-15256
* Die Seiten-Rollout-Aktion kann selbst bei mehreren Rollout-Konfigurationen keine untergeordneten Elemente über die erste Ebene hinaus erstellen. NPR-15055
* Beim Senden des Dialogfelds &quot;PageProperties&quot;über den Editor werden unveränderte Daten auf den Registerkarten LiveCopy neu geschrieben. NPR-14693
* Wenn das Dialogfeld &quot;PageProperties&quot;vom Editor gesendet wird, schreibt MSM Post Processor einige Parameter aus der Anforderung anstelle von `msm:writeLiveCopyConfig` -Parameter. NPR-14434
* Mehrere Probleme im Zusammenhang mit der Rollout-Komponente, Live Copies und anderen Aspekten von MSM. NPR-12235

### Assets {#assets-18}

* Unpack Workflow kann Bilder mit Sonderzeichen im Bilddateinamen nicht verarbeiten. NPR-15227: Hotfix für CQ-103887
* Assets mit dem Ausdruck „Mit Bedingung wiederholen“ werden nicht richtig angezeigt. Wenn die Benutzerin bzw. der Benutzer eine Vorschau der `*CDN3835RLCEN*`-Briefvorlage anzeigt, werden keine Assets angezeigt, die sich im Hauptzielbereich befinden. Bei Dateianhang-Widgets, die mehrere Anhänge zulassen, führt das Senden einer neuen Formularinstanz mit einer Anlage auf einem Widget, das bereits über eine vorherige Anlage verfügt, zur Anzeige eines Fehlercodes. NPR-14844

* Beim Erstellen einer Smart-Sammlung wird das style-Tag beim Speichern der Smart-Sammlung nicht beibehalten. NPR-15081: Hotfix für CQ-4195494
* Asset-Suchabfragen werden in der Touch-optimierten Benutzeroberfläche bei gleichzeitigen Suchvorgängen durch mehrere Benutzer langsam ausgeführt. NPR-15019: Hotfix für CQ-4195405
* Metadaten, die für eine Eigenschaft des Typs `Long[]` extrahiert wurden, werden in den Typ `String[]` konvertiert, wenn das ursprüngliche Asset an einen anderen Speicherort hochgeladen wird. NPR-15016: Hotfix für CQ-4195005

* Benutzer können gespeicherte Suchen oder Smart-Sammlungen nicht löschen. NPR-14924: Hotfix für CQ-108494
* Das Bearbeiten von Metadaten für Assets in großen Mengen (Anfügemodus) unter Verwendung eines booleschen Werts für TypeHint in einem Dropdown-Feld im zugrunde liegenden Metadatenschema führt zu einem Fehler. NPR-14529: Hotfix für CQ-106876
* Benutzer mit Replikationsrechten können jetzt Asset-Ordner löschen. NPR-14321: Hotfix für CQ-88271
* Beim Versuch, die Videoprofile für ein Video im Kanal-Editor zu bearbeiten, wird das Dialogfeld &quot;Design&quot;nicht geöffnet und löst im Fehlerprotokoll eine Null-Pointer-Ausnahme aus. NPR-14144: Hotfix für CQ-81101
* Die vom System generierte Zeitstempeleigenschaft &quot;Erstellt&quot;auf der Eigenschaftenseite für ein Asset ist falsch. NPR-13992: Hotfix für CQ-95029
* Anfrage, die Erkennung von doppelten Assets für Benutzer ohne Lesezugriff in AEM Assets zu aktivieren. NPR-13851: Hotfix für CQ-102281
* Benutzer können Metadaten für Assets nicht stapelweise auf der Eigenschaftenseite bearbeiten. NPR-13721: Hotfix für CQ-100703
* Falsche Fehlermeldung in der klassischen Benutzeroberfläche, wenn ein doppeltes Asset hochgeladen wird. Die Fehlermeldung gibt nicht an, warum der Upload fehlgeschlagen ist. NPR-13691: Hotfix für CQ-99272
* AEM Assets kann in der Listenansicht nicht mehr als 50 Assets nach Größe sortieren, wenn der Ordner mehrere Assets enthält. CQ-100588
* Wenn Sie mehrere Assets auswählen, wird ein Fehler mit Antwortcode 414 (Anfrage-URI zu lang) angezeigt, wenn der Asset-/Ordner-URI zu lang ist. NPR-13516: Hotfix für CQ-76076
* Die Seite „Assets-Bericht“ reagiert nicht mehr, wenn die Benutzerin bzw. der Benutzer im Dialogfeld `Configure Columns` alle Auswahlmöglichkeiten auswählt. NPR-13187: Hotfix für CQ-95589
* Unerwartetes Verhalten der Tag-Auswahl in Safari und Internet Explorer. NPR-13134
* Durch Bearbeiten der gespeicherten Suchen in der Asset-Admin-Suchleiste können diese als verschachtelte intelligente Auswahl gespeichert werden, was zu Problemen mit der Umgebungsstabilität führt. NPR-13119: Hotfix für CQ-99460
* Nach dem Verschieben einer Datei (oder eines Ordners) und dem anschließenden Umbenennen der Datei spiegeln die Metadaten `cq:name` nicht den neuen Dateinamen (Ordnernamen) wider. NPR-13036: Hotfix für CQ-99141
* Assets mit Namen, die Sonderzeichen enthalten, können nicht über den per E-Mail freigegebenen Download-Link heruntergeladen werden. NPR-12872: Hotfix für CQ-95795
* Vordefinierte Asset-Berichte, die generiert werden, wenn eine erhebliche Anzahl von Assets vorhanden ist, führen zu starken Durchläufen, wenn die Suche keine Index- und CPU-Auslastungsspitzen erreicht. NPR-12811: Hotfix für CQ-84409
* Benutzer in der AMS AEM Assets-Autoreninstanz greifen von unterschiedlichen Netzwerken auf Assets zu und können Assets nicht über den Chunk-Upload hochladen, ohne Berechtigungen zum Löschen von Ordnern zu erhalten. NPR-12768: Hotfix für CQ-82715
* Bei der Tag-basierten Suche nach Assets mit der Asset-Suchleiste beschränkt sich die Vervollständigungsfunktion nicht auf den Stammpfad und zeigt Tags aus allen Namespaces an. NPR-12666
* Die StaticRenditions-Komponente löst eine Null-Zeiger-Ausnahme aus. NPR-12665
* Anfrage, MissingMetadataNotificationJob zu deaktivieren, da dadurch die Benutzeroberfläche für die Badge-Benachrichtigung die Seite mit einer Laufzeitausnahme „Eingabe kann nicht gescannt werden“ unterbrochen wird. NPR-12500: Hotfix für CQ-93573
* Die Option „Bearbeiten deaktivieren“ für ein Tag-Feld funktioniert nicht auf Seiten Asset-Eigenschaften in der Touch-optimierten Benutzeroberfläche. NPR-12429: Hotfix für CQ-88835
* API-Korrekturen in AEM Assets 6.2 für die Companion App SMB-Implementierung. NPR-11099
* Seit `Jquery` aktualisiert werden, können Benutzer keine Asset-Sammlung auswählen und die Auswahl im Bereich &quot;Inhalt verknüpfen&quot;eines Inhaltsfragments bestätigen. NPR-14847: Backport für CQ-4194209
* Obwohl auf der Client-Seite eine unendliche Sortierung aufgerufen wird, werden nur Artikel/Banner/Sammlungen sortiert, die derzeit in der Benutzeroberfläche angezeigt werden. NPR-14493: Hotfix für CQ-109926
* Anforderung zur Implementierung der Omnisearch-Funktion für den AEM Mobile-on-Demand-Service. Die Keyword-Suche nach Artikeln, Sammlungen oder Bannern gibt keine Übereinstimmungen zurück. NPR-14093: Hotfix für CQ-101394
* Bei Verwendung der Coral-select-Komponente (*granite/ui/components/coral/foundation/form/select*) in einem Dialogfeld funktioniert die Wertinitialisierung im Internet Explorer (IE11- oder Edge-Browser) nicht korrekt, wenn der ausgewählte Wert ein einzelnes Element enthält. NPR-13395: Hotfix für CQ-101013

### Projekte {#projects-5}

* Beim Exportieren eines Übersetzungsprojekts, das mit der Übersetzungsmethode als &quot;human&quot;und dem Übersetzungsanbieter als &quot;none&quot;erstellt wurde, wird keine Datei translation_export_summary.xml generiert, da die GUID-Zuordnungsdatei fehlt. NPR-13137: Hotfix für CQ-91976
* Wenn in AEM-Projekten ein Projekt mit der Eigenschaft „Fälligkeitsdatum“ erstellt wird, wird bei der Datumskonvertierung die Zeit aufgrund der unterschiedlichen Zeitzone zwischen Server und Client falsch festgelegt. NPR-13003: Hotfix für CQ-98288
* Die Option „In Sites anzeigen“ wird beim im Übersetzungsvorgang nicht angezeigt, wenn ein Übersetzungsprojekt aktualisiert wird. NPR-12966: Hotfix für CQ-93740
* Wenn ein Übersetzungsprojekt für eine exportierte Site-Seite erstellt wird, wird es in der Vorschau nicht korrekt dargestellt. NPR-12964: Hotfix für CQ-84627

### Workflow {#workflow-3}

* Der Payload-Link auf der Registerkarte &quot;Archiv&quot;der Workflow-Konsole gibt einen Fehler mit dem Antwortcode &quot;404&quot;zurück, wenn darauf geklickt wird. NPR-14993: Hotfix für CQ-4194977
* Bei Verwendung von AEM-Standard-Workflows sendet der CQ Mailer keine E-Mail-Benachrichtigung an die Gruppe, wenn die E-Mail-Adresse eines Mitglieds fehlt. NPR-14804: Hotfix-Anfrage für GRANITE-91499
* Leistungsverbesserungen für Posteingang und Benachrichtigungsabzeichen in der Touch-optimierten Benutzeroberfläche. NPR-14145: Hotfix für CQ-101125
* Benutzer können beim Starten von Workflows keine Vorschau der Payload über die Workflow-Posteingangskonsole anzeigen. NPR-13226: Hotfix für CQ-100275
* Das mit dem SAML-Authentifizierungs-Handler konfigurierte Cookie &quot;saml_request_path&quot;zeigt Cookies an, die mit einem zusätzlichen `?` Zeichen. Wenn eine SAML-Antwort an AEM zurückgesendet wird, gibt das AEM-Cookie „saml_request_path“ aufgrund bereits codierter Zeichen einen ungültigen Wert zurück. NPR-13517: Proaktiver Hotfix für GRANITE-11722 und GRANITE-14414

### Dynamic Media {#dynamic-media}

* Zahlreiche `AEM-Scene7`-Sling-Vorgänge, die während der AEM-Aktivierung erstellt und abgebrochen wurden, werden während der Replikation als Archivierungsvorgänge protokolliert. NPR-12835: Hotfix für CQ-86115

### Sicherheit {#security-5}

* Anfrage zur Behebung eines Eingabevalidierungsproblems im WCMDebug-Filter. NPR-12444: Hotfix-Anfrage für CQ-94890
* Proaktive Anfrage zur Korrektur des XSS-Verhaltens bei Verwendung des Assistenten zur Launch-Erstellung.
NPR-13062: Hotfix-Anfrage für CQ-99577

#### Forms-Add-on-Paket {#forms-add-on-package-19}

`Adaptive Forms`

* Beim Erstellen eines wiederholbaren Bedienfelds mit adaptiven Formularen kann der Bedienfeldtitel zur Laufzeit nicht aktualisiert werden. NPR-15325
* Wenn Sie einen Standardwert für ein Optionsfeld festlegen und beim Speichern oder Senden einen anderen Wert auswählen, wird der ausgewählte Wert in der Vorbefüllung nicht angezeigt. NPR-15304
* Google Chrome zeigt ein falsches Verhalten bei der Verwendung des Options-Ereignisses zum dynamischen Füllen der Dropdown-Liste und zum Senden des Werts des ausgewählten Elements. NPR-15198
* Beim Erstellen eines wiederholbaren Bedienfelds mit adaptiven Formularen kann der Bedienfeldtitel zur Laufzeit nicht aktualisiert werden. NPR-15181
* Bei der Verwendung des Bearbeitungsmodus für adaptive Formulare treten JavaScript-Fehler wie &quot;Handler der Komponente ist ungültig&quot;und &quot;guidelib ist nicht definiert&quot;auf. NPR-15112
* Ein Lazy Loading-Fragment in einem sich wiederholenden Bedienfeld funktioniert nicht wie erwartet. NPR-13916, NPR-14785

`Correspondence Management`

* Korrespondenzverwaltungs-Assets mit Ausdruckssatz `'Repeat with condition'` werden nicht richtig angezeigt. NPR-14844
* Bei der Suche nach einem Korrespondenzverwaltungs-Asset (z. B. einem Brief, einem Dokumentfragment oder einem anderen Typ) fehlt das Symbol „Warteschlange für den Download“ in der Symbolleiste. NPR-14745
* Beim Erstellen eines Listenmoduls funktioniert das Umschalten der Asset-spezifischen Eigenschaften (z. B. bearbeitbar, obligatorisch) nicht. NPR-14689
* Das Bedienfeld &quot;Datenelemente&quot;im Dienstprogramm &quot;Expression Builder&quot;wird weiterhin geladen, falls ein Bedingungsmodul erstellt wird, ohne ein Datenwörterbuch auszuwählen. NPR-14688
* Bei der Vorschau eines Briefes können Benutzer keine Tabulatoren verwenden, um Inhalte im Tabellenformat auszurichten. NPR-14481
* Wenn Korrespondenzverwaltungs-Assets stapelweise aus der Benutzeroberfläche exportiert werden, generiert der AEM Forms-Server unnötige Protokolle. NPR-15226
* Wenn die Vorschau eines Briefes angezeigt wird, wird Text im Blocksatz in einer anderen Schriftart angezeigt. NPR-15468

`**Forms Portal**`

* Anlagen von übermittelten Formularen im Formularportal sind nicht sichtbar, wenn ein neuer Entwurf aus dem Portal übermittelt wird. NPR-13515

`**Forms Manager**`

* Beim Navigieren in der *FormsandDocuments* festgelegt ist, wird die Schaltfläche &quot;Einfügen&quot;nicht angezeigt, wenn der Benutzer ein Asset kopiert und dann zu einem anderen Ordner navigiert. CQ-111327

#### JEE-Installationsprogramm von Forms {#forms-jee-installer-19}

`Rights Management`

* Das auf die Benutzeranmeldung bezogene Prüfereignis wird mit ungültiger Zeit protokolliert. Die richtige Zeit für ein Prüfereignis kann nicht rückverfolgt werden. NPR-13107
* Adobe Acrobat Reader und Microsoft® Office können keine Dokumente öffnen, die mit erweiterter Authentifizierung geschützt sind. NPR-14482

`Process Management`

* Wenn eine weitergeleitete Entwurfsaufgabe in HTML Workspace an den ursprünglichen Benutzer zurückgegeben wird, wird die Aufgabe nicht in der Warteschlange des ursprünglichen Benutzers angezeigt. NPR-15178

`Assembler Service`

* AEM Forms kann PDF/A-2b mit mehr als zwei Signaturen nicht validieren. NPR-14101

`XTG`

* Beim Drucken eines Dokuments über ein Umgehungsfach des Druckers aktiviert die `GeneratePrintedOutput`-Funktion das Abholen von Papier aus dem rechten Umgehungsfach nicht. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer stürzt ab, wenn der Benutzer das Dienstprogramm &quot;Rechtschreibprüfung&quot;mit dem ausgewählten Gebietsschema für Formulare als Französisch (Kanada) ausführt. NPR-13740
* Forms Designer stürzt ab, wenn der Benutzer für ein Formularfeld „Ereignis berechnen“ oder „Ereignis validieren“ auswählt, die Sprache in JavaScript ändert und `this.` in das **[!UICONTROL Skript-Editor]**-Fenster eingibt. NPR-12974

### In CFP1 enthaltene Feature Packs {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms-Add-on-Paket):

* Wenn ein adaptives Formular aus einer XDP-Datei erstellt wird, folgt das Tab für Barrierefreiheit nicht einem festgelegten Muster. NPR-12562

`Adaptive forms` (Forms-Add-on-Paket):

* Der Regel-Builder für adaptive Formulare bietet keinen rollenbasierten Zugriff. Änderungen, die von einem Autor vorgenommen wurden, können nicht verfolgt werden. NPR-12840

`Core` (Forms JEE-Installationsprogramm):

* Die CORS-Funktion (CoreCross Origin Resource Sharing) als Servlet-Filter ist für JBoss®+ nicht aktiviert. NPR-13050

## Download-Anweisungen für CFP über die Software-Verteilung {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Für AEM Forms-Kunden ist es wichtig, das AEM Forms-Add-On-Paket zu installieren, nachdem AEM Service Pack, Cumulative Service Pack oder Feature Pack installiert wurden.

Sie können das CFP-Paket direkt von der Seite der Software-Verteilung herunterladen oder die folgenden Schritte ausführen:

1. Öffnen Sie [Software Distribution](https://experience.adobe.com/downloads). Zum Anmelden bei Software Distribution benötigen Sie eine Adobe ID.
1. Tippen Sie im Kopfzeilenmenü auf **[!UICONTROL Adobe Experience Manager]**.
1. Tippen Sie auf den Paketnamen, wählen Sie **[!UICONTROL EULA-Bedingungen akzeptieren]** und tippen Sie auf **[!UICONTROL Herunterladen]**.

## Installationsanweisungen für CFP {#installation-instructions-for-cfp}

Dieser Abschnitt erläutert die Anforderungen und Schritte zur Installation von CFP.

### Vor der Installation {#before-you-install}

>[!NOTE]
>
>Die von Adobe bereitgestellten optionalen Funktionspakete hängen von der Release-Version und dem Cumulative Fix Pack ab. Wenn Sie ein Feature Pack installiert haben, wenden Sie sich an die [AEM-Kundenunterstützung](https://experienceleague.adobe.com/de?support-solution=General#support), um die Kompatibilität mit diesem Cumulative Fix Pack für AEM 6.3 zu überprüfen.

>[!NOTE]
>
>Es wird empfohlen, die Überprüfung für jedes neue Installationspaket auszuführen, bevor Sie versuchen, das Paket zu installieren. Vor der Überprüfung werden alle Fehler analysiert und protokolliert, die vor der Installation gefunden wurden, und die Benutzer werden proaktiv vor solchen Fehlern, Überlagerung, Berechtigungen gewarnt.
>

* AEM 6.2 Service Pack 1 ist eine Voraussetzung für CFP. Installationsanweisungen finden Sie in den Versionshinweisen für [AEM 6.2 Service Pack 1](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

* Der Download des Cumulative Fix Packs ist über die [Software-Verteilung](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) verfügbar, auf die Sie direkt von der AEM-Instanz aus zugreifen können.
* Bei einer Clusterbereitstellung mit (RDBMK oder MongoDB) kann das CFP-Paket auf allen Autoreninstanzen installiert werden, die Package Manager verwenden.

* Bevor Sie das Cumulative Fix Pack installieren, stellen Sie sicher, dass Sie einen Schnappschuss erstellen oder eine Sicherung Ihrer AEM-Instanz erstellen.
* Die Deinstallation von CFP wird nicht unterstützt.

### Installieren von CFP über die Software-Verteilung {#install-the-cfp-via-package-share}

Um das Cumulative Fix Pack auf einer bestehenden AEM 6.2 SP1-Instanz zu installieren, führen Sie die folgenden Schritte aus:

1. Um das Paket herunterzuladen, klicken Sie auf [Software-Verteilung](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip).

1. Öffnen Sie [Package Manager](http://localhost:4502/crx/packmgr/index.jsp) und klicken Sie auf **[!UICONTROL Paket hochladen]**, um das Paket hochzuladen.

1. Wählen Sie das Paket aus und klicken Sie auf **[!UICONTROL Installieren]**.

### Automatische Installation {#automatic-installation}

CFP kann wie folgt automatisch in einer laufenden Instanz installiert werden:

* Legen Sie das Paket in ../crx-quickstart/install ab, während der Server läuft. Das Paket wird automatisch installiert.
* Verwenden Sie die [HTTP-API aus Package Manager](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) – es muss `cmd=install&recursive=true` sein –, damit das verschachtelte Paket installiert wird.

### Bestätigen der Installation {#validate-installation}

1. Auf der Seite „Produktinformationen“ (/system/console/productinfo) sollte nun unter „Installierte Produkte“ die aktualisierte Version „Adobe Experience Manager, Version 6.2.0.SP1-CFP20“ angezeigt werden.
1. Alle OSGI-Bundles sind entweder AKTIV oder FRAGMENT in der OSGi-Konsole (Webkonsole verwenden: /system/console/bundles).

>[!NOTE]
>
>Bei erfolgreicher Installation des Pakets wird eine Informationsmeldung angezeigt, die darauf hinweist, dass das Inhaltspaket erfolgreich installiert wurde, z. B. „AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 wurde erfolgreich installiert.“

>[!NOTE]
>
>Seit AEM 6.2 SP1-CFP1 hat sich die Protokollebene in Jackrabbit FileVault für die meisten Meldungen von INFO in DEBUG geändert. Um Installationsprotokolle für ein auf AEM 6.2 SP1-CFP1 oder höher installiertes Inhaltspaket zu erhalten, aktivieren Sie die DEBUG-Protokollebene für `org.apache.jackrabbit.vault.packaging.impl`.

### Installieren von AEM Forms {#install-forms}

>[!NOTE]
>
>Überspringen Sie diesen Abschnitt, wenn Sie AEM Forms nicht verwenden.

#### AEM Forms-Add-on installieren {#install-aem-forms-add-on}

>[!NOTE]
>
>(**Nur AEM Forms on JEE**) Das Verfahren zum Installieren eines CFP auf AEM Forms on JEE wird unter [Installieren von CFP auf AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee) beschrieben.

1. Vergewissern Sie sich, dass Sie das AEM 6.2 SP1 CFP-Paket installiert haben.
1. Wählen Sie unter den aufgeführten [AEM Forms-Versionen](aem-forms-releases.md) das für Ihr Betriebssystem passende Forms-Add-on-Paket aus und laden Sie es herunter.
1. Installieren Sie das Forms-Add-on-Paket wie unter [Installieren des AEM Forms-Add-on-Pakets](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) beschrieben.

#### Installieren des AEM Forms JEE-Bundles-Pakets {#install-aem-forms-jee-bundles-package}

Fehlerbehebungen in AEM Forms JEE werden über ein separates Installationsprogramm bereitgestellt. Informationen zum Installieren eines CFPs auf AEM Forms auf JEE finden Sie unter [Installieren von CFP auf AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Forms Designer-Installationsprogramm {#designer-installer}

1. Führen Sie zur Installation des Updates die Datei „Designer6.2.0_&lt;Sprache>_Cumulative_QF.msp“ aus.
1. Klicken Sie auf dem Begrüßungsbildschirm auf **Aktualisieren**. Die Installation wird gestartet.
1. Klicken Sie nach Abschluss der Installation auf **Beenden**.

## Benutzerkonfigurierbare Zeitlimitparameter für DTM-, Analytics- und Target-Verbindungen {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Mit AEM Cumulative Fix Pack 6.2 SP1-CFP7 und späteren Versionen wurden die Zeiträume für Verbindungs-Zeitüberschreitungen für alle oben genannten Verbindungen gemäß den folgenden Details konfigurierbar gemacht:

| **Verbindungen** | **Verbindungs-Zeitüberschreitung&#42;** | **Socket-Zeitüberschreitung&#42;&#42;** |
|---|---|---|
| DTM | 30.000 ms | 30.000 ms |
| Analyse | 30.000 ms | 30.000 ms |
| Ziel | 60.000 ms | 30.000 ms |

* **Verbindungs-Zeitüberschreitung&#42;**: Die Zeitüberschreitung (in Millisekunden), bis eine Verbindung hergestellt ist. Ein Zeitüberschreitungswert von null wird als unendliche Zeitüberschreitung interpretiert.
* **Socket-Zeitüberschreitung&#42;&#42;**: Die Zeitüberschreitung (in Millisekunden) für das Warten auf Daten oder eine maximale Zeit der Inaktivität zwischen zwei aufeinanderfolgenden Datenpaketen.

## Deaktivieren des Replikationsstatus in der Tagging-Konsole (klassische Benutzeroberfläche) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Falls Sie CFP3 oder höher verwenden, führen Sie die folgenden Anweisungen aus, um den Replizierungsstatus in der Tagging-Konsole der klassischen Benutzeroberfläche zu deaktivieren:

* Überlagerung *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;* in *`/apps`*

* Fügen Sie `replicationStateRequired`: &quot;false&quot; nach Zeile 416 hinzu.

```js
415 baseParams: {
416 count: "false",
417 "replicationStateRequired": "false"
418 },
```

## Die neueste Java 8™-Aktualisierung 131 gibt eine Ausnahme aus (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Diese Konfigurationseinstellungen sind für AEM Forms-Kunden spezifisch, die Document Security verwenden.

NPR-21355 ist in CFP12.1 enthalten. Wenn Sie CFP12.1 oder höher installieren, führen Sie das folgende Verfahren aus, um NPR-21355 auf dem JBoss®-Anwendungsserver zu konfigurieren. Wenn Sie CFP12.1 auf dem AEM Forms-Server installieren, der auf Oracle WebLogic- oder IBM® WebSphere-Programm-Servern ausgeführt wird, ist keine zusätzliche Konfiguration erforderlich:

1. Sichern, löschen und erstellen Sie eine Datei &quot;module.xml&quot;. Der Standardspeicherort der Datei ist [AEM_Forms_Installationsverzeichnis]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. Öffnen Sie die neu erstellte Datei module.xml zur Bearbeitung. Fügen Sie der Datei den folgenden Code hinzu:

```xml
<module xmlns="urn:jboss:module:1.1"
name="com.adobe.livecycle">
<resources>
<resource-root path="cryptojcommon.jar"/>
<resource-root path="cryptojce.jar"/>
<resource-root path="jcmFIPS.jar"/>
<resource-root path="certj.jar"/>
<resource-root path="cglib.jar"/>
</resources>
<dependencies>
<module name="javax.api"/>
<module name="asm.asm"/>
</dependencies>
</module>
```

1. Erstellen Sie eine Sicherungskopie des `jsafeFIPS.jar`, `jsafeJCEFIPS.jar`, und `certjFIPS.jar` Dateien unter [AEM_Forms_Installationsverzeichnis]`/jboss/modules/system/layers/base/com/adobe/livecycle/main/` und löschen Sie die Dateien aus dem zuvor erwähnten Verzeichnis.

Wenden Sie sich an den [Adobe-Support](https://experienceleague.adobe.com/de?support-solution=General#support), um neue JAR-Dateien zu erhalten. Platzieren Sie die JAR-Dateien, die Sie von [Adobe Support](https://experienceleague.adobe.com/de?support-solution=General#support) erhalten haben, unter [AEM_Forms_Installationsverzeichnis]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. (Nur Windows) Ändern Sie die Konfigurationsdateien `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` oder `domain.conf.bat`:

* Für JBoss®-Server in Einzelkonfiguration öffnen Sie die Datei „standalone.conf.bat“ zur Bearbeitung.
* Für JBoss®-Server in der Cluster-Konfiguration öffnen Sie „domain.conf.bat“ zur Bearbeitung.

  Fügen Sie die folgenden Zeilen am Ende hinzu und speichern Sie die Datei:

  `JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true`

  `JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE`

1. (Nur Linux-Betriebssystem) Ändern Sie die Konfigurationsdateien [AEM_Forms_Installationsverzeichnis]/jboss/standalone.conf oder domain.conf:

* Für JBoss®-Server in Einzelkonfiguration öffnen Sie die Datei „standalone.conf“ zur Bearbeitung.
* Für JBoss®-Server in der Cluster-Konfiguration öffnen Sie „domain.conf“ zur Bearbeitung.

  Fügen Sie die folgenden Zeilen am Ende hinzu und speichern Sie die Datei:

  `JAVA_OPTS="$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true"`

  `JAVA_OPTS="$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"`

## Für NPR-19778 erforderliche Konfigurationseinstellungen {#configuration-settings-required-for-npr}

>[!NOTE]
>
>NPR-19778 ist Teil von CFP14.

Die Anzahl für freigegebene Warteschlangen wird für andere Benutzer nicht aktualisiert, wenn ein Benutzer eine Aufgabe anfordert. Daher hat Adobe eine neue Eigenschaft eingeführt. Führen Sie die folgenden Schritte aus, um diese Eigenschaft in Ihrer AEM-Instanz zu konfigurieren:

1. Gehen Sie zu „Administrator-Benutzeroberfläche“ > „Services“ > „Arbeitsbereich“ > „Globale Verwaltung“.
1. Globale Einstellungen exportieren.
1. Fügen Sie in der heruntergeladenen XML-Datei das Tag hinzu `<client_tasksPollingInterval>10</client_tasksPollingInterval>`. Zehn ist der Beispielwert in Sekunden. Sie können ihn entsprechend ändern.
1. Speichern Sie die Datei.
1. Gehen Sie zurück zu „Administrator-Benutzeroberfläche“ > „Services“ > „Arbeitsbereich“ > „Globale Verwaltung“.
1. Importieren Sie die XML-Datei im Abschnitt „Globale Einstellungen importieren“.
1. Sie können sich jetzt vom System abmelden und erneut anmelden.
1. Die Anzahl der freigegebenen Warteschlangen wird für andere Benutzer im Workspace aktualisiert.
1. Um die Abfrage zu deaktivieren, ändern Sie den Wert in 0 und importieren Sie die XML-Datei erneut.

## Änderungen an der Benutzeroberfläche {#ui-changes}

* Verhaltensänderung bei der Anzeige von Titeln auf der Bildkarte für Bilder, bei denen die `dc:title`-Eigenschaft auf „String [] ( multifield )“ eingestellt ist: Nur der zuletzt geänderte Titel wird auf der Bildkarte in der Benutzeroberfläche angezeigt, obwohl alle Titel in CRX gespeichert werden. Hotfix für CQ-4217165

## Bekannte Probleme {#known-issues}

* Durch das Aktualisieren von AEM 6.2SP1-CFP19 und AEM 6.2SP1-CFP20 von CFP18 wird die Rot-Umleitung auf die Begrüßungsseite der klassischen Benutzeroberfläche anstelle von /sites.html/content geändert. Möglicherweise müssen Sie die Eigenschaft „sling:target“ mit CRX Explorer von „/welcome.html“ auf „/index.html“ korrigieren. Dieses Problem wird beim Aktualisieren von CFP17 oder einer älteren Version nicht beobachtet.

Die folgenden vorübergehenden Fehler können auftreten, wenn Sie AEM 6.2 SP1-CFPx installieren. Für diese Fehler ist jedoch keine Lösung erforderlich, da sie Ihre AEM-Instanz nicht beeinträchtigen und nach der CFP-Installation verschwinden:

* Beim Aktualisieren der AEM 6.2SP1-CFP20-Instanz auf AEM 6.5 funktionieren einige Vanity-URLs möglicherweise, Beispiele:

* */projects.html*
* */sites.html*

Die Problemumgehung besteht jedoch darin, die AEM-Instanz nach einer Aktualisierung neu zu starten.

* HTTP 500 Interner Server-Fehler wird empfangen, wenn die Detailseite der Web Console-Komponente geöffnet wird.
* Fehler wie **Komponenteninstanz erstellen** und **Service Factory gab null zurück** tritt aufgrund des Repository-Neustarts auf:

* com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Cannot create component instance due to failure to bind reference profileManager
* org.apache.sling.commons.scheduler FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Komponente: com.day.cq.tagging.impl.TagGarbageCollector (1687)))

* Fehler bei der CFP-Installation in Mongo und DB2® festgestellt: DB2®: **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Exception: java.lang.NullPointerException**.  Dieser Fehler tritt nach der Installation eines CFP über CFP8 nicht auf.
* (Adobe Granite Maintenance Scheduler Update-Aufgabe) com.adobe.granite.maintenance.impl.TaskScheduler: No maintenance task found with name WorkflowPurgeTask for window `granite:weekly`
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* Wenn Sie CFPx auf AEM 6.2 SP1 installieren, das das Feature Pack für Smart-Tags enthält, wird der zuvor hinzugefügte Workflow-Schritt für Smart-Tag-Assets aus dem Workflow &quot;DAM-Update-Asset&quot;gelöscht.

## Uber Jar {#uber-jar}

Das Uber Jar für 6.2 SP1-CFP20 ist im Adobe Public Maven-Repository verfügbar.

Um Uber Jar in einem Maven-Projekt zu verwenden, fügen Sie folgende Abhängigkeit in Ihr Projekt-POM ein:

```XML
<dependency>
 <groupId>com.adobe.aem</groupId>
 <artifactId>uber-jar</artifactId>
 <version>6.2.SP1-CFP20</version>
 <classifier>apis</classifier>
 <scope>provided</scope>
</dependency>
```

## Enthaltene OSGI-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-5}

Im folgenden Text wird die Liste der im CFP enthaltenen OSGI-Bundles und Inhaltspakete dokumentiert.

* [Liste der in AEM 6.2 SP1-CFP20 enthaltenen OSGi-Bundles](assets/do-not-localize/updated.txt)
* [Liste der in AEM 6.2 SP1-CFP20 enthaltenen Inhaltspakete](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [Seite mit den AEM 6.2 Hotfixes](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [AEM 6.2 SP1 – Versionshinweise](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [AEM 6.2 – Versionshinweise](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [AEM-Produktseite](https://business.adobe.com/de/products/experience-manager/adobe-experience-manager.html)
>* [Dokumentation zu AEM 6.2](https://experienceleague.adobe.com/de/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [Adobe-Prioritäts-Produkt-Updates](https://experienceleague.adobe.com/de/docs/release-notes/experience-cloud/current)
