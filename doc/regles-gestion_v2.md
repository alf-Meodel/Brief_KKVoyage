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
- RG09 : Une réservation est représenté par un identifiant unique 
- RG10 : Une réservation possède une numéro de réservation unique (Le PNR Passenger Name Record) 
- RG11 : Une réservation est identifié  par sa date de réservation
- RG11 : Une réservation est identifié  par son lieu d'arrivée
- RG11 : Une réservation est identifié  par son lieu de départ
- RG11 : Une réservation est identifié  par sa date d'arrivée
- RG11 : Une réservation est identifié  par sa date de départ
- RG11 : Une réservation est identifié  par l'horaire embarquement
- RG11 : Une réservation est identifié  par l'horaire de debarquement

```
<!-- - RG11 : Une réservation est identifié  par la durée estimé du voyage -->

----
- **RG13 :** Une réservation est associé à **un unique client**
- **RG13 :** Une réservation est associé à **un unique passager**
- **RG14 :** Une réservation concerne **un ou plusieurs vol** 

## Passager
---
```
- RG15 : Un Passager est représenté par un identifiant unique 
- RG18 : Un Passager est authentifié par un document d'identitée
- RG16 : Un Passager est authentifié par son nom
- RG17 : Un Passager est authentifié par son prenom
- RG18 : Un Passager est authentifié par son adresse

```
- **RG19 :** Un Passager est **associé à une ou n reservation**
- **RG20 :** Un Passager est **associé à un siège** unique
---


## Siège
---
```
- RG29 : Un siège est représenté par un identifiant unique 
- RG30 : Un siège est représenté par son numéro d'emplacement
- RG31 : Un siège est représenté par son prix
- RG32 : Un siège est représenté par son statut ( libre réservé)
```

- **RG33 :** Un siège peut accueillir **0 ou 1 passager**.
- **RG35 :** Un siège est associé à **un seul avion**. 


## Avion 
---
```
- RG36 : Un Avion est représenté par un identifiant unique 
- RG36 : Un Avion est représenté par un modèle
```

- **RG39 :** Un Avion est associé à **n ou m sièges** ( il ne peut y avoir un seul siege minimum 2 donc n)
- **RG40 :** Un Avion est associé à **0 ou n vols** 
( il se peut qu'un avion ne vol pas ou qu'il participe à plusieurs vols )
- **RG39 :** Un Avion peut faire l'objet d **0 ou n escales**
- **RG39 :** Un Avion peut appartenir à **0 ou n compagnies aeriennes** (location)


## Vol
---
```
- RG41 : Un vol est représenté par un identifiant unique 
- RG45 : Un vol doit avoir un numéro de vol.
```
- **RG46 :** Un vol peut etre associé à **0 ou n reservations**
- **RG47 :** un vol est associé à **1 aeroports** (un aeroport pour l'association depart et un aeroport pour l'association arrivée )
( decoller d'un aeroport faire un tour et revenir dans le même aeroport ne compte pas) 
- **RG48 :** un vol peut contenir **0 ou 1 escales**
- **RG49 :** un vol est associé à **une seule compagnies aérienne**
- **RG50 :** un vol est associé à **un avion unique**
---


## Compagnie Aérienne
---
```
- RG51 : Une compagnie aérienne est représenté par un identifiant unique 
- RG52 : Une compagnie aérienne est représenté par son nom
```

- **RG53 :**  Une compagnie aérienne peut **proposer 1 ou n vols** 
- **RG54 :**  Une compagnie aérienne peut **annuler un ou n vols qu'elle propose**
<!-- - **RG55 :**  Une compagnie aérienne peut **proposer 0 ou n reservations**
- **RG56 :**  Une compagnie aérienne peut **annuler 0 ou n reservations**    -->
- <!-- Dans la réalité métier, une compagnie aérienne ne gère pas directement les réservations. Ce sont les clients qui réservent des vols, et chaque réservation est rattachée à un vol, pas à une compagnie directement. -->
- **RG57 :**  Une compagnie aérienne dispose de **1 ou n avions** ( pas de 0,n pour les compagnies qui louent des avions car ca revient au meme elles peuvent disposer d'un avion)

remake 
- **RG55 :** Une compagnie aérienne peut proposer 1 ou n vols à la reservation. ??
- **RG56 :** Une compagnie aérienne peut annuler 1 ou n vols, ce qui entraîne l’annulation des réservations associées.
---

## Aeroport 
---
```
- RG58 :  Un aéroport est représenté par un identifiant unique 
- RG59 :  Un aéroport est représenté par son nom
- RG60 :  Un aéroport est représenté par son ville
- RG61 :  Un aéroport est représenté par son pays
```

- **RG62 :**  Un aéroport est associé **à une seule ville**
- **RG63 :**  Un aéroport peut etre associé à **0 ou n vols**
- **RG63 :**  Un aéroport peut peut accueillir **0 ou n escales**


## Escale 
--- 
```
nosu allons utiliser une clé composé 
```
```
- RG65 :  Une escale est définie par une heure d'arrivée ( combinaison 1) 
- RG66 : Une escale est définie par une heure de départ ( combinaison 2)
- RG66 : Une escale est définie par sa durée 
- RG67 : Une escale est définie par un aeroport 
- RG67 : Une escale est définie par son type (l'escale technique, l'escale avec changement d'avion et l'escale longue.)
```
- RG67 : Une escale est définie l'id vol et id aeroprt ( pour PK composé robuste  )

- **RG68 :**  une escale est **associée à un unique aeroport** 
- **RG68 :**  une escale est **associée à un vol**
<!-- - **RG68 :**  une escale peut inclure 0 ou 1 changement d'avion >>>> comem chaque vol est définit par un avion aps la peine de préciser ce changement --> 

## Ville
---
```
- RG69 :  Une ville est représenté par un identifiant unique 
- RG70 :  Une ville est représenté par son nom
- RG71 :  Une ville est représenté par sa région
- RG72 :  Une ville est représenté par son pays

```
- **RG73 :**  Une ville peut avoir **1 ou n aeroports**


-----------------------------------------
-----------------------------------------

# ╭─━━━━━─╯ Brief ╰─━━━━━─╮ 

```
- Un vol est ouvert à la réservation et refermé sur ordre de la compagnie.
- Un vol peut être annulé par la compagnie
- Des compagnies aériennes proposent différents vols.
- Un client peut réserver un ou plusieurs vols, pour des passagers différents.
- Une réservation concerne un seul vol et un seul passager.
- Une réservation peut être annulée ou confirmée.
- Un vol a un aéroport de départ et un aéroport d'arrivée.
- Un vol a un jour et une heure de départ, et un jour et une heure d'arrivée.
- Un vol peut comporter des escales dans des aéroports.
- Une escale a une heure d'arrivée et une heure de départ.
- Chaque aéroport dessert une ou plusieurs villes.
```