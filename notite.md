
## Evidentierea variabilelor
### 2.2.1 Evidentierea variabilelor in functie de calitatea lor

Graficul arata relatia dintre variabile, calitatea reprezentarii variabilelor si corelatia dintre variabile si dimensiuni:

  - Variabilele corelate pozitive sunt grupate impreuna, iar cele negative sunt pozitionate in cadrane opuse.

  - Distanta dintre punctele variabile si origine masoara calitatea variabilei pe harta factorilor. Punctele variabile care sunt departe de origine sunt bine reprezentate pe harta factorilor.

  - Cele mai corelate variabile cu o dimensiune sunt cele mai apropiate de dimensiunea respectiva.

#### Cerc MFA

De exemplu, prima dimensiune reprezinta sentimentele pozitive despre vinuri: „intensitate” si „armonie”. Cele mai corelate variabile cu cea de-a doua dimensiune sunt: i) Condimentul inainte de scuturare si intensitatea mirosului inainte de agitare pentru grupul de mirosuri; ii) Intensitatea condimentelor, a plantelor si a mirosului pentru miros dupa grupul de agitare si iii) Amaraciunea pentru grupul gustativ. Aceasta dimensiune reprezinta in esenta „picantul” si caracteristica vegetala datorata olfactiei.


## Evidentierea variabilelor
### 2.2.2 Evidentierea variabilelor in functie de contributia lor la dimensiuni

Linia punctata rosie din graficul indica valoarea medie asteptata, daca contributiile au fost uniforme
Variabilele cu valoarea mai mare contribuie cel mai mult la definirea dimensiunilor.
Variabilele care contribuie cel mai mult la Dim.1 si Dim.2 sunt cele mai importante in explicarea variabilitatii in setul de date.

---- next slide

Cele mai contribuibile variabile cantitative pot fi evidentiate pe graficul scatter folosind argumentul col.var = “contrib”.
Aceasta produce un gradient de culori, care poate fi personalizat folosind argumentul gradient.cols.


## 2.3 Rezultatul indivizilor
### 2.3.1 Graficul indivizilor

In graficul de mai sus, categoriile variabile calitative suplimentare sunt prezentate in negru. Env1, Env2, Env3 sunt categoriile de sol. Saumur, Bourgueuil si Chinon sunt categoriile etichetei de vin. Daca nu doriti sa le aratati in complot, utilizati argumentul invizibil = “quali.var”.

Persoanele cu profiluri similare sunt aproape una de cealalta pe harta factorilor. Prima axa se opune in principal vinului 1DAM si vinurilor 1VAU si 2ING. Dupa cum sa descris in sectiunea anterioara, prima dimensiune reprezinta armonia si intensitatea vinurilor. Astfel, vinul 1DAM (coordonate pozitive) a fost evaluat ca fiind cel mai „intens” si „armonios” contrar vinurilor 1VAU si 2ING (coordonate negative) care sunt cel mai putin „intens” si „armonios”. A doua axa este in esenta asociata cu cele doua vinuri T1 si T2 caracterizate printr-o valoare puternica a variabilelor Spice.before.shaking si in graficul de mai sus, categoriile variabile calitative suplimentare sunt prezentate in negru. Env1, Env2, Env3 sunt categoriile de sol. Saumur, Bourgueuil si Chinon sunt categoriile etichetei de vin. Daca nu doriti sa le aratati in complot, utilizati argumentul invizibil = “quali.var”. Odor.intensity.before.shaking.

Majoritatea categoriilor variabile calitative suplimentare sunt apropiate de originea hartii. Acest rezultat indica faptul ca categoriile in cauza nu sunt legate de prima axa („intensitatea” si „armonia” vinului) sau de a doua axa (vinul T1 si T2).

Categoria Env4 are coordonate mari pe a doua axa legata de T1 si T2.

Categoria „Referinta” este cunoscuta pentru legatura cu un sol vitivinicol excelent. Asa cum era de asteptat, analiza noastra demonstreaza ca categoria „Referinta” are coordonate inalte pe prima axa, care este corelata pozitiv cu „intensitatea” si „armonia” vinurilor.


### 2.3.1 Corelarea indivizilor

Este posibil sa colorem indivizii folosind oricare dintre variabilele calitative din tabelul de date initial. Pentru a face acest lucru, argumentul habillage este utilizat in functia fviz_mfa_ind(). De exemplu, daca dorim sa coleram vinurile in functie de variabila calitativa suplimentara „Label”, folosim urmatoarea instructiune:

Daca dorim sa coloram indivizi utilizand mai multe variabile categorice in acelasi timp, utilizam functia fviz_ellipses() astfel:


### 2.3.2 Graficul indivizilor partiali

Rezultatele pentru indivizii obtinuti din analiza efectuata cu un singur grup sunt denumiti indivizi partiali. Cu alte cuvinte, un individ considerat din punctul de vedere al unui singur grup se numeste individ partial.

In graficul implicit fviz_mfa_ind(), pentru un individ dat, punctul corespunde cu individul mediu sau cu centrul de greutate al punctelor partiale ale individului. Adica, individul vazut de toate grupurile de variabile.

Pentru un individ dat, exista atat de multe puncte partiale cat grupuri de variabile.

Graficul indivizilor partiali reprezinta fiecare vin vizualizat de fiecare grup si baricentrul sau. Pentru a trasa punctele partiale ale tuturor persoanelor, folosim urmatoarea instructiune:

Daca vrem sa vizualizam puncte partiale pentru vinurile de interes, ss spunem c(“1DAM”, “1VAU”, “2ING”).

Vinul 1DAM a fost descris in sectiunea anterioara ca fiind deosebit de „intens” si „armonios”, in special de grupul de mirosuri: are o coordonata ridicata pe prima axa din punct de vedere al grupului de variabile de miros comparativ cu punctul de vedere asupra celorlalte grupuri.

Din punct de vedere al grupului de mirosuri, 2ING a fost mai „intens” si „armonios” decat 1VAU, dar din punct de vedere al grupului gustativ, 1VAU a fost mai „intens” si „armonios” decat 2ING.


### 2.3.3 Calculul variabile continue

Incepem prin a calcula din nou analiza componentelor principale (PCA). Argumentul ncp = 3 este utilizat In functia PCA() pentru a pastra doar primele trei componente principale. Apoi, HCPC se aplica pe rezultatul PCA.

Dendrograma sugereaza o solutie cu 4 clustere.

-----

Este posibil sa vizualizam indivizii pe harta componenta principala si sa coloram indivizii in functie de grupul de care apartin. Functia fviz_cluster() [din factoextra] poate fi utilizata pentru a vizualiza clustere individuale.


-----

De asemenea, putem desena un grafic tridimensional care combina clusterizarea ierarhica si harta factoriala // utilizand graficul functiei de baza R ():


### 2.3.4 Calculul variabile categorice

Pentru variabilele categorice, calculam CA sau MCA si apoi aplicati functia HCPC() pe rezultatele descrise mai sus.

Aici, vom folosi datele despre ceai [in FactoMineR] ca set de date demo: randurile reprezinta indivizii, iar coloanele reprezinta variabile categorice.

Incepem, efectuand un MCA pe indivizi. Pastram primele 20 de axe ale MCA, care retin 87% din informatii.

------

Apoi, aplicam clustering ierarhic pe rezultatele MCA:

------

Afisam dendograma

------

Harta factorilor individuali

