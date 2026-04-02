# SQL 
## Admin BDD
créer un utilisateur avec mdp 
``` SQL
CREATE USER 'user'@'localhost' IDENTIFIED BY 'mdp';
```
Différentes contraintes pour les comptes : 

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
Afficher les différents user : 

``` SQL
Select User, Host, Password FROM mysql.user;
```



