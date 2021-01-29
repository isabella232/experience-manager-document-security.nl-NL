---
title: Documentbeveiliging AEM voor Microsoft Office - Opmerkingen bij de release
description: Lees de releaseopmerkingen voordat u AEM Document Security 6.2 Extension for Microsoft Office installeert.
uuid: f6ab73d4-ac4e-4fff-9bb8-917b75401653
content-type: reference
topic-tags: installing
discoiquuid: c9342c28-8289-4831-a613-4bc03431f557
translation-type: tm+mt
source-git-commit: 403b800eab086d131beb65a496836158778954ee
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---


# Documentbeveiliging AEM voor Microsoft Office - Opmerkingen bij de release{#aem-document-security-for-microsoft-office-release-notes}

## Nieuw in AEM Documentbeveiliging voor Microsoft Office {#whats-new-in-aem-document-security-for-microsoft-office}

* **Ondersteuning voor Office 2019**: De Uitbreiding van de Veiligheid van het document voor Microsoft Office heeft steun voor Microsoft Office 2019 toegevoegd. Het wordt ook verwacht om met Microsoft Office 2019 Desktoptoepassingen te werken die als deel van Bureau 365 worden geïnstalleerd.

>[!NOTE]
>
>Het document gebruikt onderling verwisselbaar de termen Adobe Experience Manager Document Security voor Microsoft Office, Adobe Experience Manager Document Security Extension voor Microsoft Office en Document Security Extension voor Microsoft Office.

## Installatie en configuratie AEM de Uitbreiding van de Veiligheid van het Document voor Microsoft Office {#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Deze versie van Document Security Extension voor Microsoft Office is compatibel met Adobe LiveCycle Rights Management ES2 en hoger en de Document Security Add-on voor AEM formulieren.

Controleer de informatie in dit document voordat u AEM Document Security Extension for Microsoft Office installeert. Voor gedetailleerde installatieinstructies, zie [Installatie en het Vormen AEM de Uitbreiding van de Veiligheid van het Document voor Microsoft Office](installing-configuring-aemdsext.md) artikel.

## {#fixed-issues} Opgeloste problemen

* Tekenreeksen worden verticaal weergegeven en er worden onjuiste regeleinden aan de inhoud toegevoegd. (Ref. CQ-4201054)

## Bekende problemen {#known-issues}

### Plug-ins van andere leveranciers worden niet ondersteund {#third-party-plug-ins-not-supported}

AEM de Uitbreiding van de Veiligheid van het Document voor Microsoft Office werkt niet met derdestop-ins. Verwijder eventuele plug-ins van andere leveranciers voor Microsoft Office voordat u Documentbeveiligingsextensie voor Microsoft Office installeert.

### Uitgeschakelde menuopties in Microsoft Word, Excel en PowerPoint {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

AEM de Uitbreiding van de Veiligheid van het Document voor Microsoft Office gebruikt ingebouwde beschermingseigenschappen om documenten, aantekenvellen, en presentaties te beschermen. Hiermee worden enkele opties in het menu Excel, Word en PowerPoint uitgeschakeld.

### Beperkingen voor Microsoft Office 2013, 2016 en 2019 {#restrictions-for-microsoft-office}

In Microsoft Office zijn de volgende opties niet beschikbaar tijdens een beveiligde sessie:

* Microsoft Office 2016 of Microsoft Office 2019

   * Bestand > Opslaan als
   * Bestand > Historie
   * Bestand > Delen
   * Bestand > Exporteren
   * Bestand > Publiceren
   * Bestand > Account
   * Bestand > Info > Protect-document/werkboek/presentatie > Coderen met wachtwoord
   * Bestand > Info > Protect-document > Een digitale handtekening toevoegen
   * Bestand > Info > Protect-document > Markeren als definitief
   * Optie Delen rechtsboven

* Microsoft Office 2013

   * Bestand > Opslaan als
   * Bestand > Delen
   * Bestand > Exporteren
   * Bestand > Account
   * Bestand > Info > Protect-document/werkboek/presentatie > Coderen met wachtwoord
   * Bestand > Info > Protect-document > Een digitale handtekening toevoegen
   * Bestand > Info > Protect-document > Markeren als definitief

### Een beveiligd document openen vanaf SharePoint-server {#opening-a-protected-document-from-sharepoint-server}

Het beveiligde document openen: Als u probeert om een beschermd document in de Uitbreiding van de Veiligheid van het Document voor Microsoft Office van de Server van SharePoint te openen zonder eerst het programma van Microsoft Office te openen verbonden aan het dossiertype, zoals Microsoft Word, Microsoft Excel, of Microsoft PowerPoint, kan het document niet openen. Er wordt een foutbericht weergegeven waarin wordt aangegeven dat u de toepasselijke plug-in installeert. Vandaar, wordt geadviseerd dat u het bijbehorende programma van Microsoft Office opent, alvorens u een beschermd document in de Uitbreiding van de Veiligheid van het Document voor Microsoft Office van de Server van SharePoint opent.

(Optioneel) U wordt aangeraden de cachemap te wissen voordat u een beveiligd document opent in Documentbeveiligingsextensie voor Microsoft Office vanuit SharePoint Server.

Wanneer u een beveiligd document opent vanuit SharePoint Server, worden alle machtigingen voor het document uitgeschakeld, ongeacht het beleid dat is toegepast.

### Pas een beleid met een dynamisch watermerk op Microsoft Excel 2013, Microsoft Excel 2016, en het dossier van Microsoft Excel 2019 toe zonder geïnstalleerde printer {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

Wanneer u een beleid met dynamisch watermerk op Microsoft Excel 2013, Microsoft Excel 2016, en het dossier van Microsoft Excel 2019 op een computer toepast die geen geïnstalleerde printers heeft en dan sparen het dossier, verschijnt de volgende fout: &quot;Interne fout bij het toepassen van een dynamisch watermerk.&quot; Deze fout treedt ook op wanneer u het beveiligde bestand opnieuw opent. Het watermerk wordt niet toegepast en is niet zichtbaar via Weergave > Pagina-indeling.

### De Preventie van de Uitvoering van Gegevens van Vensters voor gesteunde toepassingen {#disable-windows-data-execution-prevention-for-supported-office-applications} onbruikbaar

Men adviseert dat u het plaatsen van de Preventie van de Uitvoering van Gegevens van Vensters (DEP) onbruikbaar maakt wanneer het gebruiken van de Uitbreiding van de Veiligheid van het Document voor de toepassingen van Microsoft Office.

### Gedeelde Microsoft Office-bestanden kunnen niet worden beveiligd met Documentbeveiligingsextensie {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension}

Wanneer u een gedeeld Microsoft Office-bestand beveiligt met Documentbeveiligingsextensie, treedt een fout op en wordt het gedeelde bestand niet beveiligd.

### Office-toepassingen starten op een computer met documentbeveiligingsextensie voor Microsoft Office en McAfee VirusScan {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

Om ervoor te zorgen dat Office-toepassingen probleemloos starten op een computer waarop Documentbeveiliging is geïnstalleerd en McAfee VirusScan is ingeschakeld en On-Access Scan is ingeschakeld, schakelt u de optie Buffer Overflow Protection uit in de McAfee VirusScan-console.

### Documentbeveiligingsextensie voor Microsoft Office installeren op een computer met een niet-ondersteunde Microsoft Office-taal {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}

Voordat u de extensie Documentbeveiliging voor Microsoft Office installeert op een computer met een Microsoft Office-toepassing met een niet-ondersteunde taal, moet u de Office-toepassing minstens één keer openen.

### De knop Offline synchroniseren is ingeschakeld, zelfs als een gebruiker geen offlinerechten {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions} heeft

De knop Offline synchroniseren is beschikbaar, ook al heeft de gebruiker geen offline machtigingen voor het document. Het selecteren van de knop heeft echter geen effect.

### Geen ondersteuning voor proefversies van Microsoft Office {#no-support-for-trial-versions-of-microsoft-office}

De uitbreiding van de Veiligheid van het document voor Microsoft Office steunt spoorversies van Microsoft Office niet. Voordat u de extensie installeert, moet u controleren of u een exemplaar van Microsoft Office met licentie hebt geïnstalleerd en of deze geactiveerd is.

### Kan geen beveiligde Microsoft Office-bestanden openen {#unable-to-open-a-protected-microsoft-office-files}

Als de beveiligde weergave van Microsoft Office is ingeschakeld, kunnen met de Right Management Extension geen beveiligde Microsoft Excel-bestanden (XLS, XLSX) en beveiligde Microsoft PowerPoint-bestanden (PPT) vanaf een externe locatie worden geopend.

### De cellen van het document van Microsoft Excel die een beeld of achtergrondkleur bevatten verschijnen bovenop watermerk {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark}

Als een cel van een Microsoft Excel-document een afbeelding bevat of is gevuld met achtergrondkleur en er een dynamisch watermerkbeleid is toegepast op het document, wordt de afbeelding of de achtergrondkleur die in de cel is gevuld, boven op het watermerk weergegeven en bedekt het watermerk.

### Gebruiksprobleem met meerdere certificaten {#usability-issue-with-multiple-certificates}

Als er meerdere certificaten aanwezig zijn op de clientcomputer en de gebruiker het dialoogvenster voor certificaatselectie annuleert, wordt het dialoogvenster opnieuw weergegeven en moet de gebruiker het dialoogvenster tweemaal annuleren.

### Microsoft PowerPoint staat het bewerken van beveiligde documenten toe {#microsoft-powerpoint-allows-editing-protected-documents}

Als u probeert een beveiligd document te bewerken, wordt in Microsoft PowerPoint het volgende bericht weergegeven: &quot;U mag dit document niet wijzigen. U kunt uw wijzigingen niet opslaan.&quot;. Na het sluiten van het bericht kunnen gebruikers doorgaan met het toevoegen van tekst of het bewerken van het document. De wijzigingen die in de beveiligde documenten zijn aangebracht, worden echter niet opgeslagen.

Bovengenoemd gedrag is zoals verwacht in PowerPoint 2013, PowerPoint 2016 en PowerPoint 2019.
