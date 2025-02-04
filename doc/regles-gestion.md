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
- **RG05 :** Un client peut réserver une place sur plusieurs vols differents,
---
- **RG05 :** Un client peut réserver plusieurs place sur un vol,
- **RG05 :** Un client peut réserver plusieurs places sur plusieurs vols differents,

---

- **RG05 :** Un client peut réserver une palce pour lui même
- **RG05 :** Un client peut réserver une place pour d'autres passagers

---



## Vol
---
```
- RG08 : Un Vol est représenté par un id unique 
- RG09 : Un Vol est représenté par le nom de sa compagnie 
- RG10 : Un Vol est représenté par le modèle de son avion
```
- **RG15 :** Un Vol possède un nombre de place max
---

- **RG16 :** Un vol doit avoir un jour et une heure de départ,
 - **RG16 :** Un vol doit avoir un jour et une heure 
d'arrivée.
---

- **RG15 :** Un vol est associé à un aéroport de départ 
- **RG15 :** Un vol est associé à un aéroport d'arrivée 

---

- **RG05 :** un vol peut comporter aucune escales
- **RG05 :** un vol peut comporter plusieurs escales

---













## Compagnie Aérienne 
---
```
- RG01 :
```
- **RG12 :**  Une compagnie aérienne ouvre la réservation d'un de ces vol
- **RG12 :**  Une compagnie aérienne ferme les reservations d'un vol.
- **RG09 :** Une compagnie aérienne peut annuler un vol



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
