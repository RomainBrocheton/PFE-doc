# Visualisation 

## Introduction

Ce cas d'usage permet d'afficher sur une carte les résultats de l'analyse de trajectoires dans le but d'en faciliter la lecture. Cette étape affiche ainsi une matrice de carrés (le coté du carré peut être défini). Ces carrés seront [colorés](/doc/ref/files?id=color) en fonction du résultat de l'analyse.

Aussi, il est possible de cliquer sur un carré pour ouvrir une pop-up contenant quelques informations complèmentaires (position GPS, signification de la couleur).

Dans un cas particulier (avec direction), il est possible d'ajouter aux carrés une flêche signifiant la direction du traffic.

## Visualisation manuelle

Les utilisateurs peuvent visualiser les résultats de manière manuelle sur la carte. Pour se faire, ils doivent renseigner la latitude et la longitude centrale, un fichier [Color](/doc/ref/files?id=color) et un fichier [Grid](/doc/ref/files?id=grid).

!> TODO : Ajouter fonctionnement

## Visualisation automatique

Les utilisateurs peuvent charger depuis la base de données et visualiser les résultats de manière automatique sur la carte. Pour se faire, ils doivent choisir dans une arborescence les différents paramètres proposés.

!> TODO : Détailler fonctionnement

Les paramètres sont récupérés grâce à une requête à l'API :

| **Endpoint**  | **Méthode** |**Succès**         |
|---------------|-------------|-------------------|
| `/getCities`  | POST        |`{cities:CITIES}`  |

Le loadout de la requête est le suivant :
```json
{ 
    "token": "<token>"
}
```

Nous affichons ensuite le premier paramètre, puis à chaque nouveau choix, nous filtrons les choix suivants par rapport à ceux déjà faits.