# Dictionnaire de données
-----------------

# Dictionnaire de Données

## 1. Client
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_client        | INT (PK)      | Identifiant unique du client |
| prenom           | VARCHAR(50)   | Prénom du client |
| nom              | VARCHAR(50)   | Nom du client |
| email            | VARCHAR(100)  | Email du client (unique) |
| adresse          | TEXT          | Adresse du client |
| telephone        | VARCHAR(20)   | Numéro de téléphone du client |
| mot_de_passe     | VARCHAR(255)  | Mot de passe du client (hashé) |

## 2. Réservation
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_reservation   | INT (PK)      | Identifiant unique de la réservation |
| pnr              | VARCHAR(20)   | Numéro de réservation unique (PNR) |
| date_reservation | DATE          | Date de la réservation |
| lieu_arrivee     | VARCHAR(100)  | Lieu d'arrivée |
| lieu_depart      | VARCHAR(100)  | Lieu de départ |
| date_arrivee     | DATE          | Date d'arrivée |
| date_depart      | DATE          | Date de départ |
| horaire_emb      | TIME          | Horaire d'embarquement |
| horaire_deb      | TIME          | Horaire de débarquement |
| id_client        | INT (FK)      | Client associé à la réservation |
| id_passager      | INT (FK)      | Passager associé |
| id_vol           | INT (FK)      | Vol associé |

## 3. Passager
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_passager      | INT (PK)      | Identifiant unique du passager |
| document_id      | VARCHAR(50)   | Numéro de passeport ou ID |
| date_naissance   | DATE          | Date de naissance |
| nom             | VARCHAR(50)   | Nom du passager |
| prenom          | VARCHAR(50)   | Prénom du passager |
| adresse         | TEXT          | Adresse du passager |
| nationalite     | VARCHAR(50)   | Nationalité |

## 4. Siège
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_siege         | INT (PK)      | Identifiant unique du siège |
| numero_siege     | VARCHAR(10)   | Numéro du siège |
| prix            | DECIMAL(10,2)  | Prix du siège |
| statut          | BOOLEAN       | Statut (libre/réservé) |
| classe          | ENUM          | Classe du siège (économique, business, première) |
| position        | ENUM          | Position (couloir, fenêtre, milieu) |
| id_avion        | INT (FK)      | Avion associé |
| id_passager     | INT (FK)      | Passager occupant |

## 5. Avion
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_avion         | INT (PK)      | Identifiant unique de l'avion |
| modele          | VARCHAR(50)   | Modèle de l'avion |
| id_compagnie    | INT (FK)      | Compagnie associée |

## 6. Vol
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_vol           | INT (PK)      | Identifiant unique du vol |
| numero_vol       | VARCHAR(20)   | Numéro de vol |
| duree_vol        | TIME          | Durée du vol |
| id_avion        | INT (FK)      | Avion associé |
| id_compagnie    | INT (FK)      | Compagnie aérienne |
| id_aeroport_dep | INT (FK)      | Aéroport de départ |
| id_aeroport_arr | INT (FK)      | Aéroport d'arrivée |
| id_escale       | INT (FK)      | Escale (si applicable) |

## 7. Escale
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_escale        | INT (PK)      | Identifiant unique de l'escale |
| heure_arrivee    | TIME          | Heure d'arrivée |
| heure_depart     | TIME          | Heure de départ |
| duree           | TIME          | Durée de l'escale |
| type_escale     | ENUM          | Type d'escale (technique, changement avion, longue) |
| id_vol          | INT (FK)      | Vol concerné |
| id_aeroport     | INT (FK)      | Aéroport concerné |

## 8. Aéroport
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_aeroport      | INT (PK)      | Identifiant unique de l'aéroport |
| nom_aeroport     | VARCHAR(100)  | Nom de l'aéroport |
| ville           | VARCHAR(100)  | Ville |
| pays            | VARCHAR(100)  | Pays |

## 9. Ville
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_ville         | INT (PK)      | Identifiant unique de la ville |
| nom_ville       | VARCHAR(100)  | Nom de la ville |
| region          | VARCHAR(100)  | Région |
| pays            | VARCHAR(100)  | Pays |

## 10. Compagnie Aérienne
| Nom de l'attribut  | Type          | Description |
|-------------------|--------------|-------------|
| id_compagnie     | INT (PK)      | Identifiant unique de la compagnie |
| nom_compagnie    | VARCHAR(100)  | Nom de la compagnie |

