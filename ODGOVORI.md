ZADATAK 1
-U datoteku ODGOVORI.md napisati što znače statusi green, yellow i red (kratko objašnjenje za svaki)
Green nam govori da sve radi kako treba, te da su svi podaci dostupni, yellow  nam govori da sustav radi i podaci su dostupni, ali nema sigurnosnih kopija, dok red označava da nešto ne radi kako treba i da neki podaci nisu dostupni ili govori da postoji greška u sustavu.


ZAFATAK 2
-zašto je naslov tipa text
-zašto postoji dodatno polje naslov.keyword
-zašto su autor i zanr tipa keyword
-zašto se opis ne bi trebao spremati kao keyword

-Naslov je tipa text jer želimo pretraživati po riječima, a ne po cijelom tekstu
-naslov.keyword postoji da mozemo točno pretraživati i sortirati
-autor i zanr su keyword jer se koriste za točno filtriranje 
-Opis nije keyword jer želimo da se može pretraživati po dijelovima teksta, a ne samo točno kao kod zanr-a i autor-a

ZADATAK 3
-U ODGOVORI.md objasniti zašto pretraga 'cuprija' pronalazi dokument 'Na Drini ćuprija'
-Pogledati polje _score u rezultatu i objasniti što označava i zašto se razlikuje među dokumentima

-Pretraga "cuprija" pronalazi "ćuprija" jer analyzer uklanja slova kao što su: č, ć, š, ž, te đ
-Polje _score pokazuje koliko neki rezultat odgovara onome što smo tražili, a među dokumentima se razlikuje zato što neki dokumenti imaju više tih riječi ili su te riječi važnije u tekstu pa ih Elasticsearch smatra boljim rezultatom


ZADATAK 5
-U ODGOVORI.md zapisati listu tokena koje Elasticsearch generira
-Objasniti što rade filtri lowercase i asciifolding i u čemu je razlika
-Oobjasniti zašto je analyzer ključan za full-text search i što bi se dogodilo da ga ne koristimo

-tokeni su: na, drini, cuprija
-lowercase pretvara sva slova u mala, asciifolding uklanja kvačice (č, ć, š, ž)
-analyzer je bitan jer omogućava da pretraga radi i kad ne upišemo točno isti tekst, a kada ne bismo koristili analyzera bi pretraga bila puno teža i složenija

ZAVRŠNI ZADATAK
-U ODGOVORI.md kratko objašnjenje (5–10 rečenica) kada Elasticsearch ima prednost nad SQL upitom tipa LIKE '%tekst%' (razmislite o brzini, jezičnoj analizi, relevantnosti rezultata, skalabilnosti)

Elasticsearch je bolji od SQL LIKE pretrage jer je praktičniji i može puno brže pretraživati tekst pomoću posebnog indeksa. Također omogućuje pretragu bez obzira na to jesu li slova velika ili mala i ima li ili nema kvačica. Elasticsearch daje i točnije rezultate jer ih rangira po važnosti, pa prvo vidimo ono što nam je najrelevantnije. SQL LIKE je sporiji i traži da se tekst točno podudara, dok je Elasticsearch fleksibilniji i pametniji za rad s tekstom. Također je puno bolji kada radimo s velikom količinom podataka jer brz ilakši je za korištenje kada radimo pretrage nad tekstom.