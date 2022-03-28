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

PREGLED LITERATURE – REACT

React (poznat i kao React.js ili ReactJS) je JavaScript biblioteka otvorenog koda koja obezbeđuje pregled podataka zapisanih preko HTML-a. React obezbeđuje programeru model u kome potkomponente ne mogu direktno da utiču na spoljašnje komponente, efikasno ažuriranje HTML dokumenta pri promeni podataka i jasno razdvajanje komponenti na današnjim jednostraničnim aplikacijama.  
Stvorio ga je Jordan Valke, programer u kompaniji Facebook. Od svog debija 2011. godine, React je postao jedan od najpopularnijih front-end framework-a za izradu veb aplikacija sa ogromnom zajednicom pojedinačnih programera i kompanija. Jednostavno rečeno, ReactJS se može koristiti kao baza projekta tokom razvojnog ciklusa jednostraničnih ili progresivnih veb aplikacija. 
U većini slučajeva, glavna uloga framework-a jeste prenošenje podataka DOM-u (ili modelu objekta dokumenta), i kao takve, aplikacije koje se zasnivaju na React-u često zahtevaju dodatne biblioteke za održavanje stanja i rutiranje. Zbog ovakvih zadataka često se u procesu development-a uključuju i Redux (za održavanje stanja) i React Router (za ruting). 
React upravlja komandnom linijom za veb aplikacije, ali se takođe može koristiti za kreiranje UI komponenti za višekratnu upotrebu.  React omogućava programerima da razviju velike veb aplikacije koje omogućavaju promenu podataka bez potrebe za ponovnim osvežavanjem same stranice.  
U ovoj aplikaciji upravo su i korišćene sve prednosti koje React.js nudi, zahvaljujući React-ovim gotovim bibliotekama poput react-icons. U React-u vidimo bezbroj mogućnosti za pravljenje zanimljivih veb stranica ali i aplikacija visokog kvaliteta. 

RAZVOJ APLIKACIJE

Tema ovog domaćeg zadatka bila je izrada React aplikacije namenjena studentima FON-a, fokusirana  na korišćenje React hooks-a, useEffect-a, useState-a kao i useRef-a. U samoj aplikaciji moguće je izmeniti, dodati ili ukloniti belešku.   


LINK DO GIT REPOZITORIJUMA PROJEKTA:
https://github.com/nnastasija/React-Domaci3.git
