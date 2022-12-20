# 02-MySQL-task-Entity_Relationship-and-Relational_Model

************************************* Entity_Relationship **********************************************</br>
                                      Odnos Entiteta </br>

ENTITETI: film, zanr, glumac, reziser, festival </br>

ATRIBUTI:  </br>
ATRIBUTI za film:    id filma, naziv, trajanje </br>
ATRIBUTI za zanr:    id zanra, naziv zanra </br>
ATRIBUTI za glumca:  sifra, ime, prezime </br>
ATRIBUTI za reziser: sifra, ime, prezime </br>
ATRIBUTI ZA film:    id broj, naziv festivala, godina ucestovanja filma na festivalu, nagrada </br>

GLAGOLI: </br>
Odnos izmedju FILMA i ZANRA  je  < PRIPADA > </br>
Odnos izmedju GLUMCA i FILMA je < GLUMIO > </br>
Odnos izmedju REZISERA i FILMA je  < REZIRAO > </br>
Odnos izmedju FILMA i FESTIVALA je < UCESTVUJE > </br>

* Nakon zavrsetka sa ER dijagramom, rezultat prevodimo u relacioni dijagram</br>



************************************* Relational Model **********************************************</br>
  Gledamo nazive entiteta a to su zanr, glumac, reziser, festival 
* Kod relacionih modela uporedjujemo max broj kardinaliteta koji nam odredjjuju da li cemo imati  strani kljuc (foreign key) ili medju tabelu!

* FILM (1, 1) i ZANR (0, n) </br>
   FILM (1, 1) jedan film moze da ima max 1 zanr </br>
   ZANR (0, n) jedan zanrs moze da ima max n filmova to znaci da imamo odnos 1 : n </br>
   Kada imamo 1 : n, u onom entitetu koji ima max 1, pisemo strani kljuc na entitet n </br>
    
* FILM (1, 1) i REDITELJ (1, n)</br>
   Film moze da ima max 1 reditelja </br>
   Reditelj moze da ima max vise n filmova </br>
   Kada imamo 1 : n, u onom entitetu koji ima max 1, pisemo strani kljuc na entitet n </br>
   
* FILM (0, n) i GLUMAC (1, n) 
  FILM  u jednom filmu moze da glumi max n broj glumaca
  GLUMAC moze da glumi max n broj filmova
  Ovde immamo vezu n : n odnosno vise na vise. U tom slucaju pravimo medju tabelu.
  
* FILM (0, n) i FESTIVAL (1, n)
  Jedan film moze da ucestvuje na vise feistivala a festival moze da ima vise filmova, i iz ovog dobijamo vezu n : n (vise na vise)
  To znaci da se kreira nova tabela film_festival


![1 isecen](https://user-images.githubusercontent.com/56784702/208711222-bdce8823-c9be-45e2-8e5f-535e9dfd34e4.png)
![2](https://user-images.githubusercontent.com/56784702/208711243-cb39c901-50c5-4b11-83c3-cdee327b55c9.png)
![3](https://user-images.githubusercontent.com/56784702/208711246-9f28db43-1e96-4a8d-8b2b-c517e7babc22.png)
![4](https://user-images.githubusercontent.com/56784702/208711252-0bbc4a21-6899-43f9-a36d-40ac5c72a620.png)





