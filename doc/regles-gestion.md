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

- **RG05 :** Un client peut réserver une place sur un vol,
- **RG06 :** Un client peut réserver une place sur plusieurs vols differents,
---
- **RG07 :** Un client peut réserver plusieurs place sur un vol,
- **RG08 :** Un client peut réserver plusieurs places sur plusieurs vols differents,

---

- **RG09 :** Un client peut réserver une palce pour lui même
- **RG10 :** Un client peut réserver une place pour d'autres passagers

---



## Vol
---
```
- RG011 : Un Vol est représenté par un id unique 
- RG012 : Un Vol est représenté par le nom de sa compagnie 
- RG13 : Un Vol est représenté par le modèle de son avion

- RG14 : Un Vol possède un nombre de place max
```

---

- **RG15 :** Un vol doit avoir un jour et une heure de départ,
 - **RG16 :** Un vol doit avoir un jour et une heure 
d'arrivée.
---

- **RG17 :** Un vol est associé à un aéroport de départ 
- **RG18 :** Un vol est associé à un aéroport d'arrivée 

---

- **RG19 :** un vol peut comporter aucune escales
- **RG20 :** un vol peut comporter plusieurs escales

---

## Compagnie Aérienne 
---
```
- RG01 : Une compagnie aérienne est représenté par un id unique 
- RG01 : Une compagnie aérienne est représenté par son nom

```


- **RG12 :**  Une compagnie aérienne doit posséder au moins un vol
- **RG12 :**  Une compagnie aérienne peut avoir plusieurs vols 

---
- **RG12 :**  Une compagnie aérienne peut proposer des réservations de place sur une vol 
- **RG12 :**  Une compagnie aérienne peut arréter les réservations de place sur un vol
---

- **RG12 :** Une compagnie aérienne propose des vols
- **RG12 :** Une compagnie aérienne peut annuler des vols



<!-- - **RG12 :**  Une compagnie aérienne ouvre la réservation d'un de ces vol -->
<!-- - **RG12 :**  Une compagnie aérienne ferme les reservations d'un vol. -->
<!-- - **RG09 :** Une compagnie aérienne peut annuler un vol -->



## Reservation 
---
```
- RG01 :
```
- **RG13 :** Une réservation concerne un seul vol et un seul passager.
- **RG01 :** Une réservation peut être annulée ou confirmée.

## Escale 
---
```
- RG01 :
```
- **RG01 :** Une escale a une heure d'arrivée et une heure de départ.

## Villes
---
```
- RG01 :
```
- **RG01 :** Chaque aéroport dessert une ou plusieurs villes.
- **RG01 :** Des compagnies aériennes proposent différents vols.
