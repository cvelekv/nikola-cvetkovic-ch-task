This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).
### Zadatak

Potrebno je napraviti naslovnu stranu Hacker Newsa. Screenshot dizajna je u prilogu.

![alt text](<https://cms.jotform.com/uploads/image_upload/image_upload/global/86342_hackernews%20(1).png>)

Aplikacija treba:

Da bude napisana u Reactu
Da se povezuje sa Hacker News APIjem
Da prikazuje listu od 20 najpopularnijih postova na Hacker Newsu
Da prikaže narednih 20 postova kada se klikne na "more" link na dnu liste
Da prilikom prelaska na drugu stranu prikazuje i "prev" link koji služi za vraćanje
Da automatski osvežava listu postova na svakih 30 sekundi
Da osveži listu pritiskom na refresh dugme
Da radi lepo na Chromeu u rezoluciji 1024px i šire

Bonus:

Responsive design, da se aplikacija lepo prikazuje i na mobilnim telefonima
Da linkovi ka komentarima otvaraju komentare na Hacker News sajtu
Da radi fino na svim browserima (zanemari IE)
Svi dodatni predlozi koje nismo napomenuli ovde

Na šta ćemo najviše obratiti pažnju:

Da li aplikacija radi
Struktura aplikacije
Komponente
Na koji način se koriste React lifecycle events
Organizacija koda

Na šta ne treba gubiti vreme:

Webpack config u ovom slučaju uopšte nije bitan, nema potrebe praviti savršen setup za aplikaciju
Redux, možeš ga koristiti ako želiš, ali i ako ga izostaviš nije od ključnog značaja za test

### Starting the application
- Make sure that you're in root folder,
- Do npm install so all dependencies are installed,
- Run: npm start

### Solution

- Solution is created by using React and it was done in 11h +-.
- It is divided in several components from which App is state component and rest that are functional components (controlled)
  since all data came from App component (in this way we ensured React state to be single source of truth).
- All requiremenets are covered, Hacker news API is called and data is retrieved for top stories, 20 per page.
- You can move back and forth and view, again, 20 per page.
- Page is refreshed automatically every 30s,
- You can refresh manually with refresh button on the upper right corner.
- You can open comments for each story,
- It is tested in Chrome, FireFox and Safari and it's working as intended.
- Page is mobile responsive, tested on iPhones 6, 7, 8 and 6+, 7+, 8+, Galaxy s5.
- For page responsivness and design in general, Bootstrap library was used,
  for some special tweaking, when it comes to responsivness, CSS media queries were used.
- Notifications were implemented (snack bar component) for showing information related to data or errors.

Sources used:

-https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects 
-https://getbootstrap.com/docs/4.0/getting-started/introduction/ 
-https://hackernews.api-docs.io/v0/live-data/new-and-top-stories 
-https://medium.com/@farid12ansari7/make-a-snackbar-or-pop-up-notification-for-a-react-web-app-fd246dd1b9f0 
-https://codeburst.io/on-connecting-my-app-to-the-hackernews-firebase-api-e7b9e1ccec29

What can be improved in application

-Redux could be used for controlling state in app.
-Tests should be written,
-Add some new feature like searching for certain post, or user.
