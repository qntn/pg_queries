# PROJECT_CONTEXT.md

## Présentation

Ce dépôt rassemble des requêtes SQL pour PostgreSQL, principalement destinées à analyser l'utilisation disque des bases, tables et index, dans un contexte d'audit ou d'optimisation.

## Historique et motivation

Dans la gestion de bases PostgreSQL, il est fréquent de devoir évaluer l'espace utilisé pour anticiper des opérations de maintenance, du dimensionnement ou détecter des dérives de volumétrie. Les requêtes ici présentes correspondent à des besoins rencontrés en production ou en infogérance.

## Structure du projet

- SQL scripts uniquement, pas de code applicatif.
- Pas de gestionnaire de dépendances.
- Peut être directement cloné ou ses fichiers copiés dans des projets d'administration.

## Cas d'usage typiques

- Audit ponctuel d'un cluster Postgres
- Surveiller la croissance des tables volumineuses
- Préparer un plan de migration ou d'archivage
- Comprendre la ventilation (données, index, toast) du stockage

## Public cible

- DBAs
- Ops / DevOps
- Développeurs devant piloter la volumétrie de certaines tables

## Limites

- Les requêtes ne s'adressent qu'à PostgreSQL
- Ne couvrent pas toutes les métriques possibles (par exemple, tablespaces)
- À adapter selon les versions PG, droits, etc.
