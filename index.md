## Jakarta

Introduction:

En Indonésie, Jakarta est menacé d'être submergé par l'océan. Cette augmentation de la hauteur du niveau de la mer est fortement dû au changement climatique. Notre projet de recherche va se centrer sur le CO2 et ses répercussions. Nous allons voir si notre temps est compté ou qu'il soit tous simplement trop tard.



### La problématique

L'indonésie est-elle capable de sauver seule sa capitale d'être inondé par l'océan.

# Les méthodes

### CO2 -> Température -> Augmentation de la niveau de l'océan
Augmentation de la hauteur du niveau de l’océan si la température augmentait de deltaT:

Volume de l’océan actuellement : 1,4*10¹⁸*m³
Surface de l’océan =3,6*10¹⁴*m²
alpha :	Dilatation thermique de l'eau =1,7*10-⁴°c-¹

deltaV=alphaVodeltaT

deltaV=Surface*Hauteur

Hauteur=deltaV/Surface

sources
[Link](url)

### L'extraction de données d'une carte topographique

J'ai utilisé la bibliothèque PIL (Python Image Library) pour itérer les pixels d'une image. 

### Traitement de données

Puis j'ai utilisé une fonction pour passer des valeurs de couleur RGB aux valeurs de hauteur. 
Pour cette fonction j'ai pris l'aide d'un ami qui étudie les mathématiques à l'université de bologne en italie.

### L'optimisation

Pour optimiser le procès de création d'image, j'ai transféré les valeurs de hauteur pour chaque pixel dans une matrice numpy.
Comme ça je n'ai pas eu besoin de traiter chaque image, c'était particulièrement utile pour créer ces vidéos où j'ai complètement 
submergé la ville entière car il y avait environ 4000-5000 images par video

### Image finale

Pour les submersions d'images satellites, j'ai utilisé une fonction qui effectue les calculs sur l'image de la carte 
topographique, mais qui effectue ensuite la submersion sur une image satellite que j'ai déplacée et recadrée pour avoir la 
même résolution que la carte.

### Calcul des stats

Pour calculer la surface perdu, j'ai calculé la conversion entre les pixels sur l'image et la distance en réalité avec Google Maps
Et j'ai trouvé que chaque pixel est égale à presque 110m de taille.
Pour calculer le nombre de personnes déplacées j'ai utilisé une carte de la densité de la population de Jakarta.
J'ai créé une fonction qui trouvé le valeur de population pour chaque pixel sur la carte de la population à partir du couleur.
J'ai dû modifier un peu la forme et la taille de la carte pour l'adapter à la carte topographique et à l'image satellite. 

# Les simulations

### Progrès

https://user-images.githubusercontent.com/96302110/163871072-ebc1b22d-22fd-4b11-93c6-d2614113558b.mp4

# Scénarios

![image](https://user-images.githubusercontent.com/96302110/163873648-548cfb65-8b39-4174-8475-3a957431526b.png)

### RPC 4.5: Scénario intermédiaire

Celui-ci est décrit par le GIEC comme le scénario intermédiaire, Les émissions plafonnent vers 2040, puis diminuent.

La variation probable de la prévision du GIEC pour le RPC 4.5 est une augmentation du niveau des océans de 32 à 63 centimètres. 
Avec la valeur p de 0.5 (médiane) correspondant à *53 cm*.

Selon mon programme, cela va résulter en *25.14 km2* de terres submergées par les eaux, et *8,876 personnes* seront déplacées.


### RPC 8.5: Cas extrême

Celui-ci est le scénario dans lequel les émissions continuent d'augmenter tout au long du 21e siècle.

La variation probable de la prévision du GIEC pour le RPC 8.5 est une augmentation du niveau des océans de 45 à 82 centimètres. 
Avec la valeur p de 0.5 (médiane) correspondant à *74 cm*.

Selon mon programme, cela va résulter en *41.62 km2* de terres submergées par les eaux, et *30,276 personnes* seront déplacées.

### EFO 1.0: Régression Linéaire

Nous avons calculé l'augmentation par le régression des données entre 2000 et 2020, 
alors notre prédiction n'est pas complètement en accord avec les prédictions plus fiables du GIEC.

Celui-ci est le scénario dans lequel les émissions continuent linéairement sans aucun change de la trajectoire.

Selon ce scénario, l'eau va augmenter de 4.34m jusqu'à 2100. Et cela va résulter en 719.93 km^2 de terres submergées par les eaux,
et 1,855,484 personnes seront déplacées.

### EFO 2.0: Sans L'Indonésie

Celui-ci est le scénario dans lequel L'Indonésie cesse complètement d'émettre du CO2, dès maintenant.

Selon ce scénario, l'eau va augmenter de 4.28m, une différence de 6 centimètres par rapport à la simulation 1.0. 

Cela va résulter en 713.46 km^2 de terres submergées par les eaux, et 1,826,781 personnes seront déplacées.

Alors indonésie seule peut sauver 6.47 km^2 de terres, et les maisons de 28,703 personnes à Jakarta. Une réduction de 1%.
