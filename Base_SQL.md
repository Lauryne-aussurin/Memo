#Base SQL
##CREATE TABLE 
- table -> objet qui permet de stocket des données = garantie l'int"grité (= données stockées sont conformes aux règles définient (= contraintes))

### PRIMARY KEY :
Clé primaire :
- jamais vide, toujours unique
- peut inclure un groupe de colonne

### FOREIN KEY :
Clé étrangère :
- garantit que les valeurs d'une colonne correspondent aux valeurs de la colonne d'une autre table

###UNIQUE :
- Garantit que cette donnée est unique dans cette colonne

###NOT NULL :
- Garantit qu'une données n'est pas vide

###CHECK : 
- Satisfait une condition (ex : <5)

Les contraintes permettent de garantir la cohérence et l'intégrité des données de la BD.
Csq : 
- fiabilité de l'information
- prévenir des erreurs
- améliorer la qualité des données
- facilité la maintenance de la DB

##Les jointures : 
Jointure = Combinaison de données entre 2 tables à partir de données communes.

####Syntaxe :
```SQL
SELECT [colonne] FROM [table]
JOIN 
ON [condition];
```

###INNER JOIN :
- Retourne les correspondances entre les 2 tables
####Syntaxe :
```SQL 
SELECT * FROM B INNER JOIN A
ON A.col1 = B.col2;
```
(les deux colonnes sont censées avoir des correspondances)

###LEFT JOIN :
- Retourne les lignes A et B si une correspondance est trouvée
####Syntaxe :
```SQL
SELECT * FROM A LEFT JOIN B
ON A.col = B.col;
```
###RIGHT JOIN :
- Retourne les lignes A et B si une correspondance est trouvée
####Syntaxe :
```SQL
SELECT * FROM A RIGHT JOIN B
ON A.col = B.col;
```
###Avec + de 2 tables :
####Syntaxe :
```SQL
SELECT * FROM A
JOIN (B,C)
ON (A.col = B.col and A.col = C.col);
```
ou 
```SQL
SELECT * FROM A
JOIN B ON A.col = B.col
JOIN C ON A.col = C.col;
```

##AGRÉGATS : 
- S'applique à une seule colonne

###COUNT():
```SQL
SELECT COUNT (*) FROM TABLE;
```

###SUM():
```SQL
SELECT SUM (col) FROM TABLE;
```
AVG() -> Moyenne
MIN() -> Valeur Min
MAX() -> Valeur Max

###GROUPE BY :
- Regroupe 
