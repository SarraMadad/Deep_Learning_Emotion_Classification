# Deep_Learning_Emotion_Classification

                                                             Projet DATACAMP
## Introduction

La reconnaissance d’émotions est un secteur en plein essor qui intéresse de nombreux scientifiques du fait de ses difficultés et challenges qui font qu’elle demeure à ce jour un problème non résolu.
Le domaine est vaste, c’est pourquoi, dans le cadre de ce projet, nous allons nous limiter aux émotions dites basiques (du modèle d’Ekman), à savoir : joie, colère, dégoût, tristesse, peur et surprise auxquelles s’ajoute l’absence d’émotion (« neutre »).

Pour parvenir à concevoir un système de reconnaissance d’émotions, de manière générale avec une approche de machine learning, il est souvent convenu de procéder en suivant le pipeline présenté en Figure 1 (voir PDF du sujet).

- Figure 1 – Pipeline conventionnel en reconnaissance automatique d’émotions [2] 

À partir des images d’entrée (a), les points caractéristiques (landmarks) sont détectés et les régions englobantes du visage sont rognées (b), des features géométriques ou de texture sont ensuite extraits (c), les images sont ensuite labélisées à l’aide d’un classifieur entraîné sur les précédents features (d)

## Base de données
La base de données à votre disposition contient des images de différentes personnes, exprimant des émotions basiques (cf. Fig. 2). Une partie de la base sera utilisée pour trouver le meilleur jeu de caractéristiques et entraîner votre modèle de machine learning. Un autre jeu de donnée provenant de la même base,servira uniquement à la phase d’évaluation. Un fichier .csv accompagne chacun des jeux de données. Ces fichiers contiennent les coordonnées 2D des points caractéristiques (cf. Fig. 3) sur
chacun des visages, ainsi que l’émotion exprimée par le sujet dans l’image. La colonne label n’apparaît pas pour les données test.

- Figure 2 (voir PDF du sujet) – Émotions basiques; dans l’ordre, en haut : neutre (0), colère (1), dégoût (3), peur (4)
en bas : joie (5), tristesse (6), surprise (7)

- Figure 3 (voir PDF du sujet) – Points caractéristiques (landmarks) du visage

## Code
Il vous est demandé de proposer une solution en Python pour résoudre le problème de reconnaissance d’émotions avec le modèle de machine learning de votre choix. Pour ce faire vous devez rendre un dossier contenant votre code ainsi qu’un fichier eval.py.
Le fichier eval.py contiendra le code permettant de lire un fichier csv lu en entré, charger votre modèle, prédire les labels sur les données du jeu testset. Les prédictions devront être sauvegardées au format .csv. Le fichier de sortie sera nommé predictions.csv et contiendra une unique colonne nommé prédictions contenant les prédictions faites par votre modèle.

Votre rendu ne doit pas réentrainer le modèle, mais juste évaluer les nouvelles données. Pour faire cela, vous pouvez sauvegarder votre modèle dans un fichier .pickle.
Attention : La méthode de FineTuning d’un modèle pré-entrainé n’est pas autorisé pour ce projet.
