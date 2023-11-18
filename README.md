# Projet_2

Projet 2 d'IA pour l'embarqué. Il consistait en l'enregistrement audio des mots rouges, vert, jaunes et noise. 
Dans le tutoriel il était demandé de réaliser au moins 50 échantillons par son. Ici dans un soucis de temps seulement
21 échantillons auront étés fait. 

Résultat du MFCC qui consiste grâce à un :
![image](https://github.com/Cadedius/Projet_2/assets/62182073/91b6fa8e-780d-4537-be77-440f8e9f253d)


Le mélange des points sur le graphe MFCC indique que le modèle de reconnaissance audio rencontre des difficultés à extraire des caractéristiques distinctives à partir des signaux audio ou à distinguer clairement les différentes catégories. 
Cela peut être dû à des similarités acoustiques entre les catégories, à un manque de données d'entraînement ou à un modèle de classification peu performant.

Résultat du NNN Classifier:

![image](https://github.com/Cadedius/Projet_2/assets/62182073/87d01b63-6380-4f8c-ad21-43f31bbef862)

Les résultats du modèle de reconnaissance audio indiquent qu'il y a place à l'amélioration. La précision globale sur l'ensemble de validation est actuellement de 42,9%, ce qui suggère que le modèle peut encore être affiné pour obtenir de meilleures performances.   Le loss est de 1.33 , indique que les prédictions du modèle présentent des divergences significatives par rapport aux étiquettes réelles.

La matrice de confusion révèle des confusions fréquentes entre différentes classes, ce qui nécessite une attention particulière pour l'optimisation du modèle. Par exemple, la classe "NOISE" est correctement classée à 61,9%, mais elle est souvent confondue avec les classes "JAUNE" et "ROUGE".

Les valeurs de F1 Score, qui mesurent l'équilibre entre précision et rappel, varient de 0,09 à 0,55 pour les différentes classes, ce qui indique un besoin d'amélioration globale.

Pour améliorer les performances du modèle, on pourrait comme il était conseillé de faire au moins 50 échantillons, ou jouer avec les paramètres d'entrainement du model. Par exemple on peut améliorer la représentation MFCC dans le modèle de reconnaissance audio, plusieurs paramètres clés peuvent être ajustés. On peut modifier le nombre de coefficients MFCC pour capturer des détails plus fins tout en surveillant la dimensionnalité, ajuster la longueur des trames et leur intervalle pour capturer des caractéristiques à différentes échelles, et jouer avec le nombre de filtres de la banque de filtres de Mel pour influencer la résolution fréquentielle.
De plus, la longueur de la FFT peut être ajustée pour une meilleure résolution, le coefficient de préaccentuation peut être augmenté pour accentuer les hautes fréquences, et la fenêtre de normalisation peut être adaptée pour réduire le bruit. Enfin, l'augmentation de données peut aider à améliorer la généralisation du modèle en introduisant des variations artificielles dans les échantillons audio, et les limites de la plage de fréquence peuvent être ajustées en fonction du contexte audio. 
