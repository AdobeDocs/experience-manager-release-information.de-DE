---
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 3%
---
# Richtlinien für Beiträge zur Adobe Experience Manager-Dokumentation

## Dokumentationsphilosophie

Adobe Experience Manager-Anwender arbeiten in hart umkämpften Umgebungen und streben danach, digitale Erlebnisse zu schaffen, die sie von ihren Mitbewerbern unterscheiden. Wenn Adobe also erweiterte neue Tools in AEM einführt, bieten diese eine genaue und klare Dokumentation. Mit diesem Ansatz können Kunden sofort ihre AEM-Investitionen nutzen und den ROI maximieren.

Ziel der AEM-Dokumentation ist es, AEM-Benutzenden die Dokumentation so schnell wie möglich zur Verfügung zu stellen. Daher wird eine genaue, nutzbare Dokumentation erstellt und laufend aktualisiert und verbessert.

## Dokumentationsbeiträge

Im Interesse einer kontinuierlichen Verbesserung der AEM-Dokumentation ist die gesamte Community von AEM-Benutzenden herzlich eingeladen, zur Dokumentation beizutragen. Sei es durch Pull-Anfragen oder -Probleme, Verbesserungen an der Dokumentation können Korrekturen, Klarstellungen, Erweiterungen und mehr Beispiele sein.

## Dokumentationsstandards

Adobe begrüßt Beiträge zu der Dokumentation. Jeder Beitrag zur AEM-Dokumentation, ob eine Pull-Anfrage oder ein Problem, muss den Beitrags- und Dokumentationsstandards von Adobe entsprechen.

Beiträge, die diese Standards nicht erfüllen, können abgelehnt werden.

### Adobe schreibt über Standardanwendungsfälle.

Die Dokumentation zu AEM deckt Standardanwendungsfälle ab. Anwendungsfälle, die über den Umfang der Standardinstallation und -verwendung des Produkts hinausgehen, sind nicht Teil der Dokumentation zu AEM.

### Adobe dokumentiert im Allgemeinen keine Fehler oder Problemumgehungen.

Die Dokumentation zu AEM deckt Standardanwendungsfälle ab. Aus diesem Grund werden Fehler, durch Bugs verursachte Auswirkungen und Problemumgehungen für Bugs nicht dokumentiert.

Ausnahmen von dieser Regel gelten für die Versionshinweise, in denen bekannte Probleme mit möglichen Lösungen aufgelistet werden können, die von AEM Product Management genehmigt werden.

### Dokumentationsbeiträge dienen nicht zur Beantwortung technischer Fragen.

Alle Ideen, die Sie zur Verbesserung der AEM-Dokumentation haben, sind als Beiträge willkommen. Kommentare, Probleme und Pull-Anfragen sind jedoch nur für *Beiträge* vorgesehen. Sie sind nicht zur Beantwortung Ihrer Fragen über die Verwendung von AEM, Implementierung Ihres AEM-Projekts oder zur Lösung technischer Probleme gedacht.

Melden Sie Fragen zur Verwendung von AEM oder zu technischen Fehlern über das [Enterprise-Support-Portal für Experience Cloud](https://experienceleague.adobe.com/de?support-solution=General#support). Oder verwenden Sie die [Experience Manager-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community?profile.language=de).

***AEM-Dokumentationsbeiträge sind kein Ersatz für die Adobe-*** und Beiträge, die um Antwort auf Support-Fragen bitten, werden abgelehnt.

### Die Beiträge müssen klar auf die betroffenen Dokumentationsseiten verweisen.

Wenn Sie ein Problem erstellen, um Verbesserungen an der Dokumentation vorzuschlagen, fügen Sie Links zu den betroffenen Seiten ein. Wenn Sie ein Problem über den Link **Diese Seite bearbeiten** auf einer Dokumentationsseite erstellen, wird das Problem automatisch mit einem Link zur Seite erstellt.

Dieser Prozess gilt nicht für Pull-Anforderungen, da Pull-Anforderungen naturgemäß auf die betroffenen Seiten verweisen.

## Dokumentationsrichtlinien

Alle Beiträge zur Dokumentation müssen bestimmten Stilrichtlinien entsprechen.

Die Befolgung dieser Richtlinien erleichtert die Überprüfung Ihres Beitrags und beschleunigt somit die Integration in die Dokumentation.

### Sprache und Stil

#### Sprache

* Die AEM-Dokumentation wird in englischer Sprache verfasst und verwaltet.
* Halten Sie Sätze so einfach wie möglich.
* Halten Sie die Sprache klar und prägnant.

Denken Sie daran, dass die Leser der AEM-Dokumentation auf der ganzen Welt zu finden sind und von ihnen nicht erwartet werden kann, dass sie fließend Englisch beherrschen oder Muttersprachler sind. Umgangssprachliche Formulierungen vermeiden und die Sprache so klar und einfach wie möglich halten.

#### Folgen Sie dem Microsoft® Manual of Style

[The Microsoft® Manual of Style](https://learn.microsoft.com/en-us/style-guide/welcome/) ist ein kostenloses Stil-Handbuch zur Dokumentation von Software. Die AEM-Dokumentation folgt soweit möglich diesem Modell.

### Formatierung

| Element | Stil |
|---|---|
| Element oder Option der Benutzeroberfläche | **fett** |
| Dateiname, Pfad, Benutzereingabe, Parameterwerte | `monospaced` |
| Code, Befehlszeile | ```Code Block``` |

### Screenshots

Screenshots sind umsichtig und nur dann zu verwenden, wenn eine textliche Beschreibung nicht ausreicht.

Markierungen oder andere Anmerkungen in Screenshots (wie rote Rahmen, Pfeile oder Text) sollten nicht verwendet werden. Auf diese Weise können die Screenshots in lokalisierten Versionen der Dokumentation einfacher wiederverwendet oder repliziert werden.

### Versionsspezifische Verweise

Idealerweise sollten Sie direkte Verweise auf eine bestimmte Version im gesamten Dokumentationsinhalt vermeiden, wann immer möglich. Dieser Ansatz macht die Dokumentation flexibler und erweiterbar für zukünftige Versionen.

### Verwendung von Day, AEM, CQ, CRX

Wenn Sie das Produkt zum ersten Mal in einem Artikel erwähnen, verwenden Sie immer seinen vollständigen Namen **Adobe Experience Manager**. Danach können Sie sie als **AEM&quot;**.

Day, Day-Software, CQ und CRX sollten nur verwendet werden, wenn dies unvermeidlich ist, z. B. bei Klassennamen oder bei Verweisen auf die Historie von AEM.