---
created: 2023-02-01T09:17:16 (UTC +01:00)
tags: [IT, EA]
source: https://www.bergler.nl/entropie-in-software-ontwikkeling/
author: Menno Jongerius
type: artikel
---

# Entropie in software ontwikkeling

>[!abstract]
> Entropie is begrip uit de thermodynamica waamee de mate van chaos van een systeem beschreven wordt. Van nature zullen system streven naar een toename in de entropie en dus een toename van chaos. Anderzijds zullen systemen neigen naar een toestand van de laagste energie, hierdoor zal een warm object wel spontaan afkoelen maar een koud object nooit spontaan opwarmen.

---
**Wat is goede architectuur**  
Er zijn tal manieren om naar architectuur van software te kijken. Zijn design patterns correct toegepast? Is de software modulair? Zijn SOLID principes toegepast? Vaak wordt dan de vraag gesteld wat goede architectuur is, en het antwoord op die vraag is nog niet zo eenvoudig gegeven. Op de lange termijn bewijst goede architectuur zich door lager onderhoud van de software en lagere kosten om wijzigingen door te voeren. Op korte termijn helpt architectuur ontwikkelaars op dezelfde manier te werken en om eenduidigheid te creëren.

**Entropie**  
Entropie is begrip uit de thermodynamica waamee de mate van chaos van een systeem beschreven wordt. Van nature zullen system streven naar een toename in de entropie en dus een toename van chaos (voor veel ontwikkelaars een herkenbaar proces in hun geliefde software oplossingen). Anderzijds zullen systemen neigen naar een toestand van de laagste energie, hierdoor zal een warm object wel spontaan afkoelen maar een koud object nooit spontaan opwarmen.

**De entropie benadering**  
Ik gebruik de vergelijking wel eens met dit principe van entropie als ik kijk naar software architectuur. Ik vind een architectuur goed wanneer het voor de ontwikkelaar minder energie kost om keuzes te maken die in lijn zijn met de ontworpen architectuur, dan keuzes die de architectuur principes overtreden. Met andere woorden, dat de toename van chaos geminimaliseerd wordt.  
Dit helpt me om samen met een team architectuur keuzes te maken, want als een gekozen oplossing de ontwikkelaars heel veel moeite kost om te onderhouden is hij niet toekomstbestendig. Ik heb gemerkt dat het toepassen van SOLID principes in een loosly coupled systeem (bijvoorbeeld door MEF of Unity te gebruiken) enorm helpt om ontwikkelaars snel te laten ontwikkelen in lijn met de architectuur.

[[Conways-law]]

