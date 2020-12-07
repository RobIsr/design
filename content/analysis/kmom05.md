---
Title: Kmom05
Description: Analysis for Kmom05.
Template: analysis
---

Analys av webbsidors laddningstid och användbarhet
==================================================

I denna artikel presenteras analys av 3 stycken webbsidor för att testa deras laddningstid samt analysera
eventuell förbättringspotential.

Urval
-----

De webbsidor som valdes ut för analys är [Polisen](https://polisen.se), [Trafikverket](https://www.trafikverket.se/)
samt [Försvarsmakten](https://www.forsvarsmakten.se/sv/).

Då dessa sidor kan anses ha sammhällsviktiga funktioner och bör kunna tillgodogöras av hela allmänheten är
det intressant att studera dessa webbsidors prestanda i form av laddningstider och dataanvändning. Samtliga
myndigheter är stora aktörer med hög trafik till deras sidor och det blir intressant att studera hur de hanterar
prestandan.

De undersidor som valts ut för respektive myndighet är likartade för att kunna göra en bra jämförelse. De
utvalda sidorna är: Startsida, en sida som presenterar nyheter eller aktuell information samt en "artikel"
sida som visar information om ett specifikt område djupare in i sidan.

Metod
-----

Analysen av webbsidorna har utförts med hjälp av [Page Speed Insights](https://developers.google.com/speed/pagespeed/insights/)
ett verktyg från google som analyserar webbsidors prestanda via dess url och visar resultat i procentform samt
tips på hur prestandan på sidan kan förbättras. Då resultatet med detta verktyg kan variera mellan olika
körningar är varje test utfört 3 gånger och medelvärdet av dessa körningar blir testresultet.

Varje sida är också kontrollerad med hjälp av "Developer Tools" i Chrome. Fliken för nätverk har använts för
att kontrollera hur många resursern som laddas, hur lång tid det tar för att ladda hela sidan, samt sidans
totala storlek. Dessa tester har också körts 3 gånger för att få ett rättvisande resultat.

Alla resultat från denna analys är dokumenterade i ett Google Spreadsheet. Länk till detta finns under "Resultat"
nedan.

Resultat
--------

***
I nedanstående sammanställning över de webbsidor som analyserats kan ses de slutgiltiga resultaten för varje test.
Dessa resultat är medelvärdet av 3st separata körningar med verktyget "Page Speed Insights" samt "network"
fliken i Chrome.

För att se samtliga testdata [klicka här...](https://docs.google.com/spreadsheets/d/17LAatwKiX2q8cfmr1MAy3k_HZJ9D8stVhN2hM_qiScU/edit?usp=sharing)
***

###[Polisen - Startsida](https://polisen.se/)
![Screenshot Polisen Start](../assets/img/page-load/polisen-start.png){.screenshot .left}

* Resultat(mobil): 98.6%
* Resultat(dator): 100%
* Antal resurser: 18st
* Laddningstid: 0.7s
* Total storlek: 877kb

***

###[Polisen - Aktuellt](https://polisen.se/aktuellt/)
![Screenshot Polisen Aktuellt](../assets/img/page-load/polisen-aktuellt.png){.screenshot .left}

* Resultat(mobil): 99.3%
* Resultat(dator): 99.7%
* Antal resurser: 8st
* Laddningstid: 0.58s
* Total storlek: 490kb

***

###[Polisen - Stöld av motorfordon](https://polisen.se/utsatt-for-brott/olika-typer-av-brott/motorfordon/)
![Screenshot Polisen Artikel](../assets/img/page-load/polisen-article.png){.screenshot .left}

* Resultat(mobil): 98.3%
* Resultat(dator): 100%
* Antal resurser: 9st
* Laddningstid: 0.55s
* Total storlek: 535kb

***

Polisens webbsida är ett typexempel på en högpresterande sida. I samtliga tester får de nästan högsta
möjliga betyg. Man kan se att antalet resurser som hämtas hålls till ett minimum samt att sidans storlek
är väldigt liten.

Det är tydligt att man lagt fokus på att sidan ska prestera bra både på dator såväl som på mobila
enheter. I de tips som presenteras från Page Speed Insights ses att de med fördel skulle kunna ladda in 
sina fonter i förväg, ta bort oanvänd CSS samt att det går att använda modernare sätt för att implementera sin 
Javascript kod i sidan. I det stora hela är dessa saker något som inte påverkar sidan nämnvärt och den håller 
väldigt hög kvalité när det kommer til prestanda överlag.

***

###[Trafikverket - Startsida](https://www.trafikverket.se/)
![Screenshot Trafikverket Start](../assets/img/page-load/trafikverket-start.png){.screenshot .left}

* Resultat(mobil): 62.3%
* Resultat(dator): 86.3%
* Antal resurser: 44st
* Laddningstid: 1.2s
* Total storlek: 2.5mb

***

###[Trafikverket - Västerbotten](https://www.trafikverket.se/nara-dig/Vasterbotten/)
![Screenshot Trafikverket Aktuellt](../assets/img/page-load/trafikverket-aktuellt.jpg){.screenshot .left}

* Resultat(mobil): 34%
* Resultat(dator): 74.6%
* Antal resurser: 51st
* Laddningstid: 2.25s
* Total storlek: 4.8mb

***

###[Trafikverket - Körkort/Avgifter](https://www.trafikverket.se/korkort/betalningar/avgifter/)
![Screenshot Trafikverket Artikel](../assets/img/page-load/trafikverket-article.png){.screenshot .left}

* Resultat(mobil): 38%
* Resultat(dator): 74.3%
* Antal resurser: 45st
* Laddningstid: 2s
* Total storlek: 3.5mb

***

Trafikverkets siffror ligger ganska bra till för användare som besöker sidan via dator. Ett resultat på mellan
74 och 86 procent är inte dåligt, med tanke på att det är en stor sida. Här kan dock ses att prestandan  för mobil
andvändare ligger betydligt lägre och verkar inte vara lika prioriterat.

Ett stort antal resurser laddas, vilket tillsammans med storleken på resurserna leder till att sidan har en lite
högre laddningstid, som mest på 2.25 sekunder. 

I analysen från Page Speed Insights återfinns många problem. Likt Polisens sida rekommenderas här att resurser
bör läsas in i förväg såsom fonter samt att ta bort oanvänd CSS och Javascript. Här rekommenderas också att skicka bilder i
modernare format. Bilderna som hänvisas till är PNG bilder som förmodligen skulle passa sig bättre som JPEG
bilder då de är foton. DOM trädet anses också vara onödigt stort då det innehåller hela 1750 element. Det rekommenderas
också att undvika upprepade omdirigeringar.

***

###[Försvarsmakten - Startsida](https://www.forsvarsmakten.se/sv/)
![Screenshot Försvarsmakten Start](../assets/img/page-load/forsvar-start.jpg){.screenshot .left}


* Resultat(mobil): 36%
* Resultat(dator): 77.3%
* Antal resurser: 36st
* Laddningstid: 2s
* Total storlek: 3.5mb

***

###[Försvarsmakten - Aktuellt](https://www.forsvarsmakten.se/sv/aktuellt/)
![Screenshot Försvarsmakten Aktuellt](../assets/img/page-load/forsvar-aktuellt.png){.screenshot .left}


* Resultat(mobil): 58.7%
* Resultat(dator): 84%%
* Antal resurser: 37st
* Laddningstid: 3.7s
* Total storlek: 2.66mb

***

###[Försvarsmakten - Flygvapnet](https://www.forsvarsmakten.se/sv/var-verksamhet/det-har-gor-forsvarsmakten/flygvapnet/)
![Screenshot Försvarsmakten Artikel](../assets/img/page-load/forsvar-article.png){.screenshot .left}


* Resultat(mobil): 48.7%
* Resultat(dator): 89.3%
* Antal resurser: 37st
* Laddningstid: 6s
* Total storlek: 8.17mb

***

Försvarsmaktens siffror ligger likt Trafikverkets relativt bra för de användare som använder dator med tanke på att webbsidan
som helhet är stor. För användare som besöker sidan via mobilen är siffrorna dåliga. Även här blir mobilprestanda bortprioriterat.
Antal resurser som får också anses som högt, som mest 37st vilket tillsammans med det som sticker ut mest, den totala storleken
medför dåliga laddningstider. Den totala storleken är som mest hela 8.17mb, något som är klart över det rekommenderade. Laddnigstiden
uppstiger till som mest 6 sekunder och överstiger därmed med stor marginal de resterande sidor som undersökt här.

Resultaten från Page Speed Insights visar till skillnad från övriga sidor i detta test på rätt små tidsvinster vad gäller CSS och
Javascript, samt hur dessa läses in, även om det fanns en del oanvänd kod. Här är det stora problemet de bilder som används och 
hur de laddas. Problem finns med att bilder används med fel storlek, att de bör skickas i modernare bildformat, att inladdningen 
av de bilder som inte visas på skärmen bör skjutas upp samt att bilderna bör kodas mer effektivt.

***

Analys
-------

Bland de testade sidorna sticker Polisens ut som den absolut bästa i samtliga tester. Hos Trafikverket och Försvarsmakten
kan tydligt ses sämre prestanda, framförallt på mobila enheter. Då allt fler användare surfar på mobilen är detta en nackdel.
Även om dessa sidor inte har någon försäljning eller reklam, så behöver de nå ut till allmänheten med sin information. Kanske
behövs information från Trafikverket när någon sitter i sin bil och bara har tillgång till mobilen. Detsamma gäller polisen
där en person kan behöva snabb tillgång till information med mobilen som enda verktyg. Försvarsmakten har nog inte samma
behov av mobil tillgänglighet då informationen för det mesta inte behöver tas fram snabbt i en situation. Detta kan vara
en anledning till att fokuset på mobila enheter är lägre, samt att de använder stora och "talande" bilder för att nå ut till 
sina användare. Kanske kan man här som användare tåla en längre laddningstid för för att sedan få en bra presentation av
försvarsmakten.

Gemensamt för alla webbsidorna är att oanvänd CSS och Javascript skulle behöva tas bort. Det kan också konstateras i samtliga
fall att vissa resurser skulle kunna läsas in i förväg. Här verkar fonter vara det som är problemet. Bilder kan också identifieras
som ett problem. Bilder skulle behöva optimeras mer samt konverteras till ett modernare format. Här skulle format såsom JPEG 2000
eller webp som exempel vara bättre alternativ.

Bortsett från Polisen så är känslan att av att vissa myndigheter borde försöka hitta en struktur på sina webbsidor som laddar
färre resurser och använder mindre storlek. Sidorna bör optimeras även för mobila enheter för att minska användningen av
mobildata. Detta både för att spara pengar åt sina användare samt att minska påverkan på miljön.

Slutsats
--------

Resultat för de webbsidor som valts ut för testet:

1. Polisen
2. Trafikverket
3. Försvarsmakten

Vinnare med stor marginal är Polisen på alla delar av testerna. Sidan känns blixtsnabb när man navigerar runt på
den och testerna visar nästan maximala resultat i samtliga avseenden.

Trafikverket hamnar på andra plats. En klar skillnad gentemot Polisen kan upplevas, men sidan känns inte alls
långsam och ger en bra upplevelse generellt. Nackdel här är att väldigt många resurser används och att den totala
storleken på sidan är lite stor.

Försvarsmakten hamnar på 3:e plats. Med en laddningstid på hela 6 sekunder på artikel sidan var känslan trög.
Sidan är visserligen visuellt väldigt tilltalande, något som troligen prioriterats högt. Storleken på sidorna
ät väldigt hög och det är största bidragande faktorn till ett lite långsammare intryck.

Personligen anser jag att en laddningstid som ligger under 2 sekunder känns snabb. När jag besöker en webbsida
är i mina ögon en laddningstid på 2 - 4 sekunder ganska normalt. 4 Sekunder och uppåt ger för mig ett trögt intryck.

Övrigt
------

Författare:
Robert Israelsson
