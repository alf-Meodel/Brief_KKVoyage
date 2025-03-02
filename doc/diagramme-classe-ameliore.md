# Améliorations du Diagramme de Classe

## 1. Ajout de la classe Siège

```
+------------------------+
|         Siège          |
+------------------------+
|-siege_id: UUID         |
|-numero_siege: String   |
|-prix: Decimal          |
|-statut: Enum           |
|-classe: Enum           |
|-position: Enum         |
+------------------------+
|+Siege()                |
|+createSiege()          |
|+updateSiege()          |
|+deleteSiege()          |
|+getSiege()             |
|+getAllSieges()         |
|+checkDisponibilite()   |
|+reserverSiege()        |
|+libererSiege()         |
+------------------------+
```

## 2. Relations à ajouter

### Relation Siège-Avion
- Un avion possède plusieurs sièges (composition)
- Cardinalité: 1 Avion - 0..* Sièges
- Ajouter une flèche de composition de Avion vers Siège

### Relation Siège-Passager
- Un passager peut occuper un siège sur un vol
- Cardinalité: 0..1 Passager - 0..* Sièges
- Ajouter une association avec le nom "+occupe" entre Passager et Siège

### Relation Vol-Siège
- Un vol utilise des sièges d'un avion
- Cette relation est indirecte via l'avion, mais peut être utile pour la gestion des réservations

## 3. Attributs manquants à ajouter

### Classe Ville
- Ajouter `-code_postal: String`

### Classe Aéroport
- Ajouter `-pays: String`

### Classe Vol
- Ajouter `-statut: Enum` (ouvert, fermé, annulé)

### Classe Réservation
- Ajouter `-statut: Enum` (confirmée, annulée)

## 4. Méthodes à ajouter

### Classe Siège
- `+checkDisponibilite()`: Vérifier si le siège est disponible
- `+reserverSiege()`: Marquer le siège comme réservé
- `+libererSiege()`: Marquer le siège comme libre

### Classe Vol
- `+ouvrirReservation()`: Ouvrir le vol à la réservation
- `+fermerReservation()`: Fermer le vol à la réservation

## 5. Corrections des cardinalités

### Relation Réservation-Vol
- Selon le brief, "Une réservation concerne un seul vol et un seul passager"
- Modifier la cardinalité de 1..* à 1 du côté Vol

### Relation Réservation-Passager
- Vérifier que la cardinalité est bien 1 du côté Passager

## 6. Diagramme de classe amélioré

Le diagramme de classe amélioré devrait inclure:
- Toutes les classes existantes
- La nouvelle classe Siège
- Les relations corrigées et ajoutées
- Les attributs et méthodes ajoutés

## 7. Bonnes pratiques respectées

- Attributs en private (-)
- Méthodes en public (+)
- Nommage cohérent (camelCase pour les méthodes, snake_case pour les attributs)
- Relations clairement identifiées avec leurs cardinalités
- Séparation des responsabilités entre les classes 