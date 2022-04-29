# Web Typography, 2020/2021

Als je doof bent, of als je om een andere reden geen geluid kunt horen, dan mis je veel informatie als je een film kijkt. Knisperende voetstappen, langzaam aanzwellende muziek, nerveus getik op een deur, je hoort het natuurlijk allemaal niet. Nu bestaat er zoiets als *closed caption*, wat een type ondertiteling is waarbij ook dingen als omgevingsgeluiden en de muziek beschreven worden. Hierdoor krijgt een kijker die informatie wel binnen.

Alleen wordt die auditieve informatie nogal neutraal beschreven. Het geluid van huilend persoon zou bijvoorbeeld beschreven kunnen worden als *snikgeluid op de achtergrond*. En iemand die lacht zou geschreven kunnen worden als *iemand lacht.* Heel neutraal, bijna zakelijk, en bovendien allebei in precies hetzelfde neutrale lettertype. Terwijl het toch echt over twee heel verschillende emoties gaat. 

Dat kan visueel sterker. 

En dat gaan jullie doen.

## Leerdoelen

- Je kan de kennis over vormgeving die je hebt opgedaan tijdens de minor technisch toepassen met behulp van CSS
- Je kan verborgen nuance uit een audiotrack overtuigend vertalen naar visuele (typografische) beelden
- Je kan je typografische keuzes onderbouwen.
- Je hebt de exclusive design principles gebruikt.

__Exclusive Design__
- Study situation
<br>In order to become specialist designers for all kinds of people with all kinds of disabilities we have to study different, individual situations.

- Ignore conventions
<br>The current conventions are designed by, and thus for, designers. Not all of these conventions work for non-designers. If we want to include non-designers, and especially people with disabilities, we should reconsider these conventions, after we studied their situations.

- Prioritise identity
<br>Including excluded people into our design process, by seeing them as co-designers rather than study objects, can help in coming up with new, and relevant, conventions.

- Add nonsense
<br>Designing for people with disabilities is in large part uncharted territory. Nonsense can be a useful tool to investigate the unkown. And it’s fun.

## Oplevering

Je levert een werkende versie op, gemaakt met HTML, CSS en JavaScript. Deze staat op Github. In een duidelijke readme documenteer en onderbouw je je ontwerpkeuzes. Je developmentgeschiedenis is terug te vinden op GitHub.

Je levert ook een *screen recording* met audio op van je fragment. Dit is een video van de definitieve versie, gemaakt van jouw browserscherm.

De beoordeling is mondeling en volgt [de rubric uit het beoordelingsformulier](web-typografie-beoordeling.pdf).

## Typografische restricties

Je *moet* een van deze twee opties kiezen, en je keuze moet je onderbouwen. In je readme staat een uitleg over je overwegingen om de ene of de andere restrictie te kiezen.

### Optie 1: Systeemfont

De eerste optie is dat je gebruik maakt van het zogenaamde *systeemfont* van degene die naar jouw werk kijkt. Dit font verschilt per operating system, en het verschilt soms zelfs per versie van het operating system. Het is ook aan te passen door de gebruiker zelf. 

Je hebt dus geen controle over welk lettertype er precies gebruikt wordt. Het levert dus een onzeker, en beperkt typografisch palet op. Je hebt geen *light* versies, of *extrabold*. En ook geen serif en sans-serif versie van dezelfde familie. In dit geval heb je alleen de beschikking over normal, **bold** en _italic_. Dit heeft natuurlijk ook zijn voordelen!

### Optie 2: Brenner

Je kan er ook voor kiezen om gebruik te maken van de complete Brenner familie. Dit is een zeer uitgebreid en uiterst flexibel font. [Hier kan je je verdiepen in dit font](https://www.typotheque.com/blog/brenner_an_unusual_typeface_family_with_distinct_voices). Als je kiest voor dit font dan heb je de beschikking over een *sans serif*, een *condensed*, een *serif*, een *monotype*, een *slab*, een *display* en een *script* versie. En veel van deze versies hebben varianten van *light* tot *bold*, en allemaal zowel *bold* als *italic*.

Met Brenner zijn er natuurlijk veel en veel meer mogelijkheden dan met systeemfonts. Dat kan zowel een voordeel als een nadeel zijn. 

Voor een overzicht, zie [de brenner.pdf](brenner.pdf).

## Het fragment

Ik heb een fragment voorbereid. Het gaat om twee scenes uit *Blade Runner 2049*. De captions staan in de HTML, en ze verschijnen in sync met de video. [Kijk maar](closed-captions/index.html).

### De captions

De captions staan in de html, in het bestand index.html. Je kan aan elke paragraaf eventueel een of meer classes toevoegen. Bijvoorbeeld `voice1` of `voice2 soft`. Classes voeg je handmatig toe in de html.

Met JavaScript worden er een paar dingen extra gedaan: 

- er wordt aan elke paragraaf een unieke class toegevoegd (`p0`, `p1`, etc)
- Elk woord wordt in een aparte `span` gezet. Hierdoor kan je elk woord apart stylen, en eventueel ook [na elkaar laten verschijnen](https://github.com/cmda-minor-vid/web-typography-18-19/blob/master/closed-captions/css.css#L41).

### Tijdens het afspelen

Tijdens het afspeelen wordt er een class `on` op de caption gezet als hij moet verschijnen, en een class `off` als hij klaar is. *Zowel class `on` als class `off` blijft op de caption staan!*

De timimg van de captions kan je aanpassen in [closed-captions/captions.js](closed-captions/captions.js).

Er verschijnen ook classes op de body op momenten dat er geluiden worden afgespeeld, zoals `sound1` en `sound2`. Je kan geluiden toevoegen in [closed-captions/sounds.js](closed-captions/sounds.js).

*let op,* de geluiden zijn niet compleet, dit zal je zelf moeten aanvullen.

## Een eigen fragment (afgeraden, uitgebreide onderbouwing is nodig)

Je kan er ook voor kiezen om een eigen, *beter* fragment te gebruiken. Dit wordt afgeraden. De tijd die je besteedt aan het zoeken naar dat fragment kan je beter besteden aan het werken aan de opdracht. Bovendien blijkt dat er vaak fragmenten worden gekozen die niet goed voldoen aan de opdracht. Als je een ander fragment kiest dan *moet* je dit goed onderbouwd voorleggen aan je docent. De deadline hiervoor is vrijdagochtend in de eerste week.

### Waar moet je op letten bij het kiezen van een eigen fragment.
Lees de opdracht nog eens goed door. Waar gaat het ook al weer precies om? 

Voor een goede onderbouwing van je keuze voor een ander fragment moet je deze vragen in elk geval beantwoorden:

- Welke informatie zit er in de audio die echt niet zichtbaar is?
- Welke rol speelt de audio in het fragment?
- Werkt de scene nog zonder geluid?
- Waarom is dit fragment beter dan het aangeboden fragment?

Je kan dan de nodige HTML en JavaScript genereren door gebruik te maken van [caption generator](https://cmda-minor-vid.github.io/web-typography-18-19/generator/) (in Google Chrome). 

Als je de closed captions wil bewerken dan kan je een tool zoals [Amber Script](https://www.amberscript.com/en) gebruiken. Daar kan je exporteren als `.srt`, en die kan je weer door de generator halen.

# Verantwoording
## __Font__
- Ik heb een keuze gemaakt voor het Brenner font en dan de Sans variant. Ik heb hiervoor gekozen omdat dit type van het font naar mijn idee goed leesbaar is en duidelijk opvalt bij sommige achtergronden die ik toe pas tijdens het afspelen van de video. Het is belangrijk dat de ondertiteling goed leesbaar is voor de doelgroep aangezien zij de video niet zullen kunnen horen. 👂
- Het Brenner font heeft veel diversiteit in font-style, font-weight en meer. Hierdoor kon ik het naar mijn eigen smaak ook stylen in de css en toepassen bij de ondertiteling van de video tot in tegen deel als ik het systeem font had gekozen, waarbij ik dat niet had kunnen doen. 


## __Effecten__
1. Ik heb diverse animaties/effecten toegepast tijden het afspelen van de video. zodra de video begint zie je dat de video begint mee te trillen met het geluid om de achtergrond wat klinkt als een hard bas geluid waardoor het gaat trillen. 
2. Zodra je een eerste soort piep geluid hoort zie je dat de video groter wordt, dus mee beweegt met het piep geluid.
3. Vervolgens hoor je een soort politie piep geluid. Hierbij heb ik een gradient laten meebewegen van de rechterkant van het scherm naar de linker kant.
4. 3de piep geluid vond ik klinken alsof je door een decontaminatie gang loopt en heb om die reden er dan een soort rook effect op de achtergrond geplaatst. 
5. Beweegt de video mee van de schrik van de hoofdpersoon omdat hij ineens wordt uitgescholden door iemand die langsloopt. Ik vond dat het schrik effect van de hoofdpersoon erg op de achtergrond was waardoor hij mij de eerste keer niet opviel dat hij schrok. Ik wilde het om die reden wat meer naar voren laten komen. 
6. 4de piep is dezelde piep als punt 3. 
7. Vanaf 00:28 begint de video mee rond te schudden op basis van hoe hard de piep op de achtergrond te horen is. die wordt exponentieel een ergere beweging. 
8. 5de  piep is dezelde piep als punt 3. 
9. Wanneer het hoofdpersonage alle vragen heeft beantwoord wat rond 1:15 is. Komt er confetti te voorschijn op de achtergrond want hij heeft het succesvol gehaald!
10. Wanneer de volgende scene is, begint het scherm met het pulseren. Dit heb ik gedaan omdat ik zelf een nerveus gevoel kreeg van de scene aangezien en snelheid van zijn antwoorden niet altijd even snel waren en pauzes bevatten. Naar mijn idee kwam het over alsof hij zich onder druk gezet voelde. Ik heb dit uitgebeeld door het scherm dus te laten pulseren. Dit wordt ook exponentieel meer pulserend. 
11. Vanaf 1:43 detecten ze dat er iets mis is met hem in het beeld en gaat het niet helemaal goed en beginnen ze hun vraagtekens te krijgen bij zijn antwoorden. Ik heb dit uitgebeeld door een static effect op de achtergrond toe te passen. Static effect kwam vroeger op de tv voor wanneer er iets mis mas met de zender en je vroeg je dan vaak af 'Wat is er mis?'. Ik heb dit dus met een static achtergrond effect meer naar voren laten kwamen, dat gevoel van vraagteken.
12. Vanaf 1:43 heb ik het volgende static effect toegepast. om dezelfde reden en om het enge geluid wat je dan harde hoort meer naar voren te laten komen met een ander soort static effect. 
13. vanaf 2:02 heb ik een raar 'trippy' effect toegepast waarmee ik wil aanduiden dat er iets niet goed is met hem omdat hij anders begint na te denken dan 'normaal' is 'toegestaan'. 
14. Als laaste effect verander ik de achtergrond kleur naar dezelfde kleur van de kamer op video als een soort aanduiding van dit is het einde van de video. 


## __Ondertiteling__
- Tijdens het stylen van de ondertiteling heb ik  gekeken naar hoe ik het gevoel van de video ook in de tekst naar voren kan laten komen. <br> 
- Dit heb ik bijvoorbeeld gedaan door de tekst een transition te geven en de em aan te passen dit gaf het effect als de tekst groter of kleiner werd. 
- Een vervaag effect over de tekst te laten gaan wat helder wordt wanneer het gezegd wordt.
Vervaag effect: Heb ik gedaan omdat het voelt alsof de persoon veel zegt, achter elkaar maar het wel op een bepaalde snelheid doet. (langdradig gevoel ook).
<br> 
- Het lastigste text effect om toe te passen was de shine bij het gedeelte van wanneer 'within cells interlinkt' drie keer wordt herhaald achter elkaar. Doordat hij dit drie keer moest herhalen gaf mij dit een soort gemaakt polished gevoel. Hier zal ik in mijn proces dieper op in gaan. 
<br> 
- Ik heb gespeeld met diverse text effecten omdat ik daar zelf ook meer mee wilde spelen om te kijken wat er allemaal mogelijk is en wat mij zelf allemaal lukt.


## __Exclusive Design__
__Ik heb diverse pricipes van exclusive design toegepast:__ 
- Study situation
<br>Ik heb deze helaas niet echt kunnen toepassen aangezien we niet konden testen met de doelgroep, tevens heb ik ook geen connecties met de doelgroep. 
<br> Wel heb ik mij proberen in te leven in de doelgroep door de video ook af te spelen zonder geluid aan het begin en wanneer ik bezig was met het maken van de effecten etc. in de video. 

- Ignore conventions
<br>Tijdens het maken van de animatie/effecten en meer heb ik er rekening mee gehouden dat de doelgroep dit ook zou moeten begrijpen. Dit heb ik gedaan door de video ook af te spelen zonder geluid. 

- Prioritise identity
<br>Ik heb er voor gezorgt dat de effecten die ik gebruik tijdens het afspelen van de video de emoties en geluideffecten in de video worden afgebeeld oormiddel van beeld. Dit heb ik gedaan door te focussen op hoe het geluid wil laten overbrengen in het beeld van de video, doormiddel van de effecten en ondertiteling effecten. 

- Add nonsense
<br>Ik heb tijdens het afspelen goed geluisterd naar de tonen, geluiden en meer in de video. een van de grappige dingen die ik heb toegevoegt is hoe de tekst beweest en het effect van confetti wanneer hij de eerste keer alle vragen juist beantwoord. 🥳


## __Proces__
- Voordat ik begon met het coderen heb ik eerst de video bekeken met en zonder geluid. Dit heb ik gedaan om de doelgroep beter kunnen begrijpen zonder het geluid. Vervolgens heb ik genoteerd wat ik hoorde. Ik heb vervolgens er over nagedacht hoe ik dit zou willen tonen op het scherm en welke gevoelens het bij mij naar boven brengt.
- stap 1 na het bekijken van de video is er achter te komen hoe de code werkt ik ben hier voor gaan zitten en heb gekeken wat het allemaal doet als ik het aanpas. Hierdoor kwam ik er achter wat ik allemaal kon veranderen in de code.
<br> 
-  Ik begon met de background te wijzigen stapje voor stapje en daarna achter een volgende wanneer ik de achtergrond had gewijzigd begon ik met de tekst dit deed ik tot het deel dat hij zijn eerste ondervraging had in de kamer. Daarna heb ik het deel dat hij ondervraagt werd in de kamer gecodeerd. 
- Toen ik dat gedaan had was het tijd voor het tweede deel van de video. Dit leek hetzelfde maar was niet zo want er waren anderen vragen en intonaties in zijn stem waren anders. Ik heb dit afgebeeld doormiddel van de achtergrond aan te passen en de ondertiteling anders te doen dan het eerste doel.  
<br><br>
- Tijdens mijn proces heb ik ook een website gebruikt om animatie (keyframes) in te maken. deze website staat ook vermeld in de code maar deze website heeft mij onder andere geholpen om te zien wat er allemaal mogelijk is. 
<br>Het toepassen in mijn eigen code was af en toe nog wel tricky maar het lukte mij wel op het om te zetten naar mijn eigen code en werkend te krijgen en daar ben ik best wel trots op. 
<br>Website: https://webcode.tools/generators/css/keyframe-animation
<br><br>
- Shine effect: Ik had het idee om dit op die manier af te beelden. Ik vond het effect op een CodePen en probeerde het toe te passen.
<br> De eerste keer lukte mij dit niet. Ik wist niet wat er mis was. Na het te laten liggen en een dag later terug te kijken. Zag ik iets wat ik nog niet geprobeerd had en dat was: Er stond wel
<br> -webkit-background-clip: text; maar nog geen --> background-clip: text;
Ik zette dit er vervolgens bij en dit werkte !! 😁

## Reflectie
Als ik nu mijn eindproduct zie ben ik hier trots op en ben ik achter diverse keyframe animatie gekomen wat mogelijk is en wat mogelijk is door een opacity of transition toe te passen. Ik vond dit een leuke opdracht en kon er veel mee spelen tijdens het proces ook waren er momenten dat ik er niet uitkwam hierbij vroeg ik de docent dan om hulp en dan liet hij mij handige trucjes zien. Deze heb ik dan ook vaker toegepast zoals, animation fill mode: forwards; en de background naar 0% of none te zetten in de keyframes om het te stoppen. 
<br>
__Ik heb veel geleerd van deze opdracht en mijzelf verbaast met wat ik eigenlijk kan! 😋__

