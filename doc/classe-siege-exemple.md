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
           ▲
           |
           | 1
           |
           ▼ 0..*
+------------------------+
|         Avion          |
+------------------------+
|-avion_id: int          |
|-modele: string         |
+------------------------+
|+Avion()                |
|+createAvion()          |
|+updateAvion()          |
|+deleteAvion()          |
|+getAvion()             |
|+checkDisponibilite()   |
|+getCapacite()          |
+------------------------+

        +occupe
+------------------------+     0..*     +------------------------+
|       Passager         |◄----------►|         Siège          |
+------------------------+             +------------------------+ 