---
title: Definitionen von Aktualisierungsversionen
description: In diesem Artikel werden die verschiedenen  [!DNL Experience Manager] -Versionen beschrieben, einschließlich Vollversionen, Feature Packs und Service Packs.
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 100%

---

# Definitionen von [!DNL Experience Manager]-Aktualisierungsversionen  {#update-release-vehicle-definitions}

Dieses Dokument enthält Einzelheiten zu den verschiedenen Arten von [!DNL Adobe Experience Manager]-Versionen, einschließlich Vollversionen, Feature Packs und Service Packs, die [!DNL Adobe] für Kunden bereitstellt.

>[!NOTE]
>
>Den Veröffentlichungsplan für [!DNL Experience Manager]-Aktualisierungsversionen finden Sie unter [[!DNL Experience Manager] -Roadmap für Aktualisierungsversionen](update-releases-roadmap.md)

## Vollversion {#full-release}

| Elemente | Beschreibung |
|-------|------|
| Definition | <ul> <li> Geplante Veröffentlichung </li> <li> Unterstützt Aktualisierungspfade für bestimmte Versionen, die in den Versionshinweisen angegeben sind </li> </ul> |
| Namenskonvention | <ul> <li> Die Versionsnummer für Hauptversionen erhöht sich nach der Formel X+1.Y.Z. </li> <li> Die Versionsnummer für Nebenversionen erhöht sich nach der Formel X.Y+1.Z. </li> </ul> Dabei ist X die primäre Versionsnummer, Y die sekundäre Versionsnummer und Z die Patch-Nummer. |
| Lieferumfang | <ul> <li> Neue Funktionen </li> <li>  Verbesserungen </li> <li>  Fehlerbehebungen </li> </ul> |
| Dokumentation | <ul> <li> Versionshinweise im Dokumentationsportal </li> <li> Dokumentation zu Funktionen, Verbesserungen und Fehlerbehebungen im Dokumentationsportal </li> </ul> |
| Veröffentlichungsintervall | Jährlich |
| Verfügbarkeit und Installation | <ul> <li> Bereitstellung als eigenständiges Produktinstallationsprogramm </li> <li>  Verfügbar über Lizenzierungs-Website und Managed Services </li> <li> Lizenzierungs-Website erfordert möglicherweise eine Migration des Content-Repository </li> </ul> |
| Teststufe | Vollständige Validierung durch Qualitätssicherung |

## Service Pack {#service-pack}

| Element | Beschreibung |
|-----|-----|
| Definition | <ul> <li> Geplante Veröffentlichung </li> <li> Aktuell kein Rollback möglich </li> </ul> |
| Namenskonvention | <ul> <li> Patch-Versionsnummer ist eine einstellige Zahl </li> <li> Nach der Installation erhöht sich die Versionsnummer des installierten Patches nach der Formel X.Y.Z.SPx </li> </ul> Dabei ist X die primäre Versionsnummer, Y die sekundäre Versionsnummer und Z die Patch-Nummer. x ist die Service-Pack-Nummer. |
| Lieferumfang | <ul> <li> Neue Funktionen</li> <li>  Verbesserungen </li> <li> Fehlerbehebungen </li> <li> Feature Packs mit Funktionen von allgemeinem Interesse (falls vorhanden) </li> </ul> |
| Dokumentation | <ul> <li> Versionshinweise im Dokumentationsportal </li> <li> Dokumentation zu Funktionen, Verbesserungen, Fehlerbehebungen im Dokumentationsportal </li> </ul> |
| Veröffentlichungsintervall | Vierteljährlich |
| Verfügbarkeit und Installation | <ul> <li> Bereitstellung als Paket </li> <li> Verfügbar über Software Distribution</li> <li>  Vorhandene funktionierende Installation erforderlich </li> </ul> |
| Teststufe | <ul> <li> Alle Fehlerbehebungen durch Qualitätssicherung validiert </li> <li>  Gesamte Paketsicherheit mit Automatisierungsläufen </li> </ul> |

## Cumulative Fix Pack {#cumulative-fix-pack-aem}

| Element | Beschreibung |
|-----|-----|
| Definition | <ul> <li> Ein Bereitstellungsmodell für die Veröffentlichung von Fehlerbehebungen </li> <li> Aggregiertes Inhaltspaket mit Inhaltspaket einzelner Komponenten </li> <li>  CFPs sind ein Rollover von Hotfixes und enthalten keine Verbesserungen.  </li> </ul> |
| Namenskonvention | X.Y.Z.CFPx <br> Dabei ist X die primäre Versionsnummer, Y die sekundäre Versionsnummer und Z die Patch-Nummer. x ist die Nummer des Cumulative Service Packs. |
| Lieferumfang | CFP steht für Cumulative Fix Pack und enthält Fehlerbehebungen für alle Komponenten bis zu einem bestimmten Datum. Wenn ein Kunde z. B. CFP3 anwendet, gilt CFP3 = CFP1 + CFP2. |
| Dokumentation | Versionshinweise im Dokumentationsportal |
| Veröffentlichungsintervall | Vierteljährlich |
| Verfügbarkeit und Installation | <ul> <li> Bereitstellung als Paket </li> <li>  Verfügbar über Software Distribution </li> <li>  Abhängig vom zuletzt veröffentlichten Service Pack </li> <li>  CFPs haben keine externen Abhängigkeiten. Kundinnen und Kunden müssen sich keine Gedanken über das Suchen/Auflösen von Abhängigkeiten machen. CFPs sollten nach dem zuletzt veröffentlichten Service Pack installiert werden. </li> <li>  CFPs können als ein Paket installiert werden und verbessern so das Kundenerlebnis.  </li> </ul> |
| Teststufe | Validierung durch Qualitätssicherung auf Integrationsebene und Regressionstests |

## Überlagerung {#overlay}

| Element | Details |
|-------|--------|
| Namenskonvention | Overlay-&lt;ticket ID> |
| Lieferumfang | Fehlerbehebung für eine JS- oder JSP-Datei |
| Dokumentation | Kein |
| Veröffentlichungsintervall | Bei Bedarf |
| Verfügbarkeit und Installation | <ul> <li> Bereitstellung als Paket von der [!DNL Experience Manager]-Kundenunterstützung  </li> <li> Nicht unbedingt in Service Packs oder Vollversionen enthalten </li> </ul> |
| Teststufe | Validiert durch die Kundenunterstützung |

## Feature Pack {#feature-pack}

| Elemente | Details |
|--------|-----|
| Definition | <ul> <li>Feature Packs sind Zusatzfunktionalitäten und werden über Service Packs bereitgestellt. Wenn das letzte Service Pack für eine [!DNL Experience Manager]-Version veröffentlicht wurde, stellt Adobe in der Zukunft keine weiteren Feature Packs dafür bereit. </li> <li> FPs enthalten Produktverbesserungen, die für eine spätere Produktversion geplant sind, aber aufgrund der Entscheidung des Produkt-Managements von [!DNL Adobe's] frühzeitig bereitgestellt werden.</li> <li>  Funktionen werden immer mit der nächsten Hauptversion zusammengeführt. Sie werden dann auf die kundenseitig benötigte [!DNL Experience Manager]-Version portiert. </li> <li>  Feature Packs mit Funktionen von allgemeinem Interesse und GA Feature Packs werden mit dem nächsten Service Pack zusammengeführt  </li> </ul> |
| Namenskonvention | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Lieferumfang | <ul> <li> Neue Funktionen </li> <li> Verbesserungen </li> <li> Fehlerbehebungen (inkrementelle Produktaktualisierungen) </li> </ul> |
| Dokumentation | Die Dokumentation ist unter adobe.com/de verfügbar. |
| Veröffentlichungsintervall | Abhängig vom Produktbereich |
| Verfügbarkeit und Installation | <ul> <li>Bereitstellung über Service Packs </li> <li> Verfügbar über Software Distribution. Kunden akzeptieren die Geschäftsbedingungen von [!DNL Adobe's] über Software Distribution. </li> </ul> |
| Teststufe | General Availability Feature Packs werden durch die Qualitätssicherung validiert. |

* 1: Oak-Fehlerbehebungen werden nicht als individuelle Hotfixes bereitgestellt. Sie sind jedoch im Lieferumfang des nachfolgenden Cumulative Oak Hot Fix enthalten. Bei Bedarf kann ein Diagnose-Build zusätzlich zum aktuellen COFP bereitgestellt werden. Eine Vorbedingung hierfür ist, dass auf Kundenseite das aktuelle COFP ausgeführt wurde. Diagnose-Builds bieten nur die Qualitätssicherungsstufe eines Hotfix. Sie bieten daher nicht dieselbe Qualitätssicherungsstufe wie ein Cumulative Fix Pack, ein Service Pack oder eine Produktversion. Die endgültige Fehlerbehebung wird mit dem nächsten CFP bereitgestellt.
