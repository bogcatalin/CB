
## Identificare

Titlu: Aplicatie magazin online produse alimentare
Student: Bogdan Catalin Iulian
Grupa: 1119


## Introducere

Lansam serverul cu comanda: npm run dev

Deschidem aplicatia in browser la adresa locala [http://localhost:3000].
Stergerea elementelor afisate in aplicatie se face apasand butonul "DELETE". Noi inregistrari se pot adauga de la adresa [http://localhost:3000/insert].

Aplicația este construită folosind următoarele tehnologii și servicii:
•	Frontend: aplicația folosește Next.js - un framework React pentru construirea paginilor web dinamice, care facilitează server-side rendering și generarea de pagini statice.
•	Backend: aplicația folosește Express.js - un framework Node.js pentru construirea serverelor web. Acesta furnizează API-ul pentru comunicarea dintre frontend și baza de date MongoDB.
•	Baza de date: aplicația utilizează MongoDB - o bază de date NoSQL care stochează datele campaniilor de fundraising.
•	Deployment: aplicația este gazduită pe platforma Vercel - o platformă cloud care oferă servicii de hosting, scalabilitate și administrare pentru aplicații web.

Documentația va fi inclusă în fișierul README.md în cadrul repo-ului git [https://github.com/bogcatalin/CB].


## Descriere

Aplicația este construită într-un stil MVC (Model-View-Controller) pentru separarea responsabilităților și modularitatea codului.

In aplicatia noastra, avem un singur model, Record, care reprezinta un magazin online de produse alimentare. 
Modelul are urmatoarele campuri:
•	title: numele produsului
•	description: pretul si cantitatea aferente produsului listat

Fișierele MainPage.jsx și InsertPage.jsx sunt responsabile pentru interfața utilizatorului și interacțiunea cu utilizatorul. În ambele fișiere, comunicarea cu serverul este realizată prin apelarea API-urilor create în records.js.

Controller-ul este definit în folderul records și conține rutele API pentru accesarea datelor din baza de date. Acesta utilizează metodele din model pentru a efectua operațiile de CRUD (Create, Read, Update, Delete) pe date. Acesta folosește de asemenea Express.js pentru a defini rutele și a gestiona cererile de la client.
records.js contine urmatoarele metode:
•	getRecords: o metoda GET pentru a returna toate campaniile din baza de date
•	addRecord: o metoda POST pentru a adauga o noua campanie in baza de date
•	deleteRecord: o metoda DELETE pentru a sterge o campanie din baza de date


## Autentificare si securitate

Pentru securitate, aplicația implementează autentificarea în baza de date MongoDB. Aceasta se face prin intermediul variabilelor de mediu (process.env) pentru a ascunde cheile secrete și alte informații sensibile. Cheile secrete sunt setate în platforma Heroku, iar apoi sunt accesibile în aplicație prin intermediul variabilelor de mediu.


## Testare in Postman

Aplicația poate fi testată în Postman prin apelarea API-urilor create în records.js.


## View

View-ul este definit în folderul pages și conține componentele React pentru construirea interfeței utilizator. Componentele sunt construite folosind Tailwind CSS - o bibliotecă de clase CSS predefinite, care facilitează construirea de interfețe responsive și atractive.


## Referinte
Vercel. (2021). Vercel Documentation. Retrieved from https://vercel.com/docs
React. (2021). React Documentation. Retrieved from https://reactjs.org/docs/getting-started.html
Node.js. (2021). Node.js Documentation. Retrieved from https://nodejs.org/en/docs/
Express.js. (2021). Express.js Documentation. Retrieved from https://expressjs.com/
MongoDB. (2021). MongoDB Documentation. Retrieved from https://docs.mongodb.com/
Postman. (2021). Postman Documentation. Retrieved from https://learning.postman.com/docs/getting-started/introduction/
JWT. (2021). JWT.io Documentation. Retrieved from https://jwt.io/
OBS Studio. (2021). OBS Studio Documentation. Retrieved from https://obsproject.com/wiki/
Stack Overflow. (2021). Retrieved from https://stackoverflow.com/
GitHub. (2021). GitHub Documentation. Retrieved from https://docs.github.com/en


## Deployment si scalabilitate

Pentru a implementa si gazdui aplicatia noastra, am folosit Vercel, o platforma de deployment si hosting pentru aplicatii web.

 Am implementat aplicatia pe Vercel prin urmatorii pasi:
1.	Am creat un cont Vercel si am conectat aplicatia noastra GitHub repo cu Vercel.
2.	Am configurat variabilele de mediu pentru conexiunea cu baza de date MongoDB.
3.	Am selectat ramura (branch) potrivita si am confirmat deploymentul.

Aplicatia noastra este scalabila la nivel de baze de date MongoDB, deoarece poate fi configurata sa utilizeze un cluster MongoDB care poate fi scalat orizontal. In plus, Vercel ofera un nivel de scalabilitate pentru aplicatia noastra, permitandu-ne sa gestionam volumul de trafic si sa scalabil orizontal in functie de necesitatile aplicatiei.

Deployment-ul se afla la adresa [https://vercel.com/bogcatalin].


## Componenta de chat

Aplicatia contine si o componenta de chat [http://localhost:3000/chat] care ii permite utilizatorului sa adreseze intrebari.

Asistentul este configurat sa raspunda conform unui rol asociat (in cazul nostru Jon Snow din Game of Thrones) care poate fi modificat in functie de scopul propus.



