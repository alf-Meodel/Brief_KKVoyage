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
- RG07 : Un client est identifié par son mot de passe
```

- **RG08 :** Un client **peut effectuer 0 ou n reservation**
- **RG09 :** Un client **peut annuler ses reservations**
---

## Reservation 
---
```
- RG10 : Une réservation est représenté par un identifiant unique 
- RG11 : Une réservation possède une numéro de réservation unique (Le PNR Passenger Name Record) 
- RG12 : Une réservation est identifié  par sa date de réservation
- RG13 : Une réservation est identifié  par son lieu d'arrivée
- RG14 : Une réservation est identifié  par son lieu de départ
- RG15 : Une réservation est identifié  par sa date d'arrivée
- RG16 : Une réservation est identifié  par sa date de départ
- RG17 : Une réservation est identifié  par l'horaire embarquement
- RG18 : Une réservation est identifié  par l'horaire de debarquement
```
<!-- - RG18 : Une réservation est identifié  par le nom des vols réservés   -->

----
- **RG19 :** Une réservation est associé à **un unique client**
- **RG20 :** Une réservation est associé à **un unique passager**
- **RG21 :** Une réservation concerne **un ou plusieurs vol** 
- **RG21 :** Une réservation peut inclure  **0 ou n escales** 

---
## Passager
---
```
- RG22 : Un Passager est représenté par un identifiant unique 
- RG23 : Un Passager est authentifié par un document d'identitée ( numéro de passeport ou  id card)
- RG24 : Un Passager est authentifié par sa date de naissance
- RG25 : Un Passager est authentifié par son nom
- RG26 : Un Passager est authentifié par son prenom
- RG27 : Un Passager est authentifié par son adresse
- RG28 : Un Passager est authentifié par sa nationalité
```
- **RG29 :** Un Passager est **associé à une ou n reservation**
- **RG30 :** Un Passager est **associé au siège d'un vol**
---

## Siège
---
```
- RG31 : Un siège est représenté par un identifiant unique 
- RG32 : Un siège est représenté par son numéro de siège
- RG33 : Un siège est représenté par son prix
- RG34 : Un siège est représenté par son statut ( libre réservé) ( boolean ????)
- RG35 : Un siège est représenté par sa classe ( economique, business, première)
- RG36 : Un siège est représenté par sa position (couloir,fenetre,milieu)
```
- **RG37 :** Un siège peut accueillir **0 ou 1 passager**.
- **RG38 :** Un siège est associé à **un seul avion**. 


---
## Avion 
---
```
- RG39 : Un Avion est représenté par un identifiant unique 
- RG40 : Un Avion est représenté par un modèle
```

- **RG41 :** Un Avion est associé à **n ou m sièges** 
- **RG42 :** Un Avion est associé à **0 ou n vols** 
( il se peut qu'un avion ne vole pas ou qu'il participe à plusieurs vols )
- **RG43 :** Un Avion peut faire l'objet d **0 ou n escales**
- **RG44 :** Un Avion appartient à **une compagnie aeriennes** 


---
## Vol
---
```
- RG45 : Un vol est représenté par un identifiant unique 
- RG46 : Un vol doit avoir un numéro de vol.
- RG47 : Un vol doit avoir une durée de vol.
```
- **RG48 :** Un vol peut etre associé à **0 ou n reservations**
- **RG48 :** Un vol possède un aeroport de depart et un aeroport d'arrivée 
<!-- - **RG49 :** un vol est associé à **1 aeroports** (un aeroport pour l'association depart et un aeroport pour l'association arrivée )
( decoller d'un aeroport faire un tour et revenir dans le même aeroport ne compte pas) ?????????????? NO -->

- **RG49 :** un vol est associé à **1 aeroport de depart est 1 aeroport d'arrivée**
- **RG51 :** un vol est associé à **une seule compagnies aérienne**
- **RG52 :** un vol est associé à **un avion unique**
---


## Compagnie Aérienne
---
```
- RG53 : Une compagnie aérienne est représenté par un identifiant unique 
- RG54 : Une compagnie aérienne est représenté par son nom
- RG49 : Une compagnie aérienne est représenté par son code iata 
```

- **RG55 :**  Une compagnie aérienne peut **proposer 0 ou n vols** (une compagnie peut très bien ne proposer aucun vol comme pour le covid etc)
- **RG56 :**  Une compagnie aérienne peut **annuler un ou n vols qu'elle propose**
- **RG57 :**  Une compagnie aérienne dispose de **1 ou n avions** ( pas de 0,n pour les compagnies qui louent des avions car ca revient au meme elles peuvent disposer d'un avion)
- **RG58 :** Une compagnie aérienne peut proposer 1 ou n vols à la reservation. ??
- **RG59 :** Une compagnie aérienne peut annuler 1 ou n vols, ce qui entraîne l’annulation des réservations associées.
---

## Aeroport 
---
```
- RG60 :  Un aéroport est représenté par un identifiant unique 
- RG61 :  Un aéroport est représenté par son nom
- RG62 :  Un aéroport est représenté par son ville
- RG63 :  Un aéroport est représenté par son pays
```

- **RG64 :**  Un aéroport est associé **à une seule ville**
- **RG65 :**  Un aéroport peut etre associé à **0 ou n vols**
- **RG66 :**  Un aéroport peut peut accueillir **0 ou n escales**


--- 
## Escale 
--- 

``` 
- RG67 :  Une escale est définie par un identifiant unique 
- RG68 :  Une escale est définie par une heure d'arrivée 
- RG69 : Une escale est définie par une heure de départ 
- RG70 : Une escale est définie par sa durée 
- RG71 : Une escale est définie par son type (l'escale technique, l'escale avec changement d'avion et l'escale longue.)
```

- **RG73 :**  une escale est **associée à un unique aeroport** 
- **RG74 :**  une escale est **associée à un vol**
- **RG74 :**  une escale peut etre appartenir **0 ou n reseravtion**



---
## Ville
---
```
- RG75 :  Une ville est représenté par un identifiant unique 
- RG76 :  Une ville est représenté par son nom
- RG77 :  Une ville est représenté par sa région
- RG78 :  Une ville est représenté par son pays
- RG78 :  Une ville est représenté par son code postal
```
- **RG79 :**  Une ville peut avoir **1 ou n aeroports**

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