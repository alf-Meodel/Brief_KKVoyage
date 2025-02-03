# Règles de Gestion 
-----------------

## Client 

- **RG1 :**  Un client possède un identifiant unique
- **RG1 :**  Un client possède un nom
- **RG1 :**  Un client possède un prenom
- **RG1 :**  Un client possède un mail
----
- **RG2 :**  Un client peut réserver pour lui même
- **RG2 :**  Un client peut réserver pour des passagers différents
- **RG4 :**  Un client peut confirmer une réservation
- **RG3 :**  Un client peut annuler une réservation


## Passager

- **RG1 :**  Un passager possède un identifiant unique
- **RG1 :**  Un passager possède un nom
- **RG1 :**  Un passager possède un prenom
---- 
- **RG5 :** Un passager peut etre associé à plusieurs réservation
- **RG5 :** Un passager n'est pas obligatoirement un client 



## Reservation 



- **RG7 :**  Une réservation concerne un seul vol
- **RG8 :**  Une réservation concerne un seul passager
- **RG6 :** Une réservation est strictement liée à un seul passager

## Vol  
- **RG9 :**  Un vol a un aéroport de départ
- **RG10 :** Un vol possède un aéroport d'arrivée
- **RG11 :**  Un vol a un jour et une heure de départ
- **RG12 :** Un vol a un jour et une heure d'arrivée
- **RG13 :**  Un vol peut comporter des escales dans des aéroports
- **RG14 :**  Un vol est ouvert à la réservation 

## Escale
- **RG15 :**  Une escale a une heure de départ
- **RG16 :**  Une escale a une heure d'arrivée
- **RG17 :**  Une escale se fait dans un aeroport

## Aeroport 
- **RG18 :**  Un aéroport se trouve dans une ville
- **RG19 :**  Un aéroport a un nom
- **RG20 :**  Un aéroport dessert une ou plusieurs villes


## Ville 
- **RG20 :**  Une ville peut possèder plusieurs aéroports

## Compagnie aérienne
- **RG21 :**   Une compagnie aériennes peut proposer différents vols
- **RG22 :**   Une compagnie aériennes peut annuler un vol
- **RG23 :**  Une compagnie aerienne peut fermer la reservation d'un vol 

