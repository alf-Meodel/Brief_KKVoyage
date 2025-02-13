-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Client 
---
```
- RG01 : Un client est représenté par un identifiant unique 
- RG02 : Un client est représenté par son prenom
- RG03 : Un client est représenté par son nom
- RG04 : Un client est identifié par son email 
- RG05 : Un client est identifié par son adresse
- RG06 : Un client est identifié par son numéro de téléphone
- RG06 : Un client est identifié par son mot de passe
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
- RG12 : Une réservation est identifié  par son lieu d'arrivée
- RG13 : Une réservation est identifié  par son lieu de départ
- RG14 : Une réservation est identifié  par sa date d'arrivée
- RG15 : Une réservation est identifié  par sa date de départ
- RG16 : Une réservation est identifié  par l'horaire embarquement
- RG17 : Une réservation est identifié  par l'horaire de debarquement
```
<!-- - RG17 : Une réservation est identifié  le montant total  -->
<!-- - RG11 : Une réservation est identifié  par la durée estimé du voyage -->

----
- **RG18 :** Une réservation est associé à **un unique client**
- **RG19 :** Une réservation est associé à **un unique passager**
- **RG20 :** Une réservation concerne **un ou plusieurs vol** 

## Passager
---
```
- RG21 : Un Passager est représenté par un identifiant unique 
- RG22 : Un Passager est authentifié par un document d'identitée ( numéro de passeport ou  id card)
- RG25 : Un Passager est authentifié par sa date de naissance
- RG23 : Un Passager est authentifié par son nom
- RG24 : Un Passager est authentifié par son prenom
- RG25 : Un Passager est authentifié par son adresse
- RG25 : Un Passager est authentifié par sa nationalité

```
- **RG26 :** Un Passager est **associé à une ou n reservation**
- **RG27 :** Un Passager est **associé à un siège** unique
---


## Siège
---
```
- RG28 : Un siège est représenté par un identifiant unique 
- RG29 : Un siège est représenté par son numéro de siège
- RG30 : Un siège est représenté par son prix
- RG31 : Un siège est représenté par son statut ( libre réservé) ( boolean ????)
- RG31 : Un siège est représenté par sa classe ( economique, business, première)
- RG31 : Un siège est représenté par sa position (couloir,fenetre,milieu)
```

- **RG32 :** Un siège peut accueillir **0 ou 1 passager**.
- **RG33 :** Un siège est associé à **un seul avion**. 


## Avion 
---
```
- RG34 : Un Avion est représenté par un identifiant unique 
- RG35 : Un Avion est représenté par un modèle
```

- **RG36 :** Un Avion est associé à **n ou m sièges** ( il ne peut y avoir un seul siege minimum 2 donc n)
- **RG37 :** Un Avion est associé à **0 ou n vols** 
( il se peut qu'un avion ne vol pas ou qu'il participe à plusieurs vols )
- **RG38 :** Un Avion peut faire l'objet d **0 ou n escales**
- **RG39 :** Un Avions appartient à **une compagnie aeriennes** (location ??  )


## Vol
---
```
- RG40 : Un vol est représenté par un identifiant unique 
- RG41 : Un vol doit avoir un numéro de vol.
- RG42 : Un vol doit avoir une durée de vol.
```
- **RG43 :** Un vol peut etre associé à **0 ou n reservations**
- **RG44 :** un vol est associé à **1 aeroports** (un aeroport pour l'association depart et un aeroport pour l'association arrivée )
( decoller d'un aeroport faire un tour et revenir dans le même aeroport ne compte pas) 
- **RG45 :** un vol peut contenir **0 ou 1 escales**
- **RG46 :** un vol est associé à **une seule compagnies aérienne**
- **RG47 :** un vol est associé à **un avion unique**
---


## Compagnie Aérienne
---
```
- RG48 : Une compagnie aérienne est représenté par un identifiant unique 
- RG49 : Une compagnie aérienne est représenté par son nom
```
<!-- - RG49 : Une compagnie aérienne est représenté par son code iata  -->

- **RG50 :**  Une compagnie aérienne peut **proposer 1 ou n vols** 
- **RG51 :**  Une compagnie aérienne peut **annuler un ou n vols qu'elle propose**
- **RG52 :**  Une compagnie aérienne dispose de **1 ou n avions** ( pas de 0,n pour les compagnies qui louent des avions car ca revient au meme elles peuvent disposer d'un avion)

remake 
- **RG53 :** Une compagnie aérienne peut proposer 1 ou n vols à la reservation. ??
- **RG54 :** Une compagnie aérienne peut annuler 1 ou n vols, ce qui entraîne l’annulation des réservations associées.
---

## Aeroport 
---
```
- RG55 :  Un aéroport est représenté par un identifiant unique 
- RG56 :  Un aéroport est représenté par son nom
- RG57 :  Un aéroport est représenté par son ville
- RG58 :  Un aéroport est représenté par son pays
```

- **RG59 :**  Un aéroport est associé **à une seule ville**
- **RG60 :**  Un aéroport peut etre associé à **0 ou n vols**
- **RG61 :**  Un aéroport peut peut accueillir **0 ou n escales**


## Escale 
--- 
```
nosu allons utiliser une clé composé 
```
```
- RG62 :  Une escale est définie par une heure d'arrivée ( combinaison 1) 
- RG63 : Une escale est définie par une heure de départ ( combinaison 2)
- RG64 : Une escale est définie par sa durée 
- RG65 : Une escale est définie par son type (l'escale technique, l'escale avec changement d'avion et l'escale longue.)
```
- RG66 : Une escale est définie l'id vol et id aeroprt ( pour PK composé robuste  )

- **RG67 :**  une escale est **associée à un unique aeroport** 
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