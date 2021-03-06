# Good morning application - OpenAPI

Nina Sjöberg,
Kurs: JavaScript 2, Nackademin ht 16 - vt17


Länk till appen/sidan: http://openapi.surge.sh/

Länk till repo: https://github.com/ninasjoberg/Open_api

## Uppgift:

Du ska skapa en applikation som hämtar data från ett eller flera öppna APIs och visar upp denna data på en html-sida. Målet med uppgiften är att få en bättre översyn över hur AJAX och asynkront JavaScript fungerar.



## Syfte och funktionalitet: 

Denna applikation ger dig den viktigaste informationen du behöver på morgonen när du vaknar, allt på ett ställe. Du kan kolla vädret efter sökning på 'location' eller få väder baserat på din nuvarande position. Du får även en slumpad senaste nyhet från New Yourk times, vill du se fler nyheter kan du trycka på 'update news'. Jag vaknar ofta till en antal pushnotiser med nyheter om skjutningar och terrordåd, jag går sen också ofta in och kollar dagens väder i någon av mina väderappar. Detta gör en inte alltid på så gott humör, därför visar min app även en sektion med "dagens katt" för att du ska ha en chans till att starta dagen med ett gott humör. 

## Till denna applikation har använts:

- Vanilla JavaScript
- Fetch - ajax requests
- Bootstrap 

Design pattern: 
- Revealing Module patter

## Dessa api:er har använts:

- Openweathermaps api - för att få ut info om vädret: http://openweathermap.org/api
- The New Yourk Times api -  för att få ut nyheter: https://developer.nytimes.com
- imgurs api - för att hämta ut bilder på katter: https://api.imgur.com
- ipinfo - för att hämta ut användarens position: http://ipinfo.io

## Arbetsprocess:

Jag hade många planer och ideer inför denna uppgift, men jag hade svårt att hitta api:er som var användbara för ändamålet. Jag bestämde mig därför för att använda Smhi:s api och ta ut väder och sedan ge aktivitetstips baserade på vädret. Jag hade då hoppats att kunna använda yelp's api eller google places, men insåg sedan att båda dessa bara gick att använda server-side. Smhi:s api var inte heller särskilt pasande för upgiften då det bara gick att hämta hem ett reguest med all info. Så jag tänkte om igen, bestämde mig för att använda openweathermap's api där man kan få ut mer indformation och ställa mer specifika requests. Sen kollade jag helt enkelt på vilka api:er det fanns att tillgå som passade denna upgift, jag hittade Times api och iden till min slutgiltiga produkt kom till. 

Tyvärr så kan openweathermap inte anropas över https (om man inte betalar massa pengar), det går därför inte att använda denna app i gh-pages. Se ist. länk till sidan ovan. 

Jag tycker personligen att applikationen gör sig bäst i mobilen, dessvärre har fetch inte så bra stöd i iOS Safari, dessa användare måste se till att ha senastee versionen 10.3 för att fetch requesten ska fungera. I IE fungerar det tyvärr inte alls. 

## Förslag på framtida funktionalitet/förbättringar:

- Ge använadaren möjlighet att välja vilka kategorier av nyhetsartiklar hen vill läsa
- Lägga till exempelvis läget i tågtrafiken och på vägarna baserat på vart användaren befinner sig
- Bygga på den ursprungliga iden om att ge förslag på aktiviteter baserat på väder
- Jobba vidare på designen i laptopvy, så att sidan känns mindre rörig. 
- Göra en egen inforuta där felmeddelanden, info osv kan visas. Istället för att använda den inbyggda 'alert'.

