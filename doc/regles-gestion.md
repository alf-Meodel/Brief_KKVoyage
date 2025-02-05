-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Client 
---
```
- RG01 : Un client est représenté par un identifiant unique 
- RG02 : Un client est représenté par son nom
- RG03 : Un client est représenté par son prenom
- RG04 : Un client est représenté par son mail 
```

- **RG05 :** Un client peut réserver **pour lui** même
- **RG06 :** Un client peut réserver **pour plusieurs personnes**
---
- **RG07 :** Un client peut réserver **un siège** sur un vol,
- **RG08 :** Un client peut réserver **plusieurs sièges** sur un vol
---

- **RG09 :** Un client peut réserver **un siège** sur **un vol différents**
- **RG10 :** Un client peut réserver **plusieurs sièges** sur **un vol différents**

---


## Reservation 
---
```
- RG11 : Une Reservation est représenté par un identifiant unique 
- RG12 : Une Reservation possède une date de réservation
```

- **RG14 :** Une réservation concerne un seul passager
- **RG13 :** Une réservation concerne un ou plusieurs sièges
- **RG15 :** Une réservation concerne un ou plusieurs vols
- **RG16 :** Une réservation concerne une ou plusieurs compagnie aérienne
<!-- - **RG01 :** Une réservation peut être annulée ou confirmée. -->


## Siège
---
```
- RG17 : Un Siège est représenté par son id
- RG18 : Un Siège est représenté par un numéro de siège unique 
- RG19 : Un Siège est représenté par son prix
```

- **RG20 :** Un siège est associé à un seul client.
<!-- - **RG20 :** Un siège appartient à un avion  -->

## Vol
---
```
- RG21 : Un Vol est représenté par un id unique 
- RG022 : Un Vol est représenté par le nom de sa compagnie 
- RG23 : Un Vol est représenté par le modèle de son avion

```
- **RG24 :**  Un Vol est composé d'au moins un siège
- **RG25 :**  Un Vol est composé d'un nombre de sièges max
---
- **RG25 :**  Un Vol appartient à une seule compagnie aérienne
- **RG25 :**  Un Vol est associé à un ou plusieurs aéroports
---
- **RG26 :** Un vol doit avoir un jour et une heure de départ,
 - **RG27 :** Un vol doit avoir un jour et une heure 
d'arrivée.
---

- **RG28 :** Un vol est associé à un aéroport de départ 
- **RG29 :** Un vol est associé à un aéroport d'arrivée 
---
- **RG30 :** un vol peut comporter aucune escales
- **RG31 :** un vol peut comporter plusieurs escales
---


## Compagnie Aérienne 
---
```
- RG32 : Une compagnie aérienne est représenté par un id unique 
- RG33 : Une compagnie aérienne est représenté par son nom
```
---
- **RG34 :**  Une compagnie aérienne peut ajouter un ou plusieurs vols 
- **RG34 :**  Une compagnie aérienne peut annuler un ou plusieurs vols

---
- **RG36 :**  Une compagnie aérienne peut proposer des réservations sur un ou plusieurs vol 
- **RG37 :**  Une compagnie aérienne peut arréter les réservations sur un ou plusieurs vol
---


## Aeroport 
---
```
- RG40 :  Un aéroport possède un identifiant unique
- RG41 :  Un aéroport possède un nom

```

- **RG43 :**  Un ou plusieurs aéroports peuvent se trouver dans une même ville
- **RG43 :**  Un aéroport est associé à une ou plusieurs compagnies aériennes
- **RG43 :**  Un aéroport est composé de plusieurs vols

---

## Escale 
---
```
- RG44 : Une escale est définie par une heure de départ
- RG45 :  Une escale est définie par heure d'arrivée

```

- **RG45 :**  Une escale est associé à une ville 
- **RG45 :**  Une escale est associé à un aéroport 



---

- **RG46 :**  Une escale peut laisser aux clients le même vol
- **RG47 :**  Une escale peut donner aux clients un nouveau vol

## Villes
---
```
- RG48 :  Une ville possède un id
- RG49 :  Une ville possède un nom
```

- **RG50 :**  Une ville peut contenir un ou plusieurs aéroports

---
---

- **RG51 :** Chaque aéroport dessert une ou plusieurs villes.
- **RG52 :** Des compagnies aériennes proposent différents vols.