# React-Domaci3

                                                                 









PREDMET INTERNET TEHNOLOGIJE
Domaći zadatak 3 – React.js


 



Nastasija Nedeljković 481/17
                                                      
Beograd, 2022. godine                              
UVOD, IDEJA I DIZAJN APLIKACIJE

Tema ovog projektnog zadatka je izrada aplikacije korišćenjem React.js-a. U pitanju je sajt sa aplikacijom koja ima za cilj da studentima pomogne sa njihovim regularnim obavezama i zadacima. Praveći beleške studenti će lakše da obave sve svoje aktivnosti i obaveze u toku jednog radnog dana, sprečavajući zaboravljanje nekih bitnih rokova ili zadataka. Klikom na ikonicu plus student na aplikaciji za početak može da odabere boju svoje beleške, nakon čega se ona pojavljuje na ekranu. Unutar samog input polja može otkucati i postaviti svoju belešku.  Klikom na kontejner ikonicu student može da obriše svoju belešku ukoliko je završio sa njom, ili se predomislio. Ukoliko je došlo do eventualne greške pri kucanju postoji mogućnost i da prepravi napisanu stvar, to je moguće jednostavnom izmenom bez ograničavanja.
Koncept sajta je malo drugačiji nego inače. U ovom slučaju se sa strane nalazi Navigation bar tj. Sidebar sa tri stranice (komponente) različitog sadržaja: Početna, Beleške i FAQ, a za koje su korišćeni principi rutiranja. Korišćenjem react router-a možemo da idemo na ostale strane.

Početna

Na početnoj stranici nalazi se klasična HTML strana sa tekstom, stilizovana preko CSS-a. Cilj je postići efektan i moderan izgled na samom početku, koji bi privukao pažnju studenata.

Beleške

Na kartici Beleške nalazi se responzivna Notes aplikacija, gde student ima mogućnost da odabere boju beleške, da napiše i okači beleške ili izbriše postojeće. Svaka beleška ima svoj datum i vrema u okviru sebe same. Aplikacija je napravljena koriščenjem JavaScript biblioteke React.js-a. U potpunosti je stilizovana korišćenjem CSS-a.

FAQ

Na kartici FAQ nalazi se Accordion komponenta, koja treba da predstavi izdvojena, neka od najčešće postavljanih pitanja studenata (Frequently Asked Questions – Često postavljana pitanja). Napravljena je korišćenjem React hooks i styled components. Po pravilu ovakav vid komponente bi najviše bio koristan u situacijama da želimo da prikažemo ili sakrijemo veći broj podataka, u ovom primeru prikazana su samo neka tri izdvojena pitanja.  
FINALNI IZGLED APLIKACIJE


 
1 Početna strana aplikacije

 
2 Početna strana komponente Beleške

 
3 Primer postavljenih beleški


 
4 FAQ komponenta



PREGLED LITERATURE – REACT

React (poznat i kao React.js ili ReactJS) je JavaScript biblioteka otvorenog koda koja obezbeđuje pregled podataka zapisanih preko HTML-a. React obezbeđuje programeru model u kome potkomponente ne mogu direktno da utiču na spoljašnje komponente, efikasno ažuriranje HTML dokumenta pri promeni podataka i jasno razdvajanje komponenti na današnjim jednostraničnim aplikacijama.  
Stvorio ga je Jordan Valke, programer u kompaniji Facebook. Od svog debija 2011. godine, React je postao jedan od najpopularnijih front-end framework-a za izradu veb aplikacija sa ogromnom zajednicom pojedinačnih programera i kompanija. Jednostavno rečeno, ReactJS se može koristiti kao baza projekta tokom razvojnog ciklusa jednostraničnih ili progresivnih veb aplikacija. 
U većini slučajeva, glavna uloga framework-a jeste prenošenje podataka DOM-u (ili modelu objekta dokumenta), i kao takve, aplikacije koje se zasnivaju na React-u često zahtevaju dodatne biblioteke za održavanje stanja i rutiranje. Zbog ovakvih zadataka često se u procesu development-a uključuju i Redux (za održavanje stanja) i React Router (za ruting). 
React upravlja komandnom linijom za veb aplikacije, ali se takođe može koristiti za kreiranje UI komponenti za višekratnu upotrebu.  React omogućava programerima da razviju velike veb aplikacije koje omogućavaju promenu podataka bez potrebe za ponovnim osvežavanjem same stranice.  
U ovoj aplikaciji upravo su i korišćene sve prednosti koje React.js nudi, zahvaljujući React-ovim gotovim bibliotekama poput react-icons. U React-u vidimo bezbroj mogućnosti za pravljenje zanimljivih veb stranica ali i aplikacija visokog kvaliteta. 

RAZVOJ APLIKACIJE

Tema ovog domaćeg zadatka bila je izrada React aplikacije namenjena studentima FON-a, fokusirana  na korišćenje React hooks-a, useEffect-a, useState-a kao i useRef-a. U samoj aplikaciji moguće je izmeniti, dodati ili ukloniti belešku.   
Jedan od načina za kreiranje react aplikacije je preko Node Package Manager-a. Instalaciju je moguće skinuti preko linka: https://nodejs.org/en/download/.  
Pre samog početka potrebno je da kreirati react aplikaciju. Otvoriti command prompt ili bilo koji drugi terminal i uneti sledeću komandu: npx create-react-app react-domaci. Nakon što se instaliranje završi u command promptu dobija se nešto ovako:

 
5 pravljenje React aplikacije npx create-react-app naziv aplikacije
Takođe, treba instalirati node modules preko komande: npm install ili npm i.
Nakon što smo instalirali sve što je bilo potrebno aplikaciju pokrećemo na serveru (localhost:3000) preko komande u terminalu VSC-a i to: npm start.

 

6 npm install
 
7 npm start
Još je neophodno i otkucati i sledeću komandu u terminalu: install styled-components react-icons react-router-dom.
 
8 instalacija styled-components react-icons react-router-dom

 
9 instalirani u package.json

Pravljenjem react aplikacije na ovaj način generički se dobija i package.json, tekstualna datoteka koja sadrži sve informacije o metapodacima. Svaki Node JavaScript Package treba da sadrži ovu datoteku u osnovnom direktorijumu. 

 
10 Download-ovanje ES7 ekstenzije 
Skinuti ekstenziju ES7 preko jednostavne opcije Extensions u Visual Studio Code-u (radi lakšeg rada). Otvoriti karticu od koje počinjemo tako što ćemo otkucati rfce, zatim enter i automatski će nam izbaciti linije koda, koje se koriste kao jednostavna šema za početak rada.   
Prvo se kreira Navbar i to na sledeći način, pravimo folder components koji sadrži sledeće fajlove: Sidebar.js, SidebarData.js i SubMenu.js.
Za ovaj deo koristićemo gotovu biblioteku react-icons sa bezbroj različitih ikonica, koja će nam dosta olakšati deo dizajna. Neophodno je import-ovati iste na vrh strane, kao na slici:

 
11 SidebarData.js

Export-ujemo konstantu SidebarData u kojoj treba definisati naše tri komponente. Svaka ima svoj naslov (title) koji će zaista i biti prikazan na Sidebar-u, putanju (path), linkovane react ikonice uz njihove nazive iz biblioteke (icon).

Sledeća na redu je komponenta Sidebar.js, gde je takođe neophodno importovati na sam vrh strane react ikonice, React, styled iz styled-components, {Link} iz react-router-dom-a (kombinacija CSS-a i JavaScript-a gde možemo da nest-ujemo komponente) kao sa slike:
 
12 Sidebar.js

Kreiramo konstantu Nav gde ćemo direktno odraditi i deo za stilizaciju kao na snimku ekrana gore. Zatim kreiramo i konstantu Sidebar, unutar koje u okviru jednog div-a imamo <Nav> tag i definišemo ikonice putem taga <NavIcon> koje iako je link, za sad ne vodi ni na kakvu stranicu. 
 
13 SidebarData.js 2.0
Takođe, treba stilizovati i NavIcon ikonice u okviru Sidebar.js komponente. 
 
14 stilizovana NavIcon
Na vrh App.js fajla treba importovati i određene stavke na sledeći način:
import { BrowserRouter as Router, Switch, Route } from 'react-router-dom';
15 Početak App.js stranice
Na slici 13 takođe možemo videti i definisanu konstantu Sidebar gde koristimo useState. Kod funkcije definišemo set. pa naziv koji smo napisali na početku. U kodu !sidebar deo treba da update-uje vrednost na obrnuto od početne false.
 
16 Sidebar.js
Ono što je zanimljivo ali ujedno i olakšavajuća okolnost jeste da direktno u okviru styles možemo da prenosimo vrednosti. Na vrh strane obavezno postavljamo odgovarajući import, u ovom slučaju import {SidebarData}. Dok na strani SubMenu.js importujemo sledeće:
 
17 SubMenu.js
 
18 SubMenu.js 2.0
U delu koda {item.path} treba da definišemo našu datu što je path u okviru linka <SideBarLink>. Sve je wrap-ovano jedni div-om. Kako nam se na vrhu svake strane nalaze obavezni import-ovi, na dnu svih tih strana mora se naći i odgovarajući export. 
Kod strane Sidebar.js na 63 i 64. liniji koda definišemo item i index varijable, kako bi preneli ključ i vrednost tih promenljivih.
Preostalo stilizovanje se završava u delu konstante SideBarLink.
Dakle, fokus kod pravljenja ovog sidebar-a bio je na komponentama, data fajlovima i naravno samim stranama i rutama.
 
19 Sidebar.js
Sledeći korak je kreiranje Notes aplikacije i to na sledeći način, pravimo folder komponente koji sadrži sledeće podfoldere: Note, NoteContainer,Sidebar i assets sa ikonicama uz odgovarajuće fajlove:

 
20 komponente za beleške

Neophodno je import-ovati na vrh strane sve bitno za stranu, kako bi zaista radila. Definišemo funkciju Note u okviru koje treba da imamo formatirane mesece kao datum koji se pojavljuje na samoj beleški.

 
21 Note.js formatiranje datuma
Ovde su definisane i neke od funkcija za postavljanje osobina za datum i vreme getMinutes, getHours, getDate i getMonth, postavljene kao na slici. 
Sa druge strane imamo i metodu debounce kojom možemo smanjiti ukupan broj pozivanja funkcije. Ova metoda omogućava upravljanje događajima koji se događaju jedan za drugim. Ako je vremenski razmak između događaja manji od nekog zadatog vremena, onaj prvi događaj se neće izvesti. Kada se dogodi neki događaj nakon zadatog vremenskog intervala, funkcija se izvodi. Drugim rečima, debouncing određuje da se funkcija ne može ponoviti dok nije prošao zadati vremenski period. 
Funkcija debounce() sadrži dva argument – func i timer. Funkcija debounce() prima funkciju za koju želi da napravi debounce (argument func). Drugi argument predstavlja vremenski interval (argument timer). Pozivom debounce() funkcije pokreće se odbrojavanje (setTimeout()). Ako odbrojavanje dosegne zadato vreme (timer), debounce() funkcija vraća željenu funkciju pozvanu kroz argument.
 
22 Note.js 2.0 debounce( )
 
23 NoteContainer.js
 
24 Sidebar.js
Prethodno definisane stranice uređujemo u adekvatnim i zasebnim CSS fajlovima kao na slikama ekrana.
 
26 NoteContainer.css

 
25 Note.css

 
27 Sidebar.css
 
28 FAQ,js
 
29 FAQ.js import i stilizacija
 
30 Data.js
Za deo FAQ komponente najjednostavnija strana je Data.js kod koje se kreira konstanta Data koja kao vrednost treba da prenese objekat, pitanje i odgovor. Ta forma koda se kopira tri puta zbog tri pitanja tj. koliko god puta je potrebno. 
Na vrh strane Faq.js importujemo sve kao sa slike 29. Definišemo konstantu AccordionSection i wrap-ujemo sve <IconContext.Provider> tagom, unutar kog imamo i tagove za sam AccordionSection i naš Container. Definišu se item i index kako bismo preneli vrednost za ključ.
Stil svega potrebnog takođe videti sa snimaka ekrana.
Na liniji 69 koda takođe strane Faq.js možemo videti opet upotrebu usedState hook-a. Unutar konstante u delu [clicked, setClicked] prva vrednost predstalja neki prvenstveni state, dok druga vrednost treba da predstavlja funkciju koju obavezno započinjeno sa set. koja treba da ga menja.
Takođe, ovde se pojavljuje i konstanta toggle, gde gledamo na šta treba da se klikne. Ako je clicked == index, zapravo definišemo da ako je Accordion već otvoren nema potrebe da ga opet otvaramo. U suprotnom sama vrednost clicked jeste upravo taj index tj. clicked (index). 
Za kraj sam “padajući meni” ove accordion aplikacije definišemo preko konstante Dropdown. 

LINK DO GIT REPOZITORIJUMA PROJEKTA:
https://github.com/nnastasija/React-Domaci3.git
