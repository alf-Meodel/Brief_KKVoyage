-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Client 
---
```
- RG01 : Un client est représenté par un identifiant unique 
- RG02 : Un client est représenté par son nom
- RG03 : Un client est représenté par son prenom
- RG04 : Un client est identifié par son mail 
```

- **RG05 :** Un client peut réserver **pour lui** et **pour plusieurs personnes**
- **RG06 :** Un client peut effectuer **une reservation** 
- **RG07 :** Un client peut effectuer **plusieurs reservation**
<!-- - **RG07 :** Un client peut annuler ses reservations  -->
---


## Reservation 
---
```
- RG08 : Une Reservation est représenté par un identifiant unique 
- RG09 : Une Reservation possède une date de réservation
```

- **RG10 :** Une réservation concerne une ville de départ 
- **RG11 :** Une réservation concerne une ville d'arrivée

---
- **RG12 :** Une réservation concerne un seul passager
- **RG13 :** Une réservation concerne un ou plusieurs sièges
- **RG14 :** Une réservation concerne un ou plusieurs vols
- **RG15 :** Une réservation concerne une ou plusieurs compagnie aérienne


## Siège
---
```
- RG16 : Un siège est représenté par un identifiant unique 
- RG17 : Un siège est représenté par son numéro d'emplacement
- RG18 : Un siège est représenté par son prix
```

- **RG19 :** Un siège est associé à un seul client.
<!-- - **RG20 :** Un siège appartient à un avion  -->

## Avion
---
```
- RG20 : Un avion est représenté par un identifiant unique 
- RG021 : Un avion est représenté par le nom de sa compagnie 
- RG22 : Un avion est représenté par le modèle de son avion

```
- **RG23 :**  Un avion est composé d'au moins un siège
- **RG24 :**  Un avion est composé d'un nombre de sièges max
---
- **RG25 :**  Un avion est associé à une seule compagnie aérienne
- **RG26 :**  Un avion est associé à une ou plusieurs réservations
---
- **RG27 :**  Un avion est associé à un ou plusieurs aéroports

- **RG28 :** Un avion est associé à un aéroport de départ 
- **RG29 :** Un avion est associé à un aéroport d'arrivée 
---
- **RG30 :** un avion peut comporter aucune escales
- **RG31 :** un avion peut comporter plusieurs escales
---


## Vol
---
```
- RG21 : Un Vol est représenté par un identifiant unique 

- RG28 : Un vol est associé à un aéroport de départ 
- RG29 : Un vol est associé à un aéroport d'arrivée 

- RG26 : Un vol doit avoir un jour et une heure de départ,
- RG27 : Un vol doit avoir un jour et une heure 
d'arrivée.
```

---
- **RG25 :**  Un Vol est associé à un ou plusieurs aéroports
---

---
- **RG30 :** un vol peut comporter aucune escales???
- **RG31 :** un vol peut comporter plusieurs escales???
---


## Compagnie Aérienne 
---
```
- RG32 : Une compagnie aérienne est représenté par un identifiant unique 
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
- RG40 :  Un aéroport possède est représenté par un identifiant unique 
- RG41 :  Un aéroport possède est représenté par son nom

```

- **RG43 :**  Un ou plusieurs aéroports peuvent se trouver dans une même ville
- **RG43 :**  Un aéroport est associé à une ou plusieurs compagnies aériennes
- **RG43 :**  Un aéroport est composé de plusieurs vols

---

## Escale 
---
```
- RG44 : Une escale est définie par un identifiant unique ???????

- RG44 : Une escale est définie par une heure de départ
- RG45 :  Une escale est définie par heure d'arrivée

```
<!-- - RG45 :  Une escale est définie par une durée modulable  -->
- **RG45 :**  Une escale est associé à une ville 
- **RG45 :**  Une escale est associé à un aéroport 
---

- **RG46 :**  Une escale peut etre associé à un changement d'avion ???
- **RG46 :**  Une escale peut s'effectuer sans changement d'avion ???

## Villes
---
```
- RG48 :  Une ville possède un id
- RG49 :  Une ville possède un nom
```

- **RG50 :**  Une ville est composé d'un ou plusieurs aéroports
---
---
