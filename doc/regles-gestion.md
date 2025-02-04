
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
- **RG9 :** Un client choisit son aéroport de départ et d’arrivée lors de la réservation
- **RG10 :**  Un client est celui qui effectue la réservation 
- **RG11 :**  Un client peut réserver un ou plusieurs vols pour lui même
- **RG12 :**  Un client peut réserver un ou plusieurs vols pour d'autres personnes *** 
- **RG13 :**  Un client peut annuler une réservation
- **RG14 :**  Une client n'est pas obligatoirement un passager 


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Personne ( heritage avec passager)
 **RG15 :**  Un personne possède un identifiant unique
- **RG16 :**  Une personne possède un nom
- **RG17 :**  Une personne possède un prenom
- **RG18 :**  Une personne possède une date de naissance 
- **RG19 :**  Une personne possède une nationalité 
- **RG20 :**  Une personne possède une adresse

-----
- **RG21 :**  Une personne peut devenir un client si elle effectue une reservation
- **RG22 :**  Une personne peut devenir un passager si elle est incluse dans uen réservation confirmé 
- **RG23 :**  Une personne peut etre client et passager à la fois 
- **RG24 :**  Une personne n'est pas obligatoirement un passager 
- **RG25 :**  Une personne n'est pas obligatoirement un client 


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Passager
- **RG26 :**  Un passager possède un identifiant unique
- **RG27 :**  Un passager possède un nom
- **RG28 :**  Un passager possède un prenom
- **RG29 :**  Un passager possède une date de naissance 
- **RG30 :**  Un passager possède une nationalité 
- **RG31 :**  Un passager possède une adresse

---- 

- **RG32 :** Un passager peut etre associé à plusieurs réservation
- **RG33 :** Un passager n'est pas obligatoirement un client 

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Reservation 

- **RG34 :**  Une réservation possède un identifiant unique
- **RG35 :**  Une réservation possède une date de réservation
- **RG36 :**  Une réservation possède un statut ( en cours, annulé, validé )
----

- **RG37 :**  Une réservation se valide au payement 
- **RG38 :**  Une réservation peut concerner une ou plusieurs personnes 
- **RG39 :**  Une réservation peut etre annulée
- **RG40 :**  Une réservation peut contenir un ou plusieurs vols (vols avec escales).

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Payement

- **RG41 :**  Une payement possède un identifiant unique
- **RG42 :**  Une payement possède un montant 
- **RG43 :**  Une payement possède une devise 
- **RG44 :**  Une payement possède une date de paiement
- **RG45 :**  Une payement possède un moyen paiement ( paypal stripe cb)
- **RG46 :**  Une payement possède un statut ( en attente validé échoué)
----

- **RG47 :**  un paiement doit etre effectué par un client
- **RG48 :**  Un paiement concerne une seule réservation
- **RG49 :**  un paiement doit etre effectué par un client
- **RG50 :**  un paiement doit etre effectué par un client



-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Vol  
- **RG51 :** Un vol possède un identifiant unique
- **RG52 :** Un vol possède un numéro de vol
- **RG53 :** Un vol possède un statut ( comme les compagnies se donnent le droit d'annuler des vols; En cours, Retardé, Annulé, Terminé )
---

- **RG54:**:  Un vol a une capacité maximale de passagers,
- **RG55 :** Un vol est proposé par une seule compagnie aérienne
- **RG56 :**  Un vol peut comporter des escales techniques 

- **RG57 :**  Un vol a un aéroport de départ
- **RG58 :** Un vol possède un aéroport d'arrivée
- **RG59 :**  Un vol a un jour et une heure de départ
- **RG60 :**  Un vol a un jour et une heure d'arrivée



-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Escale
- **RG61 :**  Une escale possède un identifiant unique 
- **RG62 :**  Une escale possède un type (Technique, Commerciale).
(si l’escale est commerciale, un nouveau vol doit être assigné après l’escale)

---

- **RG63 :**  Une escale technique ne nécessite pas de changement d’avion.
- **RG64 :** Une escale commerciale peut impliquer un changement d’avion et/ou de compagnie
- **RG65 :** Une escale peut être annulée ou modifiée, entraînant un rebooking des passagers
- **RG66 :**  Une escale a une heure de départ
- **RG67 :**  Une escale a une heure d'arrivée
- **RG68 :**  Une escale a une durée estimé 
- **RG69 :**  Une escale s'effectue dans un aéroport

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Aeroport 
- **RG70 :**  Un aéroport possède un identiffiant unique 
- **RG71 :**  Un aéroport possède un nom
- **RG72 :**  Un aéroport se trouve dans une ville

---

- **RG73 :**  Un aéroport peut être desservi par plusieurs compagnies aériennes.


-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------


## Ville 
- **RG74 :**  Une ville possède un id
- **RG75 :**  Une ville possède un nom
- **RG76 :**  Une ville peut posséder un code postal
- **RG77 :**  Une ville possède un pays
----
- **RG78 :**  Une ville peut contenir un ou plusieurs aéroports

-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------

## Compagnie aérienne
- **RG79 :**   Une compagnie aériennes possède un id
- **RG80 :**   Une compagnie aériennes possède une nom
----
- **RG81 :**   Une compagnie aériennes peut proposer différents vols
- **RG82 :**   Une compagnie aériennes peut annuler un vol 

- **RG83 :** une compagnie aerienne peut ouvrir la reservation d'un vol 
- **RG84 :** une compagnie aerienne peut fermer la reservation d'un vol 

- **RG85 :** Une compagnie aérienne peut desservir plusieurs aéroports.

------------------------

