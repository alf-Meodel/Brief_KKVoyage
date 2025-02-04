
# Règles de Gestion 
-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Client 
- **RG1 :**  Un client possède un identifiant unique
- **RG2 :**  Un client possède un nom
- **RG3 :**  Un client possède un prenom
- **RG4 :**  Un client possède un email
- **RG5 :**  Un client possède un numéro de téléphone
- **RG6 :**  Un passager possède une nationalité 
- **RG7 :**  Un client possède une adresse 

----
- **RG11 :** Un client choisit son aéroport de départ et d’arrivée lors de la réservation
- **RG8 :**  Un client est celui qui effectue la réservation 
- **RG9 :**  Un client peut réserver un ou plusieurs vols pour lui même
- **RG10 :**  Un client peut réserver un ou plusieurs vols pour d'autres personnes *** 
- **RG11 :**  Un client peut annuler une réservation
- **RG12 :**  Une client n'est pas obligatoirement un passager 


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Personne ( heritage avec passager)
 **RG13 :**  Un personne possède un identifiant unique
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
- **RG23 :**  Un passager possède un identifiant unique
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
- **RG44 :**  Une payement possède un moyen paiement ( paypal stripe cb)
- **RG43 :**  Une payement possède un statut ( en attente validé échoué)
----

- **RG43 :**  un paiement doit etre effectué par un client
- **RG43 :**  Un paiement concerne une seule réservation
- **RG43 :**  un paiement doit etre effectué par un client
- **RG43 :**  un paiement doit etre effectué par un client



-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Vol  
- **RG45 :** Un vol possède un identifiant unique
- **RG46 :** Un vol possède un numéro de vol
- **RG47 :** Un vol possède un statut ( comme les compagnies se donnent le droit d'annuler des vols; En cours, Retardé, Annulé, Terminé )
---

- **RG48:**:  Un vol a une capacité maximale de passagers,
- **RG49 :** Un vol est proposé par une seule compagnie aérienne
- **RG50 :**  Un vol peut comporter des escales techniques 

- **RG51 :**  Un vol a un aéroport de départ
- **RG52 :** Un vol possède un aéroport d'arrivée
- **RG53 :**  Un vol a un jour et une heure de départ
- **RG54 :**  Un vol a un jour et une heure d'arrivée



-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Escale
- **RG56 :**  Une escale possède un identifiant unique 
- **RG57 :**  Une escale possède un type (Technique, Commerciale).
(si l’escale est commerciale, un nouveau vol doit être assigné après l’escale)

---

- **RG58 :**  Une escale technique ne nécessite pas de changement d’avion.
- **RG59 :** Une escale commerciale peut impliquer un changement d’avion et/ou de compagnie
- **RG60 :** Une escale peut être annulée ou modifiée, entraînant un rebooking des passagers
- **RG61 :**  Une escale a une heure de départ
- **RG62 :**  Une escale a une heure d'arrivée
- **RG63 :**  Une escale a une durée estimé 
- **RG64 :**  Une escale s'effectue dans un aéroport

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Aeroport 
- **RG65 :**  Un aéroport possède un identiffiant unique 
- **RG66 :**  Un aéroport possède un nom
- **RG67 :**  Un aéroport se trouve dans une ville

---

- **RG67 :**  Un aéroport peut être desservi par plusieurs compagnies aériennes.


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------


## Ville 
- **RG69 :**  Une ville possède un id
- **RG70 :**  Une ville possède un nom
- **RG71 :**  Une ville peut posséder un code postal
- **RG72 :**  Une ville possède un pays
----
- **RG73 :**  Une ville peut contenir un ou plusieurs aéroports

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Compagnie aérienne
- **RG74 :**   Une compagnie aériennes possède un id
- **RG75 :**   Une compagnie aériennes possède une nom
----
- **RG76 :**   Une compagnie aériennes peut proposer différents vols
- **RG77 :**   Une compagnie aériennes peut annuler un vol 

- **RG78 :** une compagnie aerienne peut ouvrir la reservation d'un vol 
- **RG78 :** une compagnie aerienne peut fermer la reservation d'un vol 

- **RG78 :** Une compagnie aérienne peut desservir plusieurs aéroports.

------------------------

