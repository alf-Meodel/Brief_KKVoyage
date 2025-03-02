# Diagramme de Classe Complet - KKVoyage (Version ASCII)

```
+------------------------+                                +------------------------+
|        Client          |                                |        Passager        |
+------------------------+                                +------------------------+
| -client_id: UUID       |                                | -passager_id: UUID     |
| -prenom_client: String |                                | -nom: String           |
| -nom_client: String    |                                | -prenom: String        |
| -email_client: String  |                                | -adresse: String       |
| -adresse: String       |                                | -nationalite: String   |
| -telephone: String     |                                | -date_naissance: date  |
| -mot_de_passe: String  |                                | -document_identitee: String |
+------------------------+                                +------------------------+
| +Client()              |                                | +Passager()            |
| +createClient()        |                                | +createPassager()      |
| +deleteClient()        |                                | +updatePassager()      |
| +getClient()           |                                | +deletePassager()      |
| +authenticate()        |                                | +getPassager()         |
+------------------------+                                | +getAllPassagers()     |
        |                                                 +------------------------+
        | +effectue                                                | +ajouter
        | 1..*                                                     | 1..*
        v                                                          |
+------------------------+                                         v
|      Reservation       |                                +------------------------+
+------------------------+                                |         Siege         |
| -reservation_id: UUID  |                                +------------------------+
| -numeroReservation: String |                            | -siege_id: UUID       |
| -dateReservation: date |                                | -numero_siege: String |
| -lieu_depart: string   |                                | -prix: Decimal        |
| -lieu_arrivee: string  |                                | -statut: Enum         |
| -date_depart: date     |                                | -classe: Enum         |
| -date_arrivee: date    |                                | -position: Enum       |
| -horaire_embarquement: time |                           +------------------------+
| -horaire_debarquement: time |                           | +Siege()              |
| -statut: Enum          |                                | +createSiege()        |
+------------------------+                                | +updateSiege()        |
| +Reservation()         |                                | +deleteSiege()        |
| +updateReservation()   |                                | +getSiege()           |
| +deleteReservation()   |                                | +getAllSieges()       |
| +getReservation()      |                                | +checkDisponibilite() |
| +calculatePrice()      |                                | +reserverSiege()      |
| +confirmReservation()  |                                | +libererSiege()       |
+------------------------+                                +------------------------+
        |                                                         ^
        | +inclut                                                 | +occupe
        | 1..*                                                    | 0..*
        v                                                         |
+------------------------+                                +------------------------+
|          Vol           |                                |         Avion          |
+------------------------+                                +------------------------+
| -vol_id: Integer       |                                | -avion_id: int         |
| -numeroVol: String     |                                | -modele: string        |
| -dureeVol: Integer     |                                +------------------------+
| -date_depart: date     |                                | +Avion()               |
| -heure_depart: time    |                                | +createAvion()         |
| -date_arrivee: date    |                                | +updateAvion()         |
| -heure_arrivee: time   |                                | +deleteAvion()         |
| -statut: Enum          |                                | +getAvion()            |
+------------------------+                                | +checkDisponibilite()  |
| +Vol()                 |                                | +getCapacite()         |
| +updateVol()           |                                +------------------------+
| +deleteVol()           |                                        |
| +getVol()              |                                        | +contient
| +searchVols()          |                                        | 1
| +checkDisponibilite()  |                                        v
| +calculateDuree()      |                                +------------------------+
| +ouvrirReservation()   |                                |         Siege         |
| +fermerReservation()   |                                +------------------------+
+------------------------+
        |                                                +------------------------+
        | +utiliser                                      |        Escale         |
        | 1                                              +------------------------+
        v                                                | -id_escale: Integer   |
+------------------------+                               | -heure_arrivee: DateTime |
|         Avion          |                               | -heure_depart: DateTime |
+------------------------+                               | -duree: Integer       |
                                                         | -type: String         |
                                                         +------------------------+
+------------------------+                               | +Escale()             |
|       Aeroport         |                               | +updateEscale()       |
+------------------------+                               | +deleteEscale()       |
| -aeroport_id: Integer  |                               | +calculateDureeEscale() |
| -numero_vol: Integer   |                               +------------------------+
| -code_iata: string     |
| -pays: String          |                               +------------------------+
+------------------------+                               |  CompagnieAerienne    |
| +Aeroport()            |                               +------------------------+
| +updateAeroport()      |                               | -compagnie_id: Integer |
| +deleteAeroport()      |                               | -nom: String          |
| +getAeroport()         |                               | -code_iata: String    |
| +searchAeroports()     |                               +------------------------+
+------------------------+                               | +CompagnieAerienne()  |
        |                                                | +createCompagnie()    |
        | +situer                                        | +updateCompagnie()    |
        | 1                                              | +deleteCompagnie()    |
        v                                                | +getCompagnie()       |
+------------------------+                               | +getVolsActifs()      |
|         Ville          |                               | +getProgrammeVols()   |
+------------------------+                               +------------------------+
| -id_ville: Integer     |
| -nom_ville: String     |
| -pays_ville: String    |
| -region_ville: String  |
| -code_postal: String   |
+------------------------+
| +Ville()               |
| +createVille()         |
| +updateVille()         |
| +deleteVille()         |
| +searchVilles()        |
+------------------------+
```

## Relations principales

1. **Client - Réservation**: Un client peut effectuer plusieurs réservations (1..*)
2. **Passager - Réservation**: Un passager peut être ajouté à plusieurs réservations (1..*)
3. **Réservation - Vol**: Une réservation inclut un ou plusieurs vols (1..*)
4. **Vol - Avion**: Un vol utilise un avion (1)
5. **Avion - Siège**: Un avion contient plusieurs sièges (1 à 0..*)
6. **Passager - Siège**: Un passager peut occuper plusieurs sièges (0..1 à 0..*)
7. **Vol - Aéroport**: Un vol a un aéroport de départ (1)
8. **Aéroport - Ville**: Un aéroport est situé dans une ville (1)
9. **Réservation - Escale**: Une réservation peut inclure plusieurs escales (0..*)
10. **Escale - Aéroport**: Une escale est associée à un aéroport (1)
11. **CompagnieAerienne - Vol**: Une compagnie aérienne propose des vols (0..1 à 0..1)
12. **CompagnieAerienne - Avion**: Une compagnie aérienne possède des avions (1 à 0..1)

## Améliorations apportées

1. **Ajout de la classe Siège** avec tous ses attributs et méthodes
2. **Ajout des relations** entre Siège et les autres classes (Avion, Passager, Vol)
3. **Ajout des attributs manquants**:
   - Statut dans la classe Vol
   - Statut dans la classe Réservation
   - Code postal dans la classe Ville
   - Pays dans la classe Aéroport
4. **Ajout des méthodes manquantes**:
   - ouvrirReservation() et fermerReservation() dans la classe Vol
   - reserverSiege() et libererSiege() dans la classe Siège 