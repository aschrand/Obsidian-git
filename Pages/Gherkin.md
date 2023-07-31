---
created: 2023-07-14T10:17:11 (UTC +02:00)
tags: [ICT, testen]
source: http://www.toets-je-parate-kennis-over.nl/software-testen/kennisbank/gherkin-syntax/
author: 
---

# Gherkin Syntax - Uitleg van de basis onderdelen van Gherkin - TestTalk

> ## Excerpt
> De Gherkin syntax uitgelegd aan de hand van een voorbeeld. Aan bod komen: feature file, scenario, given-when-then, And, but, background en scenario outline.

---
Binnen een [Behaviour Driven Development]( https://www.toets-je-parate-kennis-over.nl/software-testen/kennisbank/behaviour-driven-development/ "Behaviour Driven Development") (BDD) story vormen de scenario’s een belangrijk onderdeel. Elk scenario beschrijft een(1) enkel gedrag van een functie. Ze dienen als requirement en [testcase]( https://www.toets-je-parate-kennis-over.nl/software-testen/kennisbank/testgeval-software-testen/ " testcase"). In dit artikel wordt kort ingegaan hoe de scenario’s in de [Gherkin]( https://www.toets-je-parate-kennis-over.nl/software-testen/kennisbank/gherkin-syntax/ "Gherkin") feature files beschreven moeten worden.

## Introductie van Gherkin

![Gerkin Syntax](http://www.toets-je-parate-kennis-over.nl/software-testen/wp-content/uploads/sites/3/2017/12/augurken-300x224.jpg)De in een [BDD story]( https://www.toets-je-parate-kennis-over.nl/software-testen/kennisbank/story-bdd/ "BDD story") gebruikte Given-When-Then opzet is door Cucumber uitgewerkt naar de [Gherkin]( https://www.toets-je-parate-kennis-over.nl/software-testen/kennisbank/gherkin-syntax/ "Gherkin") taal. Gherkin kan gebruikt worden als basis voor het automatiseren van de [testen]( https://www.toets-je-parate-kennis-over.nl/software-testen/kennisbank/software-testen/ "testen"). Cucumber is een van de bekendste [BDD]( https://www.toets-je-parate-kennis-over.nl/software-testen/kennisbank/behaviour-driven-development/ " BDD") testautomatiserings frameworks. De meeste andere BDD frameworks gebruiken ook Gherkin, maar zijn niet altijd 100% compatibel met de Gherkin standaard van Cucumber.

De scenario’s worden met behulp van Gherkin uitgewerkt in .feature files. Deze files worden later door een BDD testautomatiserings tool uitgevoerd.

**Voorbeeld .feature file**

**Feature****:** Webshop bezoeker ziet gerelateerde producten bij bekijken product  
As a product manager  
I want dat een bezoeker van de webshop gerelateerde producten te zien krijgt bij een product  
So that de omzet per order met minimaal 5% verhoogd wordt

**Scenario**: Voorradige gerelateerde producten  
Given het product “roerstaafjes” heeft 2 gerelateerde voorradige producten  
When de webshop bezoeker het product “roerstaafjes” bekijkt  
Then worden de 2 gerelateerde producten getoond

Binnen Gherkin moet iedere niet lege regel beginnen met een Gherkin _keyword,_ gevolgd door een willekeurige tekst.

De belangrijkste _keywords_ zijn:

-   Feature
-   Scenario
-   Given, When, Then, And, But (Steps / stappen)
-   Background
-   Scenario Outline
-   Examples
