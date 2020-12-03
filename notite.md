### 2.5.3 Evidentierea variabilelor in functie de calitatea lor
Graficul arata relatia dintre variabile, calitatea reprezentarii variabilelor si corelatia dintre variabile si dimensiuni:
  - Distanta dintre puncte si origine masoara calitatea variabilei pe harta factorilor.
  - Punctele variabile care sunt departe de origine sunt bine reprezentate pe harta factorilor.

### 2.5.3 Evidentierea variabilelor in functie de contributia lor la dimensiuni
Linia punctata rosie din graficul indica valoarea medie asteptata, in cazul in care contributiile au fost uniforme.

---- next slide

Variabile cantitative care contribuie cel mai mult pot fi evidentiate pe graficul scatter folosind argumentul col.var = “contrib”.


## 2.5.3 Rezultatul indivizilor
Din grafic observam ca categoriile variabilelor calitative suplimentare sunt prezentate in negru. Daca nu dorim sa le aratam in grafic, folosim invisible = “quali.var”.

Persoanele cu profiluri similare sunt aproape una de cealalta pe harta factorilor. Prima axa se opune in principal vinului 1DAM si vinurilor 1VAU si 2ING. Prima dimensiune reprezinta armonia si intensitatea vinurilor. Astfel, vinul 1DAM (coordonate pozitive) a fost evaluat ca fiind cel mai „intens” si „armonios” contrar vinurilor 1VAU si 2ING (coordonate negative) care sunt cel mai putin „intens” si „armonios”.

### 2.5.3 Corelarea indivizilor
Efectul este asemanator cu cel de la famd, punctele reprezinta grupuri de variabile in loc de variabile

De exemplu, daca dorim sa corelam vinurile in functie de variabila calitativa suplimentara „Label”, folosim urmatoarea instructiune:

Daca dorim sa corelam indivizi utilizand mai multe variabile categorice in acelasi timp, utilizam functia fviz_ellipses() astfel:


### 2.5.4 Indivizil partiali
Indivizi partiali = Rezultatele pentru indivizii obtinuti din analiza efectuata pe un singur grup

Pentru a trasa punctele partiale ale tuturor indivizilor, folosim urmatoarea instructiune:

Daca vrem sa vizualizam puncte partiale pentru vinurile de interes, ss spunem c(“1DAM”, “1VAU”, “2ING”).

Din punct de vedere al grupului de mirosuri, 2ING a fost mai „intens” si „armonios” decat 1VAU, dar din punct de vedere al grupului gustativ, 1VAU a fost mai „intens” si „armonios” decat 2ING.


### 3.3 Calculul variabile continue
Incepem prin a calcula din nou analiza componentelor principale (PCA). Argumentul ncp = 3 este utilizat In functia PCA() pentru a pastra doar primele trei componente principale. Apoi, HCPC se aplica pe rezultatul PCA.

Dendrograma sugereaza o solutie cu 4 clustere.

-----

Este posibil sa vizualizam indivizii pe harta componenta principala si sa coloram indivizii in functie de grupul de care apartin. Functia fviz_cluster() [din factoextra] poate fi utilizata pentru a vizualiza clustere individuale.


-----

De asemenea, putem desena un grafic tridimensional care combina clusterizarea ierarhica si harta factoriala // utilizand graficul functiei de baza R ():


### 3.4 Calculul variabile categorice
Pentru variabilele categorice, calculam CA sau MCA si apoi aplicati functia HCPC() pe rezultatele descrise mai sus.

Aici, vom folosi datele despre ceai [in FactoMineR] ca set de date demo: randurile reprezinta indivizii, iar coloanele reprezinta variabile categorice.

------

Apoi, aplicam clustering ierarhic pe rezultatele MCA:

------

Afisam dendograma

------

Harta factorilor individuali

