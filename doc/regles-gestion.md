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
- **RG7 :**  Une réservation possède un identifiant unique

----
- **RG7 :**  Une réservation est strictement liée à un seul vol
- **RG7 :**  Une réservation est strictement liée à un seul passager
- **RG7 :**  Une réservation peut etre confirmée
- **RG7 :**  Une réservation peut etre annulée



## Vol  

- **RG9 :** Un vol possède un identifiant unique

---

- **RG9 :** Un vol est proposé par une seule compagnie aérienne

- **RG9 :**  Un vol a un aéroport de départ
- **RG10 :** Un vol possède un aéroport d'arrivée
- **RG11 :**  Un vol a un jour de départ
- **RG11 :**  Un vol a une heure de départ
- **RG11 :**  Un vol a un jour d'arrivée
- **RG11 :**  Un vol a une heure d'arrivée

- **RG13 :**  Un vol peut comporter une ou plusieurs escales
- **RG14 :**  Un vol est ouvert à la réservation jusqu'a sa fermeture par une compagnie aérienne

## Escale
- **RG15 :**  Une escale a une heure de départ
- **RG16 :**  Une escale a une heure d'arrivée
---
- **RG17 :**  Une escale est toujours située dans un aéroport
- **RG17 :**  Une escale est déclaré dans une reservation ????

## Aeroport 
- **RG18 :**  Un aéroport se trouve dans une ville
- **RG19 :**  Un aéroport a un nom
---
- **RG20 :**  Un aéroport dessert une ou plusieurs villes


## Ville 
- **RG20 :**  Une ville peut contenir un ou plusieurs aéroports

## Compagnie aérienne


- **RG21 :**   Une compagnie aériennes peut proposer différents vols
- **RG22 :**   Une compagnie aériennes peut annuler un vol 
- **RG23 :**  Une compagnie aerienne peut fermer la reservation d'un vol ( avant son départ ?)

