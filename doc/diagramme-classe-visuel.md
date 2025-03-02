# Diagramme de Classe Visuel - KKVoyage

```
                                   +---------------+
                                   |     Ville     |
                                   +---------------+
                                   | -id_ville     |
                                   | -nom_ville    |
                                   | -pays_ville   |
                                   | -region_ville |
                                   | -code_postal  |
                                   +---------------+
                                          ▲
                                          | situer
                                          | 1
                                          |
+---------------+                  +---------------+                  +---------------+
|    Client     |                  |   Aeroport    |                  |  Compagnie    |
+---------------+                  +---------------+                  |   Aerienne    |
| -client_id    |                  | -aeroport_id  |                  +---------------+
| -prenom       |                  | -numero_vol   |                  | -compagnie_id |
| -nom          |                  | -code_iata    |                  | -nom          |
| -email        |                  | -pays         |                  | -code_iata    |
| -adresse      |                  +---------------+                  +---------------+
| -telephone    |                          ▲                                 ▲
| -mot_de_passe |                          | depart                          | possède
+---------------+                          | 1                               | 1
       ▲                                   |                                 |
       | effectue                   +---------------+                  +---------------+
       | 1                          |      Vol      |◄---------------►|     Avion     |
       |                            +---------------+     utiliser    +---------------+
+---------------+                  | -vol_id        |       1:1       | -avion_id     |
| Reservation   |◄---------------►| -numeroVol     |                  | -modele       |
+---------------+     inclut      | -dureeVol      |                  +---------------+
| -reservation_id|      1:1       | -date_depart   |                         ▲
| -numeroRes    |                  | -heure_depart  |                         | contient
| -dateRes      |                  | -date_arrivee  |                         | 1
| -lieu_depart  |                  | -heure_arrivee |                         |
| -lieu_arrivee |                  | -statut        |                  +---------------+
| -date_depart  |                  +---------------+                  |     Siege     |
| -date_arrivee |                          ▲                          +---------------+
| -horaire_emb  |                          | associée à               | -siege_id     |
| -horaire_deb  |                          | 1                        | -numero_siege |
| -statut       |                          |                          | -prix         |
+---------------+                  +---------------+                  | -statut       |
       ▲                           |    Escale     |                  | -classe       |
       | ajouter                   +---------------+                  | -position     |
       | 1                         | -id_escale    |                  +---------------+
       |                           | -heure_arrivee|                         ▲
+---------------+                  | -heure_depart |                         | occupe
|   Passager    |                  | -duree        |                         | 0..1
+---------------+                  | -type         |                         |
| -passager_id  |                  +---------------+                  +---------------+
| -nom          |                                                     |   Passager    |
| -prenom       |                                                     +---------------+
| -adresse      |
| -nationalite  |
| -date_naissance|
| -document_id  |
+---------------+
```

## Légende des relations

- **1** : Relation "un"
- **0..\*** : Relation "zéro à plusieurs"
- **1..\*** : Relation "un à plusieurs"
- **◄---------------►** : Association bidirectionnelle
- **▲** : Direction de la relation

## Principales relations ajoutées ou corrigées

1. **Avion - Siège** : Relation de composition (1 à 0..*) - Un avion contient plusieurs sièges
2. **Passager - Siège** : Relation d'association (0..1 à 0..*) - Un passager peut occuper plusieurs sièges
3. **Vol - Siège** : Relation indirecte via l'avion - Un vol utilise les sièges de l'avion
4. **Réservation - Vol** : Cardinalité corrigée à 1:1 - Une réservation concerne un seul vol
5. **Réservation - Passager** : Cardinalité vérifiée - Une réservation est associée à un seul passager

## Attributs et méthodes ajoutés

1. **Classe Vol** : Ajout de l'attribut "statut" et des méthodes "ouvrirReservation()" et "fermerReservation()"
2. **Classe Réservation** : Ajout de l'attribut "statut"
3. **Classe Ville** : Ajout de l'attribut "code_postal"
4. **Classe Aéroport** : Ajout de l'attribut "pays" 