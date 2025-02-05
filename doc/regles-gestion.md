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


## Reservation 
---
```
- RG01 : Une Reservation est représenté par un identifiant unique 
- RG01 : Une Reservation possède une date de réservation
```

- **RG13 :** Une réservation concerne un siège
- **RG13 :** Une réservation concerne un seul passager

<!-- - **RG01 :** Une réservation peut être annulée ou confirmée. -->


## Siège
---
```
- RG03 : Un Billet est représenté par son id
- RG03 : Un Billet est représenté par son numéro
- RG03 : Un Billet est représenté par son prix
```
- **RG13 :** Un Billet concerne un seul vol et un seul passager.
- **RG01 :** Un Billet peut être annulée ou confirmée.


## Vol
---
```
- RG011 : Un Vol est représenté par un id unique 
- RG012 : Un Vol est représenté par le nom de sa compagnie 
- RG13 : Un Vol est représenté par le modèle de son avion

- RG14 : Un Vol possède un nombre de places MAX
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


- **RG12 :**  Une compagnie aérienne doit posséder un vol
- **RG12 :**  Une compagnie aérienne peut avoir plusieurs vols 

---
- **RG12 :**  Une compagnie aérienne peut proposer des réservations de place sur une vol 
- **RG12 :**  Une compagnie aérienne peut arréter les réservations de place sur un vol
---

- **RG12 :** Une compagnie aérienne peut proposer des vols
- **RG12 :** Une compagnie aérienne peut supprimer des vols ( annuler) 



<!-- - **RG12 :**  Une compagnie aérienne ouvre la réservation d'un de ces vol -->
<!-- - **RG12 :**  Une compagnie aérienne ferme les reservations d'un vol. -->
<!-- - **RG09 :** Une compagnie aérienne peut annuler un vol -->


---


## Aeroport 
---
```
- RG32 :  Un aéroport possède un identifiant unique
- RG33 :  Un aéroport possède un nom
- RG34 :  Un aéroport se trouve dans une ville
```
- **RG35 :**  Un aéroport acceuille une ou plusieurs compagnies aériennes




---

## Escale 
---
```
- RG01 : Une escale est définie par une heure de départ
- RG01 :  Une escale est définie par heure d'arrivée

```

- **RG31 :**  Une escale peut avoir lieu dans une ville 
- **RG31 :**  Une escale peut avoir lieu dans dans plusieurs villes

---

- **RG31 :**  Une escale peut laisser aux clients le même vol
- **RG31 :**  Une escale peut donner aux clients un nouveau vol




## Villes
---
```
- RG01 :  Une ville possède un id
- RG37 :  Une ville possède un nom
```

- **RG40 :**  Une ville peut contenir un ou plusieurs aéroports

---
---



- **RG01 :** Chaque aéroport dessert une ou plusieurs villes.
- **RG01 :** Des compagnies aériennes proposent différents vols.