-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Client 
```
- RG01 : Un client est représenté par un id unique 
- RG02 : Un client est représenté par son nom
- RG03 : Un client est représenté par son prenom
- RG04 : Un client est représenté par son mail 
```

- **RG05 :** Un client peut réserver un billet pour un vol,
- **RG05 :** Un client peut réserver un billet pour plusieurs vol,

- **RG06 :** Un client peut réserver un billet pour lui même
- **RG07 :** Un client peut réserver un billet pour plusieurs passagers différents.

## Vol
```
- RG01 : Un Vol est représenté par un id unique 
- RG02 : Un Vol est représenté par le nom de sa compagnie 
- RG03 : Un Vol est représenté par le modèle de son avion
```


- **RG04 :** Un Vol est déterminé par son lieux de départ
- **RG04 :** Un Vol est déterminé par sa destination

- **RG04 :** Un Vol est déterminé par sa distance parcourue 

- **RG04 :** Un Vol est déterminé par sa distance parcourue 


---


- **RG08 :** Un vol est ouvert à la réservation et refermé sur ordre de la compagnie.
- **RG09 :** Un vol peut être annulé par la compagnie
- **RG10 :** Un vol a un aéroport de départ et un aéroport d'arrivée.
- **RG11 :** Un vol a un jour et une heure de départ, et un jour et une heure 
d'arrivée.
- **RG12 :** Un vol peut comporter des escales dans des aéroports.

## Reservation 
```
- RG01 :
```
- **RG13 :** Une réservation concerne un seul vol et un seul passager.
- **RG01 :** Une réservation peut être annulée ou confirmée.

## Escale 
```
- RG01 :
```
- **RG01 :** Une escale a une heure d'arrivée et une heure de départ.

## Villes
```
- RG01 :
```
- **RG01 :** Chaque aéroport dessert une ou plusieurs villes.
- **RG01 :** Des compagnies aériennes proposent différents vols.