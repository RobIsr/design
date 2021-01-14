---
Title: Kmom10
Description: Report for Kmom10.
Template: kmom
---

Kmom10
======

I detta projekt har jag valt att gör en webbsida till dansaren Art-Ist som vill visa upp sig själv och vad han gör. Hans inriktning på dans är street/breakdance och han vill ha en webbsida som återspeglar detta. Nedan finns beskrivning på de krav som jag genomfört i projektet.

Krav 1 (Webbplats):
-------------------

När jag började jobba med projektet så valde jag att skapa ett helt nytt projekt från början med hjälp av guiden från kursmaterialet. Jag kände att det var bra repetion att gå igenom hela setup precessen igen. När jag nu hade en fungerande grund för projektet var det dags att fundera på hur designen för sidan skulle se ut.

Designprocessen tog sin början i att söka efter bildmaterial inom området breakdance/streetdance, för att få lite inspiration. På Unsplash fann jag bilden som sedan blev min "hero" image i headern. Jag ansåg att den var väldigt livlig och innehöll mycket rörelsse som representerade dans samt att det fanns bra grund i dess färger för att skapa ett färgtema för sidan.

När jag hittat denna bild använde jag designverktyget Figma för att skapa wireframes för webbsidan och dess olika delar. För att skapa färgpaletten använde jag mig av colors.adobe.com för att plcka ut lämpliga färger ur header bilden och sedan började jag skapa content för de olika sidorna. Här designade jag sidorna med layout för både desktop och mobil, vilket gjorde arbetet med koden mycket lättare.

Webbplatsen innehåller en startsida, en about sida och en highlights sida, använder både en ikon och en favicon samt är responsiv för både mobil och desktop. Footern innehåller också länkar till e-post och sociala media.

Startsidan är designad för att ge ett första intryck av rörelse och dans. Den guidar användaren med "direction" genom innehållet i sidan och ger en bra introduktion till vad den handlar om. About sidan innehåller artistens presentation av tjänster som erbjuds samt vad tanken med webbplatsen är. Den innehåller också längst ner en länk till dokumentations sidan. Här är innehållet mer formellt strukturerat än på startsidan för att användaren ska få tydlighet och ett proffessionellt intryck. På Higlights sidan visan 3 st event som artisten på olika sätt har varit inblandade i. Den är uppdelad i sektioner som dynaminskt ändrar storlek och placering beroende på skärmstorlek.

Krav 2 (Tema)
-------------

För att skapa temat för sidan har jag använt SASS och försökt dela upp koden i flera moduler för att enkelt kunna hitta rätt samt göra det enkelt att jobba med. I filen "style.scss" importerar jag normalize.css och även en fil som heter base.scss. I denna importeras i sin tur alla övriga filer som berör temat. Jag använder mig av variabler för alla färger i filen varibles.scss som är globalt tillgängliga för övriga moduler. Jag har en övergripande layout.scss som hanterar den huvudsakliga layouten såsom header, main content och footer. Layoutet använder sig av grid för att presentera innehållet. Sedan har jag i mappen modules separerat ut mindre innehåll såsom för navbar, bildremsan som ligger på startsidan, upcomin sektionen, main innehållet och stylen för en separat highlight sektion till separate filer. Detta för att enklare hitta och kunna jobba med en mindre del av sidan åt gången. Jag har också en separat fil att sköta konfigurationen av typografin på sidan.

Jag har medvetet använd färg, typografi och desinprinciper/element för att skapa en genomgående känsla som artisten ville förmedla. Mer om detta finns att läsa i dokumentations sidan på webbplatsen.

Krav 3 (Responsivitet och tillgänglighet)
-----------------------------------------

Efter mycket jobb inom områden är sidan responsiv för olika skärmstorlekar. Genom att använda grid och flexbox tillsammans med mediaqueries samt Cmage och picture/srcset hanterar webbplatsen både desktop och mobila enheter på ett bra sätt. Ett stort arbete har varit att få bildremsan som ligger i mitten av startsidan att fungera responsivt. Här var jag trungen att jobba med storleken på bilderna samt deras vertikala och horizontella placering tillsammans med de tillhörande texterna som ligger intill bilderna. För att göra detta har jag använt mig av ett 3*3 grid och förändrat vilka columner och rader som de olika bilderna ska ligga på med hjälp av mediaquery. Dett gäller också för övriga layouten såsom på highlights sidan där de två översta eventen ligger bredvid varandra på desktop med hamnar under varandra när man visar sidan på en mobil enhet.

När det gäller accessibility så får samtliga sidor på webbplatsen 100% i Lighthouse. Jag hade fokus redan från början när jag gjorde wireframes på att kontraster skulle vara tillräckliga för att klara olika typer av färgblindhet samt att textinnehållet skulle vara tydligt uppdelat i sektioner och vara lättläslig. Jag har sett till att alla bild element har tillhörande beskrivande "alt" texter och att tab ordningen fungerar bra på sidan.

Genomförande
------------

Projektet har varit kul men en stor utmaning att genomföra. Största problemet för mig var att bestämma vilken känsla jag ville förmedla för sidan. Ett verktyg som var till stor hjälp var Figma. Här kunde jag snabbt testa olika former av layout, färger och designelement redan innan jag började koda. När jag väl hittade bilden som nu ligger i min header och bestämde mig för att basera färgvalen på den blev arbetsgången genast mycket klarare. I figma använde jag mig av lorem ipsum texter i början, bara för att skapa en bild av den layout jag skulle skapa. Jag tycker att designarbetet med hjälp av Figma gjorde processen enkel och rolig.

Jag bestämde mig ganska snabbt att jag ville göra bildremsan som ligger i mitten av startsidan mer intressant. Jag började experimentera med rotation, borders och att lägga till text. Tanken var att skapa någon form av "organiserat kaos" för att återspegla livligheten i breakdance. Detta arbete gick bra och jag hade ganska snart en fungerade layout i desktop format. Jag stötte här dock på stora problem med att göra denna remsa responsiv. Det var först efter att jag bestämde mig för att prova använda ett grid för dessa bilder som allt började läsa sig. Jag har verkligen insett hur kraftfullt css grid kan vara för att skapa dynamiska webbsidor.

Projektet som helhet var som sagt en stor utmaning för mig. Jag har lärt mig mycket om design under kursens gång, men kan ändå inte säga att jag har ett "öga" för design. Jag tycket att det generellt varit ganska svårt att genomföra detta projektet och jag har fått lägga ner mycket tid. Jag inser dock att projektet egentligen inte är så omfattande och känns väldigt rimligt för en kurs i webbdesign.

Tankar om kursen
----------------

Jag tycker att innehållet i kursen överlag har varit bra. Boken var intressant att läsa och övriga artiklar och länkar har gett mycket matnyttig information. Föreläsningarna har också varit bra, med tillhörande handledning i Discord. En nackdel för själva designtänket skulle väl vara att man blir inkastad i Pico ramverket med endast en kort introduktion. Jag kände mig ganska förvirrad i början och var tvungen att lägga mycket fokus på förstå hur Pico fungerade och hur alla filer hängde ihop. Det känns dock som att jag i slutändan fått relativt god förståelse för hur det fungerar, men känner att det blev lite mycket i kombination med att lära sig området design, som i sig är ett väldigt stort ämne.

Jag i det stora hela mycket nöjd med kursen och den har givit mig mycket. Jag skulle absolut rekommendera den för någon som visar intresse för området webbdesign. Den får av mig 8 av en skala på 10.