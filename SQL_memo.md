# SQL 
## Admin BDD
### créer un utilisateur avec mdp 
``` SQL
CREATE USER 'user'@'localhost' IDENTIFIED BY 'mdp';
```

### Privilèges du compte : 
``` SQL
GRANT select, show view, lock tables, reload on *.* TO 'user'@'%';
```

### Différentes contraintes pour les comptes : 

```
PASSWORD EXPIRE NEVER
```

```
 WITH MAX_QUERIES_PER_HOUR 50
```

```
ACCOUNT LOCK
```

```
WITH MAX_USER_CONNECTIONS 1
```

### Afficher les différents user : 

``` SQL
Select User, Host, Password FROM mysql.user;
```

### Supprimer un utilisateur : 
``` SQL 
DROP USER 'user'@'%';
```

### Sauvergarder  1 BDD
```
mysqldump --host=127.0.0.1 --user=user --password=user --databases [nom_DB] > [nom_fichier.sql]
``` 

### Utilité fichier .my.cnf : 
Pour chaque user, MariaDB va chercher le fichier pour y appliquer la conf qui est est inscrite dedans.
Se situe ~/.my.cnf -> fichier caché + à la racine du répertoire personnel du user.




