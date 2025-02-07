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
- RG05 : Un client est identifié par son adresse
- RG06 : Un client est identifié par son numéro de téléphone
```

- **RG07 :** Un client **peut n'avoir aucune reservation**
- **RG07 :** Un client **peut passer plusieurs reservation**
- **RG08 :** Un client **peut annuler ses reservations**
---

## Reservation 

---

```
- RG09 : Une réservation est représenté par un identifiant unique 
- RG10 : Une réservation possède une date de réservation
```

----
**- RG11 :** Une réservation est associé à **un seul voyage**
**- RG12 :** Une réservation est associé à **un ou plusieurs passager**
**- RG13 :** Une réservation est associé à **une seule compagnie aerienne**

## voyage 
---
```
- RG14 : Un voyage est représenté par un identifiant unique 
- RG15 : Un voyage est associé à un aéroport de départ 
- RG16 : Un voyage est associé à un aéroport d'arrivée 
- RG17 : Un voyage doit avoir un jour et une heure de départ,
- RG18 : Un voyage doit avoir un jour et une heure d'arrivée.
```
---
- **RG19 :** Un voyage est associé à une reservation
- **RG20 :** un voyage est associé à plusieurs aeroports 

- **RG21 :** un voyage peut etre associé à aucune escales
- **RG21 :** un voyage peut etre associé à plusieurs escales
- **RG22 :** un voyage est associé à une ou plusieurs compagnies aérienne
---

## Escale 
---
```
- RG23 : Une escale est définie par un identifiant unique
- RG24 :  Une escale est définie par une heure d'arrivée
- RG25 : Une escale est définie par une heure de départ
```
- **RG26 :**  Aucune escales peuvent etre **associée à un voyage**
- **RG26 :**  plusieurs escale peuvent etre **associée à un voyage**

## Passager
---
```
- RG27 : Un Passager est représenté par un identifiant unique 
- RG28 : Un Passager est authentifié par son nom
- RG29 : Un Passager est authentifié par son prenom
- RG30 : Un client est authentifié par son adresse

```
- **RG31 :** Un Passager est **associé à un seul siège** 
- **RG32 :** Un Passager est **associé à une seule reservation**
---


## Siège
---
```
- RG33 : Un siège est représenté par un identifiant unique 
- RG34 : Un siège est représenté par son numéro d'emplacement
- RG35 : Un siège est représenté par son prix
- RG36 : Un siège est représenté par son statut ( libre réservé)
```

- **RG37 :** Un siège est associé à **un seul passager**.
- **RG38 :** Un ou plusieurs sièges sont associés à un avion.

## Avion
---
```
- RG39 : Un avion est représenté par un identifiant unique 
- RG40 : Un avion est représenté par le nom de sa compagnie 
- RG41 : Un avion est représenté par le modèle de son avion

```
- **RG42 :**  Un avion est composé d'**un ou plusieurs sièges**
- **RG43 :**  Un avion est associé à **un ou plusieurs aéroports**
- **RG44 :**  Un avion est associé à **une seule ou plusieurs compagnies aériennes**
---


## Compagnie Aérienne
---
```
- RG45 : Une compagnie aérienne est représenté par un identifiant unique 
- RG46 : Une compagnie aérienne est représenté par son nom
```
---
- **RG47 :**  Une compagnie aérienne peut **ajouter un ou plusieurs voyages** 
- **RG48 :**  Une compagnie aérienne peut **annuler un ou plusieurs voyages qu'elle propose**
- **RG49 :**  Une compagnie aérienne peut **proposer des réservations sur un ou plusieurs voyage qu'elle propose** 
- **RG50 :**  Une compagnie aérienne peut arréter **les réservations sur un ou plusieurs voyage qu'elle propose**
- **RG50 :**  Une compagnie aérienne est composée d'**un ou plusieurs avions**
---

## Aeroport 
---
```
- RG51 :  Un aéroport possède est représenté par un identifiant unique 
- RG52 :  Un aéroport possède est représenté par son nom
- RG53 :  Un aéroport possède est représenté par son ville
- RG54 :  Un aéroport possède est représenté par son pays
```

- **RG55 :**  Il peut n'y avoir aucun aeroport **dans une ville**
- **RG55 :**  Plusieurs aéroports peuvent se trouver **dans une même ville**

- **RG56 :**  Un aéroport peut etre associé à **aucune compagnies aériennes**
- **RG56 :**  Un aéroport peut etre associé à **plusieurs compagnies aériennes**


- **RG57 :**  Un aéroport peut proposer **aucun voyages**
- **RG57 :**  Un aéroport peut proposer **plusieurs voyages**


-----------------------------------------
-----------------------------------------
-----------------------------------------

```
- Un voyage est ouvert à la réservation et refermé sur ordre de la compagnie.
- Un voyage peut être annulé par la compagnie
- Un voyage a un aéroport de départ et un aéroport d'arrivée.
- Un voyage a un jour et une heure de départ, et un jour et une heure d'arrivée.
- Un voyage peut comporter des escales dans des aéroports.
- Une réservation concerne un seul voyage et un seul passager.
- Une réservation peut être annulée ou confirmée.
- Un client peut réserver un ou plusieurs voyages, pour des passagers différents.
- Une escale a une heure d'arrivée et une heure de départ.
- Chaque aéroport dessert une ou plusieurs villes.
- Des compagnies aériennes proposent différents voyages.
```
