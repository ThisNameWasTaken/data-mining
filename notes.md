# Notes

## 2.3 Definirea clusterelor

Variabilele “place of purchase” si “format” caracterizeaza cel mai bine impartirea in 3 clustere. 
Fiecarea din clustere este caracterizat de o categorie a variabilei “place of purchase” si de o categorie a variabilei “format”.

Cluster 1 -> cei care cumpara ceai din supermarket la pliculete
(Cla/Mod) 85.9% dintre persoanele care cumpara ceai din supermarketuri se afla în grupul 1
(Mod/Cla) 93.7% dintre persoanele din grupul 1 isi cumpara ceaiul din supermarketuri

Clusterul 2 -> cei care cumpara ceai la in magazine specializate

Clusterul 3 -> cei care cumpara si din supermarket si din magazine specializate, la plic si la vrac

## 3 Impartirea variabilelor cantitative pe clase

### Impartirea variabilelor cantitative pe clase

(Nu stiam sa facem asta in urma proiectului de la curs)
<br/>
<br/>
Variabila “age” pentru datele despre ceai a fost notata,in chestionar, ca fiind variabila cantitativa.
Pentru a evidentia relatiile neliniare dintre variabila age si celelalte date din chestionar, aceasta trebuie recodificata ca variabila categorica.
O strategie este de a construi clase asemanatoare ("likely classes"). caz in care alegem un numar de clase, in general intre patru si sapte:

### Impartirea variabilelor cantitative pe clase (continuare)

O alta strategie este de a alege numarul de clase si limitele acestora din date. De exemplu, putem folosi o histograma reprezentand distributia variabilei astfel incat sa definim nivelurile de diviziune:

----

### Impartirea variabilelor cantitative pe clase (continuare) - Hierarhical Clustering
**dupa ce am citit de pe slide**
<br/>
Codul acesta construieste arborele ierarhic si consolideaza rezultatele folosind metoda K-mediilor (metoda K-mediilor converge foarte repede atunci cand este implementata doar pe o singura variabila):

