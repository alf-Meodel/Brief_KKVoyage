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

- **RG10 :** Un client est **associé à une ou plusieurs reservation**
- **RG13 :** Un client **peut annuler ses reservations**
---

## Reservation 
---
```
- RG20 : Une réservation est représenté par un identifiant unique 
- RG21 : Une réservation possède une date de réservation
```

----
**- RG21 :** Une réservation est associé à **un unique voyage**
**- RG21 :** Une réservation est associé à **un ou plusieurs passager**


## voyage 
---
```
- RG42 : Un voyage est représenté par un identifiant unique 
- RG37 : Un voyage est associé à un aéroport de départ 
- RG38 : Un voyage est associé à un aéroport d'arrivée 
- RG39 : Un voyage doit avoir un jour et une heure de départ,
- RG40 : Un voyage doit avoir un jour et une heure d'arrivée.
```
---
- **RG41 :**  Un voyage est associé à une reservation
- **RG42 :** un voyage peut etre associé à plusieurs aeroports 
---

## Escale 
---
```
- RG55 : Une escale est définie par un identifiant unique
- RG56 : Une escale est définie par une heure de départ
- RG57 :  Une escale est définie par heure d'arrivée

```
- **RG59 :**  Une escale peut etre **associée à zero ou plusieurs voyage **

## Passager
---
```
- RG14 : Un Passager est représenté par un identifiant unique 
- RG15 : Un Passager est authentifié par son nom
- RG16 : Un Passager est authentifié par son prenom
- RG17 : Un client est authentifié par son adresse

```
- **RG18 :** Un Passager est **associé à un siège** unique
- **RG19 :** Un Passager est **associé à une reservation**
---


## Siège
---
```
- RG28 : Un siège est représenté par un identifiant unique 
- RG29 : Un siège est représenté par son numéro d'emplacement
- RG30 : Un siège est représenté par son prix
- RG31 : Un siège est représenté par son statut ( libre réservé)
```

- **RG32 :** Un siège est associé à **un seul passager**.
- **RG32 :** Un ou plusieurs sièges sont associés à un avion.

## Avion
---
```
- RG34 : Un avion est représenté par un identifiant unique 
- RG35 : Un avion est représenté par le nom de sa compagnie 
- RG36 : Un avion est représenté par le modèle de son avion

```
- **RG37 :**  Un avion est composé d'**un ou plusieurs sièges**
- **RG38 :**  Un avion est associé à **une seule compagnie aérienne**
- **RG39 :**  Un avion est associé à **un ou plusieurs aéroports**
---


## Compagnie Aérienne 
---
```
- RG44 : Une compagnie aérienne est représenté par un identifiant unique 
- RG45 : Une compagnie aérienne est représenté par son nom
```
---
- **RG46 :**  Une compagnie aérienne peut **ajouter un ou plusieurs voyages** 
- **RG47 :**  Une compagnie aérienne peut **annuler un ou plusieurs voyages**
- **RG48 :**  Une compagnie aérienne peut **proposer des réservations sur un ou plusieurs voyage** 
- **RG49 :**  Une compagnie aérienne peut arréter **les réservations sur un ou plusieurs voyage**
---

## Aeroport 
---
```
- RG50 :  Un aéroport possède est représenté par un identifiant unique 
- RG51 :  Un aéroport possède est représenté par son nom
- RG51 :  Un aéroport possède est représenté par son ville
- RG51 :  Un aéroport possède est représenté par son pays

```

- **RG52 :**  Un ou plusieurs aéroports peuvent se trouver **dans une même ville**
- **RG53 :**  Un aéroport est associé à **une ou plusieurs compagnies aériennes**
- **RG54 :**  Un aéroport est composé de **plusieurs voyages**

-----------------------------------------
-----------------------------------------
-----------------------------------------


## Villes
---
```
- RG62 :  Une ville est définie par un identifiant unique
- RG63 :  Une ville est définie par son nom
- RG64 :  Une ville est définie par son pays
```

- **RG65 :**  Une ville est composé **d'un ou plusieurs aéroports**
---
---


-----------------------
-----------------------
-----------------------
-----------------------
-----------------------
-----------------------

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