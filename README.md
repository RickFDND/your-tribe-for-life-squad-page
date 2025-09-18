# Your Tribe for Life Squadpage

Ontwerp en ontwikkel met een team een overzicht van jouw tribe met alle online visitekaartjes, op basis van een headless CMS en een framework.

Eén iemand in het team _Forked_ deze leertaak en nodigt de andere leden uit op betreffende repository. De instructie vind je in: [INSTRUCTIONS](https://github.com/fdnd-task/your-tribe-for-life-squad-page/blob/main/docs/INSTRUCTIONS.md)


## Informatie voor installatie
If you're seeing this, you've probably already done this step. Congrats!

#### create a new project in the current directory
`npx sv create`

#### create a new project in my-app
`npx sv create my-app`

### Developing
Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

`npm run dev`

#### or start the server and open the app in a new browser tab
`npm run dev -- --open`

### Building

To create a production version of your app:
`npm run build`

You can preview the production build with `npm run preview`.

To deploy your app, you may need to install an <a target="_blank" href="https://svelte.dev/docs/kit/adapters">adapter</a> for your target environment.

## Omschrijving van het project

Het project betreft de squad page van jaar 2 cohort 2025/2026. Dit project is gebouwd met Sveltekit, NodeJS en Directus. De squad page laat alle studenten uit deze cohort zien en heeft de mogelijkheid om te filteren op squad (Squad 2E/ Squad 2F). Wanneer er op een student geklikt wordt, wordt je doorverwezen naar een eigen pagina met leuke en interessante weetjes over de desbetreffende student. Op deze pagina kan er ook weer terug genavigeerd worden naar de homepagina om andere studenten te bekijken.

#### Figma Design:
https://www.figma.com/design/tOKwhcJA01KYY9lhTsJdB5/Team-Canvas-KRR?node-id=0-1&t=F0RA0wmzfvjA6W5i-1

## Ontwerpkeuzes uitleggen

Wij hebben gekozen om de kleuren van de FDND site te gebruiken, hierbij hebben wij geen andere kleuren gekozen en ons puur gehouden aan dit kleurenpallet. Wij hebben deze design keuze gemaakt omdat wij het goed bij het betreffende project vinden passen. Wij hebben net zoals op de officiele FDND site de achtergrond lichtpaars gemaakt, wij hebben er ook voor gekozen om de background van de profile cards donkerblauw te maken zodat het mooi past bij de achtergrond van de website. Hierbij hebben wij wel een licht blauwe border gegeven met een border radius voor een mooiere uitstraling. Wij hebben wel voor een andere font gekozen dan de font van de FDND site, dit hebben Wij hebben gedaan zodat het een wat moderenere en proffesionelere uitstraling kreeg. De kaartjes zijn op zowel mobiel, tablet, desktop identiek, het enige verschil zit in de layout van de visitekaartjes namelijk op mobiel staan de kaartjes onder elkaar en op tablet / desktop staat het netjes in een layout naast elkaar. Wij hebben ook gebruik gemaakt van animaties als je net op de website komt, dit vonden wij een creatieve, proffesionele maar niet hinderlijke toevoeging aan onze website. Als je op iemands profile card klikt krijg je een view transition tezien dat de foto van het betreffende visite kaartje naar het midden verplaatst en zich vergroot. Hieronder laten wij de website op 3 diverse devices zien zodat u een beeld krijgt bij de website.

### Mobile  

<img width="360" height="771" alt="Screenshot 2025-09-18 at 20 48 38" src="https://github.com/user-attachments/assets/0e75aa20-9226-4b96-bf3c-7993673f85c6" />

Zoals te zien zijn alle kaartjes op de mobiele versie netjes onder elkaar uitgelijnd, dit vonden wij de beste keuze voor mobiel voor een ovewrzichtelijk beeld.

### Tablet 

<img width="507" height="683" alt="Screenshot 2025-09-18 at 20 52 09" src="https://github.com/user-attachments/assets/113b5b19-791e-4449-a062-6ee899f26e2b" />

Zoals te zien is er op de tablet een nette layout te zien van de visitekaartjes, dit vonden wij een goede keuze omdat er anders erg veel witruimte vrij bleef.

### Desktop 

<img width="1497" height="858" alt="Screenshot 2025-09-18 at 20 53 05" src="https://github.com/user-attachments/assets/91e55bc2-322b-4705-81f4-a8b57c0812a4" />

Op desktop ziet het er vrijwel hetzelfde uit, de layout word namelijk automatisch aangepast naar de grootte van het device.

### Filmpjes van website in gebruik


https://github.com/user-attachments/assets/63eb49dc-55a0-407c-b65a-7ec3550f64f1

Zoals te zien is de navigatie makkelijk en werkt het goed.


https://github.com/user-attachments/assets/a9f75268-5cd9-429a-8465-713520f1f7a9

Zoals te zien geven de view-transitions een leuk proffesioneel effect, ook zodra er op een visitekaartje word geklikt komt het vlot zonder problemen in beeld







## Functionaliteiten uitleg




## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).
