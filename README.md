# QRT-challenge
Le challenge QRT est une competition de prédiction de résultat de match dont l'objectif est de construire un modèle prédictif riche qui peut fonctionner pour n'importe quelle ligue de football, quel que soit le niveau de compétition ou la situation géographique.
\\
\Description des données
Vous disposerez de données au niveau des équipes et des joueurs pour des dizaines de ligues de football.

Les données sont regroupées dans deux fichiers zip, X_train.zip et X_test.zip, ainsi que dans deux fichiers csv Y_train.csv et Y_train_supp.csv.

Les fichiers zip contiennent les données d'input, qui sont divisées en 4 fichiers csv. Les données sont séparées en HOME et AWAY, au grain des équipes et des joueurs. Toutes les métriques proviennent de matchs historiques réels, agrégés depuis le début de la saison ainsi que sur les 5 derniers matchs précédant le match à prédire.

La colonne ID représente un ID de match et relie les 4 tables du X_train, avec Y_train et Y_train_supp. Il en va de même pour les données de test.

Les ensembles de données d'input pour les équipes comprennent les trois colonnes d'identification suivantes : ID, LEAGUE et TEAM_NAME (notez que LEAGUE et TEAM_NAME ne sont pas inclus dans les données de test).

Vous aurez alors les 25 métriques suivantes, déclinées en somme cumulée, moyenne et écart-type :

'TEAM_ATTACKS'
'TEAM_BALL_POSSESSION'
'TEAM_BALL_SAFE'
'TEAM_CORNERS'
'TEAM_DANGEROUS_ATTACKS'
'TEAM_FOULS'
'TEAM_GAME_DRAW'
'TEAM_GAME_LOST'
'TEAM_GAME_WON'
'TEAM_GOALS'
'TEAM_INJURIES'
'TEAM_OFFSIDES'
'TEAM_PASSES'
'TEAM_PENALTIES'
'TEAM_REDCARDS'
'TEAM_SAVES'
'TEAM_SHOTS_INSIDEBOX'
'TEAM_SHOTS_OFF_TARGET'
'TEAM_SHOTS_ON_TARGET',
'TEAM_SHOTS_OUTSIDEBOX'
'TEAM_SHOTS_TOTAL'
'TEAM_SUBSTITUTIONS'
'TEAM_SUCCESSFUL_PASSES'
'TEAM_SUCCESSFUL_PASSES_PERCENTAGE'
'TEAM_YELLOWCARDS'
Les ensembles de données d'input pour les joueurs comprennent les cinq colonnes d'identification suivantes : ID, LEAGUE, TEAM_NAME, POSITION et PLAYER_NAME (notez que LEAGUE, TEAM_NAME et PLAYER_NAME ne sont pas inclus dans les données de test).

Vous aurez alors les 52 métriques, déclinées en somme cumulée, moyenne et écart-type. Elles sont similaires à celles des équipes bien que plus fines.

Les ensembles de données de sortie sont composés de 4 colonnes :

ID : identifiant unique de match - correspondant aux ID d'input,
HOME_WINS,
DRAW,
AWAY_WINS,
Le score cible est l’accuracy de la prédiction pour les trois classes [HOME_WINS, DRAW, AWAY_WINS], Il existe donc pour un match trois outputs possibles, [1,0,0]. [0,1,0] et [0,0,1].

Nous avons fourni autant de données que possible dans l'ensemble de train, mais toutes les variables ont été normalisées et les noms des équipes, des joueurs et des ligues ont été supprimés de l'ensemble de test. N'utilisiez pas de données externes sous peine de disqualification.

Un exemple de fichier de soumission contenant des prédictions aléatoires est fourni. Il y a également un notebook benchmark que vous trouverez dans les supplementary_files.

Nous avons inclus une autre target d'entraînement GOAL_DIFF_HOME_AWAY, qui est la différence de buts entre l'équipe HOME et AWAY, dans le fichier Y_train_supp.

Disclaimer : Les données fournies sont exclusivement destinées à être utilisées dans le cadre de ce challenge, et toute utilisation de cet ensemble de données à d'autres fins est strictement interdite. Les conditions générales d'utilisation sont applicables : conditions d'utilisation..
