# Dictionnaire de données
-----------------

| Nom de la colonne | Type | Description |
|-------------------|------|-------------|
| id_client | INTEGER | Identifiant unique du client |
| nom_client | VARCHAR | Nom du client |
| prenom_client | VARCHAR | Prénom du client |
| id_reservation | INTEGER | Identifiant unique de la réservation |
| statut_reservation | VARCHAR | Statut de la réservation (confirmée, annulée) |
| id_vol | INTEGER | Identifiant unique du vol |
| date_depart | TIMESTAMPTZ | Date et heure de départ du vol |
| date_arrivee | TIMESTAMPTZ | Date et heure d'arrivée du vol |
| statut_vol | VARCHAR | Statut du vol (ouvert, fermé, annulé) |
| id_aeroport_depart | INTEGER | Identifiant de l'aéroport de départ |
| id_aeroport_arrivee | INTEGER | Identifiant de l'aéroport d'arrivée |
| nom_aeroport | VARCHAR | Nom de l'aéroport |
| id_ville | INTEGER | Identifiant de la ville desservie |
| nom_ville | VARCHAR | Nom de la ville |
| id_escale | INTEGER | Identifiant unique de l'escale |
| heure_depart_escale | TIMESTAMPTZ | Heure de départ de l'escale |
| heure_arrivee_escale | TIMESTAMPTZ | Heure d'arrivée de l'escale |
| id_compagnie | INTEGER | Identifiant unique de la compagnie aérienne |
| nom_compagnie | VARCHAR | Nom de la compagnie aérienne |
| id_passager | INTEGER | Identifiant unique du passager |
| nom_passager | VARCHAR | Nom du passager |
| prenom_passager | VARCHAR | Prénom du passager | 