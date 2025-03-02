# Dictionnaire de données

-----------------

## 1. Client
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_client        | INT (PK)      | Identifiant unique du client | RG01 |
| prenom           | VARCHAR(50)   | Prénom du client | RG02 |
| nom              | VARCHAR(50)   | Nom du client | RG03 |
| email            | VARCHAR(100)  | Email du client (unique) | RG04 |
| adresse          | TEXT          | Adresse du client | RG05 |
| telephone        | VARCHAR(20)   | Numéro de téléphone du client | RG06 |
| mot_de_passe     | VARCHAR(255)  | Mot de passe du client (hashé) | RG07 |

## 2. Réservation
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_reservation   | INT (PK)      | Identifiant unique de la réservation | RG10 |
| pnr              | VARCHAR(20)   | Numéro de réservation unique (PNR) | RG11 |
| date_reservation | DATETIME      | Date et heure de la réservation | RG12 |
| lieu_arrivee     | VARCHAR(100)  | Lieu d'arrivée | RG13 |
| lieu_depart      | VARCHAR(100)  | Lieu de départ | RG14 |
| date_arrivee     | DATE          | Date d'arrivée | RG15 |
| date_depart      | DATE          | Date de départ | RG16 |
| horaire_embarquement | TIME      | Horaire d'embarquement | RG17 |
| horaire_debarquement | TIME      | Horaire de débarquement | RG18 |
| statut           | ENUM          | Statut de la réservation (confirmée, annulée) | Brief |
| id_client        | INT (FK)      | Client associé à la réservation | RG19 |
| id_passager      | INT (FK)      | Passager associé à la réservation | RG20 |

## 3. Reservation_Vol (Table de liaison)
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_reservation_vol | INT (PK)     | Identifiant unique de la liaison | - |
| id_reservation    | INT (FK)      | Réservation concernée | RG21 |
| id_vol            | INT (FK)      | Vol concerné | RG21 |

## 4. Reservation_Escale (Table de liaison)
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_reservation_escale | INT (PK)  | Identifiant unique de la liaison | - |
| id_reservation    | INT (FK)      | Réservation concernée | RG21 |
| id_escale         | INT (FK)      | Escale concernée | RG21, RG75 |

## 5. Passager
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_passager      | INT (PK)      | Identifiant unique du passager | RG22 |
| document_id      | VARCHAR(50)   | Numéro de passeport ou carte d'identité | RG23 |
| date_naissance   | DATE          | Date de naissance | RG24 |
| nom              | VARCHAR(50)   | Nom du passager | RG25 |
| prenom           | VARCHAR(50)   | Prénom du passager | RG26 |
| adresse          | TEXT          | Adresse du passager | RG27 |
| nationalite      | VARCHAR(50)   | Nationalité | RG28 |

## 6. Passager_Siege (Table de liaison)
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_passager_siege | INT (PK)     | Identifiant unique de la liaison | - |
| id_passager       | INT (FK)      | Passager concerné | RG30 |
| id_siege          | INT (FK)      | Siège concerné | RG30, RG37 |
| id_vol            | INT (FK)      | Vol concerné | RG30 |

## 7. Siège
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_siege         | INT (PK)      | Identifiant unique du siège | RG31 |
| numero_siege     | VARCHAR(10)   | Numéro du siège | RG32 |
| prix             | DECIMAL(10,2) | Prix du siège | RG33 |
| statut           | ENUM          | Statut (libre/réservé) | RG34 |
| classe           | ENUM          | Classe du siège (économique, business, première) | RG35 |
| position         | ENUM          | Position (couloir, fenêtre, milieu) | RG36 |
| id_avion         | INT (FK)      | Avion associé | RG38 |

## 8. Avion
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_avion         | INT (PK)      | Identifiant unique de l'avion | RG39 |
| modele           | VARCHAR(50)   | Modèle de l'avion | RG40 |
| id_compagnie     | INT (FK)      | Compagnie aérienne propriétaire | RG44 |

## 9. Vol
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_vol           | INT (PK)      | Identifiant unique du vol | RG45 |
| numero_vol       | VARCHAR(20)   | Numéro de vol | RG46 |
| duree_vol        | TIME          | Durée du vol | RG47 |
| date_depart      | DATE          | Jour de départ | Brief |
| heure_depart     | TIME          | Heure de départ | Brief |
| date_arrivee     | DATE          | Jour d'arrivée | Brief |
| heure_arrivee    | TIME          | Heure d'arrivée | Brief |
| statut           | ENUM          | Statut du vol (ouvert, fermé, annulé) | Brief |
| id_avion         | INT (FK)      | Avion associé | RG52 |
| id_compagnie     | INT (FK)      | Compagnie aérienne | RG51 |
| id_aeroport_depart | INT (FK)    | Aéroport de départ | RG49, RG50 |
| id_aeroport_arrivee | INT (FK)   | Aéroport d'arrivée | RG49, RG50 |

## 10. Escale
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_escale        | INT (PK)      | Identifiant unique de l'escale | RG68 |
| heure_arrivee    | TIME          | Heure d'arrivée | RG69 |
| heure_depart     | TIME          | Heure de départ | RG70 |
| duree            | TIME          | Durée de l'escale | RG71 |
| type_escale      | ENUM          | Type d'escale (technique, changement avion, longue) | RG72 |
| id_vol           | INT (FK)      | Vol concerné | RG74 |
| id_aeroport      | INT (FK)      | Aéroport concerné | RG73 |
| id_avion         | INT (FK)      | Avion concerné (pour les escales avec changement d'avion) | RG43 |

## 11. Aéroport
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_aeroport      | INT (PK)      | Identifiant unique de l'aéroport | RG61 |
| nom_aeroport     | VARCHAR(100)  | Nom de l'aéroport | RG62 |
| id_ville         | INT (FK)      | Ville associée | RG63, RG65 |
| pays             | VARCHAR(100)  | Pays | RG64 |

## 12. Ville
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_ville         | INT (PK)      | Identifiant unique de la ville | RG76 |
| nom_ville        | VARCHAR(100)  | Nom de la ville | RG77 |
| region           | VARCHAR(100)  | Région | RG78 |
| pays             | VARCHAR(100)  | Pays | RG79 |
| code_postal      | VARCHAR(20)   | Code postal | RG80 |

## 13. Compagnie Aérienne
| Nom de l'attribut  | Type          | Description | Règle de gestion |
|-------------------|--------------|-------------|-----------------|
| id_compagnie     | INT (PK)      | Identifiant unique de la compagnie | RG53 |
| nom_compagnie    | VARCHAR(100)  | Nom de la compagnie | RG54 |
| code_iata        | VARCHAR(3)    | Code IATA de la compagnie | RG55 | 