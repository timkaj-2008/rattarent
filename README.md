# Rattarent

Rattarent on süsteem, mille abil kasutajad saavad vaadata vabu 
jalgrattaid, rentida ratta, selle tagastada ja vaadata rendiinfot.

**Tegijad:** Aleksei Dubtsak, Timofei Jegorov
**Grupp:** NPTV24

## Kasutajad ja nõuded

Süsteemil on kaks rolli: kasutaja ja haldur.

Kasutaja saab vaadata vabu rattaid, rentida ja tagastada ratta 
ning vaadata rendiinfot ja rendiajalugu.

Haldur saab vaadata aktiivseid rente ja hallata rattaid.

Kuus kasutajalugu on GitHub Issues all. Kõige tähtsamad lood 
on märgitud `must`.

## Arendusmudel

Me valisime Rattarendi süsteemi jaoks inkrementaalse arendusmudeli. 
Kõigepealt arendaksime rataste vaatamise ja rentimise funktsioonid, 
sest need on süsteemi kõige tähtsamad osad. 
Seejärel lisaksime ratta tagastamise ja rendi hinna arvutamise. 
Pärast seda saaksime lisada rendiajaloo ja halduri funktsioonid. 
Kosemudel ei sobiks nii hästi, sest süsteemi vajadused võivad 
arendamise ajal muutuda.

## Diagrammid

![Kasutusjuhud](diagrammid/kasutusjuhud.png)

![Klassid](diagrammid/klassid.png)

## Makett

Me tegime maketi iteratiivselt, sest vaatasime mõlemad ekraanid 
üle ja täiendasime neid vastavalt kasutajalugudele.

![Vabad rattad](makett/vabad_rattad.png)

![Ratta rent](makett/renti_ekraan.png)

## Kuidas me töötasime

Kasutasime Miro Kanban-tahvlit, kus töö liikus veergudes 
Teha, Teen ja Valmis.

Meie töö jagunes kahe paari vahel ja kasutasime GitHubis 
harusid ning Pull Requeste.

Kõige raskem oli diagrammide ja kasutajalugude omavaheline 
ühendamine.

## Retrospektiiv

Kasutajalugude kirjutamine ja GitHub Issues kasutamine läks hästi.

Kõige raskem oli klassidiagrammi seoste ja kordsuste määramine.

Järgmisel korral planeeriksime UML-diagrammide tegemiseks rohkem aega.

## Projekti kaart

**Tellija:** Rattarendi ettevõtte omanik / haldur
**Probleem:** Klientidel puudub mugav võimalus näha vabade jalgrataste olemasolu reaalajas ning rentida ratast iseseisvalt. Rentimise ja tagastamise protsess nõuab käsitööd, mis tekitab viivitusi ning võib põhjustada vigu rendiinfo ja -hindade arvestuses.
**Eesmärk:** 1. detsembriks on valmis veebipõhine süsteem, kus kasutajad saavad ise vaadata vabu rattaid, neid rentida ja tagastada; haldur saab vaadata aktiivseid rente ja hallata rattaid; käsitsi tehtav töö väheneb 90%.
**Tulemus:** Rattarendi veebirakendus (kasutaja ja halduri vaated), andmebaasi struktuur, UML-diagrammid (Use Case, klassidiagramm) ja kasutusjuhend.

**Ulatus SEES:**
- Vabade rataste ja nende asukohtade vaatamine[cite: 1, 3]
- Ratta rentimine ja tagastamine kasutaja poolt
- Rendi hinna automaatne minutipõhine arvutamine[cite: 1, 4]
- Kasutaja rendiajaloo ja rendiinfo vaatamine
- Halduri liides aktiivsete rentide vaatamiseks ja rataste haldamiseks

**Ulatus VÄLJAS:**
- Veebimaksed ja pangalinkide liidestus (arvestus on süsteemisisene)[cite: 1, 4]
- Eralline mobiilirakendus iOS/Android tarbeks (süsteem on reageeriva veebidisainiga)
- Elektrijalgrataste akutaseme reaalajas jälgimine

**Kolmnurk:** 
- Aeg: **fikseeritud** (tähtaeg määratud)
- Raha/inimesed: **fikseeritud** (2 arendajat: Aleksei Dubtsak, Timofei Jegorov, grupp NPTV24)
- Ulatus: **paindlik** (mitte-kriitilised funktsioonid saab vajadusel edasi lükata)
- Fikseeritud on: **aeg ja inimesed**

**Rollid:** 
- Tellija: Rattarendi ettevõtte omanik / haldur
- Projektijuht / Arendajad: Aleksei Dubtsak ja Timofei Jegorov (NPTV24)
- Kasutajad: Rattarendi kliendid[cite: 1]

| Risk | Tõenäosus 1–3 | Mõju 1–3 | Mida teeme enne (ennetus) |
|---|:---:|:---:|---|
| Klassidiagrammi seoste ja kordsuste määramisel tekivad vead, mis viivitavad andmebaasi loomist | 2 | 3 | Planeerime UML-diagrammide analüüsiks ja läbirääkimiseks alguses rohkem aega[cite: 1] |
| Diagrammide ja kasutajalugude omavaheline ühendamine osutub keeruliseks[cite: 1] | 2 | 2 | Kontrollime iga kasutajaloo vastavust Use Case diagrammile enne koodi kirjutamist[cite: 1] |
| Rendi hinna minutipõhise arvutuse loogika tekitab vigu[cite: 1, 4] | 1 | 3 | Loome eraldi testimisülesanded rendi alguse ja lõpu ajaarvestuse kontrolliks |

**Edukriteerium:** Tellija kontrollib: kas kasutaja saab veebis vaba ratta valida[cite: 1, 3], rentida[cite: 1, 4], seda tagastada[cite: 1] ja kas haldur näeb aktiivset renti halduri vaates (Jah / Ei).


**Hinnang:** 68 h, 4.3 päeva kahekesi.
