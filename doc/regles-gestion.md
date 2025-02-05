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

- **RG05 :** Un client peut réserver **pour lui** même
- **RG06 :** Un client peut réserver **pour plusieurs personnes**

- **RG07 :** Un client peut effectuer **une reservation** 
- **RG08 :** Un client peut effectuer **plusieurs reservation**
<!-- - **RG07 :** Un client peut annuler ses reservations  -->
---


## Reservation 
---
```
- RG09 : Une Reservation est représenté par un identifiant unique 
- RG10 : Une Reservation possède une date de réservation
```

- **RG11 :** Une réservation concerne une ville de départ 
- **RG12 :** Une réservation concerne une ville d'arrivée

---
- **RG13 :** Une réservation concerne un seul passager
- **RG14 :** Une réservation concerne un ou plusieurs sièges
- **RG15 :** Une réservation concerne un ou plusieurs vols
- **RG16 :** Une réservation concerne une ou plusieurs compagnie aérienne


## Siège
---
```
- RG17 : Un siège est représenté par son id
- RG18 : Un siège est représenté par son numéro d'emplacement
- RG19 : Un siège est représenté par son prix
```

- **RG20 :** Un siège est associé à un seul client.
<!-- - **RG20 :** Un siège appartient à un avion  -->

## Avion
---
```
- RG21 : Un avion est représenté par un id unique 
- RG022 : Un avion est représenté par le nom de sa compagnie 
- RG23 : Un avion est représenté par le modèle de son avion

```
- **RG24 :**  Un avion est composé d'au moins un siège
- **RG25 :**  Un avion est composé d'un nombre de sièges max
---
- **RG25 :**  Un avion est associé à une seule compagnie aérienne
- **RG25 :**  Un avion est associé à une ou plusieurs réservations
---
- **RG25 :**  Un avion est associé à un ou plusieurs aéroports

- **RG28 :** Un avion est associé à un aéroport de départ 
- **RG29 :** Un avion est associé à un aéroport d'arrivée 
---
- **RG30 :** un avion peut comporter aucune escales
- **RG31 :** un avion peut comporter plusieurs escales
---


## Vol
---
```
- RG21 : Un Vol est représenté par un id unique 

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

- **RG50 :**  Une ville est composé d'un ou plusieurs aéroports
---
---
