---
title: Documentbeveiligingsextensie voor Microsoft Office installeren en configureren AEM
description: Dit document begeleidt u door het installeren en configureren van Adobe Experience Manager Document Security Extension 6.2 voor Microsoft Office.
uuid: 9d7eb6bb-4780-4d82-8657-7c6c6d523af0
content-type: reference
topic-tags: installing
discoiquuid: f1cdf344-efe4-4cb5-9fc3-47ee4ba5faf4
exl-id: 88759737-d57f-4354-951e-ad9f62d0a872
source-git-commit: 28137f26afc024d411857d44887bf69fe1ee2b81
workflow-type: tm+mt
source-wordcount: '2764'
ht-degree: 0%

---

# Documentbeveiligingsextensie voor Microsoft Office installeren en configureren AEM{#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Dit document begeleidt u door het installeren en configureren van Adobe Experience Manager Document Security Extension voor Microsoft Office.

Dit document bevat informatie over de volgende taken:

* Documentbeveiligingsextensie installeren voor Microsoft Office
* Het installatieprogramma vooraf configureren om te wijzen naar de invoegtoepassing LiveCycle Rights Management ES2 of hoger of Documentbeveiliging voor AEM 6.0 Forms of hoger.
* De automatische toepassing van standaardbeleid configureren

## Voordat u gaat installeren {#before-you-install}

Controleer voordat u Document Security Extension for Microsoft Office installeert of:

* U hebt de [Opmerkingen bij de release](document-security-extension-release-notes.md).
* Microsoft Office is geactiveerd. Het dialoogvenster Activering wordt niet weergegeven bij het openen van Microsoft Office-toepassingen.
* De nieuwste servicepacks voor Microsoft Windows en Microsoft Office zijn geïnstalleerd.
* Als u Documentbeveiliging voor Microsoft Office installeert voor een niet-ondersteunde taal, opent u de Office-toepassing minstens één keer.

>[!NOTE]
>
>Installeer de software niet in een map waarvan de naam double-bytetekens bevat. Als u dit doet, wordt het menu AEM Documentbeveiliging niet weergegeven in Microsoft Office.

>[!NOTE]
>
>Het installeren van een 32-bits versie van de extensie Documentbeveiliging op een 64-bits besturingssysteem wordt ondersteund, maar de tegenovergestelde manier wordt niet ondersteund. U kunt geen 64-bits versie van de extensie Documentbeveiliging voor Microsoft Office installeren op een 32-bits besturingssysteem.

### McAfee VirusScan uitschakelen&amp; {#disable-mcafee-virusscan}

Om ervoor te zorgen dat Office-toepassingen probleemloos starten op een computer waarop Documentbeveiligingsextensie is geïnstalleerd en McAfee VirusScan is ingeschakeld met On-Access Scan, schakelt u de optie Buffer Overflow Protection uit in de McAfee VirusScan-console.

### Plug-ins van derden verwijderen {#uninstall-third-party-plug-ins}

AEM Document Security Extension for Microsoft Office biedt geen ondersteuning voor plug-ins van derden voor Microsoft Office-toepassingen. Aangezien deze extensie een conflict veroorzaakt met plug-ins van derden, moet u eventuele niet-Adobe plug-ins voor Microsoft Office verwijderen voordat u Documentbeveiliging voor Microsoft Office installeert. Adobe biedt geen ondersteuning voor Document Security voor Microsoft Office-toepassingen waarbij plug-ins van derden zijn geïnstalleerd.

## Systeemvereisten {#system-requirements}

### Extensie Documentbeveiliging {#document-security-extension-client}

Controleer de volgende minimale configuraties waarop u Documentbeveiligingsextensie wilt installeren:

* 32-bits of 64-bits versies van Microsoft Windows 7 of Windows 10 in het Engels, Frans, Duits, Japans, Italiaans, Spaans, Braziliaans Portugees, Koreaans, Vereenvoudigd Chinees of Traditioneel Chinees.
   **Opmerking:** *Van de de veiligheidsuitbreiding van het document voor Microsoft Office wordt ook verwacht dat het aan de apparaten van de Oppervlakte van Microsoft werkt.*

* 32-bits of 64-bits versies van Microsoft Office 2013, 2016, 2019 en Microsoft Office-bureaubladtoepassingen die zijn geïnstalleerd als onderdeel van Office 365 in het Engels, Frans, Duits, Japans, Italiaans, Spaans, Braziliaans Portugees, Koreaans, Vereenvoudigd Chinees of Traditioneel Chinees.

   **Opmerking**: *AEM Document Security Extension for Microsoft Office biedt geen ondersteuning voor plug-ins van derden voor Microsoft Office-toepassingen. Aangezien deze extensie mogelijk conflicteert met plug-ins van derden, moeten niet-Adobe plug-ins voor Microsoft Office-toepassingen worden verwijderd voordat documentbeveiligingsextensie voor Microsoft Office kan worden geïnstalleerd. Adobe biedt geen ondersteuning voor Document Security Extensions voor Microsoft Office-toepassingen waarop plug-ins van derden zijn geïnstalleerd.*

* 1,3-GHz processor of hoger
* 2 GB RAM
* 100 MB beschikbare ruimte op de vaste schijf

### Documentbeveiliging {#document-security}

Als u de Extensie van de Veiligheid van het Document wilt gebruiken, zorg ervoor dat u met Adobe LiveCycle Rights Management ES2 en recenter of de Toevoeging van de Veiligheid van het Document voor AEM 6.0 vormen of later kunt verbinden.

## Documentbeveiligingsextensie installeren voor Microsoft Office {#installing-document-security-extension-for-microsoft-office}

U kunt het installatieprogramma downloaden via het dialoogvenster [downloadpagina](download-installer.md). U kunt het uitvoerbare bestand van het installatieprogramma niet rechtstreeks aanpassen, maar u kunt het interactief of in de stille modus installeren. Meld u als beheerder aan bij Windows om de software te installeren.

Afzonderlijke installatieprogramma&#39;s zijn beschikbaar voor 32-bits en 64-bits versies van Microsoft Office. Voor versie met 32 bits van Microsoft Office, download DocumentSecurityExtensionforMicrosoftOffice.exe. Voor versie met 64 bits van Microsoft Office, download DocumentSecurityExtensionforMicrosoftOffice64.exe.

>[!NOTE]
>
>Dit document gebruikt het installatiedossier met 32 bits (DocumentSecurityExtensionforMicrosoftOffice.exe) om diverse bevelen en opties te verklaren. Als u versie met 64 bits van Microsoft Office gebruikt, gebruik het installatiedossier met 64 bits (DocumentSecurityExtensionforMicrosoftOffice64.exe) om verrichtingen uit te voeren die in dit document worden vermeld.

### Installeren in de stille modus {#install-in-silent-mode}

Een hulpprogramma voor het uitpakken van bestanden, zoals WinZip, gebruiken `DocumentSecurityExtensionforMicrosoftOffice.exe` uit het installatiebestand. Open de opdrachtprompt, ga naar de map die het instellingenbestand bevat en typ de volgende tekst:

`DocumentSecurityExtensionforMicrosoftOffice.exe -s -a -s -v" /qn"`

Het installatieprogramma is ook beschikbaar als een MSI-bestand dat kan worden gebruikt voor aanpassing.

### Een MSI-bestand installeren in de stille modus {#install-an-msi-file-in-silent-mode}

1. Gebruik een hulpprogramma voor het ophalen van bestanden, zoals WinZip, om het `DocumentSecurityExtensionforMicrosoftOffice.msi` bestand uit het ZIP-bestand.

1. Open de bevelherinnering, ga naar de omslag die het MSI dossier bevat, en typ de volgende tekst:

   `msiexec /I DocumentSecurityExtensionforMicrosoftOffice.msi /qn`

## Het installatieprogramma configureren voor verbinding met documentbeveiliging {#preconfiguring-the-installer-to-connect-to-document-security}

U kunt het installatieprogramma van de Extensie van de Veiligheid van het Document voor het installatieprogramma van Microsoft Office vooraf vormen om aan een LiveCycle of AEM server te richten zodat de gebruikers die de Uitbreiding van de Veiligheid van het Document voor Microsoft Office installeren de eigenschappen kunnen gebruiken zonder een verbinding te vormen. Daarom kunnen gebruikers beveiligde documenten zonder configuratie openen. Ze kunnen nieuwe documenten echter pas beschermen als ze de client configureren voor het gebruik van een bepaalde server.

In de volgende stappen wordt beschreven hoe u een MSI-bestand maakt en configureert. Dit MSI-bestand bevat de registerwaarden die vereist zijn om het installatieprogramma voor documentbeveiliging voor Microsoft Office vooraf te configureren naar de LiveCycle- of AEM-server die in uw bedrijf is geïnstalleerd.

### Vereisten voor het aanpassen van het installatieprogramma {#prerequisites-for-customizing-the-installer}

Gebruik de Orca-database-editor om het installatieprogramma aan te passen. De volgende stappen beschrijven hoe te om een douaneMSI dossier tot stand te brengen door een exemplaar van het MSI installatiedossier te wijzigen gebruikend de Orca gegevensbestandredacteur. Orca is beschikbaar als deel van Vensters SDK voor de Server 2008 van Vensters en .NET Kader 3.5.

<!--

For more information about how to edit Microsoft Windows® Installer files using Orca, see [Microsoft Support](http://support.microsoft.com/kb/255905/EN-US/).

-->

>[!NOTE]
>
>Het wordt aanbevolen een volledige back-up te maken van alle installatiebestanden voordat u het aangepaste MSI-bestand maakt.

#### Orca installeren {#install-orca}

1. Download Vensters SDK voor de Server 2008 van Vensters en .NET Kader 3.5.
1. Dubbelklik op het bestand Orca.msi in de map \Microsoft SDK\bin.

   U hebt ook de MSI-variant van het installatiebestand nodig. Neem contact op met de Adobe-ondersteuning voor de nieuwste versie van het MSI-installatieprogramma.

   >[!NOTE]
   >
   >Sluit altijd het bestand DocumentSecurityExtensionforMicrosoftOffice.msi voordat u het installatieprogramma uitvoert. U kunt het installatieprogramma niet uitvoeren als Orca het MSI-bestand gebruikt.

### Het MSI-bestand maken en configureren {#create-and-configure-the-msi-file}

1. Klikken **[!UICONTROL Start > Programma&#39;s > Orca]**.

1. Klikken **[!UICONTROL Bestand > Openen]** en bladert u vervolgens naar de `DocumentSecurityExtensionforMicrosoftOffice.msi` bestand.

1. Selecteer Eigenschap in de lijst met tabellen (aan de linkerkant).

1. Bewerk de volgende waarden voor Naam die van toepassing zijn op de installatie van Rights Management of Documentbeveiliging in uw bedrijf.

<table>
 <tbody>
  <tr>
   <td><p><strong>K</strong><strong>e</strong><strong>y-naam</strong></p> </td>
   <td><p><strong>Beschrijving</strong></p> </td>
   <td><p><strong>K</strong><strong>e</strong><strong>Y-waarde standaard</strong></p> </td>
  </tr>
  <tr>
   <td><p><code>APS_SERVER_NAME</code></p> </td>
   <td><p>Weergavenaam.</p> </td>
   <td><p>Standaardserver</p> </td>
  </tr>
  <tr>
   <td><p><code>APS_SERVER_URL</code></p> </td>
   <td><p>URL hostserver.</p> </td>
   <td><p>https://default.corp.com:1234</p> </td>
  </tr>
 </tbody>
</table>

1. Selecteer Registratie in de lijst met tabellen (aan de linkerkant).

1. Bewerk de volgende waarde voor de sleutelnaam.

   | **Sleutelnaam** | **Beschrijving** | **Standaardwaarde toets** |
   |---|---|---|
   | `IsDefault` | De standaard APS-server. | Standaardserver |

1. Sla het gewijzigde bestand op in dezelfde map die het oorspronkelijke MSI-installatieprogramma bevat.

   >[!NOTE]
   >
   >Vaak wordt dezelfde bestandsnaam gebruikt als het oorspronkelijke MSI-bestand (bijvoorbeeld `DocumentSecurityExtensionforMicrosoftOffice.msi`).

## Het vormen automatische toepassing van een standaardbeleid {#configuring-automatic-application-of-a-default-policy}

Als onderdeel van de configuratie kunt u de automatische toepassing van een standaardbeleid zodanig configureren dat de documentbeveiligingsextensie voor Microsoft Office elk document beschermt dat wordt opgeslagen.

U kunt een van de volgende opties opgeven:

* Protect alle documenten met een standaardbeleid.
* Toestaan dat gebruikers een bestand optioneel in een niet-beveiligde indeling opslaan wanneer ze geen verbinding met de server kunnen maken. Met deze flexibiliteit kunt u rekening houden met gevallen waarin gebruikers documenten maken terwijl ze geen verbinding hebben met het netwerk (bijvoorbeeld tijdens een vliegtuig).

Nadat u de functie voor automatisch toepassen hebt ingeschakeld, wordt het document in de volgende gevallen beveiligd met het standaardbeleid:

* Gebruiker bewerkt een nieuw document en slaat dit op
* Gebruiker bewerkt en slaat een niet-beveiligd document op
* De gebruiker opent een toepassing die met een standaarddocument opent, uitgeeft, en dan bewaart het document

### Vorm automatisch toepassen beleidseigenschap in het MSI dossier  {#configure-the-auto-apply-policy-feature-in-the-msi-file}

Voordat u begint, configureert u het installatieprogramma zo dat het naar de LiveCycle- of AEM formulierserver wijst, zoals eerder in dit artikel wordt beschreven.

1. Klikken **[!UICONTROL Start > Programma&#39;s > Orca]**.

1. Klikken **[!UICONTROL Bestand > Openen]** en bladert u vervolgens naar de `DocumentSecurityExtensionforMicrosoftOffice.msi` bestand.

1. Selecteer Eigenschap in de lijst met tabellen (aan de linkerkant).

1. Bewerk de volgende waarden voor sleutelnamen die van toepassing zijn op de installatie van Rights Management of Documentbeveiliging in uw bedrijf.

<table>
 <tbody>
  <tr>
   <td><p><strong>Sleutelnaam</strong></p> </td>
   <td><p><strong>Beschrijving</strong></p> </td>
   <td><p><strong>K</strong><strong>e</strong><strong>Y-waarde standaard</strong></p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_IS_AUTO_ APPLY</code></p> </td>
   <td><p>Schakel de functie voor automatisch toepassen van beleid in of uit.</p> <p><code>1</code>: Inschakelen</p> <p>0: Uitschakelen</p> </td>
   <td><p>0</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_POLICY_I D</code></p> </td>
   <td><p>Het beleid GUID aan gebruik wanneer de nieuwe documenten worden bewaard. Is van toepassing op de functie Beleid automatisch toepassen.</p> </td>
   <td><p>Hexadecimale beleids-id als zichtbaar op de RM-server</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_SERVER_U RL</code></p> </td>
   <td><p>Server-URL.</p> </td>
   <td><p>default.corp.com</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_SERVER_P ORT_NO</code></p> </td>
   <td><p>Serverpoortnummer.</p> </td>
   <td><p>1234</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE</code></p> </td>
   <td><p>Hiermee wordt bepaald of documenten kunnen worden gemaakt zonder documentbeveiliging als de client geen contact kan opnemen met de server om het document te beveiligen bij de eerste keer opslaan.</p> <p>1: Onbeschermde opslaan toestaan </p> <p>0: Voorkomen dat er nieuwe documenten worden gemaakt wanneer de client geen contact kan opnemen met de server om het document op te slaan.</p> </td>
   <td><p>0</p> </td>
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>`AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE` Deze optie is handig wanneer u klanten wilt herinneren aan de beveiliging van alle documenten zonder hen daartoe te dwingen. Het is ook nuttig wanneer u weet dat de gebruikers documenten creëren terwijl losgemaakt van het netwerk. U wilt niet verhinderen dat ze documenten maken en opslaan.

1. Sla het gewijzigde bestand op in dezelfde map die het oorspronkelijke MSI-bestand bevat.

   >[!NOTE]
   >
   >Vaak wordt dezelfde bestandsnaam gebruikt als het oorspronkelijke MSI-bestand (bijvoorbeeld `DocumentSecurityExtensionforMicrosoftOffice.msi`).

## Automatische bescherming van nieuwe documenten mogelijk maken {#enabling-automatic-protection-of-new-documents}

De beheerder kan de mogelijkheid inschakelen om elk document dat een gebruiker opslaat, automatisch te beveiligen. De beheerder configureert de beleidsfunctie Automatisch toepassen in het installatieprogramma voor de extensie Documentbeveiliging voor Microsoft Office.

Als Beleid automatisch toepassen is ingeschakeld, worden alle documenten die de gebruiker opslaat beveiligd met het standaardbeleid. Deze actie is van toepassing in de volgende situaties:

* Wanneer een gebruiker een nieuw document maakt, bewerkt en opslaat.
* Wanneer een gebruiker een niet-beveiligd document opent, bewerkt en opslaat.

Voor informatie over het vormen Auto-apply beleid, zie [Een automatische toepassing van standaardbeleid configureren](installing-configuring-aemdsext.md#p-configuring-automatic-application-of-a-default-policy-p).

## Gebruikersinterface zonder lint inschakelen {#enable-ribbon-less-user-interface}

U kunt de gebruikersinterface zonder lint toelaten/onbruikbaar maken door montages in de Registratie van Vensters te wijzigen. Voer de volgende stappen uit om Registratie bij te werken en lint minder gebruikersinterface toe te laten:

1. Maak een back-up van het Windows-register voordat u de wijzigingen aanbrengt. Zie voor gedetailleerde instructies [Hoe te om het Register van Vensters te wijzigen](https://support.microsoft.com/en-us/kb/136393).
1. Navigeer in de Register-editor naar HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 of HKEY_LOCAL_MACHINE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0
1. Nieuwe benoemde Dword-waarde (32 bits) maken **HidePluginUI**.

1. Stel waarde van de eigenschap **HidePluginUI **eigenschap in op 1 om een gebruikersinterface zonder lint in te schakelen.

1. Sluit de Register-editor.

## Watermerk inschakelen voor afdrukken in Microsoft Excel {#enable-watermark-for-printing-in-microsoft-excel}

U kunt de registratiemontages van Vensters veranderen om dynamisch watermerk samen te maken met bestaande kopballen en footers. Met de registerinstellingen wordt het watermerk alleen tijdens het afdrukken beschikbaar gesteld. Voer de volgende stappen uit om het register bij te werken en watermerken tijdens het afdrukken in te schakelen:

1. Maak een back-up van het Windows-register voordat u de wijzigingen aanbrengt. Zie voor gedetailleerde instructies [Hoe te om het Register van Vensters te wijzigen](https://support.microsoft.com/en-us/kb/136393).
1. Navigeer in de Register-editor naar HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 of HKEY_LOCAL_MACHINE\WOW6432NODE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0
1. Een nieuwe registersleutel maken **WatermarkMode**.
1. Maak een DWORD in de registersleutel WatermarkMode. **WatermarkMode** en de waarde van DWORD instellen **WatermarkMode** tot **1**.

1. Sluit de registereditor.

>[!NOTE]
>
>In Windows Verkenner kunt u het menu Bestand of het contextmenu gebruiken om een Microsoft Excel-document te maken. Voor documenten die met opgegeven methoden zijn gemaakt, kan de afdrukdatum niet worden opgehaald of gewijzigd. Het is een beperking van Microsoft Excel. AEM watermerken voor documentbeveiliging zijn afhankelijk van de afdrukdatum van het document. Voor dergelijke documenten wordt het watermerk dus teruggezet naar een vorige datum. Bovendien blijven kop- en voetteksten niet behouden.

## Een aangepaste omslagpagina toevoegen aan een document {#coverpage}

Een gebruiker kan proberen het beveiligde document te openen op een computer waarop geen AEM insteekmodule Documentbeveiliging voor Microsoft Office is geïnstalleerd. Dergelijke machines kunnen het document niet openen. Op dergelijke computers kunt u een omslagpagina weergeven met instructies voor het downloaden AEM Document Security voor de insteekmodule Microsoft Office en andere informatie.

### Voordat u een omslagpagina configureert {#before-you-configure-a-cover-page}

* Maak een back-up van het bestand CommonResources.dll. Het standaardpad is:

   * **(Voor 32-bits kantoor op een 32-bits computer)** C:\Program Files\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(Voor 32-bits kantoor op een 64-bits computer)** C:\Program Files (x86)\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(Voor 64-bits kantoor op een 64-bits computer)** C:\Program Files\Adobe\Adobe Experience Manager Forms\Document Security Extension

* Zorg ervoor dat u Microsoft Visual Studio 2008 of later geïnstalleerd hebt. U kunt ook elk ander hulpprogramma gebruiken om de DLL-bestanden te bewerken.
* Extraheer het archief templates.zip. Het archief bevat .xlsx-, .docx- en .pptx-sjablonen voor de omslagpagina. Gebruik alleen sjablonen die zijn meegeleverd voor bestandstypen .xlsx, .docx en .pptx. U kunt uw eigen sjablonen maken voor andere bestandstypen. Pas sjablonen aan om aangepaste berichten en instructies op te nemen. U kunt template.zip vinden op:

[Bestand ophalen](assets/templates.zip)

### Structuur van het bestand CommonResources.dll {#structure-of-the-commonresources-dll-file}

Het bestand CommonResources.dll bevat informatie over de bronnensjablonen. Deze bevat twee naamid&#39;s TEMPLATE_FILE en RT_MANIFEST. Om een aangepaste omslagpagina in te schakelen, wordt de naam-id van de SJABLOON_FILE gewijzigd. De naam-id voor TEMPLATE_FILE heeft zes bronnen:

<table>
 <tbody>
  <tr>
   <td><p><strong>Resource</strong></p> </td>
   <td><p><strong>Vertegenwoordigt </strong></p> </td>
  </tr>
  <tr>
   <td><p>101 </p> </td>
   <td><p>.xls</p> </td>
  </tr>
  <tr>
   <td><p>102</p> </td>
   <td><p>.doc</p> </td>
  </tr>
  <tr>
   <td><p>103 </p> </td>
   <td><p>.ppt</p> </td>
  </tr>
  <tr>
   <td><p>104 </p> </td>
   <td><p>.xlsx</p> </td>
  </tr>
  <tr>
   <td><p>105</p> </td>
   <td><p>.docx</p> </td>
  </tr>
  <tr>
   <td><p>106</p> </td>
   <td><p>.pptx</p> </td>
  </tr>
 </tbody>
</table>

#### De sjabloon configureren als een omslagpagina {#configure-the-template-as-a-cover-page}

1. Open Microsoft Visual Studio. Blader naar het bestand CommonResources.dll en open het om het te bewerken.

   >[!NOTE]
   >
   >Als het dossier niet in het venster van de Ontdekkingsreiziger van de Oplossing verschijnt, open het dossier opnieuw gebruikend Open met optie. Selecteer de redacteur van het Middel als redacteur.

1. In het venster van de Ontdekkingsreiziger van de Oplossing, breid de folder TEMPLATE_FILE uit, en schrap middelen 101.

1. Voeg de bronnen toe:

   1. Met een project dat in de Ontdekkingsreiziger van de Oplossing, op het menu van het Project wordt geselecteerd, klik Eigenschappen.
   1. Selecteer het tabblad Bronnen.
   1. Voor de toolbar van de Ontwerper van het Middel, punt om Middel toe te voegen, klik de pijl. Voor middeltype, uitgezochte TEMPLATE_FILE, en klik de invoer.
   1. Blader in het dialoogvenster Bestaande bestanden toevoegen aan bronnen naar het bestand Resource.xlsx en klik op Openen. Het bestand wordt toegevoegd aan de map TEMPLATE_FILE.

   >[!NOTE]
   >
   >Controleer of de taalinstellingen correct zijn. Verwijder de bron met een neutrale taal.

1. Herhaal stap 2 en 3 voor alle typen bronnen.

   >[!NOTE]
   >
   >Verwijder en voeg geen middeltypes in willekeurige orde toe. Na 101, vorm 102, etc.

### Het aangepaste bestand CommonResources.dll verpakken met het installatieprogramma van AEM Document Security-extensie voor Microsoft Office  {#package-custom-commonresources-dll-file-with-the-installer-of-aem-document-security-extension-for-microsoft-office}

U kunt het bestand CommonResources.dll aanpassen en een aangepaste omslagpagina toevoegen. Nadat u het bestand hebt aangepast, kunt u het originele bestand handmatig vervangen door het aangepaste bestand op alle werkstations. U kunt ook een geautomatiseerde methode kiezen om het bestand te vervangen.

In een grote omgeving is het moeilijk en vervelend om de standaardinstelling handmatig te vervangen `CommonResources.dll file` met een aangepaste `CommonResources.dll` bestand. U kunt een zelfuitpakkend en verpakkingshulpmiddel (bijvoorbeeld, WinZip Zelfuitpakkend) gebruiken om het douaneCommonResources.dll- dossier met AEM Uitbreiding van de Veiligheid van het Document voor de installateur van Microsoft Office te verpakken. Later kunt u het aangepaste installatieprogramma naar alle werkstations distribueren. Deze methode verkort de tijd die nodig is om de standaardinstelling te vervangen `CommonResources.dll` met een aangepast bestand. Het zorgt ook dat al werkstation het vereiste dossier CommonResources.dll heeft. Het gereedschap Zelfuitpakken en verpakken is slechts een van de vele mogelijke methoden om een bestand automatisch te vervangen. U kunt elke methode kiezen die geschikt is voor uw omgeving.

U kunt de volgende stappen uitvoeren om aangepaste pakketten te maken `CommonResources.dll`bestand bij het installatieprogramma van AEM Document Security extension voor Microsoft Office:

1. Installeer een zelfextractor en een verpakkingshulpmiddel. Bijvoorbeeld WinZip Self-Extractor.
1. Maak een nieuwe map. UW_FOLDER_NAME
1. Plaats het oorspronkelijke installatieprogramma van AEM documentbeveiligingsextensie en het aangepaste bestand CommonResources.dll in de nieuwe map.
1. Maak een batchbestand in de map. UW_FOLDER_NAME\Installer.bat
1. Open het batchbestand voor bewerking en voeg de volgende code toe aan het batchbestand:

   ```shell
    @echo off
   
    setlocal EnableDelayedExpansion
   
    msiexec /i YOUR_FOLDER_NAME\MSI_NAME.exe
   
   
    FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\HARDWARE\DESCRIPTION\System\CentralProcessor\0" /v "Identifier"') DO set "IDENTIFIER=%%B"
   
    set IDENTIFIER= %IDENTIFIER: =%
   
    if not %IDENTIFIER:x86=%==%IDENTIFIER% (
   
    REM Fetching install path for 32 bit machine.
   
    FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0" /v "InstallPath"') DO set "INSTALLPATH=%%B"
   
    ) else (
   
        REM Fetching install path for 64 bit machine.
   
            FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\SOFTWARE\Wow6432Node\Adobe\LiveCycle Rights Management ES4\11.0.0" /v "InstallPath"') DO set "INSTALLPATH=%%B"
   
        )
   
    COPY "YOUR_FOLDER_NAME\CommonResources.dll" "%INSTALLPATH%"
   
    endlocal
   ```

   Als u een andere versie van LiveCycle of AEM Forms op JEE behalve LiveCycle Rights Management ES4 en versie als 11.0.0 gebruikt, vervang de weg van de registratiesleutel als volgt:

   * (Livecycle Rights Management ES2 en versie 9.0): *HKLM\SOFTWARE\Adobe/LiveCycle* *Rights Management ES2\9.0 *
   * (Livecycle Rights Management ES3 en versie 10.0)
   * (Livecycle Rights Management ES4 en versie 11.0) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0
   * (AEM 6.0 Forms op JEE en latere versies) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0

1. Vervang in de bovenstaande code alle instanties van UW_FOLDER_NAME door de naam van de map die u in stap 2 hebt gemaakt.
1. **(Voor AEM Document Security-extensie voor Microsoft Office-installatieprogramma met alleen de extensie .exe)** Vervang de volgende coderegel:

   `msiexec /i YOUR_FOLDER_NAME\MSI_NAME.msi`
with

   `START /w YOUR_FOLDER_NAME\APPLICATION_NAME.exe`

1. Sla het batchbestand op en sluit het.
1. Gebruik een zelfextractor en een verpakkingshulpprogramma om de map met het aangepaste bestand CommonResources.dll, het oorspronkelijke installatieprogramma van AEM Document Security-extensie voor Microsoft Office en het batchbestand te verpakken.

   >[!NOTE]
   >
   >Zorg ervoor dat het pakket voor zelfextractie is ingesteld op uitvoeren als beheerder en automatisch
   >Hiermee wordt het batchbestand uitgevoerd wanneer de extractie is voltooid.

Nu, is het zelf-extracterende installatieprogramma van AEM uitbreiding van de Veiligheid van het Document voor Microsoft Office pakketten douane CommonResources.dll- dossier en klaar voor distributie.
