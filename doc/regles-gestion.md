# Règles de Gestion 
-----------------

## Client 
- **RG1 :**  Un client possède un identifiant unique
- **RG2 :**  Un client possède un nom
- **RG3 :**  Un client possède un prenom
- **RG4 :**  Un client possède un email
----
- **RG5 :**  Un client peut réserver un ou plusieurs vols pour lui même
- **RG6 :**  Un client peut réserver un ou plusieurs vols pour d'autres passagers
- **RG7 :**  Un client peut confirmer une réservation
- **RG8 :**  Un client peut annuler une réservation


## Passager
- **RG9 :**  Un passager possède un identifiant unique
- **RG10 :**  Un passager possède un nom
- **RG11 :**  Un passager possède un prenom
---- 
- **RG12 :** Un passager peut etre associé à plusieurs réservation
- **RG13 :** Un passager n'est pas obligatoirement un client 

## Reservation 
- **RG14 :**  Une réservation possède un identifiant unique
- **RG14 :**  Une réservation possède une date de réservation
- **RG14 :**  Une réservation possède un statut
----
- **RG15 :**  Une réservation est strictement liée à un seul vol
- **RG16 :**  Une réservation est strictement liée à un seul passager
- **RG17 :**  Une réservation peut etre confirmée
- **RG18 :**  Une réservation peut etre annulée

## Vol  
- **RG19 :** Un vol possède un identifiant unique

---

- **RG20 :** Un vol est proposé par une seule compagnie aérienne
- **RG21 :**  Un vol a un aéroport de départ
- **RG22 :** Un vol possède un aéroport d'arrivée
- **RG23 :**  Un vol a un jour de départ
- **RG24 :**  Un vol a une heure de départ
- **RG25 :**  Un vol a un jour d'arrivée
- **RG26 :**  Un vol a une heure d'arrivée
- **RG27 :**  Un vol peut comporter une ou plusieurs escales
- **RG28 :**  Un vol est ouvert à la réservation jusqu'a sa fermeture par une compagnie aérienne

## Escale
- **RG29 :**  Une escale a une heure de départ
- **RG30 :**  Une escale a une heure d'arrivée
---
- **RG31 :**  Une escale est toujours située dans un aéroport

## Aeroport 
- **RG32 :**  Un aéroport possède un identiffiant unique 
- **RG33 :**  Un aéroport possède un nom
- **RG34 :**  Un aéroport se trouve dans une ville
---
- **RG35 :**  Un aéroport dessert une ou plusieurs villes

## Ville 
- **RG36 :**  Une ville possède un id
- **RG37 :**  Une ville possède un nom
- **RG38 :**  Une ville peut posséder un code postal
- **RG39 :**  Une ville possède un pays
----
- **RG40 :**  Une ville peut contenir un ou plusieurs aéroports

## Compagnie aérienne
- **RG41 :**   Une compagnie aériennes possède un id
- **RG42 :**   Une compagnie aériennes possède une nom
----
- **RG43 :**   Une compagnie aériennes peut proposer différents vols
- **RG44 :**   Une compagnie aériennes peut annuler un vol 
- **RG45 :**  Une compagnie aerienne peut fermer la reservation d'un vol ( avant son départ ?)

