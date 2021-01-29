---
title: Inleiding tot AEM Document Security Extension voor Microsoft Office
description: Gebruikend de Uitbreiding van de Veiligheid van het document voor Microsoft Office, kunt u vooraf bepaalde vertrouwelijkheidsmontages op uw dossiers van Microsoft Office toepassen.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
translation-type: tm+mt
source-git-commit: 19de0b62ac493c7507581abb607b008c64f77597
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 0%

---


# Inleiding om de Uitbreiding van de Veiligheid van het Document voor Microsoft Office{#introduction-to-aem-document-security-extension-for-microsoft-office} te AEM

De Uitbreiding van de Veiligheid van het Document van de Adobe® Experience Manager voor Microsoft® Office zorgt ervoor dat slechts de mensen u toestaat Word, Excel, en de dossiers van PowerPoint kunnen gebruiken die uw intellectuele bezit bevatten. Door de Uitbreiding van de Veiligheid van het Document voor Microsoft Office te gebruiken, kunt u vooraf bepaalde vertrouwelijkheidsmontages op uw dossiers toepassen.

De Uitbreiding van de Veiligheid van het document voor Microsoft Office breidt LiveCycle Rights Management en de Veiligheid van het Document toe:voegen-op voor Adobe Experience Manager Forms uit om Word, Excel, en dossiers van PowerPoint te beschermen en erkende gebruikers toe te staan die deze software hebben geïnstalleerd om beleid-beschermde dossiers volgens de vertrouwelijkheidsmontages te gebruiken die in het beleid worden gevestigd.

## Hoe de Veiligheid van het Document intellectuele eigendom {#how-document-security-protects-intellectual-property} beschermt

Documentbeveiliging zorgt ervoor dat alleen de personen die u autoriseert, bestanden kunnen gebruiken die uw intellectuele eigendom bevatten. Met Documentbeveiliging kunt u bestanden beveiligen met vertrouwelijkheidsbeleid. Een *beleid* is een inzameling van informatie die vertrouwelijkheidsmontages en een lijst van erkende gebruikers omvat. De montages u in een beleid specificeert bepalen hoe een ontvanger een dossier kan gebruiken waarop u het beleid toepast. U kunt bijvoorbeeld opgeven of ontvangers tekst kunnen afdrukken of kopiëren of wijzigingen kunnen opslaan.

Beveiliging van documenten en gebruikers maken beleid. Beheerders maken organisatiebeleid dat beschikbaar is voor alle geautoriseerde gebruikers. Beheerders of beleidssetcoördinatoren kunnen ook groepen beleidsregels maken die *beleidssets* worden genoemd en die beschikbaar zijn voor een subset gebruikers. Gebruikers kunnen hun eigen beleid maken, dat alleen zij kunnen gebruiken. Beheerders, beleidssetcoördinatoren en gebruikers maken beleid met behulp van de webpagina&#39;s Documentbeveiliging.

Hoewel het beleid op de Veiligheid van het Document wordt opgeslagen, past u hen op dossiers door Word, Excel, of PowerPoint toe. Wanneer u een beleid op een dossier toepast, wordt de informatie die het dossier bevat beschermd door de vertrouwelijkheidsmontages die in het beleid worden gespecificeerd. Wanneer u het bestand distribueert dat met een beleid is beveiligd, hebben alleen de ontvangers die door het beleid zijn gemachtigd toegang tot de inhoud van het bestand.

Het gebruiken van een beleid om een dossier te beschermen geeft u aan de gang zijnde controle over dat dossier, zelfs nadat u het verspreidt. U kunt gebeurtenissen controleren om te volgen wanneer en hoe de ontvangers uw dossier gebruiken, veranderingen in het beleid aanbrengen, gebruikers verhinderen het dossier te blijven toegang hebben, en het beleid te veranderen dat aan het dossier in bijlage is.

## Hoe beleid werkt {#how-policies-work}

Het beleid bevat informatie over de gemachtigde gebruikers en de vertrouwelijkheidsinstellingen die op intellectuele eigendom moeten worden toegepast. Gebruikers kunnen elke gebruiker zijn die door Documentbeveiliging wordt herkend door opname in een gekoppelde LDAP- of Active Directory-lijst. Gebruikers kunnen ook personen zijn die zijn uitgenodigd om zich te registreren bij Documentbeveiliging of voor wie de beheerder een account heeft gemaakt.

De vertrouwelijkheidsmontages in een beleid bepalen hoe de ontvangers dossiers kunnen gebruiken die door het beleid worden beschermd. Met beleid wordt bijvoorbeeld aangegeven of ontvangers bestanden kunnen afdrukken, inhoud naar andere bestanden kunnen kopiëren of wijzigingen in beveiligde bestanden kunnen opslaan. Het beleid kan verschillende vertrouwelijkheidsmontages voor diverse gebruikers ook specificeren.

Wanneer u een beleid op een dossier toepast, wordt de informatie die het dossier bevat beschermd door de vertrouwelijkheidsmontages die in het beleid worden gespecificeerd. Wanneer u het bestand verspreidt, worden de ontvangers die het bestand proberen te openen door Documentbeveiliging geverifieerd en wordt toegang toegestaan op basis van de bevoegdheden die in het beleid zijn opgegeven.

Nadat een beleid op een dossier wordt toegepast, kunnen de vertrouwelijkheidsmontages van het beleid op elk ogenblik worden veranderd, toestaand u om erkende gebruikers toe te voegen of te verwijderen of de voorrechten voor gebruikers te veranderen nadat zij het dossier hebben ontvangen. Het beleid dat op het bestand is toegepast, kan worden gewijzigd en de toegang tot het bestand kan worden ingetrokken, zodat iedereen met een kopie van het bestand het bestand niet meer kan openen.

Als het beleid offline toegang toestaat, kunnen de ontvangers beleid-beschermde dossiers (zonder actieve Internet of netwerkverbinding) voor de tijdspanne ook offline gebruiken die in het beleid wordt gespecificeerd.

## Hoe beleidsbeveiligde bestanden werken {#how-policy-protected-files-work}

Voor een gebruiker om beleid-beschermde Word, Excel, en de dossiers van PowerPoint te openen en te gebruiken, moet het beleid de gebruiker als ontvanger omvatten of anonieme toegang toestaan, en de gebruiker moet de Uitbreiding van de Veiligheid van het Document voor Microsoft Office hebben geïnstalleerd. Om een beleid-beschermd dossier aan iemand te geven die geen Uitbreiding van de Veiligheid van het Document voor Microsoft Office heeft, of hen een exemplaar van de software of vertelt hoe te om het van uw website te downloaden. Als u het installatieprogramma niet hebt, kunt u het downloaden van [downloadpagina](https://www.adobe.com/products/livecycle/rightsmanagement/extension/downloads.html).

Wanneer een gebruiker probeert om een beleid-beschermd dossier te openen, verbindt de Uitbreiding van de Veiligheid van het Document voor Microsoft Office met de Veiligheid van het Document om de gebruiker voor authentiek te verklaren. Als de Veiligheid van het Document aan controledossiergebruik wordt gevormd, ziet de gebruiker een bericht erop wijzend dat het dossiergebruik wordt gecontroleerd. Documentbeveiliging bepaalt welke bestandsmachtigingen de gebruiker kunnen krijgen en de gebruiker het bestand vervolgens kan gebruiken volgens de beleidsinstellingen, onder de volgende voorwaarden:

* Voor de geldigheidsperiode die in het beleid wordt gespecificeerd.
* Tot een beheerder of de persoon die het beleid toepaste, de toegang tot het bestand intrekt of het beleid wijzigt.

   Als de persoon die het beleid toepaste het beleid verandert of toegang tot het dossier herroept, worden de toestemmingen van de gebruiker voor het dossier veranderd of verwijderd alhoewel de gebruiker reeds het dossier heeft. Als het bestand zelf is ingetrokken, ontvangt de gebruiker mogelijk een URL om een bijgewerkte kopie op te halen.

   Bestanden die met een beleid zijn beveiligd, kunnen offline worden geopend (zonder internet- of netwerkverbinding) als het beleid offline toegang toestaat, voor de duur van de offline leaseperiode die in het beleid is opgegeven. Wanneer de offline leaseperiode afloopt, moet de gebruiker online gaan en synchroniseren met Documentbeveiliging, die een nieuwe leaseperiode start.

   Als het beleid toestaat dat het dossier wordt opgeslagen en een gebruiker een exemplaar van het beleid-beschermde dossier bewaart, wordt het beleid automatisch toegepast en voor het bewaarde dossier afgedwongen. Gebeurtenissen, zoals pogingen om het nieuwe bestand te openen, worden ook gecontroleerd en op dezelfde manier opgenomen als in het oorspronkelijke bestand.

## Beveiliging document gebruiken om uw bestanden te beveiligen {#using-document-security-to-protect-your-files}

U kunt beleid gebruiken om uw dossiers in diverse situaties te beschermen.

Een fabrikant accepteert bijvoorbeeld biedingen van leveranciers die onderdelen leveren voor een nieuw product. De fabrikant moet de bieders de door eigendomsrechten beschermde informatie verstrekken die zij nodig hebben om hun opmerkingen af te ronden. De fabrikant gebruikt Documentbeveiliging om de bestanden te beschermen met een beleid waarmee de bieders de bestanden kunnen openen en de informatie kunnen bekijken. Bieders kunnen de bestanden echter niet wijzigen, afdrukken of kopiëren en iedereen die geen machtiging heeft, kan de bestanden niet openen.

Nadat de fabrikant een van de biedingen heeft geaccepteerd, werkt de fabrikant het beleid bij om de winnende bieder toestemming te geven om wijzigingen lokaal af te drukken, te kopiëren en op te slaan en om de niet-winnende bieders te verwijderen, zodat ze geen toestemming meer hebben om de bestanden te openen.

Terwijl de technici van de fabrikant met de succesvolle bieder samenwerken, veranderen sommige ontwerpspecificaties in de bestanden. Om de nieuwe specificaties te publiceren, trekt de fabrikant de toegang tot sommige dossiers in en publiceert nieuwe versies. Wanneer engineers van de succesvolle bieder het bestand proberen te openen, zien ze een bericht dat de toegang tot het bestand is ingetrokken. Het bericht bevat een URL waar ze een nieuwe versie van het bestand kunnen downloaden.

## Aanvullende informatie {#additional-information}

De bronnen in deze tabel kunnen u helpen meer te weten te komen over AEM documentbeveiliging:

<table >
 <tbody>
  <tr>
   <th><p>Voor informatie over</p> </th>
   <th><p>Zie</p> </th>
  </tr>
  <tr>
   <td><p>Help bij AEM</p> </td>
   <td><p><a href="http://www.adobe.com/go/learn_aemforms_admin_65">De </a> Hulp van de beheerder, op de pagina's van het Beleid van de Veiligheid van het Document, klik de verbinding van de Hulp in de hoger-juiste hoek van een pagina.</p> </td>
  </tr>
  <tr>
   <td><p>Reparatie-updates, technische notities en aanvullende informatie over deze productversie</p> </td>
   <td><p><a href="https://helpx.adobe.com/marketing-cloud/contact-support.html">Technische ondersteuning van Marketing Cloud</a></p> </td>
  </tr>
 </tbody>
</table>

