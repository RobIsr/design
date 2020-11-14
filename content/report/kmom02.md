---
Title: Kmom01
Description: Report for Kmom01.
---

Kmom02
======

Denna veckans kursmoment har varit utmanande men väldigt givande. Jag har aldrig jobbat med 
SASS tidigare, men inser nu fördelarna med det. Det känns mycket mer naturligt att skriva 
CSS med SASS då strukturen blir mer den kod man skriver i andra programmeringsspåk. Möjligheten
att nästla css tycker jag var det mest givande.

För att komma igång med veckans arbete krävdes en hel del setup för att få allt att fungera.
Jag har använt npm tidigare men i väldigt liten utsträckning. Jag kan inte säga att jag fick
någon djupare förståelse denna veckan för hur det fungerar, men tycker det verkar vara ett bra
verktyg för att installera paket och hantera dependencies.

Att jobba med SASS innebär att man hela tiden måste kompilera om koden när man gör någon ändring
i den. Detta blir ju ett litet extrasteg att utföra rätt ofta. Jag tyckte dock att det gick
väldigt smidigt och inte något som jag kände var jobbigt. Denna veckan valde jag att inte använda
mig av "watch" för att automatiskt kompilera vid ändringar, men det nog något jag kommer att
använda mig av nästa vecka.

När jag denna vecka började jobba med mitt tema så hade jag en grund layout med de färger som 
jag ville ha. Mitt mål med designen har varit att skapa en enkel och kul sida med en lugn känsla.
Jag har lagt till en bakgrundsbild till main elementet som jag skapade själv för att representera 
mig. Jag har också använt mig av font awsome ikoner i menyn och på "Om" sidan för att göra
upplevelsen lite roligare. För små enheter valde jag att ta bort hamburgar menyn och lägga menyvalen
som ikoner just under den kurvade botten delen av headern. Då sidan i nuläget endast innehåller 3st
menyval tycker jag att det blir både snyggare och enklare att ha dem presenterade på detta sättet.
I tecktstycket om mig själv valde jag också att lägga in unicode emojis för att liva upp stämmningen
i texten. Jag har också vält två fonter som jag tycker passar in i sidan och är tydliga.

Jag har försökt dela upp koden enligt SMACSS som jag läste om förra veckan för att skapa lite struktur.
Jag har style.scss som ingångspunkt. Här importeras min css från övriga delar. I filen base.scss ligger
de grundregler för html element som jag vill ska gälla generellt över hela sidan. Filen layout.scss
innehåller de regler som styr upp placering, storlek på sidans huvud element. Under mappen "modules"
har jag försökt separera ut några mindre specifika delar av sidan i olika filer som t.ex navbar och
artikeln i main osv. Här ligger specifik styling på klasser och id som ska gälla för det individuella
"modulerna".

Min TIL för denna vecka är kunskapen om SASS och hur det underlättar arbetet med att skapa struktur
i css. Fram tills nu har känslan alltid varit dålig struktur när jag jobbat med css, vilket nu
känns mycket bättre.