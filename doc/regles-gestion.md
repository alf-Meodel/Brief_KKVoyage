# Règles de Gestion 
-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Personne 
- **RG13 :**  Un personne possède un identifiant unique
- **RG14 :**  Une personne possède un nom
- **RG15 :**  Une personne possède un prenom
- **RG16 :**  Une personne possède une date de naissance 
- **RG17 :**  Une personne possède une nationalité 
- **RG18 :**  Une personne possède une adresse

-----
- **RG7 :**  Une personne peut avoir un ou plusieurs rôles (client et/ou passager)
- **RG8 :**  Une personne devient client quand elle effectue une réservation
- **RG9 :**  Une personne devient passager quand elle est incluse dans une réservation confirmée

## Client (role)
- **RG10 :**  Un client doit fournir un email
- **RG11 :**  Un client doit fournir un numéro de téléphone

----
- **RG12 :** Un client choisit son aéroport de départ et d'arrivée lors de la réservation
- **RG13 :**  Un client est celui qui effectue la réservation 
- **RG14 :**  Un client peut réserver un ou plusieurs vols pour lui même
- **RG15 :**  Un client peut réserver un ou plusieurs vols pour d'autres personnes
- **RG16 :**  Un client peut annuler une réservation

## Passager (role)
- **RG17 :**  Un passager doit être associé à une réservation confirmée
- **RG18 :** Un passager peut être associé à plusieurs réservations
- **RG19 :** Un passager doit avoir une nationalité valide pour le vol



-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Reservation 

- **RG20 :**  Une réservation possède un identifiant unique
- **RG21 :**  Une réservation possède une date de réservation
- **RG22 :**  Une réservation possède une date limite de paiement
- **RG23 :**  Une réservation possède un statut (en cours, confirmée, annulée)
----

- **RG24 :**  Une réservation se valide au paiement complet
- **RG25 :**  Une réservation peut concerner une ou plusieurs personnes 
- **RG26 :**  Une réservation peut être annulée selon les conditions suivantes:
              - Avant paiement : sans frais
              - Après paiement : selon les conditions de la compagnie
- **RG27 :**  Une réservation peut contenir un ou plusieurs vols
- **RG28 :**  Une réservation non payée expire après 24h

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Payement

- **RG39 :**  Une paiement possède un identifiant unique
- **RG40 :**  Une paiement possède un montant 
- **RG41 :**  Une paiement possède une devise 
- **RG42 :**  Une paiement possède une date de paiement
- **RG43 :**  Une paiement possède un moyen paiement ( paypal stripe cb)
- **RG44 :**  Une paiement possède un statut ( en attente validé échoué)
----

- **RG45 :**  Un paiement concerne une seule réservation
- **RG46 :**  un paiement doit etre effectué par un client
- **RG47 :**  un paiement est oligatoire pour valider une reservation 


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Vol  
- **RG29 :** Un vol possède un identifiant unique
- **RG30 :** Un vol possède un numéro de vol
- **RG31 :** Un vol possède un statut (Programmé, En cours, Retardé, Annulé, Terminé)
---
- **RG32 :** Un vol peut être récurrent (même numéro pour différentes dates)
- **RG33 :** Un vol a une capacité maximale de passagers
- **RG34 :** Un vol est proposé par une seule compagnie aérienne
- **RG35 :** Un vol peut comporter des escales (techniques ou commerciales)
- **RG36 :** Un vol a un aéroport de départ
- **RG37 :** Un vol possède un aéroport d'arrivée
- **RG38 :** Un vol a un jour et une heure de départ
- **RG39 :** Un vol a un jour et une heure d'arrivée



-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Escale
- **RG58 :**  Une escale possède un identifiant unique 
- **RG59 :**  Une escale possède un type (Technique, Commerciale).
(si l'escale est commerciale, un nouveau vol doit être assigné après l'escale)

---

- **RG60 :**  Une escale technique ne nécessite pas de changement d'avion.
- **RG61 :** Une escale commerciale peut impliquer un changement d'avion et/ou de compagnie
- **RG62 :** Une escale peut être annulée ou modifiée, entraînant un rebooking des passagers
- **RG63 :**  Une escale a une heure de départ
- **RG64 :**  Une escale a une heure d'arrivée
- **RG65 :**  Une escale a une durée estimé 
- **RG66 :**  Une escale s'effectue dans un aéroport
- **RG67 :**  Si une escale est annulée, la réservation des passagers peut être reprogrammée sur un autre vol

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Aeroport 
- **RG68 :**  Un aéroport possède un identiffiant unique 
- **RG69 :**  Un aéroport possède un nom
- **RG70 :**  Un aéroport se trouve dans une ville

---

- **RG71 :**  Un aéroport peut être desservi par plusieurs compagnies aériennes.


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------


## Ville 
- **RG72 :**  Une ville possède un id
- **RG73 :**  Une ville possède un nom
- **RG74 :**  Une ville peut posséder un code postal
- **RG75 :**  Une ville possède un pays
----
- **RG76 :**  Une ville peut contenir un ou plusieurs aéroports

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Compagnie aérienne
- **RG77 :**   Une compagnie aériennes possède un id
- **RG78 :**   Une compagnie aériennes possède une nom
----
Une compagnie aérienne peut modifier la date et l'horaire d'un vol 

- **RG79 :**   Une compagnie aériennes peut proposer différents vols
- **RG80 :**   Une compagnie aériennes peut annuler un vol 

- **RG81 :** une compagnie aerienne peut ouvrir la reservation d'un vol 
- **RG82 :** une compagnie aerienne peut fermer la reservation d'un vol 

- **RG83 :** Une compagnie aérienne peut desservir plusieurs aéroports.

------------------------

