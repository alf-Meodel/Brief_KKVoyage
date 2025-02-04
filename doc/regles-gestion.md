# Règles de Gestion 
-----------------
-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Client 
- **RG1 :**  Un client possède un identifiant unique
- **RG2 :**  Un client possède un nom
- **RG3 :**  Un client possède un prenom
- **RG4 :**  Un client possède un email
- **RG4 :**  Un client possède un numéro de téléphone
- **RG11 :**  Un passager possède une nationalité 
- **RG4 :**  Un client possède une adresse 

----
- **RG5 :**  Un client est celui qui effectue la réservation 
- **RG5 :**  Un client peut réserver un ou plusieurs vols pour lui même
- **RG6 :**  Un client peut réserver un ou plusieurs vols pour d'autres personnes *** 
- **RG8 :**  Un client peut annuler une réservation

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Personne ( heritage avec passager)
 **RG9 :**  Un personne possède un identifiant unique
- **RG10 :**  Une personne possède un nom
- **RG11 :**  Une personne possède un prenom
- **RG11 :**  Une personne possède une date de naissance 
- **RG11 :**  Une personne possède une nationalité 
- **RG11 :**  Une personne possède une adresse

-----

- **RG11 :**  Une personne n'est pas obligatoirement un passager 
- **RG11 :**  Une personne n'est pas obligatoirement un client 

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Passager
- **RG9 :**  Un passager possède un identifiant unique
- **RG10 :**  Un passager possède un nom
- **RG11 :**  Un passager possède un prenom
- **RG11 :**  Un passager possède une date de naissance 
- **RG11 :**  Un passager possède une nationalité 
- **RG11 :**  Un passager possède une adresse
---- 

- **RG12 :** Un passager peut etre associé à plusieurs réservation
- **RG13 :** Un passager n'est pas obligatoirement un client 

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Reservation 

- **RG14 :**  Une réservation possède un identifiant unique
- **RG14 :**  Une réservation possède une date de réservation
- **RG14 :**  Une réservation possède un statut
----

- **RG17 add :**  Une réservation est confirmée lors du payement 
- **RG16 :**  Une réservation peut concerner un ou plusieurs passagers 
- **RG18 :**  Une réservation peut etre annulée

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Payement

- **RG14 :**  Une payement possède un identifiant unique
- **RG14 :**  Une payement possède un montant 
- **RG14 :**  Une payement possède une devise 
- **RG14 :**  Une payement possède une date de paiement
(
- **RG14 :**  Une payement possède un statut
- **RG14 :**  Une payement possède un moyen paiement ( paypal stripe cb)) 

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Vol  
- **RG19 :** Un vol possède un identifiant unique
- **RG19 :** Un vol possède un numéro de vol
- **RG19 :** Un vol possède un statut ( comme les compagnies se donnent le droit d'annuler des vols )
---

- **RG20 ADD:**:  Un vol a une capacité maximale de passagers,

- **RG20 ADD:** Un vol peut être retardé ou annulé 
- **RG20 :** Un vol est proposé par une seule compagnie aérienne
- **RG21 :**  Un vol a un aéroport de départ
- **RG22 :** Un vol possède un aéroport d'arrivée
- **RG23 :**  Un vol a un jour et une heure de départ
- **RG25 :**  Un vol a un jour et une heure d'arrivée
- **RG27 :**  Un vol peut comporter une ou plusieurs escales ?? 
- **RG28 :**  Un vol est ouvert à la réservation jusqu'a sa fermeture par une compagnie aérienne

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Escale
- **RG29 :**  Une escale possède un identifiant unique 
- **RG29 :** Si l’escale est commerciale, un nouveau vol doit être assigné après l’escale

- **RG29 :**  Une escale a une heure de départ
- **RG30 :**  Une escale a une heure d'arrivée
- **RG30 :**  Une escale a une durée estimé 

---
- **RG31 :**  Une escale est toujours située dans un aéroport

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

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

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Compagnie aérienne
- **RG41 :**   Une compagnie aériennes possède un id
- **RG42 :**   Une compagnie aériennes possède une nom
----
- **RG43 :**   Une compagnie aériennes peut proposer différents vols
- **RG44 :**   Une compagnie aériennes peut annuler un vol 
- **RG45 :**  Une compagnie aerienne peut fermer la reservation d'un vol ( avant son départ ?)
------------------------







-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------
------------------------------------T E S T -----------------------------------------------
-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------




- **RG17 NOPE :**  Une réservation peut etre confirmée*** - **RG17 NOPE :** via payement ? 

------------------------

- **NOPE :**  Une réservation est strictement liée à un seul vol???  * nn car une reservation peut concerner plusieurs vols ; 
- **NOPE :**  Un client peut confirmer une réservation ??? donc cela signifierais reserver puis devoir faire une autre action en mode t'es sur ? donc cette règl ne peut pas exister 
- **NOPE :**  Une réservation est strictement liée à un seul passager**** nn car quand on fait une reseravtion elle comprend les mmebres de la famille dans la reservation on ne va pas avoir une reservation differente envoyé à chaque personne 

-----------

idées : 

- **RG34 :**  Une escale peut être technique ou commerciale.
- **RG29 :** Si l’escale est technique, les passagers peuvent rester dans l’avion ou être obligés de débarquer pour un contrôle.
- **RG29 :** Une escale peut être effectuée par la même compagnie aérienne ou par une compagnie partenaire.

----- 

Créer une entité personne qui devient passager uniquement si elle est enregistrée sur une reservation 