---
title: Beveiliging-extensie AEM document gebruiken voor Microsoft&reg; Office
description: U kunt controleren hoe de ontvangers uw beleid-beschermde dossiers gebruiken, ongeacht hoe wijd u hen verspreidt. In dit document wordt uitgelegd hoe u bestanden kunt beschermen en hoe u met beveiligde bestanden kunt werken.
uuid: db4abbc8-eb21-4f4a-9950-224ada95ce66
content-type: reference
topic-tags: using
discoiquuid: f4c2460c-174f-4e4d-b804-1eb051d2781e
exl-id: 667a9718-b865-4911-96c2-7c08f75e0732
source-git-commit: f3456fa7243405a4986ac50540f8b578a6412a6c
workflow-type: tm+mt
source-wordcount: '6231'
ht-degree: 0%

---

# AEM Document Security Extension gebruiken voor Microsoft® Office{#using-aem-document-security-extension-for-microsoft-office}

## Protect-bestanden met AEM Document Security Extension {#usingaemdocumentsecurityextensiontoprotectfiles}

U kunt controleren hoe de ontvangers uw beleid-beschermde dossiers gebruiken, ongeacht hoe wijd u hen verspreidt.

Met Documentbeveiligingsextensie voor Microsoft® Office kunt u de volgende taken uitvoeren:

* Verbinding met documentbeveiliging configureren
* Een beleid toepassen op een bestand
* Open de webpagina&#39;s Documentbeveiliging om gebruikersbeleid te maken en te beheren
* Beleidsbescherming uit een bestand verwijderen
* Het beleid wijzigen dat wordt toegepast op een bestand
* Open de webpagina&#39;s Documentbeveiliging om de toegang tot bestanden in te trekken of om het beleid voor het bestand te wijzigen
* Open de webpagina&#39;s Documentbeveiliging om de auditgeschiedenis van het bestand weer te geven

### Verbinding maken met een documentbeveiligingsserver {#connect-to-a-document-security-server}

Als u beleid wilt toepassen op bestanden, moet u de verbindingsinstellingen configureren voor Documentbeveiliging. Afhankelijk van de manier waarop Documentbeveiligingsextensie voor Microsoft® Office is geïnstalleerd, hebt u mogelijk al standaardverbindingsinstellingen. U kunt verbindingsinstellingen toevoegen voor een of meer instanties van Documentbeveiliging. U kunt serverinformatie opvragen bij de documentbeveiligingsbeheerder.

Stel de server in die u wilt gebruiken om bestanden te beveiligen of om uw beveiligde bestanden te beheren als de standaardserver. Wanneer u een beleid toepast op een nieuw dossier of de Web-pagina&#39;s van de Veiligheid van het Document opent, verbindt de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office met de standaardserver. Als u bestanden beveiligt met meerdere instanties van Documentbeveiliging, moet u de standaardinstelling voor de server wijzigen wanneer u overschakelt tussen servers. U kunt bestanden openen die zijn beveiligd door elke instantie van Documentbeveiliging, zolang u over de machtiging beschikt om het bestand te openen.

Als op de documentbeveiligingsserver verificatie op basis van certificaten wordt toegepast, moet u het certificaat installeren dat u op uw lokale computer hebt ontvangen. U moet certificaatverificatie kiezen en het certificaat opgeven dat u wilt gebruiken voor verificatie.

Nadat u de verbindingsmontages voor een geval van de Veiligheid van het Document in één toepassing van Microsoft® Office vormt, wordt het gevormd voor elk van Word, Excel, en PowerPoint.

#### Het clientcertificaat installeren {#install-the-client-side-certificate}

Als u toegang moet krijgen tot de webpagina&#39;s voor documentbeveiliging via certificaatverificatie of tweerichtingsverificatie, ontvangt u het certificaat dat u op uw lokale computer moet installeren. U ontvangt een certificaatbestand (.PFX- of .P12-bestand) en het bijbehorende wachtwoord.

1. Sla het certificaatbestand op uw lokale computer op.
1. Dubbelklik op het certificaatbestand om de wizard Certificaat importeren te openen en klik op **Volgende**.
1. Klikken **Volgende** als het certificaatbestand wordt vermeld in het vak Bestandsnaam. Klikken **Bladeren** als u een ander certificaat wilt zoeken.
1. Voer het wachtwoord in dat u hebt ontvangen en klik op **Volgende**.
1. Selecteer Alle certificaten in de volgende winkel plaatsen in het dialoogvenster Certificaatarchief en klik op **Bladeren**.
1. Selecteer Persoonlijk in het dialoogvenster Certificaatarchief selecteren en klik op **OK**, klikt u op **Volgende** en klik vervolgens op **Voltooien**.

#### Verbindingsinstellingen configureren {#configure-connection-settings}

1. In Document Security Extension for Microsoft® Office 2010 and Office 2013, op de **Documentbeveiliging** tab, selecteert u **Server kiezen**.
1. Willekeurig klikken **Nieuw** om verbindingsmontages tot stand te brengen of een bestaande verbinding te selecteren en te klikken **Bewerken**.
1. Typ een naam voor de verbinding in het dialoogvenster **Naam** doos. U kunt elke gewenste naam gebruiken.
1. Typ het adres van de server in het dialoogvenster **Serveradres** doos.
1. Typ de serverpoort in het dialoogvenster **Poort** doos.
1. (Optioneel) Als u uw gebruikersnaam en wachtwoord wilt onthouden, selecteert u **Wachtwoord onthouden op deze computer** en typ uw gebruikersnaam en wachtwoord in de desbetreffende vakken. Het wordt aanbevolen deze optie niet in te schakelen als andere personen toegang hebben tot de computer.
1. Klikken **Verbinding maken met deze server**. Documentbeveiligingsextensie voor Microsoft® Office probeert verbinding te maken met de server die u hebt opgegeven. Voer afhankelijk van het opgegeven verificatietype een van de volgende handelingen uit:

   **Gebruikersnaam en wachtwoord**

   Voer de gebruikersnaam en het wachtwoord in die u van de documentbeveiligingsbeheerder hebt ontvangen.

   **Certificaatverificatie**

   Kies deze optie om het certificaat te selecteren dat u hebt ontvangen en in uw persoonlijke certificaatarchief hebt geïnstalleerd.

   Als er slechts één verificatietype is geconfigureerd in Documentbeveiliging, wordt alleen die optie weergegeven.

>[!NOTE]
>
>Als u geen verbinding kunt maken met de server, opent u de webpagina&#39;s voor documentbeveiliging in Internet Explorer. Als u geen verbinding met de server kunt maken via Internet Explorer of als er een waarschuwing over het servercertificaat wordt weergegeven, kan documentbeveiligingsextensie voor Microsoft® Office geen verbinding met de server maken. Neem contact op met de serverbeheerder voor hulp.

>[!NOTE]
Als u geen verbinding kunt maken met Documentbeveiliging, wordt een bericht weergegeven met de melding dat de gebruikersnaam en het wachtwoord onjuist zijn. Controleer de configuratie-instellingen en probeer het opnieuw. Dit bericht wordt mogelijk weergegeven als u om een andere reden geen verbinding kunt maken. Als u voor het eerst verbinding maakt met de server, controleert u of u de servernaam en poort correct hebt ingesteld.

#### De standaardserver opgeven {#specify-the-default-server}

1. Ga als volgt te werk:

   * In Document Security Extension for Microsoft® Office 2010 and Office 2013 on the **Documentbeveiliging** tab, selecteert u **Server kiezen**.

1. Selecteer een server die u als standaard wilt opgeven en klik op **Standaardwaarde instellen**. Er wordt een sterretje weergegeven naast de standaardserver.

### Het gebruiken van de leveranciers van de authentificatie van de Derden {#using-third-party-authentication-providers}

U kunt externe verificatieproviders gebruiken met AEM Forms Document Security. Met deze verificatieproviders kunt u een extra toegangslaag toevoegen aan de beveiligde documenten. AEM Forms-documentbeveiliging ondersteunt de volgende uitgebreide verificatieworkflows:

* Uitgebreide verificatie met standaard AEM Forms URL
* Uitgebreide verificatie met een aangepaste URL
* Standaard uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms op JEE-server
* Aangepaste uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms op JEE-server
* Uitgebreide verificatie met behulp van aangepaste pagina voor SAML-verificatie

#### Uitgebreide verificatie met standaard AEM Forms URL {#extended-authentication-using-default-aem-forms-url}

U kunt standaard AEM Forms URL voor uitgebreide authentificatie gebruiken. De standaardlandingspagina bevat branding van Adobe. Bovendien worden standaard AEM Forms-instellingen gebruikt voor het gebruik van standaard AEM Forms URL voor uitgebreide verificatie.

Voer de volgende stappen uit om uitgebreide verificatie in te schakelen met de standaard Adobe Landing URL:

1. Open AEM Forms Admin UI.
1. Ga naar Services > Documentbeveiliging > Configuratie > Serverconfiguratie.
1. Schakel de optie Uitgebreide verificatie toestaan in.
1. Geef de standaard URL voor het porteren van URL voor uitgebreide verificatie op. De standaard-URL is http://localhost:8080/edc/extendedauthentication/welcome.jsp.

   Klikken **[!UICONTROL Opslaan]**.

   >[!NOTE]
   Gebruik een volledig gekwalificeerde hostnaam in de URL. U wordt aangeraden het HTTPS-protocol te gebruiken.

   Nu is de beveiliging van AEM Forms-documenten geconfigureerd voor uitgebreide verificatie met de standaard AEM Forms-landings-URL.

   ![](assets/third-party-authentication.png)

#### Uitgebreide verificatie met een aangepaste bestemmings-URL {#extended-authentication-with-a-custom-landing-url}

U kunt een aangepaste URL voor uitgebreide verificatie gebruiken. Het biedt de flexibiliteit om een aangepaste verificatiepagina met aangepaste branding weer te geven. Bijvoorbeeld branding voor uw organisatie.

U kunt de aangepaste verificatiepagina in een oorlogsbestand verpakken en het oorlogsbestand op AEM Forms Server implementeren. Het oorlogsdossier bevat volledige logica om gebruikersgeloofsbrieven goed te keuren en tegen de Server van AEM Forms voor authentiek te verklaren. AEM Forms Document Security heeft de volgende vereisten voor de aangepaste verificatiepagina:

* De verificatiepagina moet gebruikersnaam als j_username en wachtwoord verzenden als j_password. De pagina moet de parameters source_url en login_url ook als verborgen verzenden.
* Na geslaagde verificatie moet de pagina automatisch worden gesloten.

Uitgebreide verificatie inschakelen met een aangepaste bestemmings-URL:

1. Implementeer het aangepaste oorlogsbestand voor verificatie naar AEM Forms Server.
1. Open AEM Forms Admin UI.
1. Ga naar Services > Documentbeveiliging > Configuratie > Serverconfiguratie.
1. Schakel de optie Uitgebreide verificatie toestaan in en geef de aangepaste URL voor het parseren van de uitgebreide verificatie op.
1. Voeg de volgende ingangen aan config.xml- dossier onder de knoop SSO na ingang toe *&lt;node name=&quot;AllowedUrls&quot;>*:

   >[!NOTE]
   &lt;entry key=&quot;sso-l&quot; value=&quot;/ sample_/login.jsp&quot; />!discoiqbr!&lt;entry key=&quot;sso-s&quot; value=&quot;/ sample_/welcome.jsp&quot;>!discoiqbr!&lt;entry key=&quot;sso-o&quot; value=&quot;/ sample_/logout.jsp&quot; />!discoiqbr!

   Voor geleidelijke informatie bij het bijwerken van het config.xml- dossier, zie [Het configuratiebestand voor documentbeveiliging handmatig bewerken](https://helpx.adobe.com/aem-forms/6-3/admin-help/configuring-client-server-options.html#manually_editing_the_document_security_configuration_file).

   Nu is de beveiliging van AEM Forms-documenten geconfigureerd voor uitgebreide verificatie met een aangepaste bestemmings-URL

#### Standaard uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms Server {#default-extended-authentication-workflow-with-third-party-identity-providers-configured-on-aem-forms-server}

Voor uitgebreide verificatie kunnen verschillende typen verificatie worden gebruikt die beschikbaar zijn op AEM Forms Server. SAML, [Meer voorbeelden].

Opmerking: Als de leveranciers van SAML op de Server van AEM Forms worden gevormd, dan alvorens het landen URL te tonen, wordt een pagina getoond die alle identiteitsleveranciers bevat die voor de authentificatie van SAML worden gevormd.

Het volgende scherm wordt weergegeven wanneer een beveiligd document wordt geopend in Acrobat.

#### Aangepaste uitgebreide verificatieworkflow wanneer SAML-providers zijn geconfigureerd op AEM Forms Server {#custom-extended-authentication-workflow-when-saml-providers-are-configured-on-aem-forms-server}

Als de leveranciers van SAML op de Server van AEM Forms worden gevormd, dan alvorens het landen URL te tonen, wordt een pagina getoond die alle identiteitsleveranciers bevat die voor de authentificatie van SAML worden gevormd.

De voorwaarden om een douane uitgebreide authentificatiewerkschema te vormen wanneer de leveranciers van SAML op de Server van AEM Forms worden gevormd zijn:

* SAML-verificatie is geconfigureerd op AEM Forms Server
* De oorlog van de douane, die een pagina van de douaneauthentificatie en volledige logica bevat om gebruikersgeloofsbrieven goed te keuren en tegen de Server van AEM Forms voor authentiek te verklaren, wordt opgesteld aan de Server van AEM Forms.

#### Aangepaste pagina gebruiken voor SAML-verificatie {#using-custom-page-for-listing-saml-authentications}

U kunt ook een aangepaste pagina weergeven met alle verificatieproviders die op AEM Forms Server zijn geconfigureerd. Zo&#39;n pagina maken:

1. Verpak de pagina van de douaneauthentificatie in een oorlogsdossier en stel het oorlogsdossier aan de Server van AEM Forms op. Het oorlogsdossier bevat volledige logica om gebruikersgeloofsbrieven goed te keuren en tegen de Server van AEM Forms voor authentiek te verklaren.
1. Open de gebruikersinterface van AEM Forms Admin en navigeer naar **[!UICONTROL Instellingen]**> **[!UICONTROL Gebruikersbeheer]** > **[!UICONTROL Configuratie]** > **[!UICONTROL Instellingen SAML Service Provider]**.
1. Voeg het volgende toe aan het veld Aangepaste eigenschappen en klik op **[!UICONTROL Opslaan]**.

   *saml.sp.discRecovery.url=/demoJSP/saml_discovery.jsp*

   Nu, wordt de documentveiligheid van AEM Forms gevormd om een douanepagina te tonen die alle gevormde authentificatieleveranciers bevat.

### Een gebruikersaccount aanvragen {#obtaining-a-user-account}

Als u nog geen account voor documentbeveiliging hebt, kan Documentbeveiliging het registratieproces starten wanneer deze gebeurtenissen zich voordoen:

* Een gebruiker van de Veiligheid van het Document die u een beleid-beschermd dossier wil verzenden voegt u aan een beleid toe.
* De beheerder van de Veiligheid van het Document leidt tot een rekening voor u.

Nadat u zich hebt geregistreerd en uw account hebt geactiveerd, kunt u met beleid beveiligde bestanden gebruiken waarvoor u toestemming hebt gekregen om deze te gebruiken.

>[!NOTE]
Als u een bestand ontvangt dat met een beleid is beveiligd en geen account voor documentbeveiliging hebt, of als u een uitnodiging tot registratie ontvangt, neemt u contact op met de persoon die u het bestand voor hulp heeft gestuurd.

Als u een e-mailuitnodiging voor registratie ontvangt van Documentbeveiliging, kunt u zich registreren met de URL in de e-mail om de online registratiepagina te openen. Nadat je je hebt geregistreerd, ontvang je een tweede bericht over het activeren van je account.

#### Een externe gebruikersaccount verkrijgen {#obtain-an-external-user-account}

1. Open de registratie-e-mail voor documentbeveiliging. De URL die het bericht bevat, is een koppeling naar de pagina Registratie van externe gebruikers van documentbeveiliging. Als u geen registratiebericht ontvangt, contacteer de persoon die u het dossier voor hulp verzond.
1. Klik op de URL of kopieer deze en plak deze in uw browser.
1. Typ uw naam, organisatie en wachtwoord in de desbetreffende vakken. Uw wachtwoord kan elke combinatie van acht tekens zijn.

   >[!NOTE]
   Zorg ervoor dat u een wachtwoord kiest dat u gemakkelijk kunt onthouden. er is geen methode beschikbaar om vergeten wachtwoorden te vinden .

1. Klikken **Registreren**. Er wordt een bericht weergegeven waarin u wordt gevraagd uw e-mail te controleren op een activeringsbericht.
1. Open het bevestigingsbericht voor documentbeveiliging.
1. Klik op de URL die in het bericht wordt weergegeven.
1. Klik op de koppeling naar de aanmeldingspagina.
1. In de **Gebruikersnaam** typt u het e-mailadres dat u bij Documentbeveiliging hebt geregistreerd. Dit e-mailadres is uw standaardgebruikersnaam voor documentbeveiliging.
1. In de **Wachtwoord** typt u het wachtwoord dat u bij de registratie hebt gemaakt.
1. Klikken **Aanmelden**.

### Beleid maken en beheren {#creating-and-managing-policies}

Als u toestemming van de beheerder van de Veiligheid van het Document hebt, kunt u beleid tot stand brengen om op uw eigen dossiers op de pagina van het Beleid van de Web-pagina&#39;s van de Veiligheid van het Document van toepassing te zijn.

Sommige beleidsinstellingen die beschikbaar zijn voor het maken van beleid op de webpagina&#39;s Documentbeveiliging, worden niet ondersteund voor Word-, Excel- en PowerPoint-bestanden. In de volgende tabellen wordt beschreven hoe de beleidsmachtigingen worden toegewezen aan Word, Excel en PowerPoint-functies.

<table>
 <thead>
  <tr>
   <th><p>Machtigingen</p></th>
   <th><p>Word-, Excel- en PowerPoint-ondersteuning</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>Afdrukken &gt; Niet toegestaan</p></td>
   <td><p>Afdrukken van het bestand is niet toegestaan.</p></td>
  </tr>
  <tr>
   <td><p>Afdrukken &gt; Toegestaan</p></td>
   <td><p>U mag het bestand afdrukken.</p><p><strong>Opmerking</strong>: <i>Als een beleid de toestemming van het Exemplaar maar niet de toestemming van de Druk geeft, kan de inhoud die aan een ander dossier wordt gekopieerd worden gedrukt.</i></p></td>
  </tr>
  <tr>
   <td><p>Afdrukken &gt; Lage resolutie. Alleen</p></td>
   <td><p>Niet van toepassing.</p></td>
  </tr>
  <tr>
   <td><p>Wijzigen &gt; Alles</p></td>
   <td><p>Het bestand kan worden gewijzigd.</p><p>Als deze machtiging niet is gegeven, kunt u beveiligde Word- en Excel-bestanden niet wijzigen. U kunt PowerPoint-bestanden wijzigen, maar u kunt de wijzigingen of presentaties voor gewijzigde bestanden niet opslaan.</p></td>
  </tr>
  <tr>
   <td><p>Wijzigen &gt; Niet toegestaan</p></td>
   <td><p>Gebruikers kunnen beveiligde bestanden niet wijzigen.</p></td>
  </tr>
  <tr>
   <td><p>Wijzigen &gt; Pagina's wijzigen</p></td>
   <td><p>Niet van toepassing.</p><p>Bevat het invoegen, verwijderen en roteren van pagina's.</p></td>
  </tr>
  <tr>
   <td><p>Wijzigen &gt; Fill &amp; Sign</p></td>
   <td><p>Niet van toepassing.</p></td>
  </tr>
  <tr>
   <td><p>Off line</p></td>
   <td><p>Het bestand kan offline worden geopend.</p></td>
  </tr>
  <tr>
   <td><p>Kopiëren</p></td>
   <td><p>Bestandsinhoud kan naar andere bestanden worden gekopieerd.</p></td>
  </tr>
  <tr>
   <td><p>Reader scherm </p></td>
   <td><p>Schermlezers (apparaten voor gebruikers met een visuele handicap) kunnen de bestandsinhoud lezen.</p></td>
  </tr>
  <tr>
   <td><p>Geldigheid machtiging</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <thead>
  <tr>
   <th><p>Algemene instellingen</p></th>
   <th><p>Word-, Excel- en PowerPoint-ondersteuning</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>Geldigheidsperiode</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Controledocument</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Automatische offline leaseperiode</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Externe machtigingsproviders</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <thead>
  <tr>
   <th><p>Geavanceerde instellingen</p></th>
   <th><p>Word-, Excel- en PowerPoint-ondersteuning</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>Dynamische watermerken</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Certificatie-plug-ins</p></td>
   <td><p>Niet van toepassing.</p></td>
  </tr>
  <tr>
   <td><p>Versleutelingsalgoritme en sleutellengte </p></td>
   <td><p>Alle opties worden ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Documentbeperking</p></td>
   <td><p>Alle bestandsinhoud wordt altijd versleuteld, ongeacht de instelling in het beleid.</p></td>
  </tr>
  <tr>
   <td><p>Foutbericht Toegang geweigerd</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
 </tbody>
</table>

Zie voor meer informatie over het maken en beheren van beleid [Help bij Eindgebruiker van documentbeveiliging](https://help.adobe.com/en_US/AEMForms/6.1/RMHelp/).

### Beleid toepassen {#applying-policies}

U kunt elk beschikbaar beleid toepassen op een bestand, inclusief het beleid dat u hebt gemaakt en het beleid dat deel uitmaakt van een beleidsset waartoe u toegang hebt. Voordat u een beleid toepast, moet u het bestand opslaan.

Nadat u een beleid toepast, wordt het toegevoegd aan de Recent Gebruikte lijst op het menu van de Veiligheid van het Document van het AEM om het voor u gemakkelijker te maken om uw het vaakst gebruikte beleid toe te passen. Als u meerdere instanties van Documentbeveiliging gebruikt, worden in de lijst Onlangs gebruikt alleen de beleidsregels weergegeven voor de server waarmee u momenteel bent verbonden of voor uw standaardserver als u zich nog niet hebt aangemeld bij een instantie van Documentbeveiliging.

>[!NOTE]
U kunt beleid slechts op het documentdossiers van Word (.doc, ook.docx en .docm in Microsoft® Office 2010 en 2013), het werkboekdossiers van Excel (.xls, ook .xlsx, en .xlsm in Microsoft® Office 2010 en 2013), en de presentatiedossiers van PowerPoint (.ppt, ook .pptx toepassen, en. .pptm in Microsoft® Office 2010 en 2013). U kunt geen beleid op de malplaatjedossiers van Word (.dot), de malplaatjedossiers van Excel (.xlt), en de dossiers van het het ontwerpmalplaatje van PowerPoint (.pot) toepassen.

#### Een beleid toepassen {#apply-a-policy}

1. In Document Security Extension for Microsoft® Office 2010 and 2013 on the **Documentbeveiliging** tab, selecteert u **Beveiligen > Beleid kiezen**.

   Als u gebruikersnaam en wachtwoord hebt gekozen als verificatiemethode op de server en nog geen aanmeldingsgegevens voor Documentbeveiliging hebt opgegeven, wordt u in een dialoogvenster gevraagd om uw gebruikersnaam en wachtwoord.

1. Selecteer een beleid in de lijst en klik op **Toepassen**.
1. Sla het bestand op.

#### Pas een onlangs gebruikt beleid toe {#apply-a-recently-used-policy}

1. In Document Security Extension for Microsoft® Office 2010 and 2013 gaat u naar de **Documentbeveiliging** tab, selecteer **Secure > ***[Beleidsnaam]*.
1. Sla het bestand op.

## Werken met de beleidsbeveiligde bestanden {#usingaemdocumentsecurityextensionpolicyprotectedfiles}

Bestanden die met een beleid zijn beveiligd, bevatten intellectuele eigendom die eigendom is van de uitgever van het bestand en die is beveiligd door Documentbeveiliging.

U kunt met beleid beveiligde bestanden gebruiken, ongeacht of dit interne of externe bestanden van de organisatie van de uitgever zijn. Als u met beleid beveiligde bestanden wilt openen, moet u worden herkend door Documentbeveiliging, door opname in een gekoppelde LDAP- of Active Directory-lijst, die wordt toegevoegd als een lokale gebruiker voor LiveCycle- of AEM-formulieren in JEE, of door te registreren bij Documentbeveiliging nadat u als gebruiker bent uitgenodigd.

Als u een bestand ontvangt dat met een beleid is beveiligd en geen account voor documentbeveiliging hebt, of als u een uitnodiging tot registratie ontvangt, neemt u contact op met de persoon die u het bestand voor hulp heeft gestuurd.

### Werken met bestanden die met een beleid zijn beveiligd in Microsoft® Office {#working-with-policy-protected-files-in-microsoft-office}

De Uitbreiding van de Veiligheid van het document voor Microsoft® Office beperkt bepaalde Word, Excel, en functionaliteit PowerPoint om het intellectuele bezit van de dossieruitgever te beschermen. Als u geen toestemming hebt om het bestand te wijzigen, kunt u er geen wijzigingen in opslaan.

Als u met een bestand werkt dat met een beleid is beveiligd, zijn bepaalde productfuncties mogelijk niet beschikbaar of werken deze mogelijk niet zoals gewoonlijk. Als u ook een niet-beveiligd bestand hebt geopend, zijn de meeste functies ingeschakeld voor het niet-beveiligde bestand, behalve de functies waarmee u inhoud kunt importeren of kopiëren uit een bestand dat met een beleid is beveiligd en waarvoor u geen kopieer- of exportmachtigingen hebt.

>[!NOTE]
Als u de Extensie-gesteunde toepassingen van het Bureau van de Veiligheid van het Document gebruikt, adviseert men dat u het plaatsen van Vensters DEP onbruikbaar maakt. Schakel ook de optie voor bufferoverloop in de McAfee VirusScan-console uit om ervoor te zorgen dat Office-toepassingen probleemloos starten op een computer waarop Documentbeveiligingsextensie is geïnstalleerd en McAfee VirusScan is ingeschakeld met On-Access Scan.

Als een functie niet beschikbaar is, zijn de opdrachtnaam in het menu en de bijbehorende werkbalkknop niet beschikbaar. Als u in Documentbeveiligingsextensie voor Microsoft® Office de muisaanwijzer boven de opdracht of knop houdt, geeft knopinfo aan dat de opdracht niet beschikbaar is gemaakt in Documentbeveiliging.

### Beleidsbeveiligde bestanden openen {#opening-policy-protected-files}

U kunt met beleid beveiligde bestanden openen met dezelfde methoden als voor het openen van andere bestanden. Als u zich nog niet hebt aangemeld bij Documentbeveiliging, wordt u gevraagd dit te doen, tenzij u geen verbinding hebt met internet en u het bestand offline kunt openen. Als u het aanmeldingsproces annuleert, wordt de toegang geweigerd.

Als u geen toestemming hebt om het bestand te openen, wordt u geïnformeerd dat de toegang wordt geweigerd. Als de toegangsrechten voor het bestand zijn ingetrokken, kunt u ook naar een bijgewerkte versie van het bestand worden geleid als er een beschikbaar is. Neem contact op met de bestandsuitgever als u geen bestand met een bestandsbeveiliging kunt openen dat is beveiligd met een beleid.

Wanneer een beveiligd bestand is geopend, wordt in de titelbalk die volgt op de bestandsnaam, aangegeven dat het bestand is beveiligd door AEM Documentbeveiliging.

Wanneer u een beveiligd document opent in Document Security Extension for Microsoft® Office vanaf SharePoint Server, moet u ervoor zorgen dat het Microsoft® Office-programma dat is gekoppeld aan het bestandstype, zoals Microsoft® Word, Microsoft® Excel of Microsoft® PowerPoint, is geopend. Als u het bestand probeert te openen zonder de bijbehorende toepassing te openen, wordt het document mogelijk niet geopend en wordt een foutbericht weergegeven dat u de toepasselijke plug-in moet installeren. Naast het openen van de vereiste toepassing, is het raadzaam de cachemap te wissen voordat u een beveiligd document opent in Document Security Extension for Microsoft® Office vanaf SharePoint Server. Wanneer u een beveiligd document opent vanaf SharePoint Server, worden bovendien alle machtigingen voor het document uitgeschakeld, ongeacht het beleid dat is toegepast.

Afhankelijk van de verificatiemethode die is geïmplementeerd op Documentbeveiliging, wordt u mogelijk gevraagd om de verificatiemethode te kiezen wanneer u een beveiligd document opent. Als Documentbeveiliging meerdere verificatiemethoden ondersteunt, worden de verificatieopties aan u getoond. Als de Document Security-server bijvoorbeeld zowel gebruikersnaam/wachtwoord als certificaatverificatie biedt, kunt u de juiste verificatiemethode kiezen. Als verificatie op basis van certificaten is ingeschakeld, wordt u gevraagd het certificaat te gebruiken dat u hebt ontvangen en geïnstalleerd.

De gebruikerservaring bij het openen van beveiligde bestanden is afhankelijk van de wederzijdse verificatieconfiguratie op de server. Als slechts één geldig clientcertificaat is geïnstalleerd, wordt er geen verificatiedialoogvenster weergegeven en worden de bestanden geopend. Als er echter meerdere clientcertificaten op een computer zijn geïnstalleerd, wordt er een dialoogvenster voor verificatie weergegeven. De gebruiker moet een geldig certificaat kiezen om het beveiligde bestand te openen.

### Beleidsbescherming uit een bestand verwijderen {#removing-policy-protection-from-a-file}

Als u dit toestaat, kunt u de beleidsbeveiliging verwijderen uit bestanden die u hebt beveiligd. Als u dit doet, wordt het bestand niet meer beveiligd door Documentbeveiliging.

1. In Document Security Extension for Microsoft® Office 2010 and 2013 gaat u naar de **Documentbeveiliging** tab, selecteert u **Verwijderen**.

   Als u nog geen aanmeldingsgegevens voor Documentbeveiliging hebt opgegeven, wordt u in een dialoogvenster gevraagd om uw gebruikersnaam en wachtwoord.

>[!NOTE]
Als u geen beleid kunt verwijderen uit een bestand dat u hebt beveiligd, neemt u contact op met de beheerder van documentbeveiliging.

### Beveiligingsinstellingen weergeven {#viewing-security-settings}

U kunt de machtigingen weergeven die u hebt voor het huidige bestand voor afdrukken, kopiëren, wijzigen en offline openen, en de geldigheidsperiode van het bestand.

In Document Security Extension for Microsoft® Office 2010 geeft de groep Security Status op het tabblad Documentbeveiliging uw machtigingen voor het bestand weer.

Ga als volgt te werk:

* In Document Security Extension for Microsoft® Office 2010 and 2013 gaat u naar de **Documentbeveiliging, tabblad** in de **Beveiligingsstatus** groep, klikt u op een item.

### Documenten opslaan wanneer Beleid automatisch toepassen is ingeschakeld {#saving-documents-when-auto-apply-policy-is-enabled}

Als de beheerder de functie voor automatisch toepassen heeft ingeschakeld, wordt elk document dat u maakt of bewerkt automatisch beveiligd wanneer u het document opslaat.

Als Beleid automatisch toepassen is ingeschakeld, wordt u gevraagd u aan te melden bij de Document Security Extension for Microsoft® Office. U moet uw gebruikersnaam en wachtwoord opgeven om door de server te worden geverifieerd. Als u de juiste aanmeldingsgegevens hebt opgegeven, wordt het document opgeslagen en beveiligd.

>[!NOTE]
Als u zich niet kunt aanmelden bij Documentbeveiliging, wordt het document mogelijk wel of niet opgeslagen. Dit hangt van af hoe uw Beheerder het Auto-apply beleid heeft gevormd. Vraag de beheerder hoe documenten in deze situatie worden verwerkt.

### Synchroniseren voor offline toegang {#synchronizing-for-offline-access}

Met beleidsregels kunt u bestanden openen terwijl u offline bent en geen verbinding hebt met Documentbeveiliging. U moet zich eerder bij de Veiligheid van het Document hebben aangemeld om uw geloofsbrieven met de server te vestigen alvorens u off-line kunt werken. Als u offline met bestanden wilt werken, is het raadzaam eerst met Documentbeveiliging te synchroniseren voordat u de verbinding verbreekt, om er zeker van te zijn dat de beleidsinstellingen voor uw bestanden up-to-date zijn met de server. U wordt aangeraden het bestand één keer online te openen voordat u het offline opent. Als u het bestand niet één keer online opent of synchroniseert met de server, kunt u mogelijk nog steeds met een beleid beveiligde bestanden gebruiken terwijl u offline bent. De offline leaseperiode mag echter niet zijn verlopen en de beleidsinstellingen voor het bestand mogen niet zijn gewijzigd sinds u de laatste keer handmatig of automatisch met de server hebt gesynchroniseerd.

Ga als volgt te werk:

* In Document Security Extension for Microsoft® Office 2010 and 2013 gaat u naar de **Documentbeveiliging** tab, selecteert u **Off line synchroniseren**.

   ***notitie**: De knop Off-line synchroniseren is beschikbaar, ook al heeft de gebruiker geen offline machtigingen voor het document. Het selecteren van de knop heeft echter geen effect. *

### Werken met dynamische watermerken {#working-with-dynamic-watermarks}

De Uitbreiding van de Veiligheid van het document voor Microsoft® Office steunt de opneming van dynamische tekst-gebaseerde watermerken in beleid-beschermde documenten. Een dynamisch watermerk kan informatie bevatten die kan worden gewijzigd, zoals de datum, de tijd, de gebruikersnaam of de naam van het beleid. Als een gebruiker een bestand afdrukt dat met een beleid is beveiligd en dat een dynamisch watermerk en de machtiging om af te drukken bevat, wordt het watermerk in de uitvoer weergegeven.

Documentbeveiligingsextensie ondersteunt geen uitgebreide watermerkfuncties, zoals watermerken op basis van PDF, meerdere elementen in een watermerk, tekstopmaakopties en paginabereik.

U maakt een dynamisch watermerk met gebruik van de webpagina&#39;s Documentbeveiliging. Voor meer informatie over het maken en opnemen van dynamische watermerken in een document dat met een beleid is beveiligd, raadpleegt u [Help bij Eindgebruiker van documentbeveiliging](https://www.adobe.com/go/learn_lc_euRightsMgmt_11).

Documentbeveiligingsextensie voor Microsoft® Office biedt ondersteuning voor de volgende watermerkfuncties:

<table>
 <thead>
  <tr>
   <th><p>Opties van het watermerk voor documentbeveiliging</p></th>
   <th><p>Word-, Excel- en PowerPoint-ondersteuning</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>Beleidsnaam</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Watermerknaam</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Als achtergrond gebruiken</p></td>
   <td><p>Het weergavegedrag van een dynamisch watermerk is hetzelfde, ongeacht of u de optie Als achtergrond gebruiken selecteert.</p><p>Voor Word 2010 en 2013 wordt een dynamisch watermerk alleen weergegeven in de afdrukweergave en in de afdrukweergave. </p><p>Voor Excel 2010 en 2013 wordt deze ook weergegeven in de weergaven Afdrukvoorbeeld en Pagina-indeling.</p></td>
  </tr>
  <tr>
   <td><p>Verticale positie</p></td>
   <td><p>Ondersteund</p></td>
  </tr>
  <tr>
   <td><p>Horizontale positie</p></td>
   <td><p>Ondersteund</p><p>Voor Excel 2010 en 2013 werkt het horizontaal plaatsen van watermerken met punten niet.</p></td>
  </tr>
  <tr>
   <td><p>Schalen</p></td>
   <td><p>Ondersteund</p></td>
  </tr>
  <tr>
   <td><p>Positie</p></td>
   <td><p>Ondersteund</p></td>
  </tr>
  <tr>
   <td><p>Dekking</p></td>
   <td><p>Ondersteund</p></td>
  </tr>
 </tbody>
</table>

### Webpagina&#39;s voor documentbeveiliging openen {#opening-the-document-security-web-pages}

U kunt de Web-pagina&#39;s van de Veiligheid van het Document openen om uw gebruikersbeleid tot stand te brengen en bij te werken en status en controleinformatie over uw beleid-beschermde dossiers te bekijken. U kunt ook de webpagina&#39;s Documentbeveiliging gebruiken om het beleid te wijzigen of om de toegang voor een bestand dat met een beleid is beveiligd, in te trekken.

U opent als volgt de webpagina&#39;s Documentbeveiliging in Document Security Extension for Microsoft® Office 2010 en 2013: **Documentbeveiliging** tab, selecteert u **Beleid maken en beheren**. Als u nog geen aanmeldingsgegevens hebt opgegeven, wordt de browser geopend op de aanmeldingspagina van de server.

### Beleid wijzigen {#changing-policies}

Als u machtigingen hebt, meestal als documentbeveiligingsbeheerder of de uitgever van het bestand, kunt u later een ander beleid toepassen op een bestand of de instellingen wijzigen van het beleid dat momenteel wordt toegepast.

Als u de instellingen voor een beleid wilt wijzigen, gebruikt u de webpagina&#39;s Documentbeveiliging.

1. Ga als volgt te werk:

   * In Document Security Extension for Microsoft® Office 2010 or 2013, op de knop **Documentbeveiliging** tab, selecteert u **Beveiligen > Beveiliging wijzigen**.

1. Selecteer een beleid in de lijst en klik op **Toepassen**.

### Toegangsrechten voor bestanden intrekken {#revoking-file-access-privileges}

U kunt de mogelijkheid intrekken om bestanden te openen die u hebt beveiligd. Wanneer u toegangsrechten voor een bestand intrekt, kunt u ook het bericht opgeven dat verschijnt voor iedereen die het bestand probeert te openen en de URL naar een bijgewerkte versie van het bestand als u het bestand vervangt door een gereviseerde kopie.

1. Ga als volgt te werk:

   * In Document Security Extension for Microsoft® Office 2010 and 2013 gaat u naar de **Documentbeveiliging** tab, selecteert u **Intrekken**.

   De webpagina&#39;s Documentbeveiliging worden geopend op de pagina Documenten intrekken.

1. Geef een bericht op dat moet worden weergegeven en, indien beschikbaar, een URL voor de bijgewerkte versie. Klik vervolgens op **OK**.

Voor meer informatie over het intrekken van de toegangsrechten voor bestanden raadpleegt u [Help bij Eindgebruiker van documentbeveiliging](https://help.adobe.com/en_US/AEMForms/6.1/RMHelp/).

Toegangsrechten kunnen opnieuw worden ingesteld via de webpagina&#39;s voor documentbeveiliging.

### De auditgeschiedenis van het bestand weergeven {#viewing-the-file-audit-history}

Met Documentbeveiliging kunt u de auditgeschiedenis opslaan voor bestanden die met een beleid zijn beveiligd, zodat u de handelingen kunt controleren die gebruikers op uw bestanden uitvoeren.

De gecontroleerde gebeurtenissen voor Word, Excel, en de dossiers van PowerPoint omvatten deze:

**Een nieuw document beveiligen** Beleid toegepast op een bestand

**Document weergeven** Bestand geopend

**Document sluiten** Bestand gesloten

**Document intrekken** Toegangsrechten verwijderd voor bestand

**Document intrekken** Toegangsrechten die aan het bestand zijn geretourneerd

**Document wijzigen** Bestand gewijzigd en lokaal opgeslagen

**Hoge resolutie afdrukken** Bestand afgedrukt

**Beveiligingshandler wijzigen** Beleidsbescherming uit bestand verwijderd

**Beleid op document schakelen** Nieuw beleid toegepast op bestand van de webpagina&#39;s Documentbeveiliging

### De auditgeschiedenis van een bestand weergeven {#view-the-audit-history-for-a-file}

In Document Security Extension for Microsoft® Office 2010 and 2013 gaat u naar de **Documentbeveiliging** tab, selecteert u **Controlegeschiedenis**.

De Web-pagina&#39;s van de Veiligheid van het Document openen aan de pagina van Gebeurtenissen, die gecontroleerde gebeurtenissen voor het huidige dossier toont.

### Beperkte functies in Microsoft® Office {#microsoft-office-restricted-features}

Om uw intellectuele eigendom te beschermen, zijn sommige functies van Microsoft® Office niet beschikbaar wanneer een bestand met beleidsbescherming is geopend. De lijst met niet-beschikbare functies is afhankelijk van de machtigingen die aan de huidige gebruiker zijn verleend. Sommige functies zijn alleen niet beschikbaar voor een beveiligd bestand en andere zijn niet beschikbaar voor alle bestanden wanneer u zich in een beveiligde sessie bevindt. Over het algemeen bevindt u zich in een beveiligde sessie vanaf het moment dat u een met een beleid beveiligd bestand opent tot u de toepassing sluit of de sessie verloopt.

De meeste beleidsregels verlenen volledige machtigingen aan de uitgever van het bestand. Andere gebruikers kunnen extra functiebeperkingen opmerken.

Als een opdracht niet beschikbaar is, worden de opdrachtnaam in het menu en de bijbehorende werkbalkknop grijs weergegeven.

>[!NOTE]
Als u een beleid toepast op een bestand dat een koppeling naar een ingesloten bestand bevat, wordt het beleid niet toegepast op het gekoppelde bestand. Documentbeveiliging voor Microsoft® Office breidt de beveiliging niet uit tot gekoppelde bestanden.

* Word-, Excel- en PowerPoint-bestanden die met een beleid zijn beveiligd, kunnen niet worden geopend in een browservenster van Internet Explorer.
* Gebruikers die alleen de machtiging Wijzigen hebben gekregen, kunnen geen inhoud kopiëren naar een bestand vanuit een andere toepassing met behulp van het Windows-klembord. Gebruikers kunnen inhoud naar bestanden kopiëren door de optie Microsoft® Office Clipboard in te schakelen.
* Als u een bestand opent dat met een beleid is beveiligd in Microsoft® Office, is de toets Print Screen niet beschikbaar totdat u de toepassing sluit of de sessie verloopt.
* Documentbeveiliging voor Microsoft® Office biedt geen ondersteuning voor WebDAV (Web-based Distributed Authoring and Versioning). Gewoonlijk kunt u geen met beleid beveiligd bestand openen vanuit een WebDAV-map. Als u een bestand kunt openen dat met een beleid is beveiligd, hebt u geen machtigingen om het bestand op te slaan, af te drukken, te wijzigen of te kopiëren.

De algemene veiligheid die op beleid-beschermde dossiers van toepassing is omvat de volgende beperkingen:

Veel veelvoorkomende functies kunnen tijdens een beveiligde sessie worden beperkt in Word, Excel en PowerPoint.

Als een bestand dat met beleid is beveiligd en dat de gebruiker niet toestaat wijzigingen aan te brengen, is geopend, zijn opdrachten die het bestand op een of andere manier wijzigen, niet beschikbaar. Alleen de opdrachten waarmee u documenten opent of maakt en de voorkeuren van de toepassing wijzigt, zijn beschikbaar.

#### Beperkingen in Word 2010 en Word 2013 {#word-2010-and-word-2013-restrictions}

Als u een bestand opent dat met een beleid is beveiligd in Word, is het niet mogelijk om automatisch herstelgegevens op te slaan totdat u Word sluit en opnieuw start. Bovendien zijn de hieronder vermelde kenmerken beperkt in de beschreven situaties:

**Bestand > Nieuw > Nieuw uit bestaand** Beschikbaar maar bestanden die met deze opdracht zijn gemaakt terwijl een bestand met een beleidsbeveiliging is geopend, kunnen niet worden opgeslagen. Inhoud in het nieuwe bestand kan niet naar een ander bestand worden gekopieerd.

**Bestand > Opslaan** Beperkt door de machtiging Wijzigen.

**Bestand > Opslaan als** Alle opties die zijn beperkt door de machtiging Wijzigen.

**Bestand > Afdrukken** Alle opties die zijn beperkt door de machtiging Afdrukken. Niet beschikbaar, tenzij het beleid afdrukken met hoge resolutie toestaat.

**Bestand > Opslaan en verzenden** Alle opties zijn niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Info > Protect-document > Coderen met wachtwoord, Digitale handtekening toevoegen, Markeren als definitief, Machtiging door personen beperken** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Workflows** Niet beschikbaar tijdens een beveiligde sessie.

***notitie **: De mogelijkheid om een workflow te starten vanuit de 2010 Microsoft® Office-systeemversies van Word, Excel en PowerPoint is alleen beschikbaar in de Office Professional Plus 2010-, Office Enterprise 2010- en Office Ultimate 2010-suites en in de zelfstandige Office-releaseversies van 2010 van deze programma&#39;s.*

**Blogbericht > Publiceren** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Server > Menu Bestandsservertaken** Niet beschikbaar tijdens een beveiligde sessie.

**Home > Clipboard > Copy** Beperkt door de machtiging Kopiëren. Als kopiëren niet is toegestaan, kan de gekopieerde inhoud niet in een ander dossier of aan het Klembord van het Bureau worden gekleefd. Inhoud kan binnen het beveiligde bestand worden gekopieerd als de gebruiker over wijzigingsmachtigingen beschikt.

**Home > Clipboard > Paste** Beperkt door de machtiging Wijzigen.

**Home > Klembord > Plakken speciaal** Beperkt door de machtiging Wijzigen.

**Invoegen > Tekst > Object** Niet beschikbaar tijdens een beveiligde sessie. Met een beleid beveiligde bestanden kunnen op geen enkel moment worden ingevoegd.

**Mabijen** De meeste opties op dit tabblad zijn niet beschikbaar tijdens een beveiligde sessie.

**Revisie > Proefdrukken > Onderzoek** Beperkt door de machtiging Kopiëren. Niet beschikbaar als kopiëren niet is toegestaan.

**Revisie > Proefdrukken > Synoniemenlijst** Beperkt door de machtiging Kopiëren. Niet beschikbaar als kopiëren niet is toegestaan.

**Reviseren > Taal > Vertalen > Document vertalen** Ingeschakeld met de machtiging Kopiëren.

**Reviseren > Taal > Vertalen > Geselecteerde tekst vertalen** Ingeschakeld met de machtiging Kopiëren.

**Revisie > Taal > Vertalen > Mini Vertaler** Ingeschakeld met de machtiging Kopiëren.

**Revisie > Vergelijken > Vergelijken** Niet beschikbaar tijdens een beveiligde sessie. Met een beleid beveiligde bestanden kunnen op geen enkel moment worden vergeleken.

**Controleren > Protect > Blokauteurs** Niet beschikbaar tijdens een beveiligde sessie.

**Revisie > Protect > Bewerken beperken** Niet beschikbaar tijdens een beveiligde sessie.

**Weergave > Macro&#39;s** Sommige macro&#39;s zijn beperkt door de machtiging Kopiëren en zijn alleen beschikbaar als kopiëren is toegestaan.

**Add-ins** Kan niet worden toegevoegd of verwijderd tijdens een beveiligde sessie.

**Online samenwerking** Niet beschikbaar tijdens een beveiligde sessie.

**Master en subdocumenten** Subdocumenten worden beheerst door het beleid voor master documenten wanneer ze worden geopend in het master document. Als subdocumenten afzonderlijk worden geopend, kunnen deze niet worden afgedrukt, gekopieerd of gewijzigd.

**Hervatten** Niet beschikbaar tijdens een beveiligde sessie.

**Frames (en alle bijbehorende opdrachten)** Niet beschikbaar tijdens een beveiligde sessie.

**Deelvenster Document** Niet beschikbaar tijdens een beveiligde sessie.

**Ontwikkelaar > Documentsjabloon** Niet beschikbaar tijdens een beveiligde sessie. U kunt deze opdracht openen door Bestand > Opties > Aanpassen > Tabblad Ontwikkelaar > Sjablonen > Documentsjabloon te selecteren.

**Omtrek > Master document > Subdocument maken, Subdocument invoegen** Niet beschikbaar tijdens een beveiligde sessie.

#### Beperkingen in Excel 2010 en Excel 2013 {#excel-2010-and-excel-2013-restrictions}

De onderstaande functies zijn beperkt in de beschreven situaties:

**Bestand > Nieuw > Nieuw uit bestaand** Beschikbaar, maar bestanden die tijdens een beveiligde sessie met deze opdracht zijn gemaakt, kunnen niet worden opgeslagen. Inhoud in het nieuwe bestand kan niet naar een ander bestand worden gekopieerd.

**Bestand > Opslaan als** Beperkt door de machtiging Wijzigen.

**Bestand > Opslaan als > PDF** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Afdrukken** Beperkt door de machtiging Afdrukken. Niet beschikbaar, tenzij het beleid afdrukken met hoge resolutie toestaat.

**Bestand > Info > Protect-document** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Info > Protect Workbook** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Opslaan en verzenden** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Opties > Add-ins** Kan niet worden toegevoegd of verwijderd tijdens een beveiligde sessie.

**Bestand > Workflows** Niet beschikbaar tijdens een beveiligde sessie.

***notitie **: De mogelijkheid om een workflow te starten vanuit de 2010 Microsoft® Office-systeemversies van Word, Excel en PowerPoint is alleen beschikbaar in de Office Professional Plus 2010-, Office Enterprise 2010- en Office Ultimate 2010-suites en in de zelfstandige Office-releaseversies van 2010 van deze programma&#39;s.*

**Bestand > Server > Menu Bestandsservertaken** Niet beschikbaar tijdens een beveiligde sessie.

**Home > Clipboard > Copy** Beperkt door de machtiging Kopiëren. Als kopiëren niet is toegestaan, kan gekopieerde inhoud niet in een ander bestand of op het Microsoft® Office-klembord worden geplakt. Inhoud kan binnen het beveiligde bestand worden gekopieerd als de gebruiker over wijzigingsmachtigingen beschikt.

**Home > Clipboard > Paste** Beperkt door de machtiging Wijzigen.

**Home > Klembord > Plakken speciaal** Beperkt door de machtiging Wijzigen.

**Home > Cellen > Opmaken > Blad verplaatsen of kopiëren** Niet beschikbaar tijdens een beveiligde sessie.

**Home > Cellen > Invoegen > Werkblad invoegen** Niet beschikbaar tijdens een beveiligde sessie.

**Home > Cellen > Verwijderen > Werkblad verwijderen** Niet beschikbaar tijdens een beveiligde sessie.

**Home > Bewerken > Vulling > Opzij werkblad** Beperkt door de machtiging Wijzigen.

**Invoegen > Tabellen > Tabel** Beperkt door de machtiging Wijzigen.

**Invoegen > Tabellen > draaitabel** Bestanden die met een beleid zijn beveiligd, kunnen niet worden geselecteerd in de wizard Creation.

**Invoegen > Tekst > Object** Niet beschikbaar tijdens een beveiligde sessie. Met een beleid beveiligde bestanden kunnen op geen enkel moment worden ingevoegd.

**Invoegen > Tekst > Koptekst en voettekst** Beperkt door de machtiging Wijzigen. Niet beschikbaar voor een document dat met een beleid is beveiligd.

**Gegevens > Externe gegevens ophalen** Gegevens uit bestanden die met een beleid zijn beveiligd, kunnen niet worden geïmporteerd.

**Gegevens > Omtrek > Subtotalen** Beperkt door de machtiging Wijzigen.

**Data > Data Tools > Data Validation** Beperkt door de machtiging Wijzigen.

**Revisie > Proefdrukken > Onderzoek** Beperkt door de machtiging Kopiëren.

**Revisie > Proefdrukken > Synoniemenlijst** Beperkt door de machtiging Kopiëren.

**Revisie > Taal > Vertalen** Beperkt door de machtiging Kopiëren.

**Revisie > Wijzigingen > Protect-blad** Niet beschikbaar tijdens een beveiligde sessie.

**Revisie > Wijzigingen > Protect Workbook** Niet beschikbaar tijdens een beveiligde sessie.

**Revisie > Wijzigingen > Werkboek delen** Niet beschikbaar tijdens een beveiligde sessie.

**Revisie > Wijzigingen > Protect en Share Workbook** Niet beschikbaar tijdens een beveiligde sessie.

**Revisie > Wijzigingen > Gebruikers toestaan bereiken te bewerken** Niet beschikbaar tijdens een beveiligde sessie.

**Revisie > Wijzigingen > Wijzigingen bijhouden > Wijzigingen markeren** Niet beschikbaar voor een bestand dat met een beleid is beveiligd en dat een dynamisch watermerk bevat.

**Weergave > Macro&#39;s** Beperkt door de machtiging Wijzigen.

**Weergave > Werkruimte opslaan** Opdracht werkt niet.

**Developer > XML > Expansion Packs** Sommige macro&#39;s zijn beperkt door de machtiging Kopiëren en zijn alleen beschikbaar als kopiëren is toegestaan.

**Formulieren > Formulercontrole > Foutencontrole** Beperkt door de machtiging Wijzigen. Niet beschikbaar, tenzij wijzigen is toegestaan.

**Online samenwerking** Niet beschikbaar tijdens een beveiligde sessie.

**Info automatisch herstel opslaan** Niet beschikbaar tijdens een beveiligde sessie.

***Opmerking **: Als u probeert een cel te wijzigen in een bestand dat met een beleid is beveiligd en waarvoor u geen machtigingen hebt om wijzigingen aan te brengen, wordt in Excel een onjuist waarschuwingsbericht weergegeven waarin wordt aangegeven dat u de beveiliging uit het bestand moet verwijderen met de opdracht Blad verwijderen. Als u de opdracht Werkblad niet beveiligen gebruikt, wordt de beleidsbescherming niet uit het bestand verwijderd.*

#### Beperkingen van PowerPoint 2010 en PowerPoint 2013 {#powerpoint-2010-and-powerpoint-2013-restrictions}

De onderstaande functies zijn beperkt in de beschreven situaties:

**Bestand > Nieuw > Nieuw uit bestaand** Beschikbaar, maar bestanden die tijdens een beveiligde sessie met deze opdracht zijn gemaakt, kunnen niet worden opgeslagen. Inhoud in het nieuwe bestand kan niet naar een ander bestand worden gekopieerd.

**Bestand > Opslaan** Beperkt door de machtiging Wijzigen.

**Bestand > Opslaan als** Alle opties die zijn beperkt door de machtiging Wijzigen.

**Bestand > Afdrukken** Alle opties die zijn beperkt door de machtiging Afdrukken. Niet beschikbaar, tenzij het beleid afdrukken met hoge resolutie toestaat.

**Bestand > Opslaan en verzenden** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Info > Protect-presentatie > Coderen met wachtwoord, Een digitale handtekening toevoegen, Markeren als definitief, Machtiging door personen beperken** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > PowerPoint-opties > Info automatisch herstel opslaan** Niet beschikbaar tijdens een beveiligde sessie.

**Bestand > Server > Menu Bestandsservertaken** Niet beschikbaar tijdens een beveiligde sessie.

**Home > Clipboard > Copy** Beperkt door de machtiging Kopiëren. Als kopiëren niet is toegestaan, kan gekopieerde inhoud niet worden geplakt in het document, in een ander bestand of op het Office-klembord. Inhoud kan binnen het beveiligde bestand worden gekopieerd als de gebruiker over wijzigingsmachtigingen beschikt.

**Home > Clipboard > Paste** Beperkt door de machtiging Wijzigen. Als kopiëren niet is toegestaan, kan gekopieerde inhoud niet in het document worden geplakt.

**Home > Klembord > Plakken speciaal** Beperkt door de machtiging Wijzigen.

**Home > Dia&#39;s > Nieuwe dia&#39;s > Dia&#39;s van overzicht, hergebruik Dia&#39;s** Niet beschikbaar tijdens een beveiligde sessie.

**Invoegen > Tekst > Object** Niet beschikbaar tijdens een beveiligde sessie. Met een beleid beveiligde bestanden kunnen op geen enkel moment worden ingevoegd.

**Design > Background > Background Styles, Hide Background Graphics, Format Background** Niet beschikbaar voor een bestand dat met een beleid is beveiligd en dat een dynamisch watermerk bevat.

**Presentatie > Instellen > Presentatie opnemen** Beperkt door wijzigingsmachtiging.

**Revisie > Proefdrukken > Synoniemenlijst** Beperkt door de machtiging Kopiëren.

**Revisie > Taal > Vertalen** Beperkt door de machtiging Kopiëren.

**Revisie > Taal > Vertalen > Mini Vertaler** Ingeschakeld met de machtiging Kopiëren.

**Weergave > Presentatieweergaven > Presentatie** Beperkt door de machtiging Wijzigen. Als wijzigingen niet zijn toegestaan, kunnen presentaties niet worden weergegeven als het bestand is gewijzigd.

**Weergave > Macro&#39;s** Sommige macro&#39;s zijn beperkt door de machtiging Kopiëren en zijn alleen beschikbaar als kopiëren is toegestaan.

**Add-ins** Kan niet worden toegevoegd of verwijderd tijdens een beveiligde sessie.

**Online samenwerking** Niet beschikbaar tijdens een beveiligde sessie.

## Andere verificatieproviders gebruiken {#use-third-party-authentication-providers}

U kunt externe verificatieproviders gebruiken met AEM Forms Document Security. Met deze verificatieproviders kunt u een extra toegangslaag toevoegen aan de beveiligde documenten. AEM Forms-documentbeveiliging ondersteunt de volgende uitgebreide verificatieworkflows:

* Uitgebreide verificatie met standaard AEM Forms URL
* Uitgebreide verificatie met een aangepaste URL
* Standaard uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms op JEE-server
* Aangepaste uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms op JEE-server
* Uitgebreide verificatie met behulp van aangepaste pagina voor SAML-verificatie

## Verklarende woordenlijst {#glossary}

Voor informatie over LiveCycle- en AEM formulieren over JEE-terminologie raadpleegt u [Hoofdstuk 19: Verklarende woordenlijst](https://www.adobe.com/go/learn_aemforms_designer_65).
