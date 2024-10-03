# Data Analytics Project “S&P 500 - Historical Data”

Analyse van Historische Trends, Volatiliteit en Prestaties van de S&P 500 (1927-2024)

2024

Algolimit

+31643685656

[algolimit@protonmail.com](mailto:algolimit@protonmail.com)

[GitHub Repo](https://github.com/algolimit/sp500)

# Inhoudsopgave
- [Inleiding](#inleiding)
- [Data Verzamelen](#data-verzamelen)
- [Data Voorbereiding](#data-voorbereiding)
- [Analyse Methoden](#analyse-methoden)
  - [Trendanalyse](#trendanalyse)
  - [Volatiliteitsanalyse](#volatiliteitsanalyse)
  - [Voorspellende Modellen](#voorspellende-modellen)
- [Resultaten en Discussie](#resultaten-en-discussie)
- [Conclusies](#conclusies)
- [Referenties](#referenties)

## Inleiding

De S&P 500-index, een van de meest gevolgde aandelenmarktindicatoren wereldwijd, biedt een uitgebreide weerspiegeling van de economische gezondheid en de markttrends in de Verenigde Staten. Dit project is gericht op het analyseren van de historische gegevens van de S&P 500 van 1927 tot 2024 om inzicht te krijgen in de algemene trend van de index over bijna een eeuw.

### Onderzoeksvragen

Door dit onderzoek willen we de volgende vragen beantwoorden:

1. **Wat is de algehele trend van de S&P 500-index van 1927 tot 2024?** Hierbij richten we ons op de lange-termijn bewegingen om te bepalen hoe de index zich over de decennia heeft ontwikkeld.

2. **Zijn er specifieke perioden van significante groei of daling geweest?** We zullen periodes zoals de Grote Depressie, de Dot-Com Bubble, de financiële crisis van 2008, en de COVID-19-pandemie onderzoeken om te zien hoe deze gebeurtenissen de index hebben beïnvloed.

3. **Wat zijn de belangrijkste keerpunten in de geschiedenis van de index en welke externe factoren hebben mogelijk invloed op deze punten gehad?** Dit deel van het onderzoek zal zich concentreren op het identificeren van keerpunten in de index en het analyseren van externe economische, politieke, en sociale factoren die bij deze veranderingen een rol hebben gespeeld.

### Doel van het Onderzoek

Het doel van dit onderzoek is om een grondig begrip te verkrijgen van de dynamiek van de S&P 500-index door de jaren heen, om zo beter inzicht te krijgen in de factoren die grote marktbewegingen veroorzaken. Dit zal niet alleen helpen bij het begrijpen van historische trends, maar het zal ook waardevolle lessen bieden voor toekomstige marktanalyse en economische voorspellingen.

## Data Verzamelen

### S&P 500 Index Data

De primaire dataset, `sp500.csv`, gebruikt voor dit onderzoek is verzameld van [Kaggle](https://www.kaggle.com/datasets/paveljurke/s-and-p-500-gspc-historical-data/code). Deze dataset bevat historische gegevens van de S&P 500-index van 1927 tot 2024, inclusief dagelijkse openings-, sluitings-, hoogste- en laagsteprijzen, evenals het handelsvolume.

### Economische Indicatoren

Aanvullende economische datasets zijn verzameld om de invloed van bredere economische factoren op de S&P 500 te analyseren:

- **Real Effective Exchange Rate**: De dataset `Real Effective Exchange Rate.xlsx` is afkomstig van het [World Bank Data Catalog](https://datacatalog.worldbank.org/search/dataset/0037798). Deze bevat maandelijkse gegevens over de effectieve wisselkoersen, wat inzicht biedt in de internationale handelscompetitiviteit van de VS.

- **Unemployment Rate**: De werkloosheidscijfers, een belangrijke indicator voor de economische gezondheid, zijn ook verzameld van de [World Bank](https://datacatalog.worldbank.org/search/dataset/0037798). Deze dataset biedt maandelijkse werkloosheidscijfers, wat helpt bij het beoordelen van de binnenlandse economische omstandigheden.

### Major Economische Events

Er is een handmatige tabel gecreëerd die belangrijke economische gebeurtenissen documenteert, zoals financiële crises, beleidswijzigingen en andere significante gebeurtenissen die een directe impact kunnen hebben op de marktvolatiliteit en indexprestaties. Deze tabel is essentieel voor het correleren van marktbewegingen met externe economische gebeurtenissen tijdens de analysefase.

### Data Integratie

Deze verzameling datasets zal worden geïntegreerd door middel van gemeenschappelijke kenmerken zoals datums en economische indicatoren, om een uitgebreide dataset te vormen die zal worden gebruikt voor verdere analyse. Dit stelt ons in staat om een holistisch beeld te krijgen van de factoren die de S&P 500 beïnvloeden.

### Beschrijving van de Dataset

De primaire dataset `sp500.csv` omvat verschillende kolommen zoals datum, open, hoog, laag, sluiten, en volume, die de dagelijkse prijsacties van de index vertegenwoordigen. Elke rij in de dataset vertegenwoordigt de marktgegevens van een specifieke handelsdag, waardoor we een gedetailleerd beeld krijgen van de marktbewegingen over een periode van bijna een eeuw.




---------------------------------------------------------------------------------------------------------------

### Verzamelproces

Het verzamelproces omvatte de volgende stappen:

1. **Registratie op Kaggle**: Om toegang te krijgen tot de dataset, was het noodzakelijk om een account op Kaggle aan te maken.

2. **Dataset Downloaden**: Na het registreren en inloggen op Kaggle, werd de dataset gedownload in CSV-formaat, wat zorgt voor gemakkelijke integratie en manipulatie in data-analyse tools zoals Python en R.

3. **Data Inspectie**: Voorafgaand aan de analyse werd een initiële inspectie van de dataset uitgevoerd om de integriteit en volledigheid van de gegevens te verzekeren. Dit hielp eventuele ontbrekende waarden of anomalieën in de dataset te identificeren.

### Uitdagingen

Tijdens het verzamelproces werden enkele uitdagingen ondervonden, zoals het verzekeren van de volledigheid van de data over de lange tijdsspanne en het begrijpen van de impact van marktveranderingen op de beschikbare data. Daarnaast was het cruciaal om een nauwkeurige kalibratie van de datums te verzekeren om consistente en betrouwbare tijdreeksanalyses uit te voeren.

### Ethische Overwegingen

Hoewel de gegevens openbaar beschikbaar zijn, werd er zorg gedragen om de gegevens alleen voor onderzoeksdoeleinden te gebruiken, met respect voor de richtlijnen en voorwaarden gesteld door Kaggle.

Deze zorgvuldig gecureerde dataset vormt de basis van onze analyse, waarmee we diepgaande inzichten in de trends en dynamieken van de S&P 500-index door de decennia heen zullen verkrijgen.


## Data Voorbereiding
Beschrijf de stappen die je hebt ondernomen om de data schoon te maken en voor te bereiden voor analyse. Dit kan het omgaan met ontbrekende waarden, het normaliseren van gegevens, en het transformeren van variabelen omvatten.

## Analyse Methoden
### Trendanalyse
Detailleer hoe je trends hebt geïdentificeerd in de S&P 500-data. Welke statistische technieken of grafieken heb je gebruikt?

### Volatiliteitsanalyse
Beschrijf hoe je de volatiliteit van de S&P 500 hebt geanalyseerd. Welke tools of modellen waren het meest effectief?

### Voorspellende Modellen
Bespreek welke modellen je hebt gebruikt om toekomstige bewegingen van de S&P 500 te voorspellen. Hoe heb je deze modellen geselecteerd en getest?

## Resultaten en Discussie
Presenteer de belangrijkste bevindingen van je analyse. Wat zeggen de resultaten over de markt? Wat zijn de implicaties van deze resultaten?

## Conclusies
Vat de belangrijkste resultaten samen en reflecteer op de onderzoeksvragen. Welke conclusies kun je trekken? Wat zijn de beperkingen van je analyse?

## Referenties
Lijst van alle gebruikte bronnen tijdens het onderzoek en het schrijven van je document.

