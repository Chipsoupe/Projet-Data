# Analyse de l'attractivité d'un joueur d'échecs pour un grand tournoi

## Objectif du projet
La scène mondiale des échecs est pleine de profils variés, aux comportements et performances différentes.

L’objectif est de répondre à la question d'un organisateur de grand tournois d'échecs : "Quels joueurs inviter ??"

Pour ce faire, il faudra établir un "Score de fiabilité" des joueurs. Ce score doit prendre en compte non seulement le classement du joueur, mais aussi sa précision de jeu, et son "sens du spectacle".

Au plus ce score est élevé, au plus le joueur est attractif, et donc intéressant à inviter dans le tournoi.

## Workflow du projet
1. **Setup des outils et du fichier .csv** (`top_100_chess_players_2026 - Projet DATA.csv`)
2. **Vérifications et nettoyage** : Vérifs des colonnes manquantes, doublons, ajustements et changements dans les colonnes
3. **Graphiques et visualisations** : Le ELO actuel des joueurs, les styles de jeu qui "dominent" le top 100, corrélation entre le ELO d'un joueur et son winrate, corrélation entre le ELO d'un joueur et sa précision en parties...
4. **Construction du score de fiabilité** : Construction des features(Ecart_Peformance, Regularite, Facteur_Spectacle) et du score composite (Score_Fiabilite = 0.50 × (Elo_Actuel/300) + 0.35 × Regularite + 0.15 × Facteur_Spectacle)
5. **Vérification des hypotèses de départ avec tests**
6. **Conclusion**
7.**Export du dataset clean avec nouvelles features** (`top_100_chess_players_nouvelles_features_clean.csv`.)

## Contenu du dépôt
- `README` : Ce document
- `meilleursjoueurs.ipynb` : notebook principal d’analyse.
- `top_100_chess_players_2026 - Projet DATA.csv` : dataset de base (version brute).
- `top_100_chess_players_nouvelles_features_clean.csv` : dataset nettoyé et enrichi.


## Installations et prérequis
### Environnement requis
- **Python** : version 3.8 ou supérieure
- **Jupyter Notebook** ou **JupyterLab**
- **Git** (pour cloner le repository)

### Librairies Python nécessaires

Le projet utilise les librairies suivantes pour l'analyse et la visualisation :
`pandas` 2.0.0 ou supérieur
`numpy` 1.24.0 ou supérieure
`matplotlib` 3.7.0 ou supérieure

### Installation

#### Cloner le repository
```bash
git clone https://github.com/Chipsoupe/Projet-Data.git
cd Projet-Data