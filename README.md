# API Horeca Finder

## Week 1

### Wat heb ik gedaan?

Tijdens week 1 ben ik vooral bezig geweest met het idee verzinnen van mijn API project. Ik wist echt niet waar ik een website over moest maken en ook niet hoe ik een api of content apis ervoor zou moeten gebruiken. Ik ben gaan brainstormen samen met Jad om iets te zoeken waar ik mee aan de slag kon. Uiteindelijk ben ik op een Horeca Finder gekomen. Ik weet nog niet hoe ik het uiteindelijk wil noemen maar we beginnen hiermee. 

Als eerst ben ik begonnen met het ondekken van Astro. Ik heb hier zelf nog nooit eerder mee gewerkt. Ik ben op hun website zelf gaan kijken naar wat er allemaal mogelijk is met Astro.Vervolgens ben ik opzoek gaan naar een API waar er genoeg informatie over de horeca in Amsterdam te vinden was. Ik ben toen bij de Explotatievergunning Amsterdam API uitgekomen. Hier staat allerlei data in over wat voor een categorie de horeca is, tot hoelaat ze open zijn, of er een terras is etc. Toen ben ik de API gaan inladen in mijn ontwerp en heb ik een stuk of 20 horecas kunnen inladen.

Mijn idee was om op basis van het stadsdeel te bekijken welke horecas er zijn. Helaas stond dit zelf niet in de API. Ik heb op internet opgezocht welke postcodes vallen onder welk stadsdeel. Op basis van die informatie heb ik samen met Jad op basis van de postcodes een selectie kunnen maken en ze op basis daarvan aan een stadsdeel kunenn koppelen. Als er nu een horeca word ingeladen dan word er dus automatisch een stadsdeel aangekoppeld. 

### Wat heb ik geleerd?

Ik heb voor het eerst gewerkt met Astro en geleerd hoe je een API inlaadt en de data vervolgens verwerkt. Ik heb ook geleerd Een belangrijk inzicht was dat API-data niet altijd precies bevat wat je nodig hebt en dat je dan zelf extra logica moet toevoegen. In dit geval heb ik op basis van postcodes zelf een stadsdeel-waarde gekoppeld aan elke horeca, wat iets is wat de API zelf niet bood.

### Voortgang

Het is nu moeilijk om een eindontwerp voor ogen te zien omdat er nog geen styling is gedaan. Ik moet goed nadenken wat het daadwerkelijke concept is en daar verder op voortbouwen.

## Week 2

### Wat heb ik gedaan?

Deze week heb ik de Local Storage workshop van Jad gevolgd. Daarnaast ben ik aan de slag gegaan met dynamic routes in Astro. Elke pagina moest een unieke URL hebben, dus hiervoor heb ik de zaaknummers uit de API gebruikt als ID. Zo ontstond de bestandsstructuur [id].astro, waarbij elk zaaknummer automatisch een eigen detailpagina krijgt. 

### Wat heb ik geleerd?

Ik heb geleerd hoe Local Storage werkt en hoe je daarmee data in de browser kunt opslaan zonder een database. Dit is handig voor dingen als favorieten bijhouden of filterinstellingen onthouden tussen bezoeken.

Daarnaast heb ik geleerd hoe Astro dynamic routes werken. Een dynamic route in Astro heeft altijd getStaticPaths() nodig, die alle mogelijke pagina's vooraf genereert. Zonder die functie weet Astro niet welke pagina's er bestaan.

<prev> [id].astro — voorbeeld van een dynamic route
export async function getStaticPaths() {
  // Haal alle horecas op en geef voor elk een id terug
  return horecas.map((horeca) => ({
    params: { id: horeca.zaaknummer },
  }));
} </prev> 

## Week 3

### Wat heb ik gedaan?

In week 3 heb ik de styling afgemaakt en een tweede API toegevoegd: de Open-Meteo API. Deze geeft het huidige weer en de temperatuur in Amsterdam weer op de pagina. Dit was ook meteen mijn tweede Web API naast de Exploitatievergunning API, wat nodig is voor de opdracht.

### Wat heb ik geleerd?

Ik heb geleerd hoe je meerdere API's in één project combineert. De Open-Meteo API werkt anders dan de Amsterdam API — er is geen authenticatie nodig en de data-structuur is heel anders opgebouwd. Het is dus elke keer opnieuw uitzoeken hoe een API in elkaar zit voordat je er iets mee kunt doen.
Terugkijkend op het project heb ik veel nieuwe dingen geleerd: Astro, API's inladen en combineren, dynamic routes, en Local Storage. Het project begon met veel onzekerheid over wat ik wilde maken, maar door stap voor stap te werken en goed te kijken naar wat de API bood, is er toch een werkend concept uitgekomen.

## Week 4

### Wat heb ik gedaan?

Ik heb de hele styling aangepast van de site om het beter te maken voor de gebruiker. 

## Bronvermelding 

- API postcodes onderscheiden 
- Astro Routing - https://docs.astro.build/en/guides/routing/
- Claude - "hoe maak ik van een string met kleine letters een string met hoofdletters in javascript?"