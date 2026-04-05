# pg_queries

Un ensemble de requêtes SQL utiles pour explorer l'espace disque utilisé par une instance PostgreSQL et ses bases/tables.

## Objectif

Fournir des scripts prêts à l'emploi pour obtenir des métriques sur l'occupation disque globale ou par table dans Postgres.

## Contenu

- `get_db_disk_usage.sql` : Affiche l'espace disque utilisé par chaque base de données, avec le propriétaire. Top 20.
- `get_tables_disk_usage.sql` : Affiche l'espace détaillé (total/index/toast/table) pour chaque table (toutes bases), avec un tri par taille.
- `get_tables_disk_usage_simple.sql` : Affiche un aperçu synthétique de l'espace disque par table (top 20).

## Utilisation

1. Connectez-vous à votre instance PostgreSQL avec un outil type psql ou PgAdmin.
2. Importez le fichier SQL souhaité :
   ```
   \i get_db_disk_usage.sql
   ```
   ou copiez son contenu dans votre requête SQL.

3. Adaptez si besoin les limites, le tri ou les filtres (schemas, etc).

## Exemples

```
psql -d votre_base -f get_tables_disk_usage.sql
```

## Licence

Voir le fichier LICENSE.
