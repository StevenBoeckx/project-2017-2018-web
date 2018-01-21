# Angular overzicht handleiding
***
Instructies komen uit ppt van **Wim Dams**. Ik heb ze kort gebundeld moest ik in de toekomst een nieuw project maken dat ik niet alle ppt's moet doorlezen.

Op het einde bevind zicht specifieke informatie over mijn project.
### Alles installeren om project te genereren
1. installeren van NodeJS [https://nodejs.org/](https://nodejs.org/)
2. (enkel voor windows) installeren van [CMder](http://cmder.net/)
3. Angular CLI installeren 
   ```sh
   npm install -g @angular/cli
   ```
  ***
### Eerste project genereren
 ```sh
 cd [NaarUwWerkMap]
ng new angular-demo
cd angular-demo
ng serve
 ```
 ***
 ### Nieuw component aanmaken
 ```sh
 ng g c [naamvancomponent]
 ```
 ***
 ### Installeren van Bootstrap
 ```sh
 npm install bootstrap@3 jquery --save
 ```
 Volgende regels moeten toegevoegd worden in .angular-cli.json
```javascript
Styles: "../node_modules/bootstrap/dist/css/bootstrap.min.css",
Scripts: "../node_modules/jquery/dist/jquery.min.js",
Scripts: "../node_modules/bootstrap/dist/js/bootstrap.min.js", 
```
 ***
 ### Specifieke elementen van mijn project
 ##### Nuttige links
 Elke link geeft informatie hoe je de module/library moet installeren en hoe te gebruiken.
+ Informatie voor **charts** die ik gebruikt heb. [https://valor-software.com/ng2-charts/](https://valor-software.com/ng2-charts/).
+ Informatie voor de **drag and drop** die ik gebruikt heb. -98 6[https://www.npmjs.com/package/ng2-drag-drop](https://www.npmjs.com/package/ng2-drag-drop)
 
 
 
 
 
 


