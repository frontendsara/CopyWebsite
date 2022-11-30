Vi har valt att återskapa huvudsidan av websidan & Other Stories med hjälp av HTML och CSS.

https://www.stories.com/en_sek/index.html 

Grupp: Sara Karlsson och Lisa Marie Andersson

DEMO [här] (https://github.com/frontendsara/CopyWebsite.git).


- Info om hur vi tänkt -

* Vi har delat in vår sida i en header (med länk för nyhetsbrev ovanför), main, aside och footer. 

* De delar i main som innehåller bilder hänvisar vi till i koden som Del 1-4. 

* Vi har främst utgått från mobil- och tablet-vyn, tex Iphone SE och Ipad Mini man får upp via inspektorn när vi skapat sidan för mobil/tablet. Dvs det går att dra ihop webbläsarfönstret och få responsivitet men innehållet kanske inte lägger sig helt som när de visas i den "riktiga" mobil/tablet-versionen då. 

* I mobil/tablet-versionen finns inte aside-delen med, den visas istället i form av en hamburgermeny    här. 

* Bilderna som finns på vår sida är skärmdumpade och beskurna från de som visades på originalsidan den 
14/9, se skärmdumpar. 

* Skärmdumpar för Tablet är tagna den 23/9 och visar därför andra bilder men samma layout. 

* All CSS för mobil/tablet/desktop ligger nu i samma mapp, vi ser fördelen av att dela upp denna i 3 st mappar i framtiden :) 



Vi har fått göra vissa avgränsningar, se nedan:


 - Typsnitt -

* Vi har använt oss av de typsnitt som är på originalsidan. Vi har dock inte kunnat göra originalhemsidans typsnitt i den utformning vi vill då vi har läst oss till att de verkar ha använt funktionen "font smooth" som inte är rekommenderad praxis och denna funktion är överstruken/går ej att applicera i VSC. Vi har testat olika sätt men hittar ingen font-weight eller liknande funktion som kan smalna av typsnittet så som font smooth verkar kunna göra. 

Info om det vi läst och bildexempel: https://developer.mozilla.org/en-US/docs/Web/CSS/font-smooth


- Ikoner - 

* Ikonerna som används är "fetstilade" gratisversioner då de som används på sidan är betalversioner. 


 - Media query - 

 * Vi har gjort en "specialstyling" för "sign in / flagga / sweden" som finns i högra hörnet i desktop-versionen. Vi kunde inte få till display none när vi la min-width som vi gjort med det övriga innehållet och behövde här ange max-width istället. Vi vet att vi fick en rekommendation på att inte blanda max/min-width. Försökt vara så tydliga som möjligt med just detta i koden. 


 - Mobil/tablet - 

* Headern ska vara fixed men pga nyhetsbrev-länken i toppen fungerar det inte att positionera den så när vi skrollar vår sida, då andra element hamnar bakom. Vi har testat z-index och att även göra nyhetsbrev-sektionen fixed utan lösning. Då detta inte fungerar tror vi javascript är lösningen då nyhets-brevlänken "trollas bort", samt en funktion dyker upp som som gör att logotypen i headern ändras till "Top" när man scrollar neråt på sidan. 

* Efter vårt samtal 23/9 på Teams testade vi att göra headern fixed igen och ta bort "Nyhetsbrev"länken. Vi har problem med att det är en liten "glipa" som syns längst upp i toppen där man ser innehållet på det som skrollas ovanför headern. Vi har försökt justera igen genom z-index, göra headern större och lägga till padding/margin på någon av berörda element men denna glipa försvinner inte. Vi har därför valt att ha kvar headern i position static med nyhetsbrev-länken ovanför.  

* "Nyhetsbrev-länken" i toppen och "headern" ligger i separata delar i bodyn för att vi inte kan styra dessa visuellt som vi vill annars. På riktigt tror vi att nyhetsbrev-delen också ligger i headern men javascript behövs för att "trolla bort" nyhetsbrev-delen när man skrollar på sidan i mobil- och tablet-version.

* Vi har valt att lägga margin på bodyn för att sidan ska få jämna marginaler i kanterna på hela innehållet. I och med detta kan vi inte få linjen som ligger under nyhetsbrev-länken att gå ut hela vägen i höger och vänster kant. Vi har testat andra sätt, men får inte till jämn marginaler på innehållet då. 

* Vi har fått trixa med storleken på vissa bilder och delar som innehåller bildinnehåll för tablet/desktop-version då vi använt oss av display grid i mobilversionen. Denna verkar lägga marginal runt och mellan bilderna som vi inte kan styra eller ta bort i tablet- och desktopversionerna - där vi istället valt att använda oss av display flex.


- Desktop -

* Originalsidans scrollbar till vänster "trollas bort" när man skrollar förbi den sista bildsektionen och footern. Vi kunde inte få till denna funktion med hjälp av html/css. Vad vi kunnat läsa oss till är detta också en funktion som kan lösas med javascript.

* Vår scrollbar är nu fixed men syns hela vägen ner till sidans botten. Vi har testat z-index och olika postioner för elementen men utan resultat, därav tror vi att javascript kan lösa problemet.

* Det "dyker upp" en top-ikon i nedre höger hörn när man skrollat ner en viss bit på originalsidan. Denna lösning har vi inte heller valt att ha med då vi gissar att den också behöver lösas med hjälp av javascript.

De delar som troligen rör javascript påverkar även andra element, tex att ikoner som är fixerade inte är positionerade helt uppe i hörnen när man skrollar sidan pga att de förhåller sig till marginalen för nyhetsbrev-sektionen i toppen. Vi har observerat detta och gjort så snarlikt vi kan med hjälp av CSS.

/Sara & Lisa Marie