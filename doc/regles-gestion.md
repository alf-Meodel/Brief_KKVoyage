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
- **RG07 :** Un client peut reserver  **un siège**
- **RG08 :** Un client peut devenir **un passager**
- **RG09 :** Un client peut ajouter d'autres **passagers**
- **RG10 :** Un client est **associé à une reservation**
- **RG11 :** Un client peut effectuer **une ou plusieurs réservation** 
- **RG12 :** Un client peut ajouter **un ou plusieurs passager** à une reservation
- **RG13 :** Un client **peut annuler ses reservations**
 <!-- ( CONFIRMER = paiement) -->
---

## Passager
---
```
- RG14 : Un Passager est représenté par un identifiant unique 
- RG15 : Un Passager est authentifié par son nom
- RG16 : Un Passager est authentifié par son prenom
- RG17 : Un client est authentifié par son adresse

```
- **RG18 :** Un Passager est **associé à un siège (réservé)**
- **RG19 :** Un Passager est **associé à une reservation**
---

## Reservation 

---
```
- RG20 : Une réservation est représenté par un identifiant unique 
- RG21 : Une réservation possède une date de réservation
```


<!-- - **RG14 :** Une réservation concerne un seul vol ( règle d'origine fausse) car une réservation peut concerner deux vols si l'avion fait escale -->

<!-- - **RG13 :** Une réservation concerne un seul passager REGLE FAUSSE CAR ON PEUT AJOUTER PLUSIEURS PASSAGERS ?  -->


----
<!-- - **RG28 :**  Un avion est composé d'**un nombre de sièges max** -->


- **RG22 :** Une réservation concerne **un ou plusieurs sièges** 
- **RG23 :** Une réservation est **limitée à un nombre maximum de sièges**
- **RG24 :** Une réservation est associée à **un ou plusieurs avions** 
- **RG25 :** Une réservation est associée à **une ou plusieurs compagnie aérienne**

- **RG26 :** Une réservation est associée à un **aeroport de départ** 
- **RG27 :** Une réservation est associée à un **aéroport d'arrivée**



## Siège
---
```
- RG28 : Un siège est représenté par un identifiant unique 
- RG29 : Un siège est représenté par son numéro d'emplacement
- RG30 : Un siège est représenté par son prix
- RG31 : Un siège est représenté par son statut ( libre réservé)
```

- **RG32 :** Un siège est associé à **un seul passager**.
- **RG33 :** Un siège est associé à **un seul avion**.
<!-- - **RG20 :** Un siège appartient à un avion  -->

## Avion
---
```
- RG34 : Un avion est représenté par un identifiant unique 
- RG35 : Un avion est représenté par le nom de sa compagnie 
- RG36 : Un avion est représenté par le modèle de son avion

```
- **RG37 :**  Un avion est composé d'**au moins un siège**
- **RG38 :**  Un avion est associé à **une seule compagnie aérienne**
<!-- - **RG30 :**  Un avion est associé à **une ou plusieurs réservations** -->
- **RG39 :**  Un avion est associé à **un ou plusieurs aéroports**
- **RG40 :**  Un avion est associé à **un aéroport de départ** 
- **RG41 :**  Un avion est associé à **un aéroport d'arrivée**
<!-- - **RG34 :**  un avion peut comporter **aucune ou plusieurs escales** -->
---


## Vol
---
```
- RG42 : Un vol est représenté par un identifiant unique 
- RG37 : Un vol est associé à un aéroport de départ 
- RG38 : Un vol est associé à un aéroport d'arrivée 
- RG39 : Un vol doit avoir un jour et une heure de départ,
- RG40 : Un vol doit avoir un jour et une heure 
d'arrivée.
```

---
- **RG41 :**  Un vol est associé à un ou plusieurs aéroports
- **RG42 :** un vol peut etre associé à une escale 
---


## Compagnie Aérienne 
---
```
- RG44 : Une compagnie aérienne est représenté par un identifiant unique 
- RG45 : Une compagnie aérienne est représenté par son nom
```
---
- **RG46 :**  Une compagnie aérienne peut **ajouter un ou plusieurs vols** 
- **RG47 :**  Une compagnie aérienne peut **annuler un ou plusieurs vols**
- **RG48 :**  Une compagnie aérienne peut **proposer des réservations sur un ou plusieurs vol** 
- **RG49 :**  Une compagnie aérienne peut arréter **les réservations sur un ou plusieurs vol**
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
- **RG54 :**  Un aéroport est composé de **plusieurs vols**

---

## Escale 

---
```
- RG55 : Une escale est définie par un identifiant unique
- RG56 : Une escale est définie par une heure de départ
- RG57 :  Une escale est définie par heure d'arrivée

```
- **RG58 :**  Une escale est **associée à une ville** 
- **RG59 :**  Une escale est **associée à un aéroport **
- **RG60 :**  Une escale peut etre **associé à un changement d'avion**
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