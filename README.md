# TP - Modélisation Formelle

Maxime Pitard



## Hypothèses

Pour ce projet j'ai pris des considérations concernant :

la SCS 15, je prend parti que l'accélération n'intervient pas dans le régulateur simplement le moteur prend le max entre l'accélération suggérée par le régulateur et l'accélération de l'utilisateur

la SCS 12 fait parti de la SCS 17



#### 1er modèle [modèle global](tpMaximePitard.html) 

Dans ce modèle la partie incrémentation / décrementation du régulateur n'est pas pris en compte c'est donc pour cela que le commodo ne peut envoyer d'action inc et dec. Ce modèle décrit cependant les cas d'activation / désactivation du régulateur en fonction des différents acteurs.

Pour les actions de l'environnement j'ai rajouté des guards afin de forçer AnimUML à vider l'event pool du controlleur avant de pouvoir envoyer un nouvel évenement

J'ai également rajouter des actions à vide dans le controller stop et start pour éviter des "faux" deadlocks dû à ces Guards.

#### Résultat

SCS vérifiées : 1, 2, 3, 16 & 17 grâce à 4 propriétés LTL



#### 2ème modèle [speedCounter](speedCounter.html) 

Dans ce modèle on bouchonne l'activation et désactivation du calculateur de vitesse. ainsi on peut vérifier le comportement relatif au calcul de la vitesse désirée



#### Résultat

SCS 1 & SCS 6 vérifiées grâce à une propriété LTL
