---
source: https://www.ct.nl/workshops/winget-update-en-installeer-programmas-in-een-handomdraai/
created: 2022-11-01
type: cheatsheet
---

In het eenvoudigste geval download je software met winget install programmanaam en installeer je het in één keer. Metuninstall in plaats van install kun je je ontdoen van een programma en met upgrade kun je een bestaande update installeren.

Om alle programma-updates te installeren die winget kent, zou je eenvoudigweg het commando **winget upgrade –r** kunnen gebruiken.

Als je je softwareverzameling up-to-date wilt houden met winget maar niet wilt vertrouwen op het commando **winget upgrade –r**, dan is de procedure meestal als volgt:

Gebruik eerst het commando winget upgrade om een overzicht te krijgen van welke updates beschikbaar zijn.
Maak vervolgens met behulp van kopiëren en plakken een commando voor elk programma dat moet worden bijgewerkt volgens het patroon **winget upgrade–id Program.ID**
