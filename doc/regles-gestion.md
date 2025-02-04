# Règles de Gestion 
-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Client 
- **RG1 :**  Un client possède un identifiant unique
- **RG2 :**  Un client possède un nom
- **RG3 :**  Un client possède un prenom
- **RG4 :**  Un client possède un email
- **RG5 :**  Un client possède un numéro de téléphone
- **RG6 :**  Un client possède une adresse 

----
- **RG7 :** Un client choisit son aéroport de départ et d'arrivée lors de la réservation
- **RG8 :**  Un client est celui qui effectue la réservation 
- **RG9 :**  Un client peut réserver un ou plusieurs vols pour lui même
- **RG10 :**  Un client peut réserver un ou plusieurs vols pour d'autres personnes *** 
- **RG11 :**  Un client peut annuler une réservation
- **RG12 :**  Une client n'est pas obligatoirement un passager 


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
- **RG19 :**  Une personne peut devenir un client si elle effectue une reservation
- **RG20 :**  Une personne peut devenir un passager si elle est incluse dans uen réservation confirmé 
- **RG21 :**  Une personne peut etre client et passager à la fois 
- **RG22 :**  Une personne n'est pas obligatoirement un passager 
- **RG23 :**  Une personne n'est pas obligatoirement un client 


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Passager
- **RG24 :**  Un passager possède un identifiant unique
- **RG25 :**  Un passager possède un nom
- **RG26 :**  Un passager possède un prenom
- **RG27 :**  Un passager possède une date de naissance 
- **RG28 :**  Un passager possède une nationalité 
- **RG29 :**  Un passager possède une adresse

---- 

- **RG30 :** Un passager peut etre associé à plusieurs réservation
- **RG31 :** Un passager n'est pas obligatoirement un client 

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Reservation 

- **RG32 :**  Une réservation possède un identifiant unique
- **RG33 :**  Une réservation possède une date de réservation
- **RG34 :**  Une réservation possède un statut ( en cours, annulé, validé )
----

- **RG35 :**  Une réservation se valide au payement 
- **RG36 :**  Une réservation peut concerner une ou plusieurs personnes 
- **RG37 :**  Une réservation peut etre annulée
- **RG38 :**  Une réservation peut contenir un ou plusieurs vols (vols avec escales).

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Payement

- **RG39 :**  Une payement possède un identifiant unique
- **RG40 :**  Une payement possède un montant 
- **RG41 :**  Une payement possède une devise 
- **RG42 :**  Une payement possède une date de paiement
- **RG43 :**  Une payement possède un moyen paiement ( paypal stripe cb)
- **RG44 :**  Une payement possède un statut ( en attente validé échoué)
----

- **RG45 :**  Un paiement concerne une seule réservation
- **RG46 :**  un paiement doit etre effectué par un client


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Vol  
- **RG47 :** Un vol possède un identifiant unique
- **RG48 :** Un vol possède un numéro de vol
- **RG49 :** Un vol possède un statut ( comme les compagnies se donnent le droit d'annuler des vols; En cours, Retardé, Annulé, Terminé )
---

- **RG50:**:  Un vol a une capacité maximale de passagers,
- **RG51 :** Un vol est proposé par une seule compagnie aérienne
- **RG52 :**  Un vol peut comporter des escales techniques 

- **RG53 :**  Un vol a un aéroport de départ
- **RG54 :** Un vol possède un aéroport d'arrivée
- **RG55 :**  Un vol a un jour et une heure de départ
- **RG56 :**  Un vol a un jour et une heure d'arrivée



-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Escale
- **RG57 :**  Une escale possède un identifiant unique 
- **RG58 :**  Une escale possède un type (Technique, Commerciale).
(si l'escale est commerciale, un nouveau vol doit être assigné après l'escale)

---

- **RG59 :**  Une escale technique ne nécessite pas de changement d'avion.
- **RG60 :** Une escale commerciale peut impliquer un changement d'avion et/ou de compagnie
- **RG61 :** Une escale peut être annulée ou modifiée, entraînant un rebooking des passagers
- **RG62 :**  Une escale a une heure de départ
- **RG63 :**  Une escale a une heure d'arrivée
- **RG64 :**  Une escale a une durée estimé 
- **RG65 :**  Une escale s'effectue dans un aéroport
- **RG66 :**  Si une escale est annulée, la réservation des passagers peut être reprogrammée sur un autre vol

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Aeroport 
- **RG67 :**  Un aéroport possède un identiffiant unique 
- **RG68 :**  Un aéroport possède un nom
- **RG69 :**  Un aéroport se trouve dans une ville

---

- **RG70 :**  Un aéroport peut être desservi par plusieurs compagnies aériennes.


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------


## Ville 
- **RG71 :**  Une ville possède un id
- **RG72 :**  Une ville possède un nom
- **RG73 :**  Une ville peut posséder un code postal
- **RG74 :**  Une ville possède un pays
----
- **RG75 :**  Une ville peut contenir un ou plusieurs aéroports

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Compagnie aérienne
- **RG76 :**   Une compagnie aériennes possède un id
- **RG77 :**   Une compagnie aériennes possède une nom
----
Une compagnie aérienne peut modifier la date et l'horaire d'un vol 

- **RG78 :**   Une compagnie aériennes peut proposer différents vols
- **RG79 :**   Une compagnie aériennes peut annuler un vol 

- **RG80 :** une compagnie aerienne peut ouvrir la reservation d'un vol 
- **RG81 :** une compagnie aerienne peut fermer la reservation d'un vol 

- **RG82 :** Une compagnie aérienne peut desservir plusieurs aéroports.

------------------------

