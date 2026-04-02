# SQL 
## Admin BDD
créer un utilisateur avec mdp 
``` SQL
CREATE USER 'user'@'localhost' IDENTIFIED BY 'mdp';
```
//différentes contraintes pour les comptes : 

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

