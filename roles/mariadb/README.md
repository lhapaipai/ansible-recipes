il n'y a pas de modules spécifiques à MariaDB dans Ansible Galaxy. Les modules MySQL peuvent être utilisés. Essayer d'utiliser les fonctionnalités spécifiques à MySQL peut entraîner des erreurs ou un comportement inattendu. Cependant, il en va de même lorsque vous essayez d'utiliser une fonctionnalité non prise en charge par la version MySQL utilisée.

Actuellement, la collection MySQL dans Ansible Galaxy contient au moins les modules suivants :

- `mysql_db` : gère les bases de données MySQL.
- `mysql_info` : rassemble des informations sur un serveur MySQL.
- `mysql_query `: exécute des requêtes SQL sur MySQL.
- `mysql_replication `: configure et exploite la réplication asynchrone.
- `mysql_user` : crée, modifie et supprime des utilisateurs MySQL.
- `mysql_variables` : gère la configuration MySQL.

```shell
ansible-galaxy collection install community.mysql
```

pour pouvoir utiliser le module mysql, la machine distante à besoin de `python3-pymysql`.