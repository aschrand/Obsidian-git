---
cssclass: dashboard

---
# Aantekeningen
- ### 💼 Werk
	- [[Artikelen]]
	- [[Definities]]
	- [[Inzichten]]
	- [[Producten]]
	- [[Organisaties]]
- ### 📚 Programmeren
	- [[Voorbeelden]]
- ### 🏠Home Assistant
`$=dv.list(dv.pages('"Pages/Home Assistant"').sort(f=>f.file.mtime.ts,"desc").limit(5).file.link)`
- ### 🆘 Cheatsheets
`$=dv.list(dv.pages('').where(p=>p.type && (p.type == "cheatsheet")).sort(f=>f.file.date,"asc").limit(5).file.link)`

# Vault Info
- ### 🗄️ Recent file updates
 `$=dv.list(dv.pages('').sort(f=>f.file.mtime.ts,"desc").limit(4).file.link)`
- ### 🔖 Tagged:  favorite 
 `$=dv.list(dv.pages('#favorite').sort(f=>f.file.date,"asc").limit(4).file.link)`
- ### 🗒️ Tagged:  Notities 
 `$=dv.list(dv.pages('').where(p=>p.type && (p.type == "notitie")).sort(f=>f.file.date,"asc").limit(4).file.link)`
- ### 〽️ Stats
	-  File Count: `$=dv.pages().length`
	-  Architectuur: `$=dv.pages('"Architectuur"').length`
	-  ICT: `$=dv.pages('"ICT"').length`
	-  Softskills: `$=dv.pages('"Softskills"').length`
---

>[!summary]- Definities
>```dataview 
>TABLE author, file.folder
> WHERE type = "definitie"
> ```

# Tags

 >[!summary]- EA en BA
>```dataview 
> Table  type, file.folder, author
> from #ea or #BA 
> SORT file.name ASC
> ```

>[!summary]- IT
> ```dataview 
> Table  type, file.folder, author
> FROM #IT
> SORT file.name ASC
> ```

>[!summary]- Micorservices
> ```dataview 
> Table  type, file.folder, author
> FROM #microservices
> SORT file.name ASC
> ```

>[!summary]- Zorg
> ```dataview 
> Table  type, file.folder, author
> FROM #zorg
> SORT file.name ASC
> ```

>[!summary]- AI
> ```dataview 
> Table  type, file.folder, author
> FROM #ai
> SORT file.name ASC
> ```