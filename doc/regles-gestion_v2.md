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

- **RG07 :** Un client **peut effectuer 0 ou n reservation**
- **RG08 :** Un client **peut annuler ses reservations**
---

## Reservation 

---

```
- RG20 : Une réservation est représenté par un identifiant unique 
- RG21 : Une réservation possède une numéro de réservation unique
- RG21 : Une réservation possède une date de réservation
```

----
- **RG21 :** Une réservation est associé à **1 ou n vol** 
- **RG21 :** Une réservation est associé à **un ou plusieurs passager**
<!-- - **RG21 :** Une réservation est associé à **une seule compagnie aerienne** -->

## Vol
---
```
- RG14 : Un vol est représenté par un identifiant unique 
- RG15 : Un vol est associé à un aéroport de départ 
- RG16 : Un vol est associé à un aéroport d'arrivée 
- RG17 : Un vol doit avoir un jour et une heure de départ,
- RG18 : Un vol doit avoir un jour et une heure d'arrivée.
```
---
- **RG19 :** Un vol est associé à **0 ou n reservation**
- **RG20 :** un vol est associé à **1 ou n aeroports** ( on peut decoller d'un aeroport faire un tour et revenir dans le même aeroport) 
- **RG21 :** un vol peut contenir **0 ou n escales**
- **RG22 :** un vol est associé à **une compagnies aérienne**
- **RG22 :** un vol est associé à **un unique avion**
---

## Avion 

---

```
- RG20 : Un Avion est représenté par un identifiant unique 
- RG21 : Un Avion possède une numéro de réservation unique
- RG21 : Un Avion possède une date de réservation
```

----
- **RG21 :** Un Avion est associé à **1 ou n sièges** 
- **RG21 :** Un Avion est associé à **0 ou n vols** ( il se peut qu'un avion ne vol pas ou qu'il participe à plusieurs vols )


## Escale 
--- 
```
- RG23 : Une escale est définie par un identifiant uniqueX
- RG24 :  Une escale est définie par une heure d'arrivée
- RG25 : Une escale est définie par une heure de départ
- RG25 : Une escale est définie par une ville 
```

- **RG26 :**  une escale est **associée à un vol**



## Passager
---
```
- RG27 : Un Passager est représenté par un identifiant unique 
- RG28 : Un Passager est authentifié par son nom
- RG29 : Un Passager est authentifié par son prenom
- RG30 : Un client est authentifié par son adresse

```
- **RG19 :** Un Passager est **associé à une ou n reservation**
- **RG18 :** Un Passager est **associé à un siège** unique
- **RG18 :** Un Passager est **associé à 0 ou n bagages**
---


## Siège
---
```
- RG33 : Un siège est représenté par un identifiant unique 
- RG34 : Un siège est représenté par son numéro d'emplacement
- RG35 : Un siège est représenté par son prix
- RG36 : Un siège est représenté par son statut ( libre réservé)
```

- **RG37 :** Un siège peut contenir **0 ou 1 passager**.
- **RG37 :** Un siège est associé à **un vol**. ( siège unique dans un vol unique)
- **RG37 :** Un siège est associé à **un seul avion**. 

## Bagage
---
```
- RG34 : Un Bagage est représenté par un identifiant unique 
- RG35 : Un Bagage est représenté par son numéro de bagage
- RG36 : Un Bagage est représenté par ses dimensions
- RG36 : Un Bagage est représenté par son poids
- RG36 : Un Bagage est représenté par son type ( bagage à main ou soute )

```
- **RG37 :**  Un Bagage est lié  à **un passager**
- **RG39 :**  Un Bagage est enregistré pour **un ou plusieurs vols**
---


## Compagnie Aérienne
---
```
- RG45 : Une compagnie aérienne est représenté par un identifiant unique 
- RG46 : Une compagnie aérienne est représenté par son nom
```
---
- **RG47 :**  Une compagnie aérienne peut **ajouter un ou plusieurs vols** 
- **RG48 :**  Une compagnie aérienne peut **annuler un ou plusieurs vols qu'elle propose**
- **RG49 :**  Une compagnie aérienne peut **proposer des réservations sur un ou plusieurs vol qu'elle propose** 
- **RG50 :**  Une compagnie aérienne peut arréter **les réservations sur un ou plusieurs vol qu'elle propose**
- **RG50 :**  Une compagnie aérienne est composée d'**un ou plusieurs avions**
<!-- - **RG50 :**  Une compagnie aérienne est composée **d'aucun avion** ???????????????  -->
- **RG50 :**  Une compagnie aérienne est associé a **un ou plusieurs aeroports**

---

## Aeroport 
---
```
- RG51 :  Un aéroport est représenté par un identifiant unique 
- RG52 :  Un aéroport est représenté par son nom
- RG53 :  Un aéroport est représenté par son ville
- RG54 :  Un aéroport est représenté par son pays
```
---
Un aéroport peut être le point de départ ou d’arrivée de plusieurs vols.

- **RG55 :**  Un aéroport est associé **à une seule ville**??
- **RG56 :**  Un aéroport peut etre associé à **0 ou n vols**

## Ville??
---
```
- RG51 :  Une ville est représenté par un identifiant unique 
- RG51 :  Une ville est représenté par son nom
- RG51 :  Une ville est représenté par sa région
- RG51 :  Une ville est représenté par son pays

```

- **RG55 :**  Une ville peut avoir 0 ou n aeroports


-----------------------------------------
-----------------------------------------
-----------------------------------------

```
- Un vol est ouvert à la réservation et refermé sur ordre de la compagnie.
- Un vol peut être annulé par la compagnie
- Un vol a un aéroport de départ et un aéroport d'arrivée.
- Un vol a un jour et une heure de départ, et un jour et une heure d'arrivée.
- Un vol peut comporter des escales dans des aéroports.
- Une réservation concerne un seul vol et un seul passager.
- Une réservation peut être annulée ou confirmée.
- Un client peut réserver un ou plusieurs vols, pour des passagers différents.
- Une escale a une heure d'arrivée et une heure de départ.
- Chaque aéroport dessert une ou plusieurs villes.
- Des compagnies aériennes proposent différents vols.